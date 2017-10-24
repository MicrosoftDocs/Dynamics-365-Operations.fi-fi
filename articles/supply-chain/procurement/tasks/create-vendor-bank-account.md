--- 
title: Luo toimittajan pankkitili
description: "Tässä menettelyssä näytetään, miten luodaan toimittajalle pankkitili."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: adb759c59d7275e7323dbb760de56acdef2e3cff
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-bank-account"></a>Luo toimittajan pankkitili

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten luodaan toimittajalle pankkitili. Voit käyttää tätä menettelyä esittely-yrityksessä USMF.

1. Valitse Hankinta > Toimittajat > Kaikki toimittajat.
2. Valitse toimittaja, jolle haluat luoda pankkitilin ja napsauta sitten toimittajan tilitunnuksen linkkiä.
3. Valitse toimintoruudussa Toimittaja.
4. Valitse Pankkitilit.
5. Valitse Uusi.
6. Kirjoita arvo Pankkitili-kenttään.
    * Tätä tunnusta käytetään toimittajatietueen pankkitilin yksilöimiseen.  
7. Kirjoita arvo Nimi-kenttään.
8. Syötä tai valitse arvo Pankkiryhmät-kentässä.
9. Valitse Pankkikoodin tyyppi -kenttään vaihtoehto.
    * Tämä on kansainvälisten tilisiirtojen pankkikoodityyppi.  
10. Kirjoita arvo Pankkitilin numero -kenttään.
11. Syötä arvo SWIFT-koodi-kenttään.
12. Syötä arvon IBAN-kenttään.
    * IBAN-tilinumeron on oltava oikeassa muodossa. Voit esimerkiksi käyttää tilinumeroa DE89370400440532013000.  
    * Pankkitilin tila on Aktiivinen, jos aktivointipäivämäärä on ohitettu, mutta vanhentumispäivää ei ole ohitettu. Se on aktiivinen myös, jos aktivointi- ja vanhentumispäiväkentät ovat tyhjiä. Jos sekä aktivointi- että vanhentumispäiväkentän päivämäärät ovat tulevia, sähköiset maksut eivät ole käytettävissä. Muut maksutyypit ovat käytettävissä, ja pankkitili on aktiivinen.  
13. Laajenna osa Asetukset.
14. Syötä arvo Tekstikoodi-kenttään.
    * Tämä kenttä määrittää koodin, joka näytetään vastaanottajan tiliotteella.  
15. Kirjoita arvo Sanoma pankille -kenttään.
16. Kirjoita arvo Vaihtokurssin viite -kenttään.
    * Tämä on muuttuvan tai kiinteän vaihtokurssin viitenumero.  
17. Anna tai valitse Valuutta-kentässä arvo.
    * Jos esilaskujen luonti on käytössä, tässä osassa on katsaus niiden tilaan (odottava tai hyväksytty).  
18. Laajenna Osoite-osa.
19. Laajenna Esilaskut-osa.
20. Laajenna Yhteystiedot-osa.
21. Kirjoita arvo Puhelin-kenttään.
22. Sulje sivu.
23. Valitse Muokkaa.
24. Laajenna Maksu-osa.
25. Valitse juuri luomasi tili Pankkitili-kentässä.
26. Valitse Tallenna.
    * Osoite voi periytyä pankkiryhmästä, jos sellainen on määritelty, tai sen voi lisätä tässä.  


