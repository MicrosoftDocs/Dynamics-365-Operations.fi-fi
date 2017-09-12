---
title: "Valuutan uudelleenarvostus konsolidointiyrityksessä"
description: 
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="a75e9-102">Valuutan uudelleenarvostus konsolidointiyrityksessä</span><span class="sxs-lookup"><span data-stu-id="a75e9-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="a75e9-103">Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, sinun on silti ajettava valuutan uudelleenarvostus, jos vaihtokursseissa tapahtuu muutoksia niin, että tiliesi saldot on uudelleenarvostettu oikein.</span><span class="sxs-lookup"><span data-stu-id="a75e9-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="a75e9-104">Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdeltä ensimmäiset vaihtokurssit, jotka muunnetaan konsolidointiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="a75e9-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="a75e9-105">Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot.</span><span class="sxs-lookup"><span data-stu-id="a75e9-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="a75e9-106">Toteutumattomat voitot tai tappiot päivitetään sitten tämän mukaisesti uuden vaihtokurssin ja päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="a75e9-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="a75e9-107">Seuraavassa esimerkissä on kuvattu kirjanpitomerkinnät, jotka luodaan tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="a75e9-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="a75e9-108">Yrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="a75e9-108">Company setup</span></span>
-   <span data-ttu-id="a75e9-109">**Lähde/toimintaa harjoittava yritys (USMF)** – Yhdysvaltain dollareita (USD) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="a75e9-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="a75e9-110">**Konsolidointiyritys (CON)** – Euroja (EUR) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="a75e9-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="a75e9-111">**Toteutunut voitto** – Kirjanpitotili 801500</span><span class="sxs-lookup"><span data-stu-id="a75e9-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="a75e9-112">**Toteutunut tappio** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="a75e9-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="a75e9-113">**Toteutumaton voitto** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="a75e9-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="a75e9-114">**Toteutumaton tappio** – Kirjanpitotili 801400</span><span class="sxs-lookup"><span data-stu-id="a75e9-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="a75e9-115">Alkuperäiset tapahtumat</span><span class="sxs-lookup"><span data-stu-id="a75e9-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="a75e9-116">Kassamaksut USMF:ssä</span><span class="sxs-lookup"><span data-stu-id="a75e9-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="a75e9-117">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="a75e9-117">Date</span></span>       | <span data-ttu-id="a75e9-118">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="a75e9-118">Ledger account</span></span>               | <span data-ttu-id="a75e9-119">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a75e9-119">Currency</span></span> | <span data-ttu-id="a75e9-120">Summa</span><span class="sxs-lookup"><span data-stu-id="a75e9-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="a75e9-121">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-121">10/11/2015</span></span> | <span data-ttu-id="a75e9-122">110110 – Käteinen</span><span class="sxs-lookup"><span data-stu-id="a75e9-122">110110 – Cash</span></span>                | <span data-ttu-id="a75e9-123">USD</span><span class="sxs-lookup"><span data-stu-id="a75e9-123">USD</span></span>      | <span data-ttu-id="a75e9-124">500</span><span class="sxs-lookup"><span data-stu-id="a75e9-124">500</span></span>    |
| <span data-ttu-id="a75e9-125">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-125">10/11/2015</span></span> | <span data-ttu-id="a75e9-126">130100 – Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="a75e9-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="a75e9-127">USD</span><span class="sxs-lookup"><span data-stu-id="a75e9-127">USD</span></span>      | <span data-ttu-id="a75e9-128">-500</span><span class="sxs-lookup"><span data-stu-id="a75e9-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="a75e9-129">Vaihtokurssit</span><span class="sxs-lookup"><span data-stu-id="a75e9-129">Exchange rates</span></span>
| <span data-ttu-id="a75e9-130">Lähdevaluutta</span><span class="sxs-lookup"><span data-stu-id="a75e9-130">From currency</span></span> | <span data-ttu-id="a75e9-131">Valuutaksi</span><span class="sxs-lookup"><span data-stu-id="a75e9-131">To currency</span></span> | <span data-ttu-id="a75e9-132">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="a75e9-132">Start date</span></span> | <span data-ttu-id="a75e9-133">Vaihtokurssi</span><span class="sxs-lookup"><span data-stu-id="a75e9-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="a75e9-134">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-134">EUR</span></span>           | <span data-ttu-id="a75e9-135">USD</span><span class="sxs-lookup"><span data-stu-id="a75e9-135">USD</span></span>         | <span data-ttu-id="a75e9-136">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-136">10/1/2015</span></span>  | <span data-ttu-id="a75e9-137">200</span><span class="sxs-lookup"><span data-stu-id="a75e9-137">200</span></span>           |
| <span data-ttu-id="a75e9-138">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-138">EUR</span></span>           | <span data-ttu-id="a75e9-139">USD</span><span class="sxs-lookup"><span data-stu-id="a75e9-139">USD</span></span>         | <span data-ttu-id="a75e9-140">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-140">11/1/2015</span></span>  | <span data-ttu-id="a75e9-141">150</span><span class="sxs-lookup"><span data-stu-id="a75e9-141">150</span></span>           |
| <span data-ttu-id="a75e9-142">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-142">EUR</span></span>           | <span data-ttu-id="a75e9-143">USD</span><span class="sxs-lookup"><span data-stu-id="a75e9-143">USD</span></span>         | <span data-ttu-id="a75e9-144">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="a75e9-144">12/1/2012</span></span>  | <span data-ttu-id="a75e9-145">100</span><span class="sxs-lookup"><span data-stu-id="a75e9-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="a75e9-146">Suorita konsolidointi lokakuulle 2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a75e9-147">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="a75e9-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="a75e9-148">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="a75e9-148">Ledger account</span></span> | <span data-ttu-id="a75e9-149">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a75e9-149">Currency</span></span> | <span data-ttu-id="a75e9-150">Summa</span><span class="sxs-lookup"><span data-stu-id="a75e9-150">Amount</span></span> | <span data-ttu-id="a75e9-151">Laskenta</span><span class="sxs-lookup"><span data-stu-id="a75e9-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="a75e9-152">110110</span><span class="sxs-lookup"><span data-stu-id="a75e9-152">110110</span></span>         | <span data-ttu-id="a75e9-153">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-153">EUR</span></span>      | <span data-ttu-id="a75e9-154">250</span><span class="sxs-lookup"><span data-stu-id="a75e9-154">250</span></span>    | <span data-ttu-id="a75e9-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="a75e9-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="a75e9-156">130100</span><span class="sxs-lookup"><span data-stu-id="a75e9-156">130100</span></span>         | <span data-ttu-id="a75e9-157">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-157">EUR</span></span>      | <span data-ttu-id="a75e9-158">-250</span><span class="sxs-lookup"><span data-stu-id="a75e9-158">-250</span></span>   | <span data-ttu-id="a75e9-159">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="a75e9-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="a75e9-160">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 30.11.2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a75e9-161">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="a75e9-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="a75e9-162">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="a75e9-162">Ledger account</span></span> | <span data-ttu-id="a75e9-163">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a75e9-163">Currency</span></span> | <span data-ttu-id="a75e9-164">Summa</span><span class="sxs-lookup"><span data-stu-id="a75e9-164">Amount</span></span>  | <span data-ttu-id="a75e9-165">Laskenta</span><span class="sxs-lookup"><span data-stu-id="a75e9-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="a75e9-166">110110</span><span class="sxs-lookup"><span data-stu-id="a75e9-166">110110</span></span>         | <span data-ttu-id="a75e9-167">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-167">EUR</span></span>      | <span data-ttu-id="a75e9-168">333,33</span><span class="sxs-lookup"><span data-stu-id="a75e9-168">333.33</span></span>  | <span data-ttu-id="a75e9-169">Alkuperäinen summa 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="a75e9-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="a75e9-170">130100</span><span class="sxs-lookup"><span data-stu-id="a75e9-170">130100</span></span>         | <span data-ttu-id="a75e9-171">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-171">EUR</span></span>      | <span data-ttu-id="a75e9-172">-333,33</span><span class="sxs-lookup"><span data-stu-id="a75e9-172">-333.33</span></span> | <span data-ttu-id="a75e9-173">Alkuperäinen summa -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="a75e9-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="a75e9-174">801400</span><span class="sxs-lookup"><span data-stu-id="a75e9-174">801400</span></span>         | <span data-ttu-id="a75e9-175">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-175">EUR</span></span>      | <span data-ttu-id="a75e9-176">83,33</span><span class="sxs-lookup"><span data-stu-id="a75e9-176">83.33</span></span>   | <span data-ttu-id="a75e9-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="a75e9-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="a75e9-178">801600</span><span class="sxs-lookup"><span data-stu-id="a75e9-178">801600</span></span>         | <span data-ttu-id="a75e9-179">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-179">EUR</span></span>      | <span data-ttu-id="a75e9-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="a75e9-180">-83.33</span></span>  | <span data-ttu-id="a75e9-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="a75e9-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="a75e9-182">Näet tässä lisätapahtumia raportointivaluutan summille.</span><span class="sxs-lookup"><span data-stu-id="a75e9-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="a75e9-183">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 31.12.2015</span><span class="sxs-lookup"><span data-stu-id="a75e9-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a75e9-184">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="a75e9-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="a75e9-185">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="a75e9-185">Ledger account</span></span> | <span data-ttu-id="a75e9-186">Valuutta</span><span class="sxs-lookup"><span data-stu-id="a75e9-186">Currency</span></span> | <span data-ttu-id="a75e9-187">Summa</span><span class="sxs-lookup"><span data-stu-id="a75e9-187">Amount</span></span>  | <span data-ttu-id="a75e9-188">Laskenta</span><span class="sxs-lookup"><span data-stu-id="a75e9-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="a75e9-189">110110</span><span class="sxs-lookup"><span data-stu-id="a75e9-189">110110</span></span>         | <span data-ttu-id="a75e9-190">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-190">EUR</span></span>      | <span data-ttu-id="a75e9-191">500,00</span><span class="sxs-lookup"><span data-stu-id="a75e9-191">500.00</span></span>  | <span data-ttu-id="a75e9-192">Alkuperäinen summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="a75e9-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="a75e9-193">130100</span><span class="sxs-lookup"><span data-stu-id="a75e9-193">130100</span></span>         | <span data-ttu-id="a75e9-194">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-194">EUR</span></span>      | <span data-ttu-id="a75e9-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="a75e9-195">-500.00</span></span> | <span data-ttu-id="a75e9-196">Alkuperäinen summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="a75e9-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="a75e9-197">801400</span><span class="sxs-lookup"><span data-stu-id="a75e9-197">801400</span></span>         | <span data-ttu-id="a75e9-198">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-198">EUR</span></span>      | <span data-ttu-id="a75e9-199">250</span><span class="sxs-lookup"><span data-stu-id="a75e9-199">250</span></span>     | <span data-ttu-id="a75e9-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="a75e9-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="a75e9-201">801600</span><span class="sxs-lookup"><span data-stu-id="a75e9-201">801600</span></span>         | <span data-ttu-id="a75e9-202">Euro</span><span class="sxs-lookup"><span data-stu-id="a75e9-202">EUR</span></span>      | <span data-ttu-id="a75e9-203">-250</span><span class="sxs-lookup"><span data-stu-id="a75e9-203">-250</span></span>    | <span data-ttu-id="a75e9-204">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="a75e9-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






