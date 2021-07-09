---
title: Ostohyvityksen vähentämisperiaatteet
description: Tässä ohjeaiheessa käsitellään ostohyvityksen vähentämisperiaatteiden määrittämistä. Vähennysperiaatteet ohjaavat toimintaa, kun samaan nimikkeeseen tai tapahtumaan sovelletaan useita ostohyvityksiä.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: a0cde0c22b69e7605708a647d47530840ce823b1
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270930"
---
# <a name="rebate-reduction-principles"></a>Ostohyvityksen vähentämisperiaatteet

[!include [banner](../includes/banner.md)]

Voit ryhmitellä ostohyvitysten hallinnan sopimukset *vähennysperiaatteiksi*, kun haluat vähentää nimikkeeseen liittyviä muita varauksia ja/tai vähentää ostohyvityslaskelmien tulosten arvoja. Kun ostohyvitysten vähennysperiaatteet on määritetty, voit tarvittaessa määrittää ne ostohyvitysten hallintasopimusten riveille.

Ostohyvitysten vähennysperiaatesääntöjä käytetään vain, kun ostohyvityssopimukset ovat päällekkäisiä. Näin ollen ne voivat myöntää useita ostohyvityksiä tilanteissa, jos useita ostohyvityksiä ei omisteta.

## <a name="manage-rebate-reduction-principles"></a>Ostohyvityksen vähentämisperiaatteiden hallinta

Voit käyttää ostohyvitysten vähennysperiaatteita kohdassa **Ostohyvitysten hallinta \> Asetukset \> Ostohyvityksen vähentämisperiaatteet**. Sitten voit lisätä ja poistaa vähentämisperiaatteita tarpeen mukaan käyttämällä toimintoruudun painikkeita. Määritä kunkin periaatteen kentät seuraavassa taulukossa kuvatulla tavalla.

| Kenttä | kuvaus |
|---|---|
| Ostohyvityksen vähentämisperiaate | Kirjoita ostohyvityksen vähennysperiaatteen yksilöivä nimi. |
| kuvaus | Kirjoita ostohyvityksen vähennysperiaatteen kuvaus. |
| Vähennyksen kohdistaminen | Valitse tämä valintaruutu, jos haluat käyttää tähän ostohyvitysvähennysperiaatteeseen kuuluvia ostohyvityksen perusteita. |
| Vähennysperuste | Jos valitsit **Vähennyksen kohdistaminen** -valintaruudun, valitse vähennysperuste (*Varaus*, *Ostohyvitykset* tai *Molemmat*). Jos valitset *Molemmat* ja jos aiemmassa sopimuksesta on kirjattu sekä varaus että ostohyvitys, vain ostohyvitys kohdistetaan. |
| Poissulkeminen vähennyksestä | Jos tämä valintaruutu on valittuna, tähän ostohyvitysvähennysperiaatteeseen kuuluvat varaukset ja ostohyvitykset suljetaan pois myöhemmistä vähennyksistä. **Vähennysperuste**-kentän asetus ei koske tätä asetusta. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Esimerkkejä ostohyvitysvähennysperiaatteen asetuksista

Seuraavassa taulukossa on tyypillisiä esimerkkejä ostohyvityksen vähennysperiaatteen asetuksista. **Kuvaus**-kentän arvo kuvaa ostohyvitysvähennysperiaatteen tarkoitusta kullekin ostohyvityksen vähennysperiaatteelle.

| Ostohyvityksen vähentämisperiaate | kuvaus | Vähennyksen kohdistaminen | Vähennysperuste | Poissulkeminen vähennyksestä |
|---|---|---|---|---|
| Lykätty | Vähennä ostohyvitystä | Kyllä | Molemmat | Nro |
| Exclreb | Poissulje ostohyvitys | Kyllä | Hyvitys   | Kyllä |
| Usea | Useita ostohyvityksiä | Kyllä | Molemmat | Kyllä |
| None | Vain varaus ja ostohyvitys | Nro | Molemmat | Kyllä |
| Varaa | Vain varaus | Kyllä | Varaa | Nro |
| Hyvitys   | Vain ostohyvitys | Kyllä | Hyvitys   | Kyllä |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Esimerkkejä ostohyvitysvähennysperiaatteen laskelmista

Myyntitilauksessa on yksi myyntitilausrivi. Rivin arvo on 1 000 $. Tilaukseen kohdistetaan seuraavat sopimukset:

- **Sopimus 1:** 10 prosenttia summasta 1 000 $
- **Sopimus 2:** 15 prosenttia summasta 1 000 $
- **Sopimus 3:** 20 prosenttia summasta 1 000 $
- **Sopimus 4:** 25 prosenttia summasta 1 000 $

