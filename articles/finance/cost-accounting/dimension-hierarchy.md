---
title: Dimensiohierarkia
description: Tässä ohjeaiheessa on tietoja dimensiohierarkioista. Dimensiohierarkian avulla voi määrittää kustannuslaskennan raportoinnin rakenteen, kustannuskäytännöt ja suojausasetukset.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2a2e48b15bedd25b685686fa18a91f30b600331c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217383"
---
# <a name="dimension-hierarchy"></a>Dimensiohierarkia

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja dimensiohierarkioista. Dimensiohierarkian avulla voi määrittää kustannuslaskennan raportoinnin rakenteen, kustannuskäytännöt ja suojausasetukset.  

## <a name="overview"></a>Yleiskuvaus

Dimensiohierarkioita käytetään useissa tilanteissa kustannuslaskennassa. Voit määrittää seuraavat tiedot dimensiohierarkian avulla:

-  Organisaation tarpeita vastaava raportointirakenne
-  Kustannuskäytännöt
-  Suojausasetukset

Esimerkki dimensiohierarkiasta.

![Esimerkki dimensiohierarkiasta](./media/dimension-hierarchy.png)

Dimensiohierarkia voidaan luoda seuraaville dimensiotyypeille:

-  Kustannustason dimensiot
-  Kustannusobjektin dimensiot
-  Tilastodimensiot

> [!NOTE]
> - Voit luoda samalle dimensiolle useita dimensiohierarkioita, jos tietoja on tarkasteltava eri näkökulmista.
> - Dimensiohierarkia voidaan liittää vain yhteen dimensioon.
> - Dimensiohierarkian rakenteessa voi olla rajoittamaton määrä tasoja. Kaikki tasot ovat käytettävissä **Kustannusseuranta**-työtilassa. Jos käytät raportointiin Microsoft Exceliä tai Microsoft Power BI:tä, vain 15 ensimmäistä dimensiohierarkian tasoa viedään. Tämä rajoitus on käytössä, koska sekä Excel että Power BI edellyttävät kiinteää rakennetta.
> - Dimensiohierarkialla ei ole voimassaoloaikaa. Tämän vuoksi kaikki dimensiohierarkiaan tehdyt muutokset tallennetaan heti tietueeseen, eikä tiettyä päivämäärää edeltävää ja sen jälkeistä vertailua voi tehdä.

## <a name="dimension-hierarchy-type"></a>Dimensiohierarkiatyyppi

Uutta dimensiohierarkiaa luotaessa on valittava hierarkiatyyppi. Valitse **Kustannuslaskenta** > **Dimensiot** > **Dimensiohierarkiat**. Valitse ensin **Uusi** ja sitten dimension hierarkiatyyppi. Voit valita joko **Dimension luokitushierarkia** tai **Dimension luokitteluhierarkia**.

### <a name="dimension-categorization-hierarchy"></a>Dimension luokitushierarkia

**Dimension luokitushierarkiaa** käytetään raportointiin. Se tukee vain kustannustason dimensioita. Kun valitset tämän tyypit, seuraavat säännöt ovat käytössä:

-  Dimension jäsen voidaan liittää hierarkiarakenteeseen useammin kuin kerran.
-  Voit sijoittaa kustannustason dimensiojäsenen eri solmukohtiin määrittämällä kustannustoiminnan lehtisolmuun.

### <a name="dimension-classification-hierarchy"></a>Dimension luokitteluhierarkia

**Dimension luokitteluhierarkia** -tyyppiä käytetään sääntöjen määrittämiseen ja raportointiin. Se tukee kaikkia dimensiota, kuten kustannusobjekteja, kustannustasoja ja tilastodimensioita. Kun valitset tämän tyypin, dimension jäsen voidaan liittää hierarkiarakenteeseen vain kerran.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Dimensiohierarkian luominen ja ylläpitäminen

Dimensiohierarkia luodaan puurakenteena, jossa on solmu- ja lehtisolmusuhteita

-  Solmussa voi olla 1:_n_ alisolmua.
-  Solmuun ei voi olla määritettynä sekä alisolmuja että lehtisolmuja.
-  Lehtisolmu voidaan määrittää vain hierarkian alimmalla tasolla.

