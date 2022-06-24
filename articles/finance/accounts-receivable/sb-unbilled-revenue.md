---
title: Laskuttamaton tuotto
description: Tässä artikkelissa kuvataan, kuinka nimikkeet ja tilit määritetään käyttämään laskuttamattoman tuoton ominaisuutta tilauslaskutuksessa.
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
ms.openlocfilehash: b3fe58fc06df3f61433c8457b337ae895283e12b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879679"
---
# <a name="unbilled-revenue"></a>Laskuttamaton tuotto

Tässä artikkelissa kuvataan laskuttamattoman tuoton ominaisuutta, jonka avulla voit sisällyttää taseeseen kokonaisten laskutusaikataulujen summat. Nämä summat sisällytetään laskuttamattomaan tuottotiliin ja laskuttamattoman tuoton vastatiliin, ja sopimus laskutetaan erissä.

## <a name="set-up-unbilled-revenue"></a>Laskuttamattoman tuoton määritys

Voit määrittää laskuttamattoman tuoton noudattamalla seuraavia ohjeita.

- Määritä **Toistuvan sopimuslaskutuksen parametrit** -sivulla **Laskuttamaton tuotto** -osan kentät.
- Laskuttamaton tuotto -toimintoa voi käyttää nimikkeille, joissa **Nimiketyyppi**-kentän arvo on **Vakio**. Sitä voidaan käyttää myös nimikkeiden lykkäyksiä varten. Jos haluat käyttää laskuttamatonta tuottoa lyhyen aikavälin toiminnoissa, määritä lyhyen aikavälin asetukset **Toistuvat sopimuksen laskutusparametrit** -sivulla.

Voit määrittää nimikkeet käyttämään laskuttamatonta tuottoa noudattamalla seuraavia ohjeita.

1. Valitse **Nimikkeet**-välilehdessä **Laskuttamattoman tuoton määritys** -sivulla **Lisää**.
2. Valitse uuden rivin **Nimikekoodi**-kohdasta nimikekoodi.
3. Valitse **Nimikesuhde**-kentässä nimikkeen suhde.
4. Toista nämä vaiheet lisätäksesi rivejä.
5. Valitse **Tallenna**.

Voit määrittää nimikkeet ja laskuttamattoman tuoton tilit noudattamalla seuraavia ohjeita.

1. Valitse **Tilit**-välilehdessä **Laskuttamattoman tuoton määritys** -sivulla **Lisää**.
2. Valitse uuden rivin **Nimikekoodi**-kohdasta nimikekoodi.
3. Valitse **Nimikesuhde**-kentässä nimikkeen suhde.
4. Valitse laskuttamattoman tuoton, laskuttamattoman alennuksen ja laskuttamattoman tuoton vastatilin tilit. Jotta lyhyen aikavälin tilejä voidaan käyttää, **Lyhytaikainen laskuttamaton menetelmä** -kentän arvoksi on määritettävä **Liukuvat kaudet** tai **Kiinteä vuosi** **Toistuvan sopimuksen laskutusparametrit** -sivulla.
5. Toista nämä vaiheet lisätäksesi rivejä.
6. Valitse **Tallenna**.

## <a name="use-unbilled-revenue"></a>Käytä laskuttamatonta tuottoa

1. Luo **Kaikki laskutusaikataulut** -sivulla laskutusaikataulu.
2. Jos nimikettä ei ole vielä määritetty käyttämään laskuttamatonta tuottoa, valitse **Laskuttamaton tuotto** -valintaruutu laskutusaikataulun rivillä.
3. Valitse **Laskuttamaton tuotto** -asetukseksi **Kyllä**. Tarkista ja muokkaa laskuttamattoman tuoton, laskuttamattoman alennuksen ja laskuttamattoman tuoton vastatilin tilejä tarpeen mukaan.
4. Luo laskuttamattoman tuoton ensimmäinen kirjauskansiomerkintä valitsemalla laskutusaikataulussa **Laskuttamattoman tuoton käsittely** -kohdassa **Luo kirjauskansiomerkintä**. Tämä vaihe on suoritettava ennen laskutusaikataulun laskutusta.
5. Kun ensimmäinen kirjauskansiomerkintä on luotu, luo myyntitilaukset ja kirjaa laskut laskutusaikatauluihin valitsemalla **Muodosta lasku**.
6. Kun laskut on kirjattu, voit tarkistaa kirjaustiedot **Kaikki laskutusaikataulut** -sivun **Uusinnat**-välilehdestä.

