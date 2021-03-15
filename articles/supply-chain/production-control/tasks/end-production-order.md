---
title: Tuotantotilauksen lopetus
description: Tässä menettelyssä selvitetään, miten tuotantotilaus päätetään.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f3e121fdc0f69ace15e0fa08bde0af739ef7d28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977810"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]