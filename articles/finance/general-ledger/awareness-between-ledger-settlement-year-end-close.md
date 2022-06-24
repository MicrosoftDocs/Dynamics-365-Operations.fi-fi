---
title: Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä
description: Tässä artikkelissa on tietoja parannuksista, jotka vaikuttavat kirjanpidon selvityksiin ja kirjanpidon vuoden lopun sulkemiseen.
author: kweekley
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 30d3cc0bbd97cd006f12d06cda64ee63cb42252e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902513"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä

[!include [banner](../includes/banner.md)]


Microsoft Dynamics 365 Finance -versiossa 10.0.25 **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuus on käytettävissä **ominaisuuden hallinnan** työtilassa. Tämä ominaisuus lisää kaksi ensisijaista parannusta, jotka vaikuttavat kirjanpidon tilitykseen ja kirjanpidon vuoden lopun sulkemiseen.

Kirjanpidon vuoden loppua suljettaessa tilitettyjä kirjanpitotapahtumia ei enää sisällytetä seuraavan tilikauden alkusaldoon. Tämä parannus varmistaa, että vain tilittämättömät kirjanpitotapahtumat sisällytetään alkusaldoon. Tämä on tärkeää, kun kirjanpidon ulkomaanvaluutan uudelleenarvostus suoritetaan. Ulkomaan valuutan uudelleenarvostus suoritetaan vain kirjanpitotapahtumille, joiden tila on **Ei selvitetty**. Ennen kuin **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuus julkaistiin, alkusaldoon tehtiin yhteenveto sekä tapahtumista, joiden tila on **Selvitetty**, että tapahtumista, joiden tila on **Ei selvitetty**, ja yhteenvetosumman tilaksi oli määritetty **Ei selvitetty**.

Toisen parannuksen ansiosta voit kirjata yksityiskohtaiset alkusaldotapahtumat kirjanpidon vuoden lopun sulkemisen aikana. Jos **Säilytä tiedot tilinpäätöksen aikana** -asetuksena on **Kyllä**, kullekin tilittämättömälle kirjanpitotapahtumalle luodaan erillinen alkusaldo. Tämä asetus määritetään kirjanpidon selvitysasetuksissa jokaiselle päätilille. Kun avaussaldoa varten pidetään yksityiskohtaiset tapahtumat, parannetaan kykyä selvittää seuraavan tilikauden selvittämättömät kirjanpitotapahtumat.

Kirjanpidon tilitykseen ja vuoden lopun sulkemiseen tehtiin muutoksia uusien parannusten tueksi.

### <a name="changes-to-ledger-settlement"></a>Muutokset kirjanpidon selvitykseen

- Kirjanpidon tilitys on tehtävä tilivuoden aikana.
- Kirjanpidon tilitys on tehtävä yhden päätilin tapahtumille. Päätili on nyt pakollinen suodatin **Kirjanpidon tilitys** -sivulla.
- Tapahtuman selvitystä ja tapahtuman selvityksen peruuttamista ei voi tehdä suljetulle tilivuodelle kirjatuille tapahtumille (kun vuoden sulkeminen on siis suoritettu).

### <a name="changes-to-year-end-close"></a>Muutokset vuoden lopun sulkemiseen

- Vuoden lopun sulkemista ei voi palauttaa, jos jokin alkusaldotapahtuma on selvitetty seuraavalla tilikaudella. Muutos koskee vuoden lopun sulkemisen peruuttamista tai kun vuoden lopun sulkeminen suoritetaan uudelleen ja **Poista tilivuoden päätöksen tapahtumat kun tilivuosi suljetaan** -asetus on **Kyllä** kirjanpidon parametreissa.
- Jos **Säilytä tiedot tilinpäätöksen aikana** -asetuksena on **Kyllä** mille tahansa kirjanpidon täsmäytyksen tasetilille, ohjelma luo yksityiskohtaisempia alkusaldotapahtumia kyseiselle päätilille.

## <a name="before-you-enable-the-feature"></a>Ennen toiminnon käyttöönottamista

Toimintojen ja tietomallin muutosten vuoksi on tärkeää ottaa huomioon seuraavat seikat, ennen kuin otat ominaisuuden käyttöön:

- Koska vain selvitettyjä tapahtumia tuodaan eteenpäin alkusaldoon, tilivuoden tapahtumat on tilitetty edellisen tilikauden tapahtumien kanssa. Tapahtumat tulee kuitata kuluvan tilikauden tapahtumia vastaan. Tämä voidaan tehdä tekemällä oikaisukirjaus kuluvalle tilikaudelle. Oikaisu palauttaa yhteenvedon alkusaldoista ja vastakirjauksista yksityiskohtaisilla tapahtumilla, jotka ovat tarpeen kuluvan vuoden kirjanpitomerkintöjen selvittämiseen. 

  > [!IMPORTANT]
  > Jos näin ei tehdä, saat **väärä saldo** -virheen, kun suoritat tilivuoden vuoden lopun. Jos kirjanpitotapahtumia, joilla on sama tilivuosi, ei ole mahdollista poistaa käytöstä ja palauttaa, älä ota tätä toimintoa käyttöön, ennen kuin vuoden sulkeminen on valmis. Ota toiminto käyttöön heti vuoden lopun sulkemisen jälkeen ja ennen kuin seuraavan tilikauden uudet kirjanpitotapahtumat selvitetään. 
  
- Kaikista tilitykseen merkityistä tapahtumista, joita ei ole vielä selvitetty, poistetaan merkintä automaattisesti, kun ominaisuus otetaan käyttöön. Voit estää työn menettämisen selvittämällä kaikki merkityt tapahtumat, ennen kuin otat ominaisuuden käyttöön.
- Osa organisaatioista suorittaa vuoden lopun sulkemisen useita kertoja saman tilivuoden osalta. Älä ota toimintoa käyttöön, jos vuoden sulkeminen on jo kerran suoritettu ja suoritetaan uudelleen samalle tilivuodelle. Ominaisuus on otettava käyttöön ennen ensimmäistä vuoden sulkemista tai tilivuoden viimeisen vuoden sulkemisen suorituksen jälkeen.

  Jos haluat ottaa toiminnon käyttöön, mutta vuoden sulkeminen on jo kerran suoritettu, vuoden sulkeminen on peruutettava, ennen kuin ominaisuus voidaan ottaa käyttöön.

- Koska päätilien välinen selvitys ei ole enää sallittua, oikaise tilikartta tai prosessit tarpeen mukaan ja varmista, että kirjanpidon tilitys voidaan tehdä samalla päätilillä.
- Toimintoa ei voi ottaa käyttöön, jos käytössä on julkisen sektorin vuoden sulkemisprosessi.

## <a name="set-up-ledger-settlement"></a>Määritä kirjanpidon tilitys

Kun ominaisuus on otettu käyttöön ja ennen seuraavan vuoden sulkemisen suorittamista kunkin organisaation on määritettävä, säilytetäänkö tapahtumatiedot vuoden lopun sulkemisen aikana. Valinnalla ei ole vaikutusta edellisen vuoden sulkemisprosessien saldon alkukirjauksiin.

**Säilytä tiedot tilinpäätöksen aikana** -asetus määritetään kunkin päätilin osalta **Kirjanpidon tilitys** -asetussivulla.

1.  Valitse **Kirjanpito** > **Kirjanpidon asetukset** > **Kirjanpitoparametrit**.
2.  Valitse **Kirjanpidon tilitykset** -välilehdessä **Kirjanpidon tilitystilit**.

-tai-

1.  Valitse **Kirjanpito** > **Kausittaiset tehtävät** > **Tapahtuman selvitykset**.
2.  Valitse **Kirjanpidon tilitystilit**.

**Kirjanpidon tilitykset** -sivulle on lisätty kaksi saraketta:
    
- **Päätilityyppi** – Tämä sarake on vain tiedoksi. Se ilmaisee päätilille määritetyn tyypin.
- **Säilytä tiedot tilinpäätöksen aikana** – Oletusarvon mukaan asetuksena on **Ei**. Sen arvoksi voidaan määrittää **Kyllä** vain, jos **Päätilityyppi**-sarakkeen arvona on **Tase**, **Käyttöomaisuus** tai **Velka**. Kun asetus on **Ei**, alkusaldot kirjataan yhteenvetona, kuten tavallisesti vuoden lopun sulkemisissa. Jos arvoksi on määritetty **Kyllä**, alkusaldot luodaan yksityiskohtaisesti jokaiselle kirjanpitotapahtumalle, jota ei ole selvitetty päätiliä varten.

## <a name="year-end-close"></a>Tilinpäätös

Kun suoritat vuoden lopun sulkemisen kohdassa **Kirjanpito** > **Kauden sulkeminen** > **Tilinpäätös**, prosessi luo kirjanpidon tilitykseen määritettyjen päätilien alkusaldot. Alkusaldot luodaan kirjanpidon tilitysasetusten mukaan joko yhteenvetona tai yksityiskohtaisesti. Prosessi sulkee pois kirjanpitotapahtumat, jotka on tilitetty, riippumatta siitä, kirjataanko kunkin päätilin alkusaldo yhteenvetona vai yksityiskohtaisesti.

