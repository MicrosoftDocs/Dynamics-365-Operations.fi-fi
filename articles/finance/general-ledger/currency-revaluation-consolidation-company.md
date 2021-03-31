---
title: Valuutan uudelleenarvostus konsolidointiyrityksessä
description: Tässä aiheessa käsitellään valuutan uudelleenarvostus konsolidointiyrityksessä.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212226"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f5517-103">Valuutan uudelleenarvostus konsolidointiyrityksessä</span><span class="sxs-lookup"><span data-stu-id="f5517-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5517-104">Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, sinun on silti ajettava valuutan uudelleenarvostus, jos vaihtokursseissa tapahtuu muutoksia niin, että tiliesi saldot on uudelleenarvostettu oikein.</span><span class="sxs-lookup"><span data-stu-id="f5517-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f5517-105">Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdeltä ensimmäiset vaihtokurssit, jotka muunnetaan konsolidointiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="f5517-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f5517-106">Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot.</span><span class="sxs-lookup"><span data-stu-id="f5517-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f5517-107">Toteutumattomat voitot tai tappiot päivitetään sitten tämän mukaisesti uuden vaihtokurssin ja päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="f5517-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f5517-108">Seuraavassa esimerkissä on kuvattu kirjanpitomerkinnät, jotka luodaan tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="f5517-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f5517-109">Yrityksen asetukset</span><span class="sxs-lookup"><span data-stu-id="f5517-109">Company setup</span></span>
-   <span data-ttu-id="f5517-110">**Lähde/toimintaa harjoittava yritys (USMF)** – Yhdysvaltain dollareita (USD) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="f5517-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f5517-111">**Konsolidointiyritys (CON)** – Euroja (EUR) käytetään kirjanpito- ja raportointivaluuttana.</span><span class="sxs-lookup"><span data-stu-id="f5517-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f5517-112">**Toteutunut voitto**– Kirjanpitotili 801500</span><span class="sxs-lookup"><span data-stu-id="f5517-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="f5517-113">**Toteutunut tappio** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="f5517-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f5517-114">**Toteutumaton voitto** – Kirjanpitotili 801600</span><span class="sxs-lookup"><span data-stu-id="f5517-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f5517-115">**Toteutumaton tappio** – Kirjanpitotili 801400</span><span class="sxs-lookup"><span data-stu-id="f5517-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f5517-116">Alkuperäiset tapahtumat</span><span class="sxs-lookup"><span data-stu-id="f5517-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f5517-117">Kassamaksut USMF:ssä</span><span class="sxs-lookup"><span data-stu-id="f5517-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f5517-118">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="f5517-118">Date</span></span>       | <span data-ttu-id="f5517-119">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="f5517-119">Ledger account</span></span>               | <span data-ttu-id="f5517-120">Valuutta</span><span class="sxs-lookup"><span data-stu-id="f5517-120">Currency</span></span> | <span data-ttu-id="f5517-121">Summa</span><span class="sxs-lookup"><span data-stu-id="f5517-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f5517-122">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="f5517-122">10/11/2015</span></span> | <span data-ttu-id="f5517-123">110110 – Käteinen</span><span class="sxs-lookup"><span data-stu-id="f5517-123">110110 – Cash</span></span>                | <span data-ttu-id="f5517-124">USD</span><span class="sxs-lookup"><span data-stu-id="f5517-124">USD</span></span>      | <span data-ttu-id="f5517-125">500</span><span class="sxs-lookup"><span data-stu-id="f5517-125">500</span></span>    |
| <span data-ttu-id="f5517-126">11/10/2015</span><span class="sxs-lookup"><span data-stu-id="f5517-126">10/11/2015</span></span> | <span data-ttu-id="f5517-127">130100 – Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="f5517-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f5517-128">USD</span><span class="sxs-lookup"><span data-stu-id="f5517-128">USD</span></span>      | <span data-ttu-id="f5517-129">-500</span><span class="sxs-lookup"><span data-stu-id="f5517-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f5517-130">Vaihtokurssit</span><span class="sxs-lookup"><span data-stu-id="f5517-130">Exchange rates</span></span>

