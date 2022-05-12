---
title: Kaupan kirjanpidon integroinnin määrittäminen
description: Tässä ohjeaiheessa on ohjeet Commerce-kanavien kirjanpidon integrointitoiminnon määrittämiseen.
author: EvgenyPopovMBS
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 51a75ce03b0ae6b744ec56df35bd3fdb1f40cf3a
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661746"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Kaupan kirjanpidon integroinnin määrittäminen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa on ohjeet Commerce-kanavien kirjanpidon integrointitoiminnon määrittämiseen. Lisätietoja kirjanpidon integroinnista on kohdassa [Commerce-kanavan kirjanpidon integroinnin yleiskatsaus](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Ominaisuuksien ottaminen käyttöön Commerce headquarters -sovelluksessa

Ota Commerce-kanavien kirjanpidon integrointitoimintoon liittyvät toiminnot käyttöön seuraavasti.

1. Valitse Commerce-pääkonttorissa **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Etsi ja ota käyttöön seuraavat toiminnot:

    - **Kassakoneiden suora verotuksen integrointi** – Tämä ominaisuus laajentaa verojen integroinnin kehystä lisäämällä mahdollisuuden luoda myyntipisteessä suoritettavia veroliittimiä. Tämäntyyppinen liitin kommunikoi verolaitteen tai -palvelun kanssa, joka tarjoaa HTTP-sovellusohjelmaliittymän (API) eikä vaadi myymälässä erillistä fyysistä laitetta. Tämä ominaisuus mahdollistaa esimerkiksi verojen integroinnin matkapuhelimista vaatimatta jaettua laitteistoasemaa.
    - **Verointegraation tekniset profiili-ohitukset** – Tämän ominaisuuden avulla voidaan laajentaa verojen integroinnin asetuksia ja mahdollistaa kassapäätteiden asetussivun yhteysparametrien tarkistamisen. Kun tämä ominaisuus on käytössä, voit ohittaa teknisen profiilin parametrit.
    - **Kassakoiden verorekisteröinnin tila** – Kun tämä ominaisuus on käytössä, voit poistaa verojen rekisteröintiprosessin käytöstä tietyistä kassakoneista. Jos kassakoneen verorekisteröinti on poistettu käytöstä, myyntitapahtumia ei voi suorittaa siinä kassapäätteessä.
    - **Verointegraation paikallinen tallennusvarmuuskopiointi** – Tämä ominaisuus laajentaa verointegraatiokehyksen virheenkäsittelyominaisuuksia. Se myös mahdollistaa verorekisteröintitietojen automaattisen varmuuskopioinnin tietojen menettämisen yhteydessä, jotta paikallisen tallennuksen tiedot palautetaan, kun laite aktivoidaan.

## <a name="set-up-commerce-parameters"></a>Määritä Commercen parametrit

Voit määrittää Commerce-parametreja noudattamalla seuraavia ohjeita.

1. Valitse **Commercen yhteiset parametrit** -sivun **Yleiset**-välilehden **Ota kirjanpidon integrointi käyttöön** -asetukseksi **Kyllä**.
1. Määritä seuraavien viitteiden numerosarjat **Numerosarjat**-välilehdessä:

    - Kirjanpidon teknisen profiilin numero
    - Kirjanpidon yhdistinryhmän numero
    - Rekisteröintiprosessin numero

1. Määritä kirjanpidon toimintaprofiilinumeron numerosarja **Commercen parametrit** -sivulla.

> [!NOTE]
> Numerosarjat ovat valinnaisia. Kaikki kirjanpidon integrointiyksiköt voidaan luoda joko numerosarjoista tai manuaalisesti.

## <a name="set-up-a-fiscal-registration-process"></a>Kirjanpidon rekisteröintiprosessin määrittäminen

Kirjanpidon integroinnin määritysprosessi sisältää seuraavat tehtävät:

- Määritä ne kirjanpidon yhdistimet, jotka edustavat kirjanpidon rekisteröinnissä käytettäviä kirjanpidon laitteita tai palveluja, kuten kuittitulostimia.
- Määritä tiedostopalvelut, jotka muodostavat kirjanpidon yhdistimien kirjanpidon laitteissa tai palveluissa rekisteröitävät kirjanpitoasiakirjat.
- Määritä kirjanpidon rekisteröintiprosessi, joka määrittää kirjanpidon rekisteröintivaiheiden järjestyksen sekä kussakin vaiheessa käytettävät kirjanpidon yhdistimet ja kirjanpitoasiakirjojen toimittajat.
- Määritä kirjanpidon rekisteröintiprosessi myyntipisteen toimintoprofiileihin.
- Määritä yhdistimen tekniset profiilit laiteprofiileihin.
- Määritä yhdistimen tekniset profiilit myyntipisteen laiteprofiileihin tai toimintoprofiileihin.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Lataa kirjanpitoasiakirjan toimittajien määritykset palvelimeen

