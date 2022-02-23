---
title: Yhtenäinen tuotekokemus
description: Tässä aiheessa kuvataan tuotetietojen integraatiota Finance and Operations -sovellusten ja Dataversen välillä.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 46f2f846f1259d433630a69f17f7b8db9514e6fa
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680045"
---
# <a name="unified-product-experience"></a>Yhtenäinen tuotekokemus

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Jos liiketoiminnan ekosysteemi muodostuu Dynamics 365 -sovelluksista, kuten Financesta, Supply Chain Managementista ja Salesista, yritykset käyttävät usein näitä sovelluksia tuotetietojen lähteenä. Tämä johtuu siitä, nämä sovellukset muodostavat toimivan tuoteinfrastruktuurin, jota kehittyneet hinnoittelukäsitteet ja tarkat käytettävissä olevan varaston tiedot täydentävät. Jos yritykset käyttävät ulkoista tuotteen elinkaaren hallinta- eli PLM-järjestelmää tuotetietojen lähteenä, he voivat kanavoida tuotteita Finance and Operations -sovelluksista muihin Dynamics 365 -sovelluksiin. Integroitu tuotetietomalli voidaan tuoda yhtenäisen tuotekokemuksen avulla Dataverseen, jolloin kaikki sovelluksen käyttäjät, myös Power Platform -käyttäjät, voivat hyödyntää Finance and Operations -sovelluksista saatavia monipuolisia tuotetietoja.

Salesin tuotetietomalli.

![CE-tuotetietomalli](media/dual-write-product-4.jpg)

Finance and Operations -sovellusten tuotetietomalli.

![Tuotetietomalli Finance and Operationsissa](media/dual-write-products-5.jpg)

Nämä kaksi tuotetietomallia on integroitu Dataversessä seuraavan kuvan osoittamalla tavalla.

![Dynamics 365 -sovellusten tuotetietomalli](media/dual-write-products-6.jpg)

Tuotteiden kaksoiskirjoituksen taulukartat on suunniteltu vain yksisuuntaista tiedonkulkua varten, ja tieto kulkee Finance and Operations -sovelluksista Dataverseen lähes reaaliaikaisesti. Tuoteinfrastruktuuri on kuitenkin avoin, joten se voidaan tarvittaessa muuttaa kaksisuuntaiseksi. Vaikka voit mukauttaa sitä omalla vastuullasi, Microsoft ei suosittele tätä lähestymistapaa.

## <a name="templates"></a>Mallit

Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot. Seuraava taulukko osoittaa, miten taulukarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.

