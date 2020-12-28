---
title: Taloushallinnon täsmäytys vähittäismyymälöissä
description: Tässä aiheessa kuvataan vähittäismyymälöiden taloushallinnon täsmäytystä myyntipisteille Microsoft Dynamics 365 Commercessa.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5d0520f35391f76b52fd8a333033b0d7ba4f7fe1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411860"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Taloushallinnon täsmäytys vähittäismyymälöissä

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce -versiossa 10.0.10 ja tätä vanhemmissa versioissa toiminto, jonka myyntipisteasiakasohjelma antaa päivän päättymisen prosesseja varten vähittäismyymälöissä, mahdollistaa päivän päätteeksi tehtävät toimenpiteet myyntiassistenteille ja myymäläpäälliköille. He voivat esimerkiksi laskea kassoja, sulkea vuoroja piilotettuina, täsmäyttää vuorotapahtumia ja sulkea vuoroja. Myyntipisteet eivät voi kuitenkaan viimeistellä vuorojen taloushallinnon tietoja, jotta niitä voidaan käyttää taloustietojen kirjaamiseen Commerce-pääkonttorissa. Tavallisesti myymäläpäälliköt ovat vastuussa tämän tehtävän suorittamisesta. Ennen kuin he voivat kirjautua ulos vuorosta, heidän on tarkistettava tiedot, tehtävä tarvittavat korjaukset ja viimeisteltävä vuoron summat. Lopulliset summat tulee sitten julkaista Commerce-pääkonttorin taloushallinnon moduuleissa.

Lisäksi Commerce-versiossa 10.0.10 ja tätä vanhemmissa versioissa myymäläpäälliköt voivat tarkastella ja säätää laskelmarivejä Commerce-pääkonttorissa. Suorituskyky on kuitenkin rajallinen, ja myymäläpäälliköillä on harvoin pääsyä Commerce-pääkonttorin asiakasohjelmaan. Lisäksi taloushallinnon raportin tarkastus ja oikaisu voidaan tehdä vain, kun raportit luodaan Commerce-pääkonttorissa. Tämä on kuitenkin tavallisesti yöllinen prosessi. Siksi myymäläpäälliköiden on odotettava vuoron päättymistä, kun vähittäismyynnin raportit luodaan Commerce-pääkonttorissa.

Commerce-versiossa 10.0.11 ja uudemmissa versioissa myymäläpäälliköt voivat tarkistaa, muokata ja viimeistellä vuorojaan itse myyntipisteasiakasohjelmassa. Näitä tietoja käytetään sitten vähittäismyynnin raporttien luomiseen ja julkaisemiseen Commerce-pääkonttorissa.

> [!NOTE]
> Toiminto, joka liittyy taloushallinnon täsmäytykseen vähittäismyyntiliikkeissä toimii vain, jos syötteisiin perustuva vähittäin suoritettava tilauksen luonti on otettu käyttöön. Lisätietoa on kohdassa [Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Taloushallinnon täsmäytyksen määrittäminen

Noudata näitä ohjeita taloushallinnon täsmäytystoiminnon käytössä.

1. Ota **Ominaisuuksien hallinta** -työtilassa käyttöön **Vähittäismyyntilaskelmat – vähittäinen syöttö** -ominaisuus.
1. Asianmukaisen myymälän myyntipisteen toimintoprofiilissa määritä **Ota taloushallinnon täsmäytys liikkeessä käyttöön** -asetukseksi **Kyllä**.

## <a name="more-information-about-financial-reconciliation"></a>Lisätietoa taloushallinnon täsmäytyksestä

Kun taloushallinnon täsmäytystoiminto otetaan käyttöön, jotkin parametreista, jotka määritetään **Laskelma/sulkeminen**-pikavälilehdessä **Vähittäismyymälät**-sivulla Commerce-pääkonttorissa, synkronoidaan kanavatietokantaan. Samaa laskelmakriteerien joukkoa ja määrärajoja, joita käytetään vähittäismyyntilaskelmiin, käytetään.

Kun **Sulje vuoro** -toimenpiteeseen ryhdytään, järjestelmä vahvistaa, että järjestelmän laskemat määrät ja ilmoitetut määrät vastaavat toisiaan. Jos ne eroavat toisistaan ja ero ylittää määritetyt rajat, käyttäjä saa kehotuksen ja voi tehdä tarvittavat oikaisut.

Oikaisut voidaan tehdä kullekin maksuvälineelle. Kun maksuväline valitaan, käyttäjä voi tarkastella eri tapahtumatyyppien summia ja muokata tietyn tapahtumatyypin summaa. Muokkauksen aikana järjestelmä näyttää alkuperäisen lasketun summan ja kyseessä olevan tapahtumatyypin hylätyn summan. Käyttäjä voit myös tallentaa huomautuksia osana muokkausprosessia. Huomautuksia voidaan käyttää auditointitarkoituksiin.

Käyttäjät voivat sivuuttaa vahvistuskehotteet ja -sanomat ja jatkaa vuoron sulkemiseen. Jos käyttäjä sivuuttaa vahvistuskehotteet, samat ongelmat kuitenkin toistuvat, ja ne on korjattava, kun vuoro julkaisee raportit Commerce-pääkonttorissa.

**Sulje vuoro** -toimenpide myyntipisteessä vahvistaa myös, että kaikki offline-tietokannan tapahtumat synkronoidaan kanavatietokantaan. Jos mitään tapahtumia ei synkronoida, käyttäjä saa varoitussanoman, sillä tämä tilanne voi aiheuttaa järjestelmän summien virheellisen laskennan. Tässä tilanteessa käyttäjä voi päättää **Sulje vuoro** -toimenpiteen ja yrittää synkronoida offline-tapahtumat kanavatietokantaan. Vaihtoehtoisesti käyttäjä voi muokata järjestelmän laskemia summia manuaalisesti selvittääkseen synkronoimattomat tapahtumat, jotta oikea taloushallinnon numeroiden joukko viimeistellään ja julkaistaan. 

Kun syötteisiin perustuvaa vähittäin suoritettavaa laskelman julkaisua käytetään, jolloin tapahtumien julkaisu tapahtuu erillään taloustietojen julkaisusta, voit päättää muokata järjestelmän laskemia summia puuttuvien offline-tapahtumien vuoksi. Näin varmistat, että taloustiedot selvitetään ja julkaistaan oikein, puuttuvista tapahtumista huolimatta. Offline-tapahtumat voidaan synkronoida kanavatietokantaan ja Commerce-pääkonttoriin ja julkaista sitten myöhemmin, erikseen taloushallinnon julkaisusta.

Tiedot vuoron taloushallinnon täsmäytyksestä synkronoidaan Commerce-pääkonttoriin P-työn avulla.

Vähittäismyynnin raportit Commerce-pääkonttorissa eivät laske summia näyttääkseen tarkempia tietoja laskelmariveillä. Sen sijaan myyntipisteasiakasohjelman viimeisteltyjä summia käytetään vähittäismyynnin raporttien luomiseen ja julkaisemiseen.
