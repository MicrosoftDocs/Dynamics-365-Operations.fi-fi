---
title: "Valuutan uudelleenarvostus konsolidointiyrityksessä"
description: "Tässä aiheessa käsitellään valuutan uudelleenarvostus konsolidointiyrityksessä."
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.contentlocale: fi-fi
ms.lasthandoff: 10/02/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="0df3c-103">Valuutan uudelleenarvostus konsolidointiyrityksessä</span><span class="sxs-lookup"><span data-stu-id="0df3c-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0df3c-104">Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, sinun on silti ajettava valuutan uudelleenarvostus, jos vaihtokursseissa tapahtuu muutoksia niin, että tiliesi saldot on uudelleenarvostettu oikein.</span><span class="sxs-lookup"><span data-stu-id="0df3c-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="0df3c-105">Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdeltä ensimmäiset vaihtokurssit, jotka muunnetaan konsolidointiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="0df3c-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="0df3c-106">Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot.</span><span class="sxs-lookup"><span data-stu-id="0df3c-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="0df3c-107">Toteutumattomat voitot tai tappiot päivitetään sitten tämän mukaisesti uuden vaihtokurssin ja päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="0df3c-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="0df3c-108">Seuraavassa esimerkissä on kuvattu kirjanpitomerkinnät, jotka luodaan tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="0df3c-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="0df3c-109">Yrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="0df3c-109">Company setup</span></span>
-   <span data-ttu-id="0df3c-110">**Lähde/toimintaa harjoittava yritys (USMF)** – Yhdysvaltain dollareita (USD) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="0df3c-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="0df3c-111">**Konsolidointiyritys (CON)** – Euroja (EUR) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="0df3c-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="0df3c-112">**Toteutunut voitto**– Kirjanpitotili 801500</span><span class="sxs-lookup"><span data-stu-id="0df3c-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="0df3c-113">**Toteutunut tappio** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="0df3c-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="0df3c-114">**Toteutumaton voitto** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="0df3c-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="0df3c-115">**Toteutumaton tappio** – Kirjanpitotili 801400</span><span class="sxs-lookup"><span data-stu-id="0df3c-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="0df3c-116">Alkuperäiset tapahtumat</span><span class="sxs-lookup"><span data-stu-id="0df3c-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="0df3c-117">Kassamaksut USMF:ssä</span><span class="sxs-lookup"><span data-stu-id="0df3c-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="0df3c-118">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="0df3c-118">Date</span></span>       | <span data-ttu-id="0df3c-119">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="0df3c-119">Ledger account</span></span>               | <span data-ttu-id="0df3c-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="0df3c-120">Currency</span></span> | <span data-ttu-id="0df3c-121">Summa</span><span class="sxs-lookup"><span data-stu-id="0df3c-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="0df3c-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-122">10/11/2015</span></span> | <span data-ttu-id="0df3c-123">110110 – Käteinen</span><span class="sxs-lookup"><span data-stu-id="0df3c-123">110110 – Cash</span></span>                | <span data-ttu-id="0df3c-124">USD</span><span class="sxs-lookup"><span data-stu-id="0df3c-124">USD</span></span>      | <span data-ttu-id="0df3c-125">500</span><span class="sxs-lookup"><span data-stu-id="0df3c-125">500</span></span>    |
| <span data-ttu-id="0df3c-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-126">10/11/2015</span></span> | <span data-ttu-id="0df3c-127">130100 – Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="0df3c-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="0df3c-128">USD</span><span class="sxs-lookup"><span data-stu-id="0df3c-128">USD</span></span>      | <span data-ttu-id="0df3c-129">-500</span><span class="sxs-lookup"><span data-stu-id="0df3c-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="0df3c-130">Vaihtokurssit</span><span class="sxs-lookup"><span data-stu-id="0df3c-130">Exchange rates</span></span>

