---
title: "Määritä tietojen tuonti SharePointista"
description: "Tässä ohjeaiheessa käsitellään tietojen tuominen Microsoft SharePointista."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 9f23f73e9a98fc50c622255bf6ed027c41ec8010
ms.contentlocale: fi-fi
ms.lasthandoff: 08/13/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Määritä tietojen tuonti SharePointista

[!include[banner](../includes/banner.md)]

Tietojen tuominen saapuvasta tiedostosta käyttämällä sähköisen raportoinnin (ER) kehystä: on määritettävä ER-muoto, joka tukee tuontia, ja sitten suorittaa mallin määritys **Kohteeseen**-tyypille, joka käyttää kyseistä muotoa tietolähteenä. Tietojen tuomiseksi siirry tiedostoon, jonka haluat tuoda. Käyttäjä voi valita manuaalisesti saapuvan tiedoston. Uuden sähköisen raportoinnin ominaisuuden kanssa, joka tukee tietojen tuomista Microsoft SharePointista, tämä prosessi voidaan määrittää automaattiseksi. Voit käyttää ER-määrityksiä suorittaaksesi tietojen tuonnin tiedostoista, jotka on tallennettu Microsoft SharePoint -kansioihin. Tässä ohjeaiheessa kerrotaan, miten voit siimeistellä tuonnin SharePointista Microsoft Dynamics 365 for Finance and Operationsiin. Esimerkissä käytetään toimittajatapahtumia liiketoimintatietoina.

## <a name="prerequisites"></a>Edellytykset
Tämän aiheen esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Finance and Operations -käyttöoikeudet seuraaville rooleille:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Finance and Operations -käyttöön määritetyn Microsoft SharePoint Server -ilmentymän käyttöoikeudet
- Sähköisen raportoinnin (ER) muoto ja mallin määritykset 1099-maksuille

### <a name="create-required-er-configurations"></a>Luo tarvittavat ER-konfiguraatiot
Toista **ER -tuo tiedot Microsoft Excel -tiedostosta** -tehtävoppaat, jotka ovat osa, **7.5.4.3 Acquire/Develop IT service/solution components (10677)** -liiketoimintaprosessia. Näissä tehtäväoppaissa selitetään ER-konfiguraatioiden suunnittelu ja käyttö, jotta voit vuorovaikutteisesti tuoda  toimittajatapahtumia ulkoisista Microsoft Excel -tiedostoista. Lisätietoja on kohdassa [Saapuvien asiakirjojen jäsennys Microsoft Excelissä](parse-incoming-documents-excel.md). Lopulta sinulla on:

