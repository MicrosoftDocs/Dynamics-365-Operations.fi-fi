---
title: "Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella"
description: "Tässä ohjeaiheessa kerrotaan, miten Alv-rajan peruste- ja Laskentatapa-kenttien arvot määrittävät myynti- ja ostotapahtumien veroprosentit."
author: twheeloc
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9bd67a2c7eed658b27b208bdb428bb880708cd31
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="96934-103">Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella</span><span class="sxs-lookup"><span data-stu-id="96934-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96934-104">Tässä ohjeaiheessa kerrotaan, miten Alv-rajan peruste- ja Laskentatapa-kenttien arvot määrittävät myynti- ja ostotapahtumien veroprosentit.</span><span class="sxs-lookup"><span data-stu-id="96934-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="96934-105">ALV-rajan peruste Arvonlisäverokoodit-sivun Laskenta-pikavälilehdessä määrittää, millä summalla sopiva veroprosentti valitaan Arvonlisäverokoodin arvot -sivulla olevista prosenteista.</span><span class="sxs-lookup"><span data-stu-id="96934-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="96934-106">Alv-rajan peruste -kentän summatyyppi yhdessä Laskentatapa-kentässä valitun menetelmän kanssa määrittää logiikan, jolla tapahtumalle etsitään oikea veroprosentti.</span><span class="sxs-lookup"><span data-stu-id="96934-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="96934-107">Seuraavat esimerkit osoittavat, että syöttämällä näihin kenttiin erilaisia yhdistelmiä saadaan hyvin erilaisia arvonlisäverolaskutuloksia.</span><span class="sxs-lookup"><span data-stu-id="96934-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="96934-108">Esimerkeissä käytetään samoja verovälin arvoja, jotka määritetään jokaiselle verokoodille Arvonlisäverokoodin arvot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="96934-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="96934-109">Voit avata sivun valitsemalla Arvonlisäverokoodi &gt; Arvonlisäverokoodit arvot -sivu.</span><span class="sxs-lookup"><span data-stu-id="96934-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="96934-110">Jos vähintään yhden arvolisäverokoodin Alv-rajan peruste perustuu rivin summiin tai yksiköihin, Kirjanpitoparametrit-sivun Laskentapa-kentän arvoksi on määritettävä Rivi.</span><span class="sxs-lookup"><span data-stu-id="96934-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="96934-111"> Rivikohtainen nettosumma</span><span class="sxs-lookup"><span data-stu-id="96934-111">Net amount per line</span></span>
<span data-ttu-id="96934-112">Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit laskurivien nettosumman perusteella ilman muita veroja.</span><span class="sxs-lookup"><span data-stu-id="96934-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="96934-113">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96934-113">Example</span></span>

<span data-ttu-id="96934-114">Arvonlisäveroprosentit määritetään seuraavilla väleillä.</span><span class="sxs-lookup"><span data-stu-id="96934-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="96934-115">Summaväli</span><span class="sxs-lookup"><span data-stu-id="96934-115">Amount interval</span></span>    | <span data-ttu-id="96934-116">Veroprosentti</span><span class="sxs-lookup"><span data-stu-id="96934-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="96934-117">0–50</span><span class="sxs-lookup"><span data-stu-id="96934-117">0 - 50</span></span>             | <span data-ttu-id="96934-118">30 %</span><span class="sxs-lookup"><span data-stu-id="96934-118">30%</span></span>      |
| <span data-ttu-id="96934-119">50–100</span><span class="sxs-lookup"><span data-stu-id="96934-119">50 - 100</span></span>           | <span data-ttu-id="96934-120">20 %</span><span class="sxs-lookup"><span data-stu-id="96934-120">20%</span></span>      |
| <span data-ttu-id="96934-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="96934-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="96934-122">10 %</span><span class="sxs-lookup"><span data-stu-id="96934-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="96934-123">Viimeisen välin yläraja nolla (0) tarkoittaa sitä, että väliin sisällytetään kaikki summat, jotka ovat yli 100.</span><span class="sxs-lookup"><span data-stu-id="96934-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="96934-124">Alv-rajan peruste: **Nettosumma riveittäin**</span><span class="sxs-lookup"><span data-stu-id="96934-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="96934-125">Laskentatapa: **Väli**</span><span class="sxs-lookup"><span data-stu-id="96934-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="96934-126">Ostat 8 lamppua, joista jokaisen hinta on 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="96934-127">Laskurivin nettosumma on 200,00.</span><span class="sxs-lookup"><span data-stu-id="96934-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="96934-128">Vero lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="96934-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="96934-129">Arvonlisävero yhteensä = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00.</span><span class="sxs-lookup"><span data-stu-id="96934-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="96934-130">Laskun kokonaissumma = 200,00 + 35,00 = 235,00.</span><span class="sxs-lookup"><span data-stu-id="96934-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="96934-131">**Vaihtelu**</span><span class="sxs-lookup"><span data-stu-id="96934-131">**Variation**</span></span> 

