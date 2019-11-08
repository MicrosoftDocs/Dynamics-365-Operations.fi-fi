---
title: Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen
description: Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570191"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="c3a79-103">Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen</span><span class="sxs-lookup"><span data-stu-id="c3a79-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3a79-104">Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.</span><span class="sxs-lookup"><span data-stu-id="c3a79-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="c3a79-105">Prosessi voidaan jakaa kolmeen vaiheeseen:</span><span class="sxs-lookup"><span data-stu-id="c3a79-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="c3a79-106">Määritä arvonlisäveron suunta.</span><span class="sxs-lookup"><span data-stu-id="c3a79-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="c3a79-107">Määritä arvonlisäveron summa, joka tallennetaan väliaikaiseen arvonlisäveron tauluun.</span><span class="sxs-lookup"><span data-stu-id="c3a79-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="c3a79-108">Määritä arvonlisäveron summa ja tositteessa oleva tili.</span><span class="sxs-lookup"><span data-stu-id="c3a79-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="c3a79-109">Määritä arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="c3a79-109">Determine the sales tax direction</span></span>

<span data-ttu-id="c3a79-110">Arvonlisäveron suunnan määritystapa riippuu tositteessa olevan tilin tyypistä.</span><span class="sxs-lookup"><span data-stu-id="c3a79-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="c3a79-111">Arvonlisäveron suunta määräytyy tilin tyypin ja arvonlisäverokoodin yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="c3a79-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="c3a79-112">Seuraavat osiot selittävät vaihtoehdot yksityiskohtaisemmin.</span><span class="sxs-lookup"><span data-stu-id="c3a79-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="c3a79-113">Tilin tyyppi on Projekti</span><span class="sxs-lookup"><span data-stu-id="c3a79-113">Account type is Project</span></span>

<span data-ttu-id="c3a79-114">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Projekti**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="c3a79-115">Sääntö esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-115">The following illustration shows the rule.</span></span> <span data-ttu-id="c3a79-116">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat projektitileille.</span><span class="sxs-lookup"><span data-stu-id="c3a79-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="c3a79-117">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="c3a79-118">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="c3a79-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c3a79-119">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c3a79-120">•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c3a79-121">Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="c3a79-122">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="c3a79-122">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat projektitileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="c3a79-124">Tilin tyyppi on Toimittaja</span><span class="sxs-lookup"><span data-stu-id="c3a79-124">Account type is Vendor</span></span>

<span data-ttu-id="c3a79-125">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Toimittaja**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="c3a79-126">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat toimittajatileille.</span><span class="sxs-lookup"><span data-stu-id="c3a79-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="c3a79-127">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="c3a79-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c3a79-128">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="c3a79-129">•   Jos arvonlisävero on käänteinen veloitus, arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="c3a79-130">Muussa tapauksessa arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c3a79-131">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="c3a79-131">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat toimittajatileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="c3a79-133">Tilin tyyppi on Asiakas</span><span class="sxs-lookup"><span data-stu-id="c3a79-133">Account type is Customer</span></span>

<span data-ttu-id="c3a79-134">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Asiakas**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="c3a79-135">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat asiakastileille.</span><span class="sxs-lookup"><span data-stu-id="c3a79-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="c3a79-136">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="c3a79-137">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="c3a79-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c3a79-138">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c3a79-139">•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c3a79-140">Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="c3a79-141">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="c3a79-141">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat asiakastileille](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="c3a79-143">Tilin tyyppi on Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="c3a79-143">Account type is Ledger</span></span>