| <span data-ttu-id="f5517-131">Lähdevaluutta</span><span class="sxs-lookup"><span data-stu-id="f5517-131">From currency</span></span> | <span data-ttu-id="f5517-132">Valuutaksi</span><span class="sxs-lookup"><span data-stu-id="f5517-132">To currency</span></span> | <span data-ttu-id="f5517-133">Alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="f5517-133">Start date</span></span> | <span data-ttu-id="f5517-134">Vaihtokurssi</span><span class="sxs-lookup"><span data-stu-id="f5517-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f5517-135">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-135">EUR</span></span>           | <span data-ttu-id="f5517-136">USD</span><span class="sxs-lookup"><span data-stu-id="f5517-136">USD</span></span>         | <span data-ttu-id="f5517-137">1/10/2015</span><span class="sxs-lookup"><span data-stu-id="f5517-137">10/1/2015</span></span>  | <span data-ttu-id="f5517-138">200</span><span class="sxs-lookup"><span data-stu-id="f5517-138">200</span></span>           |
| <span data-ttu-id="f5517-139">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-139">EUR</span></span>           | <span data-ttu-id="f5517-140">USD</span><span class="sxs-lookup"><span data-stu-id="f5517-140">USD</span></span>         | <span data-ttu-id="f5517-141">1/11/2015</span><span class="sxs-lookup"><span data-stu-id="f5517-141">11/1/2015</span></span>  | <span data-ttu-id="f5517-142">150</span><span class="sxs-lookup"><span data-stu-id="f5517-142">150</span></span>           |
| <span data-ttu-id="f5517-143">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-143">EUR</span></span>           | <span data-ttu-id="f5517-144">USD</span><span class="sxs-lookup"><span data-stu-id="f5517-144">USD</span></span>         | <span data-ttu-id="f5517-145">1/12/2012</span><span class="sxs-lookup"><span data-stu-id="f5517-145">12/1/2012</span></span>  | <span data-ttu-id="f5517-146">100</span><span class="sxs-lookup"><span data-stu-id="f5517-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f5517-147">Suorita konsolidointi lokakuulle 2015</span><span class="sxs-lookup"><span data-stu-id="f5517-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f5517-148">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="f5517-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="f5517-149">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="f5517-149">Ledger account</span></span> | <span data-ttu-id="f5517-150">Valuutta</span><span class="sxs-lookup"><span data-stu-id="f5517-150">Currency</span></span> | <span data-ttu-id="f5517-151">Summa</span><span class="sxs-lookup"><span data-stu-id="f5517-151">Amount</span></span> | <span data-ttu-id="f5517-152">Laskenta</span><span class="sxs-lookup"><span data-stu-id="f5517-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f5517-153">110110</span><span class="sxs-lookup"><span data-stu-id="f5517-153">110110</span></span>         | <span data-ttu-id="f5517-154">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-154">EUR</span></span>      | <span data-ttu-id="f5517-155">250</span><span class="sxs-lookup"><span data-stu-id="f5517-155">250</span></span>    | <span data-ttu-id="f5517-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f5517-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="f5517-157">130100</span><span class="sxs-lookup"><span data-stu-id="f5517-157">130100</span></span>         | <span data-ttu-id="f5517-158">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-158">EUR</span></span>      | <span data-ttu-id="f5517-159">-250</span><span class="sxs-lookup"><span data-stu-id="f5517-159">-250</span></span>   | <span data-ttu-id="f5517-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f5517-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f5517-161">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 30.11.2015</span><span class="sxs-lookup"><span data-stu-id="f5517-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f5517-162">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="f5517-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="f5517-163">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="f5517-163">Ledger account</span></span> | <span data-ttu-id="f5517-164">Valuutta</span><span class="sxs-lookup"><span data-stu-id="f5517-164">Currency</span></span> | <span data-ttu-id="f5517-165">Summa</span><span class="sxs-lookup"><span data-stu-id="f5517-165">Amount</span></span>  | <span data-ttu-id="f5517-166">Laskenta</span><span class="sxs-lookup"><span data-stu-id="f5517-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f5517-167">110110</span><span class="sxs-lookup"><span data-stu-id="f5517-167">110110</span></span>         | <span data-ttu-id="f5517-168">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-168">EUR</span></span>      | <span data-ttu-id="f5517-169">333,33</span><span class="sxs-lookup"><span data-stu-id="f5517-169">333.33</span></span>  | <span data-ttu-id="f5517-170">Alkuperäinen summa 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f5517-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f5517-171">130100</span><span class="sxs-lookup"><span data-stu-id="f5517-171">130100</span></span>         | <span data-ttu-id="f5517-172">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-172">EUR</span></span>      | <span data-ttu-id="f5517-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="f5517-173">-333.33</span></span> | <span data-ttu-id="f5517-174">Alkuperäinen summa -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f5517-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f5517-175">801400</span><span class="sxs-lookup"><span data-stu-id="f5517-175">801400</span></span>         | <span data-ttu-id="f5517-176">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-176">EUR</span></span>      | <span data-ttu-id="f5517-177">83,33</span><span class="sxs-lookup"><span data-stu-id="f5517-177">83.33</span></span>   | <span data-ttu-id="f5517-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="f5517-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="f5517-179">801600</span><span class="sxs-lookup"><span data-stu-id="f5517-179">801600</span></span>         | <span data-ttu-id="f5517-180">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-180">EUR</span></span>      | <span data-ttu-id="f5517-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="f5517-181">-83.33</span></span>  | <span data-ttu-id="f5517-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="f5517-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f5517-183">Näet tässä lisätapahtumia raportointivaluutan summille.</span><span class="sxs-lookup"><span data-stu-id="f5517-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f5517-184">Suorita valuutan uudelleenarvostus tileille kaudella 1.10.2015 - 31.12.2015</span><span class="sxs-lookup"><span data-stu-id="f5517-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f5517-185">Konsolidointiyrityksen saldot</span><span class="sxs-lookup"><span data-stu-id="f5517-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="f5517-186">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="f5517-186">Ledger account</span></span> | <span data-ttu-id="f5517-187">Valuutta</span><span class="sxs-lookup"><span data-stu-id="f5517-187">Currency</span></span> | <span data-ttu-id="f5517-188">Summa</span><span class="sxs-lookup"><span data-stu-id="f5517-188">Amount</span></span>  | <span data-ttu-id="f5517-189">Laskenta</span><span class="sxs-lookup"><span data-stu-id="f5517-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f5517-190">110110</span><span class="sxs-lookup"><span data-stu-id="f5517-190">110110</span></span>         | <span data-ttu-id="f5517-191">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-191">EUR</span></span>      | <span data-ttu-id="f5517-192">500,00</span><span class="sxs-lookup"><span data-stu-id="f5517-192">500.00</span></span>  | <span data-ttu-id="f5517-193">Alkuperäinen summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="f5517-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f5517-194">130100</span><span class="sxs-lookup"><span data-stu-id="f5517-194">130100</span></span>         | <span data-ttu-id="f5517-195">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-195">EUR</span></span>      | <span data-ttu-id="f5517-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="f5517-196">-500.00</span></span> | <span data-ttu-id="f5517-197">Alkuperäinen summa -500 × 1</span><span class="sxs-lookup"><span data-stu-id="f5517-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f5517-198">801400</span><span class="sxs-lookup"><span data-stu-id="f5517-198">801400</span></span>         | <span data-ttu-id="f5517-199">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-199">EUR</span></span>      | <span data-ttu-id="f5517-200">250</span><span class="sxs-lookup"><span data-stu-id="f5517-200">250</span></span>     | <span data-ttu-id="f5517-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="f5517-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f5517-202">801600</span><span class="sxs-lookup"><span data-stu-id="f5517-202">801600</span></span>         | <span data-ttu-id="f5517-203">Euro</span><span class="sxs-lookup"><span data-stu-id="f5517-203">EUR</span></span>      | <span data-ttu-id="f5517-204">-250</span><span class="sxs-lookup"><span data-stu-id="f5517-204">-250</span></span>    | <span data-ttu-id="f5517-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="f5517-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]