<span data-ttu-id="96934-132">Jos laskussa on kaksi riviä ja kumpikin rivi sisältää 4 nimikettä, kunkin rivin nettosumma on 100,00 ja arvonlisävero lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="96934-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="96934-133">Arvonlisäverorivi 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="96934-134">Arvonlisäverorivi 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="96934-135">Arvonlisävero yhteensä = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="96934-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="96934-136">Laskun kokonaissumma = 200,00 + 50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="96934-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="96934-137"> Yksikkökohtainen nettosumma</span><span class="sxs-lookup"><span data-stu-id="96934-137">Net amount per unit</span></span>
<span data-ttu-id="96934-138">Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit kunkin yksikön arvon perusteella ilman muita veroja.</span><span class="sxs-lookup"><span data-stu-id="96934-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="96934-139">Jos yksikköperusteinen ALV-rajan peruste valitaan, myös arvonlisäverokoodille on määritettävä myös yksikkö.</span><span class="sxs-lookup"><span data-stu-id="96934-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="96934-140">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96934-140">Example</span></span>

<span data-ttu-id="96934-141">Arvonlisäveroprosentit määritetään seuraavilla väleillä.</span><span class="sxs-lookup"><span data-stu-id="96934-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="96934-142">Summa</span><span class="sxs-lookup"><span data-stu-id="96934-142">Amount</span></span>             | <span data-ttu-id="96934-143">Veroprosentti</span><span class="sxs-lookup"><span data-stu-id="96934-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="96934-144">0–50</span><span class="sxs-lookup"><span data-stu-id="96934-144">0 - 50</span></span>             | <span data-ttu-id="96934-145">30 %</span><span class="sxs-lookup"><span data-stu-id="96934-145">30%</span></span>      |
| <span data-ttu-id="96934-146">50–100</span><span class="sxs-lookup"><span data-stu-id="96934-146">50 - 100</span></span>           | <span data-ttu-id="96934-147">20 %</span><span class="sxs-lookup"><span data-stu-id="96934-147">20%</span></span>      |
| <span data-ttu-id="96934-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="96934-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="96934-149">10 %</span><span class="sxs-lookup"><span data-stu-id="96934-149">10%</span></span>      |

<span data-ttu-id="96934-150">Alv-rajan peruste: **Yksikkökohtainen nettosumma**</span><span class="sxs-lookup"><span data-stu-id="96934-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="96934-151">Laskentatapa: **Koko summa**</span><span class="sxs-lookup"><span data-stu-id="96934-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="96934-152">Ostat 8 lamppua, joista jokaisen hinta on 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="96934-153">Laskurivin nettosumma on 200,00.</span><span class="sxs-lookup"><span data-stu-id="96934-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="96934-154">Vero lasketaan seuraavasti: Yksikkökohtainen arvonlisävero = 25,00 x 30 % = 7,50 Arvonlisävero yhteensä = 7,50 x 8 yksikköä = 60,00 Laskun kokonaissumma = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="96934-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="96934-155"> Laskun saldon nettosumma</span><span class="sxs-lookup"><span data-stu-id="96934-155">Net amount of invoice balance</span></span>

<span data-ttu-id="96934-156">Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit laskun kokonaisarvon perusteella ilman muita veroja.</span><span class="sxs-lookup"><span data-stu-id="96934-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="96934-157">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96934-157">Example</span></span>

<span data-ttu-id="96934-158">Arvonlisäveroprosentit määritetään seuraavilla väleillä.</span><span class="sxs-lookup"><span data-stu-id="96934-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="96934-159">Summa</span><span class="sxs-lookup"><span data-stu-id="96934-159">Amount</span></span>            | <span data-ttu-id="96934-160">Veroprosentti</span><span class="sxs-lookup"><span data-stu-id="96934-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="96934-161">0–50</span><span class="sxs-lookup"><span data-stu-id="96934-161">0 - 50</span></span>            | <span data-ttu-id="96934-162">30 %</span><span class="sxs-lookup"><span data-stu-id="96934-162">30%</span></span>      |
| <span data-ttu-id="96934-163">50–100</span><span class="sxs-lookup"><span data-stu-id="96934-163">50 - 100</span></span>          | <span data-ttu-id="96934-164">20 %</span><span class="sxs-lookup"><span data-stu-id="96934-164">20%</span></span>      |
| <span data-ttu-id="96934-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="96934-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="96934-166">10 %</span><span class="sxs-lookup"><span data-stu-id="96934-166">10%</span></span>      |

