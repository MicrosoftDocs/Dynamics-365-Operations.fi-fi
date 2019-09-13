---
title: Talleta asiakkaan maksuja
description: Talleta asiakkaan maksut.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867771"
---
# <a name="deposit-customer-payments"></a>Talleta asiakkaan maksuja

[!include [task guide banner](../../includes/task-guide-banner.md)]

Talleta asiakkaan maksut. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Maksut > Maksukirjauskansio**.
2. Valitse **Uusi**.
3. Valitse avattavasta **Nimi**-kentästä **CustPay**.
4. Valitse **Rivit**.
5. Valitse **Tili**-kentässä asiakas, jolle maksu kirjataan.
6. Syötä **Kredit**-kenttään maksun summa. Voit jättää summan tyhjäksi, jolloin järjestelmä laskee sen valitsemalla maksetut laskut.  
7. Syötä **Maksuviite**-kenttään arvo. Maksuviite voi olla syöttämäsi maksun sekkinumero. Maksuviite vaaditaan, jotta maksu voidaan sisällyttää talletuskuittiin.  
8. Valitse Käytä talletuskuittia -kohta. Jos maksu halutaan sisällyttää talletukseen, muuta tämän asetuksen arvoksi Kyllä.  
9. Valitse **Uusi**.
10. Valitse **Tili**-kentässä asiakas seuraa maksua varten.
11. Syötä **Kredit**-kenttään maksun summa.
12. Syötä **Maksuviite**-kenttään arvo.
13. Valitse **Käytä talletuskuittia** -kohta.
14. Valitse **Kirjaa**. Maksut on kirjattava, ennen kuin talletuskuitti luodaan. Näin varmistetaan, että maksut eivät muutu talletuskuitin luomisen jälkeen.  
15. Valitse **Toiminnot**.
16. Valitse **Talletuskuitti**.
17. Valitse **OK**. Ensimmäisellä sivulla luodaan talletuskuitti.  
18. Valitse **OK**. Toisessa vaiheessa talletuskuitti tulostetaan. Tämä vaihe ei kuitenkaan ole pakollinen.  

