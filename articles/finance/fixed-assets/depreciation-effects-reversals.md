---
title: Poistojen vaikutukset ja peruutukset
description: Tässä artikkelissa kuvataan käyttöomaisuustapahtuman peruuttamisen mahdolliset vaikutukset.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3c97690956b07a3a5708cfbf37c69f186073138
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995012"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="88178-103">Poistojen vaikutukset ja peruutukset</span><span class="sxs-lookup"><span data-stu-id="88178-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88178-104">Tässä artikkelissa kuvataan käyttöomaisuustapahtuman peruuttamisen mahdolliset vaikutukset.</span><span class="sxs-lookup"><span data-stu-id="88178-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="88178-105">Voit palauttaa käyttöomaisuustapahtumia sekä kyseiseen käyttöomaisuuserään liittyviä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="88178-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="88178-106">Voit myös peruuttaa palautetun tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="88178-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="88178-107">Voit peruuttaa tai palauttaa tapahtuman, joka ei ollut viimeisin omaisuuden kirjaan kirjattu tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="88178-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="88178-108">Määritä ensin, onko poistotapahtumia kirjattu peruutettavan tapahtuman jälkeen.</span><span class="sxs-lookup"><span data-stu-id="88178-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="88178-109">Tämä johtuu siitä, että poistoa ei lasketa uudelleen, kun palautat tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="88178-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="88178-110">Niinpä poisto jää usein liian suureksi tai liian pieneksi peruutuksen jälkeen, kuten esimerkeissä osoitetaan.</span><span class="sxs-lookup"><span data-stu-id="88178-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="88178-111">Voit varmistaa, että poiston määrä säilyy oikeana tapahtumaa palautettaessa, kun et jatka palautustoimintoa, jos näyttöön tulee sanoma, jonka mukaan poistoa ei lasketa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="88178-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="88178-112">Palauta sen sijaan ensin poistotapahtuma, joka on kirjattu palautettavan tapahtuman jälkeen, ja jatka sitten tapahtuman palautusta.</span><span class="sxs-lookup"><span data-stu-id="88178-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="88178-113">Tällöin järjestelmä ei varoita poiston uudelleenlaskennasta ja voit jatkaa palautusta.</span><span class="sxs-lookup"><span data-stu-id="88178-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="88178-114">Seuraavissa esimerkeissä kuvataan laskutoimitukset, joita käytetään, jos jatkat varoitussanomasta huolimatta etkä palauta ensin poistotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="88178-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="88178-115"> Esimerkki 1: Poisto raportoidaan liian suureksi</span><span class="sxs-lookup"><span data-stu-id="88178-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="88178-116">Käyttöomaisuuserälle määritetään viiden vuoden käyttöikä ja tasapoistomenetelmä (60 poistokautta).</span><span class="sxs-lookup"><span data-stu-id="88178-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="88178-117">Tässä esimerkissä poisto raportoidaan liian suureksi.</span><span class="sxs-lookup"><span data-stu-id="88178-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="88178-118">Käyttöomaisuushistoria</span><span class="sxs-lookup"><span data-stu-id="88178-118">Asset transaction history</span></span>

| <span data-ttu-id="88178-119">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="88178-119">Date</span></span>       | <span data-ttu-id="88178-120">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="88178-120">Transaction type</span></span>                                                          | <span data-ttu-id="88178-121">Summa</span><span class="sxs-lookup"><span data-stu-id="88178-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="88178-122">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-122">January 1</span></span>  | <span data-ttu-id="88178-123">Hankinta</span><span class="sxs-lookup"><span data-stu-id="88178-123">Acquisition</span></span>                                                               | <span data-ttu-id="88178-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="88178-124">59,000.00</span></span>                                 |
| <span data-ttu-id="88178-125">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-125">January 1</span></span>  | <span data-ttu-id="88178-126">Hankintaoikaisu</span><span class="sxs-lookup"><span data-stu-id="88178-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="88178-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="88178-127">1,000.00</span></span>                                  |
| <span data-ttu-id="88178-128">31. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-128">January 31</span></span> | <span data-ttu-id="88178-129">Poisto (luodaan yhden poistokauden ehdotuksen avulla)</span><span class="sxs-lookup"><span data-stu-id="88178-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="88178-130">1 000,00Laskelma: kirjanpitoarvo (59 000 + 1 000) / jäljellä olevien poistokausien lukumäärä (60)</span><span class="sxs-lookup"><span data-stu-id="88178-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="88178-131">Peruutustapahtuma</span><span class="sxs-lookup"><span data-stu-id="88178-131">Reversal action</span></span>

| <span data-ttu-id="88178-132">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="88178-132">Date</span></span>      | <span data-ttu-id="88178-133">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="88178-133">Transaction type</span></span>                | <span data-ttu-id="88178-134">Summa</span><span class="sxs-lookup"><span data-stu-id="88178-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="88178-135">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-135">January 1</span></span> | <span data-ttu-id="88178-136">Hankintaoikaisun peruutus</span><span class="sxs-lookup"><span data-stu-id="88178-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="88178-137">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="88178-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="88178-138">Poiston vaikutus</span><span class="sxs-lookup"><span data-stu-id="88178-138">Depreciation effect</span></span>

