---
title: Otsikon kulujen jakaminen suhteellisesti vastaaville myyntiriveille
description: Tässä ohjeaiheessa käsitellään Commerce-kanavan tilausten automaattisten kulujen laskemisen ja kohdistamisen lisäominaisuuksia käyttämällä automaattista etukäteisveloitustoimintoa.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0de29e1817840c172f9235f2ee48251c4878a0573d270a60fde5b42ba6f88d31
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774506"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Otsikon kulujen jakaminen suhteellisesti vastaaville myyntiriveille


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään otsikkotason automaattisten kulujen ryhmittämistoimintoa ja niiden jakamista suhteellisti kaupan myyntiriveille. Tätä toimintoa voi käyttää tapahtumissa, josta on luotu myyntipisteessä Retail-versiolla 10.0.1 ja myynneissä, jotka on luotu puhelinkeskuksessa Retail-versiolla 10.0.2.

Tämä toiminto on käytettävissä vain, jos [automaattiset etukäteisveloitukset](/dynamics365/unified-operations/retail/omni-auto-charges) on otettu käyttöön **Commercen parametrit** -sivun asetuksella. Automaattisten kulujen laajennettua laskentamenetelmään voidaan lisäksi käyttää vain myyntitilauksissa, jotka on luotu myyntikanavissa (myyntipiste, puhelinkeskus ja Dynamicsin sähköinen kaupankäyntiympäristö).

Tämän uuden toiminnon avulla organisaatiot voivat laskea ja kohdistaa otsikkotason automaattiset kulut entistä joustavammin myyntitapahtumiin.

Versiota 10.0.1 edeltävissä sovelluksen versioissa otsikkotason automaattiset kulut, joilla on tietty toimitustapasuhde, laskettiin vain, kun myyntitilauksen otsikossa oli vastaava toimitustapa.

Esimerkki: Otsikkotason automaattiset kulut on määritetty toimitustavoille **99** ja **11**. Myyntitilaus luodaan, ja tilauksessa otsikossa toimitustavaksi on määritetty **99**. Osa myyntiriveistä on kuitenkin määritetty siten, että niiden toimitukseen käytetään toimitustapaa **11**. Tässä tapauksessa vain toimitustapaan **99** linkitetyt otsikkotason kulut otetaan huomioon ja kohdistetaan myyntitilaukseen.

Commercessa otsikkotason kuluilla on lisäominaisuus, jonka avulla voi määrittää tilauksen arvoon perustuvan [maksutasomäärityksen](/dynamics365/unified-operations/retail/configure-call-center-delivery). Esimerkki: Jos tilauksen arvo 50,00–200,00 $, organisaatio voi veloittaa rahtikuluina 5,00 $. Jos tilauksen arvo on kuitenkin 200,01–500,00 $, rahtikulut voivat olla 4,00 $.

Osa organisaatioista haluaa käyttää otsikkotason kuluista saatavat maksutasolaskennan edut. Jos skenaario kuitenkin sisältää toimitustapayhdistelmän, nämä organisaatiot haluavat myös varmistaa, että laskettavat kulut perustuvat kullakin myyntirivillä määritettyyn toimitustapaan.

Voit nyt määrittää otsikkotason automaattiset kulut siten, että kaikki tilauksen toimitustavat otetaan huomioon, kuluja laskettaessa. Tämä toiminto edellyttää, että otsikkotason kulujen laskemisessa käytetään monimutkaista kustannuslaskentalogiikkaa. Logiikka ryhmittää yhteen kaikki samalla toimitustavalla lähetettävät nimikkeet ja käsittelee tätä ryhmää nimikkeiden laskentaryhmänä, kun se laskee otsikkotason automaattiset kulut. Jos nimikkeillä on sama toimitustapa, automaattiset kulut lasketaan nimikkeiden yhdistetyn myyntiarvon perusteella. Tällä tavoin määritetään asianmukainen automaattinen kulutaso.

Kun samaa toimitustapaa käyttävien myyntirivien asianmukaiset otsikkotason kulut on saatu, lasketut kulut jaetaan suhteellisesti myyntirivitasolle. Koska nämä kulut ovat rivitasolla sen sijaan, että pidettäisiin otsikkotasolla, nimikkeen ja sille lasketun kuluarvon välille muodostuu tarkka linkki. Tästä voi olla hyötyä osittaisissa palautuksissa, joissa organisaatio haluaa palauttaa koko kulun sijaan vain osan kulusta silloin, kun vain jotkin nimikkeet palautetaan.

