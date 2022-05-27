---
title: Talleta asiakkaan maksuja
description: Talleta asiakkaan maksut.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ed692d9c82fd496e31258a70415db1838d99313
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714030"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
