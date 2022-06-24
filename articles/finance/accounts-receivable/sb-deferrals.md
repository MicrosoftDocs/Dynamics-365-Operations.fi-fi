---
title: Tuottojen ja kulujen lykkäykset tilauslaskutuksen aikana
description: Tässä artikkelissa kerrotaan, miten tuoton ja kulujen lykkäys määritetään tilauslaskutuksessa.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 209afd08c0c7e3cbd63ed95613b1d1dec94856f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908093"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Tuottojen ja kulujen lykkäykset tilauslaskutuksen aikana

Tässä artikkelissa kerrotaan, miten tuoton ja kulujen lykkäys määritetään ja miten sitä käytetään tilauslaskutuksessa. Lykkäysaikataulut perustuvat aina pohjana olevaan alkuasiakirjaan tai laskutusaikatauluun. Koska ne luodaan oletusarvojen perusteella, niitä ei voi syöttää eikä luoda erikseen.

Tuottojen ja kulujen lykkäysten määrittäminen ja käyttäminen tapahtuu useilla sivuilla:

- Voit määrittää yrityksen asetukset **Tuoton ja kulujen lykkäysparametrit** -sivulla.
- Voit määrittää **Lykkäyksen oletusarvot** -sivulla lykkäysaikatauluissa käytettävät oletustilit ja -mallit.
- Voit määrittää lykkäysmalleissa käytettävät mallit **Lykkäysmallit** ja **Tapahtumapohjaiset lykkäysmallit** -sivuilla.
- **Kaikki lykkäysaikataulut** -sivulla voit tarkastella ja muokata mitä tahansa lykkäysaikataulua.

Tuottojen ja kulujen lykkäyksiä voidaan käyttää yhdessä toistuvan sopimuksen laskutuksen kanssa.

## <a name="revenue-and-expense-deferral-parameters"></a>Tuoton ja kulujen lykkäysparametrit

