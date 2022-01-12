---
title: Kassakoneen toiminnot, Norja
description: Tämä ohjeaihe sisältää Norjassa käytettävissä olevien kassakoneessa Microsoft Dynamics 365 Commercessa käytettävissä olevien toimintojen yhteenvedon sekä ohjeita toiminnon määrittämiseen.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: bb87b3a7405ef3d8435748813fa66db74b8f0971
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944937"
---
# <a name="cash-register-functionality-for-norway"></a>Kassakoneen toiminnot, Norja

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus kassakonetoiminnoista, joita Norjassa voi käyttää Dynamics 365 Commercessa. Lisäksi ohjeissa on ohjeita toiminnon määrittämisestä. Toiminnot koostuvat seuraavista osista:

- Yleiset myyntipistetoiminnot, jotka ovat asiakkaiden käytettävissä kaikissa maissa tai kaikilla alueilla. Esimerkkinä on asetus, jonka avulla voit estää kuitin kopion tulostamisen useammin kuin kerran.
- Norjan maakohtaisia toimintoja, kuten myyntitapahtumien digitaalisia allekirjoituksia.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Kassakoneen toimintojen yleiskatsaus, Norja

### <a name="common-pos-features"></a>Yleiset POS-toiminnot

Tietoja kaikkien maiden tai alueiden asiakkaiden käytettävissä olevista myyntipisteominaisuuksista on [Dynamics 365 Retail -ohjeresursseissa](../index.md).

Seuraavia POS-lokalisointitoimintoja, jotka on aiemmin otettu käyttöön ja jotka on määritetty asiakkaiden käyttöön kaikissa maissa tai kaikilla alueilla, voidaan nyt käyttää erityisesti Norjassa:

- **Tulosta kuitin tekstikentät suureen fonttikokoon.** Kuitin muodon suunnittelussa voit käyttää **Fontin koko** -parametria määrittääksesi, että kuittimuodon kentässä käytetään suurta fontin kokoa. (Suuri fontin koko on noin kaksi kertaa suurempi kuin tavallinen fonttikoko.) Tämän parametrin avulla voit esimerkiksi tulostaa kuitin kopion Kopio-ilmaisimen suurilla merkeillä.
- **Rekisteröi kuittikopioiden tulostus myyntipisteen kirjaustapahtumalokiin.** POS-toimintoprofiilin **Kirjaus**-parametrin avulla voit sallia kuittien kopioiden tulostamisen ja muiden POS-kirjaustapahtumien rekisteröimisen. Kirjaustapahtumat rekisteröidään kanavatietokantaan ja Headquartersiin. Voit tarkastella kirjaustapahtumia **Kirjaustapahtumat**-sivulla.
- **Estä kuitin kopion tulostaminen useamman kuin yhden kerran.** Kun POS-toimintoprofiilin **Kirjaus**-parametri on käytössä, **Salli kuittikopioiden tulostaminen** -POS-oikeus ohjaa kuittien kopioiden tulostamista. On myös asetus, jonka avulla voit estää kuitin kopion tulostamisen useammin kuin kerran.

Lisäksi seuraava myyntipistetoiminto on ollut käytössä Norjassa, mutta se on nyt asiakkaiden käytettävissä kaikissa maissa tai kaikilla alueilla:

- **Rekisteröi lisätapahtumia myyntipisteen kirjaustapahtumalokiin.** Jos POS-toimintoprofiilin **Kirjaus**-parametri on otettu käyttöön, seuraavat tapahtumat rekisteröidään myyntipisteen kirjaustapahtumalokiin:

    - Hinnantarkistukset
    - Veron ohitukset
    - Korjaukset rivimääriin
    - Tapahtumien tyhjentäminen kanavatietokannasta

### <a name="norway-specific-pos-features"></a>Norjan maakohtaiset POS-ominaisuudet

Seuraavat Norjan maakohtaiset myyntipisteominaisuudet otetaan käyttöön, kun POS-toimintoprofiilin **ISO-koodi**-parametriksi on määritetty **Ei**.

#### <a name="digital-signing-of-sales-transactions"></a>Myyntitapahtumien digitaalinen allekirjoittaminen

Jokainen myyntitapahtuma allekirjoitetaan digitaalisesti. Allekirjoitus luodaan ja tallennetaan myyntipisteen tapahtumakirjauskansioon samalla, kun tapahtuma viimeistellään. Allekirjoitus on käytettävissä myös kirjauskansiossa, joka viedään kirjausta varten.

