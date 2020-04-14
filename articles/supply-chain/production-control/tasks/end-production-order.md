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
ms.openlocfilehash: cb84d3b1908d6be889a49f7386de876cb52141ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149041"
---
# <a name="end-a-production-order"></a>Tuotantotilauksen lopetus

[!include [banner](../../includes/banner.md)]

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
