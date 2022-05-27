---
title: Tapahtumien lykkäykset tilauslaskutuksessa
description: Tässä aiheessa kuvataan tapahtumia, joita voidaan käyttää tapahtumien lykkäyksissä osana tuottoja ja kulujen lykkäyksiä ylläpitosopimuksen laskuttamisen yhteydessä.
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
ms.openlocfilehash: 5913308d4ee9fdcb8cf2b862171078f27f651662
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686014"
---
# <a name="deferral-default-transactions"></a>Lykkäyksen oletustapahtumat

Tässä aiheessa kuvataan tapahtumia, jotka sallivat tuottojen ja kulujen lykkäykset. Lykkäysaikataulut perustuvat aina alkuasiakirjaan tai laskutusaikatauluun. Lykkäysaikataulut luodaan oletusten perusteella, niitä eikä niitä voi syöttää eikä luoda erikseen.

## <a name="sales-order-transaction-deferral"></a>Myyntitilaustapahtuman lykkäys

Määritä tai muokkaa myyntitilausrivin lykkäysparametreja käyttämällä **Lykkäys**- tai **Luo hyvityslasku** -sivua.

> [!NOTE]
> Kun myyntitilaus luodaan laskutussuunnitelmasta, kaikki **lykkäykset**- tai **Luo hyvityslasku** -sivun arvot ovat vain luku -arvoja, eikä lykkäysparametreja voi muokata. Voit muokata arvoja **Muokkaa aikataulua** -sivulla.

### <a name="edit-deferral-options"></a>Muokkaa lykkäysasetuksia

Jos haluat muokata rivin lykkäysasetuksia, noudata seuraavia ohjeita.

1. Luo myyntitilaustapahtuma.
2. Valitse rivi ja valitse sitten **Lykkäykset**.
3. **Tapahtuman lykkäys** -sivulla **lykätty**-vaihtoehtoon määritettävä **Kyllä**. Muokkaa näitä muista kenttiä tarpeen mukaan.
4. Esikatsele lykättyä aikataulua valitsemalla **Esiversio**.
5. Jos olet tehnyt muutoksia tapahtuman lykkäyukseen, valitse **OK** ja palaa tapahtumasivulle.
6. Vahvista ja kirjaa tapahtuma.

Kun tapahtuma on kirjattu, voit tarkastella lykkäysaikataulua avaamalla **Kaikki lykkäysaikataulut** -sivun.

### <a name="create-a-credit-note"></a>Hyvityslaskun luominen

Voit luoda hyvityslaskun seuraavien ohjeiden avulla.

1. Luo myyntitilaustapahtuma.
2. Valitse **Myyntitilausrivit**-osassa nimike, jota varten haluat luoda hyvityslaskun.
3. Valitse **Myyntitilausrivi** \> **Uusi** ja valitse sitten **Hyvityslasku**.
4. Valitse **lykkäykset**.
5. Määritä **Myyntitilaustapahtuman lykkäys** - sivulla **Oikaise aiemmin luotu aikataulu** - asetuksen arvoksi **Kyllä** nimikkeelle.
6. Valitse **Oikaistu aikataulu** -kentästä lykkäyssuunnitelma, johon haluat hyvityslaskun kohdistaa.
7. Päivitä **Laske päivämäärä**- ja **Päättymispäivä** -kentät tarpeen mukaan.
8. Valitse **OK**.
9. Myyntitilaustapahtuman kirjaaminen on valmis.

### <a name="purchase-orders-and-purchase-invoices"></a>Ostotilaukset ja ostolaskut

Jos haluat käyttää ostotilauksen lykkäystoimintoa, luo lasku ensin. Tämän jälkeen voit muokata tai lisätä lykkäysnimikkeitä **odottavien toimittajien laskujen** sivulla. Et voi muokata tai lisätä lykkäyksiä suoraan ostotilaukseen.

1. Syötä toimittajan lasku **odottavien toimittajien laskujen** sivulla.

    Kun määrität rivin, lykkäys määritetään automaattisesti valitsemallesi nimike- tai hankintaluokalle. Tämä lykkäys perustuu **Lykkäyksen oletukset** -sivun lykkäysasetuksiin. Lykkäyksiä voi muokata tai lisätä jakelutasolla.