Käsittelyjärjestys on erittäin tärkeä. Käsittelyjärjsetys perustuu työskentelytapaan, joka on kuvattu kohdassa [Ostohyvitysten käsitteleminen, tarkistaminen ja kirjaaminen](process-review-post.md).

Seuraavassa taulukossa on esimerkiksi yhteenveto tuloksesta, jos käytät järjestystä *1, 2, 3, 4* ja jos käsittelet vain varaukset.

| Sopimus | Kuvaus ja asetukset | Varauksen tulos |
|---|---|---|
| 1 | <p>Luokittelu ei tarkista muita sopimuksia vähennysten varalta. Tarkistus tehdään sekä varauksille että ostohyvityksille.</p><ul><li>**Vähennyksen kohdistaminen:** *Ei*</li><li>**Vähennysperuste:** *Molemmat*</li><li>**Poissulkeminen vähennyksestä:** *Ei*</li></ul> | 1 000 $ × 10 % = 100 $ |
| 2 | <p>Luokittelu tarkistaa vähennykset muista sopimuksista, mutta se on merkitty siten, että sitä itseään oteta huomioon. Tarkistus tehdään vain ostohyvityksille.</p><ul><li>**Vähennyksen kohdistaminen:** *Kyllä*</li><li>**Vähennysperuste:** *Ostohyvitys*</li><li>**Poissulkeminen vähennyksestä:** *Kyllä*</li></ul> | 1 000 $ × 15 % = 150 $ |
| 3 | <p>Luokittelu tarkistaa muut sopimukset vähennysten varalta. Tarkistus tehdään sekä varauksille että ostohyvityksille.</p><ul><li>**Vähennyksen kohdistaminen:** *Kyllä*</li><li>**Vähennysperuste:** *Molemmat*</li><li>**Poissulkeminen vähennyksestä:** *Ei*</li></ul> | (1 000 $ – Sopimus 1) × 20 % = 180 $ |
| 4 | <p>Luokittelu tarkistaa muut sopimukset vähennysten varalta. Tarkistus tehdään sekä varauksille että ostohyvityksille.</p><ul><li>**Vähennyksen kohdistaminen:** *Kyllä*</li><li>**Vähennysperuste:** *Molemmat*</li><li>**Poissulkeminen vähennyksestä:** *Ei*</li></ul> | (1 000 $ – Sopimus 1 – Sopimus 3) × 25 % = 180 $ |

Seuraavassa taulukossa on joitakin esimerkkejä, joissa varaus käsitellään eri järjestyksissä ja missä eri summat näin ollen saavutetaan. Varausten varianssi määräytyy sen järjestyksen mukaan, jossa järjestelmä käsittelee sopimukset. On tärkeää ymmärtää, miten käsittelyjärjestys vaikuttaa lopulliseen ostohyvityssummaan.

| Järjestys | Laskelma |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Sopimus 1:** 1 000 $ × 10 % = 100 $</li><li>**Sopimus 2:** 1 000 $ × 15 % = 150 $</li><li>**Sopimus 3:** (1 000 $ – Sopimus 1) × 20 % = 180 $</li><li>**Sopimus 4:** (1 000 $ – Sopimus 1 – Sopimus 2) × 25 % = 180 $</li><li>**Varaus yhteensä:** 610 $</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Sopimus 4:** 1 000 $ x 25 % = 250 $</li><li>**Sopimus 3:** (1 000 $ – Sopimus 4) × 20 % = 150 $</li><li>**Sopimus 2:** 1 000 $ x 15 % = 150 $</li><li>**Sopimus 1:** 1 000 $ x 10 % = 100 $</li><li>**Varaus yhteensä:** 650 $</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Sopimus 3:** 1 000 $ x 20 % = 200 $</li><li>**Sopimus 2:** 1 000 $ x 15 % = 150 $</li><li>**Sopimus 1:** 1 000 $ x 10 % = 100 $</li><li>**Sopimus 4:** (1 000 $ – Sopimus 3 – Sopimus 1) × 25 % = 175 $</li><li>**Varaus yhteensä:** 625 $</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Sopimus 2:** 1 000 $ × 15 % = 150 $</li><li>**Sopimus 4:** 1 000 $ × 25 % = 250 $</li><li>**Sopimus 1:** 1 000 $ × 10 % = 100 $</li><li>**Sopimus 3:** (1 000 $ – Sopimus 4 – Sopimus 1) × 20 % = 130 $</li><li>**Varaus yhteensä:** 630 $</li></ul> |