Vain käteismyynnin tapahtumat allekirjoitetaan. Seuraavassa on muutamia esimerkkejä tapahtumista, jotka eivät sisälly allekirjoitusprosessiin:

- Ennakkomaksut (Asiakastilin talletus)
- Myyntitilausten ennakkomaksut (asiakkaan tilauksen talletus)
- Lahjakortin myöntäminen
- Ei-myyntitapahtumat (esimerkiksi liukuva merkintä, maksuvälineen poisto)

Allekirjoitetut tiedot ovat tekstimerkkijono, joka koostuu seuraavista tietokentistä. Tietokentät erotetaan puolipisteillä.

1. Saman myyntipisteen edellinen allekirjoitus (Nollaa \[**0**\] käytetään ensimmäiselle tapahtumalle.)
2. Tapahtuman päivämäärä
3. Tapahtuman aika
4. Peräkkäinen allekirjoitettu tapahtumanumero
5. Tapahtuman summa vero mukaan luettuna
6. Tapahtuman summa ilman veroa

Digitaalinen allekirjoitusprosessi käyttää 1024-bittistä RSA-avainta, jossa on SHA-1-hash-toiminto (RSA-SHA1-1024). Commerce Scale Unitiin asennettua sertifikaattia käytetään allekirjoitettaessa. Sertifikaatin yksilöivä tunnus (jalanjälki) tallennetaan yhdessä allekirjoituksen kanssa.

Allekirjoitus tallennetaan myymälätietokantaan ja pääkonttorin tietokantaan yhdessä tapahtumatietojen kanssa. Voit tarkastella tapahtuman allekirjoitusta ja sen luomisessa käytettyjä tapahtumatietoja **Kirjanpitotapahtumat**-pikavälilehdessä **Myymälän tapahtumat** -sivulla.

#### <a name="receipts"></a>Vastaanotot

Norjassa kuitit voivat sisältää mukautettuja kenttiä käyttäen toteutettuja lisätietoja:

- **Kuitin otsikko** – Voit määrittää kuitin tyypin lisäämällä kentän kuittimuodon asetteluun. Esimerkiksi myyntikuittiin lisätään teksti "Myyntikuitti".
- **Allekirjoitettu tapahtumajärjestysnumero** – Allekirjoitetun tapahtuman järjestysnumero voi näkyä kuitissa, jolloin tulostettu kuitti liitetään tietokannassa olevaan digitaaliseen allekirjoitukseen.
- **Kuittien loppusummat** – Mukautetut kentät sulkevat pois muut kuin myyntisummat tapahtumien kokonaissummista kuittien loppusummissa. Muut kuin myyntisummat sisältävät seuraavien toimintojen summat:

    - Ennakkomaksut (Asiakastilin talletus)
    - Myyntitilausten ennakkomaksut (asiakkaan tilauksen talletus)
    - Lahjakortin myöntäminen
    - Lisää varoja lahjakorttiin

#### <a name="x-and-z-reports"></a>X- ja Z-raportit

X- ja Z-raportteihin sisällytettävät tiedot perustuvat Norjan vaatimuksiin. Esimerkiksi **käteisen kokonaismyyntisummat** sisältävät vain käteismyyntitapahtumien summat ja sulkevat pois lahjakorttitoiminnot ja ennakkomaksut. Käteismyynnit yhteensä luetellaan myös nimikeryhmän ja maksutavan mukaan. Lisäksi kumulatiiviset **Kokonaismyynti**- ja **Kokonaispalautukset**-summat ylläpidetään ja tulostetaan.

#### <a name="saf-t-cash-register-audit-file"></a>Kassakoneen SAF-T-kirjaustiedosto

Voit viedä POS-tapahtumakirjauskansion valmiiksi määritetyssä kassapäätteen muodossa: Standard Audit File - Tax (SAF-T) Cash Register. Kirjaustiedosto sisältää tietoja organisaatiosta, asiaankuuluvat päätiedot (kuten nimikeryhmät, nimikkeet ja verokoodit), käteismyyntitapahtumatiedot sekä näiden tapahtumien allekirjoitukset, ei-myyntitapahtuman tiedot ja päivän päättymisen raportin tiedot.

Kirjaustiedosto voidaan viedä seuraavissa tilanteissa:

- Myymälää kohti
- Kaikki myymälät
- Päätettä kohti
- Kaikki päätteet

Voit myös lähettää raportin yhdestä yrityksestä toisen yrityksen puolesta. Tällöin vienti on suoritettava toimivasta yrityksestä ja määritettävä raportoiva yritys raportin lähettäjäksi.

SAF-T Cash Register -muoto on toteutettu Headquartersissa [sähköisen raportoinnin](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) avulla. 

## <a name="setting-up-commerce-for-norway"></a>Commercen määritys (Norja)

Tässä osassa kuvaillaan asetukset, jotka ovat erityisiä ja suositeltuja Norjassa. Lisätietoja: [Dynamics 365 Retail -ohjeresurssit](../index.md).

Voit käyttää Norjan maakohtaisia toimintoja seuraavasti:

- Määritä yrityksen ensisijaisessa osoitteessa **Maa/alue**-kentän arvoksi **NOR** (Norja).
- Jos myymälä sijaitsee Norjassa, määritä sen POS-toimintoprofiilissa **ISO-koodi**-kentän arvoksi **NO** (Norja).

Sinun on määritettävä myös seuraavat asetukset Norjassa.

### <a name="set-up-the-legal-entity"></a>Määritä yritys

Varmista, että yrityksen nimi on määritetty. Tämä nimi tulostetaan X- ja Z-raportteihin.

Määritä lisäksi organisaationumero **Pankkikoodi**-kenttään **Pankkitilitiedot**-pikavälilehdessä.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Arvonlisäveron (ALV) määrittäminen Norjan vaatimusten mukaan


Sinun on luotava arvonlisäverokoodit, arvonlisäveroryhmät ja nimikkeen arvonlisäveroryhmät. Määritä myös tuotteiden ja palveluiden arvonlisäverotiedot. Lisätietoja arvonlisäveron määrittämisestä ja käyttämisestä on ohjeaiheessa [Arvonlisäveron yleiskatsaus](../../finance/general-ledger/indirect-taxes-overview.md).

Määritä myös arvonlisäveroryhmät ja ota käyttöön Norjan myymälöiden **Hinnat sisältävät arvonlisäveron** -vaihtoehto.

### <a name="set-up-functionality-profiles"></a>Määritä toimintoprofiilit

Kirjaus on otettava käyttöön ja kuittien numeroinnit on määritettävä.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Myymälän työntekijöiden myyntipisteen käyttöoikeusryhmien ja yksittäisten käyttöoikeusasetusten päivittäminen

Määritä **Salli kuitin kopion tulostus** -käyttöoikeus sopivalle arvolle:

- **Salli aina** – Operaattori voi tulostaa kopion kuitista useita kertoja.
- **Salli vain kerran** – Operaattori voi tulostaa kopion kuitista vain kerran.
- **Salli vain kerran ja vain siinä tapauksessa, että HQ-tietokanta on käytettävissä** – Operaattori voi tulostaa kuitista kopion vain kerran ja vain siinä tapauksessa, että HQ-tietokanta on käytettävissä Commerce Data Exchange: Real-time Servicen kautta, jotta järjestelmä pystyy varmentamaan, ettei kuittien kopioita ole aiemmin tulostettu mihinkään myymälään.
- **Ei milloinkaan** – Operaattori ei voi tulostaa kopioita kuitista.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfiguroi mukautetut kentät siten, että niitä voidaan käyttää myyntikuittien kuittimuodoissa

Lisää **Kieliteksti**-sivulla seuraavat tietueet kuitin asettelun mukautettujen kenttien otsikoihin. Huomaa, että taulukossa näkyvät **kielitunnukset**, **tekstitunnukset** ja **tekstiarvot** ovat vain esimerkkejä. Voit muuttaa ne tarpeidesi mukaisiksi.

| Kielitunnus | Teksti                   | Tekstitunnus |
|-------------|------------------------|---------|
| en-US       | Kuitin nimi          | 900011  |
| en-US       | On lahjakortti           | 900012  |
| en-US       | Yhteensä (myynti)          | 900013  |
| en-US       | Vero yhteensä (myynti)      | 900014  |
| en-US       | Yhteensä veron kanssa (myynti) | 900015  |
| en-US       | Vero (myynti)     | 900016  |
| en-US       | Käteistapahtuman tunnus    | 900017  |