3. Valitse ostorivillä **Myyntitiedot \> jaa summat**.
4. Valitse kullekin jakosummalle **lykkäykset**. Kun lasku kirjataan, jokaiselle jakaumalle luodaan lykkäysaikataulu, jota varten on määritetty lykkäys.

### <a name="tax"></a>Vero

Joissakin tapauksissa veron summa voi olla kokonaan tai osittain ei-palautettava. Jos lykättävän rivin veron summa sisältää summan, jonka summaa ei voi palauttaa, verosumma sisältyy laskua kirjattaessa lykättävään aikataulun summaan.

### <a name="variance"></a>Ero

Jos toimittajalaskun rivillä oleva summa eroaa ostotilausrivin summasta, luodaan varianssijakaumat. Jos riviä lykättiin, näiden jakojen kirjanpitotiliksi määritetään lykkäystili ja summat sisällytetään laskua kirjattaessa, kun lasku kirjataan. Näitä jakoja ovat nimeltään **Hinnan varianssi** ja **kustannusten varianssi**.

### <a name="general-journals-and-invoice-journals"></a>Yleiset kirjauskansiot ja laskukirjauskansiot

Käytä **Lykkäykset**-sivua voidaksesi määrittää kirjaustositerivin lykkäysparametrit. Voit myös esikatsella tasapoistojen lykkäysaikataulua. Kun syötät rivin, lykkäys määritetään automaattisesti **Lykkäyksen oletusasetukset** -sivulla olevien lykkäystilien asetusten perusteella. Voit manuaalisesti muuttaa kunkin rivin lykkäysehtoja. Kun kirjaustosite kirjataan, luodaan lykkäysaikataulu.

#### <a name="post-and-transfer"></a>Kirjaa ja siirrä

Kirjaa kirjaustosite käyttämällä **Kirjaa ja siirrä** -komentoa. Lykkäysvaihtoehdot noudattavat riviä, jota tosite koskee. Jos tositteissa ei ole virheitä, järjestelmä luo lykkäysaikataulun, jos sitä lykättiin. Jos tositteessa on virhe ja siirretään, myös mahdolliset lykkäysvaihtoehdot siirretään sen mukana.

#### <a name="tax"></a>Vero

Joissakin tapauksissa veron summa voi olla kokonaan tai osittain ei-palautettava. Jos lykättävän rivin veron summa sisältää summan, jonka summaa ei voi palauttaa, verosumma sisältyy laskua kirjattaessa lykättävään aikataulun summaan.

## <a name="free-text-invoice-transaction-deferral"></a>Vapaatekstilaskutapahtuman lykkäys

Käytä **Lykkäykset**-sivua voidaksesi määrittää vapaatekstilaskun rivijaon lykkäysparametrit. Kun jakelu syötetään, lykkäys määritetään automaattisesti **Lykkäyksen oletusasetukset** -sivun lykkäysasetusten perusteella.

## <a name="fields"></a>Kentät