Kirjanpitoasiakirjan toimittaja vastaa niiden kirjanpitoasiakirjojen luomisesta, jotka vastaavat myyntipisteessä rekisteröityjä transaktioita ja -tapahtumia. Rekisteröinnissä käytetään samaa muotoa, jota käytetään myös kirjanpidon laitetta tai palvelua käytettäessä. Kirjanpitoasiakirjan toimittaja voi esimerkiksi luoda verokuitin XML-muodossa.

Lataa kirjanpitoasiakirjan toimittajien määritykset seuraavasti.

1. Siirry Commerce headquartersissa **Kirjanpitoasiakirjan toimittajat** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**).
1. Lataa palvelimeen kunkin käyttöön otettavan laitteen tai palvelun XML-konfiguraatio.

> [!TIP]
> Valitsemalla **Näytä** voit tarkastella kaikkia nykyiseen kirjanpitoasiakirjan toimittajaan liittyviä toimintaprofiileja.

> [!NOTE]
> Tietojen yhdistämisen katsotaan olevan osa kirjainpitoasiakirjan toimittajaa. Jos haluat määrittää samalle yhdistimelle erilaisia tietojen yhdistämisiä (kuten osavaltiokohtaisia säädöksiä), sinun on luotava erillisiä kirjainpitoasiakirjan toimittajia.

### <a name="upload-configurations-of-fiscal-connectors"></a>Veroliittimien konfiguraatioiden lataaminen palvelimeen

Kirjanpidon yhdistin vastaa kirjanpidon laitteen tai palvelun kanssa tapahtuvasta tietoliikenteestä. Kirjanpidon yhdistin voi esimerkiksi lähettää kirjanpitoasiakirjan toimittajan XML-muodossa luoman verokuitin kuittitulostimeen. Lisätietoja kirjanpidon integroinnin osista on kohdassa [Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden ja palveluiden kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Lataa kirjanpitoyhdistimien määritykset seuraavasti.

1. Siirry Commerce headquartersissa **Kirjanpitoyhdistimet** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoyhdistimet**).
1. Lataa palvelimeen kunkin kirjanpidon integroinnissa käyttöön otettavan laitteen tai palvelun XML-konfiguraatio.

> [!TIP]
> Valitsemalla **Näytä** voit tarkastella kaikkia nykyisiin kirjanpidon yhdistimeen liittyviä toimintaprofiileja ja teknisiä profiileja.

Esimerkkejä kirjanpidon yhdistimien ja kirjanpitoasiakirjojen toimittajien määrityksistä on kohdassa [Commerce SDK:n kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Luo yhdistimen toimintoprofiilit

Luo yhdistimen toimintoprofiili seuraavien ohjeiden avulla.

1. Siirry Commerce headquartersissa **Yhdistimen toiminnalliset profiilit** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**).
1. Luo kullekin kirjanpidon yhdistimeen liittyvän kirjanpidon yhdistimen ja kirjanpitoasiakirjan toimittajan yhdistelmälle yhdistimen toiminnallinen profiili seuraavasti:

    1. Valitse yhdistimen nimi.
    1. Valitse asiakirjan toimittaja.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Muuta tietojen yhdistämisparametreja yhdistimen toiminnallisessa profiilissa

Voit muuttaa tietojen yhdistämisparametreja yhdistimen toiminnallisessa profiilissa. Seuraavassa taulukossa on joitakin esimerkkejä liittimen toimintoprofiilin tietomääritysparametreista.

| Parametri | Muoto | Esimerkki |
|-----------|--------|---------|
| ALV-prosenttiasetukset | arvo: VATrate | 1 : 2000, 2 : 1800 |
| ALV-koodien yhdistäminen | VATcode : arvo | vat20 : 1, vat18 : 2 |
| Maksuvälinetyyppien yhdistäminen | TenderType : arvo | Käteinen : 1, Kortti : 2 |

