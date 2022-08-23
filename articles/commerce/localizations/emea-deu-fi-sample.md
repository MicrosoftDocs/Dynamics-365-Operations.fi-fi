---
title: Saksan tilikausirekisteröintipalvelun integroinnin malli
description: Tämä artikkeli on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Saksa).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-05-29
ms.openlocfilehash: 40f2b7ece62c495e4a719121019070a9961fa915
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280303"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Saksan tilikausirekisteröintipalvelun integroinnin malli

[!include[banner](../includes/banner.md)]

Tämä artikkeli on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Saksa).

Vaatimuksille, jotka liittyvät kassojen paikallisiin verotusvaatimuksiin Saksassa, Microsoft Dynamics 365 Commerce -toiminnallisuus Saksalle sisältää esimerkki-integraation myyntipisteestä ulkoiseen verorekisteröintipalveluun. Esimerkki laajentaa [kirjanpidon integrointitoimintoja](fiscal-integration-for-retail-channel.md). Se perustuu [EFSTA](https://www.efsta.eu/de/)-järjestelmän [EFR (Electronic Fiscal Register)](https://www.efsta.eu/de/fiskalloesungen/deutschland) -ratkaisuun, ja se ottaa yhteyden EFR-palveluun HTTPS-protokollan kautta. EFR-palvelun tulee olla isännöity joko Retail Hardware Stationissa tai erillisellä tietokoneella, johon voidaan yhdistää Hardware Stationilta. Näyte toimitetaan lähdekoodin muodossa, ja se on osa Retail-ohjelmiston kehityssarjaa (SDK).

Microsoft ei julkaise EFSTA:n laitteistoja, ohjelmistoja tai dokumentaatioita. Jos haluat lisätietoja EFR-ratkaisun saamiseksi ja sen toiminnan ylläpitämiseksi, ota yhteyttä [EFSTA:han](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Skenaariot

Seuraavat skenaariot ovat Saksan verorekisteröintipalvelun integrointiesimerkistä.

### <a name="sales-operations"></a>Myynnin työvaiheet

- **Käteismyynnin ja palautusten rekisteröiminen kirjanpidon rekisteröintipalveluun:**

    Myyntitoimintojen rekisteröiminen sisältää seuraavat vaiheet:

    1. Tapahtuman aloituksen rekisteröinti

        Kunkin tapahtuman aloitus rekisteröidään EFR-palveluun liitettynä teknisenä suojauselementtinä (TSE). Rekisteröinnin seurauksena TSE määrittää tapahtuman tunnuksen (TID).

    2. Tapahtuman lopetuksen rekisteröinti

        Kun tapahtuma lopetetaan myyntipisteessä, se rekisteröidään käyttäen samaa TID-tunnusta, joka on määritetty tapahtuman alkamisen rekisteröinnin yhteydessä. Kyseisellä hetkellä yksityiskohtaiset tapahtumatiedot lähetetään kirjanpidon rekisteröintipalveluun. Näitä tietoja ovat myyntirivin tiedot sekä alennuksia, maksuja ja veroja koskevat tiedot.

    3. Tallenna vastaus verorekisteröintipalvelusta

        Suojaustiedot vastaanotetaan TSE:stä osana vastausta ja tallennetaan tapahtumaan kanavatietokantaan. Suojaustiedot koostuvat seuraavista tiedoista:

        - TID
        - Tapahtuman alun päivämäärä ja aika
        - Tapahtuman lopun päivämäärä ja aika
        - Allekirjoituslaskuri
        - Tarkistusarvo
        - TSE:n sarjanumero

- **Asiakastilausten rekisteröiminen kirjanpidon rekisteröintipalveluun:** Rekisteröintiprosessi on sama kuin käteismyyntien ja palautusten prosessi.
- **Lahjakortteja ja talletuksia sisältävien toimintojen rekisteröiminen:** Rekisteröintiprosessi on sama kuin käteismyyntien ja palautusten prosessi.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Verorekisteröintivirheistä ilmoittaminen käyttäjille

Kirjanpidon rekisteröintipalvelu voi ilmoittaa käyttäjille verorekisteröinnin epäonnistumisesta kahdella tavalla:

- Tulosta vastauksen lisätiedot kuittien **Tietosanoma**-kenttään.
- Näytä veropalvelun ilmoitukset myyntipisteen käyttäjäsanomina.

    > [!NOTE]
    > Tämä ilmoitusmekanismi edellyttää, että **Näytä kirjanpidon rekisteröinti-ilmoitukset** -parametri **Yhdistimen tekniset profiilit** -sivulla on otettu käyttöön.

#### <a name="printing-receipts"></a>Kuittien tulostaminen

Kuitin tulostaminen on pakollista Saksassa. Kaikkien kuittien on sisällettävä vähintään seuraavat tiedot:

- Yrityksen nimi ja osoite
- Tietoja tavaroista, mukaan lukien tavaroiden hinnat ja määrät
- Tietoja vastaanotetuista maksuista
- Tietoja veroista, mukaan lukien kokonaissummat veroprosentin mukaan
- Suojaustiedot:

    - TID
    - Tapahtuman alun päivämäärä ja aika
    - Tapahtuman lopun päivämäärä ja aika
    - Allekirjoituslaskuri
    - Tarkistusarvo
    - TSE:n sarjanumero

- Tietosanoma

> [!NOTE]
> Kuitteihin voidaan tulostaa myös QR-koodi. Vaikka QR-koodi on valinnainen, se on erittäin suositeltava. Lisätietoja siitä, miten QR-koodin saa osana verorekisteröintipalvelun vastausta, on [EFSTA-dokumentaatiosivulla](https://public.efsta.net/efr/) julkaistussa EFR Guide \[DE\] -oppaassa.
>
> Kuittien **Tietosanoma**-kenttä näyttää ilmoituksen kirjanpidon rekisteröintipalvelusta. Jos esimerkiksi allekirjoituslaite hajoaa, kuittiin voidaan tulostaa erityisteksti.

#### <a name="voided-suspended-and-recalled-transactions"></a>Mitätöidyt, keskeytetyt ja peruutetut tapahtumat

- Mitätöity tapahtuma rekisteröidään pyyntönä lopettaa tapahtuma verorekisteröintipalvelussa.
- Keskeytetty tapahtuma rekisteröidään pyyntönä lopettaa tapahtuma verorekisteröintipalvelussa.
- Keskeytetyn tapahtuman peruutus rekisteröidään uuden tapahtuman aloituksena verorekisteröintipalvelussa.

### <a name="non-sales-transactions-and-shift-closing"></a>Muut kuin myyntitapahtumat ja vuorojen sulkeminen

Seuraavat muut kuin myyntitapahtumat kirjataan kirjanpidon ulkopuolisina toimintoina verorekisteröintipalveluun **NFS**-tunnisteen avulla:

- Tilitä aloitussumma
- Liukuva merkintä
- Maksuvälineen poisto
- Toimitus kassakaappiin
- Toimitus pankkiin
- Tulotilit
- Kulutilit

**Sulje vuoro** -toiminto kirjataan myös kirjanpidon ulkopuolisena toimintona verorekisteröintipalveluun **NFS**-tunnisteen avulla.

### <a name="data-export-and-audit"></a>Tietojen vieminen ja auditointi

Kaikkien tapahtumien on oltava TSE-allekirjoitettuja, jotta niiden eheys, aitous ja täydellisyys voidaan varmistaa. Tämä auttaa ehkäisemään tallennettujen tietojen manipulointia.

> [!WARNING]
> Vain vahvistettua TSE:tä voi käyttää. Lisätietoja EFR-ratkaisun tukemasta TSE-tyypeistä ja -malleista on [EFSTA-dokumentaatiosivustossa](https://public.efsta.net/efr/) julkaistussa EFR Guide \[DE\] -oppaassa. Jos haluat lisätietoja siitä, miten voit valita ja hankkia TSE:n, ota yhteyttä [EFSTA:aan](https://www.efsta.eu/at/kontakt).

Saksan säädökset edellyttävät DSFinV-K-viennin tukea. DSFinV-K-viennin voi käynnistää EFR-ratkaisussa. Lisätietoja DSFinV-K-viennistä on [EFSTA-dokumentaatiosivustossa](https://public.efsta.net/efr/) julkaistussa EFR Guide \[DE\] -oppaassa.

### <a name="limitations-of-the-sample"></a>Esimerkin rajoitukset

Verorekisteröintipalvelu tukee vain skenaarioita, joissa arvonlisävero sisältyy hintoihin. Siksi **Hinnat sisältävät arvonlisäveron** -asetuksen on oltava **Kyllä** sekä myymälöille että asiakkaille.

Veropalvelu ei tue tilanteita, joissa samalle tapahtumariville sovelletaan useita arvonlisäverokoodeja.

Verointegraatiokehys ei tue myyntitarjouksia. Siksi näitä toimintoja ei rekisteröidä veropalveluun.

## <a name="set-up-commerce-for-germany"></a>Commercen määrittäminen (Saksa)

Tässä osassa kuvaillaan Commerce-asetukset, jotka ovat erityisiä ja suositeltuja Saksassa. Lisätietoja määrityksestä on kohdassa [Commerce-aloitussivu](../index.md).

Ennen kuin voit käyttää Saksan maa-/aluekohtaista toimintoa, sinun on määritettävä seuraavat asetukset.

- Määritä yrityksen ensisijaisessa osoitteessa **Maa/alue**-kentän arvoksi **DEU** (Saksa).
- Jos myymälä sijaitsee Saksassa, määritä sen POS-toimintoprofiilissa **ISO-koodi**-kentän arvoksi **DE** (Saksa).

Sinun on määritettävä myös seuraavat asetukset Saksassa. Varmista, että asianmukaiset jakelutyöt suoritetaan asetusten määrityksen jälkeen.

### <a name="set-up-vat-per-german-requirements"></a>Arvonlisäveron määrittäminen Saksan vaatimusten mukaan

Sinun on luotava arvonlisäverokoodit, arvonlisäveroryhmät ja nimikkeen arvonlisäveroryhmät. Määritä myös tuotteiden ja palveluiden arvonlisäverotiedot. Lisätietoja arvonlisävero-ominaisuuksien määrittämisestä ja käyttämisestä on ohjeaiheessa [Arvonlisäveron yleiskatsaus](../../finance/general-ledger/indirect-taxes-overview.md).

Myyntikuitteihin voidaan tulostaa arvonlisäverokoodin lyhenne (esimerkiksi "A" tai "B"). Voit ottaa tämän toiminnon käyttöön asettamalla **Arvonlisäverokoodit**-sivun **Tulostuskoodi**-kentän.

### <a name="set-up-stores"></a>Määritä myymälät

Päivitä myymälän tiedot **Kaikki myymälät** -sivulla. Määritä erityisesti seuraavat parametrit:

- Määritä **Arvonlisäveroryhmä**-kentässä arvonlisäveroryhmä, jota pitäisi käyttää myynnissä oletusasiakkaalle.
- Määritä **Hinnat sisältävät arvonlisäveron** -vaihtoehdon arvoksi **Kyllä**.
- Määritä **Nimi**-kenttään yrityksen nimi. Muutoksen avulla voidaan varmistaa, että yrityksen nimi näkyy myyntikuitissa. Vaihtoehtoisesti voit lisätä yrityksen nimen myyntikuitin asetteluun vapaamuotoisena tekstinä.
- Määritä yrityksen tunnusnumero **Verovelvollisen tunnistenumero** -kenttään. Muutoksen avulla voidaan varmistaa, että yrityksen tunnistenumero näkyy myyntikuitissa. Vaihtoehtoisesti voit lisätä yrityksen tunnistenumeron myyntikuitin asetteluun vapaamuotoisena tekstinä.

### <a name="set-up-functionality-profiles"></a>Määritä toimintoprofiilit

POS-toimintoprofiilien määritys. Määritä **Kuitin numeroinnit** -pikavälilehdessä kuitin numeroinnit luomalla tai päivittämällä **Myynti**-, **Myyntitilaus**- ja **Palautus** -kuittitapahtumatyyppien tietueita.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfiguroi mukautetut kentät siten, että niitä voidaan käyttää myyntikuittien kuittimuodoissa

Voit konfiguroida POS-kuittimuodoissa käytettävät kielitekstit ja mukautetut kentät. Kuittiasetukset luoneen käyttäjän oletusyrityksen tulee olla sama yritys, jossa kielitekstiasetukset luodaan. Vaihtoehtoisesti samat kielitekstit tulisi luoda sekä käyttäjän oletusyrityksessä että sen myymälän yrityksessä, jota varten asetukset luodaan.

Lisää **Kieliteksti**-sivulla seuraavat tietueet kuitin asettelun mukautettujen kenttien otsikoihin. Huomaa, että taulukossa näkyvät **kielitunnukset**, **tekstitunnukset** ja **tekstiarvot** ovat vain esimerkkejä. Voit muuttaa ne tarpeidesi mukaisiksi. Käyttämäsi **tekstin tunnuksen** arvon on kuitenkin oltava yksilöivä, ja niiden on oltava yhtä suuret tai suurempia kuin 900001.

Lisää seuraavat myyntipisteen otsikot **Kieliteksti**-sivun **POS**-osaan.

| Kielitunnus | Tekstitunnus | Teksti                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR-koodi                               |
| en-US       | 900002  | Tapahtumatunnus                        |
| en-US       | 900003  | Vähittäismyyntiveron tulostuskoodi                 |
| en-US       | 900004  | Verosumma (myynti)                    |
| en-US       | 900005  | Veron peruste (myynti)                     |
| en-US       | 900006  | Tapahtuman aloituspäivämäärä ja -aika           |
| en-US       | 900007  | Tapahtuman päättymispäivämäärä ja -aika             |
| en-US       | 900008  | Suojauselementin sarjanumero |
| en-US       | 900009  | Allekirjoituslaskuri                     |
| en-US       | 900010  | Tarkistusarvo                           |
| en-US       | 900011  | Tietosanoma                          |

Lisää **Mukautetut kentät** -sivulla seuraavat tietueet kuitin asettelun mukautettuihin kenttiin. Huomaa, että **otsikkotekstin tunnuksen** arvojen on vastattava **Kieliteksti**-sivulla määritettyjä **tekstitunnuksen** arvoja.

| Nimi                            | Tyyppi    | Otsikon tekstin tunnus |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Vastaanotto | 900001          |
| TRANSACTIONID\_DE               | Vastaanotto | 900002          |
| RETAILPRINTCODE\_DE             | Vastaanotto | 900003          |
| SALESTAXAMOUNT\_DE              | Vastaanotto | 900004          |
| SALESTAXBASIS\_DE               | Vastaanotto | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Vastaanotto | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Vastaanotto | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Vastaanotto | 900008          |
| SIGNCOUNTER\_DE                 | Vastaanotto | 900009          |
| SIGN\_DE                        | Vastaanotto | 900010          |
| INFOMESSAGE\_DE                 | Vastaanotto | 900011          |

> [!NOTE]
> On tärkeää määrittää oikeat mukautetut kenttien nimet edellisen taulukon mukaan. Virheellisen mukautetun kentän nimi aiheuttaa kuiteissa puuttuvia tietoja.

### <a name="configure-receipt-formats"></a>Kuittimuotojen määrittäminen

Muuta jokaisessa vaaditussa kuittimuodossa **Tulostustoiminta**-kentän arvoksi **Tulosta aina**.

Lisää kuittien muodon suunnittelussa seuraavat mukautetut kentät asianmukaisiin kuittien osiin. Huomaa, että kenttien nimet vastaavat edellisessä osassa määritettyjä kielitekstejä.

- **Otsikko:** Lisää seuraavat kentät:

    - **Myymälän nimi** ja **Verotunnus**: näiden kenttien avulla tulostetaan yrityksen nimi ja tunnistenumero kuitteihin. Vaihtoehtoisesti voit lisätä yrityksen nimen ja tunnistenumeron asetteluun vapaamuotoisena tekstinä.
    - **Myymälän osoite**-, **Päivämäärä**-, **Aika 24H**-, **Kuitin numero**- ja **Rekisterinumero**-kentät.

- **Rivit:** Lisää seuraavat kentät:

    - **Nimikkeen nimi** -kenttä
    - **Määrä**-kenttä
    - **Verollinen kokonaishinta** -kenttä
    - **Vähittäismyyntiveron tulostuskoodi** -kenttä, jonka avulla tulostetaan nimikkeeseen sovellettavaa arvonlisäverokoodia vastaava lyhennekoodi.

- **Alatunniste:** Lisää seuraavat kentät:

    - Maksukentät, jotta kunkin maksutavan maksusummat tulostetaan. Lisää esimerkiksi **maksuvälineen nimen** ja **maksuvälinesumman** kentät yhdelle asettelun riville.
    - **Veroerittely**-kenttäryhmän kentät. Kaikki tämän kenttäryhmän kentät on tulostettava yhdelle erilliselle riville.

        - **Verotunnus**-kenttä on vakiokenttä, jonka avulla jokaiselle arvonlisäverokoodille voidaan tulostaa arvonlisäveron yhteenveto. Kenttä on lisättävä uudelle riville.
        - **Veroprosentti**-kenttä, joka on vakiokenttä, jonka avulla arvonlisäverokoodin voimassa oleva veroprosentti tulostetaan.
        - **Veron peruste (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin kokonaismyyntisumma arvonlisäverokoodille. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
        - **Verosumma (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin verosumma arvonlisäverokoodille.
        - **Vähittäismyyntiveron tulostuskoodi** -kenttä, jonka avulla tulostetaan arvonlisäverokoodia vastaava lyhennekoodi.

    - Kentät, jotka sisältävät verorekisteröintipalvelun palauttamat suojatut tapahtumatiedot:

        - **Tapahtumatunnus**: tämä kenttä määrittää kassatapahtuman numeron kirjanpidon rekisteröintipalvelussa
        - **Tapahtuman aloituspäivämäärä ja -aika** -kenttä
        - **Tapahtuman lopetuspäivämäärä ja -aika** -kenttä
        - **Suojauselementin sarjanumero** -kenttä
        - **Allekirjoituslaskuri**-kenttä
        - **Tarkistusarvo**-kenttä
        - **QR-koodi**-kenttä, jota käytetään rekisteröityjen käteistapahtumien viitteen tulostamisen QR-koodin muodossa

        > [!NOTE]
        > **QR-koodi** -arvo haetaan verorekisterin vastauksesta. EFR palauttaa vastauksessaan QR-koodin vain, jos EFR-konfiguraation **Määritteet**-kentän arvo on kuvattu EFSTA-dokumentaatiossa. EFR-konfiguraation **Määritteet**-kentän QR-koodimuodoksi on määritettävä **BMP**.

    - **Tietosanoma**-kenttä, jotta kuiteissa voidaan näyttää ilmoitussanomat kirjanpidon rekisteröintipalvelusta. Jos esimerkiksi allekirjoituslaite hajoaa, kuittiin voidaan tulostaa erityisteksti.

Lisätietoja kuittimuotojen ja kuittien muotojen suunnittelusta on kohdassa [Kuittimuotojen määrittäminen ja suunnitteleminen](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Kirjanpidon integroinnin määrittäminen (Saksa)

Saksan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Efr** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on Commerce runtimen (CRT) ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa (VM) Microsoft Dynamics Lifecycle Servicesissä (LCS). Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Saksa) (vanha)](emea-deu-fi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

Suorita verointegraation määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla:

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ota myös huomioon verorekisteröintiprosessin asetukset, jotka [liittyvät tähän verorekisteröintipalvelun integraatioesimerkkiin](#set-up-the-registration-process).
1. [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Verointegraatiokehykseen liittyvät virheenkäsittelyominaisuudet eivät ehkä ole täysin yhdenmukaisia paikallisten verosäädösten kanssa.
    >
    > - Suosittelemme, että jätät **Jatka virheen ilmetessä** -vaihtoehdon pois käytöstä **Verorekisteröintiprosessi**-sivulla, koska kaikki tapahtumat on rekisteröitävä oikein, vaikka verorekisteröinnin ensimmäinen yritys ei onnistu.
    > - Ennen kuin siirryt **Verorekisteröintiprosessi**-sivun **Ohita**- tai **Merkitse rekisteröidyksi** -valintaan, sinun on hyvä keskustella näistä muutoksista verokonsultin tai paikallisen veroviraston kanssa.

1. [Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Rekisteröintiprosessin määrittäminen

Voit ottaa rekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita. Lisätietoja on kohdassa [Commerce-kanavan verointegroinnin määritys](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot.

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan (esim. **[julkaisu 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avaa **src \> FiscalIntegration \> Efr**.
    1. Lataa veroasiakirjan tarjoajan konfigurointitiedosto kohdasta **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (esim. [the file for release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Lataa veroyhdistimen konfigurointitiedosto kohdasta **Configurations \> Connectors \> ConnectorEFRSample.xml** (esim. [julkaisun 9.33 tiedosto](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Tämän verointegraatioesimerkin konfiguraatiotiedostot sijaitsevat seuraavissa Retail SDK -sovelluksen kansioissa kehittäjän virtuaalikoneessa LCS:ssä:
    >
    > - **Veroasiakirjan tarjoajan konfigurointitiedosto:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
    > - **Veroyhdistimen konfigurointitiedosto:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**. Määritä **Yleiset**-pikavälilehdessä **Ota kirjanpidon integrointi käyttöön**-asetukseksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**, ja lataa aiemmin lataamasi kirjanpitoasiakirjan toimittajan konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**, ja lataa aiemmin lataamasi kirjanpidon yhdistimen konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**. Luo uusi yhdistimen toimintoprofiili. Valitse tiedoston tarjoaja ja aiemmin ladattu liitin. Päivitä [tietojen määritysasetukset](#default-data-mapping) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**. Luo uusi liittimen tekninen profiili ja valitse aiemmin ladattu veroliitin. Päivitä [yhdistimen asetukset](#fiscal-connector-settings) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmät**. Luo uusi veroliitinryhmä aiemmin luomallesi liittimen toimintoprofiilille.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**. Luo uusi kirjanpidon rekisteröintiprosessi ja verorekisteröintiprosessi vaihe ja valitse aiemmin luomasi kirjanpidon yhdistinryhmä.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Valitse siihen myymälään linkitetty toimintoprofiili, jossa rekisteröintiprosessi tulee aktivoida. Valitse **Kirjanpidon rekisteröintiprosessi** -pikavälilehdessä aiemmin luomasi kirjanpidon rekisteröintiprosessi.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**. Valitse Hardware stationiin liitetty laiteprofiili, johon verotulostin liitetään. Valitse **Kirjanpidon oheislaitteet** -pikavälilehdessä aiemmin luomasi liittimen tekninen profiili.
1. Avaa jakeluaikataulu (**Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**) ja valitse työt **1070** ja **1090** siirtääksesi tiedot kanavatietokantaan.

#### <a name="default-data-mapping"></a>Tietojen oletusmääritys

Seuraavat tietojen oletusmääritykset sisältyvät veroasiakirjan tarjoajan konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Maksuvälinetyypin määritys** – Maksutapojen määritys **PayG** (maksuryhmä) -määritteen arvoihin pyynnöissä, jotka lähetetään kirjanpitopalveluun. Tässä on oletusmääritys:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Kunkin parin ensimmäinen komponentti edustaa myymälälle määritettyä maksutapaa. Toinen komponentti edustaa vastaavaa maksuryhmää, jota EFR-verorekisteröintipalvelu tukee. Lisätietoja EFR:n tukemista maksuryhmistä Saksassa on [EFR:n viitteessä](https://public.efsta.net/efr/).

    Maksutapojen esimerkkiyhdistämismääritys vastaa vakio-esittelytiedoissa konfiguroidun myymälän maksutapoja.

    | Maksutapa | Maksutavan nimi |
    |----------------|---------------------|
    | 1              | Maksu                |
    | 2              | Sekki               |
    | 3              | Kortti                |
    | 4              | Asiakastili    |
    | 5              | Muu               |
    | 6              | Valuutta            |
    | 7              | Tosite             |
    | 8              | Lahjakortti           |
    | 9              | Maksuvälineen poisto tai vaihtokassa |
    | 10             | Kanta-asiakaskortit       |
    | 11             | Muut kuin paikalliset sekit    |

    Siksi esimerkkiyhdistämismääritystä on muokattava sovelluksessa konfiguroitujen maksutapojen mukaan.

- **Sisällytä asiakastiedot** – Jos tämä parametri on käytössä, veropalvelupyynnöt sisältävät asiakastietoja, kuten nimiä ja osoitteita, jos asiakas lisätään tapahtumaan.
- **ALV-prosenttimääritys** – Arvonlisäverokoodeille määritettyjen veroprosenttiarvojen yhdistäminen **TaxG** (veroryhmä) -määritteeseen pyynnöissä, jotka lähetetään veropalveluun. Tässä on oletusmääritys:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Kunkin parin 1. komponentti edustaa ALV-ryhmää, jota EFR-verorekisteröintipalvelu tukee. Toinen komponentti edustaa vastaavaa arvonlisäveroprosenttia. Lisätietoja EFR:n tukemista ALV-veroryhmistä Saksassa on [EFR:n viitteessä](https://public.efsta.net/efr/).

- **Lahjakorttien ja talletusten veroryhmä** – **TaxG**-määritteen arvo veropalvelulle lähetetyissä pyynnöissä. Arvo perustuu toimintoihin, joihin liittyy lahjakortteja tai talletuksia. Tässä on oletusmääritys:

    ```
    G
    ```

- **ALV-vapautuksen veroryhmä** – Veropalveluun lähetettyjen pyyntöjen **TaxG**-määritteen arvo. Arvo perustuu toimintoihin, jotka eivät ole verovelvollisia. Tässä on oletusmääritys:

    ```
    F
    ```

> [!NOTE]
> Tietojen oletusmäärityksen veroasetukset vastaavat siitä, että järjestelmän veroasetukset ja EFR-palvelun veroryhmät täsmäytetään. Veroryhmät voidaan tulostaa kuitteihin vain, jos **Tulostuskoodi**-kenttä on määritetty **Arvonlisäverokoodit**-sivulla.

#### <a name="fiscal-connector-settings"></a>Veroliittimen asetukset

Seuraavat asetukset sisältyvät veroyhdistimen konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Aikakatkaisu** – Aika millisekunteina, jonka veroyhdistin odottaa verorekisteröintipalvelun vastausta.
- **Näytä kirjanpidon rekisteröinnin ilmoitukset** – Tämä merkki määrittää, näytetäänkö operaattorille ilmoitukset, jotka kirjanpidon rekisteröintipalvelu palauttaa.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Saksa) (vanha)](emea-deu-fi-sample-sdk.md).
>
> Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

#### <a name="set-up-the-development-environment"></a>Kehitysympäristön määrittäminen

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa esimerkkiä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Retail SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
1. Avaa EFR-ratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** ja muodosta se.
1. Commerce Runtime -laajennusten asennus:

    1. Etsi CRT-laajennuksen asennusohjelma:

        - **Commerce Scale Unit:** Etsi **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** -kansiosta **ScaleUnit.EFR.Installer**-asennusohjelma.
        - **Paikallinen CRT Modern POS -sovelluksessa:** Etsi **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** -kansiosta **ModernPOS.EFR.Installer**-asennusohjelma.

    1. Käynnistä CRT-laajennusten asennusohjelma komentoriviltä:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Paikallinen CRT Modern POS -sovelluksessa:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Asenna veroliittimen laajennukset:

    Voit asentaa veroliittimen laajennukset [Hardware stationissa](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) tai [POS-kassapäätteessä](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Asenna Hardware station -laajennukset:

        1. Etsi **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** -kansiosta **HardwareStation.EFR.Installer**-asennusohjelma.
        1. Käynnistä laajennuksen asennusohjelma komentoriviltä suorittamalla seuraava komento.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Asenna myyntipisteen laajennukset:

        1. Avaa myyntipisteen veroliittimien esimerkkiratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** ja muodosta se.
        1. Etsi **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** -kansiosta **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer**-asennusohjelma..
        1. Käynnistä laajennuksen asennusohjelma komentoriviltä suorittamalla seuraava komento.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Tuotantoympäristö

Luo ja julkaise verointegraatioesimerkin Cloud Scale Unit ja itsepalveluna käyttöönotettavat paketit noudattamalla [Määritä koontijakso verointegraatioesimerkille](fiscal-integration-sample-build-pipeline.md) -ohjeen vaiheita. **EFR build-pipeline.yml**-niminen YAML-mallitiedosto löytyy **Pipeline\\YAML_Files** -kansiosta[Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilöstä.

## <a name="design-of-extensions"></a>Laajennusten rakenne

Saksan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Retail SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Efr** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä (esim. [julkaisun 9.33 esimerkki](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on CRT:n ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Retail SDK:n käytöstä on kohdissa [Retail SDK -arkkitehtuuri](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Määritä itsenäisen pakkaus-SDK:n koontiversioputki](../dev-itpro/build-pipeline.md).

> [!WARNING]
> [Uuden itsenäisen pakkaus- ja laajennusmallin](../dev-itpro/build-pipeline.md) rajoitusten vuoksi sitä ei voi tällä hetkellä käyttää tässä verointegraatioesimerkissä. Retail SDK:n edellistä versiota on käytettävä kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Saksa) (vanha)](emea-deu-fi-sample-sdk.md). Verointegrointiesimerkkien uuden itsenäisen pakkaus- ja laajennusmallin tukea suunnitellaan myöhempiä versioita varten.

### <a name="crt-extension-design"></a>CRT-laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä verorekisteröintipalvelun vastauksia.

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjapalvelua varten on yksi pyynnön käsittelijä, **DocumentProviderEFRFiscalDEU**. Tämän käsittelijän avulla luodaan veroasiakirjoja verorekisteröintipalvelua varten. Se on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Tämä pyyntö palauttaa vastauksen yhdessä laajennettujen tietojen kanssa.

#### <a name="configuration"></a>Konfigurointi

Veroasiakirjan tarjoajan konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** [Dynamics 365 Commerce -ratkaisujen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) säilössä. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla verotiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa.

Hardware station -laajennus on **HardwareStation.Extension.EFRSample**. Se käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo kirjanpidon rekisteröintipalveluun. Se käsittelee myös verorekisteröintipalvelusta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EFRHandler**-pyyntökäsittelijä on kirjanpidon rekisteröintipalvelun pyyntöjen käsittelyn aloituspiste. Tämä käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä:

- **SubmitDocumentFiscalDeviceRequest** – Tämä pyyntö lähettää asiakirjoja kirjanpidon rekisteröintipalveluun ja palauttaa vastauksen pyyntöön.
- **IsReadyFiscalDeviceRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun kunnon tarkastusta varten.
- **InitializeFiscalDeviceRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun alustamiseen.

#### <a name="configuration"></a>Konfigurointi

Veroliittimen konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="pos-fiscal-connector-extension-design"></a>Myyntipisteen veroyhdistimen laajennuksen rakenne

Myyntipisteen veroyhdistimen laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa myyntipisteestä. Se käyttää tietoliikenteeseen HTTPS-protokollaa.

#### <a name="fiscal-connector-factory"></a>Veroliittimen luontitoiminto

Veroliittimen luontitoiminto yhdistää liittimien nimen veroliittimien toteutukseen ja se sijaitsee **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**-tiedostossa. Yhdistimen nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

#### <a name="efr-fiscal-connector"></a>EFR-veroliitin

EFR-veroliitin sijaitsee **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**-tiedostossa. Se toteuttaa **IFiscalConnector**-rajapinnan, joka tukee seuraavia pyyntöjä:

- **FiscalRegisterSubmitDocumentClientRequest** – Tämä pyyntö lähettää asiakirjoja kirjanpidon rekisteröintipalveluun ja palauttaa vastauksen pyyntöön.
- **FiscalRegisterIsReadyClientRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun kunnon tarkastusta varten.
- **FiscalRegisterInitializeClientRequest** – Tätä pyyntöä käytetään kirjanpidon rekisteröintipalvelun alustamiseen.

#### <a name="configuration"></a>Konfiguraatio

Määritystiedosto sijaitsee **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla veroyhdistin voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen. Seuraavat asetukset lisätään:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Aikakatkaisu** – Aika millisekunteina, jonka liitin odottaa verorekisteröintipalvelun vastausta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
