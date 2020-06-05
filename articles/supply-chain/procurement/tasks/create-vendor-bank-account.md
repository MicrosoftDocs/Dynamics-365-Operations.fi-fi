---
title: Luo toimittajan pankkitili
description: Tässä menettelyssä näytetään, miten luodaan toimittajalle pankkitili.
author: mkirknel
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8092ab7f960fd36515afb8448dfe1e262197595
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383133"
---
# <a name="create-a-vendor-bank-account"></a>Luo toimittajan pankkitili

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten luodaan toimittajalle pankkitili. Voit käyttää tätä menettelyä esittely-yrityksessä USMF.

1. Siirry kohtaan **siirtymisruutu > Moduulit > Hankinta > Toimittajat > Kaikki toimittajat**.
2. Valitse toimittaja, jolle haluat luoda pankkitilin ja napsauta sitten **Toimittajan tilitunnus** -kentän linkkiä.
3. Valitse **toimintoruudussa** **Toimittaja**.
4. Valitse **Pankkitilit**.
5. Napsauta **Toimintoruudussa** **Uusi**.
6. Kirjoita arvo **Pankkitili**-kenttään. Tätä tunnusta käytetään toimittajatietueen pankkitilin yksilöimiseen.  
7. Kirjoita arvo **Nimi**-kenttään.
8. Syötä tai valitse arvo **Pankkiryhmät**-kentässä.
9. Valitse **Pankkikoodin tyyppi** -kenttään vaihtoehto. Tämä on kansainvälisten tilisiirtojen pankkikoodityyppi.  
10. Kirjoita arvo **Pankkitilin numero** -kenttään.
11. Syötä arvo **SWIFT-koodi**-kenttään.
12. Syötä arvon **IBAN**-kenttään.
    - IBAN-tilinumeron on oltava oikeassa muodossa. Voit esimerkiksi käyttää tilinumeroa DE89370400440532013000.  
    - Pankkitilin tila on Aktiivinen, jos aktivointipäivämäärä on ohitettu, mutta vanhentumispäivää ei ole ohitettu. Se on aktiivinen myös, jos aktivointi- ja vanhentumispäiväkentät ovat tyhjiä. Jos sekä aktivointi- että vanhentumispäiväkentän päivämäärät ovat tulevia, sähköiset maksut eivät ole käytettävissä. Muut maksutyypit ovat käytettävissä, ja pankkitili on aktiivinen.  
13. Laajenna osa **Asetukset**.
14. Syötä arvo **Tekstikoodi**-kenttään. Tämä kenttä määrittää koodin, joka näytetään vastaanottajan tiliotteella.  
15. Kirjoita arvo **Sanoma pankille** -kenttään.
16. Kirjoita arvo **Vaihtokurssin viite** -kenttään. Tämä on muuttuvan tai kiinteän vaihtokurssin viitenumero.
17. Anna tai valitse **Valuutta**-kentässä arvo. Jos esilaskujen luonti on käytössä, tässä osassa on katsaus niiden tilaan (odottava tai hyväksytty).  
18. Laajenna **Osoite**-osa.
19. Laajenna **Esilaskut**-osa.
20. Laajenna **Yhteystiedot**-osa.
21. Kirjoita arvo **Puhelin**-kenttään.
22. Sulje sivu.
23. Valitse **Muokkaa**.
24. Laajenna **Maksu**-osa.
25. Valitse juuri luomasi tili **Pankkitili**-kentässä.
26. Valitse **Tallenna**. Osoite voi periytyä pankkiryhmästä, jos sellainen on määritelty, tai sen voi lisätä tässä.  