Voit palauttaa kirjanpitoasiakirjan toimittajan määrityksessä määritetyt oletusparametrit valitsemalla **Päivitys** **Yhdistimen toiminnalliset profiilit** -sivulla.

> [!NOTE]
> Yhdistimen toiminnalliset profiilit ovat yrityskohtaisia. Jos aiot käyttää samaa kirjanpidon yhdistimen ja kirjanpitoasiakirjan toimittajan yhdistelmää eri yrityksissä, kullekin yritykselle on luotava yhdistimen toiminnallinen profiili.

### <a name="create-connector-technical-profiles"></a>Luo yhdistimen tekniset profiilit

Luo yhdistimen tekniset profiilit seuraavien ohjeiden avulla.

1. Siirry Commerce headquartersissa **Yhdistimen tekniset profiilit** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen tekniset profiilit**).
1. Luo liittimen tekniset profiilit kullekin veroliittimelle seuraavasti:

    1. Valitse yhdistimen nimi.
    1. Valitse yhdistimen tyyppi:

        - Valitse **Paikallinen** laitteille tai palveluille, jotka on yhdistetty Hardware stationin tai jotka ovat paikallisessa verkossa.
        - Valitse ulkoisia palveluita varten **Ulkoinen**.
        - Valitse Commerce runtimen (CRT) sisäisille liittimien **Sisäinen**. 

    1. Valitse yhdistimen sijainti:

        - Jos liitin sijaitsee Hardware stationissa, valitse **Hardware station**.
        - Jos liitin sijaitsee kassapäätteessä, valitse **Kassa**.

Yhdistimen teknisen profiilin **Laite**- ja **Asetukset**-välilehtien parametreja voi muuttaa. Voit palauttaa kirjanpidon yhdistimen määrityksessä määritetyt oletusparametrit valitsemalla **Päivitys**. Kun XML-määrityksen uutta versiota ladataan, saat ilmoituksen, jonka mukaan nykyistä kirjanpidon yhdistintä tai kirjanpitoasiakirjan toimittaja on jo käytössä. Tämä menettely ei ohita yhdistimen toiminnallisiin tai teknisiin profiileihin aiemmin tehtyjä manuaalisia muutoksia. Voit käyttää uuden määrityksen oletusparametrijoukkoa valitsemalla **Päivitä** **Yhdistimen toiminnalliset profiilit**- tai **Yhdistimen tekniset profiilit** -sivulla.

Jos sinun on määritettävä yksittäiselle kassapäätteelle tai myymälälle tietyt parametrit, noudata seuraavia ohjeita.

1. Valitse **Ohita**-valikkovaihtoehto.
1. Luo **Ohita**-sivulla uusi tietue.
1. Valitse myymälä tai kassapääte. Voit ohittaa yksittäisen kassapäätteen tai kaikkien yksittäisen myymälän kassapäätteiden valitun teknisen profiilin parametrit.
1. Lisää valitun kassan tai myymälän parametrit **Laite**-välilehdessä.

### <a name="create-fiscal-connector-groups"></a>Luo kirjanpidon yhdistinryhmät

Kirjanpidon yhdistinryhmä yhdistää ne kirjanpidon yhdistimien toiminnalliset profiilit, jotka suorittavat samoja toimintoja ja joita käytetään samassa kirjanpidon rekisteröintiprosessin vaiheessa. Jos esimerkiksi myymälässä käytetään useita kuittitulostinmalleja, kyseisten kuittitulostimien kirjanpidon yhdistimet voidaan yhdistää kirjanpidon yhdistinryhmäksi.

Luo kirjanpidon yhdistinryhmä noudattamalla seuraavia ohjeita.

1. Siirry **Kirjanpidon yhdistinryhmä** -sivulle (**Vähittäismyynti ja kauppa \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmä**).
1. Luo uusi kirjanpidon yhdistinryhmä.
1. Lisää toiminnalliset profiilit yhdistinryhmään. Valitse ensin **Toiminnalliset profiilit** -sivulla **Lisää** ja valitse sitten profiilin numero. Kullakin yhdistinryhmän kirjanpidon yhdistimellä voi olla vain yksi toiminnallinen profiili.
1. Voit keskeyttää toiminnallisen profiilin käytön valitsemalla **Poista käytöstä** -asetukseksi **Kyllä**. Muutos koskee vain nykyistä yhdistinryhmää. Voit jatkaa saman toiminnallisen profiilin käyttöä muissa yhdistinryhmissä.

