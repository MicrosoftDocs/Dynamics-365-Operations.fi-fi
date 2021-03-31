---
title: Toimittajan maksuehtojen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajalaskujen maksuehdot.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6a37272694609be14b566dae3c6cf561d4c6d2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227229"
---
# <a name="define-vendor-payment-terms"></a>Toimittajan maksuehtojen määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajalaskujen maksuehdot. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Maksun asetukset > Maksuehdot**.
2. Valitse **Uusi**. Maksuehdot-sivulla määritetään, miten eräpäivä lasketaan. Sivulla ei määritetä, miten käteisalennuksen päivämäärä lasketaan.  
3. Syötä **Maksuehdot**-kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Syötä **Päivää**-kenttään numero. Tähän syötetty luku lisätään maksutavan määrittämään eräpäivään tai kauden loppuun. Jos valitset esimerkiksi **Netto**, luku lisätään eräpäivään. Jos valitset **Nykyinen kuukausi**, luku lisätään nykyisen kuukauden viimeiseen päivään eräpäivän laskemiseksi.  
6. Valitse **Tallenna**.
7. Sulje sivu.
8. Siirry kohtaan **Ostoreskontra > Maksun asetukset > Käteisalennukset**.
9. Valitse **Uusi**.
10. Kirjoita **Käteisalennus**-kenttään tunnus.
11. Kirjoita **Kuvaus**-kenttään arvo.
12. Jos toimittaja tarjoaa alennustasoja, valitse seuraava käteisalennus nykyisen vanhennuttua.
13. Sulje sivu.
14. Syötä **Päivää**-kenttään numero. **Päivät**-kenttään syötettyä määrää käytetään käteisalennuksen päivämäärän laskemiseen **Netto-/Nykyinen**-kentässä valitun vaihtoehdon mukaan. Jos valittuna on **Netto**, määrä lisätään laskun päivämäärään käteisalennuksen päivämäärän määrittämistä varten. Jos valittuna on **Nykyinen kuukausi**, määrä lisätään nykyisen kuukauden loppuun käteisalennuksen päivämäärän määrittämistä varten.  
15. Syötä **Alennus**-kenttään käteisalennuksen prosentti. 
16. Syötä päätili, jolle käteisalennus kirjataan myyntilaskuille, ja syötä päätili, jolle käteisalennus kirjataan toimittajalaskuille. Päätiliä käytetään, jos **Käytä toimittajan alennusten päätiliä** -kohtaan on valittu **Alennuksen vastatilit**. Jos asetukseksi on valittu **Laskurivien tilit**, käteisalennus kirjataan laskurivien resurssin/kulujen tileille.  
17. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]