### <a name="milestone-billing"></a>Tavoitteisiin perustuva laskutus

Tavoitteisiin perustuva laskutus toimii laskuttamattoman tuoton kanssa seuraavien ehtojen mukaisesti:

- Jos tavoitteen päänimike on laskuttamaton (**Laskuttamaton tuotto** -valintaruutu on valittuna) ja tavoitteen alinimikkeet laskutetaan (**Laskuttamattoman tuoton** valintaruutu ei ole valittuna), päänimikkeen aloitus- ja päättymispäivät on määritettävä. Näitä päivämääriä käytetään alkuperäisen kirjauskansiomerkinnän luomiseen.
- Jos tavoitteen päänimike on laskuttamaton (**Laskuttamaton tuotto** -valintaruutu on tyhjennetty) ja tavoitteen alinimikkeet laskutetaan (**Laskuttamattoman tuoton** valintaruutu on valittuna), päänimikkeen päättymispäivä on määritettävä vain niille alinimikkeille, joille haluat luoda alkuperäisen kirjauskansioviennin.

Jokainen tavoitteen alinimike voidaan käsitellä erikseen. Päättymispäivät voidaan määrittää, kun olet valmis luomaan ensimmäisen kirjauskansiomerkinnän.

> [!NOTE]
> Jos tavoitteen pää- tai alinimikkeiden alkuperäinen kirjauskansiomerkintä on jo luotu tai lasku on luotu, alkamis- ja päättymispäivämääriä ei voi muokata.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Laskuttamaton tuotto ja tasapoiston lykkäykset

Jos haluat käyttää laskuttamatonta tuottoa tasapoiston lykkäysaikataulujen kanssa, noudata seuraavia ohjeita.

1. Luo **Kaikki laskutusaikataulut** -sivulla laskutusaikataulu.
2. Lisää nimike laskutusaikataulun riveille.
3. Valitse rivillä **Lykkäykset**.
4. Toimi **Tapahtuman lykkäys** -sivulla seuraavasti:

    1. Määritä **Lykätty**-asetukseksi **Kyllä**.
    2. Muuta tilejä tarpeen mukaan.
    3. Valitse **Aikataulu**-osassa **Tasapoisto** ja muokkaa muita arvoja tarpeen mukaan.
    4. Valitse **OK**.

5. Valitse riville **Laskuttamaton tuotto** ja noudata seuraavia ohjeita:

    1. Valitse **Laskuttamaton tuotto** -asetukseksi **Kyllä**.
    2. Valitse tuoton, alennuksen ja tuoton vastatilin tilit.

6. Valitse laskutusaikataulussa **Laskuttamattoman tuoton käsittely** -kohdasta **Luo kirjauskansiomerkintä**. Vaihtoehtoisesti voit luoda kirjauskansiomerkinnän käyttämällä **Laskuttamattoman tuoton joukkokäsittely** -sivua.
7. Lykkäysaikataulu luodaan. **Kaikki lykkäysaikataulut** -sivulla voit tarkistaa tiedot. Voit muokata laskutusaikataulun rivinimikkeen eri arvoja sen jälkeen, kun lykkäysaikataulu on luotu. Voit muokata esimerkiksi yksikköhintaa, määrää tai päivämääriä.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Laskuttamaton tuotto ja tapahtumapohjaiset lykkäykset

Jos haluat käyttää laskuttamatonta tuottoa tapahtumapohjaisten lykkäysaikataulujen kanssa, noudata seuraavia ohjeita.

1. Luo **Kaikki laskutusaikataulut** -sivulla laskutusaikataulu.
2. Lisää nimike laskutusaikataulun riveille.
3. Valitse rivillä **Lykkäykset**.
4. Toimi **Tapahtuman lykkäys** -sivulla seuraavasti:

    1. Määritä **Lykätty**-asetukseksi **Kyllä**.
    2. Muuta tilejä tarpeen mukaan.
    3. Valitse **Aikataulu**-osassa **Tapahtumaperusteinen**, **Malli**, **Kohdistustyyppi** ja **Erääntymistili**.
    4. Valitse **OK**.