Lisää **Mukautetut kentät** -sivulla seuraavat tietueet kuitin asettelun mukautettuihin kenttiin. Huomaa, että **otsikkotekstin tunnuksen** arvojen on vastattava **Kieliteksti**-sivulla määritettyjä **tekstitunnuksen** arvoja.

| Nimi                            | Tyyppi    | Otsikon tekstin tunnus |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Vastaanotto | 900011          |
| IsGiftCard                      | Vastaanotto | 900012          |
| SalesTotalExt                   | Vastaanotto | 900013          |
| TaxTotalExt                     | Vastaanotto | 900014          |
| TotalWithTaxExt                 | Vastaanotto | 900015          |
| AmountPerTaxExt                 | Vastaanotto | 900016          |
| CashTransactionSequentialNumber | Vastaanotto | 900017          |

> [!NOTE]
> On tärkeää määrittää oikeat mukautetut kenttien nimet edellisen taulukon mukaan. Virheellisen mukautetun kentän nimi aiheuttaa kuiteissa puuttuvia tietoja.

### <a name="configure-receipt-formats"></a>Kuittimuotojen määrittäminen

Muuta jokaisessa vaaditussa kuittimuodossa **Tulostustoiminta**-kentän arvoksi **Tulosta aina** kuittimuodolle.

Lisää kuittien muodon suunnittelussa seuraavat mukautetut kentät asianmukaisiin kuittien osiin. Huomaa, että kenttien nimet vastaavat edellisessä osassa määritettyjä kielitekstejä.

1. Ylätunniste:

    - **Kuitin otsikko** – Tämä kenttä määrittää kuitin tyypin.
    - **Käteistapahtuman tunnus** – Tämä kenttä tulostaa allekirjoitetun käteistapahtuman sarjanumeron.

2. Rivit:

    - **On lahjakortti** – Tämä kenttä merkitsee kuittirivin, joka liittyy Myönnä lahjakortti- tai Lisää lahjakorttiin -toimintoon.

3. Alatunniste:

    - **Kokonaissumma (myynti)** – Tämä kenttä tulostaa kuitin käteismyynnin kokonaissumman. Summa ei sisällä veroa. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
    - **Veron kokonaissumma (myynti)** – Tämä kenttä tulostaa kuitin käteismyynnin verojen kokonaissumman. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
    - **Kokonaissumma sis.verot (myynti)** – Tämä kenttä tulostaa kuitin käteismyynnin kokonaissumman. Summa sisältää veron. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.
    - **Veronsumma (myynti)** – Tämä kenttä tulostaa kuitin käteismyynnin verojen summan verokoodikohtaisesti. Ennakkomaksut ja lahjakorttitoiminnot jätetään pois.

Lisätietoja kuittimuotojen ja kuittien muotojen suunnittelusta on kohdassa [Kuittimuotojen määrittäminen ja suunnitteleminen](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>SAF-T Cash Register -vientimuodon määrittäminen

SAF-T Cash Register -konfiguraatio on mahdollista ladata Microsoft Dynamics Lifecycle Services (LCS) -palvelusta. Lisätietoja on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Lataa seuraavat konfiguraatiot:

- **Retail channel data.version.1** – Tietomallin konfigurointi.
- **DMM Retail channel data.version.1.14** – Tietomallin yhdistämismäärityksen konfigurointi.
- **NO SAF T Cash Register.version.1.20** – Muodon konfiguraatio.

Kun olet tuonut konfiguraatiot, valitse **Commercen parametrit** -sivun **Sähköiset tiedostot** -välilehden **SAF-T Cash register -vientimuoto** -kentässä tuodun muotokonfiguraation nimi.

Liitä pakolliset päätiedot myös aiemmin määritettyihin SAF-T-vakiokoodeihin. Lisätietoja on Norjan verohallinnon toimittamassa SAF-T Cash register -dokumentaatiossa. Voit luoda yhdistämismäärityksen asettamalla uuden **SAF-T Cash register -koodi** -kentän seuraavilla sivuilla:

- Nimikeryhmät
- Maksutavat
- Arvonlisäverokoodit

### <a name="configure-channel-components"></a>Määritä kanavakomponentit

Voit ottaa Norjan toiminnot käyttöön määrittämällä kanavakomponentit. Lisätietoja on kohdassa [käyttöönoton ohjeet](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
