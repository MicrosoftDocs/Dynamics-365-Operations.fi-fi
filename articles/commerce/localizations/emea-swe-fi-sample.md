---
title: Tarkistusyksikön integrointimalli – Ruotsi
description: Tämä ohjeaihe on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Ruotsi).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: ace1bd5b1a06317b6753a34779ecfa96e519a63e
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077010"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Tarkistusyksikön integrointimalli – Ruotsi

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Ruotsi).

> [!NOTE]
> Tässä esimerkissä verointegraatiotoiminto korvaa aiemman [POS-integrointi tarkistusyksiköiden kanssa -esimerkin (Ruotsi)](retail-sdk-control-unit-sample.md)kanssa. Aiempi malli ei hyödynnä [verointegraatiokehystä](./fiscal-integration-for-retail-channel.md), ja se vanhentuu myöhemmissä päivityksissä. Tietoja siitä, miten voit siirtyä aiemmasta esimerkistä Dynamics 365 Commerce -versiota **10.0.22 ja aiempia versioita** vastaavaan esimerkkiin on kohdassa [Siirtyminen aiemmasta integrointiesimerkistä](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Ruotsin Commerce-toiminto sisältää myyntipisteen (POS) esimerkki-integroinnin Ruotsin ominaisuuksiin kuuluvan verolaitteiden kanssa, joita kutsutaan *tarkistusyksiköiksi*. Tämä esimerkki laajentaa [kirjanpidon integrointitoimintoja](fiscal-integration-for-retail-channel.md). Oletetaan, että tarkistusyksikkö on fyysisesti liitetty Hardware stationiin, johon myyntipiste on liitetty. Tässä esimerkissä käytetään esimerkiksi Retail Innovation HTT AB:n [CleanCash Type A](https://www.retailinnovation.se/produkter) tarkistusyksikön ohjelmointirajapintaa (API). Käytössä on CleanCash API -versio 1.1.4.

Näyte toimitetaan lähdekoodin muodossa, ja se on osa Retail-ohjelmiston kehityssarjaa (SDK).

Microsoft ei julkaise Retail Innovation HTT AB:n laitteistoja, ohjelmistoja tai dokumentaatioita. Jos haluat lisätietoja tarkistusyksikön hankkimisesta ja käyttämisestä, ota yhteyttä [Retail Innovation HTT AB:hen](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Skenaariot

Ruotsin tarkistusyksikön integrointiesimerkki sisältää seuraavat toiminnot:

- Myynti-, palautus- ja kuittikopiot rekisteröidään automaattisesti ohjausyksikköön, joka on liitetty myyntipisteeseen liitettyyn Hardware stationiin.
- Rekisteröidyn tapahtuman ohjauskoodi ja valmistusnumero siepataan tarkistusyksiköstä ja tallennetaan tapahtumaan. Näitä tietoja kutsutaan myös *verovastaukseksi*. Verovastausta voi tarkastella **Myymälän tapahtumat** -sivulla.
- Ohjauskoodin ja ohjausyksikön valmistusnumeron mukautetut kentät voidaan lisätä kuitin asetteluun. Näin voit tulostaa tapahtuman verovastauksen kuittiin.
- Tapahtuman verovastaus näkyy **Sähköinen kirjauskansio (Ruotsi)** -kanavaraportissa.
- Käytettävissä on useita virheenkäsittelyvaihtoehtoja. Seuraavassa on muutamia esimerkkejä:

    - Yritä uudelleen rekisteröintiä, jos uudelleenyritys on mahdollista. Voit yrittää verorekisteröintiä uudelleen, jos esimerkiksi ohjausyksikköä ei ole liitetty, se ei ole valmis tai se ei vastaa.
    - Lykkää kirjanpidon rekisteröintiä.
    - Ohita verorekisteröinti tai merkitse tapahtuma rekisteröidyksi ja sisällytä tietokoodit, jotka poimivat virheen syyn ja lisätiedot.
    - Tarkista tarkistusyksikön käytettävyys ennen uuden myyntitapahtuman avaamista tai myyntitapahtuman viimeistelyä.

### <a name="limitations-of-the-sample"></a>Esimerkin rajoitukset

Ruotsin tarkistusyksikön integrointiesimerkki ei tällä hetkellä tue asiakastilausskenaarioita.

## <a name="setting-up-the-integration-with-control-units"></a>Integroinnin määritys tarkistusyksiköiden kanssa

Lisätietoja Ruotsin pakollisesta määrityksestä on kohdassa [Commercen määritys (Ruotsi)](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Ruotsin maakohtaisten kuittien konfiguroiminen

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfiguroi mukautetut kentät siten, että niitä voidaan käyttää myyntikuittien kuittimuodoissa

Voit konfiguroida POS-kuittimuodoissa käytettävät kielitekstit ja mukautetut kentät. Kuittiasetukset luoneen käyttäjän oletusyrityksen tulee olla sama yritys, jossa kielitekstiasetukset luodaan. Vaihtoehtoisesti samat kielitekstit tulisi luoda sekä käyttäjän oletusyrityksessä että sen myymälän yrityksessä, jota varten asetukset luodaan.

Lisää **Kieliteksti**-sivulla seuraavat tietueet kuitin asettelun mukautettujen kenttien otsikoihin. Huomaa, että taulukossa näkyvät **kielitunnukset**, **tekstitunnukset** ja **tekstiarvot** ovat vain esimerkkejä. Voit muuttaa ne tarpeidesi mukaisiksi. Käyttämäsi **tekstin tunnuksen** arvon on kuitenkin oltava yksilöivä, ja niiden on oltava yhtä suuret tai suurempia kuin 900001.

Lisää seuraavat myyntipisteen otsikot **Kieliteksti**-sivun **POS**-osaan.

| Kielitunnus | Tekstitunnus | Teksti                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Rekisteröi hallintakoodi |
| en-US       | 900002  | Rekisteröi laite       |

Lisää **Mukautetut kentät** -sivulla seuraavat tietueet kuitin asettelun mukautettuihin kenttiin. Huomaa, että **otsikkotekstin tunnuksen** arvojen on vastattava **Kieliteksti**-sivulla määritettyjä **tekstitunnuksen** arvoja.

| Nimi                         | Tyyppi    | Otsikon tekstin tunnus |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Vastaanotto | 900001          |
| SE_FISCALREGISTERID          | Vastaanotto | 900002          |

> [!NOTE]
> On tärkeää määrittää oikeat mukautetut kenttien nimet edellisen taulukon mukaan. Virheellisen mukautetun kentän nimi aiheuttaa kuiteissa puuttuvia tietoja.

#### <a name="configure-receipt-formats"></a>Kuittimuotojen määrittäminen

Muuta jokaisessa vaaditussa kuittimuodossa **Tulostustoiminta**-kentän arvoksi **Tulosta aina**.

Lisää kuittien muodon suunnittelussa seuraavat mukautetut kentät **Alatunniste**-osaan. Huomaa, että kenttien nimet vastaavat tämän aiheen edellisessä osassa määritettyjä kielitekstejä.

- **Rekisteröi ohjauskoodi** – Tämä kenttä tulostaa ohjauskoodin.
- **Rekisteröi laite** – Tämä kenttä tulostaa ohjausyksikön valmistusnumeron.

Lisätietoja kuittimuotojen käsittelystä on kohdassa [Kuittimallit ja tulostaminen](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Kirjanpidon integroinnin määrittäminen (Ruotsi)

Ruotsin tarkistusyksikön esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\CleanCash** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on Commerce runtimen (CRT) ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja: [Tarkistusyksikön integrointiesimerkkiä koskevat käyttöönoton ohjeet (Ruotsi) (vanha)](emea-swe-fi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

Suorita verointegraation määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla.

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ota myös huomioon verorekisteröintiprosessin asetukset, jotka [liittyvät tähän tarkistusyksikön integraatioesimerkkiin](#set-up-the-registration-process).
1. [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Rekisteröintiprosessin määrittäminen

Voit ottaa rekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita. Lisätietoja on kohdassa [Commerce-kanavan verointegroinnin määritys](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot.

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan (esim. **[julkaisu 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avaa **src \> FiscalIntegration \> CleanCash**.
    1. Lataa veroasiakirjan tarjoajan konfigurointitiedosto kohdasta **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Lataa veroliittimen konfiguraatiotiedosto kohdasta **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Tämän verointegraatioesimerkin konfiguraatiotiedostot sijaitsevat seuraavissa Retail SDK -sovelluksen kansioissa kehittäjän virtuaalikoneessa LCS:ssä:
    >
    > - **Veroasiakirjan tarjoajan konfigurointitiedosto:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Veroyhdistimen konfigurointitiedosto:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**. Määritä **Yleiset**-pikavälilehdessä **Ota kirjanpidon integrointi käyttöön**-asetukseksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**, ja lataa aiemmin lataamasi kirjanpitoasiakirjan toimittajan konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**, ja lataa aiemmin lataamasi kirjanpidon yhdistimen konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**. Luo uusi yhdistimen toimintoprofiili. Valitse tiedoston tarjoaja ja aiemmin ladattu liitin. Päivitä [tietojen määritysasetukset](#default-data-mapping) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**. Luo uusi liittimen tekninen profiili ja valitse aiemmin ladattu veroliitin. Päivitä [yhdistimen asetukset](#fiscal-connector-settings) tarvittaessa.
6. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmät**. Luo uusi veroliitinryhmä aiemmin luomallesi liittimen toimintoprofiilille.
7. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**. Luo uusi kirjanpidon rekisteröintiprosessi ja verorekisteröintiprosessi vaihe ja valitse aiemmin luomasi kirjanpidon yhdistinryhmä.
8. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Valitse siihen myymälään linkitetty toimintoprofiili, jossa rekisteröintiprosessi tulee aktivoida. Valitse **Kirjanpidon rekisteröintiprosessi** -pikavälilehdessä aiemmin luomasi kirjanpidon rekisteröintiprosessi.
9. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**. Valitse Hardware stationiin liitetty laiteprofiili, johon verotulostin liitetään. Valitse **Kirjanpidon oheislaitteet** -pikavälilehdessä aiemmin luomasi liittimen tekninen profiili.
10. Avaa jakeluaikataulu (**Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**) ja valitse työt **1070** ja **1090** siirtääksesi tiedot kanavatietokantaan.

#### <a name="default-data-mapping"></a>Tietojen oletusmääritys

Seuraavat tietojen oletusmääritykset sisältyvät veroasiakirjan tarjoajan konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Arvonlisäverokoodimääritys** – Tämä määritys asettaa laitekohtaiset arvonlisäverokoodit vastaaviin arvonlisäverokoodeihin. ALV-koodin määrityksen muodon tulee olla seuraava:

    ```
    1 : code1 ; 2 : code2
    ```

    Selitys tästä muodosta:

    - *1* ja *2* ovat laitekohtaisia ALV-koodeja.
    - Puolipistettä (;) käytetään erottimena.
    - *code1* ja *code2* ovat arvonlisäverokoodeja, jotka on konfiguroitu Commerce headquarters -sovelluksessa. Esimerkkiyhdistämismääritystä on muokattava sovelluksessa konfiguroitujen verokoodien mukaan.

    Tarkistusyksiköt tukevat enintään neljää erilaista ALV-koodia. Näin ollen ALV-koodimääritys voidaan määrittää seuraavasti:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Samaan laitekohtaiseen ALV-koodiin voi määrittää useita arvonlisäverokoodeja.

#### <a name="fiscal-connector-settings"></a>Veroliittimen asetukset

Seuraavat asetukset sisältyvät veroyhdistimen konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Yhteysmerkkijono** – tarkistusyksikön yhteysasetukset.
- **Aikakatkaisu** – Aika millisekunteina, jonka ajuri odottaa tarkistusyksikön vastausta.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Tarkistusyksikön integrointiesimerkkiä koskevat käyttöönoton ohjeet (Ruotsi) (vanha)](emea-swe-fi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

#### <a name="set-up-the-development-environment"></a>Kehitysympäristön määrittäminen

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa esimerkkiä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Retail SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
1. Avaa tarkistusyksikön integraatioratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** ja muodosta se.
1. Asenna CRT-laajennukset:

    1. Etsi CRT-laajennuksen asennusohjelma:

        - **Commerce Scale Unit:** Etsi **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461**-kansiosta **ScaleUnit.CleanCash.Installer**-asennusohjelma.
        - **Paikallinen CRT Modern POS -sovelluksessa:** Etsi **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** -kansiosta **ModernPOS.CleanCash.Installer**-asennusohjelma.

    2. Käynnistä CRT-laajennusten asennusohjelma komentoriviltä:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Paikallinen CRT Modern POS -sovelluksessa:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Asenna Hardware station -laajennukset:

    1. Etsi **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461**-kansiosta **HardwareStation.CleanCash.Installer**-asennusohjelma.
    1. Käynnistä laajennusten asennusohjelma komentoriviltä:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tuotantoympäristö

Luo ja julkaise verointegraatioesimerkin Cloud Scale Unit ja itsepalveluna käyttöönotettavat paketit noudattamalla [Määritä koontijakso verointegraatioesimerkille](fiscal-integration-sample-build-pipeline.md) -ohjeen vaiheita. **CleanCash build-pipeline.yml**-niminen YAML-mallitiedosto löytyy **Pipeline\\YAML_Files** -kansiosta[Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilöstä.

## <a name="design-of-the-extensions"></a>Laajennusten rakenne

Ruotsin tarkistusyksikön esimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\CleanCash** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on CRT:n ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Tarkistusyksikön integrointiesimerkkiä koskevat käyttöönoton ohjeet (Ruotsi) (vanha)](emea-swe-fi-sample-sdk.md). Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

### <a name="crt-extension-design"></a>CRT-laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä tarkistusyksikön vastauksia.

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjapalvelua varten on yksi pyynnön käsittelijä, **DocumentProviderCleanCash**. Tämän käsittelijän avulla luodaan veroasiakirjoja tarkistusyksikköä varten.

Tämä käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä tarkistusyksikköön.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Myyntitapahtumia ja kirjaustapahtumia tuetaan tällä hetkellä.

#### <a name="configuration"></a>Konfigurointi

Veroasiakirjan tarjoajan konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla tiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida tarkistusyksikön kanssa. Se käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo tarkistusyksikköön. Se käsittelee myös tarkistusyksiköstä saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**CleanCashHandler**-pyyntökäsittelijä on tarkistusyksikön pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja tarkistusyksikköön ja palauttaa vastauksen pyyntöön.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään tarkistusyksikön kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään tarkistusyksikön alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Veroyhdistimen konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
