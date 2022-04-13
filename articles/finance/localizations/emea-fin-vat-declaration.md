---
title: ALV-ilmoitus (Suomi)
description: Tässä aiheessa kuvataan, miten ALV-ilmoitus määritetään ja luodaan Suomessa.
author: liza-golub
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Finland
ms.author: elgolu
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2bba16b26a50b7f0a4add292cb1238182ab229f9
ms.sourcegitcommit: acac5e59be7c8f4e9a7ae9be58c636c70342e784
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8466881"
---
# <a name="vat-declaration-finland"></a>ALV-ilmoitus (Suomi)

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten ALV-ilmoitus määritetään ja luodaan Suomessa virallisessa XML-muodossa. Siinä kerrotaan myös, miten ALV-ilmoitus esikatsellaan Microsoft Excelissä.

Voit luoda raportin automaattisesti luomalla ensin tarpeeksi arvonlisäverokoodeja, jotta voit pitää erillistä ALV-kirjanpitoa jokaisesta Suomen arvonlisäveroilmoituksessa raportoitavasta toiminnasta. Lisäksi ALV-ilmoituksen sähköisen raportoinnin (ER) muodon sovelluskohtaisissa parametreissa arvonlisäverokoodit liitetään **Raporttikentän haku** -hakukentän hakutulokseen. Seuraavassa taulukossa Hakutulos-sarakkeessa näkyy hakutulos, joka on määritetty valmiiksi tietylle ALV-ilmoituskentän tunnukselle ALV-ilmoitusmuodossa. Näiden tietojen avulla voit liittää arvonlisäverokoodit oikein hakutuloksiin ja sitten ALV-ilmoituskentän tunnukseen.

## <a name="vat-declaration-overview"></a>ALV-ilmoituksen yleiskuvaus

Suomen ALV-ilmoitus sisältää seuraavat kentät, joita käytetään arvonlisäveroihin liittyvien summien raportoinnissa.