### <a name="example"></a>Esimerkki

Pienyrityksessä on seuraava organisaatiorakenne, jossa ovat taloushallinto ja henkilöstöhallinto ovat hallinnon alaisia osastoja, kun taas kokoonpano ja pakkaus ovat tuotannon alaisia osastoja.

![Organisaatiorakenteen esimerkki](./media/dimension-hierarchy-org.png)

Kustannusobjektidimensio vastaa organisaation kaikkia kustannuspaikkoja.

- Kustannusobjektin dimensio
    - Kustannuspaikat

Kaikkia kustannuspaikkoja vastaava kustannusobjektidimensio voidaan määrittää tässä kuvatulla tavalla.

| Kustannuspaikat | kuvaus |
|--------------|-------------|
| CC001        | Henkilöstöhallinto          |
| CC002        | Myyntitiedot     |
| CC003        | Vero         |
| CC007        | Myyntireskontra/ostoreskontra       |
| CC005        | Kokoonpano    |
| CC006        | Pakkaus   |

Kustannustasodimensio vastaa organisaation kaikkia kustannustasoja

- Kustannustason dimensio
    - Kustannustasot

Kaikkia kustannustasoja vastaava kustannustasodimensio voidaan määrittää tässä kuvatulla tavalla.

| Kustannustasot | kuvaus |
|---------------|-------------|
| 10 001         | Sähkö |
| 10010         | Siivous    |
| 10011         | Lämmitys     |
| 40001         | MTKUST        |

Organisaation raportointivaatimukset täyttävä dimension hierarkia voidaan määrittää tässä kuvatulla tavalla.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio    | Dimensiohierarkiatyypin nimi      | Käyttöoikeusluettelohierarkia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisaatio             | Kustannuspaikat | Dimension luokitteluhierarkia | Nro                    |

Raportoinnin dimensiohierarkia voidaan määrittää tässä kuvatulla tavalla.

|                   | Dimension jäsenalueet   |                         |
|-------------------|---------------------------|-------------------------|
| **Solmukohdat**         | **Lähtödimension jäsen** | **Kohdedimension jäsen** |
| Organisaatio      |                           |                         |
| &nbsp;&nbsp;Hallinto         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto        | CC001                     | CC001                   |
| &nbsp;&nbsp;Tuotanto    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkaus | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano  | CC006                     | CC006                   |

Käytäntövaatimukset täyttävä dimension hierarkia voidaan määrittää tässä kuvatulla tavalla.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio     | Dimensiohierarkiatyypin nimi      |
|--------------------------|---------------|------------------------------------|
| Kustannustoiminta            | Kustannustasot | Dimension luokitteluhierarkia |

Käytännön dimensiohierarkia voidaan määrittää tässä kuvatulla tavalla.

|                   | Dimension jäsenalueet   |                         |
|-------------------|---------------------------|-------------------------|
| **Solmukohdat**         | **Lähtödimension jäsen** | **Kohdedimension jäsen** |
| Kustannustoiminta     |                           |                         |
| &nbsp;&nbsp;Kiinteä kustannus    | 10 001                     | 10011                   |
|&nbsp;&nbsp;Muuttuva kulu | 40001                     | 40010                   |

> [!NOTE]
> Solmulla voi olla **Dimension jäsenalueet** -kohdassa 1:_n_ dimension jäsenaluetta. Voit lisätä ne dimension jäsentunnukset, jotka eivät ole vielä dimension jäseniä. Tämä menetelmä mahdollistaa hierarkian käytön myös tulevaisuudessa.  

### <a name="copy-a-hierarchy"></a>Hierarkian kopiointi

Voit kopioida nykyisen dimensiohierarkian uuden dimensiohierarkian lähtökohdaksi. Tämä on kätevää, jos haluat verrata edellistä dimensiohierarkiaa uuteen dimensiohierarkiaan.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Hierarkian solmujen järjestäminen uudelleen

Voit siirtää solmua rakenteessa ylös- tai alaspäin nykyisellä tasolla. Voit järjestää tällä tavoin solmut uudelleen **Kustannusseuranta**-työtilassa tehtävää raportointia varten.

Voit siirtää solmu hierarkiassa uuteen sijaintiin valitsemalla kohdesolmun. Solmun voi siirtää kahdella tavalla:

- **Siirrä alapuolelle** – siirrä valittu solmu nykyisestä sijainnista hierarkiassa ja lisää valitun kohdesolmun **alapuolelle**.
- **Siirrä jälkeen** – siirrä valittu solmu nykyisestä sijainnista hierarkiassa ja lisää se valitun kohdesolmun **jälkeen** hierarkiatasolla.

> [!NOTE] 
> Solmujen järjestystä ei säilytetä, kun tiedot viedään Exceliin tai Power BI:hin, koska niistä käytetään oletusarvoisesti aakkosnumeerista lajittelua. Järjestys on palautettava manuaalisesti.

## <a name="define-dimension-hierarchies-for-reporting"></a>Raportoinnin dimensiohierarkioiden määrittäminen

Dimensiohierarkiat ovat tärkeitä raportoinnissa. Voit määrittää niiden avulla yksittäiseen organisaatioon sopivan rakenteen. Koosteet tehdään dimensiohierarkian solmutasolla, jotta asianomaiset millä tahansa organisaatiotasolla voivat nähdä minkä tahansa tason tietoja.

Dimensiohierarkiat ovat käytettävissä seuraavissa raportointityökaluissa. Tällä tavoin voidaan varmistaa raportointirakenteen yhdenmukaisuus.

- **Kustannusseuranta** -työtila (asiakasohjelma):

    - Määritykset ohjaavat.

- **Kustannusseuranta**-työtila (mobiilisovellus):

    - Määritykset ohjaavat.

- Excel

    - Mahdollisuus valita tietyt vientimääritelmäkohtaiset dimensiohierarkiat:

        - Yksi kustannustason dimensiohierarkia (pakollinen)
        - Yksi kustannusobjektin dimensiohierarkia (valinnainen)
        - Yksi tilastodimension hierarkia (valinnainen)

- Power BI:

    - Kaikki dimensiohierarkiat ovat käytettävissä.
    
Jos luot raportteja Excelissä tai Power BI:ssä, vain 15 ensimmäistä dimensiohierarkian tasoa viedään. Tämä rajoitus on käytössä, Excelissä ja Power BI:ssä on käytettävä kiinteää rakennetta. Jos hierarkiassa on yli 15 tasoa, lisätasoja ei viedä. Normalisoidussa taulussa on tietue kullekin hierarkian dimension jäsenelle. Niinpä kooste tehdään automaattisesti. Tämä auttaa varmistamaan, että minkä tahansa hierarkian 15 käytettävissä olevan tason saldot ovat edelleen oikeat.

Seuraavassa on esimerkki raportointirakenteen dimensiohierarkiasta.

| Kustannusobjektin dimensiohierarkia – taso 1 | Kustannusobjektin dimensiohierarkia – taso 2 | Kustannusobjektin dimensiohierarkia – taso 3 | Kustannusobjektin dimensiohierarkia – taso 4 | Kustannusobjektin dimensiohierarkia – taso 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organisaatio                              | Hallinto                                     | Myyntitiedot                                   | CC002                                     |                                            |
| Organisaatio                              | Hallinto                                     | Myyntitiedot                                   | CC003                                     |                                            |
| Organisaatio                              | Hallinto                                     | Myyntitiedot                                   | CC007                                     |                                            |
| Organisaatio                              | Hallinto                                     | Henkilöstöhallinto                                        | CC001                                     |                                            |
| Organisaatio                              | Tuotanto                                | Pakkaus                                 | CC005                                     |                                            |
| Organisaatio                              | Tuotanto                                | Kokoonpano                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Raportoinnissa käytettävien dimensiohierarkioiden päivittäminen 

Edellä mainituissa raportointityökaluissa käytettävät dimensiohierarkiat on ajan mittaan päivitettävä. Dimensiohierarkiat voi päivittää asiakasohjelman päivityksellä.

- **Kustannusseuranta** -työtila (asiakasohjelma)
- **Kustannusseuranta**-työtila (mobiilisovellus)

Välimuistiin valmiiksi tallennettu työ noutaa dimensiohierarkioiden päivitykset 24 tunnin välein. Kun viedyt tiedot on päivitetty, päivitetyt dimensiohierarkiat ovat käytettävissä seuraavissa työkaluissa:

- Excel
- Power BI

> [!NOTE] 
> Voit käynnistää dimensiohierarkian välimuistin päivityksen viemällä dimensiohierarkian tai päivitettävät hierarkiat uudelleen Exceliin.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Kustannuskäytäntöjen dimensiohierarkioiden määrittäminen

Kustannuslaskenta sisältää useita käytäntöjä, joissa yksityiskohtaiset säännöt määritetään. Seuraaville käytännöille on määritettävä vähintään yksi dimensiohierarkia:

- Kustannustoiminta
- Kustannusten jako
- Kustannusten kohdistus
- Kustannusten koonti

Sääntöjä on helppo luoda dimensiohierarkioissa. Sinun ei tarvitse luoda sääntöjä dimensioyhdistelmän jokaiselle jäsenelle, jos käytät dimensiohierarkian tasojen mukaan muodostettavia dimension jäsenkoosteita. Jos sinulla on päällekkäisiä sääntöjä, sinun on määritettävä järjestelmää varten säännöt, jotka se ottaa huomioon yleiskustannuslaskennassa.

### <a name="example-define-a-cost-behavior-policy"></a>Esimerkki: kustannustoimintakäytännön määrittäminen

Uusi kustannustoimintakäytäntö luodaan ja soveltuvat dimensiohierarkiat määritetään käytäntöön tässä kuvatulla tavalla.

**Kustannustoimintakäytäntö**

| Käytännön nimi   | Kustannustason dimensiohierarkia | Kustannusobjektin dimensiohierarkia | Kirjanpitovaluutta |
|---------------|----------------------------------|---------------------------------|---------------------|
| Kustannustoiminta | Kustannustoiminta                    | Organisaatio                    | USD                 |

**Säännöt**

| Kustannustason dimensiohierarkiasolmu | Kustannusobjektin dimensiohierarkiasolmu | Kiinteä prosenttiosuus | Kiinteä summa | Voimassaolo alkaa | Voimassaolo päättyy |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Kiinteä kustannus                            | Organisaatio                         | 100,00           | 0,00         | 1/1/2017   | En koskaan    |
| 10 001                                 | Organisaatio                         | 0,00             | 150,00       | 1/1/2017   | En koskaan    |
| 10001 (\*)                             | Myyntitiedot                              |                  | 50,00        | 1/1/2017   | En koskaan    |
| Kustannustoiminta tai muuttuva kulu(\*\*)   | Organisaatio                         | 0,00             | 0,00         | 1/1/2017   | En koskaan    |

\* Muuttuvan kulun solmua ei tarvita. Jos kustannusta ei ole luokiteltu kiinteäksi kustannukseksi, sen on oltava muuttuva kulu.

\*\* Yksityiskohtainen sääntö luodaan kustannustason jäsenen 10001 ja kaikkien niiden kustannusobjektin jäsenten yhdistelmällä, jotka on koottu taloushallinnon hierarkiatasossa (CC002, CC003, CC007).

Edellä olevat säännöt osoittavat, miten joustavia dimensiohierarkiat ovat. Ylätasojen sääntöjen määrittäminen pitää ylläpidon tarpeen mahdollisimman vähäisenä. Voit sitten määrittää yksityiskohtaisia, tiettyyn liiketoimintatavoitteeseen sopivia sääntöjä.

Jos säännössä käytettäviä dimensiohierarkioita päivitetään, järjestelmä tuo päivitykset automaattisesti eteen.

Jos säännön rakeisuustasoa ei enää tarvita, sääntö vanhenee.

Esimerkiksi tiettyä taloushallinnon kustannusobjektidimension hierarkiasolmun kustannustoimintasääntöä ei enää tarvita. Siinä tapauksessa **Vanhenemissääntö**-vaihtoehdon valinta määrittää säännön vanhentumaan.

| Kustannustason dimensiohierarkiasolmu | Kustannusobjektin dimensiohierarkiasolmu | Kiinteä prosenttiosuus | Kiinteä summa | Voimassaolo alkaa | Voimassaolo päättyy  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Kiinteä kustannus                            | Organisaatio                         | 100,00           | 0,00         | 1/1/2017   | En koskaan     |
| 10 001                                 | Organisaatio                         | 0,00             | 150,00       | 1/1/2017   | En koskaan     |
| 10 001                                 | Myyntitiedot                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Kustannustoiminta tai muuttuva kulu        | Organisaatio                         | 0,00             | 0,00         | 1/1/2017   | En koskaan     |