<span data-ttu-id="c3a79-144">Seuraavassa kuvassa esitetään sääntö, jota käytetään, kun tositteessa on vain kirjauskansiorivejä, joissa tilin tyyppi **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="c3a79-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="c3a79-145">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="c3a79-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="c3a79-146">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="c3a79-147">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="c3a79-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="c3a79-148">Muussa tapauksessa, jos kirjauskansion summa on debet (positiivinen), arvonlisäveron suunta on Saatava arvonlisävero. Jos kirjauskansion summa on kredit (negatiivinen), arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="c3a79-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="c3a79-149">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="c3a79-149">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat kirjanpitotileille](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="c3a79-151">Korvaa arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="c3a79-151">Override the sales tax direction</span></span>

<span data-ttu-id="c3a79-152">Voit korvata arvonlisäveron suunnan, kun tosite sisältää vain rivejä, jossa tilin tyyppi on **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="c3a79-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="c3a79-153">Siirry kohtaan **Kirjanpito \> Tilikartta \> Tilit \> Päätilit** ja valitse **Yrityksen ohitukset** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="c3a79-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="c3a79-154">Määritä arvonlisäveron summa</span><span class="sxs-lookup"><span data-stu-id="c3a79-154">Determine the sales tax amount</span></span>

<span data-ttu-id="c3a79-155">Tässä osiossa kuvataan, miten arvonlisäveron summan etumerkki lasketaan.</span><span class="sxs-lookup"><span data-stu-id="c3a79-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Arvonlisäverotapahtumat-sivu](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="c3a79-157">Seuraavassa taulukossa esitetään yleinen sääntö, joka määrittää arvonlisäveron summien etumerkin väliaikaisessa arvonlisäveron taulussa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="c3a79-158">Kirjauskansiorivin summa</span><span class="sxs-lookup"><span data-stu-id="c3a79-158">Journal line amount</span></span> | <span data-ttu-id="c3a79-159">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="c3a79-159">Sales tax direction</span></span>  | <span data-ttu-id="c3a79-160">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="c3a79-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="c3a79-161">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-161">Positive</span></span>            | <span data-ttu-id="c3a79-162">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-162">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-163">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-163">Positive</span></span>              |
| <span data-ttu-id="c3a79-164">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-164">Positive</span></span>            | <span data-ttu-id="c3a79-165">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-165">Sales Tax Payable</span></span>    | <span data-ttu-id="c3a79-166">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-166">Negative</span></span>              |
| <span data-ttu-id="c3a79-167">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-167">Negative</span></span>            | <span data-ttu-id="c3a79-168">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-168">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-169">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-169">Negative</span></span>              |
| <span data-ttu-id="c3a79-170">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-170">Negative</span></span>            | <span data-ttu-id="c3a79-171">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-171">Sales Tax Payable</span></span>    | <span data-ttu-id="c3a79-172">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-172">Positive</span></span>              |

<span data-ttu-id="c3a79-173">Tositteilla, joilla on vain **Projekti**- tai **Kirjanpito**-rivejä, on erityissääntö, kun **Kirjanpito**-riville on valittu arvonlisäveroryhmä tai nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="c3a79-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="c3a79-174">Tätä sääntöä ohjaa yleisten kirjauskansioiden Ota käyttöön itsenäinen arvonlisäveron laskeminen -toiminto.</span><span class="sxs-lookup"><span data-stu-id="c3a79-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="c3a79-175">Kun tämä toiminto ei ole käytössä, **Kirjanpito**-rivin veron summa käyttää **Projekti**-rivin debet/kredit-suuntaa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="c3a79-176">Kun tämä toiminto on käytössä, **Kirjanpito**-rivin veron summa käyttää sen omaa debet/kredit-suuntaa.</span><span class="sxs-lookup"><span data-stu-id="c3a79-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="c3a79-177">Seuraava taulukko esittää säännön molemmille skenaariolle.</span><span class="sxs-lookup"><span data-stu-id="c3a79-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="c3a79-178">**Sääntö, kun toiminto on käytössä**</span><span class="sxs-lookup"><span data-stu-id="c3a79-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="c3a79-179">Kirjauskansiorivin projektin summa</span><span class="sxs-lookup"><span data-stu-id="c3a79-179">Journal line amount of project</span></span> | <span data-ttu-id="c3a79-180">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="c3a79-180">Sales tax direction</span></span>  | <span data-ttu-id="c3a79-181">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="c3a79-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="c3a79-182">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-182">Positive</span></span>                       | <span data-ttu-id="c3a79-183">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-183">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-184">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-184">Positive</span></span>              |
| <span data-ttu-id="c3a79-185">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-185">Negative</span></span>                       | <span data-ttu-id="c3a79-186">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-186">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-187">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-187">Negative</span></span>              |

<span data-ttu-id="c3a79-188">**Sääntö, kun toiminto ei ole käytössä**</span><span class="sxs-lookup"><span data-stu-id="c3a79-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="c3a79-189">Kirjauskansiorivin kirjanpidon summa</span><span class="sxs-lookup"><span data-stu-id="c3a79-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="c3a79-190">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="c3a79-190">Sales tax direction</span></span>  | <span data-ttu-id="c3a79-191">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="c3a79-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="c3a79-192">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-192">Positive</span></span>                       | <span data-ttu-id="c3a79-193">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-193">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-194">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-194">Positive</span></span>              |
| <span data-ttu-id="c3a79-195">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-195">Negative</span></span>                       | <span data-ttu-id="c3a79-196">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-196">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-197">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="c3a79-198">Määritä arvonlisäveron summa ja tositteessa oleva tili</span><span class="sxs-lookup"><span data-stu-id="c3a79-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="c3a79-199">Kun kirjaat arvonlisäveroja, päätili haetaan kirjanpidon kirjausryhmän profiilista.</span><span class="sxs-lookup"><span data-stu-id="c3a79-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="c3a79-200">Kun arvonlisäverot ovat saatavia, järjestelmä käyttää profiilissa määritettyä Saatava arvonlisävero -tiliä.</span><span class="sxs-lookup"><span data-stu-id="c3a79-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="c3a79-201">Kun arvonlisäverot ovat maksettavia, järjestelmä käyttää profiilissa määritettyä Maksettava arvonlisävero -tiliä.</span><span class="sxs-lookup"><span data-stu-id="c3a79-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="c3a79-202">Seuraavassa taulukossa kuvataan yleinen sääntö.</span><span class="sxs-lookup"><span data-stu-id="c3a79-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="c3a79-203">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="c3a79-203">Sales tax direction</span></span>  | <span data-ttu-id="c3a79-204">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="c3a79-204">Sales tax amount sign</span></span> | <span data-ttu-id="c3a79-205">Arvonlisäverotili</span><span class="sxs-lookup"><span data-stu-id="c3a79-205">Sales tax account</span></span>      | <span data-ttu-id="c3a79-206">Tositteen summa</span><span class="sxs-lookup"><span data-stu-id="c3a79-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="c3a79-207">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-207">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-208">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-208">Positive</span></span>              | <span data-ttu-id="c3a79-209">Saatava vero -tili</span><span class="sxs-lookup"><span data-stu-id="c3a79-209">Tax Receivable Account</span></span> | <span data-ttu-id="c3a79-210">Positiivinen (debet)</span><span class="sxs-lookup"><span data-stu-id="c3a79-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="c3a79-211">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-211">Sales Tax Receivable</span></span> | <span data-ttu-id="c3a79-212">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-212">Negative</span></span>              | <span data-ttu-id="c3a79-213">Saatava vero -tili</span><span class="sxs-lookup"><span data-stu-id="c3a79-213">Tax Receivable Account</span></span> | <span data-ttu-id="c3a79-214">Negatiivinen (kredit)</span><span class="sxs-lookup"><span data-stu-id="c3a79-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="c3a79-215">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-215">Sales Tax Payable</span></span>    | <span data-ttu-id="c3a79-216">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-216">Positive</span></span>              | <span data-ttu-id="c3a79-217">Maksettava vero -tili</span><span class="sxs-lookup"><span data-stu-id="c3a79-217">Tax Payable Account</span></span>    | <span data-ttu-id="c3a79-218">Negatiivinen (kredit)</span><span class="sxs-lookup"><span data-stu-id="c3a79-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="c3a79-219">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="c3a79-219">Sales Tax Payable</span></span>    | <span data-ttu-id="c3a79-220">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="c3a79-220">Negative</span></span>              | <span data-ttu-id="c3a79-221">Maksettava vero -tili</span><span class="sxs-lookup"><span data-stu-id="c3a79-221">Tax Payable Account</span></span>    | <span data-ttu-id="c3a79-222">Positiivinen (debet)</span><span class="sxs-lookup"><span data-stu-id="c3a79-222">Positive (Debit)</span></span>  |