**Tuoton ja kulujen lykkäysparametrit** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|---|---| 
| **Aikataulu**-välilehti | |
| Yhtä suuri joka kaudelle | <p>Määritä, käytetäänkö kauden päivien määrää, kun kausikohtainen summa lasketaan lykkäystä varten:</p><ul><li>**Kyllä** – Kunkin kauden summa on sama kauden päivien määrästä riippumatta. Osajaksot (kuten kaudet lykkäysaikataulun alussa tai lopussa) jakavat ne.</li><li>**Ei** – Tämä summa lasketaan kunkin kauden päivien määrän perusteella.</li></ul><p>Voit ohittaa tämän asetuksen tapahtumatasolla.</p> |
| Myyntialennuksen lykkäysasetus | <p>Määritä, luodaanko alennus- ja myyntitilaussummia varten erilliset lykkäyssuunnitelmat:</p><ul><li>**Erillinen alennussuunnitelma** – Alennuksen summa pidetään erillään tuoton summasta.<p>Tällöin luodaan myyntitilauksen luomisen ja kirjaamisen yhteydessä kaksi lykkäysaikataulua. Alennus- ja tuottosummat kirjataan eri lykkäystileille.</p></li><li>**Yhdistä alennus tuottoon** – Alennuksen summa yhdistetään tuoton summaan. Luodaan yksi lykkäyssuunnitelma, ja sekä alennuksen summa että tuoton summa kirjataan samalle lykkäystilille.<p>Tällöin luodaan myyntitilauksen luomisen ja kirjaamisen yhteydessä yksi lykkäysaikataulu. Sekä alennuksen summa että tuoton summa kirjataan samalle lykkäystilille.</p></li></ul><p>**Huomautus:** Voit kohdistaa alennuksia nimikkeisiin, jotka käyttävät laskuttamatonta tuottoa, valitsemalla **erilliset alennusaikataulut**. Tämän jälkeen alennuksia voidaan käyttää kaikissa nimikkeissä riippumatta siitä, käytetäänkö laskuttamatonta tuottoa. Jos **yhdistä alennus tuottoon** -vaihtoehto on valittuna, alennuksia ei voi käyttää nimikkeisiin, jotka käyttävät laskuttamatonta tuottoa.</p> |
| Oston alennuksen lykkäysasetus | <p>Valitse, luodaanko alennus- ja ostotilaussummia varten erilliset lykkäyssuunnitelmat:</p><ul><li>**Erillinen alennussuunnitelma** – Alennuksen summa pidetään erillään kulun summasta.<p>Tällöin luodaan ostotilauksen luomisen ja kirjaamisen yhteydessä kaksi lykkäysaikataulua. Alennus- ja kulusummat kirjataan eri lykkäystileille.</p></li><li>**Yhdistä alennus tuottoon** – Alennuksen summa yhdistetään kulun summaan. Luodaan yksi lykkäyssuunnitelma, ja sekä alennuksen summa että kulun summa kirjataan samalle lykkäystilille.<p>Tällöin luodaan ostotilauksen luomisen ja kirjaamisen yhteydessä yksi lykkäysaikataulu. Sekä alennuksen summa että kulun summa kirjataan samalle lykkäystilille.</p></li></ul> |
| Konsolidoi aiemmat kaudet | <p>Määritä, konsolidoidaanko edellisten kausien lykkäysrivit:</p><ul><li>**Kyllä** – Jos lykkäyksen alkamispäivämäärä on tapahtumapäivää ennen jaksoa, kaikki tapahtumapäivämäärän kauden kautta olevat summat yhdistetään yksittäiseen lykkäyssuunnitelmariviin.</li><li>**Ei** – Kaikkien kausien summat pidetään erillisinä lykkäysriveillä.<p>Jos lykkäyksen alkamispäivä on samassa ajanjaksossa tai myöhempi kuin tapahtumapäivä, tällä vaihtoehdolla ei ole vaikutusta.</p></li></ul><p>Tämä asetus voidaan päivittää tapahtumatasolla.</p> |
| Lykkäyksen oletusarvoinen alkamispäivä | <p>Valitse sääntö, jota käytetään lykkäysaikataulun alkamispäivän määrittämiseen:</p><ul><li>**Tapahtumapäivä** – Käytä tapahtuman päivämäärää aloituspäivämääränä.</li><li>**Kuluvan kuukauden alku** – Käytä aloituspäivänä kuluvan kuukauden ensimmäistä päivää. Jos tapahtumapäivämäärä on kuukauden ensimmäinen päivä, aloituspäivämäärä on kuluvan kuukauden ensimmäinen päivä.</li><li>**Seuraavan kuukauden alku** – Käytä aloituspäivänä seuraavan kuukauden ensimmäistä päivää. Jos tapahtuman päivämäärä on ensimmäinen päivä, tapahtumapäivämäärää käytetään. Muussa tapauksessa käytetään seuraavan kuukauden ensimmäistä.</li><li>**15:n sääntö** – Jos tapahtuman päivämäärä on ensimmäisen ja viidennentoista päivän välissä, aloituspäivänä käytetään kuluvan kuukauden ensimmäistä. Jos tapahtumapäivämäärä on kuukauden kuudestoista tai myöhempi, aloituspäivämäärä on seuraavan kuukauden ensimmäinen päivä.</li></ul><p>Voit päivittää tämän asetuksen tapahtumatasolla.</p> |
| Lyhytaikainen lykkäysmenetelmä | <p>Valitse lyhyt lykkäysmenetelmä: **ei mitään**, **liukuvat kaudet** tai **kiinteä vuosi**.</p><p>|
| Lykkäyskirjausmenetelmä | <p>Valitse tapa, jota on käytetty lykkäystapahtumien luontiin.</p><ul><li>**Tase** – Luo lykkäystapahtumia taseen kirjausmenetelmän avulla.</li><li>**Voitto ja tappio** – Käytä voitto- ja tappiokirjaustapaa luodaksesi lykkäystapahtumia. Kun tapahtumat kirjataan, voit tarkistaa laskutositteen lisämerkinnät, jotka tasaavat alkuperäisen kirjauksen ja kirjauksen vastakirjauksen summat.</li></ul> |
| Kumoa tulos luotossa | <p>**Huomautus:** Tämä kenttä on käytettävissä vain, kun **Lykkäyskirjaustapa**-kentän arvoksi on määritetty **Voitto ja tappio**.</p><p>Määritä, palautetaanko tulossummat, kun laskutusaikatauluun tai myyntitilaukseen sovelletaan peruuttamista, irtisanomista tai hyvitystä:</p><ul><li>**Kyllä** – Palauta tulossummat ja käytä hyvitysoikaisusummaa lykkäysaikataulussa.<p>Jos peruutus tapahtuu laskutuskauden puolessavälissä, määrät suhteutetaan.</p></li><li>**Ei** – Voitolle ja tappiolle ei luoda peruutustapahtumaa, kun laskutusaikatauluun tai myyntitilaukseen sovelletaan peruutusta, lopettamista tai hyvitystä.</li></ul> |
| **Tuloutus**-välilehti | |
| Kirjaa yleiset kirjauskansiot automaattisesti | <p>Määritä, kirjataanko tuoton ja kulun lykkäyksien luomat kirjauskansiomerkinnät automaattisesti:</p><ul><li>**Kyllä** – Kirjaa automaattisesti kirjauskansiokirjaukset, jotka on luotu tulojen ja kulujen lykkäysten perusteella.<p>**Vihje:** Jos valitset **Kyllä**, voit estää kirjanpidon epäyhtenäisyydet, jotka manuaaliset tositteen muutokset aiheuttavat.</p></li><li>**Ei** – Kirjauskansiokirjauksia, jotka on luotu tulojen ja kulujen lykkäysten perusteella ei kirjata automaattisesti. Kaikki kirjauskansiot on kirjattava manuaalisesti.</li></ul> |
| Luo tuloutuskirjauskansion yhteenveto | <p>Määritä, konsolidoidaanko tuloutustositteet oletusarvoisesti:</p><ul><li>**Kyllä** – Luo yksi tosite kaikille tunnistusriveille, joissa on sama päivämäärä. Kaikki saman tilin tositteen rivit konsolidoidaan yhdelle riville.</li><li>**Ei** – Luo tosite kullekin tuloutusriville.</li></ul><p>Voit päivittää tämän asetuksen **Tuloutuksen käsittely** -sivulla.</p> |
| Kirjauskansion oletusnimi | Valitse nimi kirjauskansiolle, joka luodaan tuotto- ja kulujen lykkäysprosesseista, kuten kirjauskäsittelystä. |
| Tuloutuksen kirjauskansiorivin kuvaus | <p>Valitse kirjauskansiotositerivin kuvauksessa näkyvä kuvaus.</p><ul><li>**Ajoita rivin päivämäärät** – Näytä aikataulun rivipäivämäärät kirjauskansiorivin kuvauksessa.</li><li>**Alkuperätapahtuman tiedot** – Näytä alkuperätapahtumatiedot kirjauskansiorivin kuvauksessa.<p>**Esimerkki:** USMF-0001, CIV-00839, Ohjelmiston tuotto</p></li></ul> |
| **Numerosarjat**-välilehti | Tässä välilehdessä voit määrittää vuokranumerosarjojen oletusarvot. Numerosarjan luontitoimintoa käytetään numerosarjojen luomisessa ja määrittämisessä automaattisesti. Numerosarjaa ei tarvitse muuttaa, ellet halua tehdä luotuihin numerosarjoihin muutoksia manuaalisesti. |
| Aikataulun numero | Numero, jota käytetään lykkäysaikatauluissa. |

