---
title: Vaihtoehtoisen tietovuon määrittäminen suosituksia varten
description: Tässä artikkelissa kerrotaan, miten ympäristö määritetään käyttämällä vaihtoehtoista tietovuota tietojen tarjoamiseksi suosituspalvelulle.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460160"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Vaihtoehtoisen tietovuon määrittäminen suosituksia varten

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten ympäristö määritetään käyttämällä vaihtoehtoista tietovuota tietojen tarjoamiseksi suosituspalvelulle.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Valmiin ja vaihtoehtoisen tietovuon vertailu

Alla oleva kuva esittää ympäristön valmista tietovuota.

![Ympäristön valmis tietovuo](media/reco-out-of-the-box-dataflow-2.png)

Alla oleva kuva esittää vaihtoehtoista tietovuota, jossa yksikkösäilön synkronoinnin erätyö korvataan vaihtoehtoisen tietovuon vaiheilla.

![Ympäristön vaihtoehtoinen tietovuo](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Oletustiedot

- Tässä artikkelissa oletetaan, että ympäristössä on jo otettu käyttöön suosituspalvelu. Lisätietoja on kohdassa [Tuotesuositusten käyttöönotto](enable-product-recommendations.md).
- Tee seuraavat toiminnot, kun käsittelyssä ovat Microsoft Azure Data Lake -tallennustilin tiedostot ja kansiot:

    - Voit käyttää Azure-verkkoportaalin liittymää tai Azure Storage Explorer -sovellusta.
    - Tiedostojen ja kansioiden käsitteleminen aloitetaan **dynamics365-financeandoperations**-säilössä, joka sijaitsee siinä kansiossa, jolle annettiin ympäristön URL-osoitetta vastaava nimi.
    - Jos eristysympäristön nimi on **MyUAT**, ympäristön perus-URL-osoite on `myuat.sandbox.operations.dynamics.com`.
    - Jos samaan tallennustiliin on yhdistetty useita ympäristöjä, jokaisella ympäristöllä on oma juurikansio.

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on täytyttävä, ennen kuin vaihtoehtoisen tietovuon menetelmä voidaan toteuttaa.

### <a name="set-up-microsoft-power-platform"></a>Määritä Microsoft Power Platform

Jos haluat määrittää Microsoft Power Platformin, noudata kohdan [Microsoft Power Platform -integroinnin käyttöönotto](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) ohjeita.

### <a name="install-the-export-to-data-lake-add-in"></a>Vie Data Lakeen -apuohjelman asentaminen

Jos haluat asentaa Vie Data Lake -apuohjelman, seuraa kohdan [Vie Azure Data Lakeen -apuohjelman asentaminen](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ohjeita.

> [!NOTE]
> Merkitse määritysarvot muistiin, koska tarvitset niitä joidenkin seuraavien vaiheiden aikana.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Dynamics 365:een vietävien taulujen määrittäminen

Taulun synkronointia Dynamics 365:stä Azure Data Lake Storageen hallitaan **Vie Data Lakeen** -sivulla. Koska sivulla ei ole tällä hetkellä valikon vaihtoehtoa, vain **järjestelmänvalvojan** käyttöoikeusroolin omaavat käyttäjät voivat avata sen.

Jos haluat määrittää taulut Dynamics 365:een viemistä varten, noudata alla olevia vaiheita.

1. Avaa **Vie Data Lakeen** -sivu, lisää merkkijono `?mi=DataFeedsDefinitionWorkspace` ympäristön perus-URL-osoitteeseen seuraavassa esimerkissä esitetyllä tavalla:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Kopioi **Vie Data Lakeen** -sivulla taulut, jotka mainitaan tämän artikkelin [RetailSales-kuution taulujen luettelo](#list-of-retailsales-cube-tables) -osassa.
1. Laajenna suodatinvaihtoehtojen luettelo **Järjestelmän nimi** -sarakkeessa.
1. Valitse suodatintyypiksi **on yksi seuraavista**. Aseta osoitin tekstiruutuun ja liitä **Vie Data Lakeen** -sivulta kopioitu taululuettelo.
1. Valitse suodatinvaihtoehtojen luettelon alaosassa **Käytä**.
1. Valitse ruudukon kaikki rivit ja valitse sitten **Aktivoi**.

> [!NOTE]
> Ennen siirtymistä seuraavaan vaiheeseen kaikkien rivien tilaksi on päivitettävä **Käynnissä**. Tee vianmääritys ja ratkaise mahdolliset virheet.

### <a name="create-a-synapse-workspace"></a>Synapse-työtilan luominen

Jos sinulla ei ole vielä Synapse-työtilaa, mutta haluat luoda sellaisen, seuraa kohdan [Pika-aloitus: Synapse-työtilan luominen](/azure/synapse-analytics/quickstart-create-workspace) ohjeita.

Azure-resurssit voi pitää järjestyksessä sijoittamalla Data Lake Storage -tili ja Synapse-työtila yhdessä Azuren resurssiryhmään. Voit käyttää uudelleen sitä tallennustiliä, joka luotiin Vie Data Lakeen -apuohjelman asentamisen yhteydessä.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Synapsen tietokannan luominen suoritustietojen käsittelemistä varten

Luo Synapse-työtilan tietokanta Common Data Model -apuohjelman konsolisovelluksen (CDMUtil_ConsoleApp) avulla ja täytä se Data Lake Storagen Common Data Model -taulujen tiedoille. Common Data Model -täydennysohjelmaa kannattaa käyttää kehitysympäristön tietokannan kanssa siltä varalta, että laajennuksia on luotu.

> [!NOTE]
> Seuraavissa vaiheissa oletetaan, että RetailSales-kuutioon ei lisätä laajennuksen tietoja.

Jos haluat luoda tietokannan Synapsessa, noudata alla olevia ohjeita.

1. Siirry kohtaan [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) ja lataa **CDMUtilConsoleApp.zip**-tiedosto alla olevien ohjeiden mukaan.
1. Pura zip-tiedosto paikalliseen kansioon.
1. Avaa **CDMUtil_ConsoleApp.dll.config**-tiedosto tekstieditorissa ja päivitä seuraavat arvot:

    1. Määritä **Vuokraajan tunnus** arvo (Azure-vuokraajan tunnus).
    1. Määritä **käyttöoikeusavaimen** arvo (Data Lake Storage -tilin käyttöoikeusavain).

        1. Avaa Azure-portaalissa tallennustili.
        1. Valitse sivun vasemmanpuoleisessa valikossa **Käyttöoikeusavain**.
        1. Valitse sivun yläosassa **Näytä avaimet**.
        1. Valitse jommankumman avainkentän kopiointipainike ja liitä arvo määritystiedostoon lainausmerkkien väliin.

    1. Määritä **ManifestURL**-arvoksi Azure Data Lake Storagen **Tables.manifest.cdm.json**-tiedoston URL-osoite. Voit hankkia URL-osoitteen hakemalla tiedosto selaamalla Azure-portaalissa, valitsemalla näkymän oikealla puolella oleva ellipsi (**...**) ja valitsemalla sitten **Ominaisuudet**. URL-osoite on ensimmäinen **Yleiskatsaus**-välilehdessä näkyvä ominaisuus.
    1. Määritä Synapse-työtilan valmiin palvelimettoman SQL-poolin yhteysmerkkijonon **TargetDbConnectionString**-arvo.

        1. Valitse Synapse-työtilassa **Hallitse**-välilehti.
        1. Valitse alivalikossa **SQL-poolit**.
        1. Valitse **Valmis**-nimi, jos haluat tarkastella poolin ominaisuuksia.
        1. Valitse ominaisuuksien valintaikkunassa ADO.NET-yhteystyyppi, jota haluat käyttää. Kopioi sitten yhteysmerkkijonon arvo ja liitä se kaksoismerkkien väliin määritystiedostoon.

        > [!NOTE]
        > Sinulla on oltava tietokantojen luontioikeus. Käytön helpottamiseksi kannattaa käyttää **sqladminuser**-järjestelmänvalvojatiliä.

    1. Poista **ProcessEntities**-solmu ja määritä sen arvoksi **tosi** (esimerkiksi `<add key="ProcessEntities" value ="true"/>`).

1. Tallenna ja sulje **CDMUtil_ConsoleApp.dll.config**-tiedosto.
1. Kopioi **EntityList.json**-tiedosto **/Manifest**-hakemistoon.
1. Suorita Komentokehote-ikkunassa **cdmutil_consoleapp.exe**-tiedosto.

> [!NOTE]
> Kun tarkastelet tulosta, näkyvissä tulisi olla 35 entiteettiä/näkymää, vähintään 75 taulua eikä yhtään virhettä.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Data Lake -tallennustilan RetailSales-koostemittojen hakemiston valmisteleminen

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Nykyisen RetailSales-kuution tietojen varmuuskopioiminen Data Lake Storagesta

Helpoin tapa varmuuskopioida nykyiset RetailSales-kuution tiedot on nimetä Data Lake Storagen **RetailSales**-hakemisto uudelleen käyttämällä esimerkiksi nimeä **RetailSales-varmuuskopio**. Tämä menetelmä säilyttää olemassa olevat tiedot mahdollista myöhemmin vaadittavaa vianmääritystä varten.

**/RetailSales**-kuution kansio löytyy seuraavasta sijainnista:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Uuden RetailSales-kansion luominen ja mallitiedoston lataaminen

Voit luoda uuden **RetailSales**-hakemiston ja ladata **model.json**-tiedoston Data Lake Storageen alla mainittujen vaiheiden avulla.

1. Luo uusi tyhjä hakemisto samalla tasolla kuin edellinen hakemisto ja anna sen nimeksi **RetailSales**.
1. Lataa **model.json**-tiedosto uuteen hakemistoon.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Putken luominen RetailSales-kuution tietojen kopioimista varten

Putki lukee RetailSales-kuution näkymät ja vie tiedot Data Lake Storagen .csv-tiedostoihin.

Luo putki RetailSales-kuution tietojen kopioimista varten alla olevien vaiheiden avulla.

1. Valitse Synapse-työtilassa **Integroi**-välilehti.
1. Valitse plusmerkki (**+**) ja valitse sitten **Tuo putkimallista**.
1. Lataa ja valitse [ExportRetailSalesCubeViews.zip-tiedosto](https://aka.ms/reco-alternate-dataflow-files).
1. Valitse SQL-tietokannan linkitetty palvelu.
1. Valitse tallennustilin linkitetty palvelu.
1. Avaa **Kopioi tiedot** -työkalu ja muuta **kansion polun** arvoksi **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Putken suorituksen testaaminen

Putki kannattaa testata käyttämällä vain yhtä näkymää. **RetailSales_RetailMediaTemplateView**-näkymä toimii hyvin, koska siinä on yleensä alle 10 riviä.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Putken ajoittaminen suoritettavaksi toistuvan aikataulun mukaan

Aina, kun putki suoritetaan, tapahtuu Azuren kulutusta. Suorittaminen kannattaa ajoittaa tehtäväksi enintään 48 tunnin välein. Voit suorittaa putken manuaalisesti milloin tahansa, jos tiedot on synkronoitava heti. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Taululuettelo Dynamics 365:stä Data Lake Storageen synkronointia varten

Alla oleva taululuettelo on kaikkien niiden taulujen alijoukko, jotka koko RetailSales-kuutio vaatii. RetailSales-kuution näkymistä vain 15 on suosituspalvelun käytössä. Pakollisten taulujen luettelo suodatettiin vastaavasti.

### <a name="list-of-retailsales-cube-tables"></a>RetailSales-kuution taulujen luettelo

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Luettelo
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- AsiakasLaskuTapahtuma
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Parametriluettelon tarkasteleminen Synapse-putkelle välittämistä varten

Seuraava pilkulla erotettu luettelo sisältää sen RetailSales-kuution näkymät, jossa putki suorittaa valintatoiminnon. Tämän jälkeen tulokset kopioidaan Data Lake Storageen.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Putken parametrin on oltava yhdellä pilkulla erotettujen näkymien nimien luettelo. Välilyöntejä tai rivisyöttöjä ei saa olla.

## <a name="environment-specific-fixes"></a>Ympäristökohtaiset korjaukset

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW-korjaus

**RETAILCHANNELVIEW**-näkymä sisältää kiinteästi koodatun kokonaisluvun, joka edustaa vähittäismyyntikanavatyyppistä organisaatiota. Tyypin todellinen arvo voi muuttua ympäristön tai vuokraajan mukaan.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Päivitä kiinteästi koodattu kokonaisluku seuraavien vaiheiden avulla.

1. Etsi Dynamics 365:ssä verkkokanavan **ChannelID**-arvo.
1. Suorita seuraava kysely SQL Server Management Studion (SSMS) Synapse-tietokantaan liitetyssä esiintymässä.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopioi ensimmäisen sarakkeen (**INSTANCERELATIONTYPE**) arvo ja liitä se näkymän määritykseen.

## <a name="troubleshooting"></a>Vianmääritys

### <a name="pipeline-task-fails"></a>Putken tehtävä epäonnistuu

**CopyData**-tehtävällä tulisi olla 15 putken tehtävän suoritusta. Jos jokin suoritus epäonnistuu, on varmistettava, että kaikki riippuvaiset SQL-objektit ovat olemassa ja että kyselyt suoritetaan. Kaikki riippuvuudet löydetään helpoiten muodostamalla tietokantaan yhteys SSMS:n avulla. Tämän jälkeen voit valita näkymän ja pitää sitä valittuna (tai napsauttaa sitä hiiren kaksoispainikkeella) ja valita sen jälkeen **Luo LUO uuteen ikkunaan**.

Virhesanoma voi sisältää seuraavan tekstin:

- Virhe: Lähdepuolella tapahtui virhe
- Virhe käsiteltäessä ulkoista tiedostoa: Virheiden enimmäismäärä.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Esimerkkiskenaario

Tässä esimerkissä **RetailSales_RetailProductCategory** -tehtävä epäonnistuu, ja näkyviin tulee Virheiden enimmäismäärä -virheen.

Voit tehdä virheenmäärityksen alla olevien vaiheiden avulla.

1. Avaa **EntityList.json**-tiedosto tekstieditorissa (esimerkiksi Visual Studio Code -editorissa).
1. Etsi näkymän määritys **RetailSales_RetailProductCategory**-näkymälle.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Tämä näkymä riippuu vain seuraavasta näkymästä: **RetailProductCategoryView** _. Etsi näkymän määritys _*RetailProductCategoryView**-näkymälle.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Tämä näkymä riippuu seuraavista kolmesta näkymästä: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** ja **RETAILCATEGORYEXPANDED**. Etsi kunkin näkymän määritys ja luetteloi niiden riippuvuudet. Jatka, kunnes näet kaikki riippuvaiset näkymät.

    Tässä on koko luettelo riippuvuuspuun järjestyksessä. Vahvistettavia näkymiä on kolmetoista.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. Luo Excelissä seuraavat 13 **select count(\*) from \<view_name\>** -lauseketta. Suorita nämä lausekkeet SSMS:ssä ja lähetä tulokset tekstiksi. Selaa sitten tuloksia ja tarkista, onko jokin näkymistä epäonnistunut. Alkuperäinen virhe kertoo, että ainakin toinen näkymistä epäonnistuu.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Eräs tapa vahvistaa kohteet on luoda juuresta riippuvainen näkymä, jonka avulla luodaan näkymän määritys SSMS:ssä. Vahvista sitten, että järjestelmässä on Azure Data Lake -tiedostosarake, jonka nimi on **r.filepath**. Tämä sarakkeen tavoitettavuus osoittaa, että tarkastettava näkymä lukee tietoja Data Lake Storagesta.

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
