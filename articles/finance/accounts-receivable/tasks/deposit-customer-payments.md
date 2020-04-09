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
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140174"
---
# <a name="deposit-customer-payments"></a>Talleta asiakkaan maksuja

[!include [banner](../../includes/banner.md)]

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