## <a name="deferral-templates"></a>Lykkäysmallit

**Lykkäysmallit**-sivulla voit määrittää tasapoistomalleja, joita käytetään lykkäyksissä.

Seuraavassa on joitakin mallin käytön etuja:

* Järjestelmä laskee lykkäyspituuden automaattisesti.
* Voit sallia lykkäysaikataulut, joilla on jaksoja, joiden kirjaaminen ohitetaan.
* Voit automatisoida lykkäykset liitämällä mallin tuotteeseen, tuoteryhmään, tuoteluokkaan, asiakkaisiin tai asiakasryhmään. Mallimääritys tehdään **Lykkäyksen oletukset** -sivulla.

Malleille on saatavana useita ajanjaksojen esiintymistiheyksiä: päivittäinen, kuukausittainen tai tilikausittainen.

Mallirivit koostuvat tyypistä (**Tunnistettu** tai **Ohitettu**) ja kauden pituudesta. Ohitetuilla riveillä on summa 0 (nolla) lykkäysriveillä. Tämä toiminto voi olla hyödyllinen, jos et halua tunnistaa tuottoa kaikilla kausilla.

### <a name="create-a-deferral-template"></a>Luo lykkäysmalli

Voit luoda lykkäysmallin seuraavien vaiheiden avulla.

