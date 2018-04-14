---
title: Tuotantotilauksen kustannusarvio
description: "Tämä artikkeli sisältää tietoja tuotannon kustannusarviosta. Tuotannon kustannusarvio sisältää arvioidut materiaalin ja kapasiteetin kulutuksesta aiheutuneet kustannukset, jotka syntyvät kun nimikettä tuotetaan suunniteltu tuotantotilausmäärä."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef5a1b83ad0e6e0ef5c840913ce1a985dba69174
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="production-order-cost-estimation"></a><span data-ttu-id="28e10-104">Tuotantotilauksen kustannusarvio</span><span class="sxs-lookup"><span data-stu-id="28e10-104">Production order cost estimation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="28e10-105">Tämä artikkeli sisältää tietoja tuotannon kustannusarviosta.</span><span class="sxs-lookup"><span data-stu-id="28e10-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="28e10-106">Tuotannon kustannusarvio sisältää arvioidut materiaalin ja kapasiteetin kulutuksesta aiheutuneet kustannukset, jotka syntyvät kun nimikettä tuotetaan suunniteltu tuotantotilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="28e10-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="28e10-107">Tuotantokustannukset on arvioitava tuotantotilauksen luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="28e10-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="28e10-108">Tarkoitus on arvioida tuotantoprosessin nimikkeen ja reitityksen kulutus, koska nämä arviot muodostavat perustan seuraaville ajoitus- ja tuotantoprosesseille.</span><span class="sxs-lookup"><span data-stu-id="28e10-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="28e10-109">Tuotannon kustannusarvio</span><span class="sxs-lookup"><span data-stu-id="28e10-109">Production cost estimation</span></span>
<span data-ttu-id="28e10-110">Tuotantokustannusten arviot perustuvat seuraaviin tietoihin:</span><span class="sxs-lookup"><span data-stu-id="28e10-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="28e10-111">tuotantotilauksen määrä</span><span class="sxs-lookup"><span data-stu-id="28e10-111">The quantity on the production order</span></span>
-   <span data-ttu-id="28e10-112">tuotannon tuoterakenteiden komponentit</span><span class="sxs-lookup"><span data-stu-id="28e10-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="28e10-113">tuotantoreitityksen reititystyövaiheet</span><span class="sxs-lookup"><span data-stu-id="28e10-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="28e10-114">komponenttien ja työvaiheiden epäsuorat kustannukset</span><span class="sxs-lookup"><span data-stu-id="28e10-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="28e10-115">aktiivisten kustannusten tiedot laskentapäivän mukaan.</span><span class="sxs-lookup"><span data-stu-id="28e10-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="28e10-116">Jos tuotannon tuoterakenteissa on haamurivin nimike, laskelmat ovat haamun komponenttien ja reititystyövaiheiden mukaisia.</span><span class="sxs-lookup"><span data-stu-id="28e10-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="28e10-117">Arviointitehtävää voi käyttää laskettaessa arvioidut kustannukset uudelleen niin, että ne vastaavat päivitettyjä tietoja.</span><span class="sxs-lookup"><span data-stu-id="28e10-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="28e10-118">Päivitetyt tiedot voivat olla esimerkiksi muutoksia tuotantotilauksen määrässä, tuotannon tuoterakenteiden komponenteissa, tuotantoreitityksen reititystyövaiheissa, näitä komponentteja ja työvaiheita koskevissa epäsuorissa kustannuksissa tai laskentapäivämäärän mukaisissa aktiivisten kustannusten tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="28e10-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="28e10-119">Arvioitujen kustannusten laskelmat ehdottavat myös tuotantonimikkeelle myyntihintaa, joka perustuu hinta+hinnankorotus-malliin.</span><span class="sxs-lookup"><span data-stu-id="28e10-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="28e10-120">Arvioitujen kustannusten laskelmat voivat koskea vaihtoehtoisesti myös viitetilauksia, jotka vastaavat tuotantotilaukseen linkitettyjä muita tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="28e10-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="28e10-121">Arvioitujen kustannusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="28e10-121">View the estimated costs</span></span>
<span data-ttu-id="28e10-122">Kun arviointi on suoritettu, tulokset näkyvät **Hinnan laskenta** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="28e10-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="28e10-123">Arviointi laskee seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="28e10-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="28e10-124">**Tuotantokustannukset** – Tuotantokustannukset ovat arvion ylimmällä rivillä.</span><span class="sxs-lookup"><span data-stu-id="28e10-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="28e10-125">Rivillä näkyvät kaikki tuotantotilauksen suorittamisesta aiheutuvat kustannukset sekä tuotannon kokonaismyyntihinta.</span><span class="sxs-lookup"><span data-stu-id="28e10-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="28e10-126">Tuotantokustannukset ovat arvion kaikkien kustannusrivien summa.</span><span class="sxs-lookup"><span data-stu-id="28e10-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="28e10-127">**Reitti- tai resurssikustannukset** – Reitti- tai resurssikustannukset ovat tuotannon työvaiheiden kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="28e10-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="28e10-128">Ne sisältävät kustannuksia elementeistä, kuten asetusajasta, ajoajasta ja yleiskustannuksista.</span><span class="sxs-lookup"><span data-stu-id="28e10-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="28e10-129">**Materiaalikustannukset** – Materiaalikustannukset ovat nimikkeen tuottamisessa tarvittavien tuoterakennekomponenttien kustannuksia ja hintoja.</span><span class="sxs-lookup"><span data-stu-id="28e10-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="28e10-130">Nämä kustannukset on määritetty aiemmin järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="28e10-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="28e10-131">Kustannusarvion muita käyttökohteita</span><span class="sxs-lookup"><span data-stu-id="28e10-131">Other uses of cost estimation</span></span>
<span data-ttu-id="28e10-132">Kustannusarvio sisältää myös seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="28e10-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="28e10-133">järkevät hintatarjoukset</span><span class="sxs-lookup"><span data-stu-id="28e10-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="28e10-134">tilauksen kannattavuuden arviointi</span><span class="sxs-lookup"><span data-stu-id="28e10-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="28e10-135">raaka-aineiden käytön arviointi</span><span class="sxs-lookup"><span data-stu-id="28e10-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="28e10-136">aikaisempien tuotantojen kustannustietojen vertailu</span><span class="sxs-lookup"><span data-stu-id="28e10-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="28e10-137">budjetti- ja ennustetiedot</span><span class="sxs-lookup"><span data-stu-id="28e10-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="28e10-138">tietyn kustannustason ylläpitämiseen tarvittavien tuotantokokojen arviointi.</span><span class="sxs-lookup"><span data-stu-id="28e10-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>





