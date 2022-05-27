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
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 07408e608496dcc19562b866449b3b27f5f80edd
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719929"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Kirjauskansioon kirjaamisen epäonnistuminen täsmäämättömyyden vuoksi

[!include [banner](../includes/banner.md)]

Tässä käsitellään, miksi debetit ja kreditit eivät täsmää tositetapahtumissa, mikä puolestaan estää tapahtumien kirjaamisen. Tässä aiheessa on myös ohjeet ongelman korjaamiseen.

## <a name="symptom"></a>Oire

Joissakin tapauksissa kirjauskansiota ei voi kirjata ja näkyviin tulee seuraava sanoma: Tietyn tositteen tapahtumia ei voi täsmätä tietystä päivämäärästä alkaen (kirjanpitovaluutta: 0,01 - raportointivaluutta: 0,06). Miksi kirjauskansiota ei voi kirjata?

## <a name="resolution"></a>Ratkaisu

Kirjanpitoon kirjauksen yhteydessä jokainen tosite on täsmäytettävä tapahtumavaluutassa, kirjanpitovaluutassa ja raportointivaluutassa, jos kyseiset valuutat on määritetty **Kirjanpidon asetukset** -sivulla. (Tositteet täsmäytetään, kun debetien yhteissumma on sama kuin kreditien yhteissumma.)

Summat näytetään kirjauskansion rivisivun alareunassa kirjanpitovaluuttana ja raportointivaluuttana. Niitä **ei** näytetä ulkomaanvaluuttatapahtumien tapahtumavaluuttana. Lisäksi virhesanomassa, jonka käyttäjät saavat simulaation tai kirjauksen aikana, näkyy vain kirjanpitovaluutan ja raportointivaluutan erot. Niitä ei näytetä tapahtumavaluuttana, koska yksittäisessä tositteessa voi olla useita tapahtumavaluuttoja ja kirjauskansio voi sisältää eri tapahtumavaluuttaisia tositteita. Siksi on tärkeää varmistaa manuaalisesti, että kaikkien tositteiden, joissa on vain yksi tapahtumavaluutta, summat on täsmäytetty.

### <a name="transaction-currency"></a>Tapahtumavaluutta

Järjestelmä tarkistaa simulaation ja kirjauksen aikana, että jokainen tosite, jossa on vain yksi tapahtumavaluutta, on täsmäytetty tapahtumavaluuttana. Jokaisessa viedyssä tositteessa voi olla yksi tai useita tapahtumavaluutan valuuttoja. Kirjanpitoon viedyssä tositteessa voi olla esimerkiksi kaksi tapahtumavaluuttaa, kun käteistä siirretään euroja (EUR) käyttävältä pankkitililtä Kanadan dollareita (CAD) käyttävällä pankkitilille.

Jos tositteessa on vain yksi tapahtumavaluutta, kyseisen tositteen debetien summan on oltava yhtä suuri kuin sen kreditien summa tositteen valuuttana. Asiakkaat ovat havainneet seuraavia skenaarioita, joissa kirjaaminen epäonnistui, koska tapahtumavaluutan summia ei oltu täsmäytetty:

- Debetien summaa ja kreditien summaa **ei** oltu täsmäytetty tapahtumavaluuttana vaikka ne oli täsmäytetty kirjanpitovaluuttana ja raportointivaluuttana. Asiakas oletti, että tosite kuitenkin kirjattaisiin. Tämä oletus oli kuitenkin virheellinen. **Tositteen tapahtumavaluutan summien on aina oltava täsmäytetty, kun kaikilla tositteen riveillä on sama tapahtumavaluutta.**
- Tosite on tuotu tietoyksikön kanssa Data Management Framework (DMF) -kehyksen kautta, ja käyttäjä ajatteli, että tapahtumavaluuttasummat oli täsmäytetty. Tuontitiedoston joissakin summissa oli yli kaksi desimaalia, ja tuotuihin arvoihin sisältyi yli kaksi arvoa. Niinpä debetit eivät ole yhtä suuria kuin kreditit, koska niiden poikkeama oli pyöristyksen murto-osa. Kirjauskansio ei näytä tätä ero tositteen riveillä, koska summissa näytetään vain kaksi desimaalia.
- Tosite tuotiin tietoentiteetin kanssa DMF:n kautta ja käyttäjä oletti, että tapahtumavaluutan summat oli täsmäytetty. Vaikka **tosite** oli täsmäytetty, joillakin tositteen riveillä oli eri tapahtumapäivämäärät. Jos debetien summa ja kreditien summa tapahtumavaluuttana lisättiin **tosite- ja tapahtumapäivämääräkohtaisesti**, ne eivät olleet täsmäytettyjä. Tätä edellytystä valvotaan, kun tosite viedään kirjanpidon kautta järjestelmässä. Sitä ei ei kuitenkaan pakoteta, kun tosite tuodaan tietoentiteetin kanssa DMF:n kautta.