### <a name="create-a-fiscal-registration-process"></a>Luo kirjanpidon rekisteröintiprosessi

Rekisteröintivaiheiden järjestys ja kussakin vaiheessa käytetty yhdistinryhmä määrittävät kirjanpidon rekisteröintiprosessin.

Luo kirjanpidon rekisteröintiprosessi noudattamalla seuraavia ohjeita.

1. Siirry Commerce headquartersissa **Kirjanpidon rekisteröintiprosessi** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**).
1. Luo uusi tietue kutakin yksilöivää verorekisteröintiprosessia varten.
1. Lisää prosessiin rekisteröintivaiheet seuraavasti:

    1. Valitse **Lisää**.
    1. Valitse kirjanpidon yhdistimen tyyppi.
    1. Valitse sopiva kirjanpidon yhdistinryhmä **Ryhmän numero** -kentässä.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Määritä kirjanpidon rekisteröintiprosessiyksiköt myyntipisteen profiileihin

Määritä kirjanpidon rekisteröintiprosessiyksiköt myyntipisteen profiileihin seuraavasti.

1. Siirry Commerce headquartersissa **POS-toimintoprofiili** -sivulle (**Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**). 
1. Määritä kirjanpidon rekisteröintiprosessi myyntipisteen toimintoprofiiliin.
1. Valitse ensin **Muokkaa** ja sitten prosessi **Kirjanpidon rekisteröintiprosessi** -välilehden **Prosessin numero** -kentässä.
1. Valitse **Veropalvelut**-välilehdestä liittimen tekniset profiilit, jossa liittimen sijainti on **Kassakone**.
1. Siirry **Myyntipisteen laitteistoprofiili** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipisteen profiilit \> Laiteprofiilit**).
1. Määritä yhdistimen tekniset profiilit laiteprofiiliin. 
1. Valitse **Muokkaa** ja lisää sitten rivi **Kirjanpidon oheislaitteet** -välilehdessä. 
1. Valitse yhdistimen tekninen profiili **Profiilin numero** -kentässä.
1. Valitse **Kirjanpidon oheislaitteet**-välilehdestä liittimen tekniset profiilit, jossa liittimen sijainti on **Hardware station**.

> [!NOTE]
> Voit lisätä useita teknisiä profiileja samaan laiteprofiiliin. Laiteprofiilia tai myyntipisteen toimintoprofiilia voi kuitenkin käyttää vain kerran samassa kirjanpidon yhdistinryhmässä.

Kirjanpidon rekisteröinnin työnkulun määrittää kirjanpidon rekisteröintiprosessi sekä tietyt kirjanpidon integrointiosien osat: kirjanpitoasiakirjan toimittajan CRT-laajennus ja kirjanpidon yhdistimen Hardware station -laajennus.

- Kirjanpidon rekisteröinnin tapahtumien ja transaktioiden tilaus määritetään valmiiksi kirjanpitoasiakirjan toimittajassa.
- Kirjanpitoasiakirjan toimittaja vastaa myös kirjanpidon rekisteröinnissä käytettävän kirjanpidon yhdistimen tunnistamisesta. Se yhdistää siihen kirjanpidon yhdistinryhmään sisältyvät yhdistimen toiminnalliset profiilit, joka on määritetty kirjanpidon rekisteröintiprosessin nykyiselle vaiheelle, siihen yhdistimen tekniseen profiilin, joka on määritetty myyntipisteeseen pariliitoksen muodostaneen laiteaseman laiteprofiiliin.
- Kirjanpitoasiakirjan toimittaja käyttää kirjanpitoasiakirjan toimittajan määrityksen tietojen yhdistämisasetuksia transaktio- tai tapahtumatietojen, kuten verojen ja maksujen, muuntamiseen kirjanpitoasiakirjaa luotaessa.
- Kun kirjanpitoasiakirjan toimittaja luo kirjanpitoasiakirjan, kirjanpidon yhdistin voi joko lähettää sen sellaisenaan kirjanpidon laitteeseen tai muuntaa sen sarjaksi laitteen API-komentoja. Valittu vaihtoehto perustuu siihen, miten tietoliikennettä käsitellään.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Kassakoneiden määrittäminen kirjanpidon rekisteröintirajoitusten mukaan

Voit valita kassakoneita, joissa verorekisteröinti on kielletty esimerkiksi silloin, kun sinun on toimitettava vain muita kuin verotoimintoja, kuten tuoteluettelohaku, asiakashaku tai tapahtumien luonnoksen luominen näillä laitteilla.