5. Valitse riville **Laskuttamaton tuotto** ja noudata seuraavia ohjeita:

    - Valitse **Laskuttamaton tuotto** -asetukseksi **Kyllä**.
    - Valitse tuoton, alennuksen ja tuoton vastatilin tilit.

6. Valitse laskutusaikataulussa **Laskuttamattoman tuoton käsittely** -kohdasta **Luo kirjauskansiomerkintä**. Vaihtoehtoisesti voit luoda kirjauskansiomerkinnän käyttämällä **Laskuttamattoman tuoton joukkokäsittely** -sivua.
7. Lykkäysaikataulu luodaan. **Kaikki lykkäysaikataulut** -sivulla voit tarkistaa tiedot. Voit muokata laskutusaikataulun rivinimikkeen eri arvoja sen jälkeen, kun lykkäysaikataulu on luotu. Voit muokata esimerkiksi yksikköhintaa, määrää tai päivämääriä. Lykkäysaikataulu lasketaan uudelleen uusien arvojen perusteella.

Jakaumat lasketaan uudelleen valitun kohdistustyypin perusteella (**Prosentti**, **Valmistumisprosentti** tai **Yhtä suuret summat**). **Muuttuvat summat** -kohdistustyypille jakauma lasketaan uudelleen tapahtuman alkuperäisen arvon prosenttiosuuden perusteella. Alkuperäinen yksikköhinta on esimerkiksi 100,00 USD ja aloitusarvon prosenttiosuus 55,00 USD (55 prosenttia). Jos yksikköhinnaksi muutetaan 200,00 USD, tapahtuman muuttuvaksi summaksi tulee 110,00 USD (edelleen 55 prosenttia).

> [!NOTE]
> Jos on tunnistettu lykkäysaikataulurivejä, laskutusaikataulun rivinimikettä ei voi muokata. Jos haluat muokata rivinimikettä, sinun on ensin peruutettava tunnistetut rivit. Sitten laskutusaikataulun riviä voi päivittää.

### <a name="unbilled-revenue-and-top-billing"></a>Laskuttamaton tuotto ja ylimpien laskutus

Laskutussuunnitelma kirjataan kolmelle vuodelle, ja laskut laskutetaan vuosittain kolmen vuoden jaksolla. Koko sopimuksen summa kirjataan laskuttamattomalle tuottotilille, josta vuosittaiset laskut luodaan. Vastatili on tuottotili tai lykätty tuottotili.

Huomaa, että ylimpien laskutus ja laskuttamaton tuotto eivät toimi yhdessä, koska täsmäytysongelmia voi ilmetä kirjanpidossa. Esimerkiksi **Nimikeryhmän asetukset** -sivulla nimikeryhmä A määritetään niin, että **Ylimpien rivien määrä** -kentän arvoksi määritetään **2**. **Laskutusaikataulut**- sivulla on kolme nimikettä. Kaikki kolme nimikettä kuuluvat nimikeryhmään A. Kun laskuttamatonta tuottoa varten luodaan alkuperäinen kirjauskansion kirjaus, kaikkien kolmen nimikkeen summa käsitellään laskuttamattomalle tilille. Kun laskutusaikataulun lasku luodaan, vain kahden ylimmän nimikkeen summat sisällytetään. Näin ollen laskun summa ei vastaa laskuttamatonta tuottotiliä ja täsmäytysongelmia tapahtuu kirjanpidossa.

Jos haluat käyttää laskuttamatonta tuottoa, jätä **Nimikeryhmän asetus** -sivu tyhjäksi tai määritä kaikki nimikeryhmät niin, että **Ylimpien rivien määrä** -kentän arvoksi määritetään **0** (nolla). Jos haluat käyttää ylimpien laskutusta, laskuttamattoman tuoton toimintoja ei ole käytettävissä.

### <a name="examples"></a>Esimerkkejä

Versiosta 10.0.27 lähtien käytössä on uusi tili, jota käytetään, kun käytetään laskuttamatonta tuottoa. Kun ensimmäinen **Luo kirjauskansiovienti** -prosessi kirjataan, kredit merkitään uudelle laskuttamattoman tuoton vastatilille. Tätä tiliä käytetään tuottotilin asemesta, koska sama arvo on peruutettava, kun laskutusaikataulu laskutetaan. Jos vaihtokurssi- tai pyöristyseroja ilmenee, **Luo lasku** -prosessin aikana lasketut summat voivat olla erilaiset. Näin varmistetaan, että tilien nettosumma on 0 (nolla).

