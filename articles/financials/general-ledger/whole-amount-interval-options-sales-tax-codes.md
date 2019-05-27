---
title: Alv-koodien koko summa- ja väli-laskentavaihtoehdot
description: Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16ea19a6d3cfea325281f301e0502bb051381d9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566746"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="63bef-103">Alv-koodien koko summa- ja väli-laskentavaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="63bef-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="63bef-104">Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten.</span><span class="sxs-lookup"><span data-stu-id="63bef-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="63bef-105">Voit määrittää, että alv-koodi lasketaan koko summan tai välisumman perusteella.</span><span class="sxs-lookup"><span data-stu-id="63bef-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="63bef-106">Valitse Arvonlisäverokoodit-sivulla alv-koodin laskentatapa Laskenta-pikavälilehden Laskentatapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63bef-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="63bef-107">Koko summa – veroprosentti kohdistetaan koko verotettavaan summaan.</span><span class="sxs-lookup"><span data-stu-id="63bef-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="63bef-108">Väli – Verotettava summa on jaettu osiin, joista jokainen kuuluu tietyn alv-prosentin alueeseen.</span><span class="sxs-lookup"><span data-stu-id="63bef-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="63bef-109">Määritetylle välille osuvan summan vero lasketaan kyseistä väliä koskevan prosentin mukaan.</span><span class="sxs-lookup"><span data-stu-id="63bef-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="63bef-110">Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.</span><span class="sxs-lookup"><span data-stu-id="63bef-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="63bef-111">Väli-vaihtoehto on käytettävissä vain, jos valitset Kirjanpitoparametrit-sivulla Arvonlisävero-alueen Laskentatapa-kentästä Rivi-vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="63bef-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="63bef-112">Välit määritetään Arvonlisäverokoodin arvot -sivulla syöttämällä kunkin veroprosentin vähimmäis- ja enimmäisrajasummat.</span><span class="sxs-lookup"><span data-stu-id="63bef-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="63bef-113">Jotta verot voidaan laskea kaikille verotettaville summille valitusta laskentatavasta riippumatta, välien on noudatettava seuraavia sääntöjä:</span><span class="sxs-lookup"><span data-stu-id="63bef-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="63bef-114">Ensimmäisen välin vähimmäisraja on oltava 0.</span><span class="sxs-lookup"><span data-stu-id="63bef-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="63bef-115">Viimeisen välin enimmäisrajan on oltava nolla, joka tarkoittaa ääretöntä.</span><span class="sxs-lookup"><span data-stu-id="63bef-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="63bef-116">Välin enimmäisrajan on oltava seuraavan välin vähimmäisraja.</span><span class="sxs-lookup"><span data-stu-id="63bef-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="63bef-117">Jos summa on edellisen välin enimmäisraja ja seuraavan välin vähimmäisraja, summaan käytetään ensimmäisen välin arvonlisäveroprosenttia.</span><span class="sxs-lookup"><span data-stu-id="63bef-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="63bef-118">Jos summa jää enimmäis- ja vähimmäisrajojen määrittämien välien ulkopuolelle, alv-prosentti on 0.</span><span class="sxs-lookup"><span data-stu-id="63bef-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="63bef-119">Esimerkki: Koko summa -laskutapa</span><span class="sxs-lookup"><span data-stu-id="63bef-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="63bef-120">Arvonlisäveron koodi -sivulla arvonlisäveroprosentit määritetään seuraavin välein:</span><span class="sxs-lookup"><span data-stu-id="63bef-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="63bef-121">**Vähimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="63bef-121">**Minimum limit**</span></span> | <span data-ttu-id="63bef-122">**Enimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="63bef-122">**Maximum limit**</span></span> | <span data-ttu-id="63bef-123">**Veroprosentti**</span><span class="sxs-lookup"><span data-stu-id="63bef-123">**Tax rate**</span></span> |
| <span data-ttu-id="63bef-124">0,00</span><span class="sxs-lookup"><span data-stu-id="63bef-124">0.00</span></span>              | <span data-ttu-id="63bef-125">50,00</span><span class="sxs-lookup"><span data-stu-id="63bef-125">50.00</span></span>             | <span data-ttu-id="63bef-126">30 %</span><span class="sxs-lookup"><span data-stu-id="63bef-126">30%</span></span>          |
| <span data-ttu-id="63bef-127">50,00</span><span class="sxs-lookup"><span data-stu-id="63bef-127">50.00</span></span>             | <span data-ttu-id="63bef-128">100,00</span><span class="sxs-lookup"><span data-stu-id="63bef-128">100.00</span></span>            | <span data-ttu-id="63bef-129">20 %</span><span class="sxs-lookup"><span data-stu-id="63bef-129">20%</span></span>          |
| <span data-ttu-id="63bef-130">100,00</span><span class="sxs-lookup"><span data-stu-id="63bef-130">100.00</span></span>            | <span data-ttu-id="63bef-131">0,00</span><span class="sxs-lookup"><span data-stu-id="63bef-131">0.00</span></span>              | <span data-ttu-id="63bef-132">10 %</span><span class="sxs-lookup"><span data-stu-id="63bef-132">10%</span></span>          |