1. Valitse **Lykkäysmallit**-sivulla **Uusi**.
2. Kirjoita nimi **Malli**-kenttään.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Kauden taajuus** -kentässä kauden taajuus.
5. Valitse **Lisää**, jos haluat lisätä rivin riviluettelon yläosaan, tai lisää rivi luettelon loppuun valitsemalla **Liitä**.
6. Valitse **Tyyppi**-kentässä kauden tyyppi.
7. Määritä **Kauden pituus** -kenttään kauden pituus.
8. Toista vaiheet 5-7 jokaiselle tarvitsemallesi lisäyritykselle.
9. Valitse **Tallenna**.

## <a name="deferral-defaults"></a>Lykkäyksen oletusarvot

**Lykkäyksen oletukset** -sivun avulla voit määrittää nimikkeiden oletuslykkäystilit ja määrittää nimikkeiden oletusmallit. Voit myös määrittää maksuille lykkäystilejä ja määrittää malleja lykkäyksille.

**Lykkäys nimikkeen mukaan**

Jos tapahtumalla on nimike (esimerkiksi myyntitilauksia), voit määrittää tilejä ja malleja tietyille nimikkeille ja asiakkaille. Näitä asetuksia käytetään oletusarvoina, kun tapahtumaa lykätään. Jos haluat, että tapahtumasta tehdään oletusarvoisesti lykkäys, sinun on määritettävä nimikkeet **Lykättävät nimikkeet** -sivulla.

**Lykkää tilin mukaan**

Jos tapahtumalla ei ole nimikkeitä (esimerkiksi yleisiä kirjauskansioita), voit määrittää lykkäystilit. Kun tilejä käytetään tapahtumarivillä, tapahtuma merkitään automaattisesti lykättyksi. Tapahtumariville määritetään vastaava malli- ja tuloutustili.

**Kaikki tapahtumatyypit (esimerkiksi Myyntitilaus-, Osto- ja Kirjanpito-välilehdet)**

Sivun tilit ovat päätilejä, etkä voi käyttää taloushallinnon dimensioita. Tunnustustilin taloushallinnon dimensiot ovat asiakkaalta tai nimikkeeltä organisaation mukaan.

Jokaisella mallirivillä on oltava joko tasapoistomalli tai tapahtumapohjainen malli. Siinä ei voi olla molempia.

### <a name="for-sales-orders"></a>Myyntitilaukset

Voit määrittää myyntitilausten lykkäyksen oletusarvot noudattamalla seuraavia vaiheita.

1. Valitse **Myyntitilaus**-välilehdestä lykkäystyyppi.
2. Lisää rivi valitsemalla **Lisää**.
3. Valitse **Nimikekoodi**-kentässä nimikkeen koodi. Nimikekoodi määrittää, miten lykkäysten oletusarvoja käytetään.
4. Määritä, miten nimikekoodia käytetään:

    * Jos **Tuotekoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse nimikesuhde **Tuotesuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi on määritetty **Luokka**, valitse luokkasuhde **Luokkasuhteesta**.
    * Jos **Nimikekoodi**-kentän arvoksi määritetään **Kaikki**, oletusarvot koskevat kaikkia soveltuvia tietueita.