Kassakoneiden määrittämisen kirjanpidon rekisteröintirajoitusten mukaan voit tehdä seuraavasti.

1. Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**.
1. Valitse haluttu prosessi.
1. Valitse **Myyntipisteen kassakoneet ja kirjanpitoprosessin rajoitukset** -välilehti.
1. Lisää tarpeen mukaan kassakoneita, joissa ja kirjanpitoprosessin rajoitukset.

### <a name="validate-the-fiscal-registration-process"></a>Verorekisteröintiprosessin tarkistaminen

On suositeltavaa tarkistaa verorekisteröintiprosessi seuraavissa tapauksissa:

- Olet suorittanut kaikki uuden rekisteröintiprosessin asetukset. Näitä asetuksia ovat rekisteröintiprosessien määrittäminen POS-toimintoprofiileihin ja laiteprofiileihin.
- Olet tehnyt muutoksia aiemmin luotuun verorekisteröintiprosessiin, ja muutokset voivat aiheuttaa sen, että suorituksen aikana valitaan eri veroliitin. (Olet esimerkiksi muuttanut verorekisteröintiprosessin vaiheen liitinryhmää, ottanut liittimen toimintaprofiilin käyttöön liitinryhmässä tai lisännyt uuden liittimen toimintaprofiilin liitinryhmään.)
- Yhdistimen teknisten profiilien laiteprofiileihin määrittämisessä tehtyjen muutosten jälkeen.

Tarkista kirjanpidon rekisteröintiprosessi noudattamalla seuraavia ohjeita.

1. Siirry Commerce headquartersissa **Kirjanpidon rekisteröintiprosessi** -sivulle (**Retail ja Commerce \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**).
1. Valitse **Tarkista** kun haluat tarkistaa kirjanpidon rekisteröintiprosessin.
1. Siirrä tiedot kanavatietokantaan suorittamalla **Jakeluaikataulu** -sivulla **1070**- ja **1090**-työt.

## <a name="set-up-fiscal-texts-for-discounts"></a>Alennusten kirjanpitotekstien määrittäminen

Alennusta käytettäessä verokuittiin on joissakin tapauksissa tulostettava erityinen teksti. Voit määrittää alennusten kirjanpitotekstit **Kirjanpidon yhdistinryhmä** -sivulla (**Vähittäismyynti ja kauppa \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmä**).

- Jos kyse on manuaalisesti myyntipisteessä lisättävistä alennuksista, tietokoodin tai tietokoodiryhmän kirjanpitoteksti on määritettävä. Tämä tietokoodi määritetään myyntipisteen toimintaprofiilissa **Tuotealennus**-tietokoodina.

    1. Valitse **Kirjanpidon yhdistinryhmä** -sivulla **Verokuitin teksti**.
    1. Valitse **Tietokoodit**-välilehdessä ensin **Lisää** ja sitten tietokoodi tai tietokoodiryhmä.
    1. Valitse arvo **Tietokoodin numero** -kentässä.
    1. Valitse **Alikoodin numero** -kentässä arvo, jos valittu tietokoodi edellyttää alikoodia.
    1. Määritä **Verokuitin teksti** -kentässä verokuittiin tulostettava kirjanpitoteksti.
    1. Valitse **Tulosta käyttäjän syöte verokuittiin** -asetukseksi **Kyllä**, jolloin verokuitin teksti korvataan käyttäjän myyntipisteessä manuaalisesti antamilla tiedoilla. Tämä asetus koskee vain tietokoodeja, joiden syötetyyppi on **Teksti**.

    > [!NOTE]
    > Voit määrittää kirjanpitotekstin useisiin tietokoodeihin sellaisia skenaarioita varten, joissa käytetään tietokoodiryhmiä. linkitettyjä tietokoodeja ja käynnistettyjä tietokoodeja. Näissä skenaarioissa verokuitissa on kirjanpitotekstiä kaikista siihen tapahtumariviin linkitetyistä tietokoodeista, jossa alennusta käytettiin.