<span data-ttu-id="63bef-133">Arvonlisävero lasketaan koko verotettavasta summasta</span><span class="sxs-lookup"><span data-stu-id="63bef-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="63bef-134">Verotettava summa (hinta)</span><span class="sxs-lookup"><span data-stu-id="63bef-134">Taxable amount (price)</span></span> | <span data-ttu-id="63bef-135">Laskelma</span><span class="sxs-lookup"><span data-stu-id="63bef-135">Calculation</span></span>    | <span data-ttu-id="63bef-136">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="63bef-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="63bef-137">35,00</span><span class="sxs-lookup"><span data-stu-id="63bef-137">35.00</span></span>                  | <span data-ttu-id="63bef-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="63bef-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="63bef-139">10,50</span><span class="sxs-lookup"><span data-stu-id="63bef-139">10.50</span></span>     |
| <span data-ttu-id="63bef-140">50,00</span><span class="sxs-lookup"><span data-stu-id="63bef-140">50.00</span></span>                  | <span data-ttu-id="63bef-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="63bef-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="63bef-142">15,00</span><span class="sxs-lookup"><span data-stu-id="63bef-142">15.00</span></span>     |
| <span data-ttu-id="63bef-143">85,00</span><span class="sxs-lookup"><span data-stu-id="63bef-143">85.00</span></span>                  | <span data-ttu-id="63bef-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="63bef-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="63bef-145">17,00</span><span class="sxs-lookup"><span data-stu-id="63bef-145">17.00</span></span>     |
| <span data-ttu-id="63bef-146">305,00</span><span class="sxs-lookup"><span data-stu-id="63bef-146">305.00</span></span>                 | <span data-ttu-id="63bef-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="63bef-147">305.00 \* 0.10</span></span> | <span data-ttu-id="63bef-148">30,50</span><span class="sxs-lookup"><span data-stu-id="63bef-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="63bef-149"> Esimerkki: Väli-laskentatapa</span><span class="sxs-lookup"><span data-stu-id="63bef-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="63bef-150">Arvonlisäveroprosentit määritetään Arvot-sivulla seuraavin välein:</span><span class="sxs-lookup"><span data-stu-id="63bef-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="63bef-151">**Vähimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="63bef-151">**Minimum limit**</span></span> | <span data-ttu-id="63bef-152">**Enimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="63bef-152">**Maximum limit**</span></span> | <span data-ttu-id="63bef-153">**Veroprosentti**</span><span class="sxs-lookup"><span data-stu-id="63bef-153">**Tax rate**</span></span> |
| <span data-ttu-id="63bef-154">0,00</span><span class="sxs-lookup"><span data-stu-id="63bef-154">0.00</span></span>              | <span data-ttu-id="63bef-155">50,00</span><span class="sxs-lookup"><span data-stu-id="63bef-155">50.00</span></span>             | <span data-ttu-id="63bef-156">30 %</span><span class="sxs-lookup"><span data-stu-id="63bef-156">30%</span></span>          |
| <span data-ttu-id="63bef-157">50,00</span><span class="sxs-lookup"><span data-stu-id="63bef-157">50.00</span></span>             | <span data-ttu-id="63bef-158">100,00</span><span class="sxs-lookup"><span data-stu-id="63bef-158">100.00</span></span>            | <span data-ttu-id="63bef-159">20 %</span><span class="sxs-lookup"><span data-stu-id="63bef-159">20%</span></span>          |
| <span data-ttu-id="63bef-160">100,00</span><span class="sxs-lookup"><span data-stu-id="63bef-160">100.00</span></span>            | <span data-ttu-id="63bef-161">0,00</span><span class="sxs-lookup"><span data-stu-id="63bef-161">0.00</span></span>              | <span data-ttu-id="63bef-162">10 %</span><span class="sxs-lookup"><span data-stu-id="63bef-162">10%</span></span>          |

<span data-ttu-id="63bef-163">Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.</span><span class="sxs-lookup"><span data-stu-id="63bef-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="63bef-164">Verotettava summa (hinta)</span><span class="sxs-lookup"><span data-stu-id="63bef-164">Taxable amount (price)</span></span> | <span data-ttu-id="63bef-165">Laskelma</span><span class="sxs-lookup"><span data-stu-id="63bef-165">Calculation</span></span>                                                               | <span data-ttu-id="63bef-166">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="63bef-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="63bef-167">35,00</span><span class="sxs-lookup"><span data-stu-id="63bef-167">35.00</span></span>                  | <span data-ttu-id="63bef-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="63bef-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="63bef-169">10,50</span><span class="sxs-lookup"><span data-stu-id="63bef-169">10.50</span></span>     |
| <span data-ttu-id="63bef-170">50,00</span><span class="sxs-lookup"><span data-stu-id="63bef-170">50.00</span></span>                  | <span data-ttu-id="63bef-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="63bef-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="63bef-172">15,00</span><span class="sxs-lookup"><span data-stu-id="63bef-172">15.00</span></span>     |
| <span data-ttu-id="63bef-173">85,00</span><span class="sxs-lookup"><span data-stu-id="63bef-173">85.00</span></span>                  | <span data-ttu-id="63bef-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="63bef-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="63bef-175">22,00</span><span class="sxs-lookup"><span data-stu-id="63bef-175">22.00</span></span>     |
| <span data-ttu-id="63bef-176">305,00</span><span class="sxs-lookup"><span data-stu-id="63bef-176">305.00</span></span>                 | <span data-ttu-id="63bef-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="63bef-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="63bef-178">45,50</span><span class="sxs-lookup"><span data-stu-id="63bef-178">45.50</span></span>     |



<span data-ttu-id="63bef-179">Lisätietoja on kohdassa [Arvonlisäveroprosenttien määrittäminen Alv-rajan peruste- ja Laskentatapa-kenttien perusteella](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="63bef-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





