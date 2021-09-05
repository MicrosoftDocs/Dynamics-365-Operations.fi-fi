---
title: Kirjauskansioon kirjaamisen epäonnistuminen täsmäämättömyyden vuoksi
description: Tässä käsitellään, miksi debetit ja kreditit eivät täsmää tositetapahtumissa, mikä puolestaan estää tapahtumien kirjaamisen. Tässä aiheessa on myös ohjeet ongelman korjaamiseen.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385720"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Kirjauskansioon kirjaamisen epäonnistuminen täsmäämättömyyden vuoksi

[!include [banner](../includes/banner.md)]

Tässä käsitellään, miksi debetit ja kreditit eivät täsmää tositetapahtumissa, mikä puolestaan estää tapahtumien kirjaamisen. Tässä aiheessa on myös ohjeet ongelman korjaamiseen.

## <a name="symptom"></a>Oire

Joissakin tapauksissa kirjauskansiota ei voi kirjata ja näkyviin tulee seuraava sanoma: Tietyn tositteen tapahtumia ei voi täsmätä tietystä päivämäärästä alkaen (kirjanpitovaluutta: 0,01 - raportointivaluutta: 0,06). Miksi kirjauskansiota ei voi kirjata?

## <a name="resolution"></a>Ratkaisu

Kirjanpitoon kirjauksen yhteydessä jokainen tosite on täsmäytettävä tapahtumavaluutassa, kirjanpitovaluutassa ja raportointivaluutassa, jos kyseiset valuutat on määritetty **Kirjanpidon asetukset** -sivulla. (Tositteet täsmäytetään, kun debetien yhteissumma on sama kuin kreditien yhteissumma.)

Summat näytetään kirjauskansion rivisivun alareunassa kirjanpitovaluuttana ja raportointivaluuttana. Niitä **ei** näytetä ulkomaanvaluuttatapahtumien tapahtumavaluuttana. Lisäksi virhesanomassa, jonka käyttäjät saavat simulaation tai kirjauksen aikana, näkyy vain kirjanpitovaluutan ja raportointivaluutan erot. Niitä ei näytetä tapahtumavaluuttana, koska yksittäisessä tositteessa voi olla useita tapahtumavaluuttoja ja kirjauskansio voi sisältää eri tapahtumavaluuttaisia tositteita. Tämän vuoksi on tärkeää tarkistaa, että jokaisen tositteen tapahtumavaluuttasummat on täsmäytetty.

### <a name="transaction-currency"></a>Tapahtumavaluutta

Järjestelmä tarkistaa simulaation ja kirjauksen aikana, että jokainen tosite on täsmäytetty tapahtumavaluuttana. Jokaisessa viedyssä tositteessa voi olla yksi tai useita tapahtumavaluutan valuuttoja. Kirjanpitoon viedyssä tositteessa voi olla esimerkiksi kaksi tapahtumavaluuttaa, kun käteistä siirretään euroja (EUR) käyttävältä pankkitililtä Kanadan dollareita (CAD) käyttävällä pankkitilille.

Jos tositteessa on vain yksi tapahtumavaluutta, kyseisen tositteen debetien summan on oltava yhtä suuri kuin sen kreditien summa. Asiakkaat ovat havainneet seuraavia skenaarioita, joissa kirjaaminen epäonnistui, koska tapahtumavaluutan summia ei oltu täsmäytetty:

- Debetien summaa ja kreditien summaa **ei** oltu täsmäytetty tapahtumavaluuttana vaikka ne oli täsmäytetty kirjanpitovaluuttana ja raportointivaluuttana. Asiakas oletti, että tosite kuitenkin kirjattaisiin. Tämä oletus oli kuitenkin virheellinen. **Tositteen tapahtumavaluutan summien on aina oltava täsmäytetty, kun kaikilla tositteen riveillä on sama valuutta.**
- Tosite tuotiin Microsoft Excelistä ja käyttäjä oletti, että tapahtumavaluutan summat oli täsmäytetty. Tuotavat summat oli määritetty Excel-työkirjassa **numeerisina** arvoina eikä **valuutta**-arvoina. Tässä skenaariossa työkirjan numeerisissa arvoissa oli yli kaksi desimaalia, ja tuotuihin arvoihin sisältyi yli kaksi arvoa. Niinpä debetit eivät ole yhtä suuria kuin kreditit, koska niiden poikkeama oli pyöristyksen murto-osa. Kirjauskansio ei näytä tätä ero tositteen riveillä, koska summissa näytetään vain kaksi desimaalia.
- Tosite tuotiin Excelistä ja käyttäjä oletti, että tapahtumavaluutan summat oli täsmäytetty. Vaikka tosite oli täsmäytetty, joillakin tositteen riveillä oli eri tapahtumapäivämäärät. Jos debetien summa ja kreditien summa lisättiin tosite- ja tapahtumapäivämääräkohtaisesti, ne eivät olleet täsmäytettyjä. Järjestelmä estää nyt tämän skenaarion. Tositteessa voi olla vain yksi tapahtumapäivämäärä. Tätä edellytystä valvotaan, kun tosite viedään kirjanpidon kautta järjestelmässä. Sitä ei kuitenkaan alun perin valvottu, kun tosite tuotiin Excelistä.

Tositteella voi olla yhdessä tuetussa skenaariossa monta tapahtumavaluuttaa. Siinä tapauksessa järjestelmä **ei** tarkista, että debetit ja kreditit ovat yhtä suuria tapahtumavaluuttana, koska valuutat eivät täsmää. Järjestelmä tarkistaa sen sijaan, että kirjapitovaluutan summat on täsmäytetty.

### <a name="accounting-currency"></a>Kirjanpitovaluutta

Jos kaikilla tositteen riveillä on sama tapahtumavaluutta ja jos tapahtumavaluutan summat on täsmäytetty, järjestelmä tarkistaa, että kirjanpitovaluutan summat on täsmäytetty. Jos tosite viedään ulkomaanvaluuttana, tapahtumavaluutan summat muunnetaan kirjanpitovaluutaksi tositteen rivien vaihtokurssin avulla: Ensimmäiseksi muunnetaan tositteen jokainen rivi. Sen jälkeen rivit lasketaan yhteen ja määritetään tällä tavoin debetien summa ja kreditien summa. Koska kukin rivi muunnetaan, debetien summa ja kreditien summa eivät ehkä täsmää. Jos ero on kuitenkin **Kirjanpitoparametrit**-sivulla määritetyn **Suurin pyöristysero** -arvon mukainen, tosite kirjataan ja ero kirjataan automaattisesti pyörityserotilille.

Jos tositteessa on useita tapahtumavaluuttoja, kukin tositteen rivi muunnetaan kirjanpitovaluutaksi, jonka jälkeen rivit lasketaan yhteen. Näin määritetään debetien summa ja kreditien summa. Täsmäyttäminen edellyttää, että debetit ja kreditit on täsmäytetty ja että pyörityseroa ei ole.

### <a name="reporting-currency"></a>Raportoinnin valuutta

Jos kaikilla tositteen riveillä on sama tapahtumavaluutta ja jos tapahtumavaluutan summat on täsmäytetty, järjestelmä tarkistaa, että raportointivaluutan summat on täsmäytetty. Jos tosite viedään ulkomaanvaluuttana, tapahtumavaluutan summat muunnetaan raportointivaluutaksi tositteen rivien vaihtokurssin avulla: Ensimmäiseksi muunnetaan tositteen jokainen rivi. Sen jälkeen rivit lasketaan yhteen ja määritetään tällä tavoin debetien summa ja kreditien summa. Koska kukin rivi muunnetaan, debetien summa ja kreditien summa eivät ehkä täsmää. Jos ero on kuitenkin **Kirjanpitoparametrit**-sivulla määritetyn **Suurin pyöristys raportointivaluuttana** -arvon mukainen, tosite kirjataan ja ero kirjataan automaattisesti pyörityserotilille.

Jos tositteessa on useita tapahtumavaluuttoja, kukin tositteen rivi muunnetaan raportointivaluutaksi, jonka jälkeen rivit lasketaan yhteen. Näin määritetään debetien summa ja kreditien summa. Täsmäyttäminen edellyttää, että debetit ja kreditit on täsmäytetty ja että pyörityseroa ei ole.