5. Määritä, miten tilikoodia käytetään:

    * Jos **Tilikoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse tilisuhde **Tilisuhde**-kentässä.
    * Jos **Tilikoodi**-kentän arvoksi määritetään **Kaikki**, tili koskee kaikkia soveltuvia tietueita.

6. Valitse **Päätili**-kentässä päätili lykkäyksen kirjaamista varten.
7. Jos **Lykkäyskirjausmenetelmä**-kentän arvoksi on määritetty **Tuotto ja tappio**, valitse alkuperäinen tuottotili **Alkuperäinen tuottotili** -kentässä ja tuoton vastatili **Tuottovastatili**-kentässä.
8. Jos **lyhytkestoisten lykkäysmenetelmien** kentän arvoksi on määritetty **Liukuvat jaksot** tai **Kiinteä vuosi**, valitse lyhyt lykkäystili **lyhytkestoinen lykkäystili** -kentässä.
9. Jos haluat lisätä rivin malliin, valitse **Lisää**.
10. Valitse **Nimikekoodi**-kentässä nimikkeen koodi.
11. Määritä, miten nimikekoodia käytetään:

    * Jos **Tuotekoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse nimikesuhde **Tuotesuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi on määritetty **Luokka**, valitse luokkasuhde **Luokkasuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi määritetään **Kaikki**, oletusarvot koskevat kaikkia soveltuvia tietueita.

12. Määritä, miten tilikoodia käytetään:

    * Jos **Tilikoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse tilisuhde **Tilisuhde**-kentässä.
    * Jos **Tilikoodi**-kentän arvoksi määritetään **Kaikki**, tili koskee kaikkia soveltuvia tietueita.
    * Valitse tasapoistomalli **Tasapoistomalli**-kentästä tai tapahtumapohjaisesta mallista **Tapahtumamalli**-kentästä.

13. Valitse **Tallenna**.

### <a name="for-purchase-orders"></a>Ostotilaukset

Voit määrittää ostotilausten lykkäyksen oletusarvot noudattamalla seuraavia vaiheita.

1. Valitse **Osto**-välilehdestä lykkäystyyppi.
2. Lisää rivi valitsemalla **Lisää**.
3. Valitse **Nimikekoodi**-kentässä nimikkeen koodi.
4. Määritä, miten nimikekoodia käytetään:

    * Jos **Tuotekoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse nimikesuhde **Tuotesuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi on määritetty **Luokka**, valitse luokkasuhde **Luokkasuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi määritetään **Kaikki**, oletusarvot koskevat kaikkia soveltuvia tietueita.

5. Määritä, miten tilikoodia käytetään:

    * Jos **Tilikoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse tilisuhde **Tilisuhde**-kentässä.
    * Jos **Tilikoodi**-kentän arvoksi määritetään **Kaikki**, tili koskee kaikkia soveltuvia tietueita.

6. Valitse **Päätili**-kentässä päätili lykkäyksen kirjaamista varten.
7. Jos **Lykkäyskirjausmenetelmä**-kentän arvoksi on määritetty **Tuotto ja tappio**, valitse alkuperäinen tuottotili **Alkuperäinen tuottotili** -kentässä ja tuoton vastatili **Tuottovastatili**-kentässä.
8. Jos **lyhytkestoisten lykkäysmenetelmien** kentän arvoksi on määritetty **Liukuvat jaksot** tai **Kiinteä vuosi**, valitse lyhyt lykkäystili **lyhytkestoinen lykkäystili** -kentässä.
9. Jos haluat lisätä rivin malliin, valitse **Lisää**. 
10. Valitse **Nimikekoodi**-kentässä nimikkeen koodi.
11. Määritä, miten nimikekoodia käytetään:

    * Jos **Tuotekoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse nimikesuhde **Tuotesuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi on määritetty **Luokka**, valitse luokkasuhde **Luokkasuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi määritetään **Kaikki**, oletusarvot koskevat kaikkia soveltuvia tietueita.

