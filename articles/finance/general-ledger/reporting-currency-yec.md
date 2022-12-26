---
title: Raportointivaluutta ei täsmää, kun tilikauden lopetus suoritetaan
description: Tässä artikkelissa käsitellään sitä, että raportointivaluutta ei täsmää, kun tilikauden lopetus suoritetaan.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850258"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Raportointivaluutta ei täsmää, kun tilikauden lopetus suoritetaan

Kun **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuus (**Tietoja**-ominaisuus) on otettu käyttöön, selvitettyjä kirjanpitotapahtumia ei enää sisällytetä seuraavan tilikauden alkusaldoon kirjanpidon tilikauden lopetusta suoritettaessa. Selvitettyjen kirjanpitotapahtumien poisjättäminen voi aiheuttaa haasteita asiakkaille tilikautta lopetettaessa, jos kirjanpitoon on määritetty raportointivaluutta.

Tapahtuman selvitys tehdään vain kirjanpidon valuuttaa varten. Kun kirjanpitotapahtumat selvitetään, tarkistus vahvistaa, että kirjanpidon valuutan debetit vastaavat kirjanpidon valuutan kreditejä. Kyseisten kirjanpitotapahtumien raportointivaluuttasummia ei tarkisteta, eivätkä debetit välttämällä vastaa niiden kreditejä. Tapahtuman tilitys ei myöskään automaattisesti laske ja kirjaa voittoa/tappiota raportointivaluuttana.

Näiden rajoitusten vuoksi voitto/tappio-tapahtuman on oltava raportointivaluuttana, kun tapahtuma selvitetään. Jos voitto/tappio ei sisälly tapahtuman selvitykseen, täsmäämättömyysanoma näytetään, kun tilikauden lopetus suoritetaan.

Seuraavassa esimerkissä käsitellään tämän ongelman ratkaisemista ennen tilikauden lopetuksen suorittamista.

## <a name="example-setup"></a>Esimerkkimääritykset

Tämän esimerkin määrityksiä varten **Tietoja**-ominaisuus on otettava käyttöön ja tapahtuman selvityksen päätiliksi määritetään 110180. Seuraavassa kuvassa näkyy DEMF-yrityksessä kirjatut kirjanpitotapahtumat. DEMF-yrityksen kirjanpidon valuutta on Yhdysvaltain dollari (USD) ja raportointivaluutta on euro (EUR).

![Raportointivaluuttana kirjatut kirjanpitotapahtumat](./media/reporting-currency-1.png)

**Tapahtuman selvitykset** -sivulla on päätilin 110180 kirjanpitotapahtumat. Valitse se ja pidä valittuna (tai valitse hiiren kakkospainikkeella) ruudukossa ja valitse sitten **Lisää sarakkeita**. Lisää **Summa raportointivaluuttana** -sarake, sillä näin summat näkyvät tapahtuman valuuttana, kirjanpidon valuuttana ja raportointivaluuttana.

![Raportointivaluuttasarakkeen summa on lisätty Tapahtuman selvitykset -sivulle](./media/Ledger-settlement2.png)

Kaksi ensimmäistä 100,00 EUR:n kirjanpitotapahtumaa on selvitetty yhtenä ryhmänä ja seuraavat kaksi 200,00 EUR:n kirjanpitotapahtumaa on selvitetty toisena ryhmänä. (Kahdella tapahtumalla on eri selvitystunnukset.) Tämä määritys osoittaa, että organisaatioilla on useita kirjanpitotapahtumaryhmiä, jotka selvitetään eri aikoina ja joilla on eri selvityspäivä. Kun selvitys on valmis **Tapahtuman selvitykset** -sivulla näkyy seuraavat tiedot, kun se on suodatettu näyttämään tapahtumat, joiden tila on **Selvitetty**.

![Selvitetyt tapahtumat Tapahtuman selvitykset -sivulla](./media/Settled-trans-filtered3.png)

Valitse **Summa**-sarake **Tapahtuman selvitykset** -sivulla ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten **Tämä sarake yhteensä**. Toista tämä vaihe **Summa raportointivaluuttana** -sarakkeiden osalta. Kirjanpidon valtuutan eron on oltava 0 (nolla), jotta selvitys voi tapahtua. Raportointivaluutan selvityssummaa ei kuitenkaan tarkisteta. Seuraavassa kuvassa raportointivaluutan ero on -27,79 USD.

![Raportointivaluutan ero](./media/Difference4.png)

## <a name="year-end-close"></a>Tilinpäätös

Jos tilinpäätöksen lopetus suoritetaan nyt vuodelle 2022, prosessi päättyy täsmäämättömyysvirheeseen Tämä virheen aiheutuu suoraan siitä, että raportointivaluutan tapahtuman selvityssumma ei ole 0 (nolla).

