---
title: Kerroinpoisto
description: "Tämä artikkeli sisältää kerroinpoistomenetelmän yleiskatsauksen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6e7eb5c924f27446fcba9b0f340b7110dbdaab8b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="factor-depreciation"></a><span data-ttu-id="7f56c-103">Kerroinpoisto</span><span class="sxs-lookup"><span data-stu-id="7f56c-103">Factor depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="7f56c-104">Tämä artikkeli sisältää kerroinpoistomenetelmän yleiskatsauksen.</span><span class="sxs-lookup"><span data-stu-id="7f56c-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="7f56c-105">Kertoimet ovat käyttöomaisuuserien poistamiseen käytettäviä prosenttiosuuksia.</span><span class="sxs-lookup"><span data-stu-id="7f56c-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="7f56c-106">Kun määrität käyttöomaisuuden poistoprofiilin ja valitset **Poistoprofiilit**-sivulla **Tapa**-kentästä **Kerroin**-vaihtoehdon, voit määrittää nousevan poiston, laskevan poiston tai tasapoiston:</span><span class="sxs-lookup"><span data-stu-id="7f56c-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="7f56c-107">Nousevassa poistossa poiston määrä kasvaa jokaisella poistokaudella.</span><span class="sxs-lookup"><span data-stu-id="7f56c-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="7f56c-108">Laskevassa poistossa poiston määrä pienenee ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="7f56c-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="7f56c-109">Tasapoistossa poisto on sama jokaisella kaudella.</span><span class="sxs-lookup"><span data-stu-id="7f56c-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="7f56c-110">Seuraavassa on sääntöjä ja esimerkkejä, jotka osoittavat, miten eri poistotyyppien kertoimet voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="7f56c-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7f56c-111">Kun valitset **Tapa**-kentästä **Kerroin**-vaihtoehdon, näkyviin tulevat **Kerroin**- ja **Väli**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="7f56c-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="7f56c-112">Nouseva poisto</span><span class="sxs-lookup"><span data-stu-id="7f56c-112">Progressive depreciation</span></span>
<span data-ttu-id="7f56c-113">**Kerroin**-kentän arvo on suurempi kuin **50**.</span><span class="sxs-lookup"><span data-stu-id="7f56c-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="7f56c-114">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7f56c-114">Example</span></span>

<span data-ttu-id="7f56c-115">Hankintahinta on 100 000, kerroin on 70, käyttöikä on 10 vuotta ja poisto alkaa 1.1.</span><span class="sxs-lookup"><span data-stu-id="7f56c-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="7f56c-116">Poistosummat ja nettokirjanpitoarvon summat näytetään vain ensimmäisen kuuden vuoden käyttöiän osalta.</span><span class="sxs-lookup"><span data-stu-id="7f56c-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="7f56c-117">Vuosi(a)</span><span class="sxs-lookup"><span data-stu-id="7f56c-117">Year</span></span> | <span data-ttu-id="7f56c-118">Kausi</span><span class="sxs-lookup"><span data-stu-id="7f56c-118">Period</span></span>      | <span data-ttu-id="7f56c-119">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="7f56c-119">Depreciation amount</span></span> | <span data-ttu-id="7f56c-120">Nettokirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="7f56c-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="7f56c-121">1</span><span class="sxs-lookup"><span data-stu-id="7f56c-121">1</span></span>    | <span data-ttu-id="7f56c-122">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-122">December 31</span></span> | <span data-ttu-id="7f56c-123">307,69</span><span class="sxs-lookup"><span data-stu-id="7f56c-123">307.69</span></span>              | <span data-ttu-id="7f56c-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="7f56c-124">99,692.31</span></span>             |
| <span data-ttu-id="7f56c-125">2</span><span class="sxs-lookup"><span data-stu-id="7f56c-125">2</span></span>    | <span data-ttu-id="7f56c-126">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-126">December 31</span></span> | <span data-ttu-id="7f56c-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="7f56c-127">1,447.21</span></span>            | <span data-ttu-id="7f56c-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="7f56c-128">98,245.10</span></span>             |
| <span data-ttu-id="7f56c-129">3</span><span class="sxs-lookup"><span data-stu-id="7f56c-129">3</span></span>    | <span data-ttu-id="7f56c-130">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-130">December 31</span></span> | <span data-ttu-id="7f56c-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="7f56c-131">3,104.50</span></span>            | <span data-ttu-id="7f56c-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="7f56c-132">95,140.60</span></span>             |
| <span data-ttu-id="7f56c-133">4</span><span class="sxs-lookup"><span data-stu-id="7f56c-133">4</span></span>    | <span data-ttu-id="7f56c-134">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-134">December 31</span></span> | <span data-ttu-id="7f56c-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="7f56c-135">5,150.21</span></span>            | <span data-ttu-id="7f56c-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="7f56c-136">89,990.39</span></span>             |
| <span data-ttu-id="7f56c-137">5</span><span class="sxs-lookup"><span data-stu-id="7f56c-137">5</span></span>    | <span data-ttu-id="7f56c-138">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-138">December 31</span></span> | <span data-ttu-id="7f56c-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="7f56c-139">7,522.95</span></span>            | <span data-ttu-id="7f56c-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="7f56c-140">82,467.44</span></span>             |
| <span data-ttu-id="7f56c-141">6</span><span class="sxs-lookup"><span data-stu-id="7f56c-141">6</span></span>    | <span data-ttu-id="7f56c-142">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-142">December 31</span></span> | <span data-ttu-id="7f56c-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="7f56c-143">10,184.06</span></span>           | <span data-ttu-id="7f56c-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="7f56c-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="7f56c-145">Laskeva poisto</span><span class="sxs-lookup"><span data-stu-id="7f56c-145">Digressive depreciation</span></span>
<span data-ttu-id="7f56c-146">**Kerroin**-kentän arvo on pienempi kuin **50**.</span><span class="sxs-lookup"><span data-stu-id="7f56c-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="7f56c-147">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7f56c-147">Example</span></span>

