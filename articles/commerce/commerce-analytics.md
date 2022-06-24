---
title: Commercen analytiikka (esiversio)
description: Tässä artikkelissa kerrotaan, miten analytiikkaominaisuuden voi asentaa ja käyttää Microsoft Dynamics 365 Commercessa.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 9ffa0affa0b80af65dd2aa37ef2fe969752ae332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887163"
---
# <a name="commerce-analytics-preview"></a>Commercen analytiikka (esiversio)

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka Commercen analytiikka (esiversio) asennetaan. Se on Microsoft Dynamics 365 Commerceen sisältyvä toiminnallisen analytiikan toiminto.

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

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a>Ylätason suodattimet

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

#### <a name="products"></a><a name="ProductsPage"></a> Tuotteet

- Myynti
- Reunus
- Palautukset

#### <a name="customers"></a><a name="CustomersPage"></a> Asiakkaat

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
> Commercen analytiikka (esiversio) on saatavilla esiversiona on Yhdysvalloissa, Kanadassa, Yhdistyneessä kuningaskunnassa, Euroopassa, Kaakkois-Aasiassa, Itä-Aasiassa, Australiassa ja Japanissa. Jos talous- ja toimintoympäristösi sijaitsee näillä alueilla, voit ottaa tämän ominaisuuden käyttöön ympäristössäsi käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palveluita. Ennen kuin voit käyttää tätä toimintoa, katso kohta [Määritä vienti Azure Data Lake -tallennustilaan](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commercen analytiikan (esiversio) ottaminen käyttöön ja määrittäminen

Jos haluat asentaa Commercen analytiikan (esiversio), sinulla on oltava käyttöoikeudet resurssien luontia varten Azure-tilauksessa. Sinulla on oltava myös käyttöoikeudet, jotta voit asentaa lisäosia LCS:ssä.

Voit ottaa käyttöön ja määrittää Commercen analytiikka (esiversio) -ominaisuuden seuraavasti.

1. [Lähetä Commercen analytiikan (esiversio) esiversion sisäänottolomake](#joinPreview)
2. [Data Lake -viennin lisäosan käyttöönotto ja määritys](#enableExportToDataLake).
3. [Azure Synapse workspacen asentaminen ja konfiguroiminen](#configureAzureSynapse).
4. [Lisää salasanat Key Vaultiin](#addSecrets).
5. [Commercen analytiikka (esiversio) -lisäosan ottaminen käyttöön ja määrittäminen](#enableCommerceAnalyticsAddin).
6. [Power BI -mallisovelluksen asentaminen](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Lähetä Commercen analytiikan (esiversio) esiversion sisäänottolomake

Lähetä [Commercen analytiikan (esiversio) esiversion sisäänottolomake](https://forms.office.com/r/vW5VLJGXZ2). Kun pyyntösi on käsitelty, lomakkeessa antamaasi sähköpostiosoitteeseesi lähetetään vahvistussähköposti.

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Data Lake -viennin lisäosan käyttöönotto ja määritys

> [!IMPORTANT]
> Kun määrität Vie Data Lakeen -lisäosan, varmista, että reaaliaikaisia tietojen muutoksia ei ole otettu käyttöön, tyhjentämällä **reaaliaikaiset tietomuutokset** -valintaruudun Vie Data Lakeen -lisäosan asetussivulla. **Reaaliaikainen tietojen muutos** -ominaisuus on esiversiona, eikä Commerce Analytics tue sitä tällä hetkellä. Jos otat ominaisuuden käyttöön, Commerce Analytics ei voi käsitellä tietojasi Data Lakessa, ja useimmissa Power BI -raporteissasi ei näy tietoja.

Commercen analytiikka (esiversio) luottaa Vie Data Lake -tallennustilaan -toimintoon viedäkseen Commerce headquarters -tietoja Data Lake -tallennustilaan ja pitääkseen tiedot ajan tasalla. Ennen Commercen analytiikka (esiversio) -määritystä sinun on otettava käyttöön ja konfiguroitava Data Lake -vienti seuraamalla seuraavia ohjeita: [Azure Data Lake -viennin määritys](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Kun olet määrittämässä Vie Data Lake -tallennustilaan -lisäosaa, merkitse seuraavat tiedot muistiin, sillä tiedot on syötettävä myöhemmin:

- <a name="keyVault"></a>Toimittamasi Key Vaultin DNS-toimialuenimi.
- Toimittamasi salasanojen nimet, jotka sisältävät sovellustunnuksen sekä sovelluksen salasanan. Lisätietoja: [Salaisuuksien lisääminen avainsäilöön](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Azure Synapse workspacen asentaminen ja konfiguroiminen

Commercen analytiikan (esiversio) käyttäminen edellyttää, että Synapse SQL on-demand on valmisteltu Azure Synapse workspacessa. Asenna ja määritä Azure Synapse workspace noudattamalla seuraavia vaiheita.

1. Asenna Azure Synapse workspace Azure-tilaukseesi. Lisätietoja on kohdassa [Pika-aloitus: Synapse workspacen luominen](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a>Kun työtila on valmisteltu, avaa resurssin yhteenvetosivu ja merkitse **Serverless SQL -päätepiste** -arvo muistiin. Tämä arvo on tallennettava Key Vaultiin seuraavassa osiossa.
1. Avaa työtilan Azure Synapse Studio valitsemalla yhteenvetosivulla **Avaa Synapse Studio** -linkki.
1. Valitse vasemmassa valikossa **Hallinta**. Jos haluat tarkastella valikkojen nimiä, sinun on ehkä valittava vasemmanpuoleisen valikon laajennuslinkki.
1. Valitse **Käyttöoikeusryhmä**-kohdasta **Käytönvalvonta**. 
1. Valitse **Lisää**.
1. Määritä roolin määritykset **Lisää roolimääritys** -ruudussa seuraavassa taulukossa kuvatulla tavalla.

    | Vaihtoehto | Arvo |
    |--------|-------|
    | Vaikutusalue | **Työtilan** valitseminen. |
    | Rooli | Valitse **Synapse SQL -järjestelmänvalvoja**.|
    | Valitse käyttäjä | Hae sen sovelluksen nimeä, jonka [loit Vie Data Lakeen -lisäosan asennuksen yhteydessä](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Kun sovellus tulee näkyviin hakutuloksissa, valitse se. Sovellus näkyy nyt **Valitut käyttäjät, ryhmät tai palvelun pääkäyttäjät** -osassa. |

1. Suorita roolimääritys valmiiksi valitsemalla **Käytä**. Sovellukselle myönnetään Synapse SQL -järjestelmänvalvojan oikeudet. Siksi se voi luoda tarvittavat näkymät Commercen analytiikan (esiversio) LCS-lisäosan konfiguroinnin aikana.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Lisää salasanat Key Vaultiin

Seuraavassa taulukossa näkyvät salasanat on lisättävä samaan [Key Vaultiin](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault), jota olet käyttänyt määrittäessäsi Vie Data Lakeen -lisäosan. Sinun on määritettävä kullekin salasanalle salasanan nimi ja määritetty arvo.

| Ehdotettu salaisuuden nimi | Salaisen koodin arvo | Esimerkki salasanan arvosta |
|---------|---------|---------|
| synapse-sql-server | Serverless SQL -päätepistearvo, jonka merkitsit muistiin [Azure Synapse workspacen konfiguroinnissa](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | SQL:n vain luku -käyttäjälle määritettävä salasana. Power BI -raportti käyttää tätä salasanaa palvelimettoman SQL-yhteyden muodostamiseen. Voit määrittää salasanan noudattamalla organisaatiosi salasanakäytäntöjä. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Commercen analytiikka (esiversio) -lisäosan ottaminen käyttöön ja määrittäminen

Commercen analytiikka (esiversio) -lisäosan asentaminen edellyttää, että olet ympäristön järjestelmänvalvoja LCS:ssä käytettävässä ympäristössä.

Voit asentaa ja määrittää Commercen analytiikka (esiversio) -lisäosan seuraavasti.

1. Kirjaudu [LCS:ään](https://lcs.dynamics.com/) ja siirry ympäristöösi.
2. Valitse **Ympäristö**-sivun **Ympäristöapuohjelmat**-välilehdessä **Asenna uusi apuohjelma**.
3. Valitse valintaikkunassa **Commercen analytiikka (esiversio)**.
4. Anna seuraavat tiedot **Apuohjelman määritys** -valintaikkunassa.

    | Tietoja | Lähde | Esimerkkiarvo |
    |---|---|---|
    | Azure Active Directory (Azure AD) -vuokraajan tunnus | Kirjaudu sisään [Azure-portaaliin](https://portal.azure.com/) ja avaa **Azure Active Directory** -palvelu. Avaa sitten **Ominaisuudet**-sivu ja kopioi **Vuokraajan tunnus**-kentän arvo. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | Azure Key Vaultin DNS-nimi | Anna avainsäilön DNS-nimi. Tämä arvo olisi pitänyt merkitä muistiin, kun [konfiguroit Vie Data Lakeen -lisäosaa](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Salaisuuden nimi, joka sisältää sovellustunnuksen | Kirjoita sen salaisuuden nimi, johon sovellustunnus on tallennettu. Tämä arvo olisi pitänyt merkitä muistiin, kun [konfiguroit Vie Data Lakeen -lisäosaa](#keyVault). | `app-id` |
    | Salaisuuden nimi, joka sisältää sovelluksen salasanan | Kirjoita sen salaisuuden nimi, johon sovelluksen salasana on tallennettu. Tämä arvo olisi pitänyt merkitä muistiin, kun [konfiguroit Vie Data Lakeen -lisäosaa](#keyVault). | `app-secret` |
    | Salasanan nimi, joka sisältää Azure Synapsen palvelimettoman SQL-päätepisteen | Kirjoita sen salaisuuden nimi, johon palvelimeton SQL-päätepiste on tallennettu. Sinun olisi pitänyt luoda salaisuus, [kun olet lisännyt salasanoja avainarvoon](#addSecrets). | `synapse-sql-server` |
    | Salasanan nimi, joka sisältää SQL:n vain luku -käyttäjille määritettävän salasanan Azure Synapsessa | Kirjoita palvelimettoman SQL:n vain luku -käyttäjälle määritettävän salasanan tallentavan salaisuuden nimi. Tämä käyttäjä luodaan sinulle, ja sitä tulee käyttää Power BI -raportissa yhteyden muodostamiseen palvelimettomaan SQL-palvelimeen. Sinun olisi pitänyt luoda salaisuus, [kun olet lisännyt salasanoja avainarvoon](#addSecrets). | `readonly-sql-pwd` |

1. Hyväksy tarjouksen ehdot valitsemalla valintaruutu ja valitsemalla sitten **Asenna**.

    Järjestelmä asentaa ja määrittää Commercen analytiikka (esiversio) -lisäosan ympäristöä varten. Tämä prosessi voi kestää muutamia minuutteja. Kun se on valmis, **Commercen analytiikka (esiversio)** näkyy **Ympäristö**-sivulla, ja tilan tulee olla **Asennettu**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI -mallisovelluksen asentaminen

Voit asentaa Commercen analytiikalle (esiversio) Power BI -mallisovelluksen seuraavasti.

1. Kirjaudu sisään [Power BI -portaaliin](https://powerbi.microsoft.com/) organisaatiotunnustasi käyttäen.
1. Asenna Commercen analytiikan (esiversio) Power BI -mallisovellus siirtymällä osoitteeseen [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Vaihtoehtoisesti voit käydä [AppSource-sivulla: Dynamics 365 Commerce Analytics](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics), ja valita **Hanki nyt**.
1. Jos asennat sovelluksen ensimmäistä kertaa, siirry suoraan vaiheeseen 5. Jos olet asentanut sen aiemmin, käytössä ovat seuraavat sovelluksen päivitysasetukset:

    - **Päivitä työtila ja sovellus** – Päivitä aiemmin luotu mallisovellus ja korvaa aiemmin luodut sovelluksen asetukset, kuten sovellusinstanssin nimi ja käyttöoikeuskonfiguraatiot.
    - **Päivitä vain työtilan sisältö päivittämättä sovellusta** – Päivitä aiemmin luotu mallisovellus mutta säilytä sovelluksessa olevat asetukset. *Tämä vaihtoehto on suositeltava sovelluspäivitysten vaihtoehto.*
    - **Asenna sovelluksesta toinen kopio uuteen työtilaan** – Luo uusi työtila ja luo sitten aiemmin luodun mallisovelluksen kopio siihen. Aiemmin luotu työtila jätetään ennalleen.

1. Valitse jokin päivitysvaihtoehdoista ja valitse sitten **Asenna**.
1. Avaa asennettu sovellus valitsemalla **Sovellukset** vasemmassa ruudussa ja valitsemalla sitten sovellus.
1. Yhdistä sovellus tietolähteeseen valitsemalla **Yhdistä**. Jos olet asentanut sovelluksen ennen, valitse **Yhdistä tietoihin** -linkki keltaisessa sanomapalkissa.
1. Määritä seuraavat kentät.

    | Kenttä | Arvo |
    |---|---|
    | Palvelin | Määritä palvelimeton SQL-päätepiste, jonka olet merkinnyt muistiin [Azure Synapse workspacen luomisen](#serverlessep) jälkeen. |
    | Tietokanta | Kirjoita **CommerceAnalytics**. |
    | Kieli | Valitse arvo luettelosta. Tätä kenttää käytetään lokalisoitujen tuotteiden ja luokkien nimissä. Arvon kirjainkoolla on merkitystä. |
    | Päivämääräalue | Valitse arvo luettelosta. Valitun kuukausien määrän tiedot tuodaan Power BI -tietojoukkoon. Valittava arvo vaikuttaa tietojoukon kokoon ja synkronoinnissa tarvittavaan aikaan. |

1. Valitse **Seuraava**. Kun järjestelmä pyytää määrittämään Azure Synapse SQL -tietokantaan yhteyden muodostamisen käyttöoikeudet, määritä kentän arvot seuraavan taulukon mukaisesti.

    | Kenttä | Arvo |
    |---|---|
    | Todentamismenetelmä | Valitse **Perus**. |
    | Käyttäjänimi | Kirjoita **reportreadonlyuser**. |
    | Salasana | Kirjoita salasana, jonka [tallensit SQL:n vain luku -käyttäjälle Key Vaultissa](#roUser). |

1. Valitse **Kirjaudu ja yhdistä**.
1. Odota, kunnes tietojoukko on päivitetty onnistuneesti. Avaa sitten sovelluksen työtila valitsemalla **Muokkaa sovellusta**. Työtilassa voit tarkastella tietojoukon päivitystilaa. Sovelluksen työtilassa voit myös määrittää tietojoukolle automaattisia päivitysaikatauluja, hallita käyttöoikeuksia ja nimetä sovelluksen esiintymän uudelleen.

### <a name="privacy"></a><a name="privacy"></a>Tietosuoja

Tietosuojasi on meille tärkeä. Lisätietoja on [tietosuojalausekkeessa](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