12. Määritä, miten tilikoodia käytetään:

    * Jos **Tilikoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse tilisuhde **Tilisuhteesta**.
    * Jos **Tilikoodi**-kentän arvoksi määritetään **Kaikki**, tili koskee kaikkia soveltuvia tietueita.
    * Valitse tasapoistomalli **Tasapoistomalli**-kentästä tai tapahtumapohjaisesta mallista **Tapahtumamalli**-kentästä.

13. Valitse **Tallenna**.

### <a name="for-general-journals"></a>Yleisille kirjauskansioille

Voit määrittää lykkäyksen oletusarvot yleisille kirjauskansioille seuraavasti.

1. Valitse **Yleinen kirjauskansio** -välilehti.
2. Jos haluat lisätä rivin lykkäykseen, valitse **Lisää**.
3. Jos **lyhytkestoisten lykkäysmenetelmien** kentän arvoksi on määritetty **Liukuvat jaksot** tai **Kiinteä vuosi**, valitse lyhyt lykkäystili **lyhytkestoinen lykkäystili** -kentässä.
4. Valitse **Lykkäystili**-kentässä lykkäystili.
5. Valitse **Tuottokirjaustili**-kentässä tuottokirjaustili.
6. Jos **Lykkäyskirjausmenetelmä**-kentän arvoksi on määritetty **Tuotto ja tappio**, valitse alkuperäinen tuottotili **Alkuperäinen tuottotili** -kentässä ja tuoton vastatili **Tuottovastatili**-kentässä.
7. Valitse tasapoistomalli **Tasapoistomalli**-kentästä tai tapahtumapohjaisesta mallista **Tapahtumamalli**-kentästä.
8. Valitse **Tallenna**.

### <a name="for-free-text-invoices"></a>Vapaatekstilaskuille

Voit määrittää vapaatekstilaskujen lykkäyksen oletusarvot noudattamalla seuraavia vaiheita.

1. Valitse **Vapaatekstimuotoinen lasku** -välilehti.
2. Jos haluat lisätä rivin lykkäykseen, valitse **Lisää**.
3. Määritä, miten tilikoodia käytetään:

    * Jos **Tilikoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse tilisuhde **Tilisuhde**-kentässä.
    * Jos **Tilikoodi**-kentän arvoksi määritetään **Kaikki**, tilikoodi koskee kaikkia soveltuvia tietueita.

4. Valitse **Lykkäystili**-kentässä lykkäystili.
5. Jos **lyhytkestoisten lykkäysmenetelmien** kentän arvoksi on määritetty **Liukuvat jaksot** tai **Kiinteä vuosi**, valitse lyhyt lykkäystili **lyhytkestoinen lykkäystili** -kentässä.
6. Valitse **Tuottokirjaustili**-kentässä tuottokirjaustili.
7. Jos **Lykkäyskirjausmenetelmä**-kentän arvoksi on määritetty **Tuotto ja tappio**, valitse alkuperäinen tuottotili **Alkuperäinen tuottotili** -kentässä ja tuoton vastatili **Tuottovastatili**-kentässä.
8. Valitse tasapoistomalli **Tasapoistomalli**-kentästä tai tapahtumapohjaisesta mallista **Tapahtumamalli**-kentästä.
9. Valitse **Tallenna**.

### <a name="for-invoice-journals"></a>Toimittajan laskun kirjauskansioille

Voit määrittää lykkäyksen oletusarvot laskukirjauskansioille seuraavasti.

1. Valitse **Laskukirjauskansio**-välilehti.
2. Jos haluat lisätä rivin lykkäykseen, valitse **Lisää**.
3. Määritä, miten tilikoodia käytetään:

    * Jos **Tilikoodi**-kentän arvo on **Taulukko** tai **Ryhmä**, valitse tilisuhde **Tilisuhde**-kentässä.
    * Jos **Tilikoodi**-kentän arvoksi määritetään **Kaikki**, tilikoodi koskee kaikkia soveltuvia tietueita.