Tositteella voi olla yhdessä tuetussa skenaariossa monta tapahtumavaluuttaa. Siinä tapauksessa järjestelmä **ei** tarkista, että debetit ja kreditit ovat yhtä suuria tapahtumavaluuttana, koska valuutat eivät täsmää. Järjestelmä tarkistaa sen sijaan, että kirjapitovaluutan ja raportointivaluutan summat on täsmäytetty.

### <a name="accounting-currency"></a>Kirjanpitovaluutta

Jos kaikilla tositteen riveillä on sama tapahtumavaluutta ja jos tapahtumavaluutan summat on täsmäytetty, järjestelmä tarkistaa, että kirjanpitovaluutan summat on täsmäytetty. Jos tosite viedään ulkomaanvaluuttana, tapahtumavaluutan summat muunnetaan kirjanpitovaluutaksi tositteen rivien vaihtokurssin avulla: Ensin tositteen jokainen rivi käännetään ja pyöristetään kahteen desimaaliin. Sen jälkeen rivit lasketaan yhteen ja määritetään tällä tavoin debetien summa ja kreditien summa. Koska kukin rivi muunnetaan, debetien summa ja kreditien summa eivät ehkä täsmää. Jos eron itseisarvo on kuitenkin **Kirjanpitoparametrit**-sivulla määritetyn **Suurin pyöristysero** -arvon mukainen, tosite kirjataan ja ero kirjataan automaattisesti pyörityserotilille.

Jos tositteessa on useita tapahtumavaluuttoja, kukin tositteen rivi muunnetaan kirjanpitovaluutaksi ja pyöristetään kahteen desimaalin tarkkuuteen, jonka jälkeen rivit lasketaan yhteen. Näin määritetään debetien summa ja kreditien summa. Täsmäyttäminen edellyttää, että debetit ja kreditit on täsmäytetty kirjanpitovaluuttana.  Pyöristyserotiliä ei koskaan lisätä tositteeseen kirjanpitovaluutassa, jotta veloitukset ja hyvitykset saadaan tasapainoon. 

### <a name="reporting-currency"></a>Raportoinnin valuutta

Jos kaikilla tositteen riveillä on sama tapahtumavaluutta ja jos tapahtumavaluutan summat on täsmäytetty, järjestelmä tarkistaa, että raportointivaluutan summat on täsmäytetty. Jos tosite viedään ulkomaanvaluuttana, tapahtumavaluutan summat muunnetaan raportointivaluutaksi tositteen rivien vaihtokurssin avulla: Ensin tositteen jokainen rivi käännetään ja pyöristetään kahteen desimaaliin. Sen jälkeen rivit lasketaan yhteen ja määritetään tällä tavoin debetien summa ja kreditien summa. Koska kukin rivi muunnetaan, debetien summa ja kreditien summa eivät ehkä täsmää. Jos ero on kuitenkin **Kirjanpitoparametrit**-sivulla määritetyn **Suurin pyöristys raportointivaluuttana** -arvon mukainen, tosite kirjataan ja ero kirjataan automaattisesti pyörityserotilille.

Jos tositteessa on useita tapahtumavaluuttoja, kukin tositteen rivi muunnetaan raportointivaluutaksi ja pyöristetään kahteen desimaalin tarkkuuteen, jonka jälkeen rivit lasketaan yhteen. Näin määritetään debetien summa ja kreditien summa. Täsmäyttäminen edellyttää, että debetit ja kreditit on täsmäytetty raportointivaluuttana.  Pyöristyserotiliä ei koskaan lisätä tositteeseen raportointivaluutassa, jotta veloitukset ja hyvitykset saadaan tasapainoon.

### <a name="example-for-an-accounting-currency-imbalance"></a>Esimerkki kirjanpitovaluutan täsmäämättömyydestä

> [!NOTE]
> Raportointivaluutan summa lasketaan tapahtumavaluuttasummasta samalla tavalla kuin kirjanpitovaluuttasumma.

Vaihtokurssi: 1,5

| Rivi | Tosite | Tili | Valuutta | Debet (tapahtuma) | Kredit (tapahtuma) | Debet (kirjanpito) | Kredit (kirjanpito) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10.00 | | 15.00 |
| **Yhteensä** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Kirjanpitovaluutta on täsmäyttämätön arvolla 0,01. Jos pyöristyksen enimmäismäärä kirjanpitovaluuttana on vähintään 0,01, ero kirjataan automaattisesti pyöristyserotilille ja tosite kirjataan onnistuneesti.