Finance and Operations -sovellukset | Muut Dynamics 365 -sovellukset | kuvaus
-----------------------|--------------------------------|---
Vapautetut tuotteet V2 | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails**-yksikkö sisältää ne Finance and Operations -sovellusten kentät, jotka määrittävät tuotteen ja jotka sisältävät tuotteen taloudelliset ja hallinnolliset tiedot. 
Dataversen vapautetut erilliset tuotteet | Tuote | **Tuote**-yksikön kentät määrittävät tuotteen. Se sisältää yksittäisiä tuotteita (tuotteita, joissa on alatyypin tuote) ja tuotevariantteja. Yhdistämismääritykset ovat seuraavassa taulukossa.
Tuotenumeron viivakoodi | msdyn\_productbarcodes | Tuotteen viivakoodeja käytetään tuotteiden yksilöimiseen.
Tilauksen oletusasetukset | msdyn\_productdefaultordersettings
Tuotekohtaiset oletustilausasetukset | msdyn_productdefaultordersettings
Tuotedimension ryhmät | msdyn\_productdimensiongroups | Tuotedimensioryhmä määrittää, mitkä tuotedimensiot määrittävät tuotteet. 
Varastodimensioryhmät | msdyn\_productstoragedimensiongroups | Tuotteen varastodimensioryhmä ilmaisee menetelmän, jolla tuotteiden sijoittaminen varastoon määritetään.
Seurantadimensioryhmät | msdyn\_producttrackingdimensiongroups | Tuotteen seurantadimensioryhmä ilmaisee menetelmän, jolla varastossa olevia tuotteita seurataan.
Värit | msdyn\_productcolors
Koot | msdyn\_productsizes
Tyylit | msdyn\_productsytles
Konfiguroinnit | msdyn\_productconfigurations
Päätuotteen värit | msdyn_sharedproductcolors | **Jaettu tuoteväri** -yksikkö ilmaisee värit, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
Päätuotteen koot | msdyn_sharedproductsizes | **Jaettu tuotekoko** -yksikkö ilmaisee koot, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
Päätuotteen tyylit | msdyn_sharedproductstyles | **Jaettu tuotetyyli** -yksikkö ilmaisee tyylit, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
Päätuotteen konfiguraatiot | msdyn_sharedproductconfigurations | **Jaettu tuotekonfiguraatio** -yksikkö ilmaisee konfiguraatiot, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Dataverseen, jotta tiedot pysyvät yhdenmukaisina.
Kaikki tuotteet | msdyn_globalproducts | Kaikkien tuotteiden yksikkö sisältää kaikki tuotteet, jotka ovat käytettävissä Finance and Operations -sovelluksessa – siis sekä vapautetut tuotteet että tuotteet, joita ei ole vapautettu.
Yksikkö | uoms
Yksikkömuunnokset | msdyn_ unitofmeasureconversions
Tuotekohtainen mittayksikön muunnos | msdyn_productspecificunitofmeasureconversion
Tuoteluokat | msdyn_productcategories | Kukin tuoteluokka sekä tiedot sen rakenteesta ja ominaisuuksista sisältyy tuoteluokkayksikköön. 
Tuoteluokkahierarkiat | msdyn_productcategoryhierarhies | Tuotehierarkioiden avulla luokittelet tai ryhmittelet tuotteita. Luokkahierarkiat ovat käytettävissä Dataversessä tuoteluokkahierarkiayksikön avulla. 
Tuoteluokkahierarkian roolit | msdyn_productcategoryhierarchies | Tuotehierarkioita käytetään D365 Finance and Operationsin eri rooleissa. Kussakin roolissa käytettävä luokkaa määritetään tuoteluokkahierarkiayksikön avulla. 
Tuoteluokan määritykset | msdyn_productcategoryassignments | Tuote voidaan määrittää luokkaan tuoteluokan määritysyksikön avulla.

## <a name="integration-of-products"></a>Tuotteiden integrointi

Tässä mallissa tuotetta vastaa kahden Dataversen taulun yhdistelmä: **tuote** ja **msdyn\_sharedproductdetails**. Siinä missä ensimmäinen yksikkö sisältää tuotteen määritelmän (tuotteen yksilöivän tunnisteen, tuotteen nimien ja kuvauksen), toinen yksikkö sisältää tuotetasolla tallennetut kentät. Tuote määritetään näiden kahden taulun yhdistelmällä varastointiyksikkö (SKU) -käsitteen mukaisesti. Kunkin julkaistun tuotteen tiedot ovat näissä tauluissa (tuote ja jaetut tuotetiedot). Kaikkia tuotteita (julkaistuja ja julkaisemattomia) voidaan seurata **Tuotteet yleisesti** -yksikön avulla. 

Koska tuote ilmaista varastointiyksikkönä, käsitteet erilliset tuotteet, päätuotteet ja tuotevariantit voidaan tallentaa Dataverseen seuraavasti:

- **Tuotteet, joissa on alatyypin tuote** ovat itsensä määrittäviä tuotteita. Dimensioita ei tarvitse määrittää. Tällainen tuote on esimerkiksi tietty kirja. Näille tuotteille luodaan yksi tietue **Tuote**-yksikössä ja yksi tietue **msdyn\_sharedproductdetails**-yksikössä. Tuoteperhetietuetta ei luoda.
- **Päätuotteita** käytetään yleisinä tuotteina, joissa olevat säännöt ja määritelmä määrittävät liiketoimintaprosessien toiminnan. Näiden määritelmien perusteella voidaan luoda tuotevarianteiksi kutsuttuja erillisiä tuotteita. Esimerkiksi t-paita on päätuote, jonka dimensioita väri ja koko voivat olla. Julkaistavissa varianteissa voi olla erilaisia dimensioyhdistelmiä, kuten s-kokoinen sininen t-paita tai m-kokoinen vihreä t-paita. Integroinnissa tuotetauluun luodaan kullekin variantille yksi tietue. Tämä tietue sisältää varianttikohtaiset tiedot, kuten eri dimensiot. Tuotteen yleiset tiedot tallennetaan **msdyn\_sharedproductdetails**-yksikköön. (Nämä yleiset tiedot on tallennettu päätuotteeseen.) Päätuotteen tiedot synkronoidaan Dataverseen heti, kun vapautettu päätuote luodaan (mutta ennen varianttien vapauttamista).
- **Erillisillä tuotteilla** tarkoitetaan kaikkia tuotteiden alatyypin tuotteita ja kaikkia tuotevariantteja. 