<span data-ttu-id="96934-167">Alv-rajan peruste: **Laskun saldon nettosumma**</span><span class="sxs-lookup"><span data-stu-id="96934-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="96934-168">Laskentatapa: **Väli** Myyntilaskussa on 2 riviä ja kummallakin rivillä 4 lamppua, joiden hinta on 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="96934-169">Laskun saldon nettosumma on 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="96934-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="96934-170">Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Laskun kokonaissumma = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="96934-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="96934-171"> Rivikohtainen bruttosumma</span><span class="sxs-lookup"><span data-stu-id="96934-171">Gross amount per line</span></span>

<span data-ttu-id="96934-172">Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit rivin arvon perusteella. Rivin arvo sisältää myös muut kyseisen rivin verot.</span><span class="sxs-lookup"><span data-stu-id="96934-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="96934-173">Arvonlisäveroryhmässä voi olla vain yksi arvonlisäverokoodi, jossa tämä valinta on tehty Alv-rajan peruste -kentässä.</span><span class="sxs-lookup"><span data-stu-id="96934-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="96934-174">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96934-174">Example</span></span>

<span data-ttu-id="96934-175">Arvonlisäveroprosentit määritetään seuraavilla väleillä.</span><span class="sxs-lookup"><span data-stu-id="96934-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="96934-176">Summa</span><span class="sxs-lookup"><span data-stu-id="96934-176">Amount</span></span>             | <span data-ttu-id="96934-177">Veroprosentti</span><span class="sxs-lookup"><span data-stu-id="96934-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="96934-178">0–50</span><span class="sxs-lookup"><span data-stu-id="96934-178">0 - 50</span></span>             | <span data-ttu-id="96934-179">30 %</span><span class="sxs-lookup"><span data-stu-id="96934-179">30%</span></span>      |
| <span data-ttu-id="96934-180">50–100</span><span class="sxs-lookup"><span data-stu-id="96934-180">50 - 100</span></span>           | <span data-ttu-id="96934-181">20 %</span><span class="sxs-lookup"><span data-stu-id="96934-181">20%</span></span>      |
| <span data-ttu-id="96934-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="96934-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="96934-183">10 %</span><span class="sxs-lookup"><span data-stu-id="96934-183">10%</span></span>      |

<span data-ttu-id="96934-184">ALV-rajan peruste: **Rivikohtainen bruttosumma** Laskentatapa: **Väli** Kullakin lampulla on myös erikoismaksu, jonka suuruus on 5,00 ja jolle lasketaan toinen verokoodi.</span><span class="sxs-lookup"><span data-stu-id="96934-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="96934-185">Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista.</span><span class="sxs-lookup"><span data-stu-id="96934-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="96934-186">Ostat 8 lamppua, joista jokaisen hinta on 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="96934-187">Laskurivin nettosumma on 200,00.</span><span class="sxs-lookup"><span data-stu-id="96934-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="96934-188">Laskurivin bruttosumma on 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="96934-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="96934-189">Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="96934-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="96934-190">**Vaihtelu**</span><span class="sxs-lookup"><span data-stu-id="96934-190">**Variation**</span></span> 

<span data-ttu-id="96934-191">Jos lasku luodaan käyttämällä kahta laskuriviä ja kumpikin rivi sisältää 4 nimikettä, laskurivin nettosumma on 100.</span><span class="sxs-lookup"><span data-stu-id="96934-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="96934-192">Laskurivikohtainen bruttosumma (mukaan lukien vero 4 x 5,00) olisi 120,00 ja arvonlisävero luodaan seuraavasti: Arvonlisävero laskun rivi 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Arvonlisävero laskun rivi 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Arvonlisävero yhteensä = 27,00 + 27,00 = 54,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="96934-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="96934-193"> Yksikkökohtainen bruttosumma</span><span class="sxs-lookup"><span data-stu-id="96934-193">Gross amount per unit</span></span>

<span data-ttu-id="96934-194">Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit kunkin yksikön arvon perusteella mukaan lukien muut verot.</span><span class="sxs-lookup"><span data-stu-id="96934-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="96934-195">Arvonlisäveroryhmässä voi olla vain yksi arvonlisäverokoodi, jossa tämä valinta on tehty Alv-rajan peruste -kentässä.</span><span class="sxs-lookup"><span data-stu-id="96934-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="96934-196">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96934-196">Example</span></span>

