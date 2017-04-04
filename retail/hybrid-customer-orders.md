---
title: Hybrid asiakkaiden tilaukset
description: "Hybrid asiakastilaus on yksittäisen tilauksen, joka sisältää tuotteita, jotka voidaan suorittaa kauppa pois asiakkaan sekä tuotteita, jotka kyytiin tai myöhemmin toimitettu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid asiakkaiden tilaukset

Hybrid asiakastilaus on yksittäisen tilauksen, joka sisältää tuotteita, jotka voidaan suorittaa kauppa pois asiakkaan sekä tuotteita, jotka kyytiin tai myöhemmin toimitettu.

Microsoft Dynamics-365 - toimintojen vähittäismyynnin, voit valita kaikki tuotteet joko toteuttaa tai suorittaa valitut tuotteet asiakkaan tilauksen. Tuotteen rivit, jotka on merkitty kuin suorittaa automaattisesti laskutetaan tilauksen luonnin jälkeen, samoin Tämä vastaa tilausta, joka on poimittu ylöspäin sen jälkeen, kun tilaus luodaan. Erääntynyt summa hybridi-tilaukset määritetään lisäämällä talletusten arvoa poiminta ja aluksen tuotteen rivit, joiden rivien suoritettava koko summa. Hybrid tilauksia järjestelmä vaihtaa asiakkaan tilauksen tila ja Itsepalvelutukku tila välillä seuraavasti:

-   Jos ostoskorin kaikki tuotteet ovat **suorittaa toimituksen**, kuin Itsepalvelutukku-tapahtuma käsitellään järjestyksessä.
-   Jos ostoskorin tai kaikki rivit on määritetty joko **poiminta** tai **aluksen toimituksen**, tilaus käsitellään asiakkaan tilauksen tapahtumana.

Jos valitun myyntikorin rivin ja **kerää valitut**, **valitaan aluksen**, tai **suorittaa valitun** on valittuna, vain tietyn ostoskorin rivi on määritetty kyseisen toimitustavan. Tässä tapauksessa toiminnan tilaajalle jatkuu tavalliseen tapaan. Kuitenkin jos **kerää valitut**, **valittu aluksen**, tai **suorittaa valitun** ilman myyntikorin rivin valittuna, uusi sivu avautuu, jossa luetellaan kaikki ostoskorin rivit on valittu. Näytössä, voit valita useita rivejä kerralla toimitustavan asettamiseen. Kun kyseistä menetelmää käytetään rivin valitseminen, ohitetaan edelliseen toimitustapa, joka on määritetty rivin.

<a name="see-also"></a>Lisätietoja
--------

[Asiakkaan tilaukset yleistä](customer-orders-overview.md)