## <a name="scenarios"></a>Skenaariot

Kahdessa seuraavassa malliskenaariossa havainnollistetaan, miten nämä kulut lasketaan silloin, kun uusi toiminto on käytössä ja silloin kun sitä ei käytetä.

### <a name="scenario-1"></a>Skenaario 1

Tämä skenaario havainnollistaa, mitä tapahtuu, kun automaattisten kulujen asetuksissa **Jaa suhteellisesti vastaaville myyntiriveille** -asetuksen arvoksi valitaan **Ei**. (Tämä toiminta vastaa otsikko tason kuluja versiota 10.0.1 edeltävissä sovellusversioissa.)

Tässä skenaariossa organisaatio on määrittänyt toimitustapasuhteiden **99** ja **11** otsikkotason kulut. Toimitustavalle **21** ei ole määritetty automaattisia kuluja.

![Toimitustavan 99 automaattiset kulut, kun vastaavan rivin suhteellinen jako on poistettu käytöstä.](media/99_disabled.png)

![Toimitustavan 11 automaattiset kulut, kun vastaavan rivin suhteellinen jako on poistettu käytöstä.](media/11_disabled.png)

Myyntitilaus luodaan puhelinkeskuksessa ja toimitustavaksi määritetään **99**. Tässä tilauksessa on viisi nimikettä. Kaksi tilausriviä on määritetty käyttämään toimitustapaa **99**, kaksi riviä toimitustapaa **11** ja yksi rivi toimitustapaa **21** (katso seuraava taulukko).

| Nimike  | Rivin määrä | Toimitustapa | Yksikköhinta |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 $            |
| 81332 | 1             | 99            | 50 $            |
| 81333 | 2             | 11            | 30 $            |
| 81334 | 3             | 99            | 10 $            |
| 81334 | 3             | 21            | 5 $             |

Tässä skenaariossa koko tilaus arvioidaan toimitustavan **99** automaattisen kulutaulukon perusteella. Kaikkien myyntirivien kokonaissumman perusteella määritetään automaattisen kulumäärityksen vastaava taso, ja tätä kulua käytetään tilauksen otsikkotasolla. Tässä esimerkiksi tilauksen kokonaissumma on 165,00 $, ja tilauksen otsikkoon on kohdistettu 15,00 $:n rahtikulu. Toimitustavalle **11** määritettyjä automaattisia kustannuksia ei koskaan tarkisteta tai käytetä.

Jos asiakas palauttaa tässä skenaariossa joitakin tilauksen nimikkeitä ja jos [kulukoodi on määritetty siten, että se palautetaan](/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), palautetukseen käytetään järjestelmällisesti otsikkotason kokonaiskulua, vaikka voi osa nimikkeistä palautetaan.

### <a name="scenario-2"></a>Skenaario 2

Tässä skenaariossa on määritetty toimitustapasuhteiden **99** ja **11** otsikkotason kulut. Näiden automaattisten kulutaulukkojen **Jaa suhteellisesti vastaaville myyntiriveille** -asetukseksi on määritetty **Kyllä**.

![Toimitustavan 99 automaattiset kulut, kun vastaavan rivin suhteellinen jako on otettu käyttöön.](media/99_enabled.png)

![Toimitustavan 11 automaattiset kulut, kun vastaavan rivin suhteellinen jako on otettu käyttöön.](media/11_enabled.png)

Tässä skenaariossa käytetään samaa viisi riviä sisältävää myyntiriviä. Vaikka tilauksen otsikon toimitustavaksi määritetään **99**, myyntilauksen kunkin rivin toimitustapa määritetään seuraavaan taulukon mukaisesti.

| Nimike  | Rivin määrä | Toimitustapa | Yksikköhinta |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 $            |
| 81332 | 1             | 99            | 50 $            |
| 81333 | 2             | 11            | 30 $            |
| 81334 | 3             | 99            | 10 $            |
| 81334 | 3             | 21            | 5 $             |

Koska automaattinen kulumääritys on määritetty jaettavaksi suhteellisesti vastaaville myyntiriveille, järjestelmää suorittaa seuraavat laskelmat.

