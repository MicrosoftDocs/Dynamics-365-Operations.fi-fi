---
title: Talleta asiakkaan maksuja
description: Talleta asiakkaan maksut.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565482"
---
# <a name="deposit-customer-payments"></a>Talleta asiakkaan maksuja

[!include [task guide banner](../../includes/task-guide-banner.md)]

Talleta asiakkaan maksut. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
4. Valitse maksukirjauskansio. 
5. Valitse Rivit.
6. Valitse Tili-kentässä asiakas, jolle maksu kirjataan.
7. Syötä Kredit-kenttään maksun summa.
    * Voit jättää summan tyhjäksi, jolloin järjestelmä laskee sen valitsemalla maksetut laskut.  
8. Syötä Maksuviite-kenttään arvo.
    * Maksuviite voi olla syöttämäsi maksun sekkinumero. Maksuviite vaaditaan, jotta maksu voidaan sisällyttää talletuskuittiin.  
9. Valitse Käytä talletuskuittia -kohta.
    * Jos maksu halutaan sisällyttää talletukseen, muuta tämän asetuksen arvoksi Kyllä.  
10. Valitse Uusi.
11. Valitse Tili-kentässä asiakas seuraa maksua varten.
12. Syötä Kredit-kenttään maksun summa.
13. Syötä Maksuviite-kenttään arvo.
14. Valitse Käytä talletuskuittia -kohta.
15. Valitse Kirjaa.
    * Maksut on kirjattava, ennen kuin talletuskuitti luodaan. Näin varmistetaan, että maksut eivät muutu talletuskuitin luomisen jälkeen.  
16. Valitse Toiminnot.
17. Tulosta talletuskuitti.
18. Valitse OK.
    * Ensimmäisellä sivulla luodaan talletuskuitti.  
19. Valitse OK.
    * Toisessa vaiheessa talletuskuitti tulostetaan. Tämä vaihe ei kuitenkaan ole pakollinen.  

