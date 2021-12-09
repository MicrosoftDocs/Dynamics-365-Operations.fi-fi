---
title: Commercen analytiikka (esiversio)
description: Tässä aiheessa kerrotaan, miten analytiikkaominaisuuden voi asentaa ja käyttää Microsoft Dynamics 365 Commercessa.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862770"
---
# <a name="commerce-analytics-preview"></a>Commercen analytiikka (esiversio)

[!include [banner](includes/banner.md)]

Tässä aiheessa kerrotaan, kuinka Commercen analytiikka (esiversio) asennetaan. Se on Microsoft Dynamics 365 Commerceen sisältyvä toiminnallisen analytiikan toiminto.

## <a name="commerce-analytics-preview-live-demo"></a>Commercen analytiikka (esiversio) – live-esittely

Voit kokeilla [Commercen analytiikan (esiversio) live-esittelyä](https://aka.ms/CommerceAnalyticsDemo).

![Commercen analytiikka (esiversio) – yhteenveto](media/CommerceAnalytics_Summary.png)
![Commercen analytiikka (esiversio) – maksut](media/CommerceAnalytics_Payments.png)
![Commercen analytiikka (esiversio) – verkon aktiviteetti](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Commercen analytiikka (esiversio) – järjestelmän arkkitehtuuri

### <a name="key-components"></a>Tärkeimmät osat

Commercen analytiikka (esiversio) koostuu seuraavista avainkomponenteista:

- Vuorovaikutteiset Power BI -raportit, jotka ovat valmiita käytettäväksi
- SQL-näkymät Azure Synapse Analyticsissa
- Entiteetti- ja ontologiatiedot Azure Data Lake -tallennustilassa
- Raakatiedot Data Lake -tallennustilassa

![Commercen analytiikan järjestelmäarkkitehtuurin tärkeimmät komponentit](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Tietojen virtaus

#### <a name="step-1-data-generation"></a>Vaihe 1: Tietojen luominen

Tiedot ovat peräisin joko tapahtumatietona tai toimintatietona seuraavista lähteistä:

- Puhelinkeskuksen asiakaspalvelija käyttää Commerce HQ -asiakasohjelmaa myyntitilausten käsittelemiseen.
- Kassanhoitaja käsittelee myyntitapahtumia myyntipisteessä.
- Myynti luodaan mukautetuissa sovelluksissa käyttämällä palvelitonta Commercea (Commerce Scale Unit).
- Sähköisen kaupankäynnin ostaja selaa sähköistä verkkokauppasivustoa.
- Sähköisen kaupankäynnin ostaja tekee tilauksen sähköisessä verkkokauppasivustoa.
- Tiedot ovat muiden järjestelmien tuottamia, esimerkiksi Dynamics 365 Connected Spacesin tuottamia.

#### <a name="step-2-ingestion-and-pre-processing"></a>Vaihe 2: Sisäänotto ja esikäsittely

Tapahtumatiedot siirtyvät Commerce HQ -järjestelmään joko suoraan (suoraan Commerce HQ -asiakkaalla siepatut tilaukset) tai Commerce Scale Unitin kautta (jos tilaukset siepataan myyntipisteessä, sähköisessä kaupankäynnissä tai mukautetuissa asiakkaissa, joissa käytetään palvelitonta Commercea).

Sen jälkeen tapahtumatiedot viedään Data Lake -tallennustilaan raakatietoina Vie Data Lake -tallennustilaan -toiminnolla. Raakatiedot tallennetaan Data Lake -tallennustilassa Taulut-kansioon.

Sähköisen kaupankäynnin verkkoaktiviteettitiedot lähetetään suoraan Data Lake -tallennustilaan. Muissa järjestelmissä, kuten Dynamics 365 Connected Spacesissa, tuotetut tiedot, lähetetään suoraan Data Lake -tallennustilaan näiden järjestelmien toimesta.

#### <a name="step-3-transformation-and-aggregation"></a>Vaihe 3: Muunnos ja koostaminen

Kun raakatiedot ovat Data Lake -tallennustilassa, Commercen analytiikkapalvelu lukee ne, muuntaa ne, koostaa ne ja kirjoittaa sen takaisin Data Lake -tallennustilaan loogisten entiteettien muodossa (Entiteetit-kansiossa) ja koostaa mittarit (Ontologiat-kansiossa).

#### <a name="step-4-querying"></a>Vaihe 4: Kyselyt

Azure Synapse Analyticsin avulla voi tehdä kyselyjä dataasi Data Lake -tallennustilassa Transact-SQL (T-SQL) -liittymän kautta. Tämä liittymä sisältää SQL-näkymät. SQL-näkymien avulla voi suorittaa tietojen yhdistettyjä kyselyjä Data Lake -tallennustilassa, joko suoraan T-SQL-asiakkaan kautta (ad-hoc-analyysiä varten) tai visualisointityökalun, kuten Power BI:n, avulla.

#### <a name="step-5-modeling-and-serving"></a>Vaihe 5: Mallinnus ja palvelu

Azure Synapse Analyticsin kyselemät tiedot siirtyvät semanttiseen Power BI -malliin. Tietotyypistä riippuen tiedot tuodaan kausittain muistin sisäisesti Power BI:hin tai kysellään suoraan suorituksen aikana.

Lopuksi tiedot hahmonnetaan Power BI -visualisoinneiksi, jotta käyttäjät voivat tarkastella tietoja ja olla niiden kanssa vuorovaikutuksessa.

## <a name="commerce-analytics-preview-functional-overview"></a>Commercen analytiikan (esiversio) toimintojen yleiskuvaus

### <a name="summary"></a>Yhteenveto

Commercen analytiikka (esiversio) -mallisovellus sisältää seuraavat raporttien pääsivut:

1. [Ylätason suodattimet](#TopLevelFilters)
2. [Tuotteet](#ProductsPage)
3. [Asiakkaat](#CustomersPage)
4. [Kanavat](#ChannelsPage)
5. [Myynti](#SalesPage)
6. [Reunukset](#MarginsPage)
7. [Palautukset](#ReturnsPage)
8. [Alennukset](#DiscountsPage)
9. [Maksut](#PaymentsPage)
10. [Asiakkaat](#CustomersPage)
11. [Vertailu](#ComparisonPage)
12. [Verkkoaktiviteetti](#WebActivityPage)
13. [Verkkoaktiviteetti - ylimmän tason suodatin](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a>Ylätason suodattimet

- Päivämääräasetukset

    - Vuosi(a)
    - Vuosineljännes
    - Kuukausi
    - Viikko
    - Päivä

- Kanavan asetukset

    - Oikeushenkilö
    - Kanavatyyppi
    - Asiakastyyppi
    - Myyntityyppi
    - Kanava
    - Organisaatiohierarkia

- Tuoteasetukset

    - Luokkahierarkia
    - Luokka

####  <a name="products"></a><a name="ProductsPage"></a> Tuotteet

- Myynti
- Reunus
- Palautukset

####  <a name="customers"></a><a name="CustomersPage"></a> Asiakkaat

- Myynti
- Reunus
- Palautukset

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanavat

- Myynti
- Reunus
- Palautukset

### <a name="sales"></a>Myynti <a name="SalesPage"></a>

- Toimitussijainnin mukaan
- Kanavan/myymälän/päätteen mukaan
- Työntekijän mukaan
- Päivämäärän mukaan
- Tunnin mukaan
- Tuoteluokittain

### <a name="margins"></a><a name="MarginsPage"></a> Reunukset

- Toimitussijainnin mukaan
- Sivutuote
- Päivämäärän mukaan

### <a name="returns"></a><a name="ReturnsPage"></a> Palautukset

- Palautus summan mukaan

    - Myymälän mukaan
    - Sivutuote
    - Päivämäärän mukaan

- Palautus tapahtuman mukaan

    - Myymälän mukaan
    - Sivutuote
    - Päivämäärän mukaan

### <a name="discounts"></a><a name="DiscountsPage"></a> Alennukset

- Myymälän mukaan
- Sivutuote
- Päivämäärän mukaan
- Hajottaminen

    - Oikeushenkilö
    - Myymälä
    - Alennustyyppi
    - Alennuksen nimi
    - Tuote

### <a name="payments"></a><a name="PaymentsPage"></a> Maksut

- Kanavan/päätteen mukaan
- Maksutavan/tyypin mukaan
- Päivämäärän mukaan
- Hajottaminen

    - Oikeushenkilö
    - Kanavatyyppi
    - Myymälä
    - Pääte
    - Maksutapa

### <a name="customers"></a><a name="CustomersPage"></a> Asiakkaat

- Elinkaaren arvo (LTV)

    LTV lasketaan sen kokonaissumman perusteella, jonka asiakas käyttää kaikkien Dynamics 365 Commerce -myyntikanavien kautta (myyntipiste, sähköinen kauppa ja puhelinkeskus mukaan lukien).

- Recency

    Viimeaikaisuus lasketaan niiden päivien määrän perusteella, jolloin asiakkaan viimeinen tapahtuma organisaation kanssa tapahtui. Tällä hetkellä viimeaikaisuus ei ota huomioon ei-tapahtumallisia vuorovaikutussignaaleja, kuten verkkokaupan selailuaktiviteettia.

- Tiheys

    Tiheys lasketaan asiakkaan ja organisaation tapahtumavuorovaikutuksen perusteella. Tällä hetkellä tiheys ei ota huomioon ei-tapahtumallisia vuorovaikutussignaaleja, kuten verkkokaupan selailuaktiviteettia.

- Suhteen pituus

    Suhteen pituus lasketaan niiden päivien määrän perusteella, jolloin asiakastietue luotiin järjestelmässä.

- Tapahtumien määrä

### <a name="comparison"></a><a name="ComparisonPage"></a> Vertailu

- Tuotevertailu aikajakson mukaan

    - Myynti ja myyntiero
    - Marginaali ja marginaaliero

- Asiakas aikajakson mukaan

    - Myynti ja myyntiero
    - Marginaali ja marginaaliero

### <a name="web-activity"></a><a name="WebActivityPage"></a> Verkkoaktiviteetti

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Ylätason suodattimet

- Päivämääräalue
- Kanavatyyppi
- Kanava
- Luokkahierarkia

#### <a name="acquisitions"></a>Hankinnat

- Sivunäkymät

    - Maan tai alueen mukaan
    - Sivutuote
    - Kirjautuneen käyttäjän tilan mukaan
    - Päivämäärän mukaan

- Sähköisen kaupankäynnin tilaukset
- Vaihtokurssi

    - Päivämäärän mukaan

- Muuntosuppilo

    - Sivunäkymä sivutyypin mukaan (kotisivu, luokkasivu tai tuotteen tietosivu)
    - Lisää koriin
    - Kassalle
    - Osto

#### <a name="sessions"></a>Istunnot

Istunto on käyttäjän vierailu verkkokauppasivustossasi. Istunto pidetään päättyneenä 30 minuutin käyttämättömyyden tai 24 tunnin aktiivisuuden jälkeen.

- Maan tai alueen mukaan
- Alkuperän mukaan (ulkoinen viittaus)
- Kirjautuneen käyttäjän tilan mukaan
- Istuntojen määrä

    - Päivämäärän mukaan
    - Saapumissivun mukaan

- Tilaus per istunto

    - Päivämäärän mukaan

- Istunnon hylkäysprosentti

    Istunnon hylkäys on istunto, jossa käyttäjä poistuu heti saavuttuaan sähköisen kaupankäynnin sivustoosi. Lisätietoja on kohdassa [Hylkäysprosentti](https://en.wikipedia.org/wiki/Bounce_rate).

- Napsautukset per istunto

#### <a name="visitors"></a>Vierailijat

Verkkokauppaasivuston anonyymi vierailija voidaan tunnistaa käyttäjän käyttämän selaimen ja tietyn laitteen perusteella. Commercen analytiikka ei seuraa anonyymeja vierailijoita eri selainten tai laitteiden välillä. Saman laitteen samaa selainta käyttävät nimettömät vierailijat tunnistetaan käyttäjäistuntojen välillä, kunnes joko selaimen välimuistiin tallennetut tiedot tyhjenevät tai kausi (yleensä 12 kuukautta) kuluu (sen mukaan, kumpi tapahtuu ensin).

Jos vierailijat selaavat verkkokauppasivustoasi, kun he ovat kirjautuneena sisään, Commercen analytiikka voi antaa lisätietoja heistä. Nämä tiedot perustuvat aiemmin luotuun suhteeseen, joka organisaatiollasi on vierailijaan tuloksena kaikkien Dynamics 365 Commerce -myyntikanavien ostoista (myyntipiste, sähköinen kauppa ja puhelinkeskus mukaan lukien). Lisätietoja ovat viimeaikaisuus, suhteen pituus, elinkaaren arvo ja tiheys.

- Vierailijan marginaali
- Vierailijan keskimääräiset tilaukset
- Vierailijan keskimääräinen myynti
- Sähköisen kaupankäynnin vierailijoiden määrä

    - Päivämäärän mukaan
    - Sijainnin mukaan

        Tällä hetkellä Commercen analytiikka voi tarjota vain maan/alueen tason rakeisuutta sijaintianalytiikalle sähköisen kaupankäynnin vierailijoita varten.

    - Viimeaikaisuuden mukaan

        Viimeaikaisuus lasketaan niiden päivien määrän perusteella, jolloin asiakkaan viimeinen tapahtuma organisaation kanssa tapahtui. Tällä hetkellä viimeaikaisuus ei ota huomioon ei-tapahtumallisia vuorovaikutussignaaleja, kuten verkkokaupan selailuaktiviteettia.

    - Suhteen pituuden mukaan

        Suhteen pituus lasketaan niiden päivien määrän perusteella, jolloin asiakastietue luotiin järjestelmässä.

    - Elinkaaren arvon (LTV) mukaan

        LTV lasketaan sen kokonaissumman perusteella, jonka asiakas käyttää kaikkien Dynamics 365 Commerce -myyntikanavien kautta (myyntipiste, sähköinen kauppa ja puhelinkeskus mukaan lukien).

    - Tiheyden mukaan

        Tiheys lasketaan asiakkaan ja organisaation tapahtumavuorovaikutuksen perusteella. Tällä hetkellä tiheys ei ota huomioon ei-tapahtumallisia vuorovaikutussignaaleja, kuten verkkokaupan selailuaktiviteettia.

#### <a name="impressions"></a>Näyttökerrat

Näyttökerta on yksittäinen näkymä tuotteen visualisoinnista sähköisen kaupankäynnin vierailijalle. Esimerkiksi sähköisen kaupankäynnin vierailija menee sähköisen kaupankäynnin sivuston aloitussivulle ja näkee joogamatto-tuotteen **Eniten myydyt** -luettelomoduulissa. Sen jälkeen vierailija näkee saman joogamaton **Sinulle suositellut** -luettelomoduulissa. Tässä tapauksessa on kaksi tuotteen näyttökertaa. 

Tällä hetkellä näyttökertoja seurataan seuraavissa kohteissa:

- Luettelot (esimerkiksi **Suositellut**, **Myydyimmät**, **Sinulle suositellut** ja **Nousussa**)
- Ostoskorimoduuli
- Hakutulossäilö
- Luokkahaun tulossäilö

Tällä hetkellä tuotteita, jotka hahmonnetaan karusellimoduulissa tai mukautetuissa visualisoinneissa, ei lasketa näyttökertamittareihin.

**Näyttökertaraportti**-sivu sisältää seuraavat mittarit:

- Näyttökertojen määrä

    - Sivutyypin ja moduulin mukaan

        Sivutyyppi on yleinen sivutyyppi, joka on määritetty kullekin sähköisen kaupankäynnin sivuston sivulle. Moduulityyppi on verkkokaupan visuaalisen moduulin tyyppi, jossa tuote on näkyvissä.

        Jos haluat tarkastella näyttökertoja moduulin mukaan, sinun on ehkä porauduttava sivulle ja moduulin visualisointeihin.

    - Sivutuote
    - Kirjautuneen käyttäjän tilan mukaan
    - Päivämäärän mukaan

- Näyttökertojen napsautusten määrä

    Näyttökerran napsautus tapahtuu, kun sähköisen kaupankäynnin vierailija valitsee tuotteen visualisoinnin. Sen jälkeen vierailija yleensä siirtyy tuotteen tuotetietosivulle.

- Näyttökertojen napsautusprosentti (CTR).

    CTR lasketaan seuraavasti: näyttökertojen napsautusten määrä jaettuna näyttökertojen kokonaismäärällä.

## <a name="commerce-analytics-preview-installation"></a>Commercen analytiikan (esiversio) asennus

> [!NOTE]
> Commercen analytiikka (esiversio) on saatavilla esiversiona on Yhdysvalloissa, Kanadassa, Yhdistyneessä kuningaskunnassa, Euroopassa, Kaakkois-Aasiassa, Itä-Aasiassa, Australiassa ja Japanissa. Jos Finance and Operations -ympäristösi sijaitsee näillä alueilla, voit ottaa tämän ominaisuuden käyttöön ympäristössäsi käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palveluita. Ennen kuin voit käyttää tätä toimintoa, katso kohta [Määritä vienti Azure Data Lake -tallennustilaan](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commercen analytiikan (esiversio) ottaminen käyttöön ja määrittäminen

Jos haluat asentaa Commercen analytiikan (esiversio), sinulla on oltava käyttöoikeudet resurssien luontia varten Azure-tilauksessa. Sinulla on oltava myös käyttöoikeudet, jotta voit asentaa lisäosia LCS:ssä. Vaiheiden yhteenveto:

1. [Lähetä Commercen analytiikan (esiversio) esiversion sisäänottolomake](#joinPreview).
2. [Data Lake -viennin käyttöönotto ja määritys](#enableExportToDataLake).
3. [Commercen analytiikka (esiversio) -lisäosan ottaminen käyttöön ja määrittäminen](#enableCommerceAnalyticsAddin).
4. [Luo tallennustilille jaettu allekirjoituksen tunnus (SAS)](#getSASToken).
5. [Lataa Azure Synapse -näkymien käyttöönoton komentosarjat](#downloadSynapseDeploymentScripts).
6. [Azure Synapse workspacen asentaminen ja konfiguroiminen](#configureAzureSynapse).
7. [Power BI -mallisovelluksen asentaminen](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Lähetä Commercen analytiikan (esiversio) esiversion sisäänottolomake

Lähetä [Commercen analytiikan (esiversio) esiversion sisäänottolomake](https://forms.office.com/r/vW5VLJGXZ2). Lomakkeen käsittelemiseen voi kulua kolme arkipäivää. Kun se on käsitelty, sinulle lomakkeessa annettuun sähköpostiosoitteeseesi lähetetään vahvistussähköposti.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Data Lake -viennin käyttöönotto ja määritys

Commercen analytiikka (esiversio) luottaa Vie Data Lake -tallennustilaan -toimintoon viedäkseen Commerce HQ -tietoja Data Lake -tallennustilaan ja pitääkseen tiedot ajan tasalla. Ennen Commercen analytiikka (esiversio) -määritystä sinun on otettava käyttöön ja konfiguroitava Data Lake -vienti seuraamalla seuraavia ohjeita: [Azure Data Lake -viennin määritys](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Kun olet määrittämässä vientiä Data Lake -tallennustilaan, merkitse seuraavat tiedot muistiin, sillä tiedot on syötettävä myöhemmin:

- <a name="keyVault"></a>Avainsäilön DNS-nimi sekä sovellustunnuksen ja sovelluksen salasanan salaiset nimet. Lisätietoja: [Salaisuuksien lisääminen avainsäilöön](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a>Data Lake -esiintymän tallennustilin nimi. Lisätietoja: [Data Lake Storage (Gen2) -tilin luonti tilaukseen](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Commercen analytiikka (esiversio) -lisäosan ottaminen käyttöön ja määrittäminen

Commercen analytiikka (esiversio) -lisäosan asentaminen edellyttää, että olet ympäristön järjestelmänvalvoja LCS:ssä käytettävässä ympäristössä.

Voit asentaa ja määrittää Commercen analytiikka (esiversio) -lisäosan seuraavasti.

1. Kirjaudu [LCS:ään](https://lcs.dynamics.com/) ja siirry ympäristöösi.
2. Valitse **Ympäristö**-sivun **Ympäristöapuohjelmat**-välilehdessä **Asenna uusi apuohjelma**.
3. Valitse valintaikkunassa **Commercen analytiikka (esiversio)**.

    Jos **Commercen analytiikka (esiversio)** ei ole luettelossa, varmista, että olet mukana Insider-ohjelmassa.

4. Anna seuraavat tiedot **Apuohjelman määritys** -valintaikkunassa.

    | Ilmoitus | Lähde | Esimerkkiarvo |
    |---|---|---|
    | Ympäristösi Azure AD -vuokraajan tunnus | Kirjaudu sisään [Azure-portaaliin](https://portal.azure.com/) ja avaa **Azure Active Directory** -palvelu. Avaa sitten **Ominaisuudet**-sivu ja kopioi **Hakemistotunnus**-kentän arvo. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | Avainsäilön DNS-nimi | Anna avainsäilön [DNS-nimi](#keyVault). Tämä arvo olisi pitänyt ottaa muistiin edellisessä osassa. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Salaisuus, joka sisältää sovellustunnuksen | Kirjoita [sen salaisuuden nimi, johon sovellustunnus on tallennettu](#keyVault). Tämä arvo olisi pitänyt ottaa muistiin edellisessä osassa. | sovelluksen tunnus |
    | Salaisuus, joka sisältää sovelluksen salasanan | Kirjoita [sen salaisuuden nimi, johon sovelluksen salasana on tallennettu](#keyVault). Tämä arvo olisi pitänyt ottaa muistiin edellisessä osassa. | sovelluksen salainen koodi |

5. Hyväksy tarjouksen ehdot valitsemalla valintaruutu ja valitsemalla sitten **Asenna**.

    Järjestelmä asentaa ja määrittää Commercen analytiikka (esiversio) -lisäosan ympäristöä varten. Tämä prosessi voi kestää muutamia minuutteja. Kun se on valmis, **Commercen analytiikka (esiversio)** näkyy **Ympäristö**-sivulla, ja tilan tulee olla **Asennettu**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>SAS-tunnuksen luominen tallennustilille

SAS-tunnuksen avulla ulkoiset yksiköt voivat käyttää tallennustiliäsi ja käyttää tiettyä käyttöoikeusjoukkoa tietyn ajan sisällä. Azure Synapse käyttää SAS-tunnuksen avulla Data Lake -tallennustilan pohjana olevia tietoja.

> [!NOTE]
> Commercen analytiikan (esiversio) tunnetun rajoituksen vuoksi Azure Synapse -esiintymä ei enää saa käyttöoikeutta Data Lake -tallennustilaan sen jälkeen, kun SAS tunnuksen voimassaolo päättyy. Kun siis muodostat SAS-tunnuksen, sinun on määritettävä organisaation suojauskäytäntöjen salliman vanhenemisajan enimmäispäivämäärä.

Luo SAS-tunnus noudattamalla seuraavia ohjeita.

1. Siirry Azure-portaalissa [tallennustilille](#storageAccount), jonka olet luonut määrittäessäsi vientiä Data Lake -tallennustilaan.
2. Valitse tallennustilin vasemmanpuoleisesta ruudusta **Jaetun käyttöoikeuden allekirjoitus**.
3. Määritä **SAS-asetukset** -sivulla seuraavat kentät.

    | Kenttä | Arvo |
    |---|---|
    | Sallitut palvelut | Valitse **Blob**. |
    | Sallitut resurssityypit | Valitse **Palvelu**, **Säilö** ja **Objekti**. |
    | Sallitut käyttöoikeudet | Valitse **Luku**, **Kirjoitus**, **Poisto**, **Luettelo**, **Lisäys** ja **Luonti**. |
    | Blob-versioinnin käyttöoikeudet | Valitse **Ottaa versioiden poiston käyttöön**. |
    | Alkamisen ja vanhentumisen päivämäärä ja -aika | Määritä SAS-tunnuksen aloitus- ja lopetuspäivämäärä ja -kellonaika tarpeen mukaan. |
    | Sallitut IP-osoitteet | Jätä tämä kenttä tyhjäksi. |
    | Sallitut protokollat | Valitse **Vain HTTPS**. |
    | Ensisijainen reititystaso | Valitse **Perus (oletus)**. |
    | Allekirjoitusavain | Valitse **key1** tai **key2** tarpeen mukaan. |

4. Valitse **Luo SAS ja yhteysmerkkijono**.
5. Kopioi arvo **SAS-tunnus** -kentästä ja liitä se tekstieditoriin, kuten Muistioon.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>Lataa Azure Synapse -näkymien käyttöönoton komentosarjat

Voit luoda ja julkaista tarvittavat näkymät Azure Synapse workspacessa, kun suoritat komentosarjojen joukon. Lataa komentosarjat seuraavasti.

1. Siirry GitHubissa [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -tietovarastoon (repo).
2. Voit ladata komentosarjat paikalliseen tietokoneeseen kloonaamalla säilön tai lataamalla sen zip-tiedostona.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Azure Synapse workspacen asentaminen ja konfiguroiminen

Asenna ja määritä Azure Synapse workspace noudattamalla seuraavia vaiheita.

1. Asenna Azure Synapse workspace Azure-tilaukseesi. Lisätietoja on kohdassa [Pika-aloitus: Synapse workspacen luominen](/azure/synapse-analytics/quickstart-create-workspace).
2. Avaa Notepadissa tai toisella tekstieditorilla **SetupSynapse.sql** -komentosarjatiedosto sen paikallisen tietokoneen kansiosta, jonka kloonasit tai latasit Dynamics365Commerce.Solutions-säilöstä edellisessä osassa. Komentosarjatiedosto sijaitsee /Pipeline/CommerceAnalyticsSynapse/-kansiossa. Korvaa komentotiedostossa paikkamerkin teksti arvoilla, jotka näkyvät seuraavassa taulukossa.

    | Paikkamerkkiteksti | Korvaava arvo |
    |---|---|
    | placeholder_storageaccount | Sen [tallennustilin](#storageAccount) nimi, jonka olet luonut määrittäessäsi vientiä Data Lake -tallennustilaan. |
    | <a name="phContainer"></a>placeholder_container | Data Lake -esiintymässä luodun tallennussäilön nimi sen jälkeen, kun olet asentanut LCS:ssä Vie Data Lake -tallennustilaan -lisäosan. Jotta voit käyttää säilön nimeä, sinun on selattava tallennustiliä käyttäen tallennustilan hallintaa Azure-portaalissa. |
    | placeholder_sastoken | Luomasi [SAS-tunnus](#getSASToken). Varmista, että poistat kysymysmerkin (**?**) SAS-tunnuksen alusta. |
    | <a name="phUserPwd"></a>placeholder_password | Valitsemasi vahva salasana. Kirjoita salasana muistiin. Se määritetään uuden **reportreadonlyuser**-tilin salasanaksi, jonka komentosarja luo. **Älä** kirjoita **sqladminuser**-tilin salasanaa. |

3. Kopioi komentosarjatiedoston päivitetty sisältö.
4. Siirry Azure-portaalissa uuteen Azure Synapse workspace -työtilaan. Valitse **Yhteenveto**-sivulta **Avaa Synapse Studio**.
5. Valitse Synapse Studiossa **Uusi \> SQL-komentosarja** ja liitä komentosarjatiedoston sisältö SQL-komentosarjaeditoriin.
6. Varmista, että **Käytä tietokantaa**-kentän arvoksi on määritetty **master**.
7. Valitse **Suorita** ja odota komentosarjan suorittamisen valmistumista. Komentosarjan suorituksen onnistuminen luo tietokannan Commercen analytiikalle, käyttäjätiedot, jotka käyttävät Data Lake -tallennustilaa, ja vain luku -käyttäjätilin, jota Power BI -käyttää yhteyden muodostamiseen Azure Synapse -instanssiin.
8. Avaa Windows PowerShell paikallisessa tietokoneessa järjestelmänvalvojatilassa ja siirry /Pipeline/CommerceAnalyticsSynapse/-kansioon kansiossa, jonka olet kloonannut tai ladannut Dynamics365Commerce.Solutions-säilöstä.
9. Määritä Windows PowerShellin suorituskäytäntö suorittamalla seuraava komento.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Jos SQL Server PowerShell -moduulia ei ole vielä asennettu, asenna se suorittamalla seuraava komento.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Moduulin asennuksen aikana näyttöön saattaa tulla kehote asentaa NuGet-palveluntarjoaja. Valitse tässä tapauksessa **Y** asentaaksesi NuGet-palveluntarjoajan. Ohjelma saattaa kehottaa myös tiedostamaan, että asennat moduuleita epäluotettavasta tietovarastosta. Valitse tässä tapauksessa **Y** jatkaaksesi asennusta. Voit halutessasi käyttää **Set-PSRepository** -cmdlet-cmdlet-komentoa, kun haluat luottaa **PSGallery**-tietovarastoon.

11. Julkaise Azure Synapse -näkymät suorittamalla seuraava komento.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Kun suoritat tätä komentoa, korvaa paikkamerkki arvoilla, jotka näkyvät seuraavassa taulukossa.

    | Paikkamerkin arvo | Korvaava arvo |
    |---|---|
    | SERVER_NAME | Azure Synapse Serverless SQL -päätepisteen nimi. Voit saada tämän arvon Azure Synapse workspacen **Yhteenveto**-sivulta Azure-portaalissa. |
    | PASSWORD | **sqladminuser**-tilin salasana. |
    | STORAGE_ACCOUNT | Data Lake -tallennustilan tallennustilin nimi. |
    | CONTAINER_NAME | Vie Data Lake -tallennustilaan -ominaisuuden luoman säilön nimi. Tämä säilö on sama säilö, jonka olet määrittänyt [placeholder_container](#phContainer)-säilöksi vaiheessa 2. |
    | DATA_ROOT_PATH | Kansion nimi säilössä, joka sisältää kaikki tiedot. |

    > [!NOTE]
    > Voit etsiä tallennustilin nimen, säilön nimen ja tietojen juuripolun käyttäen Azure-tallennustilan selainta ja Data Lake -tallennustiliä Azure-portaalissa.

12. Odota komentosarjan suorittamisen valmistumista. Komentosarjan suorittaminen onnistuneesti luo SQL-näkymät Azure Synapse Serverless SQL -esiintymään.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI -mallisovelluksen asentaminen

Voit asentaa Commercen analytiikalle (esiversio) Power BI -mallisovelluksen seuraavasti.

1. Kirjaudu sisään [Power BI -portaaliin](https://powerbi.microsoft.com/) organisaatiotunnustasi käyttäen.
2. Asenna Commercen analytiikan (esiversio) Power BI -mallisovellus siirtymällä osoitteeseen [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Näyttöön voi tulla varoitus, joka varoittaa, että sovellusta ei ole AppSourcen luettelossa. Valitse **Asenna**.
3. Jos asennat sovelluksen ensimmäistä kertaa, siirry suoraan vaiheeseen 5. Jos olet asentanut tämän sovelluksen ennen, näkyvissä ovat seuraavat sovelluksen päivitysasetukset:

    - **Päivitä työtila ja sovellus** – Päivitä aiemmin luotu mallisovellus ja korvaa aiemmin luodut sovelluksen asetukset, kuten sovellusinstanssin nimi ja käyttöoikeuskonfiguraatiot.
    - **Päivitä vain työtilan sisältö päivittämättä sovellusta** – Päivitä aiemmin luotu mallisovellus mutta säilytä sovelluksessa olevat asetukset. *Tämä vaihtoehto on suositeltava sovelluspäivitysten vaihtoehto.*
    - **Asenna sovelluksesta toinen kopio uuteen työtilaan** – Luo uusi työtila ja luo sitten aiemmin luodun mallisovelluksen kopio siihen. Aiemmin luotu työtila jätetään ennalleen.

4. Valitse jokin päivitysvaihtoehdoista ja valitse sitten **Asenna**.
5. Avaa asennettu sovellus valitsemalla **Sovellukset** vasemmassa ruudussa ja valitsemalla sitten sovellus.
6. Yhdistä sovellus tietolähteeseen valitsemalla **Yhdistä**. Jos olet asentanut sovelluksen ennen, valitse **Yhdistä tietoihin** -linkki keltaisessa sanomapalkissa.
7. Määritä seuraavat kentät.

    | Kenttä | Arvo |
    |---|---|
    | Palvelin | Kirjoita edellisessä osassa luomasi Azure Synapse Serverless SQL -päätepisteen nimi. Voit saada tämän arvon Azure Synapse workspacen **Yhteenveto**-sivulta Azure-portaalissa. |
    | Tietokanta | Kirjoita **CommerceAnalytics**. |
    | Kieli | Valitse arvo luettelosta. Tätä kenttää käytetään lokalisoitujen tuotteiden ja luokkien nimissä. Arvon kirjainkoolla on merkitystä. |
    | Päivämääräalue | Valitse arvo luettelosta. Valitun kuukausien määrän tiedot tuodaan Power BI -tietojoukkoon. Valittava arvo vaikuttaa tietojoukon kokoon ja synkronoinnissa tarvittavaan aikaan. |

8. Valitse **Seuraava**. Järjestelmä pyytää määrittämään tunnistetiedot Azure Synapse SQL -tietokantaan yhdistämistä varten. Määritä kentät seuraavassa taulukossa ilmaistulla tavalla.

    | Kenttä | Arvo |
    |---|---|
    | Todentamismenetelmä | Valitse **Perus**. |
    | Käyttäjänimi | Kirjoita **reportreadonlyuser**. |
    | Salasana | Kirjoita arvo, jolla korvasit [placeholder_password](#phUserPwd)-paikkamerkin SetupSynapse.sql-komentosarjassa. Tämä salasana on **reportreadonlyuser**-tilin salasana. |

9. Valitse **Kirjaudu ja yhdistä**.
10. Odota, kunnes tietojoukko päivitetään onnistuneesti. Avaa sitten sovelluksen työtila valitsemalla **Muokkaa sovellusta** -painike, jossa voit tarkastella tietojoukon päivitystilaa. Sovelluksen työtilassa voit myös määrittää tietojoukolle automaattisia päivitysaikatauluja, hallita käyttöoikeuksia ja nimetä sovelluksen esiintymän uudelleen.

### <a name="privacy"></a><a name="privacy"></a>Tietosuoja

Tietosuojasi on meille tärkeä. Lisätietoja on [tietosuojalausekkeessa](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