Tätä sääntöä ei oteta enää huomioon, jos yleiskustannuslaskenta tehdään myöhemmin kuin 20.1.2017.

> [!NOTE] 
> **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttiä voimassaolopäivä ja -aika. Voit määrittää säännön vanhentumaan ja suorittaa uuden yleiskustannuslaskennan samana päivänä.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Suojausasetusten dimensiohierarkioiden määrittäminen

Kustannuslaskentatietojen pitäisi olla kaikkien raportointiyksiköistä vastaavien esimiesten käytettävissä. Kustannuslaskennan terminologiassa raportointiyksikkö vastaa kustannusobjektia tai kustannusobjektien joukkoa.

Periaatteessa kaikki esimiehet voivat käyttää erittäin arkaluonteisia liiketoimintatietoja, kuten tuottoja ja katteita. Tämän vuoksi on suojausasetusten määrittäminen on tärkeää, jotta esimiehet näkevät heidän kannaltaan oleelliset tiedot. Dimensiohierarkioiden määrittäminen auttaa hallitsemaan tietojen suojausta.

- Dimensiohierarkioita käytetään vain silloin, kun dimensiohierarkiaviittauksessa valittu dimensioarvo on kustannusobjektidimensio.
- Käyttöoikeusluettelon hierarkiassa yhdelle kustannusobjektidimensiolle voidaan ottaa käyttöön vain yksi dimensiohierarkia.

**Dimension hierarkiatiedot**

| Dimensiohierarkian nimi | Dimensio    | Dimensiohierarkiatyypin nimi      | Käyttöoikeusluettelohierarkia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisaatio             | Kustannuspaikat | Dimension luokitteluhierarkia | **Kyllä**               |

Hierarkian suunnittelutoiminnossa on uusi **Käyttäjät**-pikavälilehti. Voit lisätä välilehdessä yhden käyttäjätunnukset tai useita tunnuksia jokaiseen hierarkian solmuun.

|                 | Käyttäjät            | Dimension jäsenalueet   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Solmukohdat**       | **Käyttäjätunnus**      | **Lähtödimension jäsen** | **Kohdedimension jäsen** |
| Organisaatio    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Hallinto         | Huhtikuu            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Myyntitiedot   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Henkilöstöhallinto        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Tuotanto    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkaus | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Kokoonpano  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Kustannuslaskijat on määritettävä hierarkian ylimmälle tasolle, jotta he näkevät kaikki kustannuslaskennan merkinnät.

Ota käyttöoikeusluettelon hierarkian ja sen suojausasetukset käyttöön valitsemalla **Kustannuslaskenta** > **Asetukset** > **Parametrit** > **Yleiset**. Valitse parametri **Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille**.

Käyttöoikeusluettelon hierarkian asetuksilla hallitaan seuraavilla alueilla näkyviä tietoja:

- **Kustannusseuranta** -työtila (asiakasohjelma):

    - Niiden lomakkeiden tiedot, joilla skenaarioihin poraudutaan

- **Kustannusseuranta**-työtila (mobiilisovellus):

    - Korttien saldot

- Power BI:

    - Power BI -visualisoinneissa näytettävät tiedot
    - Tietojen Power BI -visualisoinnit, jotka on upotettu Dynamics 365 Financen asiakasohjelmassa

> [!NOTE] 
> - Käyttöoikeusluettelon hierarkia ei ole vaikuta Power BI -tietoihin, ennen kuin käyttöoikeusluettelon hierarkia ja Power BI:n rivitason suojaus ovat muodostaneet parin. Lisätietoja on ohjeaiheessa [Kustannuslaskennan sisältöpaketin suojauksen määrittäminen](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Käyttöoikeusluettelon hierarkia ei suojaa Exceliin vietyjä tietoja. Niinpä vain niiden kustannuslaskijoiden ja esimiesten, joilla on tietojen täydet katseluoikeudet, pitäisi käyttää raportointityökalua.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]