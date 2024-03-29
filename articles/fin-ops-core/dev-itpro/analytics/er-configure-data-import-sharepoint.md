---
title: Tietojen SharePointista tuonnin määrittäminen
description: Tässä artikkelissa käsitellään tietojen tuominen Microsoft SharePointista.
author: kfend
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 11208267de0cc35db55c64ccf2de224df854404d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277783"
---
# <a name="configure-data-import-from-sharepoint"></a>Tietojen SharePointista tuonnin määrittäminen

[!include[banner](../includes/banner.md)]

Tietojen tuominen saapuvasta tiedostosta käyttämällä sähköisen raportoinnin (ER) kehystä: on määritettävä ER-muoto, joka tukee tuontia, ja sitten suorittaa mallin määritys **Kohteeseen**-tyypille, joka käyttää kyseistä muotoa tietolähteenä. Tietojen tuomiseksi siirry tiedostoon, jonka haluat tuoda. Käyttäjä voi valita manuaalisesti saapuvan tiedoston. Uuden sähköisen raportoinnin ominaisuuden kanssa, joka tukee tietojen tuomista Microsoft SharePointista, tämä prosessi voidaan määrittää automaattiseksi. Voit käyttää ER-määrityksiä suorittaaksesi tietojen tuonnin tiedostoista, jotka on tallennettu Microsoft SharePoint -kansioihin. Tässä artikkelissa kerrotaan, miten voit viimeistellä tuonnin SharePointista. Esimerkissä käytetään toimittajatapahtumia liiketoimintatietoina.

## <a name="prerequisites"></a>Edellytykset
Tämän artikkelin esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Käytä jotain seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Sovelluksen käyttöön määritetyn Microsoft SharePoint Server -esiintymän käyttöoikeudet.
- Sähköisen raportoinnin (ER) muoto ja mallin määritykset 1099-maksuille.

### <a name="create-required-er-configurations"></a>Luo tarvittavat ER-konfiguraatiot
Toista **ER -tuo tiedot Microsoft Excel -tiedostosta** -tehtäväoppaat, jotka ovat osa, **7.5.4.3 Acquire/Develop IT service/solution components (10677)** -liiketoimintaprosessia. Näissä tehtäväoppaissa selitetään ER-konfiguraatioiden suunnittelu ja käyttö, jotta voit vuorovaikutteisesti tuoda toimittajatapahtumia Microsoft Excel -tiedostoista. Lisätietoja on kohdassa [Saapuvien asiakirjojen jäsennys Excel-muodossa](parse-incoming-documents-excel.md). Tehtäväoppaiden suorittamisen jälkeen sinulla on seuraavat määritykset.

#### <a name="er-configurations"></a>ER-määritykset

- ER-mallikonfiguraatio, **1099-maksumalli**
- ER-muotokonfiguraatio **Muoto toimittajatapahtumien tuomiseksi Excelistä**