4. Valitse **Lykkäystili**-kentässä lykkäystili.
5. Jos **lyhytkestoisten lykkäysmenetelmien** kentän arvoksi on määritetty **Liukuvat jaksot** tai **Kiinteä vuosi**, valitse lyhyt lykkäystili **lyhytkestoinen lykkäystili** -kentässä.
6. Valitse **Tuottokirjaustili**-kentässä tuottokirjaustili.
7. Jos **Lykkäyskirjausmenetelmä**-kentän arvoksi on määritetty **Tuotto ja tappio**, valitse alkuperäinen tuottotili **Alkuperäinen tuottotili** -kentässä ja tuoton vastatili **Tuottovastatili**-kentässä.
8. Valitse tasapoistomalli **Tasapoistomalli**-kentästä tai tapahtumapohjaisesta mallista **Tapahtumamalli**-kentästä.
9. Valitse **Tallenna**.

### <a name="items-that-are-deferred-by-default"></a>Oletusarvoisesti lykätyt nimikkeet

**Oletusarvoisesti lykätyt nimikkeet** -sivulla voit määrittää, mitä nimikkeitä lykätty oletusarvoisesti käytetään. Voit määrittää tapahtumatyypit, joista nimikkeitä lykätään. Voit määrittää, onko yksittäistä nimikettä lykätty vai koko nimikeryhmää tai luokkaa.

Kun määrität nimikkeet lykätyiksi, valitse oletustilit ja -mallit **Lykkäämisen oletukset** -sivulla. Jos tilejä ja malleja ei valita, tapahtumarivejä, joiden nimikkeet syötetään, ei lykätä.

Niiden tuotteiden osalta, joita lykätään sen myynti- tai ostoluokan perusteella, johon ne liittyvät, lykkäysasetukset perustuvat luokkaan. Jos luokkaa ei kuitenkaan ole valittu **Luokkasuhde**-kentässä, käytetään sen luokan lykkäysasetuksia, jonka taso on korkeampi. Voit esimerkiksi lisätä **Kotivideo**-myyntiluokan, mutta et **Televisio** myyntiluokkaa. Kun lisäät **Televisio**-luokkaan liittyvän lykkäysnimikkeen, nimikkeelle käytetään **Kotivideon** lykkäysasetuksia.

### <a name="set-up-deferred-items"></a>Määritä lykätyt nimikkeet

Voit määrittää oletusarvoisesti lykätyt nimikkeet noudattamalla seuraavia ohjeita.

1. Valitse **Lykättyjen nimikkeiden oletukset** -sivulla välilehti, jonka haluat määrittää **myyntitilaukseksi** tai **ostoksi**.
2. Lisää rivi valitsemalla **Lisää**.
3. Valitse **Nimikekoodi**-kentässä nimikkeen koodi.
4. Määritä, miten nimikekoodia käytetään:

    * Jos **Tuotekoodi**-kentän arvo on **Ryhmä** tai **Taulukko**, valitse nimikesuhde **Tuotesuhde**-kentässä.
    * Jos **Nimikekoodi**-kentän arvoksi on määritetty **Luokka**, valitse luokkasuhde **Luokkasuhde**-kentässä.

5. Toista vaiheet 2-4 jokaiselle tarvitsemallesi lisäyritykselle.
6. Valitse **Tallenna**.

## <a name="deferred-charges"></a>Lykätyt kulut

**Lykkäyskulut**-sivulla voit määrittää, mitä kuluja lykätään oletusarvoisesti.

> [!NOTE]
> * Tällä hetkellä lykättävät maksut ovat saatavilla vain myyntitilauksille.
> * Kuluja voidaan lykätä vain rivitasolla. Jos haluat lykätä kulua myyntitilauksen otsikon tasolla, voit määrittää kulun lykättyksi nimikkeeksi myyntitilauksen erilliselle riville.
> * Jos haluat lykätä vapaatekstilaskun veloituskuluja, sinun on kirjoitettava kulu erillisenä lykättynä laskurivinä.
> * Tämä toiminto ei ole käytettävissä tukimaksuissa eikä tuottojen jakamistoiminnoissa.

