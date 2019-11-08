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
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc998ddc2f654afba778c8c3af85dce37d3c3427
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570168"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="68b81-103">Alv-koodien koko summa- ja väli-laskentavaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="68b81-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68b81-104">Tässä artikkelissa kuvataan arvonlisäverokoodien Laskentatapa-kentän asetuksia ja sitä, miten arvonlisävero lasketaan välejä ja koko summia varten.</span><span class="sxs-lookup"><span data-stu-id="68b81-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="68b81-105">Voit määrittää, että alv-koodi lasketaan koko summan tai välisumman perusteella.</span><span class="sxs-lookup"><span data-stu-id="68b81-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="68b81-106">Valitse Arvonlisäverokoodit-sivulla alv-koodin laskentatapa Laskenta-pikavälilehden Laskentatapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="68b81-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="68b81-107">Koko summa – veroprosentti kohdistetaan koko verotettavaan summaan.</span><span class="sxs-lookup"><span data-stu-id="68b81-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="68b81-108">Väli – Verotettava summa on jaettu osiin, joista jokainen kuuluu tietyn alv-prosentin alueeseen.</span><span class="sxs-lookup"><span data-stu-id="68b81-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="68b81-109">Määritetylle välille osuvan summan vero lasketaan kyseistä väliä koskevan prosentin mukaan.</span><span class="sxs-lookup"><span data-stu-id="68b81-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="68b81-110">Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.</span><span class="sxs-lookup"><span data-stu-id="68b81-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="68b81-111">Väli-vaihtoehto on käytettävissä vain, jos valitset Kirjanpitoparametrit-sivulla Arvonlisävero-alueen Laskentatapa-kentästä Rivi-vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="68b81-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="68b81-112">Välit määritetään Arvonlisäverokoodin arvot -sivulla syöttämällä kunkin veroprosentin vähimmäis- ja enimmäisrajasummat.</span><span class="sxs-lookup"><span data-stu-id="68b81-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="68b81-113">Jotta verot voidaan laskea kaikille verotettaville summille valitusta laskentatavasta riippumatta, välien on noudatettava seuraavia sääntöjä:</span><span class="sxs-lookup"><span data-stu-id="68b81-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="68b81-114">Ensimmäisen välin vähimmäisraja on oltava 0.</span><span class="sxs-lookup"><span data-stu-id="68b81-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="68b81-115">Viimeisen välin enimmäisrajan on oltava nolla, joka tarkoittaa ääretöntä.</span><span class="sxs-lookup"><span data-stu-id="68b81-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="68b81-116">Välin enimmäisrajan on oltava seuraavan välin vähimmäisraja.</span><span class="sxs-lookup"><span data-stu-id="68b81-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="68b81-117">Jos summa on edellisen välin enimmäisraja ja seuraavan välin vähimmäisraja, summaan käytetään ensimmäisen välin arvonlisäveroprosenttia.</span><span class="sxs-lookup"><span data-stu-id="68b81-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="68b81-118">Jos summa jää enimmäis- ja vähimmäisrajojen määrittämien välien ulkopuolelle, alv-prosentti on 0.</span><span class="sxs-lookup"><span data-stu-id="68b81-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="68b81-119">Esimerkki: Koko summa -laskutapa</span><span class="sxs-lookup"><span data-stu-id="68b81-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="68b81-120">Arvonlisäveron koodi -sivulla arvonlisäveroprosentit määritetään seuraavin välein:</span><span class="sxs-lookup"><span data-stu-id="68b81-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="68b81-121">**Vähimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="68b81-121">**Minimum limit**</span></span> | <span data-ttu-id="68b81-122">**Enimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="68b81-122">**Maximum limit**</span></span> | <span data-ttu-id="68b81-123">**Veroprosentti**</span><span class="sxs-lookup"><span data-stu-id="68b81-123">**Tax rate**</span></span> |
| <span data-ttu-id="68b81-124">0,00</span><span class="sxs-lookup"><span data-stu-id="68b81-124">0.00</span></span>              | <span data-ttu-id="68b81-125">50,00</span><span class="sxs-lookup"><span data-stu-id="68b81-125">50.00</span></span>             | <span data-ttu-id="68b81-126">30 %</span><span class="sxs-lookup"><span data-stu-id="68b81-126">30%</span></span>          |
| <span data-ttu-id="68b81-127">50,00</span><span class="sxs-lookup"><span data-stu-id="68b81-127">50.00</span></span>             | <span data-ttu-id="68b81-128">100,00</span><span class="sxs-lookup"><span data-stu-id="68b81-128">100.00</span></span>            | <span data-ttu-id="68b81-129">20 %</span><span class="sxs-lookup"><span data-stu-id="68b81-129">20%</span></span>          |
| <span data-ttu-id="68b81-130">100,00</span><span class="sxs-lookup"><span data-stu-id="68b81-130">100.00</span></span>            | <span data-ttu-id="68b81-131">0,00</span><span class="sxs-lookup"><span data-stu-id="68b81-131">0.00</span></span>              | <span data-ttu-id="68b81-132">10 %</span><span class="sxs-lookup"><span data-stu-id="68b81-132">10%</span></span>          |

