---
title: "Valuutan uudelleenarvostus konsolidointiyrityksessä"
description: "Tässä aiheessa käsitellään valuutan uudelleenarvostus konsolidointiyrityksessä."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 27059b0d2a781453a7594bdc430005df6ea5c167
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="e6488-103">Valuutan uudelleenarvostus konsolidointiyrityksessä</span><span class="sxs-lookup"><span data-stu-id="e6488-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="e6488-104">Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, sinun on silti ajettava valuutan uudelleenarvostus, jos vaihtokursseissa tapahtuu muutoksia niin, että tiliesi saldot on uudelleenarvostettu oikein.</span><span class="sxs-lookup"><span data-stu-id="e6488-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="e6488-105">Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdeltä ensimmäiset vaihtokurssit, jotka muunnetaan konsolidointiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="e6488-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="e6488-106">Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot.</span><span class="sxs-lookup"><span data-stu-id="e6488-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="e6488-107">Toteutumattomat voitot tai tappiot päivitetään sitten tämän mukaisesti uuden vaihtokurssin ja päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="e6488-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="e6488-108">Seuraavassa esimerkissä on kuvattu kirjanpitomerkinnät, jotka luodaan tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="e6488-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="e6488-109">Yrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="e6488-109">Company setup</span></span>
-   <span data-ttu-id="e6488-110">**Lähde/toimintaa harjoittava yritys (USMF)** – Yhdysvaltain dollareita (USD) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="e6488-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="e6488-111">**Konsolidointiyritys (CON)** – Euroja (EUR) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="e6488-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="e6488-112">**Toteutunut voitto** – Kirjanpitotili 801500</span><span class="sxs-lookup"><span data-stu-id="e6488-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="e6488-113">**Toteutunut tappio** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="e6488-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="e6488-114">**Toteutumaton voitto** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="e6488-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="e6488-115">**Toteutumaton tappio** – Kirjanpitotili 801400</span><span class="sxs-lookup"><span data-stu-id="e6488-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="e6488-116">Alkuperäiset tapahtumat</span><span class="sxs-lookup"><span data-stu-id="e6488-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="e6488-117">Kassamaksut USMF:ssä</span><span class="sxs-lookup"><span data-stu-id="e6488-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="e6488-118">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="e6488-118">Date</span></span>       | <span data-ttu-id="e6488-119">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="e6488-119">Ledger account</span></span>               | <span data-ttu-id="e6488-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="e6488-120">Currency</span></span> | <span data-ttu-id="e6488-121">Summa</span><span class="sxs-lookup"><span data-stu-id="e6488-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="e6488-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="e6488-122">10/11/2015</span></span> | <span data-ttu-id="e6488-123">110110 – Käteinen</span><span class="sxs-lookup"><span data-stu-id="e6488-123">110110 – Cash</span></span>                | <span data-ttu-id="e6488-124">USD</span><span class="sxs-lookup"><span data-stu-id="e6488-124">USD</span></span>      | <span data-ttu-id="e6488-125">500</span><span class="sxs-lookup"><span data-stu-id="e6488-125">500</span></span>    |
| <span data-ttu-id="e6488-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="e6488-126">10/11/2015</span></span> | <span data-ttu-id="e6488-127">130100 – Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="e6488-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="e6488-128">USD</span><span class="sxs-lookup"><span data-stu-id="e6488-128">USD</span></span>      | <span data-ttu-id="e6488-129">-500</span><span class="sxs-lookup"><span data-stu-id="e6488-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="e6488-130">Vaihtokurssit</span><span class="sxs-lookup"><span data-stu-id="e6488-130">Exchange rates</span></span>
| <span data-ttu-id="e6488-131">Lähdevaluutta</span><span class="sxs-lookup"><span data-stu-id="e6488-131">From currency</span></span> | <span data-ttu-id="e6488-132">Valuutaksi</span><span class="sxs-lookup"><span data-stu-id="e6488-132">To currency</span></span> | <span data-ttu-id="e6488-133">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="e6488-133">Start date</span></span> | <span data-ttu-id="e6488-134">Vaihtokurssi</span><span class="sxs-lookup"><span data-stu-id="e6488-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="e6488-135">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-135">EUR</span></span>           | <span data-ttu-id="e6488-136">USD</span><span class="sxs-lookup"><span data-stu-id="e6488-136">USD</span></span>         | <span data-ttu-id="e6488-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="e6488-137">10/1/2015</span></span>  | <span data-ttu-id="e6488-138">200</span><span class="sxs-lookup"><span data-stu-id="e6488-138">200</span></span>           |
| <span data-ttu-id="e6488-139">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-139">EUR</span></span>           | <span data-ttu-id="e6488-140">USD</span><span class="sxs-lookup"><span data-stu-id="e6488-140">USD</span></span>         | <span data-ttu-id="e6488-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="e6488-141">11/1/2015</span></span>  | <span data-ttu-id="e6488-142">150</span><span class="sxs-lookup"><span data-stu-id="e6488-142">150</span></span>           |
| <span data-ttu-id="e6488-143">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-143">EUR</span></span>           | <span data-ttu-id="e6488-144">USD</span><span class="sxs-lookup"><span data-stu-id="e6488-144">USD</span></span>         | <span data-ttu-id="e6488-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="e6488-145">12/1/2012</span></span>  | <span data-ttu-id="e6488-146">100</span><span class="sxs-lookup"><span data-stu-id="e6488-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="e6488-147">Suorita konsolidointi lokakuulle 2015</span><span class="sxs-lookup"><span data-stu-id="e6488-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e6488-148">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="e6488-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="e6488-149">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="e6488-149">Ledger account</span></span> | <span data-ttu-id="e6488-150">Valuutta</span><span class="sxs-lookup"><span data-stu-id="e6488-150">Currency</span></span> | <span data-ttu-id="e6488-151">Summa</span><span class="sxs-lookup"><span data-stu-id="e6488-151">Amount</span></span> | <span data-ttu-id="e6488-152">Laskenta</span><span class="sxs-lookup"><span data-stu-id="e6488-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="e6488-153">110110</span><span class="sxs-lookup"><span data-stu-id="e6488-153">110110</span></span>         | <span data-ttu-id="e6488-154">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-154">EUR</span></span>      | <span data-ttu-id="e6488-155">250</span><span class="sxs-lookup"><span data-stu-id="e6488-155">250</span></span>    | <span data-ttu-id="e6488-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="e6488-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="e6488-157">130100</span><span class="sxs-lookup"><span data-stu-id="e6488-157">130100</span></span>         | <span data-ttu-id="e6488-158">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-158">EUR</span></span>      | <span data-ttu-id="e6488-159">-250</span><span class="sxs-lookup"><span data-stu-id="e6488-159">-250</span></span>   | <span data-ttu-id="e6488-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="e6488-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="e6488-161">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 30.11.2015</span><span class="sxs-lookup"><span data-stu-id="e6488-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e6488-162">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="e6488-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="e6488-163">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="e6488-163">Ledger account</span></span> | <span data-ttu-id="e6488-164">Valuutta</span><span class="sxs-lookup"><span data-stu-id="e6488-164">Currency</span></span> | <span data-ttu-id="e6488-165">Summa</span><span class="sxs-lookup"><span data-stu-id="e6488-165">Amount</span></span>  | <span data-ttu-id="e6488-166">Laskenta</span><span class="sxs-lookup"><span data-stu-id="e6488-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="e6488-167">110110</span><span class="sxs-lookup"><span data-stu-id="e6488-167">110110</span></span>         | <span data-ttu-id="e6488-168">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-168">EUR</span></span>      | <span data-ttu-id="e6488-169">333,33</span><span class="sxs-lookup"><span data-stu-id="e6488-169">333.33</span></span>  | <span data-ttu-id="e6488-170">Alkuperäinen summa 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="e6488-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="e6488-171">130100</span><span class="sxs-lookup"><span data-stu-id="e6488-171">130100</span></span>         | <span data-ttu-id="e6488-172">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-172">EUR</span></span>      | <span data-ttu-id="e6488-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="e6488-173">-333.33</span></span> | <span data-ttu-id="e6488-174">Alkuperäinen summa -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="e6488-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="e6488-175">801400</span><span class="sxs-lookup"><span data-stu-id="e6488-175">801400</span></span>         | <span data-ttu-id="e6488-176">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-176">EUR</span></span>      | <span data-ttu-id="e6488-177">83,33</span><span class="sxs-lookup"><span data-stu-id="e6488-177">83.33</span></span>   | <span data-ttu-id="e6488-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="e6488-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="e6488-179">801600</span><span class="sxs-lookup"><span data-stu-id="e6488-179">801600</span></span>         | <span data-ttu-id="e6488-180">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-180">EUR</span></span>      | <span data-ttu-id="e6488-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="e6488-181">-83.33</span></span>  | <span data-ttu-id="e6488-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="e6488-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="e6488-183">Näet tässä lisätapahtumia raportointivaluutan summille.</span><span class="sxs-lookup"><span data-stu-id="e6488-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="e6488-184">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 31.12.2015</span><span class="sxs-lookup"><span data-stu-id="e6488-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="e6488-185">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="e6488-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="e6488-186">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="e6488-186">Ledger account</span></span> | <span data-ttu-id="e6488-187">Valuutta</span><span class="sxs-lookup"><span data-stu-id="e6488-187">Currency</span></span> | <span data-ttu-id="e6488-188">Summa</span><span class="sxs-lookup"><span data-stu-id="e6488-188">Amount</span></span>  | <span data-ttu-id="e6488-189">Laskenta</span><span class="sxs-lookup"><span data-stu-id="e6488-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="e6488-190">110110</span><span class="sxs-lookup"><span data-stu-id="e6488-190">110110</span></span>         | <span data-ttu-id="e6488-191">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-191">EUR</span></span>      | <span data-ttu-id="e6488-192">500,00</span><span class="sxs-lookup"><span data-stu-id="e6488-192">500.00</span></span>  | <span data-ttu-id="e6488-193">Alkuperäinen summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="e6488-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="e6488-194">130100</span><span class="sxs-lookup"><span data-stu-id="e6488-194">130100</span></span>         | <span data-ttu-id="e6488-195">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-195">EUR</span></span>      | <span data-ttu-id="e6488-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="e6488-196">-500.00</span></span> | <span data-ttu-id="e6488-197">Alkuperäinen summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="e6488-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="e6488-198">801400</span><span class="sxs-lookup"><span data-stu-id="e6488-198">801400</span></span>         | <span data-ttu-id="e6488-199">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-199">EUR</span></span>      | <span data-ttu-id="e6488-200">250</span><span class="sxs-lookup"><span data-stu-id="e6488-200">250</span></span>     | <span data-ttu-id="e6488-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="e6488-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="e6488-202">801600</span><span class="sxs-lookup"><span data-stu-id="e6488-202">801600</span></span>         | <span data-ttu-id="e6488-203">Euro</span><span class="sxs-lookup"><span data-stu-id="e6488-203">EUR</span></span>      | <span data-ttu-id="e6488-204">-250</span><span class="sxs-lookup"><span data-stu-id="e6488-204">-250</span></span>    | <span data-ttu-id="e6488-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="e6488-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