| <span data-ttu-id="88178-139">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="88178-139">Date</span></span>        | <span data-ttu-id="88178-140">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="88178-140">Transaction type</span></span>        | <span data-ttu-id="88178-141">Summa</span><span class="sxs-lookup"><span data-stu-id="88178-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88178-142">28. helmikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-142">February 28</span></span> | <span data-ttu-id="88178-143">Poisto (ehdotus)</span><span class="sxs-lookup"><span data-stu-id="88178-143">Depreciation (proposal)</span></span> | <span data-ttu-id="88178-144">983,05Laskelma: kirjanpitoarvo (59 000 - 1 000:n poisto) / jäljellä olevien poistokausien lukumäärä (59)</span><span class="sxs-lookup"><span data-stu-id="88178-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="88178-145">Poisto raportoidaan 16,95 yksikköä liian suureksi (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="88178-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="88178-146"> Esimerkki 2: Poisto raportoidaan liian pieneksi</span><span class="sxs-lookup"><span data-stu-id="88178-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="88178-147">Käyttöomaisuuserälle määritetään viiden vuoden käyttöikä ja tasapoistomenetelmä (60 poistokautta).</span><span class="sxs-lookup"><span data-stu-id="88178-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="88178-148">Tässä esimerkissä poisto raportoidaan liian pieneksi.</span><span class="sxs-lookup"><span data-stu-id="88178-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="88178-149">Käyttöomaisuushistoria</span><span class="sxs-lookup"><span data-stu-id="88178-149">Asset transaction history</span></span>

| <span data-ttu-id="88178-150">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="88178-150">Date</span></span>       | <span data-ttu-id="88178-151">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="88178-151">Transaction type</span></span>                                                          | <span data-ttu-id="88178-152">Summa</span><span class="sxs-lookup"><span data-stu-id="88178-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="88178-153">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-153">January 1</span></span>  | <span data-ttu-id="88178-154">Hankinta</span><span class="sxs-lookup"><span data-stu-id="88178-154">Acquisition</span></span>                                                               | <span data-ttu-id="88178-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="88178-155">59,000.00</span></span>                                   |
| <span data-ttu-id="88178-156">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-156">January 1</span></span>  | <span data-ttu-id="88178-157">Kirjanpitoarvon alennus</span><span class="sxs-lookup"><span data-stu-id="88178-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="88178-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="88178-158">1,000.00</span></span>                                    |
| <span data-ttu-id="88178-159">31. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-159">January 31</span></span> | <span data-ttu-id="88178-160">Poisto (luodaan yhden poistokauden ehdotuksen avulla)</span><span class="sxs-lookup"><span data-stu-id="88178-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="88178-161">966,67Laskelma: Kirjanpitoarvo (59 000 - 1 000) / jäljellä olevien poistokausien lukumäärä (60)</span><span class="sxs-lookup"><span data-stu-id="88178-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="88178-162">Peruutustapahtuma</span><span class="sxs-lookup"><span data-stu-id="88178-162">Reversal action</span></span>

| <span data-ttu-id="88178-163">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="88178-163">Date</span></span>      | <span data-ttu-id="88178-164">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="88178-164">Transaction type</span></span>               | <span data-ttu-id="88178-165">Summa</span><span class="sxs-lookup"><span data-stu-id="88178-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="88178-166">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-166">January 1</span></span> | <span data-ttu-id="88178-167">Kirjanpitoarvon alennuksen peruutus</span><span class="sxs-lookup"><span data-stu-id="88178-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="88178-168">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="88178-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="88178-169">Poiston vaikutus</span><span class="sxs-lookup"><span data-stu-id="88178-169">Depreciation effect</span></span>

| <span data-ttu-id="88178-170">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="88178-170">Date</span></span>        | <span data-ttu-id="88178-171">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="88178-171">Transaction type</span></span>        | <span data-ttu-id="88178-172">Summa</span><span class="sxs-lookup"><span data-stu-id="88178-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88178-173">28. helmikuuta</span><span class="sxs-lookup"><span data-stu-id="88178-173">February 28</span></span> | <span data-ttu-id="88178-174">Poisto (ehdotus)</span><span class="sxs-lookup"><span data-stu-id="88178-174">Depreciation (proposal)</span></span> | <span data-ttu-id="88178-175">983,62Laskelma: Kirjanpitoarvo (59 000 - 966,67:n poisto) / jäljellä olevien poistokausien lukumäärä (59)</span><span class="sxs-lookup"><span data-stu-id="88178-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="88178-176">Poisto raportoidaan 16,95 yksikköä liian pieneksi (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="88178-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="88178-177">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="88178-177">Additional resources</span></span>
--------

[<span data-ttu-id="88178-178">Käyttöomaisuuden poisto</span><span class="sxs-lookup"><span data-stu-id="88178-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