### <a name="set-up-deferred-charges"></a>Määritä lykätyt kulut

Voit määrittää lykätyt kulut noudattamalla seuraavia ohjeita.

1. Lisää rivi valitsemalla **Lykätyt kulut**-sivulla **Lisää**.
2. Valitse **Veloituskoodi**-kentässä veloituksen koodi.
3. Valitse **Veloitussuhde**-kentässä veloitussuhde.
4. Toista vaiheet 1-3 jokaiselle tarvitsemallesi lisäyritykselle.
5. Valitse **Tallenna**.

## <a name="event-based-deferral-templates"></a>Tapahtumaan perustuvat lykkäysmallit

**Tapahtumapohjaiset lykkäysmallit** -sivulla voit määrittää tapahtumapohjaiset lykkäysmallit, joita voit käyttää tapahtumien lykkäyksissä ja liittää ne **Lykkäyksen oletukset** -sivulle.

### <a name="create-an-event-based-template"></a>Luo tapahtumaan perustuva malli

Voit luoda tapahtumaan perustuvan lykkäysmallin seuraavien vaiheiden avulla.

1. Valitse **Tapahtumaan perustuvat lykkäysmallit** -sivulla **Uusi**.
2. Anna **Malli**-kentässä malliryhmän yksilöivä nimi.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Kohdistustyyppi**-kentässä kohdistustyyppi.

    * **Muuttujasumma** – Kohdista tietty summa jokaiselle syötetylle riville.
    * **Sama summa** – Kohdista sama summa jokaiselle syötetylle riville. 
    * **Prosentti** – Kohdista summa, joka perustuu kullekin riville syötettyyn prosenttiarvoon.
    * **Valmistumisprosentti** – Anna kullekin syötetylle riville kumulatiivinen valmistumisarvo.
    * **Muuttujamäärä** – Kohdista tietty määrä jokaiselle syötetylle riville.

5. Aseta **Luo erilliset tapahtumat yksikköä kohden** -asetukseksi **Kyllä**, jos haluat, että jokainen tapahtumarivi jaetaan tasaisesti laskutapahtuman yksikkömäärän mukaan. Määritä arvoksi **Ei**, jos et halua jakaa tapahtumarivejä.
6. Valitse **Vanhenemistili**-kentässä vanhenemistili.
7. Valitse **Lisää**, jos haluat lisätä rivin riviluettelon yläosaan, tai lisää rivi luettelon loppuun valitsemalla **Liitä**.
8. Anna tapahtuman kuvaus **Kuvaus**-kentässä.
9. Jos **Kohdistustyyppi**-kentän arvo on **Prosenttiosuus**, määritä jakoprosentti **Kohdistusprosentti**-kenttään. Prosentin on oltava välillä 0 (nolla) ja 100. Jos jätät **Kohdistusprosentti**-kentän tyhjäksi, prosenttiarvoksi katsotaan 0. Kaikkien prosenttiosuuksien summa näkyy sivun alalaidan **Kokonaisprosentti**-kentässä, ja sen on oltava 100.
10. Määritä **Kuukautta vanhenemiseen** -kenttään, kuinka monta kuukautta tapahtuma on voimassa. Tapahtuman lykkäyspäivämäärä määritetään automaattisesti tämän arvon perusteella.
11. Valitse **Tuotto kirjattaessa** -valintaruutu, kun haluat tunnistaa tuoton automaattisesti, kun tapahtuma kirjataan. Jos valintaruutua jätetään tyhjäksi, tuotto on tunnistettava manuaalisesti.
12. Valitse **Tuottokirjaustili**-kentästä tapahtuman tunnustustili, jos tapahtuma käyttää eri tiliä kuin koko lykkäysaikataulu. Tätä kenttää käytetään yhdessä **Tuotto kirjattaessa** -valintaruudun kanssa.
13. Toista vaiheet 7-12 jokaiselle tarvitsemallesi lisäyritykselle.
14. Valitse **Tallenna**.