Esimerkiksi päätilille 130100 kirjataan useita tapahtumia tilikaudella 2021.

| Kirjauskansion numero | Tosite  | Päivämäärä       | Tyyppi      | Kirjanpitotili | Tilin nimi        | Kuvaus       | Valuutta | Summa tapahtuman valuuttana | Summa  | Summa raportointivaluuttana |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 12/3/2021  | Käytössä | 130100-001-    | Myyntireskontra | Palvelumaksu       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 12/5/2021  | Käytössä | 130100-002-    | Myyntireskontra | Työkalut         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 12/16/2021 | Käytössä | 130100-001-    | Myyntireskontra | Hyvitys            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 12/20/2021 | Käytössä | 130100-002-    | Myyntireskontra |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 12/20/2021 | Käytössä | 130100-002-    | Myyntireskontra |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 12/21/2021 | Käytössä | 130100-002-    | Myyntireskontra | Tilin kredit | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 12/28/2021 | Käytössä | 130100-001-    | Myyntireskontra | Työkalut         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 12/29/2021 | Käytössä | 130100-002-    | Myyntireskontra | Palvelu           | USD      | 300                            | 300     | 300                          |

Näistä tapahtumista kolme selvitetään tapahtumien selvityksen aikana.

Lasku on 175 dollaria (175 USD). Tämä lasku maksettiin euroina (EUR) ja käteisalennus tehtiin.

| Kirjauskansion numero | Tosite  | Päivämäärä       | Tyyppi      | Kirjanpitotili | Tilin nimi        | Kuvaus | Valuutta | Summa tapahtuman valuuttana | Summa  | Summa raportointivaluuttana |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 12/5/2021  | Käytössä | 130100-002-    | Myyntireskontra | Työkalut   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 12/20/2021 | Käytössä | 130100-002-    | Myyntireskontra |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 12/20/2021 | Käytössä | 130100-002-    | Myyntireskontra |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Päätilin 130100 tulokset riippuvat siitä, onko toiminto käytössä ennen vuoden lopun sulkemista. Jos ominaisuus on käytössä, tulos määräytyy myös Säilytä tiedot tilinpäätöksen aikana -asetuksen mukaan.

### <a name="the-feature-isnt-enabled"></a>Toiminto ei ole käytössä
Vuoden lopun sulkeminen luo kolme alkusaldotapahtumaa päätilille 130100 vuonna 2022. Tapahtumien summa kirjanpitovaluuttana on 525 USD.

| Kirjauskansion numero | Tosite  | Päivämäärä     | Tyyppi    | Kirjanpitotili | Tilin nimi        | Kuvaus | Valuutta | Summa tapahtuman valuuttana | Summa  | Summa raportointivaluuttana |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-002-    | Myyntireskontra |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-001-    | Myyntireskontra |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-002-    | Myyntireskontra |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Vaikka maksun -127,11 euron tapahtuma selvitettiin kirjanpitoon, tapahtuma tulee siitä eteenpäin alkusaldona.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Ominaisuus on käytössä ja Säilytä tiedot tilinpäätöksen aikana = Ei

Vuoden lopun sulkeminen luo kaksi alkusaldotapahtumaa päätilille 130100 vuonna 2022. Tapahtumien summa kirjanpitovaluuttana on edelleen 525 USD, mutta kirjanpitoon täsmäytettyjä tapahtumia ei sisällytetä alkusaldoon. Tilin 130100-002 kokonaissumma on 125 USD eikä 299,12 USD, ja tapahtuma 127,11 EUR/174,12 USD suljetaan kokonaan pois.

| Kirjauskansion numero | Tosite  | Päivämäärä     | Tyyppi    | Kirjanpitotili | Tilin nimi        | Kuvaus | Valuutta | Summa tapahtuman valuuttana | Summa | Summa raportointivaluuttana |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-002-    | Myyntireskontra |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-001-    | Myyntireskontra |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Ominaisuus on käytössä ja Säilytä tiedot tilinpäätöksen aikana = Kyllä

Vuoden lopun sulkeminen luo viisi alkusaldotapahtumaa päätilille 130100 vuonna 2022. Ohjelma luo erillisen alkusaldotapahtuman kullekin viidestä tapahtumasta, joita ei ollut selvitetty. Tapahtumien summa kirjanpitovaluuttana on edelleen 525 USD.

