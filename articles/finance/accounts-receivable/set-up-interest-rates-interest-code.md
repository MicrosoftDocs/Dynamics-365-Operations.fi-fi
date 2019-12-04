---
title: Korkoryhmän korkoprosenttien määrittäminen
description: Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188990"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a>Korkoryhmän korkoprosenttien määrittäminen

[!include [banner](../includes/banner.md)]

Korkokoodit sisältävät asetukset, joilla määritetään, milloin korkoa veloitetaan ja miten se lasketaan erääntyneillä tileillä.

Voit määrittää yksittäisen korkokoodin ja käyttää sitä useassa asiakaskirjausprofiilissa, laskutuskoodeissa tai tietyillä laskuriviellä. Kun korkokoodin tietoja muutetaan, kaikki koodia käyttävät toiminnot käyttävät automaattisesti muutoksia uusissa tapahtumissa. Kullekin korkokoodille voi määrittää kahdentyyppisiä tuloja:
-   Tulot korkoansioista – Nämä ovat tuloja, jotka on ansaittu veloittamalla korkoa laskuista tai korkolaskuista.
-   TUlost kokorkomaksuista – Nämä ovat kustannuksia, jotka maksetaan korkolaskujen koroista.

Molemmat korkotyypit voivat olla olemassa samanaikaisesti ja samassa korkokoodissa. Korot voivat perustua kolmeen laskentatyyppin:
-   Korko prosenttiosuuden mukaan.
-   Korko summan mukaan.
-   Korko alueen mukaan, joka tuottaa yhden prosenttiosuuden tai summan.

Kun korkokoodia käytetään koron laskennassa, luodaan erillinen korkolasku kutakin korkotasoa varten, joka on voimassa sinä aikana, jonka maksu on ylittänyt tapahtuman eräpäivän. Voit määrittää **Korkoryhmä**-sivun **Ansiot**-välilehdessä korkotasot koroille, jotka ansaitaan veloittamalla korkoa. Määritä korkotasot itse maksamillesi koroille **Maksut**-välilehdessä.

## <a name="interest-rates-based-on-a-percentage"></a>Prosenttiosuuksiin perustuvat korkotasot
Voit määrittää korkotasot, jotka laskevat määritetyn prosenttiosuuden.

- Korkosumman koskee kaikkia valuuttoja.
- Korkosumman rajojen antaminen on valinnaista.
- <strong>Prosentti</strong> valitaan** <strong>Korkokoodien määrittäminen</strong> -sivun <strong>**Käytä korkolaskennan perusteena</strong> -kentässä.

Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 5 prosentin koron jokaista kahta kuukautta kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 2 **Koronlaskentaväli**-kenttään ja valitse **Kuukausi**.

## <a name="interest-rates-based-on-amounts"></a>Summin perustuvat korkotasot
Voit määrittää korkotasot, jotka laskevat määritetyn summan valuuttaa kohden.
- Korkosumma on määritettävä jokaiselle korkokoodin valuutalle.
- Korkosumman rajojen antaminen on valinnaista.
- **Summa** valitaan **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä.

Jos esimerkiksi haluat määrittää korkokoodin, joka määrää 25,00 valuuttayksikön koron jokaista 20 päivää kohti, jonka laskun maksaminen ylittää tapahtuman eräpäivän, anna arvo 20 **Koronlaskentaväli**-kentässä ja valitse **Päivä**.

## <a name="interest-rates-based-on-ranges"></a>Alueisiin perustuvat korkotasot
Voit määrittää korkotasot, jotka vaihtelevat myöhässä olevan summan, summan myöhässä olevien päivien määrän tai summan myöhässä olevien kuukausien määrän mukaan.
-   Voit määrittää kunkin valuutan korkoasetukset **Ansiot valuutan mukaan** -välilehdessä. Myös alue määritetään tässä välilehdessä.
-   Lisää **Alueet**-painikkeella rivit, jotka ilmaisevat määritettäviä alueita. **Mistä**-arvo ilmaisee alueen alkamiskohdan ja **Korkoarvo**-luku ilmaisee joko prosentin tai summan sen mukaan, mitä **Korkokoodien määrittäminen** -sivun **Käytä korkolaskennan perusteena** -kentässä on valittu.