- ER-konfiguroinnit:

    - ER-mallikonfiguraatio, **1099-maksumalli**
    - ER-muotokonfiguraatio **Muoto toimittajatapahtumien tuomiseksi Excelistä**

    [![ER-määritykset tietojen tuomiseksi SharePointista](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Näyte saapuvasta tiedostosta tietojen tuontia varten:

    - Excel-tiedosto **1099import-data.xlsx**, joka sisältää toimittajatapahtumat, ja joka pitäisi tuoda Finance and Operationsiin

    [![Microsoft Excel -mallitiedosto SharePointista tuontia varten](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Toimittajatapahtumien tuonnin muoto valitaan oletusmallimääritykseksi. Siksi, jos suoritat **1099-maksumallin** mallin määrityksen ja tämä mallin määritys on **Kohteeseen**-tyyppiä, mallin määritys suorittaa tätä muotoa, tuodakseen tietoja ulkoisista tiedostoista. Sitten se käyttää näitä tietoja sovellustaulujen päivittämiseen.

## <a name="configure-document-management-parameters"></a>Tiedostonhallintaparametrien konfigurointi
1. Konfiguroi **Tiedostonhallintaparametrit**-sivulla SharePoint Server -ilmentymän käyttöoikeudet, joita käytetään yrityksessä, johon olet tällä hetkellä kirjautunut. Tässä esimerkissä yritys on USMF.
2. Testaa yhteys varmistaaksesi, että sinulle myönnetty SharePoint Server -ilmentymän käyttöoikeudet.

    [![Tiedostonhallinnan asetukset – SharePoint Server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Avaa määritetty SharePoint-sivusto ja luo seuraavat kansiot, joihin saapuvat tiedostot voidaan tallentaa:

    - Tiedostojen tuonnin lähde (ensisijainen)
    - Tiedostojen tuonnin lähde (vaihtoehtoinen)

    [![Tiedostonhallinnan asetukset – SharePoint Server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

    [![Tiedostonhallinnan asetukset – SharePoint Server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Voit luoda Finance and Operationsin **Tiedostotyypit**-sivulla seuraavat tiedostotyypit, joita käytetään juuri luomiisi SharePoint-kansioihin kirjauduttaessa.

    - SP – ensisijainen
    - SP – vaihtoehtoinen

5. Luotuja asiakirjatyyppejä varten, **Ryhmä**-kenttään valitse **Tiedosto** ja **Sijainti**-kenttään valitse **SharePoint**. Kirjoita sitten SharePoint-kansion osoite:

    - **SP – ensisijainen** -tiedostotyypille: tiedostojen tuonnin lähde (ensisijainen)
    - **SP – vaihtoehtoinen** -tiedostotyypille: tiedostojen tuonnin lähde (vaihtoehtoinen)

    [![SharePoint-asetus – uusi asiakirjatyyppi](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Määritä ER-muodon ER-lähteet
1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin lähde**.
2. Määritä **Sähköisen raportoinnin lähde** -sivulla tietojen tuonin lähdetiedostot käyttämällä määritettyä ER-muotoa.
3. Määritä tiedostonimen peite, jotta tuotaisiin vain tiedostot, joiden pääte on .xlsx. Tiedostonimen peite on valinnainen, ja sitä käytetään vain, jos se on määritetty. Kullekin ER-muodolle voi määrittää vain yhden peitteen.
4. Valitse molemmat aiemmin luomistasi SharePoint-kansioista.

    [![ER-tiedostojen lähdeasetukset](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - Sähköisen raportoinnin *lähde* määritetään kullekin sovelluksen yritykselle erikseen. Sen sijaan sähköisen raportoinnin *konfiguraatiot* ovat yhteisiä kaikille yrityksille.
> - Kun poistat sähköisen raportoinnin muodon ER-lähdeasetukset, kaikki liittyvät tiedostotilat (ks. alla) poistetaan myös.

## <a name="review-the-files-states-for-the-er-format"></a>Tarkista ER-muodon tiedostotilat
1. Valitse **Sähköisen raportoinnin lähde** -sivulla **Tiedostojen tilat lähteitä varten** tarkistaaksesi määritettyjen tiedostolähteiden sisällön nykyiselle ER-muodolle.
2. Takista **Tiedostot**-osassa tiedostojen luettelo. Luettelo sisältää:

    - Soveltuvat lähdetiedostot tiedostonimen peitteen perusteella (jos tiedostonimen peite on määritetty), jotka ovat valmiita tietojen tuontia varten. Näiden tiedostojen **Tuontimuodon lähteiden lokit** -osa on tyhjä.
    - Aiemmin tuodut tiedostot. Voit tarkistaa kaikkien näiden tiedostojen **Tuontimuodon lähteiden lokit** -osassa kyseisen tiedoston tuonnin historiatiedot.

Voit myös avata **Tiedostojen tilat lähteitä varten** -sivun valitsemalla **Organisaation hallinto** \> **Sähköinen raportointi** \> **Tiedostojen tilat lähteitä varten**. Tässä tapauksessa sivulla on tietoja tiedostolähteista kaikille ER-muodoille, joille on määritetty tiedostolähteet yrityksessä, johon olet parhaillaan kirjautuneena.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Tietojen tuominen Excel-tiedostoista, jotka ovat SharePoint-kansiossa
1. Lataa SharePointissa Microsoft Excel -tiedosto **1099import-data.xlsx**, joka sisältää toimittajatapahtumat, SharePointin **Tiedostojen tuonnin lähde (ensisijainen)** -kansioon, jonka loit aikaisemmin.

    [![SharePoint-sisältö – Microsoft Excel -tiedosto tuontia varten](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Valitse Finance and Operationsin **Tiedostojen tilat lähteitä varten** -sivulla **Päivitä** päivittäksesi sivun. Huomaa, että Excel-tiedosto, joka on ladattu SharePointiin, oli tässä muodossa tilassa **Valmis**. Tällä hetkellä tuetaan seuraavia tiloja:

    - **Valmis** – Määritetty automaattisesti kullekin uudelle tiedostolle SharePoint-kansiossa. Tämä tila tarkoittaa, että tiedosto on tuontivalmis.
    - **Tuodaan** – ER-raportin automaattisesti määrittämä, kun tuontiprosessi on lukinnut tiedoston estääkseen muita prosesseja käyttämästä sitä (jos useita on käynnissä yhtä aikaa).
    - **Tuotu** – ER-raportin automaattisesti määrittämä, kun tiedoston tuominen on onnistunut ja valmis. Tämä tila tarkoittaa, että tuotu tiedosto on poistettu määritetystä tiedostolähteestä (SharePoint-kansiosta).
    - **Epäonnistui** – ER-raportin automaattisesti määrittämä, kun tiedoston tuominen on valmis, mutta tapahtui virheitä tai poikkeuksia.
    - **Pidossa** – Käyttäjä määrittää manuaalisesti tässä lomakkeessa. Tämä tila tarkoittaa, että tiedostoa ei tuoda nyt. Tätä tilaa voidaan käyttää lykkäämään joidenkin tiedostojen tuontia.

    [![ER – tiedostotilojen sivu valituille lähteille](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Tietojen tuominen SharePoint-tiedostoista
1. Avaa Er-konfiguraatiopuu, valitse **1099-maksumalli** ja laajenna ER-mallin komponenttiluettelo.
2. Valitse mallin määrityksen nimi avataksesi valitun ER-mallin konfiguraation mallimääritykset.

    [![ER – tiedostotilojen sivu valituille lähteille](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Valitse **Suorita** suorittaaksesi valitun mallimäärityksen. Koska määritit ER-muodon tiedostolähteet, voit muuttaa asetusta **Tiedoston lähde** tarpeen mukaan. Jos pidät tämän asetuksen arvon, .xslx-tiedostot tuodaan määritetyistä lähteistä (SharePoint-kansiot tässä esimerkissä).

    Tässä esimerkissä tuodaan vain yksi tiedosto. Jos tiedostoja on useita, ne valitaan tuontiin siinä järjestyksessä, jossa ne lisättiin SharePoint-kansioon. Kukin ER-muodon suoritus tuo yhden valitun tiedoston.

    [![Suorita ER-mallimääritys](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Mallin määritys voidaan suorittaa automaattisesti erätilassa. Tässä tapauksessa aina, kun eräkäsittely suorittaa tämän ER-muodon, tuodaan yksi tiedosto määritetyistä tiedostolähteistä. Seuraavan koodin avulla voit toteuttaa tämän eräajon suorittamisen.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Kun tiedosto on onnistuneesti tuotu SharePoint-kansiosta, se poistetaan kyseisestä kansiosta.

5. Syötä tositteen tunnus, kuten **V-00001**, ja valitse sitten **OK**.

    [![Suorita ER-mallimääritys](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Valitse **Tiedostojen tilat lähteitä varten** -sivulla **Päivitä** päivittäksesi sivun.

    [![ER – tiedostotilojen sivu valituille lähteille](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Takista **Tiedostot**-osassa tiedostojen luettelo. **Tuontimuodon lähteiden lokit** -osa sisältää Excel-tiedostojen tuomisen historian. Koska tiedosto tuotiin onnistuneesti, se on merkitty arvolla **Poistettu** SharePoint-kansiossa.
8. Tarkista SharePoint-kansio **Tiedostojen tuonnin lähde (ensisijainen)**. Tästä kansiosta on poistettu Excel-tiedostot, jotka tuotiin onnistuneesti.
9. Valitse Finance and Operationsissa **Ostoreskontra** \> **Kausittaiset tehtävät** \> **Valmistevero (1099)** \> **Toimittajien tilitykset valmisteveroja (1099) varten**.
10. Valitse **Päivämäärästä**- ja **Päivämäärään**-kenttiin asianmukaiset arvot. Valitse sitten **Manuaaliset 1099-tapahtumat**.

    Toimittajatapahtumat, jotka tuotiin SharePointin Excel-tiedostoista tositteelle **V-00001**, näytetään sivulla.

    [![Toimittajan 1099-tapahtumat -sivu](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>valmistele Excel-tiedosto tuontia varten
1. Avaa aiemmin käyttämäsi Excel-tiedosto. Lisää riville 3 ja sarakkeeseen 1 toimittajakoodi, jota ei ole sovelluksessa. Lisää muut keksityt toimittajatiedot riville.

    [![Microsoft Excel -mallitiedosto SharePointista tuontia varten](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Lataa päivitetty Excel-tiedosto, joka sisältää toimittajatapahtumat, SharePoint-kansioon **Tiedostojen tuonnin lähde (ensisijainen)**.
3. Avaa Finance and Operationsissa ER-konfiguraatiopuu, valitse **1099-maksumalli** ja laajenna ER-mallin komponenttiluettelo.
4. Valitse mallimääritykseen nimi päivittääksesi mallin määrittämisen siten, että virheellistä toimittajakoodia pidetään virheenä tietojen tuonnin aikana.
5. Valitse **Suunnittelu**.
6. Muuta **Vahvistukset**-välilehdessä vahvistuksen jälkeinen toiminto vahvistussäännölle, joka on määritetty sen arvioimiseksi, onko tuotu toimittajatili sovelluksessa. Päivitä **Tarkistuksen jälkeinen toiminto** -kentän arvoksi **Lopeta suoritus**, tallenna muutokset ja sulje sivu.

    [![ER-mallimäärityksen sunnittelun sivu](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Tallenna muutokset ja sulje ER-mallimäärityksen suunnitteluohjelma.
8. Valitse **Suorita** suorittaaksesi muutetun ER-mallimäärityksen.
9. Syötä tositteen tunnus, kuten **V-00002**, ja valitse sitten **OK**.

    Huomaa, että tietoloki sisältää ilmoituksen siitä, että SharePoint-kansion tiedosto sisältää virheellisen toimittajatilin, eikä sitä voi tuoda.

    [![Suorita ER-mallimääritys](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Valitse **Tiedostojen tilat lähteitä varten** -sivulla **Päivitä** ja tarkista **Tiedostot**-osassa tiedostojen luettelo.

    [![ER – tiedostotilojen sivu valituille lähteille](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

    **Tuontimuodon lähteiden lokit** -osa ilmaisee, että tuonti epäonnistui ja että tiedosto on yhä SharePoint-kansiossa (**On poistettu** -valintaruutua ei ole valittu). Jos korjaat tämän tiedoton SharePointissa lisäämällä asianmukaisen toimittajan koodin ja sitten muutat tiedoston tilasta **Epäonnistui** tilaan **Valmis** **Tuontimuodon lähteiden lokit** -osassa, voit tuoda tiedoston uudelleen.

11. Tarkista SharePoint-kansio **Tiedostojen tuonnin lähde (ensisijainen)**. Huomaa, että Excel-tiedosto, jota ei tuotu, on edelleen tässä kansiossa.
12. Valitse Finance and Operationsin kohdassa **Ostoreskontra** \> **Kausittaiset tehtävät** \> **Valmistevero (1099)** \> **Toimittajien tilitykset valmisteveroja (1099) varten** asianmukaiset arvot **Päivämäärästä**- ja **Päivämäärään**-kenttiin ja valitse sitten **Manuaaliset 1099-tapahtumat**.

    Vain tositteen V-00001 tapahtumat ovat käytettävissä. Tositteen V-00002 tapahtumat eivät ole käytettävissä vaikka viimeisen tuodun tapahtuman virhe havaittiin Excel-tiedostossa.