| Kirjauskansion numero | Tosite  | Päivämäärä     | Tyyppi    | Kirjanpitotili | Tilin nimi        | Kuvaus       | Valuutta | Summa tapahtuman valuuttana | Summa | Summa raportointivaluuttana |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-001-    | Myyntireskontra | Palvelumaksu       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-001-    | Myyntireskontra | Hyvitys            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-002-    | Myyntireskontra | Tilin kredit | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-001-    | Myyntireskontra | Työkalut         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1.1.2022 | Avaaminen | 130100-002-    | Myyntireskontra | Palvelu           | USD      | 300                            | 300    | 300                          |

Kun tapahtumatiedot säilytetään, ei ole vaikutusta alkuperäisiin yksityiskohtaisiin tapahtumiin. Ne jäävät kirjatuiksi ja selvittämättömiksi suljettavalla tilikaudella. Kopio näistä tapahtumista luodaan alkusaldoa varten. Seuraavat arvot alkuperäisistä tapahtumista kopioidaan avaussaldon tapahtumiin.

- Kirjanpitotili (päätili ja kaikki taloushallinnon dimensiot)
- Summat tapahtuma-, kirjanpito- ja raportointivaluuttana
- Kuvaus
- Kirjanpitotaso
- Kirjaustyyppi

   > [!NOTE]
   > Kirjaustyypille ei ole määritetty muita alkusaldotapahtumia. Kirjaustyyppiä voidaan siten käyttää erottelemaan avaustapahtumat, jotka vietiin eteenpäin yksityiskohtaisesti.

Joidenkin alkuperäisten tapahtumien kenttien on muututtava alkusaldon yksityiskohtaisissa tapahtumissa. Alkusaldotapahtumien päivämäärä on aina seuraavan tilikauden ensimmäinen päivä. Kirjauskansion numeron on muututtava ja tositenumero muuttuu vuoden lopun sulkemisvalintaikkunassa annettuun arvoon.

Alkuperäisten tapahtumien tiedot ovat **Kirjanpidon tilitys** -sivulla. Jokaisessa yksityiskohtaisessa alkusaldotapahtumassa näkyy ruudukon **Alkuperäinen tapahtumapäivämäärä** -sarake. Tämän sarakkeen avulla voit täsmätä uuden tilikauden tapahtumia. Voit porautua alkuperäiseen tositteeseen valitsemalla **Näytä alkuperäinen tosite**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Selvitä tapahtumat
Voit selvittää kirjanpitotapahtumia seuraavien ohjeiden avulla.

1. Valitse **Kirjanpito** > **Kausittaiset tehtävät** > **Tapahtuman selvitykset**.
2.  Määritä sivun yläosassa olevat suodattimet.

    1. Valitse päivämääräväli. Valitse vaihtoehtoisesti päivämääräaluekoodi täyttääksesi automaattisesti päivämäärävälin.

       - Päivämääräalue ei voi ylittää tilikausia. Jos päivämääräväli ylittää tilivuodet, **Näytä tapahtumat** -kohtaa valitessa ei näytetä tapahtumia.
       - Jos päivämääräalue on avoimena tilivuotena, tapahtumat voidaan selvittää ja selvitys voidaan palauttaa. Jos päivämääräalue on suljetussa tilivuodessa tai jos vuoden sulkeminen on valmis, tapahtumat näytetään, mutta niitä ei voi selvittää tai peruuttaa selvitystä. Voit poistaa tapahtumien merkitsemisen vain suljetulla tilikaudella. Jos päivämääräalue on suljetussa tilivuodessa, **Merkitse valitut**- **Selvitä merkityt tapahtumat**- ja **Palauta merkityt tapahtumat** -painikkeet eivät ole käytettävissä.

    2. Valitse päätili, jonka tapahtumia näytetään. Tämä kenttä on pakollinen. Haku näyttää vain päätilit, jotka on valittu yrityksen tilikartan **Kirjanpidon tilitys** -sivulla.
    3. Valitse kirjaustaso. Et voi selvittää tapahtumia, jotka ovat eri kirjaustasoilla.
    4. Jos haluat näyttää päätiliin ja dimensiot erillisissä sarakkeissa, valitse taloushallinnon dimensioyhdistelmä.

