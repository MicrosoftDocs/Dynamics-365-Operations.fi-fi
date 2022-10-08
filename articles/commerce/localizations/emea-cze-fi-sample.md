---
title: Tšekin tasavallan verorekisteröintipalvelun integroinnin malli
description: Tämä artikkeli on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Tšekin tasavalta).
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-01
ms.openlocfilehash: de26b038009d8bf3518c67389c96aade19a0b65b
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631282"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Tšekin tasavallan verorekisteröintipalvelun integroinnin malli

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tämä artikkeli on yleiskatsaus Microsoft Dynamics 365 Commercen kirjanpidon integrointiesimerkistä (Tšekin tasavalta).

Vaatimuksille, jotka liittyvät kassojen paikallisiin verotusvaatimuksiin Tšekin tasavallassa, Dynamics 365 Commerce -toiminnallisuus Tšekin tasavallalle sisältää esimerkki-integraation myyntipisteestä ulkoiseen verorekisteröintipalveluun. Esimerkki laajentaa [kirjanpidon integrointitoimintoja](fiscal-integration-for-retail-channel.md). Se perustuu [EFSTA](https://efsta.org/)-järjestelmän [EFR (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) -ratkaisuun, ja se ottaa yhteyden EFR-palveluun HTTPS-protokollan kautta. EFR-palvelu varmistaa myynnin sähköisen rekisteröinnin (Elektronická evidence tržeb \[EET\]). Se siis varmistaa myyntitietojen online-siirron veroviranomaisten verkkopalveluun. EFR-palvelun tulee olla isännöity joko Commerce Hardware Stationissa tai erillisellä koneella, johon voidaan yhdistää Hardware Stationilta. Näyte toimitetaan lähdekoodin muodossa, ja se on osa Commerce-ohjelmiston kehityssarjaa (SDK).

Microsoft ei julkaise EFSTA:n laitteistoja, ohjelmistoja tai dokumentaatioita. Jos haluat lisätietoja EFR-ratkaisun saamiseksi ja sen toiminnan ylläpitämiseksi, ota yhteyttä [EFSTA:han](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Skenaariot

Seuraavat skenaariot ovat Tšekin tasavallan verorekisteröintipalvelun integrointiesimerkistä.

- Käteistapahtumien rekisteröiminen verorekisteröintipalveluun.

    - Lähetä yksityiskohtaiset tapahtumatiedot kirjanpidon rekisteröintipalveluun. Näitä tietoja ovat myyntirivin tiedot sekä alennuksia, maksuja ja veroja koskevat tiedot. Verorekisteröintipalvelu lähettää edelleen tiedot veroviranomaisten verkkopalveluun ja saa veroviranomaisilta vahvistuksen, joka sisältää tapahtuman verotustunnuksen.
    - Tallentaa vastauksen verorekisteröintipalvelusta. Tämä vastaus sisältää esimerkiksi verotiedot, kuten verotustunnuksen ja tapahtuman suojauskoodin.
    - Tulosta rekisteröidyn tapahtuman kirjanpitotiedot kuitille.

- Lahjakorttitoimintojen ja asiakkaan talletusten rekisteröinti verorekisteröintipalveluun.

    - Myönnä tai lisää rahaa lahjakorttiin.
    - Rekisteröin asiakastilin talletus.
    - Luo asiakastilaus ja rekisteröi tilaukselle talletus.
    - Muokkaa asiakastilausta ja ohita tilauksen talletus.
    - Peruuta asiakastilaus ja hyvitä tilauksen talletus.

- Virheiden käsittely, esimerkiksi seuraavat vaihtoehdot.

    - Yritä verorekisteröintiä uudelleen esimerkiksi silloin, kun kirjanpidon rekisteröintipalvelu ei ole käytettävissä, se ei ole valmis tai se ei vastaa.
    - Lykkää kirjanpidon rekisteröintiä.
    - Ohita verorekisteröinti tai merkitse tapahtuma rekisteröidyksi ja sisällytä tietokoodit, jotka poimivat virheen syyn ja lisätiedot.
    - Tarkista kirjanpidon rekisteröintipalvelun käytettävyys ennen uuden myyntitapahtuman avaamista tai myyntitapahtuman viimeistelyä.

### <a name="gift-cards"></a>Lahjakortit

Verorekisteröintipalvelun integrointiesimerkki toteuttaa seuraavia lahjakortteihin liittyviä sääntöjä.

- Myyntitapahtuman *Myönnä lahjakortti*- tai *Lisää lahjakorttiin* -toimintoihin liittyvät myyntirivit merkitään erityismääritteellä, kun tapahtuma rekisteröidään verorekisteröintipalveluun.
- Lahjakorttimaksua käsitellään tavallisena maksuna, ja se merkitään erityisellä määritteellä, kun tapahtuma rekisteröidään verorekisteröintipalveluun.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Asiakastilien talletukset ja asiakastilausten talletukset

Verorekisteröintipalvelun integrointiesimerkissä otetaan käyttöön seuraavat säännöt, jotka liittyvät asiakastilitalletukseen ja asiakastilaustalletuksiin.

- Asiakastilitalletukseen tai asiakastilauksen talletukseen liittyvä tapahtuma rekisteröidään kirjanpidon rekisteröintipalveluun yhtenä rivitapahtumana, ja se merkitään erityisellä määritteellä. Talletusten ALV-ryhmä määritetään tällä rivillä.
- Kun luodaan hybridiasiakastilaus eli asiakastilaus, joka sisältää myymälästä otettavia tuotteita, sekä myöhemmin noudettavia tai toimitettavia tuotteita, kirjanpidon rekisteröintipalveluun kirjattu tapahtuma sisältää rivejä myymälästä vietäviä tuotteita varten sekä tilaustalletuksen rivin.
- Maksua asiakastililtä käsitellään tavallisena maksuna, ja se merkitään erityisellä määritteellä, kun tapahtuma rekisteröidään verorekisteröintipalveluun.
- Asiakkaan tilauksen talletussummaa, jota käytetään asiakastilauksen noutotoimintoon, käsitellään tavallisena maksuna, ja se merkitään erityismääritteellä, kun tapahtuma rekisteröidään kirjanpidon rekisteröintipalveluun.

### <a name="offline-registration"></a>Offline-rekisteröinti

Jos verorekisteröintipalvelu ei siirrä tapahtumatietoja veroviranomaisten kirjanpidon verkkopalveluun (esimerkiksi vastauksen aikakatkaisun vuoksi) ja vastaanoton vahvistusta verkkopalvelulta (tapahtuman verotustunnuskoodi) ei saada, se luo tapahtuman paikallisen allekirjoituksen ja sisällyttää sen sekä erityisvirhekoodin vastaukseen. Verorekisteripalvelu lähettää tapahtumat uudelleen alkuperäiseen tilaukseen taustalla heti, kun verkkoyhteys on palautettu.

### <a name="limitations-of-the-sample"></a>Esimerkin rajoitukset

Verorekisteröintipalvelu tukee vain skenaarioita, joissa arvonlisävero sisältyy hintaan. Siksi **Hinta sisältää arvonlisäveron** -asetuksen on oltava **Kyllä** sekä myymälöille että asiakkaille.

## <a name="set-up-commerce-for-the-czech-republic"></a>Commercen määritys (Tšekin tasavalta)

Tässä osassa kuvaillaan Commerce-asetukset, jotka ovat erityisiä ja suositeltuja Tšekin tasavallassa. Lisätietoja on kohdassa [Commerce-aloitussivu](../index.md).

Ennen kuin voit käyttää Tšekin tasavallan maa-/aluekohtaista toimintoa, sinun on määritettävä seuraavat asetukset.

- Määritä yrityksen ensisijaisessa osoitteessa **Maa/alue**-kentän arvoksi **CZE** (Tšekin tasavalta).
- Jos myymälä sijaitsee Tšekin tasavallassa, määritä sen POS-toimintoprofiilissa **ISO-koodi**-kentän arvoksi **CZ** (Tšekin tasavalta).

Sinun on määritettävä myös seuraavat asetukset Tšekin tasavallassa. Huomaa, että asianmukaiset jakelutyöt on suoritettava asetusten määrityksen jälkeen.

### <a name="set-up-vat-per-czech-republic-requirements"></a>ALV:n määritys Tšekin tasavallan vaatimusten mukaan


Sinun on luotava arvonlisäverokoodit, arvonlisäveroryhmät ja nimikkeen arvonlisäveroryhmät. Määritä myös tuotteiden ja palveluiden arvonlisäverotiedot. Lisätietoja arvonlisävero-ominaisuuksien määrittämisestä ja käyttämisestä on ohjeaiheessa [Arvonlisäveron yleiskatsaus](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Määritä myymälät

Päivitä myymälän tiedot **Kaikki myymälät** -sivulla. Määritä erityisesti seuraavat parametrit.

- Määritä **Arvonlisäveroryhmä**-kentässä arvonlisäveroryhmä, jota pitäisi käyttää myynnissä oletusasiakkaalle.
- Määritä **Hinnat sisältävät arvonlisäveron** -vaihtoehdon arvoksi **Kyllä**.
- Määritä **Nimi**-kenttään yrityksen nimi. Muutoksen avulla voidaan varmistaa, että yrityksen nimi näkyy myyntikuitissa. Vaihtoehtoisesti voit lisätä yrityksen nimen myyntikuitin asetteluun vapaamuotoisena tekstinä.
- Määritä yrityksen tunnusnumero **Verovelvollisen tunnistenumero** -kenttään. Muutoksen avulla voidaan varmistaa, että yrityksen tunnistenumero näkyy myyntikuitissa. Vaihtoehtoisesti voit lisätä yrityksen tunnistenumeron myyntikuitin asetteluun vapaamuotoisena tekstinä.

### <a name="set-up-functionality-profiles"></a>Määritä toimintoprofiilit

POS-toimintoprofiilien määritys.

- Määritä **Kuitin numeroinnit** -pikavälilehdessä kuitin numeroinnit luomalla tai päivittämällä **Myynti**-, **Myyntitilaus**- ja **Palautus** -kuittitapahtumatyyppien tietueita.

### <a name="set-up-registration-numbers"></a>Määritä rekisteröintinumerot

1. Valitse **Organisaation hallinto \> Yleinen osoitekirja \> Rekisteröintityypit \> Rekisteröintityypit**. Uuden rekisteröintityypin luominen Määritä **Maa/alue**-kentän arvoksi **CZE** (Tšekin tasavalta) ja rajaa se organisaatioon.
2. Valitse **Organisaation hallinto \> Yleinen osoitekirja \> Rekisteröintityypit \> Rekisteröintiluokat**. Luo uusi rekisteröintiluokka. Valitse rekisteröintityyppi edellisestä vaiheesta ja määritä **rekisteröintiluokaksi** **Business Premise ID**.
3. Valitse **Organisaation hallinto \> Organisaatiot \> Toimintayksiköt**. Valitse jokaiselle Tšekin tasavallassa sijaitsevalle myymälälle liittyvä yksikkö. Laajenna **Osoite**-pikavälilehdessä avattava **Lisää vaihtoehtoja** -luettelo ja valitse sitten **Lisäasetukset**. 
4. Avatulla **Osoitteiden hallinta** -sivulla on määritettävä seuraavat asetukset:

    - Määritä **Osoite**-pikavälilehden **Maa/alue**-kentän arvoksi **CZE**.
    - Luo uusi tietue **Rekisteröintitunnus**-pikavälilehdessä. Valitse aiemmin luotu rekisteröintityyppi ja määritä rekisteröintinumero.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfiguroi mukautetut kentät siten, että niitä voidaan käyttää myyntikuittien kuittimuodoissa

Voit konfiguroida POS-kuittimuodoissa käytettävät kielitekstit ja mukautetut kentät. Kuittiasetukset luoneen käyttäjän oletusyrityksen tulee olla sama yritys, jossa kielitekstiasetukset luodaan. Vaihtoehtoisesti samat kielitekstit tulisi luoda sekä käyttäjän oletusyrityksessä että sen myymälän yrityksessä, jota varten asetukset luodaan.

Lisää **Kieliteksti**-sivulla seuraavat tietueet kuitin asettelun mukautettujen kenttien otsikoihin. Huomaa, että taulukossa näkyvät **kielitunnukset**, **tekstitunnukset** ja **tekstiarvot** ovat vain esimerkkejä. Voit muuttaa ne tarpeidesi mukaisiksi. Käyttämäsi **tekstin tunnuksen** arvon on kuitenkin oltava yksilöivä, ja niiden on oltava yhtä suuret tai suurempia kuin 900001.

Lisää taulusta seuraavat myyntipisteen otsikot **kielitekstin** **POS**-osaan:

| Kielitunnus | Tekstitunnus | Teksti                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Tiedot                   |
| en-US       | 900006  | Järjestysnumero        |

Lisää **Mukautetut kentät** -sivulla seuraavat tietueet kuitin asettelun mukautettuihin kenttiin. Huomaa, että **otsikkotekstin tunnuksen** arvojen on vastattava **Kieliteksti**-sivulla määritettyjä **tekstitunnuksen** arvoja:

| Nimi                 | Tyyppi    | Otsikon tekstin tunnus |
|----------------------|---------|-----------------|
| TLT                  | Vastaanotto | 900001          |
| SEC                  | Vastaanotto | 900002          |
| SIGN                 | Vastaanotto | 900003          |
| FISCAL               | Vastaanotto | 900004          |
| INFO                 | Vastaanotto | 900005          |
| CONTINUOUSNUMBER     | Vastaanotto | 900006          |

> [!NOTE]
> On tärkeää määrittää oikeat mukautetut kenttien nimet edellisen taulukon mukaan. Virheellisen mukautetun kentän nimi aiheuttaa kuiteissa puuttuvia tietoja.

### <a name="configure-receipt-formats"></a>Kuittimuotojen määrittäminen

Muuta jokaisessa vaaditussa kuittimuodossa **Tulostustoiminta**-kentän arvoksi **Tulosta aina**.

Lisää kuittien muodon suunnittelussa seuraavat mukautetut kentät asianmukaisiin kuittien osiin. Huomaa, että kenttien nimet vastaavat edellisessä osassa määritettyjä kielitekstejä.

- **Otsikko:** Lisää seuraavat kentät.

    - **Myymälän nimi** ja **Verotunnus**: näiden kenttien avulla tulostetaan yrityksen nimi ja tunnusnumero kuitteihin. Vaihtoehtoisesti voit lisätä yrityksen nimen ja tunnistenumeron asetteluun vapaamuotoisena tekstinä.
    - **Myymälän osoite**, **Päivämäärä**, **Aika 24H**, **Kuitin numero** ja **Rekisterinumero**.
    - **Järjestysnumero**: tämä kenttä määrittää kassatapahtuman numeron kirjanpidon rekisteröintipalvelussa.

- **Rivit:** Lisää seuraavat kentät.

    - **Nimikkeen nimi**
    - **Määrä**
    - **Verollinen kokonaishinta**

- **Alatunniste:** Lisää seuraavat kentät.

    - Maksukentät, jotta kunkin maksutavan maksusummat tulostetaan. Lisää esimerkiksi **maksuvälineen nimen** ja **maksuvälinesumman** kentät yhdelle asettelun riville.
    - **ID provozovny/pokladny**: tämä kenttä tulostaa liiketilojen ja kassapäätteiden tunnukset.
    - **BKP**: tämä kenttä tulostaa verovelvollisen suojauskoodin, jonka verorekisteröintipalvelu määrittää.
    - **FIK**: tämä kenttä tulostaa sen tapahtuman verotustunnuksen, jonka veroviranomaisten Internet-palvelu määrittää onnistuneen online-rekisteröinnin yhteydessä.
    - **PKP**: tämä kenttä tulostaa verovelvollisen allekirjoituskoodin, jonka verorekisteröintipalvelu luo offline-rekisteröinnin yhteydessä.
    - **Info**: tämä kenttä tulostaa verorekisteröintipalvelun lisätiedot.

Lisätietoja kuittimuotojen ja kuittien muotojen suunnittelusta on kohdassa [Kuittimuotojen määrittäminen ja suunnitteleminen](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Verointegroinnin määrittäminen (Tšekin tasavalta)

Tšekin tasavallan verorekisteröintipalvelun integrointiesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Commerce SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Efr** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. [Esimerkki](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) koostuu veroasiakirjan tarjoajasta, joka on Commerce runtimen (CRT) laajennus, ja veroliitin, joka on Commerce Hardware Stationin laajennus. Lisätietoja Commerce SDK:n käyttämisestä on kohdissa [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja  NuGetista](../dev-itpro/retail-sdk/sdk-github.md) ja [Koontijakson asetusten määrittäminen riippumattoman pakkauksen SDK:ta varten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Tšekin tasavallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commerce SDK:ssa Commercen versiosta 10.0.29 alkaen. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa Microsoft Dynamics Lifecycle Servicesissa (LCS). Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Tšekin tasavalta) (vanha)](emea-cze-fi-sample-sdk.md).

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
    1. Lataa veroasiakirjan tarjoajan määritystiedosto kohdassa **Määritykset \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml**.
    1. Lataa veroliittimen määritystiedosto kohdassa **Määritykset \> Liittimet \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa LCS:ssä. Tämän verointegraatioesimerkin konfiguraatiotiedostot sijaitsevat seuraavissa Retail SDK -sovelluksen kansioissa kehittäjän virtuaalikoneessa LCS:ssä:
    >
    > - **Veroasiakirjan tarjoajan konfigurointitiedosto:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **Veroyhdistimen konfigurointitiedosto:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**. Määritä **Yleiset**-pikavälilehdessä **Ota kirjanpidon integrointi käyttöön**-asetukseksi **Kyllä**.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**, ja lataa aiemmin lataamasi kirjanpitoasiakirjan toimittajan konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**, ja lataa aiemmin lataamasi kirjanpidon yhdistimen konfigurointitiedosto.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**. Luo uusi yhdistimen toimintoprofiili. Valitse tiedoston tarjoaja ja aiemmin ladattu liitin. Päivitä [tietojen määritysasetukset](#default-data-mapping) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**. Luo uusi liittimen tekninen profiili ja valitse aiemmin ladattu veroliitin. Päivitä [yhdistimen asetukset](#fiscal-connector-settings) tarvittaessa.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmät**. Luo uusi veroliitinryhmä aiemmin luomallesi liittimen toimintoprofiilille.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**. Luo uusi kirjanpidon rekisteröintiprosessi ja verorekisteröintiprosessi vaihe ja valitse aiemmin luomasi kirjanpidon yhdistinryhmä.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**. Valitse siihen myymälään linkitetty toimintoprofiili, jossa rekisteröintiprosessi tulee aktivoida. Valitse **Kirjanpidon rekisteröintiprosessi** -pikavälilehdessä aiemmin luomasi kirjanpidon rekisteröintiprosessi.
1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laiteprofiilit**. Valitse Hardware Stationiin liitetty laiteprofiili, johon verorekisteröintipalvelu liitetään. Valitse **Kirjanpidon oheislaitteet** -pikavälilehdessä aiemmin luomasi liittimen tekninen profiili.
1. Avaa jakeluaikataulu (**Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**) ja valitse työt **1070** ja **1090** siirtääksesi tiedot kanavatietokantaan.

#### <a name="default-data-mapping"></a>Tietojen oletusmääritys

Seuraavat tietojen oletusmääritykset sisältyvät veroasiakirjan tarjoajan konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **ALV-prosenttimääritys** – Arvonlisäverokoodeille määritettyjen veroprosenttiarvojen yhdistäminen **TaxG** (veroryhmä) -määritteeseen pyynnöissä, jotka lähetetään veropalveluun. Tässä on oletusmääritys:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Kunkin parin 1. komponentti edustaa ALV-ryhmää, jota EFR-verorekisteröintipalvelu tukee. Toinen komponentti edustaa vastaavaa arvonlisäveroprosenttia. Lisätietoja EFR:n tukemista ALV-veroryhmistä Tšekin tasavallassa on [EFR:n viitteessä](https://public.efsta.net/efr/).

- **ALV-ryhmän oletusmääritys** – Kaikki ALV-summat, joita ei voi määrittää mihinkään ennalta määritettyihin ALV-ryhmiin, luokitellaan oletusarvoiseen perus-ALV-ryhmään. Tässä on oletusmääritys:

    ```
    A
    ```

- **Talletusten ALV-ryhmän määritys** – Asiakkaan talletussummat ja asiakkaan tilauksen talletussummat luokitellaan talletuksen ALV-ryhmään. Tässä on oletusmääritys:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Veroliittimen asetukset

Seuraavat asetukset sisältyvät veroyhdistimen konfiguraatioon, joka toimitetaan osana verointegraation esimerkkiä:

- **Päätepisteen osoite** – verorekisteröintipalvelun URL-osoite.
- **Aikakatkaisu** – Aika millisekunteina, jonka veroyhdistin odottaa verorekisteröintipalvelun vastausta.

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

> [!NOTE]
> - Tšekin tasavallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commerce SDK:ssa Commercen versiosta 10.0.29 alkaen. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Tšekin tasavalta) (vanha)](emea-cze-fi-sample-sdk.md).
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

Tšekin tasavallan verorekisteröintipalvelun integrointiesimerkki perustuu [verointegraation toimintoihin](fiscal-integration-for-retail-channel.md) ja se kuuluu osana Commerce SDK -pakettiin. Esimerkki sijaitsee **src\\FiscalIntegration\\Efr** -kansiossa [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. [Esimerkki](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) koostuu veroasiakirjan tarjoajasta, joka on CRT:n laajennus, ja veroliittimestä, joka on Commerce Hardware Stationin laajennus. Lisätietoja Commerce SDK:n käyttämisestä on kohdissa [Commerce SDK -esimerkkien ja -viitepakettien lataaminen GitHubista ja  NuGetista](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Koontijakson asetusten määrittäminen riippumattoman pakkauksen SDK:ta varten](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Tšekin tasavallan verorekisteröintipalvelun integraatioesimerkki on saatavilla Commerce SDK:ssa Commercen versiosta 10.0.29 alkaen. Commercen versiossa 10.0.28 ja aiemmissa versioissa on käytettävä Retail SDK:n edellistä versiota kehittäjän virtuaalikoneessa LCS:ssä. Lisätietoja: [Verointegroinnin esimerkkiä koskevat käyttöönoton ohjeet (Tšekin tasavalta) (vanha)](emea-cze-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime -laajennusten rakenne

Veroasiakirjojen palveluntarjoajana toimivan laajennuksen tarkoituksena on luoda palvelukohtaisia asiakirjoja ja käsitellä verorekisteröintipalvelun vastauksia.

#### <a name="request-handler"></a>Pyyntökäsittelijä

Asiakirjatoimittajalle on yksi **DocumentProviderEFRFiscalCZE**-pyyntökäsittelijä, jota käytetään veroasiakirjojen tuottamiseen verorekisteripalvelua varten.

Tämä käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty yhdistintiedoston tarjoajan nimi.

Liitin tukee seuraavia pyyntöjä.

- **GetFiscalDocumentDocumentProviderRequest** – Tämä pyyntö sisältää tietoja siitä, mikä asiakirja tulee luoda. Se palauttaa palvelukohtaisen asiakirjan, jotka on rekisteröitävä kirjanpidon rekisteröintipalveluun.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Tämä pyyntö palauttaa tilattavien tapahtumien luettelon. Tällä hetkellä seuraavia tapahtumia tuetaan: myynti, asiakastilitalletus ja asiakastilausten talletukset.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Tämä pyyntö palauttaa vastauksen verorekisteröintipalvelusta. Tämä vastaus sarjoitettu muodostamaan merkkijonon, joten se on valmis tallennettavaksi.

#### <a name="configuration"></a>Konfigurointi

Veroasiakirjan tarjoajan konfiguraatiotiedosto sijaitsee kohdassa **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/) -säilössä. Tämän tiedoston tarkoitus on ottaa käyttöön asetukset, joiden avulla verotiedoston tarjoaja voidaan konfiguroida Commerce Headquartersista. Tiedostomuoto on verotuksen integroinnin konfiguraation vaatimusten mukainen.

### <a name="hardware-station-extension-design"></a>Hardware station -laajennuksen rakenne

Veroyhdistimenä toimivan laajennuksen tarkoituksena on kommunikoida verorekisteröintipalvelun kanssa. Hardware station -laajennus käyttää HTTP-protokollaa asiakirjojen lähettämiseen, jotka CRT-laajennus luo kirjanpidon rekisteröintipalveluun. Se käsittelee myös verorekisteröintipalvelusta saadut vastaukset.

#### <a name="request-handler"></a>Pyyntökäsittelijä

**EFRHandler**-pyyntökäsittelijä on kirjanpidon rekisteröintipalvelun pyyntöjen käsittelyn aloituspiste.

Käsittelijä on peritty **INamedRequestHandler**-liittymästä. **HandlerName**-menetelmä vastaa käsittelijän nimen palauttamisesta. Käsittelijän nimen on oltava sama kuin Commerce Headquarters -sovelluksessa määritetty veroyhdistimen nimi.

Liitin tukee seuraavia pyyntöjä.

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