<span data-ttu-id="96934-197">Arvonlisäveroprosentit määritetään seuraavilla väleillä.</span><span class="sxs-lookup"><span data-stu-id="96934-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="96934-198">Summa</span><span class="sxs-lookup"><span data-stu-id="96934-198">Amount</span></span>             | <span data-ttu-id="96934-199">Veroprosentti</span><span class="sxs-lookup"><span data-stu-id="96934-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="96934-200">0–50</span><span class="sxs-lookup"><span data-stu-id="96934-200">0 - 50</span></span>             | <span data-ttu-id="96934-201">30 %</span><span class="sxs-lookup"><span data-stu-id="96934-201">30%</span></span>      |
| <span data-ttu-id="96934-202">50–100</span><span class="sxs-lookup"><span data-stu-id="96934-202">50 - 100</span></span>           | <span data-ttu-id="96934-203">20 %</span><span class="sxs-lookup"><span data-stu-id="96934-203">20%</span></span>      |
| <span data-ttu-id="96934-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="96934-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="96934-205">10 %</span><span class="sxs-lookup"><span data-stu-id="96934-205">10%</span></span>      |

<span data-ttu-id="96934-206">ALV-rajan peruste: **Yksikkökohtainen bruttosumma** Kullakin lampulla on erikoismaksu, jonka suuruus on 5,00.</span><span class="sxs-lookup"><span data-stu-id="96934-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="96934-207">Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista.</span><span class="sxs-lookup"><span data-stu-id="96934-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="96934-208">Ostat 8 lamppua, joista jokaisen hinta on 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="96934-209">Yksikkökohtainen bruttosumma on 30,00.</span><span class="sxs-lookup"><span data-stu-id="96934-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="96934-210">Vero lasketaan seuraavasti: Yksikkökohtainen arvonlisävero = 30 x 30 % = 9,00 Arvonlisävero yhteensä 9,00 + 8 = 72,00 Erikoismaksu yhteensä = 5,00 + 8 = 40,00 Laskun kokonaissumma = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="96934-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="96934-211"> Laskun loppusumma muut arvonlisäverosummat mukaan luettuna</span><span class="sxs-lookup"><span data-stu-id="96934-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="96934-212">Valitsemalla tämän asetuksen voit määrittää arvonlisäveroprosentit laskun kokonaisarvon perusteella mukaan lukien muut verot.</span><span class="sxs-lookup"><span data-stu-id="96934-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="96934-213">Arvonlisäveroryhmässä voi olla vain yksi arvonlisäverokoodi, jossa tämä valinta on tehty Alv-rajan peruste -kentässä</span><span class="sxs-lookup"><span data-stu-id="96934-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="96934-214">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="96934-214">Example</span></span>

<span data-ttu-id="96934-215">Arvonlisäveroprosentit määritetään seuraavilla väleillä.</span><span class="sxs-lookup"><span data-stu-id="96934-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="96934-216">Summa</span><span class="sxs-lookup"><span data-stu-id="96934-216">Amount</span></span>             | <span data-ttu-id="96934-217">Veroprosentti</span><span class="sxs-lookup"><span data-stu-id="96934-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="96934-218">0–50</span><span class="sxs-lookup"><span data-stu-id="96934-218">0 - 50</span></span>             | <span data-ttu-id="96934-219">30 %</span><span class="sxs-lookup"><span data-stu-id="96934-219">30%</span></span>      |
| <span data-ttu-id="96934-220">50–100</span><span class="sxs-lookup"><span data-stu-id="96934-220">50 - 100</span></span>           | <span data-ttu-id="96934-221">20 %</span><span class="sxs-lookup"><span data-stu-id="96934-221">20%</span></span>      |
| <span data-ttu-id="96934-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="96934-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="96934-223">10 %</span><span class="sxs-lookup"><span data-stu-id="96934-223">10%</span></span>      |

<span data-ttu-id="96934-224">Alv-rajan peruste: **Laskun loppusumma muut arvonlisäverosummat mukaan luettuna** Laskentatapa: **Väli** </span><span class="sxs-lookup"><span data-stu-id="96934-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="96934-225">Jokaisella lampulla on erikoismaksu 5,00.</span><span class="sxs-lookup"><span data-stu-id="96934-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="96934-226">Erikoismaksu lisätään nettosummaan ennen arvonlisäveron laskemista.</span><span class="sxs-lookup"><span data-stu-id="96934-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="96934-227">Ostat 8 lamppua, joista jokaisen hinta on 25,00.</span><span class="sxs-lookup"><span data-stu-id="96934-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="96934-228">Laskun nettosumma on 200,00.</span><span class="sxs-lookup"><span data-stu-id="96934-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="96934-229">Laskun bruttosumma on 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="96934-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="96934-230">Vero lasketaan seuraavasti: Arvonlisävero yhteensä = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Erikoismaksut yhteensä = 5,00 x 8 = 40,00 Laskun kokonaissumma = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="96934-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="96934-231">Lisätietoja: [Alv-koodien koko summa- ja väli-laskentavaihtoehdot](whole-amount-interval-options-sales-tax-codes.md) [Arvonlisäveron laskentatavat Alkuperä-kentässä](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="96934-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>