## <a name="example-1-interest-by-range--amount"></a>Esimerkki 1: Korko alueen mukaan = summa
Määrität korkokoodin, joka arvioi koron kerran jokaista kolmea kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä. Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten summavälien mukaan. Koron arvo on 1 prosentti laskun summasta summaan 1 000,00 saakka, 2 prosenttia summasta välillä 1 001,00–5 000,00 ja 3 prosenttia yli 5 000,00:n summista. Määrität korkokoodin kenttien arvot seuraavasti.

| **Kentän nimi**                  | **Kentän arvo** |
|---------------------------------|-----------------|
| **Korkoryhmä**               | 3M%ByAmt        |
| **Koronlaskentaväli**    | 3/kuukausi         |
| **Korko alueen mukaan**           | Summa          |
| **Käytä korkolaskennan perusteena** | Prosentti      |

Määrität alueen tiedot seuraavasti.

| **Arvosta** | **Korkoarvo** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |


## <a name="example-2-interest-by-range--days"></a>Esimerkki 2: Korko alueen mukaan = päivät
--------------------------------------------------

Määrität korkokoodin, joka arvioi koron kerran jokaista 15 päivää kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä. Haluat laskennan perustuvan summan korkoarvoon askeleittaisten päivävälien mukaan. Koron arvo on 10,00 kutakin 15 päivää kohden 60 ensimmäisen päivän ajan, 15,00 kutakin 15 päivää kohden päivien 61–90 ajan ja 20,00 kutakin 15 päivää kohden päivän 91 ja sen jälkeisten päivien ajan. Määrität korkokoodin kenttien arvot seuraavasti.

| **Kentän nimi**                  | **Kentän arvo** |
|---------------------------------|-----------------|
| **Korkoryhmä**               | 15DAmtXDay      |
| **Koronlaskentaväli**    | 15/päivä          |
| **Korko alueen mukaan**           | Päivää            |
| **Käytä korkolaskennan perusteena** | Summa          |

Määrität alueen tiedot seuraavasti.

| **Arvosta** | **Korkoarvo** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |


## <a name="example-3-interest-by-range--months"></a>Esimerkki 3: Korko alueen mukaan = kuukaudet
----------------------------------------------------

Määrität korkokoodin, joka arvioi koron kerran jokaista kuukautta kohden, jonka laskun maksu on myöhässä tapahtuman eräpäivästä. Haluat laskennan perustuvan prosentuaaliseen korkoarvoon askeleittaisten kuukausivälien mukaan. Koron arvo on 1,5 prosenttia kuukaudessa eräpäivän jälkeisen kolmen ensimmäisen kuukauden ajan, 2,0 prosenttia kuukaudessa toisen kolmen kuukauden jakson ajan ja 2,5 prosenttia kuukaudessa kuuden ensimmäisen kuukauden jälkeen. Määrität korkokoodin kenttien arvot seuraavasti.

| **Kentän nimi**                  | **Kentän arvo** |
|---------------------------------|-----------------|
| **Korkoryhmä**               | 1M%ByMth        |
| **Koronlaskentaväli**    | 1/kuukausi         |
| **Korko alueen mukaan**           | Kuukautta          |
| **Käytä korkolaskennan perusteena** | Prosentti      |

Määrität alueen tiedot seuraavasti.

| **Arvosta** | **Korkoarvo** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Uudet versiot
Korkokoodeilla on voimassaolopäivät. Jos haluat muokata korkoprosenttia, voit luoda **uuden version**, jonka voimassaolo alkaa tiettynä päivänä tulevaisuudessa.

Voit tarkastella eri versioita valitsemalla **Alkupäivämäärä**-valikkovaihtoehdolla katkaisupäivämäärän. Jos haluat tarkastella kaikkia sivun korkoprosentteja, valitse **Näytä kaikki tietueet**.