- Kanavakohtaisissa alennuksissa alennustunnukselle on määritettävä kirjanpitoteksti.

    1. Valitse **Kirjanpidon yhdistinryhmä** -sivulla **Verokuitin teksti**.
    1. Valitse **Alennukset**-välilehdessä ensin **Lisää** ja sitten alennustunnus.
    1. Määritä **Verokuitin teksti** -kentässä verokuittiin tulostettava kirjanpitoteksti.

    > [!NOTE]
    > Jos samalle tapahtumariville käytetään useita alennuksia, verokuitissa on kirjanpitotekstiä kaikista kyseiseen tapahtumariviin linkitetyistä alennuksista.

## <a name="set-error-handling-settings"></a>Virheen käsittelyasetusten määrittäminen

Kirjanpidon integroinnissa käytettävissä olevat virheen käsittelyasetukset määritetään kirjanpidon rekisteröintiprosessissa. Lisätietoja virheen käsittelystä kirjanpidon integroinnissa on kohdassa [Virheen käsittely](fiscal-integration-for-retail-channel.md#error-handling).

Voit määrittää virheiden käsittelyasetukset noudattamalla seuraavia vaiheita.

1. Voit määrittää seuraavat parametrit kirjanpidon rekisteröinnin kullekin vaiheelle **Kirjanpidon rekisteröintiprosessi** -sivulla (**Vähittäismyynti ja kauppa \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessi**):

    - **Salli ohitus** – tämä parametri ottaa **Ohita**-asetuksen käyttöön virheen käsittelyn valintaikkunassa.
    - **Salli rekisteröidyksi merkitseminen** – tämä parametri ottaa **Merkitse rekisteröidyksi** -asetuksen käyttöön virheen käsittelyn valintaikkunassa.
    - **Salli viivytys** – tämä parametri ottaa **Viivytä**-asetuksen käyttöön virheen käsittelyn valintaikkunassa.
    - **Jatka virheen ilmetessä** – Jos tämä parametri on käytössä, kirjanpidon rekisteröintiprosessi voi jatkua POS-rekisterissä, jos transaktion tai tapahtuman tilikausirekisteröinti epäonnistuu. Muussa tapauksessa operaattorin on suoritettava epäonnistunut tilikausirekisteröinti uudelleen, ohitettava se tai merkittävä transaktio tai tapahtuma rekisteröidyksi, jos haluaa suorittaa seuraavan transaktion tai tapahtuman tilikausirekisteröinnin. Lisätietoja on kohdassa [valinnainen tilikausirekisteröinti](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Jos **Jatka virheen ilmetessä** -parametri on käytössä, **Salli Ohita**- ja **Salli Merkitse rekisteröidyksi** -parametrit ovat automaattisesti poissa käytöstä.

1. Virheen käsittelyn valintaikkunan **Ohita**- ja **Merkitse rekisteröidyksi** -asetukset edellyttävät **Salli rekisteröinnin ohitus tai rekisteröidyksi merkitseminen** -käyttöoikeuden käyttöönoton. Ota käyttöoikeus käyttöön määrittämällä **Salli ohita rekisteröinti tai rekisteröidyksi merkitseminen** -asetukseksi **Kyllä** **Käyttöoikeusryhmät** -sivulla (**Vähittäismyynti ja kauppa \> Työntekijät \> Käyttöoikeusryhmät**).
1. **Salli viivytys** -parametri pitää olla käytössä, jotta **Viivytä**-asetus voidaan ottaa käyttöön virheen käsittelyn valintaikkunassa. Ota käyttöoikeus käyttöön määrittämällä **Salli viivytys** -asetukseksi **Kyllä** **Käyttöoikeusryhmät** -sivulla (**Vähittäismyynti ja kauppa \> Työntekijät \> Käyttöoikeusryhmät**).
1. Käyttäjät voivat antaa **Ohita**-, **Merkitse rekisteröidyksi**- ja **Viivytä**-asetuksilla lisätietoja siitä, milloin kirjanpidon rekisteröinti epäonnistuu. Voit ottaa tämän toiminnon käyttöön määrittämällä **Ohita**-, **Merkitse rekisteröidyksi**- ja **Viivytä**-tietokoodit kirjanpidon yhdistinryhmässä. Käyttäjien antamat tiedot tallennetaan sitten kirjanpitotapahtumaan linkitettyjä tietokooditapahtumana. Lisätietoja tietokoodeista on kohdassa [Tietokoodit ja tietokoodiryhmät](../info-codes-retail.md).

    > [!NOTE]
    > **Tuotteen** käynnistintoimintoa ei tueta tietokoodeissa, joita käytetään **Ohita**- ja **Merkitse rekisteröidyksi** -asetuksina kirjanpidon yhdistinryhmissä.

    - Valitse **Kirjanpidon yhdistinryhmä** -sivun **Tietokoodit**-välilehdessä tietokoodit tai tietokoodiryhmät **Ohita**-, **Merkitse rekisteröidyksi**-ja **Viivytä** -kentissä.

    > [!NOTE]
    > Kirjanpidon rekisteröintiprosessin missä tahansa vaiheessa voidaan luoda yksi kirjanpitoasiakirja ja yksi muu kuin kirjanpitoasiakirja. Kirjanpitoasiakirjan toimittajalaajennus tunnistaa jokaisen transaktio- tai tapahtumatyypin kirjanpitoasiakirjaan tai muuhun kuin kirjanpitoasiakirjaan liittyväksi. Virheen käsittelytoiminto koskee vain kirjanpitoasiakirjoja.
    >
    > - **Kirjanpitoasiakirja** – pakollinen asiakirja, jonka rekisteröitymisen on onnistuttava (esimerkiksi verokuitti).
    > - **Muu kuin kirjanpitoasiakirja** – transaktion tai tapahtuman täydentävä asiakirja (esimerkiksi lahjakortti).

1. Jos operaattorin on voitava jatkaa nykyisen toiminnan käsittelyä (esimerkiksi tapahtuman luominen tai viimeistely) kuntotarkastuksen virheen jälkeen, sen on otettava käyttöön **Salli kuntotarkistuksen virheen ohitus** -käyttöoikeudet **Käyttöoikeusryhmät** -sivulla (**Vähittäismyynti ja kauppa \> työntekijät \> käyttöoikeusryhmät**). Saat lisätietoja kuntotarkastusmenettelystä kohdasta [Tilikausirekisteröinnin kuntotarkastus](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Kirjanpidon X/Z-raporttien määrittäminen myyntipisteessä

Kirjanpidon X/Z-raporttien suorittaminen myyntipisteestä edellyttää, että myyntipisteen asetteluun lisätään uusia painikkeita.

- Asenna suunnitteluohjelma ja päivitä myyntipisteen asettelu **Painikeruudukot**-sivulla noudattamalla kohdan [Myyntipistetoimintojen lisääminen myyntipisteasetteluihin käyttämällä painikeruudukon suunnittelutoimintoa](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) ohjeita.

    1. Valitse päivitettävä asettelu. 
    1. Lisää uusi painike, määritä **Tulosta kuitti X** -painikeominaisuus.
    1. Lisää uusi painike ja määritä **Tulosta kuitti Z** -painikeominaisuus.
    1. Siirrä muutokset kanavatietokantaan suorittamalla työ **1090** **Ajastuksen jakelu** -sivulla.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö

Jos haluat ottaa käyttöön lykätyn tilikausirekisteröinnin manuaalisen käytön, lisää uusi painike POS-asetteluun.

- Asenna suunnitteluohjelma ja päivitä myyntipisteen asettelu **Painikeruudukot**-sivulla noudattamalla kohdan [Myyntipistetoimintojen lisääminen myyntipisteasetteluihin käyttämällä painikeruudukon suunnittelutoimintoa](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) ohjeita.

    1. Valitse päivitettävä asettelu.
    1. Lisää uusi painike, määritä **Viimeistele tilikausirekisteröintiprosessi** -painikeominaisuus.
    1. Siirrä tekemäsi muutokset kanavatietokantaan suorittamalla työ **1090** **Ajastuksen jakelu** -sivulla.


## <a name="view-connection-parameters-and-other-information-in-pos"></a>Yhteysparametrien ja muiden tietojen tarkasteleminen myyntipisteessä

Yhteysparametrien ja muiden tietojen tarkasteleminen myyntipisteessä tapahtuu seuraavasti.

1. Avaa Modern POS (MPOS) tai Cloud POS (CPOS).
1. Valitse **Asetukset**. Jos kirjanpidon integrointi on otettu käyttöön, oikealla olevassa **Verotuksen integrointi** -osassa näkyvät seuraavat tiedot:

    - Verorekisteröinnin tila
    - Viimeisimmän verotapahtuman tila
    - Odottavien seurantatapahtumien määrä

1. Voit näyttää seuraavat tiedot valitsemalla **Tiedot**:

    - Rekisteröintiprosessin vaiheet
    - Yhteysparametrit
    - Tarkistustapahtumien tiedot
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