3.  Valitse **Näytä tapahtumat**, jos haluat näyttää kaikki määritettyjä suodattimia vastaavat tapahtumat. Jos muutat suodattimia tai dimensioyhdistelmiä, sinun on valittava uudelleen **Näytä tapahtumat**.
4.  Valitse rivit tilitykseen. Sivun yläosassa olevan **Valittu summa** -kentän arvo suurenee tai pienenee valittujen rivien kokonaissumman mukaan.
5.  Kun olet valinnut tapahtumat, valitse **Merkitse valitut**. Kunkin valitun tapahtuman **Merkitty**-sarakkeeseen tulee valintamerkki. Lisäksi ruudukon yläpuolella olevan **Merkitty summa** -kentän arvo suurenee tai pienenee merkittyjen rivien kokonaissumman mukaan.
6.  Kun **Merkitty summa** -kentän arvo on **0** (nolla), valitse **Selvitä merkityt tapahtumat**.

    - Osittaista selvitystä ei sallita. Et esimerkiksi voi selvittää 100 dollarin debet-tapahtumaa 90 dollarin kredit-tapahtumaa vastaan. Jäljellä oleva 10 dollaria on myös merkittävä sisällytettäväksi tilitykseen.
    - Määritä selvityspäivä. Päivämäärän on oltava selvitykseen merkittyjen tapahtumien viimeinen päivä tai viimeisen päivämäärän jälkeen.

Merkittyjen tapahtumien tilaksi päivitetään **Selvitetty**.

> [!IMPORTANT]
> Kaikki aktiiviseen yritykseen täsmäytykseen merkityt tapahtumat selvitetään. Valittu päätili selvitetään. Tapahtumien ei tarvitse näkyä sivulla. Ne selvitetään, vaikka ne olisikin piilotettu suodattimen vuoksi.

Jotkin prosessit, kuten tapahtuman peruuttaminen, tilittää kirjanpitotapahtumat automaattisesti. Maksu ja lasku esimerkiksi selvitetään myyntireskontrassa, ja tilitys luo realisoituneen voiton/tappion. Maksun ja laskun selvitys ei selvitä kirjanpitotapahtumia, kuten myyntireskontran kirjanpitotilin tapahtumia. Jos maksu ja lasku on kuitenkin selvittämättömiä myyntireskontrassa, myyntireskontran selvityksen peruutuksen yhteydessä kirjattu kirjanpidon peruutus aiheuttaa sen, että alkuperäiset kirjanpitomerkinnät ja peruuttavat kirjanpitotapahtumat täsmäytetään kirjanpitoon. Kun **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuus on käytössä, peruutuksen selvitys ei tapahdu automaattisesti, jos peruutuspäivämäärä on eri tilikaudella.

## <a name="use-excel-for-ledger-settlement"></a>Excelin käyttö tapahtuman selvitykseen

**Kirjanpidon tilitys** -sivulla näkyvät tapahtumat voidaan viedä Exceliin. Excelissä voit suodattaa tapahtumia edelleen selvittääksesi, mitä tapahtumia haluat merkitä tilitettäviksi.
Molemmat kirjanpidon selvitysyksiköt vievät kirjanpitotapahtumia vain **Kirjanpidon tilitys** -sivulla valitulle päätilille. Vaikka suljettujen tilikausien tapahtumat voidaankin merkitä tai poistaa merkintä Excelin avulla, niitä ei voi selvittää. Lisäksi tilitettyjä tapahtumia ei voi palauttaa kyseiselle tilivuodelle.

## <a name="make-transactions-easier-to-find"></a>Tapahtumien löytämisen helpottaminen

**Tapahtuman selvitykset** -sivulla on toimintoja, jotka helpottavat selvitettävän tapahtuman näkemistä.

•   **Merkitty**-suodattimella voi suodataa tapahtumia sen perusteella, onko tapahtumien **Merkitty**-valintaruutu valittu.
•   Käytä **Tila**-suodatinta, kun haluat suodattaa tapahtumia niiden tilan mukaan.
•   Lajittele summat absoluuttisen summan mukaan valitsemalla **Lajittelu absoluuttisen arvon mukaan**. Näin voit ryhmitellä debet- ja kredit-merkinnät, joissa on sama summa.

## <a name="reverse-a-settlement"></a>Käänteinen tilitys

Voit tehdä tarvittaessa käänteisen tilityksen.

1.  Voit tarkastella haluamiasi tapahtumia noudattamalla [Tilitä tapahtumat](#settle-transactions) -osan vaiheita 1–3.
2.  Valitse **Tila**-suodattimessa **Selvitetty**.
3.  Valitse peruutettavat rivit.
4.  Valitse **Peruuta merkityt tapahtumat**. Kaikkien niiden tapahtumien tilaksi päivitetään **Ei selvitetty**, joiden tilityksen tunnus on sama.

> [!IMPORTANT]
> Kaikki tapahtumat, joilla on sama tilitystunnus, palautetaan, vaikka niitä ei olisi merkitty. Esimerkiksi neljä riviä on merkitty ja selvitetty. Kaikilla neljällä rivillä on sama tilitystunnus. Jos merkitset jo jonkin näistä neljästä rivistä ja valitset sitten **Palauta merkityt tapahtumat**, kaikki neljä riviä palautetaan.






