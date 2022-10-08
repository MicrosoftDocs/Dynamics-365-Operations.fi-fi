---
title: Itävallan tilikausirekisteröintipalvelun integroinnin malli
description: Tämä artikkeli on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Itävalta).
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 603316ea07e5951b3bc5f96af28f549bdafd3b0e
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631339"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Itävallan tilikausirekisteröintipalvelun integroinnin malli

[!include [banner](../includes/banner.md)]

Tämä artikkeli on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Itävalta).

Vaatimuksille, jotka liittyvät kassojen paikallisiin verotusvaatimuksiin Itävallassa, Dynamics 365 Retail -toiminnallisuus Itävallalle sisältää esimerkki-integraation myyntipisteestä ulkoiseen verorekisteröintipalveluun. Esimerkki laajentaa [kirjanpidon integrointitoimintoja](fiscal-integration-for-retail-channel.md). Se perustuu [EFSTA](https://www.efsta.eu/at/)-järjestelmän [EFR (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) -ratkaisuun, ja se ottaa yhteyden EFR-palveluun HTTPS-protokollan kautta. EFR-palvelun tulee olla isännöity joko Retail Hardware Stationissa tai erillisellä koneella, johon voidaan yhdistää Hardware Stationilta. Näyte toimitetaan lähdekoodin muodossa, ja se on osa Commerce-ohjelmiston kehityssarjaa (SDK).

Microsoft ei julkaise EFSTA:n laitteistoja, ohjelmistoja tai dokumentaatioita. Jos haluat lisätietoja EFR-ratkaisun saamiseksi ja sen toiminnan ylläpitämiseksi, ota yhteyttä [EFSTA:han](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Skenaariot

Seuraavat skenaariot ovat Itävallan verorekisteröintipalvelun integrointiesimerkistä:

- Käteistapahtumien rekisteröiminen verorekisteröintipalveluun:

    - Lähetä yksityiskohtaiset tapahtumatiedot kirjanpidon rekisteröintipalveluun. Näitä tietoja ovat myyntirivin tiedot sekä alennuksia, maksuja ja veroja koskevat tiedot.
    - Tallentaa vastauksen verorekisteröintipalvelusta. Tämä vastaus sisältää digitaalisen allekirjoituksen ja linkin rekisteröityyn tapahtumaan.
    - Rekisteröi verot ja liitä ne verorekisteröintipalvelun verokoodeihin.
    - Tulosta rekisteröidyn tapahtuman QR-koodi kuitille.

- Lahjakorttitoimintojen ja asiakkaan talletusten rekisteröinti ei-käteistapahtumina verorekisteröintipalveluun:

    - Myönnä tai lisää rahaa lahjakorttiin.
    - Rekisteröin asiakastilin talletus.
    - Rekisteröi asiakastilauksen talletus.

- Ei-myyntitapahtumien rekisteröinti ei-käteistapahtumina verorekisteröintipalveluun:

    - Avaa vuoro ja sulje vuoro
    - Aloitussumma, liukuva merkintä ja maksuvälineen poisto
    - Hinnan ohitus
    - Veron ohitus
    - Tulosta kuitin kopio
    - Kassan avaus
    - Tulosta X-raportti
    - Tulosta Z-raportti

- Päivän lopun raporttien (X/Z-raporttien) tulostaminen, kun kenttiä on Itävaltaa varten:

    - Asiakkaille toimitettujen tuotteiden tai palvelujen kokonaismäärä
    - Myynnin erittely veroprosenttien mukaan
    - Maksujen erittely kassanhoitajan/kassaoperaattorin mukaan
    - Päivittäistä myyntiä vähentävät hinta-alennukset ja palautukset
    - Nollamyynti (antamiset)

- Virheiden käsittely, esimerkiksi seuraavat vaihtoehdot:

    - Yritä verorekisteröintiä uudelleen esimerkiksi silloin, kun kirjanpidon rekisteröintipalvelu ei ole käytettävissä, se ei ole valmis tai se ei vastaa.
    - Lykkää kirjanpidon rekisteröintiä.
    - Ohita verorekisteröinti tai merkitse tapahtuma rekisteröidyksi ja sisällytä tietokoodit, jotka poimivat virheen syyn ja lisätiedot.
    - Tarkista kirjanpidon rekisteröintipalvelun käytettävyys ennen uuden myyntitapahtuman avaamista tai myyntitapahtuman viimeistelyä.

### <a name="gift-cards"></a>Lahjakortit

Verorekisteröintipalvelun integrointiesimerkki toteuttaa seuraavia lahjakortteihin liittyviä sääntöjä:

- Sulje käteistapahtumasta pois myyntirivit, jotka liittyvät *Myönnä lahjakortti*- ja *Lisää lahjakorttiin* -toimintoihin. Sen sijaan, että rekisteröit nämä rivit osana käteistapahtumaa, kirjaa ne erillisiksi ei-kassatapahtumiksi verorekisteröintipalveluun.
- Älä tulosta veroryhmän erittelyä ja QR-koodia kuittiin, jos kuitti koostuu vain lahjakorttiriveistä.
- Tulosta tapahtumassa myönnettyjen tai uudelleen veloitettavan lahjakorttien kokonaissumma erillisenä kuitin käteistapahtuman summasta.
- Tallenna maksurivien lasketut oikaisut kanavatietokantaan ja viittaus vastaavaan kirjanpitotapahtumaan.
- Lahjakortilla maksamista pidetään tavallisena maksuna.

### <a name="customer-deposits-and-customer-order-deposits"></a>Asiakastalletukset ja asiakastilausten talletukset

Verorekisteröintipalvelun integrointiesimerkissä otetaan käyttöön seuraavat säännöt, jotka liittyvät asiakastalletukseen ja asiakastilaustalletuksiin:

- Rekisteröi muu kuin käteistapahtuma, jos tapahtuma on asiakastalletus.
- Rekisteröi muu kuin käteistapahtuma, jos tapahtuma sisältää vain asiakastilaustalletuksen tai asiakastilauksen talletushyvityksen.
- Vähennä asiakkaan tilauksen talletussumma maksuriveiltä, kun hybridiasiakastilaus luodaan.
- Tallenna maksurivien lasketut oikaisut kanavatietokantaan ja viittaus vastaavaan hybridiasiakastilauksen kirjanpitotapahtumaan.

### <a name="limitations-of-the-sample"></a>Esimerkin rajoitukset

Verorekisteröintipalvelu tukee vain skenaarioita, joissa arvonlisävero sisältyy hintaan. Siksi **Hinta sisältää arvonlisäveron** -asetuksen on oltava **Kyllä** sekä myymälöille että asiakkaille.

## <a name="set-up-commerce-for-austria"></a>Commercen määrittäminen (Itävalta)

Tässä osassa kuvaillaan Commerce-asetukset, jotka ovat erityisiä ja suositeltuja Itävallassa. Lisätietoja määrityksestä on kohdassa [Commerce-aloitussivu](../index.md).

Ennen kuin voit käyttää Itävallan maa-/aluekohtaista toimintoa, sinun on määritettävä seuraavat asetukset:

- Määritä yrityksen ensisijaisessa osoitteessa **Maa/alue**-kentän arvoksi **AUT** (Itävalta).
- Jos myymälä sijaitsee Itävallassa, määritä sen POS-toimintoprofiilissa **ISO-koodi**-kentän arvoksi **AT** (Itävalta).

Sinun on määritettävä myös seuraavat asetukset Itävallassa. Huomaa, että asianmukaiset jakelutyöt on suoritettava asetusten määrityksen jälkeen.

### <a name="enable-features-for-austria"></a>Toimintojen käyttöönotto Itävaltaa varten

Ota käyttöön seuraavat toiminnot **Toimintojen hallinta** -työtilassa:

- (Itävalta) Ota lisätarkistustapahtumat käyttöön myyntipisteessä
- (Itävalta) Ota lisätiedot käyttöön myyntipisteen päivän lopun laskelmissa

### <a name="set-up-vat-per-austrian-requirements"></a>Arvonlisäveron määrittäminen Itävallan vaatimusten mukaan

Sinun on luotava arvonlisäverokoodit, arvonlisäveroryhmät ja nimikkeen arvonlisäveroryhmät. Määritä myös tuotteiden ja palveluiden arvonlisäverotiedot. Lisätietoja arvonlisävero-ominaisuuksien määrittämisestä ja käyttämisestä on ohjeaiheessa [Arvonlisäveron yleiskatsaus](../../finance/general-ledger/indirect-taxes-overview.md).

Myyntikuitteihin voidaan tulostaa arvonlisäverokoodin lyhenne (esimerkiksi "A" tai "B"). Voit ottaa tämän toiminnon käyttöön asettamalla **Arvonlisäverokoodit**-sivun **Tulosta koodi** -kentän.

### <a name="set-up-stores"></a>Määritä myymälät

Päivitä myymälän tiedot **Kaikki myymälät** -sivulla. Määritä erityisesti seuraavat parametrit:

- Määritä **Arvonlisäveroryhmä**-kentässä arvonlisäveroryhmä, jota pitäisi käyttää myynnissä oletusasiakkaalle.
- Määritä **Hinnat sisältävät arvonlisäveron** -vaihtoehdon arvoksi **Kyllä**.
- Määritä **Nimi**-kenttään yrityksen nimi. Muutoksen avulla voidaan varmistaa, että yrityksen nimi näkyy myyntikuitissa. Vaihtoehtoisesti voit lisätä yrityksen nimen myyntikuitin asetteluun vapaamuotoisena tekstinä.
- Määritä yrityksen tunnusnumero **Verovelvollisen tunnistenumero** -kenttään. Muutoksen avulla voidaan varmistaa, että yrityksen tunnistenumero näkyy myyntikuitissa. Vaihtoehtoisesti voit lisätä yrityksen tunnistenumeron myyntikuitin asetteluun vapaamuotoisena tekstinä.

### <a name="set-up-functionality-profiles"></a>Määritä toimintoprofiilit

POS-toimintoprofiilien määritys:

- Määritä **Kuitin numeroinnit** -pikavälilehdessä kuitin numeroinnit luomalla tai päivittämällä **Myynti**-, **Myyntitilaus**- ja **Palautus** -kuittitapahtumatyyppien tietueita.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfiguroi mukautetut kentät siten, että niitä voidaan käyttää myyntikuittien kuittimuodoissa

Voit konfiguroida POS-kuittimuodoissa käytettävät kielitekstit ja mukautetut kentät. Kuittiasetukset luoneen käyttäjän oletusyrityksen tulee olla sama yritys, jossa kielitekstiasetukset luodaan. Vaihtoehtoisesti samat kielitekstit tulisi luoda sekä käyttäjän oletusyrityksessä että sen myymälän yrityksessä, jota varten asetukset luodaan.

Lisää **Kieliteksti**-sivulla seuraavat tietueet kuitin asettelun mukautettujen kenttien otsikoihin. Huomaa, että taulukossa näkyvät **kielitunnukset**, **tekstitunnukset** ja **tekstiarvot** ovat vain esimerkkejä. Voit muuttaa ne tarpeidesi mukaisiksi. Käyttämäsi **tekstin tunnuksen** arvon on kuitenkin oltava yksilöivä, ja niiden on oltava yhtä suuret tai suurempia kuin 900001.

Lisää taulusta seuraavat myyntipisteen otsikot **kielitekstin** **POS**-osaan:

| Kielitunnus | Tekstitunnus | Teksti                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR-koodi                   |
| en-US       | 900002  | Jatkuva numero         |
| en-US       | 900003  | Vähittäismyyntiveron tulostuskoodi     |
| en-US       | 900004  | Yhteensä (myynti)             |
| en-US       | 900005  | Verot yhteensä (myynti)         |
| en-US       | 900006  | Loppusumma sis.veron (myynti) |
| en-US       | 900007  | Verosumma (myynti)        |
| en-US       | 900008  | Veron peruste (myynti)         |

Lisää **Mukautetut kentät** -sivulla seuraavat tietueet kuitin asettelun mukautettuihin kenttiin. Huomaa, että **otsikkotekstin tunnuksen** arvojen on vastattava **Kieliteksti**-sivulla määritettyjä **tekstitunnuksen** arvoja:

| Nimi                 | Tyyppi    | Otsikon tekstin tunnus |
|----------------------|---------|-----------------|
| QRCODE               | Vastaanotto | 900001          |
| CONTINUOUSNUMBER     | Vastaanotto | 900002          |
| RETAILPRINTCODE      | Vastaanotto | 900003          |
| SALESTOTAL           | Vastaanotto | 900004          |
| SALESTOTALTAX        | Vastaanotto | 900005          |
| SALESTOTALINCLUDETAX | Vastaanotto | 900006          |
| SALESTAXAMOUNT       | Vastaanotto | 900007          |
| SALESTAXBASIS        | Vastaanotto | 900008          |

> [!NOTE]
> On tärkeää määrittää oikeat mukautetut kenttien nimet edellisen taulukon mukaan. Virheellisen mukautetun kentän nimi aiheuttaa kuiteissa puuttuvia tietoja.

### <a name="configure-receipt-formats"></a>Kuittimuotojen määrittäminen

Muuta jokaisessa vaaditussa kuittimuodossa **Tulostustoiminta**-kentän arvoksi **Tulosta aina**.

Lisää kuittien muodon suunnittelussa seuraavat mukautetut kentät asianmukaisiin kuittien osiin. Huomaa, että kenttien nimet vastaavat edellisessä osassa määritettyjä kielitekstejä.

- **Otsikko:** Lisää seuraavat kentät:

    - **Myymälän nimi** ja **Verotunnus**: näiden kenttien avulla tulostetaan yrityksen nimi ja tunnusnumero kuitteihin. Vaihtoehtoisesti voit lisätä yrityksen nimen ja tunnistenumeron asetteluun vapaamuotoisena tekstinä.
    - **Myymälän osoite**-, **Päivämäärä**-, **Aika 24H**-, **Kuitin numero**- ja **Rekisterinumero**-kentät.
    - **Jatkuva numero** -kentät määrittävät kassatapahtuman numeron kirjanpidon rekisteröintipalvelussa.

- **Rivit:** Lisää seuraavat kentät:

    - **Nimikkeen nimi**.
    - **Määrä**.
    - **Verollinen kokonaishinta**.
    - **Vähittäismyyntiveron tulostuskoodi**, jonka avulla tulostetaan nimikkeeseen sovellettavaa arvonlisäverokoodia vastaava lyhennekoodi.

- **Alatunniste:** Lisää seuraavat kentät:

    - Maksukentät, jotta kunkin maksutavan maksusummat tulostetaan. Lisää esimerkiksi **maksuvälineen nimen** ja **maksuvälinesumman** kentät yhdelle asettelun riville.
    - **Myynti yhteensä** -kenttäryhmä:

        - **Kokonaissumma (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin kokonaissumma. Summa ei sisällä veroa. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
        - **Loppusumma sis.veron (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin kokonaissumma. Summa sisältää veron. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
        - **Verot yhteensä (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin veron kokonaissumma. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.

    - **Veroerittely**-kenttäryhmä. Kaikki tämän kenttäryhmän kentät on tulostettava yhdelle erilliselle riville.

        - **Verotunnus**-kenttä on vakiokenttä, jonka avulla jokaiselle arvonlisäverokoodille voidaan tulostaa arvonlisäveron yhteenveto. Kenttä on lisättävä uudelle riville.
        - **Veroprosentti**-kenttä, joka on vakiokenttä, jonka avulla arvonlisäverokoodin voimassa oleva veroprosentti tulostetaan.
        - **Veron peruste (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin kokonaismyyntisumma arvonlisäverokoodille. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
        - **Verosumma (myynti)** -kentän avulla tulostetaan kuitin käteismyynnin verosumma arvonlisäverokoodille.
        - **Vähittäismyyntiveron tulostuskoodi** -kenttä, jonka avulla tulostetaan arvonlisäverokoodia vastaava lyhennekoodi.

    - **QR-koodi**-kenttä, jota käytetään rekisteröityjen käteistapahtumien viitteen tulostamisen QR-koodin muodossa.

        > [!NOTE]
        > **QR-koodi** -arvo haetaan verorekisterin vastauksesta. EFR palauttaa vastauksessaan QR-koodin vain, jos EFR-konfiguraation **Määritteet**-kentän arvo on kuvattu EFSTA-dokumentaatiossa. EFR-konfiguraation **Määritteet**-kentän QR-koodimuodoksi on määritettävä **BMP**.

Lisätietoja kuittimuotojen ja kuittien muotojen suunnittelusta on kohdassa [Kuittimuotojen määrittäminen ja suunnitteleminen](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Kirjanpidon integroinnin määrittäminen (Itävalta)

Itävallan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Commerce SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Efr** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. [Esimerkki](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) koostuu veroasiakirjan tarjoajasta, joka on Commerce runtimen (CRT) laajennus, ja veroliitin, joka on Commerce Hardware Stationin laajennus. Lisätietoja Commerce SDK:n käyttämisestä on kohdissa [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja  NuGetista](../dev-itpro/retail-sdk/sdk-github.md) ja [Koontijakson asetusten määrittäminen riippumattoman pakkauksen SDK:ta varten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Itävallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commerce SDK:ssa Commercen versiosta 10.0.29 alkaen. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa Microsoft Dynamics Lifecycle Servicesissa (LCS). Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Itävalta) (vanha)](emea-aut-fi-sample-sdk.md).

Suorita verointegraation määritysvaiheet [Commerce-kanavien kirjanpidon integroinnin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md) -kohdassa kuvatulla tavalla:

1. [Kirjanpidon rekisteröintiprosessin määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ota myös huomioon verorekisteröintiprosessin asetukset, jotka [liittyvät tähän verorekisteröintipalvelun integraatioesimerkkiin](#set-up-the-registration-process).
1. [Virheen käsittelyasetusten määrittäminen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Lykätyn kirjanpidon rekisteröinnin manuaalisen suorituksen käyttöönotto](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Määritä kanavakomponentit](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Rekisteröintiprosessin määrittäminen

Voit ottaa rekisteröintiprosessin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita. Lisätietoja on kohdassa [Commerce-kanavan verointegroinnin määritys](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritystiedostot.

    1. Avaa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilö.
    1. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan.
    1. Avaa **src \> FiscalIntegration \> Efr**.
    1. Avaa kohta **Määritykset \> DocumentProviders** ja lataa seuraavat veroasiakirjan tarjoajan määritystiedostot: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Lataa veroliittimen määritystiedosto kohdassa **Määritykset \> Liittimet \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa LCS:ssä. Tämän verointegraatioesimerkin konfiguraatiotiedostot sijaitsevat seuraavissa Retail SDK -sovelluksen kansioissa kehittäjän virtuaalikoneessa LCS:ssä:
    >
    > - **Veroasiakirjan tarjoajan konfigurointitiedostot:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Veroyhdistimen konfigurointitiedosto:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**. Määritä **Yleiset**-pikavälilehdessä **Ota kirjanpidon integrointi käyttöön**-asetukseksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**, ja lataa aiemmin lataamasi kirjanpitoasiakirjan toimittajan konfigurointitiedostot.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**, ja lataa aiemmin lataamasi kirjanpidon yhdistimen konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**. Luo kaksi uutta liittimen toimintoprofiilia, yksi kullekin aiemmin ladatulle veroasiakirjan tarjoajalle ja valitse aiemmin ladattu veroliitin. Päivitä [tietojen määritysasetukset](#default-data-mapping) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**. Luo uusi liittimen tekninen profiili ja valitse aiemmin ladattu veroliitin. Päivitä [yhdistimen asetukset](#fiscal-connector-settings) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmät**. Luo kaksi uutta veroliitinryhmää, yksi kullekin aiemmin luomallesi liittimen toimintoprofiilille.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**. Luo uusi kirjanpidon rekisteröintiprosessi ja kaksi verorekisteröintiprosessin vaihetta ja valitse aiemmin luomasi kirjanpidon yhdistinryhmät.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Valitse siihen myymälään linkitetty toimintoprofiili, jossa rekisteröintiprosessi tulee aktivoida. Valitse **Kirjanpidon rekisteröintiprosessi** -pikavälilehdessä aiemmin luomasi kirjanpidon rekisteröintiprosessi. Voit ottaa muiden kuin verotapahtumien rekisteröinnin käyttöön myyntipisteessä valitsemalla **Toiminnot**-pikavälilehden **POS**-kohdasta **Kirjaus**-asetuksen arvoksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**. Valitse Hardware Stationiin liitetty laiteprofiili, johon verorekisteröintipalvelu liitetään. Valitse **Kirjanpidon oheislaitteet** -pikavälilehdessä aiemmin luomasi liittimen tekninen profiili.
1. Avaa jakeluaikataulu (**Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**) ja valitse työt **1070** ja **1090** siirtääksesi tiedot kanavatietokantaan.

#### <a name="default-data-mapping"></a>Tietojen oletusmääritys

Seuraavat tietojen oletusmääritykset sisältyvät veroasiakirjan tarjoajan konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **ALV-prosenttimääritys** – Arvonlisäverokoodeille määritettyjen veroprosenttiarvojen yhdistäminen **TaxG** (veroryhmä) -määritteeseen pyynnöissä, jotka lähetetään veropalveluun. Tässä on oletusmääritys:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Kunkin parin 1. komponentti edustaa ALV-ryhmää, jota EFR-verorekisteröintipalvelu tukee. Toinen komponentti edustaa vastaavaa arvonlisäveroprosenttia. Lisätietoja EFR:n tukemista ALV-veroryhmistä Itävallassa on [EFR:n viitteessä](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Veroliittimen asetukset

Seuraavat asetukset sisältyvät veroyhdistimen konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Laitteen aikakatkaisu** – Aika millisekunteina, jonka veroyhdistin odottaa verorekisteröintipalvelun vastausta.
- **Näytä kirjanpidon rekisteröinnin ilmoitukset** – Tämä merkki määrittää, näytetäänkö operaattorille ilmoitukset, jotka kirjanpidon rekisteröintipalvelu palauttaa.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

> [!NOTE]
> - Itävallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commerce SDK:ssa Commercen versiosta 10.0.29 alkaen. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Itävalta) (vanha)](emea-aut-fi-sample-sdk.md).
> - Ympäristössä käyttöönotettuja Commerce-esimerkkejä ei päivitetä automaattisesti, kun Commerce-osien palvelu- tai laatupäivitykset otetaan käyttöön. Vaaditut esimerkit on päivitettävä manuaalisesti.

#### <a name="set-up-the-development-environment"></a>Kehitysympäristön määrittäminen

Suorita nämä vaiheet, kun haluat määrittää kehitysympäristön, jonka avulla voit testata ja laajentaa esimerkkiä.

1. Kloonaa tai lataa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) -säilö. Valitse oikea julkaisuhaaran versio SDK-/sovellusversion mukaan. Lisätietoja: [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja NuGetista](../dev-itpro/retail-sdk/sdk-github.md).
1. Avaa EFR-ratkaisu kohdassa **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** ja muodosta se.
1. Asenna CRT-laajennukset:

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

Itävallan verorekisteröintipalvelun integraatioesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Commerce SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Efr** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Esimerkki [koostuu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) veroasiakirjan tarjoajasta, joka on CRT:n ja veroliittimen laajennus, joka on Commerce Hardware Stationin laajennus. Lisätietoja Commerce SDK:n käyttämisestä on kohdissa [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja  NuGetista](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Koontijakson asetusten määrittäminen riippumattoman pakkauksen SDK:ta varten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Itävallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commerce SDK:ssa Commercen versiosta 10.0.29 alkaen. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Itävalta) (vanha)](emea-aut-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne 

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä verorekisteröintipalvelun vastauksia.

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjatarjoajia varten on kaksi pyynnön käsittelijää:

- **DocumentProviderEFRFiscalAUT** – Tämän käsittelijän avulla luodaan veroasiakirjoja verorekisteröintipalvelua varten.
- **DocumentProviderEFRNonFiscalAUT** – Tämän käsittelijän avulla luodaan muita kuin veroasiakirjoja verorekisteröintipalvelua varten.

Nämä käsittelijät on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä:

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetNonFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä muu kuin veroasiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavat tapahtumat ovat tuettuja: myynti, X-raportin tulostaminen, Z-raportin tulostaminen, asiakastilitalletus, asiakastilausten talletukset, kirjaustapahtumat sekä muut kuin myyntitapahtumat.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Tämä pyyntö palauttaa vastauksen verorekisteröintipalvelusta. Tämä vastaus sarjoitettu muodostamaan merkkijonon, joten se on valmis tallennettavaksi.

#### <a name="configuration"></a>Konfigurointi

Veroasiakirjan tarjoajan konfiguraatiotiedostot sijaitsevat **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä:

- **DocumentProviderFiscalEFRSampleAustria** – veroasiakirjojen tarjoajan konfiguraatiotiedosto.
- **DocumentProviderNonFiscalEFRSampleAustria** – muiden kuin veroasiakirjojen tarjoajan konfiguraatiotiedosto.

Näiden tiedostojen tarkoitus on ottaa käyttöön asetukset, joiden avulla verotiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa. Hardware station -laajennus käyttää HTTP-ja HTTPS-protokollia asiakirjojen lähettämiseen, jotka CRT-laajennus luo kirjanpidon rekisteröintipalveluun. Se käsittelee myös verorekisteröintipalvelusta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EFRHandler**-pyyntökäsittelijä on kirjanpidon rekisteröintipalvelun pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Veroliitin tukee seuraavia pyyntöjä:

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