| Kentän tunnus (tunnus) | Kuvaus (englanti) | Kuvaus (suomi) | Haun tulos |
|---|---|---|---|
| 301 | Kotimaanmyynnin vero vakioveroprosenttina. | Kotimaan verollinen myynti yleisellä verokannalla | DomesticSalesStandardRate |
| 302 | Kotimaanmyynnin vero korkeampana alennettuna veroprosenttina. | Kotimaan verollinen myynti suuremman alennetun verokannan mukaan | DomesticSalesHigherReducedRate |
| 303 | Kotimaanmyynnin vero alempana alennettuna veroprosenttina. | Kotimaan verollinen myynti pienemmän alennetun verokannan mukaan | DomesticSalesLowerReducedRate |
| 304 | Vero tuotteiden tuonnista Euroopan unionin (EU) ulkopuolelta. | Vero tavaroiden maahantuonnista EU:n ulkopuolelta | <p>ImportsOfGoods</p><p>ImportsOfGoodsUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 305 | Muista EU:n jäsenvaltioista ostettujen tavaroiden vero. | Vero tavaraostoista muista EU-maista | <p>GoodsPurchasedFromEU</p><p>GoodsPurchasedFromEUUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 306 | Muista EU:n jäsenvaltioista ostettujen palveluiden vero. | Vero palveluostoista muista EU-maista | <p>ServicesPurchasedFromEU</p><p>ServicesPurchasedFromEUUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 307 | Verokauden vähennyskelpoinen vero. | Verokauden vähennettävä vero | <p>Vähennysmäärä</p><p>Kun **Käytä veroa** -valintaa käytetään:</p><ul><li>GoodsPurchasedFromEUUseTax</li><li>ImportsOfGoodsUseTax</li><li>PurchasesReverseChargeUseTax</li><li>ServicesPurchasedFromEUUseTax</li></ul> |
| 308 | Maksettava vero/palautukseen oikeuttava negatiivinen vero (‒). | Maksettava vero / Palautukseen oikeuttava vero (-) | Ei käytettävissä. Määrä lasketaan automaattisesti. |
| 309 | Arvonlisäverollinen liikevaihto arvonlisäverolla 0 (nolla). | 0-verokannan alainen liikevaihto | TaxableSalesZero |
| 310 | EU:n ulkopuolelta peräisin olevien tavaroiden tuonti. | Tavaroiden maahantuonnit EU:n ulkopuolelta | <p>ImportsOfGoods</p><p>ImportsOfGoodsUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 311 | Tavaroiden myynti muihin EU:n jäsenvaltioihin. | Tavaroiden myynnit muihin EU-maihin | EUSalesOfGoods |
| 312 | Palveluiden myynti muihin EU:n jäsenvaltioihin. | Palveluiden myynnit muihin EU-maihin | EUSalesOfServices |
| 313 | Muista EU:n jäsenvaltioista peräisin olevien tavaroiden ostot. | Tavaraostot muista EU-maista | <p>GoodsPurchasedFromEU</p><p>GoodsPurchasedFromEUUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 314 | Muista EU:n jäsenvaltioista peräisin olevien palveluiden ostot. | Palveluostot muista EU-maista | <p>ServicesPurchasedFromEU</p><p>ServicesPurchasedFromEUUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 315 | ALV-huojennukseen oikeuttava liikevaihto. | Alarajahuojennukseen oikeuttava liikevaihto | Ei käytettävissä. Summa täytetään **ALV-helpotusta - myyntisumman** käyttäjän syöteparametria käyttäen raportin valintaikkunassa. |
| 316 | ALV-huojennukseen oikeuttava vero. | Alarajahuojennukseen oikeuttava vero | Ei käytettävissä. Summa täytetään **ALV-helpotusta - verosumman** käyttäjän syöteparametria käyttäen raportin valintaikkunassa. |
| 317 | ALV-helpotuksen summa. | Alarajahuojennuksen määrä | Ei käytettävissä. Määrä lasketaan automaattisesti. |
| 318 | Rakennuspalveluiden ja hävikkimetallin ostoista perittävä vero (käänteinen verovelvollisuus). | Vero rakentamispalvelun ja metalliromun ostoista | <p>PurchasesReverseCharge</p><p>PurchasesReverseChargeUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |
| 319 | Rakennuspalveluiden ja hävikkimetallin myynti (käänteinen verovelvollisuus). | Rakentamispalvelun ja metalliromun myynnit | SalesReverseCharge |
| 320 | Rakennuspalveluiden ja hävikkimetallin ostot (käänteinen verovelvollisuus). | Rakentamispalvelun ja metalliromun ostot | <p>PurchasesReverseCharge</p><p>PurchasesReverseChargeUseTax (kun **Käytä veroa** -valintaa käytetään)</p> |

Lisätietoja käänteisen verovelvollisuuden määrittämisestä: [Käänteinen verovelvollisuus](emea-reverse-charge.md).

