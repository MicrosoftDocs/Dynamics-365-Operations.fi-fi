---
title: Kerroinpoisto
description: Tämä artikkeli sisältää kerroinpoistomenetelmän yleiskatsauksen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840526"
---
# <a name="factor-depreciation"></a><span data-ttu-id="9da96-103">Kerroinpoisto</span><span class="sxs-lookup"><span data-stu-id="9da96-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9da96-104">Tämä artikkeli sisältää kerroinpoistomenetelmän yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="9da96-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="9da96-105">Kertoimet ovat käyttöomaisuuserien poistamiseen käytettäviä prosenttiosuuksia.</span><span class="sxs-lookup"><span data-stu-id="9da96-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="9da96-106">Kun määrität käyttöomaisuuden poistoprofiilin ja valitset **Poistoprofiilit**-sivulla **Tapa**-kentästä **Kerroin**-vaihtoehdon, voit määrittää nousevan poiston, laskevan poiston tai tasapoiston:</span><span class="sxs-lookup"><span data-stu-id="9da96-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="9da96-107">Nousevassa poistossa poiston määrä kasvaa jokaisella poistokaudella.</span><span class="sxs-lookup"><span data-stu-id="9da96-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="9da96-108">Laskevassa poistossa poiston määrä pienenee ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="9da96-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="9da96-109">Tasapoistossa poisto on sama jokaisella kaudella.</span><span class="sxs-lookup"><span data-stu-id="9da96-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="9da96-110">Seuraavassa on sääntöjä ja esimerkkejä, jotka osoittavat, miten eri poistotyyppien kertoimet voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="9da96-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="9da96-111">Kun valitset **Tapa**-kentästä **Kerroin**-vaihtoehdon, näkyviin tulevat **Kerroin**- ja **Väli**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="9da96-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="9da96-112">Nouseva poisto</span><span class="sxs-lookup"><span data-stu-id="9da96-112">Progressive depreciation</span></span>
<span data-ttu-id="9da96-113">**Kerroin**-kentän arvo on suurempi kuin **50**.</span><span class="sxs-lookup"><span data-stu-id="9da96-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="9da96-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="9da96-114">Example</span></span>

<span data-ttu-id="9da96-115">Hankintahinta on 100 000, kerroin on 70, käyttöikä on 10 vuotta ja poisto alkaa 1.1.</span><span class="sxs-lookup"><span data-stu-id="9da96-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="9da96-116">Poistosummat ja nettokirjanpitoarvon summat näytetään vain ensimmäisen kuuden vuoden käyttöiän osalta.</span><span class="sxs-lookup"><span data-stu-id="9da96-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="9da96-117">Vuosi(a)</span><span class="sxs-lookup"><span data-stu-id="9da96-117">Year</span></span> | <span data-ttu-id="9da96-118">Kausi</span><span class="sxs-lookup"><span data-stu-id="9da96-118">Period</span></span>      | <span data-ttu-id="9da96-119">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="9da96-119">Depreciation amount</span></span> | <span data-ttu-id="9da96-120">Nettokirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="9da96-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="9da96-121">1</span><span class="sxs-lookup"><span data-stu-id="9da96-121">1</span></span>    | <span data-ttu-id="9da96-122">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-122">December 31</span></span> | <span data-ttu-id="9da96-123">307,69</span><span class="sxs-lookup"><span data-stu-id="9da96-123">307.69</span></span>              | <span data-ttu-id="9da96-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="9da96-124">99,692.31</span></span>             |
| <span data-ttu-id="9da96-125">2</span><span class="sxs-lookup"><span data-stu-id="9da96-125">2</span></span>    | <span data-ttu-id="9da96-126">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-126">December 31</span></span> | <span data-ttu-id="9da96-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="9da96-127">1,447.21</span></span>            | <span data-ttu-id="9da96-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="9da96-128">98,245.10</span></span>             |
| <span data-ttu-id="9da96-129">3</span><span class="sxs-lookup"><span data-stu-id="9da96-129">3</span></span>    | <span data-ttu-id="9da96-130">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-130">December 31</span></span> | <span data-ttu-id="9da96-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="9da96-131">3,104.50</span></span>            | <span data-ttu-id="9da96-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="9da96-132">95,140.60</span></span>             |
| <span data-ttu-id="9da96-133">4</span><span class="sxs-lookup"><span data-stu-id="9da96-133">4</span></span>    | <span data-ttu-id="9da96-134">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-134">December 31</span></span> | <span data-ttu-id="9da96-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="9da96-135">5,150.21</span></span>            | <span data-ttu-id="9da96-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="9da96-136">89,990.39</span></span>             |
| <span data-ttu-id="9da96-137">5</span><span class="sxs-lookup"><span data-stu-id="9da96-137">5</span></span>    | <span data-ttu-id="9da96-138">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-138">December 31</span></span> | <span data-ttu-id="9da96-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="9da96-139">7,522.95</span></span>            | <span data-ttu-id="9da96-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="9da96-140">82,467.44</span></span>             |
| <span data-ttu-id="9da96-141">6</span><span class="sxs-lookup"><span data-stu-id="9da96-141">6</span></span>    | <span data-ttu-id="9da96-142">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-142">December 31</span></span> | <span data-ttu-id="9da96-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="9da96-143">10,184.06</span></span>           | <span data-ttu-id="9da96-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="9da96-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="9da96-145">Laskeva poisto</span><span class="sxs-lookup"><span data-stu-id="9da96-145">Digressive depreciation</span></span>
<span data-ttu-id="9da96-146">**Kerroin**-kentän arvo on pienempi kuin **50**.</span><span class="sxs-lookup"><span data-stu-id="9da96-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="9da96-147">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="9da96-147">Example</span></span>

