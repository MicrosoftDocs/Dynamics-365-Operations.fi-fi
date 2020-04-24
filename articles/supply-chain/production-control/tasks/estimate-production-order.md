---
title: Arvioi tuotantotilaus
description: Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omaa tietojoukkoa.
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
ms.openlocfilehash: 5bbb541a09809c1f1bfada42094d840a2f6e7764
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207045"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="7949c-103">Arvioi tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="7949c-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7949c-104">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omaa tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="7949c-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="7949c-105">Molemmissa tapauksissa sinulla on oltava avoin tuotantotilaus, jonka tila on Luotu.</span><span class="sxs-lookup"><span data-stu-id="7949c-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="7949c-106">Tämä on toinen seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="7949c-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="7949c-107">Arvioi tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="7949c-107">Estimate a production order</span></span>
1. <span data-ttu-id="7949c-108">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="7949c-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="7949c-109">Valitse ruudukossa tuotantotilaus, jonka tila on Luotu</span><span class="sxs-lookup"><span data-stu-id="7949c-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="7949c-110">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="7949c-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="7949c-111">Valitse Arvio.</span><span class="sxs-lookup"><span data-stu-id="7949c-111">Click Estimate.</span></span>
    * <span data-ttu-id="7949c-112">Tässä vaiheessa lasketaan yhden tuotantotilauksen arvioidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7949c-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="7949c-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7949c-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="7949c-114">Näytä laskennan tiedot</span><span class="sxs-lookup"><span data-stu-id="7949c-114">View the calculation details</span></span>
1. <span data-ttu-id="7949c-115">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="7949c-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="7949c-116">Valitse Näytä laskennan tiedot.</span><span class="sxs-lookup"><span data-stu-id="7949c-116">Click View calculation details.</span></span>
    * <span data-ttu-id="7949c-117">Kustannuserittely näkyy tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="7949c-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="7949c-118">Voit esimerkiksi tarkastella ensimmäisellä rivillä valmiin tuotteen yksikkökohtaista kokonaiskustannushintaa.</span><span class="sxs-lookup"><span data-stu-id="7949c-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="7949c-119">Seuraavilla riveillä on tuoterakenteen ja tuotantoreitin kustannukset sekä välilliset kustannukset.</span><span class="sxs-lookup"><span data-stu-id="7949c-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