| <span data-ttu-id="0df3c-131">Lähdevaluutta</span><span class="sxs-lookup"><span data-stu-id="0df3c-131">From currency</span></span> | <span data-ttu-id="0df3c-132">Valuutaksi</span><span class="sxs-lookup"><span data-stu-id="0df3c-132">To currency</span></span> | <span data-ttu-id="0df3c-133">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="0df3c-133">Start date</span></span> | <span data-ttu-id="0df3c-134">Vaihtokurssi</span><span class="sxs-lookup"><span data-stu-id="0df3c-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="0df3c-135">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-135">EUR</span></span>           | <span data-ttu-id="0df3c-136">USD</span><span class="sxs-lookup"><span data-stu-id="0df3c-136">USD</span></span>         | <span data-ttu-id="0df3c-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-137">10/1/2015</span></span>  | <span data-ttu-id="0df3c-138">200</span><span class="sxs-lookup"><span data-stu-id="0df3c-138">200</span></span>           |
| <span data-ttu-id="0df3c-139">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-139">EUR</span></span>           | <span data-ttu-id="0df3c-140">USD</span><span class="sxs-lookup"><span data-stu-id="0df3c-140">USD</span></span>         | <span data-ttu-id="0df3c-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-141">11/1/2015</span></span>  | <span data-ttu-id="0df3c-142">150</span><span class="sxs-lookup"><span data-stu-id="0df3c-142">150</span></span>           |
| <span data-ttu-id="0df3c-143">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-143">EUR</span></span>           | <span data-ttu-id="0df3c-144">USD</span><span class="sxs-lookup"><span data-stu-id="0df3c-144">USD</span></span>         | <span data-ttu-id="0df3c-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="0df3c-145">12/1/2012</span></span>  | <span data-ttu-id="0df3c-146">100</span><span class="sxs-lookup"><span data-stu-id="0df3c-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="0df3c-147">Suorita konsolidointi lokakuulle 2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0df3c-148">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="0df3c-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="0df3c-149">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="0df3c-149">Ledger account</span></span> | <span data-ttu-id="0df3c-150">Valuutta</span><span class="sxs-lookup"><span data-stu-id="0df3c-150">Currency</span></span> | <span data-ttu-id="0df3c-151">Summa</span><span class="sxs-lookup"><span data-stu-id="0df3c-151">Amount</span></span> | <span data-ttu-id="0df3c-152">Laskenta</span><span class="sxs-lookup"><span data-stu-id="0df3c-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="0df3c-153">110110</span><span class="sxs-lookup"><span data-stu-id="0df3c-153">110110</span></span>         | <span data-ttu-id="0df3c-154">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-154">EUR</span></span>      | <span data-ttu-id="0df3c-155">250</span><span class="sxs-lookup"><span data-stu-id="0df3c-155">250</span></span>    | <span data-ttu-id="0df3c-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="0df3c-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="0df3c-157">130100</span><span class="sxs-lookup"><span data-stu-id="0df3c-157">130100</span></span>         | <span data-ttu-id="0df3c-158">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-158">EUR</span></span>      | <span data-ttu-id="0df3c-159">-250</span><span class="sxs-lookup"><span data-stu-id="0df3c-159">-250</span></span>   | <span data-ttu-id="0df3c-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="0df3c-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="0df3c-161">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 30.11.2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0df3c-162">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="0df3c-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="0df3c-163">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="0df3c-163">Ledger account</span></span> | <span data-ttu-id="0df3c-164">Valuutta</span><span class="sxs-lookup"><span data-stu-id="0df3c-164">Currency</span></span> | <span data-ttu-id="0df3c-165">Summa</span><span class="sxs-lookup"><span data-stu-id="0df3c-165">Amount</span></span>  | <span data-ttu-id="0df3c-166">Laskenta</span><span class="sxs-lookup"><span data-stu-id="0df3c-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="0df3c-167">110110</span><span class="sxs-lookup"><span data-stu-id="0df3c-167">110110</span></span>         | <span data-ttu-id="0df3c-168">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-168">EUR</span></span>      | <span data-ttu-id="0df3c-169">333,33</span><span class="sxs-lookup"><span data-stu-id="0df3c-169">333.33</span></span>  | <span data-ttu-id="0df3c-170">Alkuperäinen summa 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="0df3c-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="0df3c-171">130100</span><span class="sxs-lookup"><span data-stu-id="0df3c-171">130100</span></span>         | <span data-ttu-id="0df3c-172">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-172">EUR</span></span>      | <span data-ttu-id="0df3c-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="0df3c-173">-333.33</span></span> | <span data-ttu-id="0df3c-174">Alkuperäinen summa -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="0df3c-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="0df3c-175">801400</span><span class="sxs-lookup"><span data-stu-id="0df3c-175">801400</span></span>         | <span data-ttu-id="0df3c-176">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-176">EUR</span></span>      | <span data-ttu-id="0df3c-177">83,33</span><span class="sxs-lookup"><span data-stu-id="0df3c-177">83.33</span></span>   | <span data-ttu-id="0df3c-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="0df3c-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="0df3c-179">801600</span><span class="sxs-lookup"><span data-stu-id="0df3c-179">801600</span></span>         | <span data-ttu-id="0df3c-180">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-180">EUR</span></span>      | <span data-ttu-id="0df3c-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="0df3c-181">-83.33</span></span>  | <span data-ttu-id="0df3c-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="0df3c-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="0df3c-183">Näet tässä lisätapahtumia raportointivaluutan summille.</span><span class="sxs-lookup"><span data-stu-id="0df3c-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="0df3c-184">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 31.12.2015</span><span class="sxs-lookup"><span data-stu-id="0df3c-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0df3c-185">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="0df3c-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="0df3c-186">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="0df3c-186">Ledger account</span></span> | <span data-ttu-id="0df3c-187">Valuutta</span><span class="sxs-lookup"><span data-stu-id="0df3c-187">Currency</span></span> | <span data-ttu-id="0df3c-188">Summa</span><span class="sxs-lookup"><span data-stu-id="0df3c-188">Amount</span></span>  | <span data-ttu-id="0df3c-189">Laskenta</span><span class="sxs-lookup"><span data-stu-id="0df3c-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="0df3c-190">110110</span><span class="sxs-lookup"><span data-stu-id="0df3c-190">110110</span></span>         | <span data-ttu-id="0df3c-191">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-191">EUR</span></span>      | <span data-ttu-id="0df3c-192">500,00</span><span class="sxs-lookup"><span data-stu-id="0df3c-192">500.00</span></span>  | <span data-ttu-id="0df3c-193">Alkuperäinen summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="0df3c-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="0df3c-194">130100</span><span class="sxs-lookup"><span data-stu-id="0df3c-194">130100</span></span>         | <span data-ttu-id="0df3c-195">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-195">EUR</span></span>      | <span data-ttu-id="0df3c-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="0df3c-196">-500.00</span></span> | <span data-ttu-id="0df3c-197">Alkuperäinen summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="0df3c-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="0df3c-198">801400</span><span class="sxs-lookup"><span data-stu-id="0df3c-198">801400</span></span>         | <span data-ttu-id="0df3c-199">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-199">EUR</span></span>      | <span data-ttu-id="0df3c-200">250</span><span class="sxs-lookup"><span data-stu-id="0df3c-200">250</span></span>     | <span data-ttu-id="0df3c-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="0df3c-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="0df3c-202">801600</span><span class="sxs-lookup"><span data-stu-id="0df3c-202">801600</span></span>         | <span data-ttu-id="0df3c-203">Euro</span><span class="sxs-lookup"><span data-stu-id="0df3c-203">EUR</span></span>      | <span data-ttu-id="0df3c-204">-250</span><span class="sxs-lookup"><span data-stu-id="0df3c-204">-250</span></span>    | <span data-ttu-id="0df3c-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="0df3c-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