**Tapahtuman lykkäys**-sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------|
| Lykätty | <p>Määritä, onko rivi lykättävä:</p><ul><li>**Kyllä** – Rivi on lykättävä.</li><li>**Ei** – Rivi ei ole lykättävä.</li></ul><p>Kun tämän vaihtoehdon arvoksi on määritetty **Kyllä**, **Aiemmin luodun aikataulun oikaiseminen** -vaihtoehto ei ole käytettävissä. Nimikkeiden ja kulujen, jotka on jo määritetty lykätyksi, asetuksena on **Kyllä**. Valitse **Kyllä** tuotteille ja maksuille, joita ei ole oletusarvoisesti määritetty lykätyiksi.</p> |
| Muuta aiemmin luotua aikataulua | <p>Määritä, onko rivi oikaisu aiemmin luotuun lykkäysaikatauluun:</p><ul><li>**Kyllä** – Uusi myyntirivi on oikaisu aiemmin luotuun lykkäysaikatauluun. Tässä tapauksessa voit valita lykkäysaikataulun **Oikaistu aikataulu** -kentästä.</li><li>**Ei** – Uusi myyntirivi ei ole oikaisu aiemmin luotuun lykkäysaikatauluun.</li></ul><p>Kun tämän vaihtoehdon arvoksi on määritetty **Kyllä**, **Lykätty**-vaihtoehto ei ole käytettävissä.</p> |
| Muutettu aikataulu | <p>Valitse lykkäyssuunnitelma, jota rivi oikaisee. Kaikki sivun arvot päivitetään sitten alkuperäisen lykkäysaikataulun arvoilla. Näitä arvoja ei voi muokata.</p><p>Tämä kenttä on käytettävissä vain, kun **Muokkaa olemassa olevaa aikataulua** -asetuksena on **Kyllä**.</p> |
| Uudelleenlaskentapäivä | <p>Määritä sen kauden alkamispäivämäärä, jolloin haluat laskea jäljellä olevan summan uudelleen. Oletuspäivämäärä on seuraavan toteutumattoman kauden päivämäärä.</p><p>Tämä kenttä on käytettävissä vain, kun **Muokkaa olemassa olevaa aikataulua** -asetuksena on **Kyllä**.</p> |
| Päättymispäivä | <p>Lykkäystyypistä riippuen päättymispäivä saattaa päivittyä:</p><ul><li>Jos haluat käyttää rivin lykkäystä, määritä aikataulun uusi päättymispäivä. Lykkäysaikataulun päättymispäivä on oletusarvo.</li><li>Jos tapahtuma perustuu lykkäyseen, määritä hyvitystapahtumarivin päättymispäivämäärä. Tämä päivämäärä voi olla tyhjä.</li></ul><p>Tämä kenttä on käytettävissä vain, kun **Muokkaa olemassa olevaa aikataulua** -asetuksena on **Kyllä**.</p> |
| Laskutusaikataulun numero | <p>Laskutusaikataulun numero.</p><p>Tämä kenttä on käytettävissä vain toistuvia sopimuslaskutusaikatauluja varten.</p> |
| Lykkäyksen oikaisumenetelmä | <p>Lykätty oikaisumenetelmä. Arvo vastaa toistuvan sopimuksen laskutusaikataulun **Massairtisanomisen käsittely** -sivulla olevaa arvoa.</p><p>Tämä kenttä on käytettävissä vain toistuvia sopimuslaskutusaikatauluja varten.</p> |
| **Tilit - tuotto** | |
| Lykkäystili | <p>Lykkäystili eli **myyntitilaus**-sivulla näkyvä kirjaustili.</p><p>Jos riviä ei lykätä, tämä kenttä on tyhjä. Tässä tapauksessa kirjaustili on oletustuottotili.</p> |
| Tuloutustili | <p>Määritä tili, jota käytetään, kun lykkäys hyväksytään. Tilin tulee olla eri kuin lykkäystili.</p><p>Kun **Lykätty**-asetuksena on aluksi **Kyllä**, lykkäystilillä käytettävät dimensioarvot kopioidaan hyväksyntätilille. Jos lykkäystilin dimensiota ei ole hyväksyntätilille, se ohitetaan.</p> |
| Alkuperäinen tuloutustili | <p>Valitse alkuperäisen tuoton tuloutuksen tili. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Tuottojen ja kulujen lykkäysparametrit** -sivun **Lykkäyksen kirjausmenetelmä** -kentän arvo on **Tuotto ja tappio**.</p> |
| Tuloutuksen vastatili | <p>Valitse tili tulojen kirjaamisen kuittaamista varten. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Tuottojen ja kulujen lykkäysparametrit** -sivun **Lykkäyksen kirjausmenetelmä** -kentän arvo on **Tuotto ja tappio**.</p> |
| **Tilit - Alennus** | Tämä osa on näkyvissä vain lykätyille nimikkeille. Se on piilotettu lykätyille kuluille. |
| Lykkäystili | <p>Määritä alennuksen lykkäystilin numero. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Alennuksen lykkäysvaihtoehto** -kentän arvoksi on asetettu **Alennuksen erillinen aikataulu** **Tulojen ja kulujen lykkäysparametrit** -sivulla ja riville on myönnetty alennus.</p> |
| Tuloutustili | <p>Määritä alennuksen hyväksyntätilin numero. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Alennuksen lykkäysvaihtoehto** -kentän arvoksi on asetettu **Alennuksen erillinen aikataulu** **Tulojen ja kulujen lykkäysparametrit** -sivulla ja riville on myönnetty alennus.</p> |
| Alkuperäinen tuloutustili | <p>Valitse alkuperäisen alennuksen hyväksyntätili. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Lykkäyksen kirjaustapa** -kentän arvoksi on asetettu **Tuotto ja tappio** **Tulojen ja kulujen lykkäysparametrit** -sivulla ja riville on myönnetty alennus.</p> |
| Tuloutuksen vastatili | <p>Valitse tili tulojen kirjaamisen kuittaamista varten. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Lykkäyksen kirjaustapa** -kentän arvoksi on asetettu **Tuotto ja tappio** **Tulojen ja kulujen lykkäysparametrit** -sivulla ja riville on myönnetty alennus.</p> |
| **Tilit - Kulutus** | Tämä osa on näkyvissä vain lykätyille nimikkeille. Se on piilotettu lykätyille kuluille. |
| Lykkäystili | <p>Määritä kulutuksen lykkäystilin numero.</p><p>Vakiotuotteille luodaan kaksi lykkäysaikataulua:</p><ul><li>**Vakiomyynti** – Tuottosuunnitelma, jolla on luottosaldo. Valitse tällöin kulutuksen lykkäystili.</li><li>**Kulutus** – Kulutus (myydyn tavaran kustannus \[COGS\]) kuluaikataulu, jolla on veloitussaldo. Valitse tällöin kulutuksen hyväksyntätili.</li></ul><p>Kun lasku kirjataan, kulutussumma kirjataan määritetylle kulutuksen lykkäystilille. Nämä kentät eivät ole käytettävissä huoltonimikkeissä.</p> |
| Tuloutustili | Määritä kulutuksen hyväksyntätilin numero. |
| Alkuperäinen tuloutustili | <p>Määritä alkuperäisen kulutuksenkirjauksen summan tili. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Tuottojen ja kulujen lykkäysparametrit** -sivun **Lykkäyksen kirjausmenetelmä** -kentän arvo on **Tuotto ja tappio**.</p> |
| Tuloutuksen vastatili | <p>Määritä kulutuksenkirjauksen summan vastatili. Oletusarvo on peräisin **lykkäyksen oletukset** -sivusta.</p><p>Tämä kenttä on käytettävissä vain, kun **Tuottojen ja kulujen lykkäysparametrit** -sivun **Lykkäyksen kirjausmenetelmä** -kentän arvo on **Tuotto ja tappio**.</p> |
| **Aikatauluta** | |
| Aikataulutyyppi | <p>Valitse lykkäysaikataulun tyyppi: **tasapoisto** (oletusarvo) tai **tapahtumaperuste**.</p><p>Sivulla näkyvät vaihtoehdot perustuvat valitsemaasi lykkäystyyppiin.</p><p>Jos oletusmalli on asetettu tapahtumariville **Lykkäyksen oletukset** -sivulle, lykkäysaikataulun tyyppi perustuu valitun mallin tyyppiin.</p> |
| **Aikataulu - Tasapoisto** | |
| Konsolidoi aiemmat kaudet | <p>Määritä, haluatko yhdistää aikaisempien kausien lykkäysaikataulurivit:</p><ul><li>**Kyllä** – Konsolidoi aiempien kausien lykkäysaikataulun rivit.</li><li>**EI** – Älä konsolidoi aiempien kausien lykkäysaikataulun rivejä.</li></ul><p>Oletusarvo on **tuotto- ja kululykkäyksien parametrit** -sivulla.</p> |
| Yhtä suuri joka kaudelle | <p>Määritä, onko päivien määrä jokaisella kaudella yhtä suuri vai voiko se vaihdella eri kausien välillä:</p><ul><li>**Kyllä** – Jokaisella kaudella on sama määrä päiviä.</li><li>**Ei** – Kausilla ei ole samaa päivien määrää.</li></ul><p>Kun tämän vaihtoehdon arvoksi määritetään **Ei**, jaksojen päivien määrä lasketaan, kun kunkin jaksotuksen summa lasketaan.</p><p>Oletusarvo on **tuotto- ja kululykkäyksien parametrit** -sivulla.</p> |
| Aikataulu mallista | <p>Määritä, luodaanko lykkäyssuunnitelma mallin vai päättymispäivän perusteella:</p><ul><li>**Kyllä** – Lykkäysaikataulu luodaan mallin perusteella.</li><li>**EI** – Lykkäysaikataulu luodaan päättymispäivän perusteella.</li></ul> |
| Malli | Valitse lykkäysmalli. |
| Ohituksen alkamispäivä | <p>Määritä, ohitatko aloituspäivän:</p><ul><li>**Kyllä** – Ohita aloituspäivä aloituspäivällä, jonka syötit **aloituspäivämäärä**-kentässä.</li><li>**Ei** – Alkamispäivä on **Lykkäyksen oletusalkamispäivä** -sääntö, jota sovelletaan **Laskun kirjaus** -sivulla määritettyyn laskun päivämäärään. Tämä sääntö voidaan asettaa **Tulojen ja kulujen lykkäysparametrit** -sivulla.</li></ul> |
| Lykkäyksen alkamispäivä | Määritä lykkäysaikataulun alkamispäivä. Tapahtumapäivä on oletusarvo. |
| Lykkäyksen päättymispäivä | <p>Lykkäyksen päättymispäivämäärä.</p><p>Tämä päivämäärä lasketaan automaattisesti lykkäysmallin perusteella. Jos mitään mallia ei ole valittu, päivämäärä on kirjoitettava manuaalisesti.</p> |
| **Aikataulu - Tapahtumaan perustuva** | |
| Malli | <p>Valitse tapahtumaan perustuva malli. Tämä kenttä ei ole pakollinen.</p><p>Jos valitset mallin, mallin arvot korvaavat kaikki tapahtumapohjaiset tiedot ja tapahtumarivit.</p> |
| Kohdistustyyppi | <p>Valitse tapahtumarivien kohdistustyyppi:</p><ul><li>**Muuttujasummat** – Tietty summa jokaiselle syötetylle riville.</li><li>**Yhtä suuret summat** – Summa kohdistetaan tasan kullekin riville.</li><li>**Prosentti** – Summa, joka kohdistetaan perustuen kullekin riville syötettyyn prosenttiarvoon.</li><li>**Valmistumisprosentti** – Kullekin riville syötetään kumulatiivista valmistumisarvoa.</li><p>**Muuttujamäärä** – Tietty määrä kohdistettuna jokaiselle syötetylle riville.</li></ul><p>**Huomautus:** Jos haluat valita **valmistumisprosentin**, päivämäärien on oltava nousevassa järjestyksessä.</p> |
| **Luo erilliset tapahtumat yksikköä kohden** | |
| Kuvaus | <p>Määritä, haluatko eritellä tapahtumat yksikköä kohden:</p><ul><li>**Kyllä** – Erota tapahtumarivit siten, että määrää kohden on yksi rivi.<p>Tapahtumarivejä on esimerkiksi kolme, ja laskun määrä on neljä. Tässä tapauksessa tuloksena saatavassa lykkäysaikataulussa on 12 riviä.</p></li><li>**Ei** – Älä erota tapahtumarivejä toisistaan.</li></ul> |
| Vanhentumistili | <p>Valitse tili, jota käytetään hyväksytyille vanhentuneille riveille. Voit valita tilin, kun lykkäysaikataulu on luotu.</p><p>Jos tapahtumalle määritetään erääntymispäivä, hyväksymissumma siirtyy tunnistustilin asemesta vanhentumistilille tunnistusprosessin aikana.</p> |
| **Aikataulu - Tapahtumaan perustuvat rivit** | |
| Kuvaus | Tapahtuman kuvaus. |
| Lykkäyksen päättymispäivä | <p>Valitse tapahtuman päättymispäivä.</p><p>**Huomautus:** Jos valitset päättymispäivän, **päättymispäivä**-kentän valinta tyhjeni. Päättymispäivää ja vanhentumispäivää ei voi käyttää.</p> |
| Vanhentumispäivä | <p>Valitse tapahtuman vanhentumispäivä.</p><p>**Huomautus:** Jos valitset päättymispäivän, **päättymispäivä**-kentän valinta tyhjeni. Päättymispäivää ja vanhentumispäivää ei voi käyttää.</p> |
| Määrä | <p>Määritä kohdistusmäärä. Kaikkien rivien oletusarvo on **0** (nolla). Jos päivität määrän, kaikkien rivien kokonaismäärän on oltava yhtä suuri tai pienempi kuin myyntitilauksen rivinimikkeelle määritetty määrä.</p><p>Tämä kenttä on käytettävissä vain, jos **Kohdistustyyppi** -kentän arvoksi on valittu **Muuttujan määrä**.</p><p>Jos myyntitilauksen rivinimikkeen määrä muuttuu niin, että se on pienempi kuin alkuperäinen määrä ja lasku luodaan, tapahtumaan perustuvia rivejä luodaan vähemmän. Kohdistettu kokonaismäärä ei ylitä alkuperäisen myyntitilauksen tai laskutusaikataulun määrää.</p> |
| Varausprosentti | <p>Määritä kohdistusprosentti. Jos **Kohdistustyyppi**-kentän arvoksi määritetään **Prosentti** tai **Valmistumisprosentti**, voit syöttää prosenttiluvun manuaalisesti. Muuten se lasketaan automaattisesti.</p><p>Jos **Kohdistustyyppi**-kentän arvoksi määritetään **Prosentti**, prosenttiosuuden kokonaissumman tulee olla 100.</p> |
| Määrä | <p>Määritä kohdistussumma. Jos **Kohdistustyyppi**-kentän arvoksi määritetään **muuttujien määrät** tai **Valmistumisprosentti**, voit syöttää määrän manuaalisesti.</p><p>Jos **Kohdistustyyppi**-kentän arvoksi määritetään **Valmistumisprosentti** ja kirjoitat summan tähän, **valmistumisprosentti**-kentän arvo lasketaan automaattisesti.</p><p>Pyöristys on mahdollista, kun laskettu summa ei välttämättä vastaa manuaalisesti syötettyä summaa. Jos tarvitset tarkan summan, määritä **Kohdistustyyppi**-kentän arvoksi **Muuttuvat summat**.</p> |
| Valmistumisprosentti | <p>Määritä valmistumisen prosenttiosuus. Arvon on oltava väliltä 0 (nolla) - 100.</p><p>Tämä kenttä on käytettävissä vain, jos **Kohdistustyyppi** -kentän arvoksi on valittu **Valmistumisprosentti**.</p> |
| Valmistumissumma | <p>Kaikkien lykkäysaikataulun rivien laskettu kokonaissumma.</p><p>Jos **Kohdistustyyppi**-kentän arvoksi määritetään **Valmistumisprosentti**, voit syöttää määrän manuaalisesti. Tällöin **valmistumisprosentti**-kentän arvo lasketaan syötetyn summan perusteella.</p><p>Pyöristys on mahdollista, kun laskettu summa ei välttämättä vastaa manuaalisesti syötettyä summaa.</p><p>Tämä kenttä on käytettävissä vain, jos **Kohdistustyyppi** -kentän arvoksi on valittu **Valmistumisprosentti**.</p> |
| Hyväksyntä kirjaamisessa | <p>Määritä, hyväksytäänkö rivi automaattisesti, kun tapahtuma kirjataan:</p><ul><li>**Valittu** – Rivi hyväksytään automaattisesti, kun tapahtuma kirjataan.</li><li>**Poistettu** – Riviä ei hyväksytä automaattisesti, kun tapahtuma kirjataan.</li></ul> |
| Tuloutustili | <p>Määritä tapahtuman hyväksyntätili, jos tili poikkeaa koko lykkäysaikataulussa käytetystä tilistä.</p><p>Tätä kenttää voidaan käyttää yhdessä **Hyväksy kirjauksessa** -vaihtoehdon kanssa.</p> |