<span data-ttu-id="7f56c-148">Hankintahinta on 100 000, kerroin on 20, käyttöikä on 10 vuotta ja poisto alkaa 1.1.</span><span class="sxs-lookup"><span data-stu-id="7f56c-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="7f56c-149">Poistosummat ja nettokirjanpitoarvon summat näytetään vain ensimmäisen kuuden vuoden käyttöiän osalta.</span><span class="sxs-lookup"><span data-stu-id="7f56c-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="7f56c-150">Vuosi(a)</span><span class="sxs-lookup"><span data-stu-id="7f56c-150">Year</span></span> | <span data-ttu-id="7f56c-151">Kausi</span><span class="sxs-lookup"><span data-stu-id="7f56c-151">Period</span></span>      | <span data-ttu-id="7f56c-152">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="7f56c-152">Depreciation amount</span></span> | <span data-ttu-id="7f56c-153">Nettokirjanpitoarvo</span><span class="sxs-lookup"><span data-stu-id="7f56c-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="7f56c-154">1</span><span class="sxs-lookup"><span data-stu-id="7f56c-154">1</span></span>    | <span data-ttu-id="7f56c-155">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-155">December 31</span></span> | <span data-ttu-id="7f56c-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="7f56c-156">56,080.43</span></span>           | <span data-ttu-id="7f56c-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="7f56c-157">43,919.57</span></span>             |
| <span data-ttu-id="7f56c-158">2</span><span class="sxs-lookup"><span data-stu-id="7f56c-158">2</span></span>    | <span data-ttu-id="7f56c-159">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-159">December 31</span></span> | <span data-ttu-id="7f56c-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="7f56c-160">10,665.70</span></span>           | <span data-ttu-id="7f56c-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="7f56c-161">33,253.87</span></span>             |
| <span data-ttu-id="7f56c-162">3</span><span class="sxs-lookup"><span data-stu-id="7f56c-162">3</span></span>    | <span data-ttu-id="7f56c-163">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-163">December 31</span></span> | <span data-ttu-id="7f56c-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="7f56c-164">7,156.22</span></span>            | <span data-ttu-id="7f56c-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="7f56c-165">26,097.65</span></span>             |
| <span data-ttu-id="7f56c-166">4</span><span class="sxs-lookup"><span data-stu-id="7f56c-166">4</span></span>    | <span data-ttu-id="7f56c-167">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-167">December 31</span></span> | <span data-ttu-id="7f56c-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="7f56c-168">5,538.06</span></span>            | <span data-ttu-id="7f56c-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="7f56c-169">20,559.59</span></span>             |
| <span data-ttu-id="7f56c-170">5</span><span class="sxs-lookup"><span data-stu-id="7f56c-170">5</span></span>    | <span data-ttu-id="7f56c-171">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-171">December 31</span></span> | <span data-ttu-id="7f56c-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="7f56c-172">4,579.89</span></span>            | <span data-ttu-id="7f56c-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="7f56c-173">15,979.70</span></span>             |
| <span data-ttu-id="7f56c-174">6</span><span class="sxs-lookup"><span data-stu-id="7f56c-174">6</span></span>    | <span data-ttu-id="7f56c-175">31. joulukuuta</span><span class="sxs-lookup"><span data-stu-id="7f56c-175">December 31</span></span> | <span data-ttu-id="7f56c-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="7f56c-176">3,937.36</span></span>            | <span data-ttu-id="7f56c-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="7f56c-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="7f56c-178">Tasapoisto</span><span class="sxs-lookup"><span data-stu-id="7f56c-178">Straight line depreciation</span></span>
<span data-ttu-id="7f56c-179">**Kerroin**-kentän arvo on yhtä suuri kuin **50**.</span><span class="sxs-lookup"><span data-stu-id="7f56c-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="7f56c-180">Poistosumma on tällöin sama jokaisella kaudella. Muiden kenttien valintojen merkitykset tulisi ottaa huomioon. Nämä on kuvattu ohjeaiheessa [Käyttöikään perustuva tasapoisto](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="7f56c-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