![Tuotteiden tietomalli](media/dual-write-product.png)

Kun kaksoiskirjoitustoiminto on käytössä, Finance and Operationsin tuotteet synkronoidaan muissa Dynamics 365 -tuotteissa **Luonnos**-tilassa. Ne lisätään ensimmäiseen hinnastoon, jossa on sama valuutta. Ne siis toisin sanoen lisätään ensimmäiseen Dynamics 365 -sovelluksen hinnastoon, joka vastaa sen yrityksen valuuttaa, jossa tuote vapautetaan Finance and Operations -sovelluksessa. 

Finance and Operations -sovellusten oletustuotteet synkronoidaan muihin Dynamics 365 -sovelluksiin **Luonnos**-tilassa. Jos haluat synkronoida **Aktiivinen**-tilassa olevan tuotteen, jotta sitä voi käyttää esimerkiksi suoraan myyntitilauksen tarjouksissa, seuraavat asetukset on valittava: valitse ensin **Järjestelmä> Hallinto > Järjestelmän hallinta > Järjestelmäasetukset > Sales**-välilehti ja sitten **Luo tuotteet aktiivisessa tilassa = kyllä**. 

Huomaa, että tuotteet synkronoidaan Finance and Operations -sovelluksista Dataverseen. Tämän vuoksi tuoteyksikkökenttien arvot voidaan muuttaa Dataversessa, mutta kun synkronointi käynnistyy (tuotekenttää muokataan Finance and Operations -sovelluksessa), se korvaa Dataversen arvot. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Tuotedimensiot 

Tuotedimensiot ovat ominaisuuksia, joilla voidaan tuotevariantti tunnistetaan. Neljä tuotedimensiota (väri, koko, tyyli ja konfiguraatio) yhdistetään myös Dataverseen määrittämää tuotevariantteja. Seuraavassa kuvassa on Väri-tuotedimension tietomalli. Samaa mallia käytetään myös kokojen, tyylien ja konfiguraatioiden osalta. 