Lisätietoja sovelluskohtaisten parametrien määrittämisestä on jäljempänä tässä ohjeaiheessa kohdassa [ALV-ilmoituskenttien sovelluskohtaisten parametrien määrittäminen](#set-up).

## <a name="set-up-the-vat-declaration-for-finland"></a>Suomen ALV-ilmoituksen määritys

Nämä tehtävät valmistelevat Microsoft Dynamics 365 Finance -ympäristösi luomaan sähköisen tiedoston Suomen ALV-ilmoitusta varten ja esikatselemaan ALV-summia Excel-muodossa.

- [ER-konfiguraatioiden tuominen](#import-er).
- [Sovelluskohtaisten parametrien määrittäminen ALV-ilmoituskentille](#set-up).
- [ALV-raportointimuodon asetus Excelin esikatselua varten](#setup-preview).
- [Sähköisten sanomien määrittäminen](#setup-em).
- [Määritä arvonlisäveroa raportoivan yrityksen ALV-rekisterinumero](#vat-id).

### <a name="import-er-configurations"></a><a name="import-er"></a>ER-konfiguraatioiden tuominen

Avaa **Sähköisen raportoinnin** työtila ja tuo viimeisimmät versiot seuraavista ER-muodoista kohdassa **Veroilmoitusmalli**.

- ALV-ilmoitus TXT (FI)
- ALV-ilmoitus, Excel (FI)

Lisätietoja on kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä varastosta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up"></a>Sovelluskohtaisten parametrien määrittäminen ALV-ilmoituskentille

Kun haluat luoda ALV-ilmoituksen automaattisesti, liitä arvonlisäverokoodit Financeen ja hakutuloksiin ER-konfiguraatiossa.

> [!NOTE]
> Suosittelemme, että otat tätä varten käyttöön **Käytä sovelluskohtaisia parametreja sähköisen raportoinnin muotojen aiemmista versioista** -ominaisuuden **Ominaisuuksienhallinta**-työtilassa. Kun tämä ominaisuus on käytössä, ER-muodon aiemmassa versiossa konfiguroivat parametrit tulevat automaattisesti käyttöön saman muodon myöhemmässä versiossa. Jos tätä toimintoa ei ole otettu käyttöön, sovelluskohtaiset parametrit on määritettävä erikseen kullekin muotoversiolle. **Käytä sovelluskohtaisia parametreja aiemmista ER-muotojen versioista** -ominaisuus on käytettävissä **Ominaisuuksien hallinta** -työtilassa Financen versiosta 10.0.23 alkaen. Lisätietoja ER-muodon parametrien määrittämisestä kullekin yritykselle on kohdassa [ER-muodon parametrien määrittämisestä kullekin yritykselle](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Seuraavia ohjeita noudattamalla voit määrittää, mitkä Financen liikevaihtoverokoodit luovat minkä kenttätunnuksen Suomen ALV-ilmoitukseen.

1. Valitse **Työtilat** \> **Sähköinen raportointi** ja sitten **Raportointimääritykset**.
2. Valitse **ALV-ilmoitus TXT (FI)** -konfiguraatio ja valitse sitten toimintoruudusta **Määritykset \> Sovelluskohtaisten parametrien määritys**.
3. Valitse **Sovelluskohtaiset parametrit** -sivun **Haku**-pikavälilehdestä **Raporttikentän haku**.
4. Liitä arvonlisäverokoodit ja raporttikentät määrittämällä seuraavat **Ehdot**-pikavälilehden kentät.


    | Kenttä | Kuvaus |
    |---|---|
    | Haun tulos | Valitse raporttikentän arvo. Lisätietoja arvoista ja niiden määrityksestä ALV-ilmoitusriveille on tämän ohjeaiheen aiemmassa kohdassa [ALV-ilmoituksen yhteenveto](#vat-declaration-overview). |
    | Alv-koodi | Valitse raporttikenttään liitettävä arvonlisäverokoodi. Valittua arvonlisäverokoodia käyttävät kirjatut verotapahtumat kerätään soveltuvassa ilmoitusruudussa. On suositeltavaa erotella arvonlisäverokoodit siten, että yksi arvonlisäverokoodi luo summia vain yhteen ilmoitusruutuun. |
    | Tapahtumaluokan valitsin | <p>Jos olet luonut tarpeeksi arvonlisäverokoodeja ilmoitusruudun määrittämiseksi, valitse **\*Ei tyhjä\***. Jos et luonut tarpeeksi arvonlisäverokoodeja niin, että yksi arvonlisäverokoodi luo summia vain yhteen ilmoitusruutuun, voit määrittää tapahtumaluokan valitsimen. Seuraavat tapahtumaluokan valitsimet ovat käytettävissä:</p><ul><li>**Osto**</li><li>**PurchaseExempt** (verovapaa osto)</li><li>**PurchaseReverseCharge** (oston käänteisen kulun verosaatavat)</li><li>**Myynti**</li><li>**SalesExempt** (veroton myynti)</li><li>**SalesReverseCharge** (oston käänteisen kulun tai myynnin käänteisen kulun maksettava vero)</li><li>**Käyttövero**</li></ul><p>Lisäksi kutakin tapahtumaluokan valitsinta varten on käytettävissä hyvityslaskun luokan valitsin. Yksi näistä luokan valitsimista on esimerkiksi **PurchaseCreditNote** (ostohyvityslasku).</p><p>Luo jokaiselle arvonlisäverokoodille kaksi riviä: yksi, jolla on tapahtumaluokan valitsimen arvo ja toinen, jolla on tapahtumaluokan valitsin hyvityslaskun arvoa varten.</p> |

    > [!NOTE]
    > Liitä kaikki arvonlisäverokoodit hakutuloksiin. Jos jokin arvonlisäverokoodi ei saa luoda arvoja ALV-ilmoitukseen, liitä ne **Muut**-hakutulokseen.

5. Muuta **Tila**-kentän arvoksi **Valmis**.
6. Valitse toimintoruudusta **Vie**, kun haluat viedä sovelluskohtaisten parametrien asetukset.
7. Valitse **ALV-ilmoitus-Excel (FI)** -konfigurointi ja tuo **ALV-ilmoitus-Excel (FI)** -kohteen parametrit valitsemalla toimintoruudusta **Tuo**.
8. Valitse **Tila**-kentässä **Valmis**.

### <a name="set-up-the-vat-reporting-format-to-preview-amounts-in-excel"></a><a name="setup-preview"></a>ALV-raportointimuodon asetus Excelin esikatselua varten

1. Etsi ja valitse **Ominaisuuksien hallinta** -työtilan luettelosta **ALV-ilmoitusmuotoiset raportit** -ominaisuus ja valitse sitten **Ota käyttöön nyt**.
2. Siirry kohtaan **Vero** \> **Epäsuorat verot** \> **Arvonlisävero** \> **Arvonlisäveroviranomaiset** ja valitse veroviranomainen.
3. Valitse **Raportin asettelu** -kentässä **Oletus**.
4. Siirry kohtaan **Kirjanpito** \> **Asetukset** \> **Kirjanpitoparametrit**.
5. Valitse **Arvonlisävero**-välilehden **Veroasetukset**-pikavälilehden **ALV-ilmoituksen muodon määritys** -kentästä **ALV-ilmoitus-Excel (FI)** ER-muoto.

    Tämä muoto tulostetaan, kun suoritat **Ilmoita arvonlisävero tilityskaudelle** -raportin. Se tulostetaan myös, kun valitset **Arvonlisäveromaksut**-sivulla **Tulosta**.

Jos konfiguroit ALV-ilmoituksen Suomessa yrityksessä, jossa on [useita ALV-rekisteröintejä](emea-reporting-for-multiple-vat-registrations.md), toimi seuraavasti.

1. Siirry kohtaan **Kirjanpito** \> **Asetukset** \> **Kirjanpitoparametrit**.
2. Valitse **Arvonlisävero**-välilehden **Sähköisen raportoinnin maat/alueet** -pikavälilehdessä **FIN**-rivillä ER-muoto **VAT Declaration Excel (FI)**.

### <a name="set-up-electronic-messages"></a><a name="setup-em"></a>Sähköisten sanomien määrittäminen

Sähköisen viestinnän (EM) toiminnallisuus on tarkoitettu ylläpitämään erilaisia prosesseja, joita käytetään sähköisessä raportoinnissa eri asiakirjatyypeille. Lisätietoja sähköisestä viestinnästä on kohdassa [Sähköinen viestintä](../general-ledger/electronic-messaging.md).

#### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a><a name="import-em"></a>Lataa ja tuo tietopaketti, joka sisältää sähköisten viestien esimerkkiasetukset

Prosessi, jossa määritetään sähköisen viestinnän toiminto, jotta Suomen ALV-ilmoitus voidaan luoda TXT-muodossa ja esikatsella sitä Excelissä, on useita vaiheita. Koska joidenkin yksiköiden tietoja käytetään ER-määrityksessä, käytä esimääritettyjen arvojen joukkoa, joka toimitetaan liittyvien taulujen tietoyksiköiden pakettiin. Voit laajentaa näitä asetuksia tai luoda omia.

> [!NOTE]
> Joissakin paketin tietoyksiköiden tietueissa on linkki ER-määrityksiin. Ennen kuin aloitat tietoyksiköiden paketin tuonnin, [tuo ER-konfiguraatiot Financeen](#import-er).

1. Valitse [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) -kohdan jaetussa käyttöomaisuuskirjastossa käyttöomaisuuserän tyypiksi **Tietopaketti** ja lataa sitten **FI – ALV-ilmoitus – EM** -paketti. Ladatun tiedoston nimi on **FI VAT declaration EM package.zip**.
2. Valitse Financessa **Tietojen hallinta** -työtilassa **Tuo**.
3. Kirjoita **Tuo**-pikavälilehden **Ryhmän nimi**-kenttään työn nimi.
4. Valitse **Valitut yksiköt** -välilehdessä **Lisää tiedosto**.
5. Varmista **Lisää tiedosto** -valintaikkunassa, että **Lähteen tietomuoto** -kentän arvo on **Paketti**, valitse **Lataa palvelimeen ja lisää** sekä valitse sitten aiemmin lataamasi zip-tiedosto.
6. Valitse **Sulje**.
7. Valitse tietoyksiköiden lataamisen jälkeen toimintoruudusta **Tuo**.
8. Siirry kohtaan **Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköiset sanomat** ja vahvista tuodun sähköisen sanoman käsittely (**FI ALV-ilmoitus**).

Lisätietoja tietojen hallintakehyksen käytöstä on kohdassa [Tiedonhallinta](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

#### <a name="configure-electronic-messages"></a>Sähköiset sanomat – määritys

1. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Tietueiden täyttötoiminnot**.
2. Valitse **FI – Täytä ALV-palautustietueet** -rivi ja valitse **Muokkaa kyselyä**.
3. Suodatinta käyttämällä voit määrittää raporttiin sisällytettävät tilityskaudet.
4. Jos haluat raportoida muiden tilityskausien verotapahtumat eri ilmoituksessa, luo uusi **Täytä tietueet** -toimenpide ja valitse asianmukaiset tilityskaudet.

### <a name="set-up-the-vat-registration-number-of-the-company-that-is-reporting-vat"></a><a id="vat-id"></a>Määritä arvonlisäveroa raportoivan yrityksen ALV-rekisterinumero

Kun haluat luoda ALV-ilmoituksen, määritä organisaation verorekisteröintinumero (kenttä 010, Asiakkaan y-tunnus tai henkilötunnus).

1. Valitse **Organisaation hallinto** \> **Organisaatiot** \> **Yritykset**.
2. Valitse yritys ja sitten **Rekisteröintitunnukset**.
3. Valitse tai luo osoite Suomessa. Valitse sitten **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
4. Valitse **Rekisteröintityyppi**-kentässä Suomea varten rekisteröity rekisteröintityyppi, joka käyttää **ALV-tunnus**-rekisteröintiluokkaa.
5. Anna **Rekisteröintinumero**-kentässä veronumero.
6. Kirjoita **Voimassa**-kenttään **Yleiset**-välilehdessä päivämäärä, jolloin numero tulee voimaan.

Lisätietoja rekisteröintiluokkien ja rekisteröintityyppien määrittämisestä on kohdassa [Rekisteröintitunnukset](emea-registration-ids.md).

Seuraavia ohjeita noudattamalla voit määrittää ALV-rekisteröintinumeron, jota EM käyttää Suomen ALV-ilmoituksen luonnin yhteydessä.

1. Mene kohtaan **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sähköisten sanomien käsittely** ja valitse **FI ALV-ilmoitus** -käsittely.
2. Määritä **Sanoman lisäkentät** -pikavälilehden **Verorekisteröintinumero**-kenttään ALV-rekisteröintinumero, jota on käytettävä Suomen ALV-ilmoituksessa.
3. Tallenna muutokset.

Jos ALV-rekisteröintinumeroa ei ole määritetty **FI ALV-ilmoituksen** käsittelyn **Verorekisteröintinumero**-lisäkentässä, järjestelmä hakee sen rekisteröintitunnuksesta,joka on määritetty sen yrityksen ominaisuuksissa, joka on liitetty **ALV-tunnuksen** rekisteröintiluokkaan.

## <a name="preview-the-vat-declaration-in-excel"></a>ALV-ilmoituksen esikatselu Excelissä

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="report-sales-tax-for-settlement-period"></a>ALV-ilmoituksen esikatselu Excelissä kausittaisen Ilmoita arvonlisävero tilityskaudelle -tehtävän avulla

1. Valitse **Vero** \> **Kausittaiset tehtävät** \> **Ilmoitukset** \> **Arvonlisävero** \> **Ilmoita arvonlisävero tilityskaudelle**.
2. Määritä seuraavat kentät.

    | Kenttä | Kuvaus |
    |---|---|
    | Päivämäärästä | Valitse raportointikauden alkamispäivä. |
    | Tilityskausi | Valitse tilityskausi. |
    | Arvonlisäveron maksuversio | <p>Valitse jokin seuraavista:</p><ul><li>**Alkuperäinen** – Luo raportti alkuperäisen arvonlisäveromaksun arvonlisäverotapahtumista tai ennen arvonlisäveromaksun muodostamista.</li><li>**Oikaisut** – Luo raportti kaikkien seuraavien arvonlisäveromaksujen arvonlisäverotapahtumista kaudella.</li><li>**Koko luettelo** – Luo raportti kaikista arvonlisäverotapahtumista kaudella, sisältäen alkuperäiset ja korjaukset.</li></ul> |

3. Valitse **OK** ja määritä seuraavat kentät avautuvassa valintaikkunassa.

    | Kenttä | Kuvaus |
    |---|---|
    | ALV-huojennus - myyntisumma | Määritä myynnin summa, joka oikeuttaa arvonlisäveron helpotukseen. |
    | ALV-huojennus - verosumma | Määritä veron summa, joka oikeuttaa arvonlisäveron helpotukseen. |
    | ALV-huojennus - syy | <p>**Huomautus:** Arvonlisäveron vapautusta voi pyytää vain tilivuoden lopulliselle verojaksolle, kalenterivuoden viimeiselle vuosineljänneksille ja ajanjaksolle, jolloin arvonlisäveron verovelvollisen velka on päättynyt.</p><p>Valitse syy, miksi ALV-vapautusta pyydetään:</p><ul><li>**1** – Tämä verokausi on tilivuoden lopullinen verokausi.</li><li>**2** – Tämä vuosineljännes on kalenterivuoden viimeinen neljännes.</li><li>**3** – ALV-vaatimus päätettiin tämän verokauden aikana.</li><li>**0** – Vapautusta ei ole pyydetty (oletusarvo).</li></ul> |
    | Käteiseen perustuvan ALV:n kirjanpito | Valitse täksi vaihtoehdoksi **Kyllä**, jos arvonlisäveroa tilitetään käteisenä. |
    | Korjauksen syyt | Valitse vähintään yksi korjauksen syy tarpeen mukaan. |
    | Yhteyshenkilö | Valitse yhteyshenkilö. |

4. Valitse **OK** ja tarkista Excel-raportti.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>ALV-ilmoituksen esikatselu Excelissä arvonlisäveromaksusta

Liikevaihtoveron maksutapahtuma tuotetaan [Selvitä ja kirjaa arvonlisävero](../general-ledger/tasks/create-sales-tax-payment.md) -työmenettelyllä, joka maksaa arvonlisäveron saldot liikevaihtoverotileillä ja kuittaa ne myyntiveron selvitystilille tietyltä ajanjaksolta. Kun **Selvitä ja kirjaa liikevaihtovero** -työprosessi on suoritettu myyntiveron selvitysjakson aikana, voit luoda arvonlisäveroilmoituksen Excelissä **Arvonlisäveron maksut** -sivulta.

1. Siirry kohtaan **Vero** \> **Kyselyt ja raportit** \> **Arvonlisäverokyselyt** \> **Arvonlisäveromaksut** ja valitse arvonlisäveron maksurivi.
2. Valitse ensin **Tulosta raportti** ja sitten **OK**.
3. Tarkista valitulle arvonlisäveron maksuriville luotu Excel-tiedosto.

    > [!NOTE]
    > Raportti luodaan vain valitulle arvonlisäveron maksuriville. Jos sinun tulee luoda esimerkiksi korjausilmoitus, joka sisältää kauden kaikki korjaukset, tai korvaavan ilmoituksen, joka sisältää alkuperäiset tiedot ja kaikki korjaukset, käytä kausittaista tehtävää [Ilmoita arvonlisävero tilityskaudelle](#report-sales-tax-for-settlement-period).

## <a name="generate-the-electronic-file-for-the-vat-declaration-from-electronic-messages"></a>Sähköisen tiedoston muodostaminen ALV-ilmoitusta varten sähköisistä sanomista

Kun muodostat raportin sähköisten viestien avulla, voit kerätä verotietoja useista yrityksistä. Lisätietoja on tässä ohjeaiheessa jäljempänä kohdassa [ALV-ilmoituksen suorittaminen useille yrityksille](#run-the-vat-declaration-for-multiple-legal-entities).

Seuraavat vaiheet koskevat sähköisen sanoman käsittelyesimerkkiä, jonka olet [tuonut aiemmin LCS:n jaetusta käyttöomaisuuskirjastosta](#import-em).

1. Valitse **Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköiset sanomat**.
2. Valitse vasemmasta ruudusta **FI – ALV-ilmoitus**.
3. Valitse **Sanomat**-pikavälilehdessä **Uusi**.
4. **Suorituksen käsittely** -valintaikkunassa **FI ALV -luontisanoma** -toiminto on määritetty valmiiksi. Valitse **OK**.
5. Valitse luotava sanomarivi, kirjoita kuvaus ja määritä sitten ilmoituksen alkamis- ja päättymispäivät.
6. Valitse **Sanomat**-pikavälilehdessä **Kerää tiedot** ja valitse sitten **OK**. Sanomaan lisätään arvonlisäveromaksut, jotka on luotu aiemmin [Arvonlisäveron tilityksen ja kirjaamisen](../general-ledger/tasks/create-sales-tax-payment.md) -työproseduurin takia.
7. Tarkista **Sanomanimikkeet**-pikavälilehdessä käsittelyyn siirretyt arvonlisäveromaksut. Oletusarvon mukaan kaikki valitun kauden arvonlisäveromaksut, jotka eivät sisälly saman käsittelyn muihin sanomaan, sisällytetään mukaan.
8. Valinnainen: Tarkista arvonlisäveromaksut valitsemalla **Alkuperäinen tiedosto**. Voit myös sulkea arvonlisäveromaksut pois käsittelystä valitsemalla **Poista**.
9. Valitse **Sanomat**-pikavälilehdessä **Päivitä tila**.
10. Valitse **Päivitä tila** -valintaikkunassa **FI ALV Valmis luotavaksi** ja valitse sitten **OK**.
11. Vahvista, että sanoman tilaksi tulee **FI ALV Valmis luomaan ALV-palautus**.
12. Valitse **Luo raportti**.
13. Voit esikatsella ALV-ilmoituksen summia valitsemalla **Suorita käsittely** -valintaikkunassa **FI ALV Esikatsele raporttia** ja valitsemalla sitten **OK**.
14. Aseta **Sähköisen raportoinnin parametrit** -valintaikkunassa kentät kuten on kuvattu osiossa [Esikatsele arvonlisäveroilmoitusta Excelissä Raportoi myyntivero tilikauden määräaikaistehtävästä](#report-sales-tax-for-settlement-period) aiemmin tähän aiheeseen ja valitse sitten **OK**.
15. Valitse sivun oikeasta yläkulmasta **Liitteet**-painike (paperiliitinsymboli) ja avaa tiedosto valitsemalla **Avaa**.
16. Tarkista Excel-tiedoston summat ja valitse sitten **Luo raportti**.
17. Voit luoda ALV-ilmoituksen TXT-muodossa valitsemalla **Suorita käsittely** -valintaikkunassa **FI ALV Luo raportti** ja valitsemalla sitten **OK**.
18. Aseta **Sähköisen raportoinnin parametrit** -valintaikkunassa kentät kuten on kuvattu osiossa [Esikatsele arvonlisäveroilmoitusta Excelissä Raportoi myyntivero tilikauden määräaikaistehtävästä](#report-sales-tax-for-settlement-period) ja valitse sitten **OK**.
19. Valitse sivun oikeasta yläkulmasta **Liitteet**-painike (paperiliitinsymboli), lataa tiedosto ja käytä sitä lähetyksessä veroviranomaiselle.

## <a name="run-the-vat-declaration-for-multiple-legal-entities"></a>ALV-ilmoituksen suorittaminen useille yrityksille

Jos haluat käyttää muotoja yritysryhmän ALV-ilmoituksen raportoimiseen, sinun on ensin määritettävä kaikkien tarvittavien yritysten ER-muotojen sovelluskohtaiset parametrit arvonlisäverokoodeille.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Sähköisten viestien tietojen kerääminen usealta yritykseltä

Noudattamalla näitä ohjeita voit määrittää sähköiset sanomat, jotka keräävät tietoja useilta yrityksiltä.

1. Valitse **Työtilat** \> **Ominaisuuden hallinta**.
2. Etsi ja valitse **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -toiminto luettelosta ja sitten **Ota käyttöön nyt**.
3. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Tietueiden täyttötoiminnot**.
4. Valitse **Tietueiden täyttötoiminto** -sivulla rivi, jossa on **FI – Täytä ALV-palautustietueet**.

    Uusi **Yritys**-kenttä on käytettävissä **Tietolähteiden asetukset** -ruudukossa. Tässä kentässä näkyy aiemmin luotujen tietueiden tapauksessa nykyisen yrityksen tunnus.

5. Lisää **Tietolähteiden asetukset** -ruudukkoon rivi kutakin raportointiin sisällytettävää lisäyritystä varten. Määritä kullekin uudelle riville seuraavat kentät.

    | Kenttä | Kuvaus |
    |---|---|
    | Nimi | Kirjoita arvo, joka auttaa ymmärtämään, mistä tämä tietue tulee. Syötä esimerkiksi **Tytäryhtiön 1 ALV-maksu**. |
    | Sanoman nimiketyyppi | Valitse **ALV-palautus**. Tämä arvo on ainoa arvo, joka on käytettävissä kaikille tietueille. |
    | Tilityyppi | Valitse **Kaikki**. |
    | Päätaulun nimi | Määritä kaikille tietueille **TaxReportVoucher**. |
    | Asiakirjan numerokenttä | Määritä kaikille tietueille **Voucher**. |
    | Asiakirjan päivämääräkenttä | Määritä kaikille tietueille **TransDate**. |
    | Asiakirjan tilikenttä | Määritä kaikille tietueille **TaxPeriod**. |
    | Yritys | Valitse yrityksen tunnus. |
    | Käyttäjän kysely | Tämä valintaruutu valitaan automaattisesti, kun määrität ehtoja valitsemalla **Muokkaa kyselyä**. |

6. Valitse kullekin uudelle riville **Muokkaa kyselyä** ja määritä liittyvä tilityskausi rivin **Yritys**-kentässä määritetylle yritykselle.

    Kun määritys on valmis, **Sähköiset sanomat** -sivun **Kerää tiedot** -toiminto kerää arvonlisäveromaksut kaikilta määritetyiltä yrityksiltä.
