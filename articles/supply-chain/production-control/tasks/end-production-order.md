---
title: Tuotantotilauksen lopetus
description: Tässä menettelyssä selvitetään, miten tuotantotilaus päätetään.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f5cb4afdc0285a6ccf28dbd362df3799c0ecc74
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555836"
---
# <a name="end-a-production-order"></a>Tuotantotilauksen lopetus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä selvitetään, miten tuotantotilaus päätetään. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä on viimeinen seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.


## <a name="end-a-production-order"></a>Tuotantotilauksen lopetus
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
    * Valitse tuotantotilaus, jonka tila on Ilmoitettu valmiiksi.  
2. Valitse toimintoruudussa Tuotantotilaus.
3. Valitse Lopetus.
    * Voit vahvistaa tällä sivulla, että haluat päättää tuotantotilauksen.  
4. Valitse Yleiset-välilehti.
5. Syötä Päivämäärään-kenttään päivämäärä.
6. Valitse Hävikkimenetelmä-kentässä Kohdistus.
    * Kun valitset kohdistusmenetelmän, materiaalihävikki kustannukset lisätään valmiisiin tuotteisiin.  
7. Valitse OK.

## <a name="validate-calculation-results"></a>Vahvista laskennan tulokset
1. Valitse toimintoruudussa Hallitse kustannuksia.
2. Valitse Näytä kustannusvertailu.
    * Kun tuotantotilaus on päätetty, voit verrata arvioitua kustannushintaa toteutuneisiin kustannushintaan. Saat tällä tavoin paremman käsityksen tuotannon variansseista.  