![Tuotedimensioiden tietomalli](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Kun tuotteella on erilaisia tuotedimensioita (esimerkiksi koko ja väri ovat päätuotteen tuotedimensioita), kukin erillinen tuote (toisin sanoen kukin tuotevariantti) määritetään kyseisten tuotedimensioiden yhdistelmänä. Esimerkiksi tuotenumero B0001 on XS-kokoinen musta t-paita, ja tuotenumero B0002 on S-kokoinen musta t-paita. Tässä tapauksessa määritetään aiemmin luodut tuotedimensioyhdistelmät. Esimerkiksi edellisen esimerkin t-paita voi olla XS-kokoinen ja musta, S-kokoinen ja musta, M-kokoinen ja musta tai L-kokoinen ja musta mutta se ei voi olla XL-kokoinen ja musta. Päätuotteessa käytettävät tuotedimensiot on siis määritetty, ja variantit voidaan vapauttaa näiden arvojen perusteella.

Päätuotteen käytössä olevien tuotedimensioiden seuraamista varten on luotu seuraavat taulut, jotka on yhdistetty kunkin tuotedimension osalta Dataverseen. Lisätietoja on kohdassa [Tuotetietojen yleiskatsaus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Tilauksen oletusasetukset ja tuotekohtaiset tilauksen oletusasetukset

Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Näitä tietoja voidaan käyttää Dataversessa käyttämällä tilauksen oletusasetusten ja tuotekohtaisen tilauksen oletusasetusten yksikön avulla. Lisätietoja toiminnosta on kohdassa [Tilauksen oletusasetukset](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mittayksikkö ja mittayksikön muunnokset

Mittayksikkö ja sen muunnos ovat käytettävissä Dataversessa seuraavassa kuvassa olevan tietomallin mukaisesti.

![Mittayksikön tietomalli](media/dual-write-product-three.png)

Mittayksikkökäsite on integroitu Finance and Operations- ja muiden Dynamics 365 -sovellusten välillä. Kullekin Finance and Operations -sovelluksen yksikköluokalle luodaan Dynamics 365 -sovelluksessa yksikköryhmä, joka sisältää yksikköluokkaan kuuluvat yksiköt. Jokaiselle yksikköryhmälle luodaan myös oletusarvoinen perusyksikkö. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Vastaavien yksiköiden tietojen ensimmäinen synkronointi Finance and Operationsin ja Dataversen välillä

### <a name="initial-synchronization-of-units"></a>Yksiköiden ensimmäinen synkronointi

Kun kaksoiskirjoitus on otettu käyttöön, Finance and Operations -sovellusten yksiköt synkronoidaan muihin Dynamics 365 -sovelluksiin. Finance and Operations -sovelluksista Dataversessä synkronoiduilla yksikköryhmillä on merkintäjoukko, joka ilmaisee niiden olevan ulkoisesti ylläpidettyjä.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finance and Operations- ja muiden Dynamics 365 -sovellusten yksiköiden ja yksikköluokkien tai -ryhmien täsmäyttäminen

Ensinnäkin on tärkeää huomata, että yksikön integrointiavain on msdyn_symbol. Tämän vuoksi tämän arvon on oltava yksilöivä Dataversen tai muun Dynamics 365 -sovelluksen arvo. Koska muissa Dynamics 365 -sovelluksissa Yksikköryhmän tunnus- ja Nimi-pari määrittää yksikön yksilöllisyyden, Finance and Operations -sovellusten ja Dataversen yksikkötietojen täsmäyttämisessä on otettava huomioon erilaisia skenaarioita.

Finance and Operations -sovellusten ja muiden Dynamics 365 -sovellusten samanlaiset tai päällekkäiset yksiköt:

+ **Yksikkö kuuluu johonkin muun Dynamics 365 -sovelluksen yksikköryhmään, joka vastaa Finance and Operations -sovellusten liitettyä luokkaa**. Tässä tapauksessa muiden Dynamics 365 -sovellusten kenttään msdyn_symbol on täytettävä Finance and Operations -sovellusten yksikkösymboli. Tämän vuoksi tietoja täsmäytettäessä yksikköryhmä määritetään ulkoisesti ylläpidetyksi muissa Dynamics 365 -sovelluksissa.
+ **Yksikkö kuuluu johonkin muun Dynamics 365 -sovelluksen yksikköryhmään, joka ei vastaa Finance and Operations -sovellusten liitettyä luokkaa (Finance and Operations -sovelluksissa ei ole aiemmin luotua yksikköluokkaa muiden Dynamics 365 -sovellusten yksikköluokalle)**. Tässä tapauksessa kenttään msdyn_symbol on täytettävä satunnainen merkkijono. Huomaa, että tämän arvon on oltava yksilöivä muissa Dynamics 365 -sovelluksissa.

Finance and Operationsin yksiköitä ja yksikköluokkia ei ole muissa Dynamics 365 -sovelluksissa:

Kaksoiskirjoituksen osana Finance and Operations -sovellusten yksikköryhmät ja niitä vastaavat yksiköt luodaan ja synkronoidaan muissa Dynamics 365 -sovelluksissa ja Dataversessä. Lisäksi yksikköryhmä määritetään ulkoisesti ylläpidetyksi. Ylimääräisiä käynnistystoimia ei tarvita.

Muiden Dynamics 365 -sovellusten yksiköitä ei ole Finance and Operations -sovelluksissa:

Kaikkien yksiköiden kenttä msdyn_symbol on täytettävä. Yksiköt voidaan aina luoda Finance and Operations -sovellusten vastaavassa yksikköluokassa (jos sellainen on). Jos yksikköluokkaa ei ole, muiden Dynamics 365 -sovellusten yksikköryhmää vastaava ensimmäinen yksikköluokka on luotava. (Huomaa, että Finance and Operations -sovelluksissa ei voi luoda yksikköluokkaa muuten kuin laajentamalla, jos luettelointia laajennetaan.) Voit luoda sitten yksikön. Huomaa, että Finance and Operations -sovellusten yksikkösymbolin on oltava se msdyn_symbol, joka määritettiin yksikölle aiemmin muissa Dynamics 365 -sovelluksissa.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Tuotekäytännöt: dimensio-, seuranta- ja varastoryhmät

Tuotekäytännöt ovat käytäntöjoukkoja, jolla määritetään varaston tuotteet ja niiden ominaisuudet. Tuotedimensioryhmää, tuotteen seurantadimensioryhmää ja varastodimensioryhmää voi etsiä tuotekäytäntöinä. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Tuotehierarkiat

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Tuotteiden integrointiavain 

Dynamics 365 for Finance and Operationsin ja Dataversen väliseen tuotteiden yksilöivään tunnistamiseen käytetään integrointiavaimia. Tuotteiden **(productnumber)** on yksilöivä avain, jolla tuote tunnistetaan Dataversessa. Se muodostetaan seuraavasta ketjutuksesta: **(yritys, msdyn_productnumber)**. **Yritys** ilmaisee Finance and Operationsin yrityksen, kun taas **msdyn_productnumber** ilmaisee tietyn tuotteen tuotenumeron Finance and Operationsissa. 

Muiden Dynamics 365 -sovellusten käyttäjät tunnistavat tuotteen käyttöliittymässä kentän **msdyn_productnumber** mukaan. (Huomaa, että kentän otsikko on **Tuotenumero**.) Tuotelomakkeessa näkyy sekä yritys että msydn_productnumber. (productnumber)-kenttää eli tuotteen yksilöivää avainta ei kuitenkaan näytetä. 

Jos muodostat sovelluksia Dataversessä, kiinnitä huomiota **productnumber**-kohdan (tuotteen yksilöivä tunnus) käyttämiseen integrointiavaimena. Älä käytä **msdyn_productnumber**-arvoa, koska se ei ole yksilöllinen. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Tuotteiden ensimmäinen synkronointi ja tietojen siirtäminen Dataversesta Finance and Operationsiin

### <a name="initial-synchronization-of-products"></a>Tuotteiden ensimmäinen synkronointi 

Kun kaksoiskirjoitus on otettu käyttöön Finance and Operations -sovellusten tuotteet synkronoidaan Dataverseen ja muiden Dynamics 365:n mallipohjaisten sovellusten kanssa. Dataversessä ja muissa Dynamics 365 -sovelluksissa ennen kaksoiskirjoituksen julkaisua luotuja tuotteita ei päivitetä eikä täsmäytetä Finance and Operations -sovellusten tuotetietojen kanssa.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Tuotetietojen täsmäyttäminen Finance and Operationsista ja muista Dynamics 365 -sovelluksista

Jos samat tuotteet säilytetään (päällekkäiset tai vastaavat) Finance and Operationsissa sekä Dataversessä ja muissa Dynamics 365 -sovelluksissa, kun kaksoiskirjoitusta otetaan käyttöön, Finance and Operationsin tuotteiden synkronointi tehdään ja Dataversessa näkyy saman tuotteen tietueiden kaksoiskappaleita.
Jotta näin ei tapahtuisi siinä tapauksessa, että muissa Dynamics 365 -sovelluksissa on tuotteita, jotka ovat päällekkäisiä tai vastaavia kuin Finance and Operationsin tuotteet, kaksoiskirjoituksen käyttöönottavan järjestelmänvalvojan on käynnistettävä kentät **Yritys** (esimerkki: USMF) ja **msdyn_productnumber** (esimerkki: 1234:Black:S), ennen kuin tuotteet synkronoidaan. Toisin sanoen näiden kahden Dataversen tuotteen kenttiin on täytettävä se Finance and Operationsin yritys, johon tuote on täsmäytettävä, ja sen tuotenumero. 

Kun synkronointi sitten otetaan käyttöön ja sitä käytetään, Finance and Operationsin tuotteet synkronoidaan vastaaviin Dataversen ja muiden Dynamics 365 -sovellusten tuotteisiin. Tämä koskee sekä erillisiä tuotteita että tuotevariantteja. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Tuotetietojen siirtäminen täsmäyttäminen muista Dynamics 365 -sovelluksista Finance and Operationsiin

Jos muissa Dynamics 365 -sovelluksissa on tuotteita, joita ei ole Finance and Operationsissa, järjestelmänvalvoja voi tuoda kyseiset tuotteet Finance and Operationsiin käyttämällä kohdetta **EcoResReleasedProductCreationV2Entity**. Sitten tuotetiedot on täsmättävä Finance and Operationsista ja muista Dynamics 365 -sovelluksista edellä kuvatulla tavalla. 
