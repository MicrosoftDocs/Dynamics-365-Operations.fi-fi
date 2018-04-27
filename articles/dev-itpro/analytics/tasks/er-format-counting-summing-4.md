--- 
title: Muodon suorittaminen laskennan ja summien tuottamiseksi
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e3569e48bcc063b2423a60038732e8e53dbea2cb
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="run-the-format-to-do-counting-and-summing"></a>Muodon suorittaminen laskennan ja summien tuottamiseksi

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella. Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.

Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 3: Käytä laskentoja tuotoksen luomiseen)" -menettelyn vaiheet.

Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Testaa konfiguraation Intrastat-raporttien luonti
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Laajenna puussa solmu "Intrastat model".
4. Laajenna puusta "Intrastat model\Intrastat (DE)"
5. Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
6. Valitse toimintoruudussa Konfiguroinnit.
7. Valitse Käyttäjän parametrit.
8. Valitse Suorita asetukset -kentässä Kyllä.
9. Valitse OK.
10. Valitse Muokkaa.
11. Valitse Suorita luonnos -kentässä Kyllä.
12. Valitse Tallenna.
13. Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.
14. Laajenna Sähköinen raportointi -osa.
15. Valitse Intrastat (DE) with counting & summing -konfiguraatio.
16. Valitse Intrastat (DE) with counting & summing -konfiguraatio.
17. Valitse Tallenna.
18. Sulje sivu.
19. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.
20. Valitse Tulostus.
21. Valitse Raportti.
    * Aja Intrastat-raportin luontiprosessi.  
22. Syötä Päivämäärästä-kenttään päivämäärä 1.1.2000.
    * Määritä raportointikauden aloitus- ja päättymispäivämäärät, joka sisältää aiemmin luodin lomakkeen tapahtumilla.  
23. Lisää Päivämäärään-kenttään päivämäärä 31.12.2022.
    * Määritä raportointikauden aloitus- ja päättymispäivämäärät, joka sisältää aiemmin luodin lomakkeen tapahtumilla.  
24. Valitse Saapumiset-vaihtoehto kentässä Suunta.
25. Valitse Luo tiedosto -kentässä Kyllä.
26. Valitse OK.
    * Tarkasta luotu tuotos ja sen yhteenvetorivit.  
27. Valitse Uusi.
28. Merkitse valittu rivi luettelossa.
29. Valitse Toimitukset-vaihtoehto kentässä Suunta.
30. Syötä tai valitse arvo Nimiketunnus-kentässä.
31. Syötä tai valitse arvo Kauppatavara-kentässä.
32. Aseta painoarvoksi 10.
33. Aseta laskun summaksi 10000.
34. Aseta tilastosummaksi 10000.
35. Valitse Tulostus.
36. Valitse Raportti.
37. Valitse Toimitukset-vaihtoehto kentässä Suunta.
38. Valitse OK.
    * Tarkasta luotu tuotos ja sen yhteenvetorivit. Huomaa, että ne ovat muuttuneet ensimmäiseen ajoon verrattuna.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Tämän konfiguraation suorittaminen vianmääritystilassa kerättyjen laskenta- ja summaustietojen arvioimiseksi
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa solmu "Intrastat model".
3. Laajenna puusta "Intrastat model\Intrastat (DE)"
4. Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
5. Valitse toimintoruudussa Konfiguroinnit.
6. Valitse Käyttäjän parametrit.
7. Valitse Suorita vianmääritystilassa -kentässä Kyllä.
8. Valitse OK.
9. Sulje sivu.
10. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.
11. Valitse Tulostus.
12. Valitse Raportti.
13. Valitse OK.
14. Sulje sivu.
15. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
16. Laajenna puussa solmu "Intrastat model".
17. Laajenna puusta "Intrastat model\Intrastat (DE)"
18. Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
19. Valitse Vianmäärityslokit.
    * Huomaa, että valitun konfiguraation ajoprosessille on luotu vianmäärityslokitietue.  
20. Valitse Liitä.
21. Valitse Avaa.
    * Tarkista luotu XML-tiedosto, joka sisältää laskennan ja summauksen tiedot, jotka on kerättiin valitun konfiguraation ajon aikana.  


