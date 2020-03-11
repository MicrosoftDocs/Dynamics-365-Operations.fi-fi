---
title: Suunnittelu negatiivisilla käytettävissä olevalla määrillä
description: Tässä ohjeaiheessa kerrotaan, miten negatiivista käytettävissä olevaa määrää käsitellään suunnittelun optimoinnissa.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca12d13f7318f649cb1dbc0f7c3cf56502c9d3ea
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077481"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="d8079-103">Suunnittelu negatiivisilla käytettävissä olevalla määrillä</span><span class="sxs-lookup"><span data-stu-id="d8079-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8079-104">Jos järjestelmässä näkyy negatiivinen käytettävissä oleva koostettu määrä, suunnittelumoduuli käsittelee määrää arvona 0 (nolla), mikä helpottaa ylitarjonnan välttämistä.</span><span class="sxs-lookup"><span data-stu-id="d8079-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="d8079-105">Tämä toiminto toimii seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d8079-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="d8079-106">Suunnittelun optimointitoiminto koostaa käytettävissä olevat määrät kattavuusdimensioiden alimmalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="d8079-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="d8079-107">(Jos esimerkiksi *sijainti* ei ole kattavuusdimensio, suunnittelun optimointi koostaa käytettävissä olevat määrät *varaston* tasolla.)</span><span class="sxs-lookup"><span data-stu-id="d8079-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="d8079-108">Jos kattavuusdimensioiden alimman tason koostettu kokonaismäärä on negatiivinen, järjestelmä olettaa, että käytettävissä oleva määrä on todella 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="d8079-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8079-109">Suunnittelujärjestelmän tarkkuus on sama kuin syöttötietojen tarkkuus.</span><span class="sxs-lookup"><span data-stu-id="d8079-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="d8079-110">Jos syöttötiedot ovat virheellisiä, negatiiviset käytettävissä olevat tietueet osoittavat, että varaston tietoja ei ole synkronoitu Microsoft Dynamics 365 Supply Chain Management -sovelluksessa todellisen tilanteen kanssa.</span><span class="sxs-lookup"><span data-stu-id="d8079-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="d8079-111">Suunnittelun tulos on siis virheellinen.</span><span class="sxs-lookup"><span data-stu-id="d8079-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="d8079-112">Jos haluat tarkan suunnittelun tuloksen, minimoi negatiivista käytettävissä olevaa määrää näyttävien tietueiden määrä.</span><span class="sxs-lookup"><span data-stu-id="d8079-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="d8079-113">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="d8079-113">Example 1</span></span>

<span data-ttu-id="d8079-114">Varasto 13 on määritetty seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="d8079-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="d8079-115">**Kattavuuskoodi:** Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="d8079-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="d8079-116">**Minimi:** 15 kappaletta (kpl)</span><span class="sxs-lookup"><span data-stu-id="d8079-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="d8079-117">**Maksimi:** 25 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="d8079-118">Kattavuusdimension alin taso on *varasto*. Seuraavat käytettävissä olevat määrät tallennetaan *sijainnin* tasolle:</span><span class="sxs-lookup"><span data-stu-id="d8079-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="d8079-119">**Toimipaikka 1, varasto 13, sijainti 1:** 20 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="d8079-120">**Toimipaikan 1 varasto 13, sijainti 2:** &minus;8 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="d8079-121">Tämän vuoksi varaston 13 käytettävissä oleva koostettu määrä on 12 kpl.</span><span class="sxs-lookup"><span data-stu-id="d8079-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="d8079-122">(= 20 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-122">(= 20 pcs.</span></span> <span data-ttu-id="d8079-123">&minus; 8 kpl).</span><span class="sxs-lookup"><span data-stu-id="d8079-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="d8079-124">Tässä tapauksessa suunnittelumoduuli käyttää käytettävissä olevan varaston koostetta, joka on 12 kpl.</span><span class="sxs-lookup"><span data-stu-id="d8079-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="d8079-125">varastolle 13.</span><span class="sxs-lookup"><span data-stu-id="d8079-125">for warehouse 13.</span></span>

<span data-ttu-id="d8079-126">Tuloksena on 13 kappaleen suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="d8079-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="d8079-127">(= 25 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-127">(= 25 pcs.</span></span> <span data-ttu-id="d8079-128">&minus; 12 kpl) ja täyttää varaston 13 käyttämällä 12 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="d8079-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="d8079-129">25 kappaleeseen asti</span><span class="sxs-lookup"><span data-stu-id="d8079-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="d8079-130">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="d8079-130">Example 2</span></span>

<span data-ttu-id="d8079-131">Varasto 13 on määritetty seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="d8079-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="d8079-132">**Kattavuuskoodi:** Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="d8079-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="d8079-133">**Minimi:** 15 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="d8079-134">**Maksimi:** 25 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="d8079-135">Kattavuusdimension alin taso on *varasto*. Seuraavat käytettävissä olevat määrät tallennetaan *sijainnin* tasolle:</span><span class="sxs-lookup"><span data-stu-id="d8079-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="d8079-136">**Toimipaikka 1, varasto 13, sijainti 1:** 4 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="d8079-137">**Toimipaikan 1 varasto 13, sijainti 2:** &minus;8 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="d8079-138">Tämän vuoksi varaston 13 käytettävissä oleva koostettu määrä on &minus;4 kpl.</span><span class="sxs-lookup"><span data-stu-id="d8079-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="d8079-139">(= 4 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-139">(= 4 pcs.</span></span> <span data-ttu-id="d8079-140">&minus; 8 kpl).</span><span class="sxs-lookup"><span data-stu-id="d8079-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="d8079-141">Se on toisin sanoen pienempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="d8079-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="d8079-142">Tässä tapauksessa suunnittelumoduuli olettaa, että varaston 13 käytettävissä oleva määrä on 0 kpl.</span><span class="sxs-lookup"><span data-stu-id="d8079-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="d8079-143">sen sijaan, että se olisi &minus;4 kpl.</span><span class="sxs-lookup"><span data-stu-id="d8079-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="d8079-144">Tuloksena on 25 kappaleen suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="d8079-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="d8079-145">(= 25 kpl</span><span class="sxs-lookup"><span data-stu-id="d8079-145">(= 25 pcs.</span></span> <span data-ttu-id="d8079-146">&minus; 0 kpl) ja täyttää varaston 13 käyttämällä 0 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="d8079-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="d8079-147">25 kappaleeseen asti</span><span class="sxs-lookup"><span data-stu-id="d8079-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d8079-148">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="d8079-148">Related resources</span></span>

[<span data-ttu-id="d8079-149">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d8079-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="d8079-150">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="d8079-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="d8079-151">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="d8079-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="d8079-152">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="d8079-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="d8079-153">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="d8079-153">Cancel a planning job</span></span>](cancel-planning-job.md)