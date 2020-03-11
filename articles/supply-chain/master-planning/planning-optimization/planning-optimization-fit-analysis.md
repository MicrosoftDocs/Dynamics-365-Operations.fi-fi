---
title: Suunnittelun optimoinnin sopivuusanalyysi
description: Tässä ohjeaiheessa käsitellään, miten nykyisten asetusten ja tietojen yhteensopivuus suunnittelun optimointitoiminnon ominaisuuksien kanssa varmistetaan.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 25f3b39d0e6e88eb3f042ab93773e9724528ab0f
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076175"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="247d2-103">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="247d2-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="247d2-104">Voit tarkistaa, kuinka yhteensopivia nykyiset asetukset ja tiedot ovat suunnittelu optimointitoiminnon kanssa valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin sopivuusanalyysi** ja valitse sitten **Suorita analyysi**.</span><span class="sxs-lookup"><span data-stu-id="247d2-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="247d2-105">Jos analyysissa havaitaan ristiriitoja, ne mainitaan samalla sivulla.</span><span class="sxs-lookup"><span data-stu-id="247d2-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="247d2-106">(Analyysin suorittaminen voi kestää muutaman minuutin.)</span><span class="sxs-lookup"><span data-stu-id="247d2-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="247d2-107">Jos ristiriitoja löytyy, suunnittelun optimointia voi silti käyttää.</span><span class="sxs-lookup"><span data-stu-id="247d2-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="247d2-108">Sopivuusanalyysin tulokset vain osoittavat, missä suunnittelupalvelu ei noudata nykyisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="247d2-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="247d2-109">Ne siis näyttävät kohdat, joissa joitakin prosesseja voidaan ohittaa tai joissa niitä ei ehkä tueta.</span><span class="sxs-lookup"><span data-stu-id="247d2-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="247d2-110">Analyysin tulokset: Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="247d2-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="247d2-111">**Toiminto:** Tuotanto</span><span class="sxs-lookup"><span data-stu-id="247d2-111">**Feature:** Production</span></span>
- <span data-ttu-id="247d2-112">**Ongelma:** Nimikkeet, joiden tuoterakenteen taso on suurempi kuin nolla: 56</span><span class="sxs-lookup"><span data-stu-id="247d2-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="247d2-113">**Selitys:** Sopivuusanalyysi löysi 56 nimikettä, joissa on tuotannon tuoterakenteen asetuksia.</span><span class="sxs-lookup"><span data-stu-id="247d2-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="247d2-114">Koska suunnittelun optimoinnin nykyinen versio ei tue tuotantoa, suunnittelun optimointi luo suunniteltuja ostotilauksia eikä suunniteltuja tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="247d2-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="247d2-115">Näkyviin tulee myös varoitus, jossa mainitaan nimikkeet, joita ongelma koskee.</span><span class="sxs-lookup"><span data-stu-id="247d2-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="247d2-116">Analyysin tulokset: Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="247d2-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="247d2-117">**Toiminto:** Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="247d2-117">**Feature:** Actions</span></span>
- <span data-ttu-id="247d2-118">**Ongelma:** Kattavuusryhmät, joissa toimenpidelaskelma on otettu käyttöön: 6</span><span class="sxs-lookup"><span data-stu-id="247d2-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="247d2-119">**Selitys:** Sopivuusanalyysi havaitsi kuusi kattavuusryhmää, joissa toimenpidelaskelma on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="247d2-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="247d2-120">Koska suunnittelun optimoinnin nykyinen versio ei tue toimenpiteitä, toimenpiteitä ei luoda pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="247d2-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="247d2-121">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="247d2-121">Related resources</span></span>

[<span data-ttu-id="247d2-122">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="247d2-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="247d2-123">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="247d2-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="247d2-124">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="247d2-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="247d2-125">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="247d2-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="247d2-126">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="247d2-126">Cancel a planning job</span></span>](cancel-planning-job.md)