1. Kaikki nimikkeet, joilla on sama toimitustapa, ryhmitetään yhteen, ja järjestelmä laskee ryhmän nimikkeiden tuotearvon yhteensä.

    **Toimitustapa 11**

    - Nimike 81331, määrä 1 = 10 $
    - Nimike 81333, määrä 2 = 60 $ netto (30 $/yksikkö)
    - **Toimitustavan 11 tuotearvo yhteensä = 70 $**

    **Toimitustapa 99**

    - Nimike 81332, määrä 1 = 50 $
    - Nimike 81334, määrä 3 = 30 $ netto
    - **Toimitustavan 99 tuotearvo yhteensä = 80 $**

    **Toimitustapa 21**

    - Nimike 81334, määrä 3 = 15 $ netto
    - **Toimitustavan 21 tuotearvo yhteensä = 15 $**

2. Järjestelmä etsii sellaisen otsikkotason automaattisten kulujen määrityksen, joka vastaa asiakkaan ja kunkin nimikeryhmän toimitustapa-asetuksia. Jos määritys löytyy, järjestelmä etsii tasomäärityksestä käytettävän kulun toimitustaparyhmän nimikkeiden tuotearvon kokonaissumman perusteella.

    **Toimitustapa 11**

    - Tuotteen kokonaisarvo = 70 $
    - **Kulujen arvo = 7 $**

    **Toimitustapa 99**

    - Tuotteen kokonaisarvo = 80 $
    - **Kulujen arvo = 15 $**

    **Toimitustapa 21**

    - Tuotteen kokonaisarvo = 15 $
    - **Kulujen arvo = 0 $** (tälle asiakas- ja toimitustapayhdistelmälle ei ole määritetty automaattisia kuluja)

    ![Toimitustavan 11 kulut menevät korostettuun tasoon.](media/step2mode11.png)

    ![Toimitustavan 99 kulut menevät korostettuun tasoon.](media/step2mode99.png)

3. Järjestelmä laskee kullakin rivillä käytettävän kulujen arvon sellaisen suhteelliseen jaon logiikan mukaan, joka ottaa huomion rivin suhteellisen arvon suhteessa ryhmän tuotteen kokonaisarvoon.

    **Toimitustapa 11**

    - Kulujen arvo = 7 $
    - Ryhmän tuotteen arvo = 70 $
    - Rivin 1 arvo = 10 $ (= 14,2857 prosenttia ryhmän arvosta)
    - Rivin 3 arvo = 60 $ (= 85,7143 prosenttia ryhmän arvosta)
    - **Rivin 1 rivin kulu = 1 $**
    - **Rivin 3 rivin kulu = 6 $**

    **Toimitustapa 99**

    - Kulujen arvo = 15 $
    - Ryhmän tuotteen arvo = 80 $
    - Rivin 2 arvo = 50 $ (= 62,5 prosenttia ryhmän arvosta)
    - Rivin 4 arvo = 30 $ (= 37,5 prosenttia ryhmän arvosta)
    - **Rivin 2 rivin kulu = 9,38 $**
    - **Rivin 4 rivin kulu = 5,62 $**

    **Toimitustapa 21**

    - Kulujen arvo = 0 $
    - Ryhmän tuotteen arvo = 15 $
    - Rivin 5 arvo = 15 $ (= 100 prosenttia ryhmän arvosta)
    - **Rivin 5 rivin kulu = 0 $**

Tämän vuoksi tässä esimerkissä nimikkeelle 81334 määritetään rahtikuluksi 5,62 $. Voit tarkastella näitä kuluja myyntirivin **Kulujen ylläpito** -sivulla. Seuraava kuva osoittaa, miltä kyseinen sivu näyttää nimikkeelle 81334.

![Nimikkeen 81334 myyntirivin suhteellisesti jaetut kulut.](media/proratedlinecharge.png)

Kun tätä laskentamenetelmää käytetään osittaisen palautuksen skenaariossa, jossa kulukoodi on palautettavissa, vain osa kyseiselle riville kohdistetusta kulusta palautetaan nimikkeen palautuksen yhteydessä.

## <a name="additional-resources"></a>Lisäresurssit

[Omnikanavan automaattiset etukäteisveloitukset](omni-auto-charges.md)

[Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]