Tässä esimerkissä kerrotaan, kuinka laskuttamatonta tuottoa käytetään, kun sopimuksen koko summa taseessa tunnistetaan laskuttamattomaksi tuotoksi. Kirjauksen toinen puoli on laskuttamattoman tuoton vastakirjaus. Kun laskutat asiakasta, laskuttamaton tuotto ja laskuttamattoman tuoton vastakirjaus käännetään. Tuoton kirjaus tapahtuu joko laskutuksen yhteydessä tai määritetyn lykkäystunnistusaikataulun mukaan.

#### <a name="assumptions"></a>Oletustiedot

- Asiakas allekirjoittaa kuluvan vuoden tammikuun 1. päivänä kolmen vuoden sopimuksen arvolla 390 USD.
- Sopimus sisältää kaksi osaa: käyttöoikeudet ja ylläpitosopimuksen.
- Käyttöoikeusmaksun myyntihinta 300 USD ja asiakasta laskutetaan 100 USD 1.1. kunakin sopimusvuonna. 300 dollarin käyttöoikeusmaksu otetaan tuottona, kun sopimus allekirjoitetaan.
- Ylläpitomaksun myyntihinta 90 USD ja asiakasta laskutetaan 30 USD 1.1. kunakin sopimusvuonna. 90 dollarin ylläpitomaksu lykätään, ja 2,50 USD tuloutetaan sopimuksen joka kuukausi.
- Asiakasta laskutetaan 130 USD sopimuksen kunkin kolmen vuoden alussa (1. tammikuuta).

#### <a name="steps"></a>Vaiheet

1. Määritä kaksi vapautettua nimikettä laskuttamattomiksi nimikkeiksi. **Laskuttamattoman tuoton määritys** -sivulla voit määrittää nimikkeet ja tilit, jotka käyttävät laskuttamatonta tuottoa.
2. Tässä esimerkissä ylläpitomaksua lykätään. Nimike edellyttää lykkäysmallia, joka määritetään **Lykkäysmallit**-sivulla. Mallin **Kuukausittainen** kausiväli ja tuloutuskauden pituus on 36 kuukautta. Tämän vuoksi kuukausittainen tuotto on 2,50 USD.
3. Määritä **Oletusarvoisesti lykätty nimikkeet** -sivulla **Ylläpitomaksu**-kentän arvoksi **Lykättävä nimike**. Tämä vaihe ja seuraava vaihe aiheuttavat ylläpitomaksunimikkeen lykkäyksen, kun nimike myydään tai sisällytetään laskutusaikatauluun.
4. Valitse **Lykkäyksen oletusarvot** \> **Mallit** ja lisää nimike ylläpitomaksua ja vaiheen 2 tasapoistomallia varten. Ylläpitomaksun nimike linkitetään 36 kuukauden lykkäyssuunnitelmaan.
5. Luo laskutusaikataulu, joka sisältää kaksi laskuttamatonta nimikettä. Sopimuksen laskutusaikataulu määritetään seuraavin nimikkein.

    | Nimike | Aloituspäivämäärä | Päättymispäivämäärä | Määrä | Laskutustiheys | Lykkäysnimike | Laskuttamaton tuotto | Kuvaus |
    |---|---|---|---|---|---|---|---|
    | Käyttöoikeus | 01. tammikuuta, CY | 31. joulukuuta CY + 2 | 100,00 USD | Vuosittain | En | Kyllä | Asiakasta laskutetaan 100,00 USD vuosittain. Kokonaissumma 300,00 USD kirjataan ennakkoon laskuttamattomana tuottona taseessa ja tuottona voittoihin ja tappioihin. Jokainen lasku pienentää laskuttamatonta summaa. |
    | Ylläpito | 01. tammikuuta, CY | 31. joulukuuta CY + 2 | 30,00 USD | Vuosittain | Kyllä | Kyllä | Asiakasta laskutetaan 30,00 USD vuosittain. Kokonaissumma 90,00 USD kirjataan ennakkoon laskuttamattomana tuottona ja lykättynä tuottona taseessa. Jokainen lasku pienentää laskuttamatonta summaa. Lykätty tuotto kirjataan kuukausittain 36 kuukauden kuluessa. |

