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
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207068"
---
# <a name="end-a-production-order"></a><span data-ttu-id="a8a79-103">Tuotantotilauksen lopetus</span><span class="sxs-lookup"><span data-stu-id="a8a79-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8a79-104">Tässä menettelyssä selvitetään, miten tuotantotilaus päätetään.</span><span class="sxs-lookup"><span data-stu-id="a8a79-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="a8a79-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a8a79-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a8a79-106">Tämä on viimeinen seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="a8a79-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="a8a79-107">Tuotantotilauksen lopetus</span><span class="sxs-lookup"><span data-stu-id="a8a79-107">End a production order</span></span>
1. <span data-ttu-id="a8a79-108">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="a8a79-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="a8a79-109">Valitse tuotantotilaus, jonka tila on Ilmoitettu valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="a8a79-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="a8a79-110">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="a8a79-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="a8a79-111">Valitse Lopetus.</span><span class="sxs-lookup"><span data-stu-id="a8a79-111">Click End.</span></span>
    * <span data-ttu-id="a8a79-112">Voit vahvistaa tällä sivulla, että haluat päättää tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="a8a79-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="a8a79-113">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a8a79-113">Click the General tab.</span></span>
5. <span data-ttu-id="a8a79-114">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a8a79-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="a8a79-115">Valitse Hävikkimenetelmä-kentässä Kohdistus.</span><span class="sxs-lookup"><span data-stu-id="a8a79-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="a8a79-116">Kun valitset kohdistusmenetelmän, materiaalihävikki kustannukset lisätään valmiisiin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="a8a79-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="a8a79-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8a79-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="a8a79-118">Vahvista laskennan tulokset</span><span class="sxs-lookup"><span data-stu-id="a8a79-118">Validate calculation results</span></span>
1. <span data-ttu-id="a8a79-119">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="a8a79-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="a8a79-120">Valitse Näytä kustannusvertailu.</span><span class="sxs-lookup"><span data-stu-id="a8a79-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="a8a79-121">Kun tuotantotilaus on päätetty, voit verrata arvioitua kustannushintaa toteutuneisiin kustannushintaan. Saat tällä tavoin paremman käsityksen tuotannon variansseista.</span><span class="sxs-lookup"><span data-stu-id="a8a79-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