![ER-määritykset tietojen tuomiseksi SharePointista.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Näyte saapuvasta tiedostosta tietojen tuontia varten

- Excel-tiedosto **1099import-data.xlsx**, joka sisältää toimittajatapahtumat ja joka pitäisi tuoda.

![Excel-mallitiedosto SharePointista tuomista varten.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Toimittajatapahtumien tuonnin muoto valitaan oletusmallimääritykseksi. Siksi, jos suoritat **1099-maksumallin** mallin määrityksen ja tämä mallin määritys on **Kohteeseen**-tyyppiä, mallin määritys suorittaa tätä muotoa, tuodakseen tietoja ulkoisista tiedostoista. Sitten se käyttää näitä tietoja sovellustaulujen päivittämiseen.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>SharePoint-käytön määrittäminen tiedostojen tallennusta varten
Jos haluat tallentaa sähköiset raporttitiedostot SharePoint-sijaintiin, sinun on määritettävä käyttöoikeus nykyisen yrityksen käyttämään SharePoint Server -esiintymään. Tässä esimerkissä yritys on USMF. Lisätietoja on kohdassa [SharePoint-tallennustilan määrittäminen](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Suorita kohdan [SharePoint-tallennustilan määrittäminen](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage) vaiheet.
2. Avaa määritetty SharePoint-sivusto.
3. Luo seuraavat kansiota, joihin saapuvat ER-tiedostot voidaan tallentaa:

     - Tiedostojen tuontilähde (tärkein) (alla olevassa näyttökuvassa on esimerkki)
     - Tiedostojen tuonnin lähde (vaihtoehtoinen)

    ![Tiedostojen tuonnin lähde (ensisijainen).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Valinnainen) Luo seuraavat kansiota, joihin tiedostot voidaan tallentaa tuonnin jälkeen. 

    - Tiedostojen arkistokansio – tämä kansio on tarkoitettu tiedostoille, joiden tuonti onnistui.
    - Tiedostojen varoituskansio – tämä kansio on tiedostoille, joiden tuontiin liittyi varoitus.
    - Tiedostojen virhekansio – tämä kansio on tarkoitettu tiedostoille, joiden tuonti epäonnistui.

4. Siirry kohtaan **Organisaation hallinto > Asiakirjojen hallinta > Asiakirjatyypit**.
5. Luo seuraavat asiakirjatyypit, joilla voi käyttää luotuja SharePoint-kansioita. Lisätietoja on kohdassa [Tiedostotyyppien määrittäminen](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Tiedostotyyppi       | Ryhmä              | Paikka      | SharePoint-kansio      |
|--------------------|--------------------|---------------|------------------------|
|SP – ensisijainen             |Tiedosto                |SharePoint     |Tiedostojen tuonnin lähde (ensisijainen)|
|SP – vaihtoehtoinen             |Tiedosto                |SharePoint     |Tiedostojen tuonnin lähde (vaihtoehtoinen)|
|SP-arkisto             |Tiedosto                |SharePoint     |Tiedostojen arkistokansio|
|SP-varoitus             |Tiedosto                |SharePoint     |Tietojen varoituskansio|
|SP-virhe             |Tiedosto                |SharePoint     |Tiedostojen virhekansio|

![SharePoint-asetus – uusi tiedostotyyppi.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Määritä ER-muodon ER-lähteet
1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin lähde**.
2. Määritä **Sähköisen raportoinnin lähde** -sivulla tietojen tuonin lähdetiedostot käyttämällä määritettyä ER-muotoa.
3. Määritä tiedostonimen peite, jotta tuotaisiin vain tiedostot, joiden pääte on .xlsx. Tiedostonimen peite on valinnainen, ja sitä käytetään vain, jos se on määritetty. Kullekin ER-muodolle voi määrittää vain yhden peitteen.
4. **Lajittele tiedostot ennen tuontia** -asetuksen vaihtaminen **Älä lajittele** -asetukseksi, jos tuotavia tiedostoja on useita, eikä tuontijärjestyksellä ole väliä
5. Valitse kaikki aiemmin luodut SharePoint-kansiot.

    [![ER-tiedostojen lähdeasetukset.](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - Sähköisen raportoinnin *lähde* määritetään kullekin sovelluksen yritykselle erikseen. Sen sijaan sähköisen raportoinnin *konfiguraatiot* ovat yhteisiä kaikille yrityksille.
> - Kun poistat sähköisen raportoinnin muodon ER-lähdeasetukset, kaikki liittyvät tiedostotilat (katso alla) poistetaan myös vahvistuksen perusteella.

## <a name="review-the-files-states-for-the-er-format"></a>Tarkista ER-muodon tiedostotilat
1. Valitse **Sähköisen raportoinnin lähde** -sivulla **Tiedostojen tilat lähteitä varten** tarkistaaksesi määritettyjen tiedostolähteiden sisällön nykyiselle ER-muodolle.
2. Takista **Tiedostot**-osassa tiedostojen luettelo. Luettelo sisältää:

    - Soveltuvat lähdetiedostot tiedostonimen peitteen perusteella (jos tiedostonimen peite on määritetty), jotka ovat valmiita tietojen tuontia varten. Näiden tiedostojen **Tuontimuodon lähteiden lokit** -osa on tyhjä.
    - Aiemmin tuodut tiedostot. Voit tarkistaa kaikkien näiden tiedostojen **Tuontimuodon lähteiden lokit** -osassa kyseisen tiedoston tuonnin historiatiedot.

Voit myös avata **Tiedostojen tilat lähteitä varten** -sivun valitsemalla **Organisaation hallinto** \> **Sähköinen raportointi** \> **Tiedostojen tilat lähteitä varten**. Tässä tapauksessa sivulla on tietoja tiedostolähteista kaikille ER-muodoille, joille on määritetty tiedostolähteet yrityksessä, johon olet parhaillaan kirjautuneena.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Tietojen tuominen Excel-tiedostoista, jotka ovat SharePoint-kansiossa
1. Lataa SharePointissa Microsoft Excel -tiedosto **1099import-data.xlsx**, joka sisältää toimittajatapahtumat **Tiedostojen tuonnin lähde (ensisijainen)** -kansioon, jonka loit aikaisemmin SharePointissa. 

    [![SharePoint-sisältö – Microsoft Excel -tiedosto tuontia varten.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Valitse **Tiedostojen tilat lähteitä varten** -sivulla **Päivitä** päivittäksesi sivun. SharePointiin ladatun Excel-tiedoston tila oli tällä sivulla **Valmis**. Tällä hetkellä tuetaan seuraavia tiloja:

    - **Valmis** – Määritetty automaattisesti kullekin uudelle tiedostolle SharePoint-kansiossa. Tämä tila tarkoittaa, että tiedosto on tuontivalmis.
    - **Tuodaan** – ER-raportin automaattisesti määrittämä, kun tuontiprosessi on lukinnut tiedoston estääkseen muita prosesseja käyttämästä sitä (jos useita on käynnissä yhtä aikaa).
    - **Tuotu** – ER-raportin automaattisesti määrittämä, kun tiedoston tuominen on onnistunut ja valmis. Tämä tila tarkoittaa, että tuotu tiedosto on poistettu määritetystä tiedostolähteestä (SharePoint-kansiosta).
    - **Epäonnistui** – ER-raportin automaattisesti määrittämä, kun tiedoston tuominen on valmis, mutta tapahtui virheitä tai poikkeuksia.
    - **Pidossa** – Käyttäjä määritetään manuaalisesti tällä sivulla. Tämä tila tarkoittaa, että tiedostoa ei tuoda nyt. Tätä tilaa voidaan käyttää lykkäämään joidenkin tiedostojen tuontia.

    [![Päivitetty ER-tiedostotilojen sivu valituille lähteille.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Tietojen tuominen SharePoint-tiedostoista
1. Avaa Er-konfiguraatiopuu, valitse **1099-maksumalli** ja laajenna ER-mallin komponenttiluettelo.
2. Valitse mallin määrityksen nimi avataksesi valitun ER-mallin konfiguraation mallimääritykset.

    [![Määrityssivu.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Valitse **Suorita** suorittaaksesi valitun mallimäärityksen. Koska määritit ER-muodon tiedostolähteet, voit muuttaa **Tiedoston lähde** -asetusta tarvittaessa. Jos pidät tämän asetuksen arvon, .xslx-tiedostot tuodaan määritetyistä lähteistä (SharePoint-kansiot tässä esimerkissä).

    Tässä esimerkissä tuodaan vain yksi tiedosto. Jos tiedostoja on useita, ne valitaan tuontiin siinä järjestyksessä, jossa ne lisättiin SharePoint-kansioon. Kukin ER-muodon suoritus tuo yhden valitun tiedoston.

    [![Tuo SharePointista ja suorita ER-mallin määritys.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Mallin määritys voidaan suorittaa [valvomattomasti](#limitations) erätilassa. Tässä tapauksessa aina, kun eräkäsittely suorittaa tämän ER-muodon, tuodaan yksi tiedosto määritetyistä tiedostolähteistä.

    Kun tiedoston tuonti SharePoint-kansiosta onnistuu, se poistetaan kyseisestä kansiosta ja siirretään onnistuneiden tiedostotuontien tai varoituksia sisältävien tiedostojen kansioon. Muussa tapauksessa se siirretään epäonnistuneiden tietojen kansioon tai se pysyy tässä kansiossa, jos epäonnistuneiden tiedostojen kansiota ei ole määritetty. 

5. Syötä tositteen tunnus, kuten **V-00001**, ja valitse sitten **OK**.

    [![Suorita ER-mallimääritys.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Valitse **Tiedostojen tilat lähteitä varten** -sivulla **Päivitä** päivittäksesi sivun.

    [![ER-tiedostotilat lähteiden sivulle.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Takista **Tiedostot**-osassa tiedostojen luettelo. **Tuontimuodon lähteiden lokit** -osa sisältää Excel-tiedostojen tuomisen historian. Koska tiedosto tuotiin onnistuneesti, se on merkitty arvolla **Poistettu** SharePoint-kansiossa.
8. Tarkista SharePoint-kansio **Tiedostojen tuonnin lähde (ensisijainen)**. Tästä kansiosta on poistettu Excel-tiedostot, jotka tuotiin onnistuneesti.
9. Valitse **Ostoreskontra** \> **Kausittaiset tehtävät** \> **Valmistevero (1099)** \> **Toimittajien tilitykset valmisteveroja (1099) varten**.
10. Valitse **Päivämäärästä**- ja **Päivämäärään**-kenttiin asianmukaiset arvot. Valitse sitten **Manuaaliset 1099-tapahtumat**.

    Sivulla näytetään toimittajatapahtumat, jotka tuotiin SharePointin Excel-tiedostoista tositteelle **V-00001**.

    [![Toimittajan 1099-tapahtumat -sivu.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>valmistele Excel-tiedosto tuontia varten
1. Avaa aiemmin käyttämäsi Excel-tiedosto. Lisää riville 3 ja sarakkeeseen 1 toimittajakoodi, jota ei ole sovelluksessa. Lisää muut keksityt toimittajatiedot riville.

    [![Microsoft Excel -mallitiedosto SharePointista tuontia varten.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Lataa päivitetty Excel-tiedosto, joka sisältää toimittajatapahtumat, SharePoint-kansioon **Tiedostojen tuonnin lähde (ensisijainen)**.
3. Avaa Er-konfiguraatiopuu, valitse **1099-maksumalli** ja laajenna ER-mallin komponenttiluettelo.
4. Valitse mallimääritykseen nimi päivittääksesi mallin määrittämisen siten, että virheellistä toimittajakoodia pidetään virheenä tietojen tuonnin aikana.
5. Valitse **Suunnittelu**.
6. Muuta **Vahvistukset**-välilehdessä vahvistuksen jälkeinen toiminto vahvistussäännölle, joka on määritetty sen arvioimiseksi, onko tuotu toimittajatili sovelluksessa. Päivitä **Tarkistuksen jälkeinen toiminto** -kentän arvoksi **Lopeta suoritus**, tallenna muutokset ja sulje sivu.

    [![ER-mallimäärityksen suunnittelun sivu.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Tallenna muutokset ja sulje ER-mallimäärityksen suunnitteluohjelma.
8. Valitse **Suorita** suorittaaksesi muutetun ER-mallimäärityksen.
9. Syötä tositteen tunnus, kuten **V-00002**, ja valitse sitten **OK**.

    Tietoloki sisältää ilmoituksen SharePoint-kansiossa olevasta tiedostosta, joka sisältää virheellisen toimittajatilin jota ei voi tuoda.

    [![Suorita ER-mallimääritys suoritettu.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Valitse **Tiedostojen tilat lähteitä varten** -sivulla **Päivitä** ja tarkista **Tiedostot**-osassa tiedostojen luettelo.

    [![ER – tiedostotilojen sivu valituille lähteille.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   **Tuontimuodon lähteiden lokit** -osa ilmaisee, että tuonti epäonnistui ja että tiedosto on yhä SharePointin tiedostojen virheet -kansiossa (**On poistettu** -valintaruutua ei ole valittu). Jos korjaat tämän tiedoston SharePointissa lisäämällä oikean toimittajakoodin ja siirtämällä sen sitten SharePointin Tiedostojen tuonnin lähde (ensisijainen) -kansioon, voit tuoda tiedoston uudelleen.

11. Valitse kohdassa **Ostoreskontra** \> **Kausittaiset tehtävät** \> **Valmistevero (1099)** \> **Toimittajien tilitykset valmisteveroja (1099) varten** asianmukaiset arvot **Päivämäärästä**- ja **Päivämäärään**-kenttiin ja valitse sitten **Manuaaliset 1099-tapahtumat**.

    Vain tositteen V-00001 tapahtumat ovat käytettävissä. Tositteen V-00002 tapahtumat eivät ole käytettävissä vaikka viimeisen tuodun tapahtuman virhe havaittiin Excel-tiedostossa.

## <a name=""></a><a name="limitations">Rajoitukset</a>

Dynamics 365 Finance -versioissa, jotka ovat vanhempia kuin 10.0.25, ER-kehyksen käyttöliittymä ei tarjoa mahdollisuutta aloittaa uutta erätyötä, joka suorittaa mallin yhdistämisen valvomattomassa tilassa tietojen tuontia varten. Sen sijaan sinun on kehitettävä uusi logiikka, jotta konfiguroitua ER-mallikartoitusta voidaan kutsua sovelluksen käyttöliittymästä tietojen tuomiseksi saapuvista tiedostoista. Tämän logiikan kehittämiseen tarvitaan hieman suunnittelutyötä. 

Lisätietoja tähän liittyvästä ER-ohjelmointirajapinnasta on [Koodi, joka suorittaa mallin yhdistämismäärityksen tietojen tuonnista](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) -osassa aiheessa [ER-kehyksen ohjelmointirajapinnan muutokset Sovelluspäivitykselle 7.3](er-apis-app73.md). Tarkastele koodia `BankImport_RU`-luokassa `Application Suite` -mallissa nähdäksesi, kuinka mukautettu logiikka voidaan toteuttaa. `BankImport_RU`-luokka laajentaa luokkaa `RunBaseBatch`. Tarkastele erityisesti metodia `runER()`, jossa `ERIModelMappingDestinationRun`-objekti luodaan ER-mallin yhdistämismäärityksen suorittajaksi.

Finance-versiossa 10.0.25 ja sitä uudemmissa versioissa ER-kehyksen käyttöliittymä ei tarjoa mahdollisuutta aloittaa uutta erätyötä, joka suorittaa mallin yhdistämisen valvomattomassa tilassa tietojen tuontia varten. Lisätietoja tästä prosessista on kohdassa [Tietojen tuominen erätilassa manuaalisesti valituista tiedostoista](er-configure-data-import-batch.md).

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[ER-kehyksen ohjelmointirajapinnan muutokset Sovelluspäivitykselle 7.3](er-apis-app73.md)

[ER-kehyksen ohjelmointirajapinnan muutokset Sovelluspäivitykselle 10.0.23](er-apis-app10-0-23.md)

[ER-kehyksen ohjelmointirajapinnan muutokset Sovelluspäivitykselle 10.0.25](er-apis-app10-0-25.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