<span data-ttu-id="68b81-133">Arvonlisävero lasketaan koko verotettavasta summasta</span><span class="sxs-lookup"><span data-stu-id="68b81-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="68b81-134">Verotettava summa (hinta)</span><span class="sxs-lookup"><span data-stu-id="68b81-134">Taxable amount (price)</span></span> | <span data-ttu-id="68b81-135">Laskelma</span><span class="sxs-lookup"><span data-stu-id="68b81-135">Calculation</span></span>    | <span data-ttu-id="68b81-136">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="68b81-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="68b81-137">35,00</span><span class="sxs-lookup"><span data-stu-id="68b81-137">35.00</span></span>                  | <span data-ttu-id="68b81-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="68b81-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="68b81-139">10,50</span><span class="sxs-lookup"><span data-stu-id="68b81-139">10.50</span></span>     |
| <span data-ttu-id="68b81-140">50,00</span><span class="sxs-lookup"><span data-stu-id="68b81-140">50.00</span></span>                  | <span data-ttu-id="68b81-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="68b81-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="68b81-142">15,00</span><span class="sxs-lookup"><span data-stu-id="68b81-142">15.00</span></span>     |
| <span data-ttu-id="68b81-143">85,00</span><span class="sxs-lookup"><span data-stu-id="68b81-143">85.00</span></span>                  | <span data-ttu-id="68b81-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="68b81-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="68b81-145">17,00</span><span class="sxs-lookup"><span data-stu-id="68b81-145">17.00</span></span>     |
| <span data-ttu-id="68b81-146">305,00</span><span class="sxs-lookup"><span data-stu-id="68b81-146">305.00</span></span>                 | <span data-ttu-id="68b81-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="68b81-147">305.00 \* 0.10</span></span> | <span data-ttu-id="68b81-148">30,50</span><span class="sxs-lookup"><span data-stu-id="68b81-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="68b81-149"> Esimerkki: Väli-laskentatapa</span><span class="sxs-lookup"><span data-stu-id="68b81-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="68b81-150">Arvonlisäveroprosentit määritetään Arvot-sivulla seuraavin välein:</span><span class="sxs-lookup"><span data-stu-id="68b81-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="68b81-151">**Vähimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="68b81-151">**Minimum limit**</span></span> | <span data-ttu-id="68b81-152">**Enimmäisraja**</span><span class="sxs-lookup"><span data-stu-id="68b81-152">**Maximum limit**</span></span> | <span data-ttu-id="68b81-153">**Veroprosentti**</span><span class="sxs-lookup"><span data-stu-id="68b81-153">**Tax rate**</span></span> |
| <span data-ttu-id="68b81-154">0,00</span><span class="sxs-lookup"><span data-stu-id="68b81-154">0.00</span></span>              | <span data-ttu-id="68b81-155">50,00</span><span class="sxs-lookup"><span data-stu-id="68b81-155">50.00</span></span>             | <span data-ttu-id="68b81-156">30 %</span><span class="sxs-lookup"><span data-stu-id="68b81-156">30%</span></span>          |
| <span data-ttu-id="68b81-157">50,00</span><span class="sxs-lookup"><span data-stu-id="68b81-157">50.00</span></span>             | <span data-ttu-id="68b81-158">100,00</span><span class="sxs-lookup"><span data-stu-id="68b81-158">100.00</span></span>            | <span data-ttu-id="68b81-159">20 %</span><span class="sxs-lookup"><span data-stu-id="68b81-159">20%</span></span>          |
| <span data-ttu-id="68b81-160">100,00</span><span class="sxs-lookup"><span data-stu-id="68b81-160">100.00</span></span>            | <span data-ttu-id="68b81-161">0,00</span><span class="sxs-lookup"><span data-stu-id="68b81-161">0.00</span></span>              | <span data-ttu-id="68b81-162">10 %</span><span class="sxs-lookup"><span data-stu-id="68b81-162">10%</span></span>          |

<span data-ttu-id="68b81-163">Arvonlisävero on kullekin summavälille laskettavien verosummien yhteissumma.</span><span class="sxs-lookup"><span data-stu-id="68b81-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="68b81-164">Verotettava summa (hinta)</span><span class="sxs-lookup"><span data-stu-id="68b81-164">Taxable amount (price)</span></span> | <span data-ttu-id="68b81-165">Laskelma</span><span class="sxs-lookup"><span data-stu-id="68b81-165">Calculation</span></span>                                                               | <span data-ttu-id="68b81-166">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="68b81-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="68b81-167">35,00</span><span class="sxs-lookup"><span data-stu-id="68b81-167">35.00</span></span>                  | <span data-ttu-id="68b81-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="68b81-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="68b81-169">10,50</span><span class="sxs-lookup"><span data-stu-id="68b81-169">10.50</span></span>     |
| <span data-ttu-id="68b81-170">50,00</span><span class="sxs-lookup"><span data-stu-id="68b81-170">50.00</span></span>                  | <span data-ttu-id="68b81-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="68b81-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="68b81-172">15,00</span><span class="sxs-lookup"><span data-stu-id="68b81-172">15.00</span></span>     |
| <span data-ttu-id="68b81-173">85,00</span><span class="sxs-lookup"><span data-stu-id="68b81-173">85.00</span></span>                  | <span data-ttu-id="68b81-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="68b81-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="68b81-175">22,00</span><span class="sxs-lookup"><span data-stu-id="68b81-175">22.00</span></span>     |
| <span data-ttu-id="68b81-176">305,00</span><span class="sxs-lookup"><span data-stu-id="68b81-176">305.00</span></span>                 | <span data-ttu-id="68b81-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="68b81-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="68b81-178">45,50</span><span class="sxs-lookup"><span data-stu-id="68b81-178">45.50</span></span>     |



<span data-ttu-id="68b81-179">Lisätietoja on kohdassa [Arvonlisäveroprosenttien määrittäminen Alv-rajan peruste- ja Laskentatapa-kenttien perusteella](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="68b81-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