<span data-ttu-id="9da96-148">Hankintahinta on 100 000, kerroin on 20, käyttöikä on 10 vuotta ja poisto alkaa 1.1.</span><span class="sxs-lookup"><span data-stu-id="9da96-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="9da96-149">Poistosummat ja nettokirjanpitoarvon summat näytetään vain ensimmäisen kuuden vuoden käyttöiän osalta.</span><span class="sxs-lookup"><span data-stu-id="9da96-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="9da96-150">Vuosi(a)</span><span class="sxs-lookup"><span data-stu-id="9da96-150">Year</span></span> | <span data-ttu-id="9da96-151">Kausi</span><span class="sxs-lookup"><span data-stu-id="9da96-151">Period</span></span>      | <span data-ttu-id="9da96-152">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="9da96-152">Depreciation amount</span></span> | <span data-ttu-id="9da96-153">Nettokirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="9da96-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="9da96-154">1</span><span class="sxs-lookup"><span data-stu-id="9da96-154">1</span></span>    | <span data-ttu-id="9da96-155">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-155">December 31</span></span> | <span data-ttu-id="9da96-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="9da96-156">56,080.43</span></span>           | <span data-ttu-id="9da96-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="9da96-157">43,919.57</span></span>             |
| <span data-ttu-id="9da96-158">2</span><span class="sxs-lookup"><span data-stu-id="9da96-158">2</span></span>    | <span data-ttu-id="9da96-159">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-159">December 31</span></span> | <span data-ttu-id="9da96-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="9da96-160">10,665.70</span></span>           | <span data-ttu-id="9da96-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="9da96-161">33,253.87</span></span>             |
| <span data-ttu-id="9da96-162">3</span><span class="sxs-lookup"><span data-stu-id="9da96-162">3</span></span>    | <span data-ttu-id="9da96-163">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-163">December 31</span></span> | <span data-ttu-id="9da96-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="9da96-164">7,156.22</span></span>            | <span data-ttu-id="9da96-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="9da96-165">26,097.65</span></span>             |
| <span data-ttu-id="9da96-166">4</span><span class="sxs-lookup"><span data-stu-id="9da96-166">4</span></span>    | <span data-ttu-id="9da96-167">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-167">December 31</span></span> | <span data-ttu-id="9da96-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="9da96-168">5,538.06</span></span>            | <span data-ttu-id="9da96-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="9da96-169">20,559.59</span></span>             |
| <span data-ttu-id="9da96-170">5</span><span class="sxs-lookup"><span data-stu-id="9da96-170">5</span></span>    | <span data-ttu-id="9da96-171">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-171">December 31</span></span> | <span data-ttu-id="9da96-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="9da96-172">4,579.89</span></span>            | <span data-ttu-id="9da96-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="9da96-173">15,979.70</span></span>             |
| <span data-ttu-id="9da96-174">6</span><span class="sxs-lookup"><span data-stu-id="9da96-174">6</span></span>    | <span data-ttu-id="9da96-175">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="9da96-175">December 31</span></span> | <span data-ttu-id="9da96-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="9da96-176">3,937.36</span></span>            | <span data-ttu-id="9da96-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="9da96-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="9da96-178">Tasapoisto</span><span class="sxs-lookup"><span data-stu-id="9da96-178">Straight line depreciation</span></span>
<span data-ttu-id="9da96-179">**Kerroin**-kentän arvo on yhtä suuri kuin **50**.</span><span class="sxs-lookup"><span data-stu-id="9da96-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="9da96-180">Poistosumma on tällöin sama jokaisella kaudella. Muiden kenttien valintojen merkitykset tulisi ottaa huomioon. Nämä on kuvattu ohjeaiheessa [Käyttöikään perustuva tasapoisto](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="9da96-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