![Virhesanoma ilmaisee, että tapahtuman selvityssumma ei ole 0 (nolla)](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Raportointivaluutan voiton/tappion kirjaaminen

Tilikauden lopetuksen onnistunut suorittaminen edellyttää, että raportointivaluutan summan ero on otettava huomioon ja sisällytettävä tapahtuman selvitykseen. Yleensä ero käsitellään voittona tai tappiona. Raportointivaluutan voiton/tappion voi kirjata useilla eri tavoilla:

- Jos päätili on osto- tai myyntireskontra, kyseisten asiakirjojen osto- ja myyntireskontratilitys luo tarvittavan voiton/tappion. Kyseinen kirjanpitomerkintä on sisällytettävä tapahtuman selvitykseen, kun vastaavat kirjanpitotapahtumat selvitetään esimerkiksi laskusta, maksuista tai hyvityslaskuista.
- Jos päätili on jokin muu tili kuin osto- tai myyntireskontra, voitto/tappio on annettava manuaalisesti. Kun voitto/tappio kirjataan, organisaatio määrittää, kuinka tarkka kirjanpitomerkintä on.
- Kunkin päätilin osalta on määritettävä raportointivaluutan voitto/tappio, joka on kirjattava.

Kuten aiemmin mainittiin, tämä kirjaus voidaan tehdä **Tapahtuman selvitykset** -sivulla.

1. Suodata päivämääräalue, jonka voitto/tappio halutaan kirjata. Jos voitto/tappio on tarkoitus kirjata kuukausittain, suodata kukin kuukausi. Jos voitto/tappio on tarkoitus kirjat tilikausittain, suodata koko vuosi.
2. Suodata päätili.
3. Suodata tila siten, että vain **selvitetyt** tapahtumat näkyvät.
4. Lisää summa **Summa raportointivaluuttana** -sarakkeessa.
5. Jos voitto/tappio halutaan kirjata eritellymmin, lisäsuodatus voidaan tehdä esimerkiksi selvitystunnuksen tai taloushallinnon dimensioiden perusteella. **Summa raportointivaluuttana** -sarakkeen kokonaissumma ilmaisee summan, joka kirjataan voitoksi/tappioksi.
6. Valitse **Kirjanpito \> Kirjauskansioviennit \> Raportointivaluutan muutosten kirjauskansiot**.
7. Syötä voiton/tappion tapahtuma. Tämä kirjauskansio kirjaa muutoksen vain raportointivaluuttana. Kirjattujen tapahtuman valuutan ja kirjanpidon valuutan summat ovat aina 0 (nolla). Jos tätä kirjauskansiota ei ole käytetty aiemmin, on ehkä luotava kirjauskansio, jonka kirjauskansiotyyppi on **Raportointivaluutan muutos**. Tämä tehdään valitsemalla **Kirjanpito \> Kirjauskansion asetukset \> Kirjauskansioiden nimet**.
8. Jos päätili ei salli manuaalista määritystä, tätä muutosta ei voi kirjata. Tämän vuoksi **Älä salli manuaalista määritystä** -parametri on ehkä poistettava väliaikaisesti käytöstä **Päätili**-sivulla.

![Manuaalinen määritys Kirjaustosite-sivulla](./media/Manual-entry6.png)

Kun oikaisukirjauskansio on kirjattu, palaa **Tapahtuman selvitykset** -sivulle ja valitse päätilin, johon voitto/tappio kirjattiin. Voitto/tappio-oikaisu on sisällytettävä tapahtuman selvitykseen. Koska raportointivaluutan summa ei tarvitse olla 0 (nolla), aiempien tapahtumien selvitys voidaan kumota ja selvittää sitten uudelleen voitto/tappio sisällytettynä. Voiton/tappion kirjauksen ja kyseisen voiton/tappion selvityksen tarkkuus tapahtuman selvityksessä on organisaation päätettävissä.

Seuraavassa kuvassa 200 EUR:n tapahtumien selvitys kumottiin ja merkittiin sitten uudelleen selvitettäväksi. Tällä kertaa ne sisältävät voitto/tappio-oikaisun.

![Voitto/tappio-oikaisu Tapahtuman selvitykset -sivulla](./media/gain-loss7.png)

Muuta **Tila**-suodatinta tapahtumien selvityksen jälkeen siten, että **Selvitetyt** tapahtumat näkyvät sivulla. **Summa raportointivaluuttana** -sarakkeen summa on nyt 0 (nolla). Tilikauden lopetuksen suorittaminen onnistuu nyt.

![Onnistunut tilikauden lopetus](./media/Zero-settled8.png)