6. Käytä **Kaikki laskutusaikataulut** -sivulla **Luo kirjauskansionmerkintä** -prosessia, kun haluat kirjata sopimuksen arvon taseeseen laskuttamattomana tuottona.

Ohjelma luo kaksi kirjauskansiomerkintää, yhden jokaista laskutusaikataulun riviä varten.

| Laskuttamattoman tuoton tili | Laskuttamattoman tuoton vastatili | Veloitussumma | Luottosumma |
|---|---|---|---|
| Laskuttamattoman tuoton tili | | 300,00 USD | |
| | Laskuttamattoman tuoton vastatili | | 300,00 USD |

| Laskuttamattoman tuoton tili | Viivästetty tuotto | Veloitussumma | Luottosumma |
|---|---|---|---|
| Laskuttamattoman tuoton tili | | 90,00 USD | |
| |Lykätty ylläpidon tuotto | | 90,00 USD |

Ensimmäinen kirjauskansiomerkintä kirjataan laskuttamattoman tuoton vastatilille ja toinen kirjataan lykättyjen tuottojen tilille. Jos laskutusrivillä on sekä laskuttamaton että lykätty tuotto, käytetään lykättyjen tuottojen tiliä, ei laskuttamattoman tuoton vastatiliä. Sopimus edellyttää, että asiakkaan lasku luodaan kunkin vuoden alussa. Luo lasku **Luo lasku** -prosessia käyttämällä. Seuraavat kirjauskansiomerkinnät luodaan, kun lasku luodaan.

| Päätili | Laskuttamattoman tuoton tili | Veloitussumma | Luottosumma |
|---|---|---|---|
| Laskuttamattoman tuoton vastakirjaus | | 100,00 USD | |
| | Laskuttamattoman tuoton tili | | 100,00 USD |
| Myyntireskontra | | 100,00 USD | |
| | Tuottotili | | 100,00 USD |

| Päätili | Laskuttamattoman tuoton tili | Veloitussumma | Luottosumma |
|---|---|---|---|
| Lykätty ylläpidon tuottotili | | 30,00 USD | |
| | Laskuttamattoman tuoton tili | | 30,00 USD |
| Myyntireskontra | | 30,00 USD | |
| | Lykätty ylläpidon tuottotili | | 30,00 USD |

Tämä sama kirjauskansiomerkintä luodaan laskuilla, jotka kirjataan seuraavan kahden vuoden alussa. Lykättyjen tuottojen tilin nettosumma on 0 (nolla), koska pyöristys- tai vaihtokurssieroja ei ole. Lykätty tuotto on peruutettava samoin kuin se kredit-merkittiin **Luo kirjauskansiovienti** -prosessin aikana. Koska tuottoa lykätään edelleen ja se tuloutetaan myöhemmin, lykätyn tuoton tilille tulee kredit jälleen.

Viimeisessä vaiheessa tuloutuksen kirjauskansiovienti luodaan kuukausittain, jotta lykätty ylläpitomaksun tuotto tuloutetaan. Kirjauskansiomerkinnän voi luoda **Tuloutuksen käsittely** -sivua käyttäen. Voit luoda sen myös valitsemalla **Lykkäysaikataulu**-sivujen riveille **Tulouta**-vaihtoehdon.

| Lykätty tuottotili | Tuottotili | Veloitussumma | Luottosumma |
|---|---|---|---|
| Lykätty ylläpidon tuotto | | 2,50 USD | |
| | Ylläpidon tuotto | | 2,50 USD |

Tämä kirjauskansiomerkintä luodaan aina, kun tälle lykätylle nimikkeelle suoritetaan tuloutusprosessi (yhteensä 36 kertaa).

#### <a name="short-term-fixed-year"></a>Lyhytaikainen: Kiinteä vuosi

Voit käyttää laskuttamatonta tuottoa yhdessä lyhyen aikavälin toimintojen kanssa määrittämällä **Lyhytaikainen laskuttamaton** -kentän **Toistuvat sopimuksen laskutusparametrit** -sivulla. Seuraavassa esimerkissä esitetään laskutoimitukset, jotka tehdään, kun laskuttamatonta tuottoa käytetään yhdessä **kiinteän vuoden** lyhyen aikavälin laskuttamattoman menetelmän kanssa.

