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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c91399e96c54f7cf9968a15e3fff90c3a71ca6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="bd1c3-103">Valuutan uudelleenarvostus konsolidointiyrityksessä</span><span class="sxs-lookup"><span data-stu-id="bd1c3-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="bd1c3-104">Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, sinun on silti ajettava valuutan uudelleenarvostus, jos vaihtokursseissa tapahtuu muutoksia niin, että tiliesi saldot on uudelleenarvostettu oikein.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="bd1c3-105">Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdeltä ensimmäiset vaihtokurssit, jotka muunnetaan konsolidointiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="bd1c3-106">Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="bd1c3-107">Toteutumattomat voitot tai tappiot päivitetään sitten tämän mukaisesti uuden vaihtokurssin ja päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="bd1c3-108">Seuraavassa esimerkissä on kuvattu kirjanpitomerkinnät, jotka luodaan tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="bd1c3-109">Yrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="bd1c3-109">Company setup</span></span>
-   <span data-ttu-id="bd1c3-110">**Lähde/toimintaa harjoittava yritys (USMF)** – Yhdysvaltain dollareita (USD) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="bd1c3-111">**Konsolidointiyritys (CON)** – Euroja (EUR) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="bd1c3-112">**Toteutunut voitto** – Kirjanpitotili 801500</span><span class="sxs-lookup"><span data-stu-id="bd1c3-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="bd1c3-113">**Toteutunut tappio** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="bd1c3-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="bd1c3-114">**Toteutumaton voitto** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="bd1c3-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="bd1c3-115">**Toteutumaton tappio** – Kirjanpitotili 801400</span><span class="sxs-lookup"><span data-stu-id="bd1c3-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="bd1c3-116">Alkuperäiset tapahtumat</span><span class="sxs-lookup"><span data-stu-id="bd1c3-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="bd1c3-117">Kassamaksut USMF:ssä</span><span class="sxs-lookup"><span data-stu-id="bd1c3-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="bd1c3-118">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="bd1c3-118">Date</span></span>       | <span data-ttu-id="bd1c3-119">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="bd1c3-119">Ledger account</span></span>               | <span data-ttu-id="bd1c3-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-120">Currency</span></span> | <span data-ttu-id="bd1c3-121">Summa</span><span class="sxs-lookup"><span data-stu-id="bd1c3-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="bd1c3-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-122">10/11/2015</span></span> | <span data-ttu-id="bd1c3-123">110110 – Käteinen</span><span class="sxs-lookup"><span data-stu-id="bd1c3-123">110110 – Cash</span></span>                | <span data-ttu-id="bd1c3-124">USD</span><span class="sxs-lookup"><span data-stu-id="bd1c3-124">USD</span></span>      | <span data-ttu-id="bd1c3-125">500</span><span class="sxs-lookup"><span data-stu-id="bd1c3-125">500</span></span>    |
| <span data-ttu-id="bd1c3-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-126">10/11/2015</span></span> | <span data-ttu-id="bd1c3-127">130100 – Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="bd1c3-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="bd1c3-128">USD</span><span class="sxs-lookup"><span data-stu-id="bd1c3-128">USD</span></span>      | <span data-ttu-id="bd1c3-129">-500</span><span class="sxs-lookup"><span data-stu-id="bd1c3-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="bd1c3-130">Vaihtokurssit</span><span class="sxs-lookup"><span data-stu-id="bd1c3-130">Exchange rates</span></span>
| <span data-ttu-id="bd1c3-131">Lähdevaluutta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-131">From currency</span></span> | <span data-ttu-id="bd1c3-132">Valuutaksi</span><span class="sxs-lookup"><span data-stu-id="bd1c3-132">To currency</span></span> | <span data-ttu-id="bd1c3-133">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="bd1c3-133">Start date</span></span> | <span data-ttu-id="bd1c3-134">Vaihtokurssi</span><span class="sxs-lookup"><span data-stu-id="bd1c3-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="bd1c3-135">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-135">EUR</span></span>           | <span data-ttu-id="bd1c3-136">USD</span><span class="sxs-lookup"><span data-stu-id="bd1c3-136">USD</span></span>         | <span data-ttu-id="bd1c3-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-137">10/1/2015</span></span>  | <span data-ttu-id="bd1c3-138">200</span><span class="sxs-lookup"><span data-stu-id="bd1c3-138">200</span></span>           |
| <span data-ttu-id="bd1c3-139">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-139">EUR</span></span>           | <span data-ttu-id="bd1c3-140">USD</span><span class="sxs-lookup"><span data-stu-id="bd1c3-140">USD</span></span>         | <span data-ttu-id="bd1c3-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-141">11/1/2015</span></span>  | <span data-ttu-id="bd1c3-142">150</span><span class="sxs-lookup"><span data-stu-id="bd1c3-142">150</span></span>           |
| <span data-ttu-id="bd1c3-143">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-143">EUR</span></span>           | <span data-ttu-id="bd1c3-144">USD</span><span class="sxs-lookup"><span data-stu-id="bd1c3-144">USD</span></span>         | <span data-ttu-id="bd1c3-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="bd1c3-145">12/1/2012</span></span>  | <span data-ttu-id="bd1c3-146">100</span><span class="sxs-lookup"><span data-stu-id="bd1c3-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="bd1c3-147">Suorita konsolidointi lokakuulle 2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="bd1c3-148">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="bd1c3-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="bd1c3-149">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="bd1c3-149">Ledger account</span></span> | <span data-ttu-id="bd1c3-150">Valuutta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-150">Currency</span></span> | <span data-ttu-id="bd1c3-151">Summa</span><span class="sxs-lookup"><span data-stu-id="bd1c3-151">Amount</span></span> | <span data-ttu-id="bd1c3-152">Laskenta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="bd1c3-153">110110</span><span class="sxs-lookup"><span data-stu-id="bd1c3-153">110110</span></span>         | <span data-ttu-id="bd1c3-154">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-154">EUR</span></span>      | <span data-ttu-id="bd1c3-155">250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-155">250</span></span>    | <span data-ttu-id="bd1c3-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="bd1c3-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="bd1c3-157">130100</span><span class="sxs-lookup"><span data-stu-id="bd1c3-157">130100</span></span>         | <span data-ttu-id="bd1c3-158">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-158">EUR</span></span>      | <span data-ttu-id="bd1c3-159">-250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-159">-250</span></span>   | <span data-ttu-id="bd1c3-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="bd1c3-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="bd1c3-161">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 30.11.2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="bd1c3-162">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="bd1c3-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="bd1c3-163">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="bd1c3-163">Ledger account</span></span> | <span data-ttu-id="bd1c3-164">Valuutta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-164">Currency</span></span> | <span data-ttu-id="bd1c3-165">Summa</span><span class="sxs-lookup"><span data-stu-id="bd1c3-165">Amount</span></span>  | <span data-ttu-id="bd1c3-166">Laskenta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="bd1c3-167">110110</span><span class="sxs-lookup"><span data-stu-id="bd1c3-167">110110</span></span>         | <span data-ttu-id="bd1c3-168">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-168">EUR</span></span>      | <span data-ttu-id="bd1c3-169">333,33</span><span class="sxs-lookup"><span data-stu-id="bd1c3-169">333.33</span></span>  | <span data-ttu-id="bd1c3-170">Alkuperäinen summa 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="bd1c3-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="bd1c3-171">130100</span><span class="sxs-lookup"><span data-stu-id="bd1c3-171">130100</span></span>         | <span data-ttu-id="bd1c3-172">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-172">EUR</span></span>      | <span data-ttu-id="bd1c3-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="bd1c3-173">-333.33</span></span> | <span data-ttu-id="bd1c3-174">Alkuperäinen summa -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="bd1c3-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="bd1c3-175">801400</span><span class="sxs-lookup"><span data-stu-id="bd1c3-175">801400</span></span>         | <span data-ttu-id="bd1c3-176">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-176">EUR</span></span>      | <span data-ttu-id="bd1c3-177">83,33</span><span class="sxs-lookup"><span data-stu-id="bd1c3-177">83.33</span></span>   | <span data-ttu-id="bd1c3-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="bd1c3-179">801600</span><span class="sxs-lookup"><span data-stu-id="bd1c3-179">801600</span></span>         | <span data-ttu-id="bd1c3-180">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-180">EUR</span></span>      | <span data-ttu-id="bd1c3-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="bd1c3-181">-83.33</span></span>  | <span data-ttu-id="bd1c3-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="bd1c3-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="bd1c3-183">Näet tässä lisätapahtumia raportointivaluutan summille.</span><span class="sxs-lookup"><span data-stu-id="bd1c3-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="bd1c3-184">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 31.12.2015</span><span class="sxs-lookup"><span data-stu-id="bd1c3-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="bd1c3-185">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="bd1c3-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="bd1c3-186">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="bd1c3-186">Ledger account</span></span> | <span data-ttu-id="bd1c3-187">Valuutta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-187">Currency</span></span> | <span data-ttu-id="bd1c3-188">Summa</span><span class="sxs-lookup"><span data-stu-id="bd1c3-188">Amount</span></span>  | <span data-ttu-id="bd1c3-189">Laskenta</span><span class="sxs-lookup"><span data-stu-id="bd1c3-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="bd1c3-190">110110</span><span class="sxs-lookup"><span data-stu-id="bd1c3-190">110110</span></span>         | <span data-ttu-id="bd1c3-191">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-191">EUR</span></span>      | <span data-ttu-id="bd1c3-192">500,00</span><span class="sxs-lookup"><span data-stu-id="bd1c3-192">500.00</span></span>  | <span data-ttu-id="bd1c3-193">Alkuperäinen summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="bd1c3-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="bd1c3-194">130100</span><span class="sxs-lookup"><span data-stu-id="bd1c3-194">130100</span></span>         | <span data-ttu-id="bd1c3-195">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-195">EUR</span></span>      | <span data-ttu-id="bd1c3-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="bd1c3-196">-500.00</span></span> | <span data-ttu-id="bd1c3-197">Alkuperäinen summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="bd1c3-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="bd1c3-198">801400</span><span class="sxs-lookup"><span data-stu-id="bd1c3-198">801400</span></span>         | <span data-ttu-id="bd1c3-199">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-199">EUR</span></span>      | <span data-ttu-id="bd1c3-200">250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-200">250</span></span>     | <span data-ttu-id="bd1c3-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="bd1c3-202">801600</span><span class="sxs-lookup"><span data-stu-id="bd1c3-202">801600</span></span>         | <span data-ttu-id="bd1c3-203">Euro</span><span class="sxs-lookup"><span data-stu-id="bd1c3-203">EUR</span></span>      | <span data-ttu-id="bd1c3-204">-250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-204">-250</span></span>    | <span data-ttu-id="bd1c3-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="bd1c3-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






