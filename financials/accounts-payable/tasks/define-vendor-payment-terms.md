--- 
title: "Määritä toimittajan maksuehdot"
description: "Määritä toimittajan laskujen maksuehdot."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>Määritä toimittajan maksuehdot

[!include[task guide banner](../../includes/task-guide-banner.md)]

Määritä toimittajan laskujen maksuehdot. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksuehdot.
2. Valitse Uusi.
    * Maksuehdot-sivulla määritetään, miten eräpäivä lasketaan. Sivulla ei määritetä, miten käteisalennuksen päivämäärä lasketaan.  
3. Syötä Maksuehdot-kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä Päivät-kenttään numero.
    * Tähän syötetty luku lisätään maksutavan määrittämään eräpäivään tai kauden loppuun. Jos valitset esimerkiksi Netto, luku lisätään eräpäivään. Jos valitset Nykyinen kuukausi, luku lisätään nykyisen kuukauden viimeiseen päivään eräpäivän laskemiseksi.  
6. Valitse Tallenna.
7. Sulje sivu.
8. Siirry kohtaan Ostoreskontra > Maksun asetukset > Käteisalennukset.
9. Valitse Uusi.
10. Kirjoita Käteisalennus-kenttään tunnus.
11. Kirjoita arvo Kuvaus-kenttään.
12. Jos toimittaja tarjoaa alennustasoja, valitse seuraava käteisalennus nykyisen vanhennuttua.
13. Sulje sivu.
14. Syötä Päivät-kenttään numero.
    * Päivät-kenttään syötettyä määrää käytetään käteisalennuksen päivämäärän laskemiseen Netto-/Nykyinen-kentässä valitun vaihtoehdon mukaan. Jos valittuna on Netto, määrä lisätään laskun päivämäärään käteisalennuksen päivämäärän määrittämistä varten. Jos valittuna on Nykyinen kuukausi, määrä lisätään nykyisen kuukauden loppuun käteisalennuksen päivämäärän määrittämistä varten.  
15. Syötä Alennus-kenttään käteisalennuksen prosentti. 
16. Syötä päätili, jolle myyntilaskujen käteisalennus kirjataan.
17. Syötä päätili, jolle toimittajan laskujen käteisalennus kirjataan.
    * Päätiliä käytetään, jos Käytä toimittajan alennusten päätiliä -kohtaan on valittu Alennuksen vastatilit.  Jos asetukseksi on valittu Laskurivien tilit, käteisalennus kirjataan laskurivien käyttöomaisuuserän/kulujen tileille.  
18. Valitse Tallenna.