Ohjelma luo laskutusaikataulun, jolla on seuraavat ehdot:

- **Aloituspäivä:** 1. kesäkuuta 2020
- **Päättymispäivä:** 31. joulukuuta 2021
- **Yksikköhinta:** 100 USD
- **Tiheys:** Kuukausittain

**Kaikki laskutusaikataulut** -sivulla ensimmäinen kirjauskansiomerkintä luodaan **Luo kirjauskansiomerkintä** -prosessissa. Nykyiset lyhytaikaiset ja pitkäaikaiset summat lasketaan seuraavasti:

- **Nykyinen lyhytaikainen laskuttamaton tuoton summa:** 700 USD
- **Nykyinen pitkäaikainen laskuttamaton tuoton summa:** 1 200 USD

Lasku luodaan laskutuskaudella 1.6.2020 - 30.11.2020. Nykyiset lyhytaikaiset ja pitkäaikaiset summat lasketaan seuraavasti:

- **Nykyinen lyhytaikainen laskuttamaton tuoton summa:** 100 USD
- **Nykyinen pitkäaikainen laskuttamaton tuoton summa:** 1 200 USD

Lasku luodaan laskutuskaudella 1.12.2020 - 31.12.2020. Nykyiset lyhytaikaiset ja pitkäaikaiset summat lasketaan seuraavasti:

- **Nykyinen lyhytaikainen laskuttamaton tuoton summa:** 1 200 USD
- **Nykyinen pitkäaikainen laskuttamaton tuoton summa:** 0 USD

#### <a name="short-term-rolling-periods"></a>Lyhytaikainen: liukuvat kaudet

Voit käyttää laskuttamatonta tuottoa yhdessä lyhyen aikavälin toimintojen kanssa määrittämällä lyhytaikainen laskuttamaton -menetelmän **Toistuvat sopimuksen laskutusparametrit** -sivulla. Seuraavassa esimerkissä esitetään laskutoimitukset, jotka tehdään, kun laskuttamatonta tuottoa käytetään yhdessä **Liukuvat kaudet** lyhyen aikavälin laskuttamattoman menetelmän kanssa.

Ohjelma luo laskutusaikataulun, jolla on seuraavat ehdot:

- **Aloituspäivä:** 1. kesäkuuta 2020
- **Päättymispäivä:** 31. joulukuuta 2021
- **Yksikköhinta:** 100 USD
- **Tiheys:** Kuukausittain

**Kaikki laskutusaikataulut** -sivulla ensimmäinen kirjauskansiomerkintä luodaan **Luo kirjauskansiomerkintä** -prosessissa. Nykyiset lyhytaikaiset ja pitkäaikaiset summat lasketaan seuraavasti:

- **Nykyinen lyhytaikainen laskuttamaton tuoton summa:** 1 200 USD
- **Nykyinen pitkäaikainen laskuttamaton tuoton summa:** 700 USD

Lasku luodaan laskutuskaudella 1.6.2020 - 30.11.2020. Nykyiset lyhytaikaiset ja pitkäaikaiset summat lasketaan seuraavasti:

- **Nykyinen lyhytaikainen laskuttamaton tuoton summa:** 1 200 USD
- **Nykyinen pitkäaikainen laskuttamaton tuoton summa:** 100 USD

Lasku luodaan laskutuskaudella 1.12.2020 - 31.12.2020. Nykyiset lyhytaikaiset ja pitkäaikaiset summat lasketaan seuraavasti:

- **Nykyinen lyhytaikainen laskuttamaton tuoton summa:** 1 200 USD
- **Nykyinen pitkäaikainen laskuttamaton tuoton summa:** 0 USD

### <a name="items-with-revenue-allocation"></a>Nimikkeet, joilla on tuottojen kohdistus

Laskuaikatauluun lisätään kaksi nimikettä, joissa on eri laskutustiheydet. Molemmat käyttävät laskuttamatonta tuottoa ja ovat lykättäviä nimikkeitä.

- **Nimiketunnus 1000:** Surface Pro 128 Gt

    - **Laskutustiheys:** Kertalaskutus
    - **Yksikköhinta:** 1 500 USD
    - **Erillismyyntihinta:** 1 600 USD
    - **Sopimuksen tuotto:** 1 465,26 USD

- **Nimiketunnus S0021:** Vakuutus, joka myydään yhdessä nimiketunnuksen 1000 kanssa.

    - **Laskutustiheys:** kuukausittain 12 kuukauden ajan
    - **Yksikköhinta:** 20 USD kuukaudessa
    - **Erillismyyntihinta:** 25 USD
    - **Sopimuksen tuotto:** 264,74 USD

Koska molemmat nimikkeet käyttävät laskuttamatonta tuottoa ja tuottojen kohdistusta, sopimuksen kokonaissumma uusimisrivillä on 0 (nolla). **Sopimuksen tuotto** -sarake lisätään ja näyttää sopimuksen tuoton summan.

Seuraavassa taulukossa on nimikkeiden ja laskun alkuperäinen kirjauskansiomerkintä.

| Laskuttamattoman tuoton tili | Lykätty tuottotili | Veloitussumma | Luottosumma |
|---|---|---|---|
| **Nimikkeen 1000 kirjauskansiovienti** | | | |
| Debit – laskuttamattoman tuoton tili (401250) | | 1 465,26 USD | |
| | Kredit – Lykätty tuottotili (250600) | | 1 465,26 USD |
| **Nimikkeen 0021 kirjauskansiovienti** | | | |
| Debit – laskuttamattoman tuoton tili (401250) | | 274,74 USD | |
| | Kredit – Lykätty tuottotili (250600) | | 274,74 USD |
| **Lasku** | | | |
| | Kredit – Laskuttamattoman tuoton tili | | 1 465,26 USD |
| | Kredit – Laskuttamattoman tuoton tili | | 274,74 USD |
| Debet – Myyntireskontratili (130100) | | 1 488,16 USD | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Laskutusaikataulun rivin, laskutustietojen rivin tai tuoton kohdistuksen muutokset

Kun yksikköhintaa tai määrää muutetaan, tuoton sopimussumma on päivitettävä jokaisen sellaisen nimikkeen osalta, joka kuuluu tuoton kohdistukseen. Siksi kirjauskansiovienti lasketaan uudelleen.

Esimerkiksi nimikkeen 1000 yksikköhinta muutetaan arvosta 1 500 USD arvoon 1 600 USD. Tällöin sopimuksen tuoton summa lasketaan automaattisesti uudelleen arvona 1 549,47 USD. Nimikkeen S0021 sopimustuotto lasketaan uudelleen arvona 290,53 USD.

Kun muutos on vahvistettu ja sidottu, molempien nimikkeiden alkuperäiset kirjauskansiomerkinnät palautetaan ja uudet kirjauskansiomerkinnät luodaan:

- **Nimike 1000:** Alkuperäisen kirjauskansiomerkinnän 1 465,26 USD peruutetaan. Uusi kirjauskansiovienti 1 549,47 USD luodaan.
- **Nimike S0021:** Alkuperäisen kirjauskansiomerkinnän 274,74 USD peruutetaan. Uusi kirjauskansiovienti 290,53 USD luodaan.

#### <a name="termination"></a>Irtisanominen

Nimikkeen S0021 aloituspäivä on tammikuussa 2020 ja päättymispäivä joulukuussa 2020, mutta sen voimassaolo päättyy kesäkuussa 2020. Molempien nimikkeiden sopimustuottosumma on laskettava uudelleen:

- **Nimike 1000:** sopimustuotto lasketaan uudelleen arvona 1 567,67 USD.
- **Nimike S0021:** sopimustuotto lasketaan uudelleen arvona 124,00 USD.

Päätettävälle riville luodaan oikaisukirjauskansiomerkintä. Samaan usean elementin järjestelyyn (MEA) kuuluvan rivin kirjauskansiomerkintä peruutetaan, ja järjestelmä luo uuden kirjauskansiomerkinnän:

- **Nimike 1000:** Alkuperäisen kirjauskansiomerkinnän 1 465,26 USD peruutetaan. Oikaisukirjauskansiovienti 1 549,47 USD luodaan.
- **Nimike S0021:** Alkuperäisen kirjauskansiomerkinnän 274,74 USD peruutetaan. Uusi kirjauskansiovienti 124,00 USD luodaan.
