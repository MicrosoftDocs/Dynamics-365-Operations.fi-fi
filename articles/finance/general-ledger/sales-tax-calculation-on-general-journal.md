---
title: Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen
description: Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.
author: EricWang
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e4d367fe6cb729c9c5658a9bbbac04e53fdf9644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815329"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="7f9bf-103">Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f9bf-104">Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="7f9bf-105">Prosessi voidaan jakaa kolmeen vaiheeseen:</span><span class="sxs-lookup"><span data-stu-id="7f9bf-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="7f9bf-106">Määritä arvonlisäveron suunta.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="7f9bf-107">Määritä arvonlisäveron summa, joka tallennetaan väliaikaiseen arvonlisäveron tauluun.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="7f9bf-108">Määritä arvonlisäveron summa ja tositteessa oleva tili.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="7f9bf-109">Määritä arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="7f9bf-109">Determine the sales tax direction</span></span>

<span data-ttu-id="7f9bf-110">Arvonlisäveron suunnan määritystapa riippuu tositteessa olevan tilin tyypistä.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="7f9bf-111">Arvonlisäveron suunta määräytyy tilin tyypin ja arvonlisäverokoodin yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="7f9bf-112">Seuraavat osiot selittävät vaihtoehdot yksityiskohtaisemmin.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="7f9bf-113">Tilin tyyppi on Projekti</span><span class="sxs-lookup"><span data-stu-id="7f9bf-113">Account type is Project</span></span>

<span data-ttu-id="7f9bf-114">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Projekti**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="7f9bf-115">Sääntö esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-115">The following illustration shows the rule.</span></span> <span data-ttu-id="7f9bf-116">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat projektitileille.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="7f9bf-117">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="7f9bf-118">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="7f9bf-119">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="7f9bf-120">•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="7f9bf-121">Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="7f9bf-122">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-122">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat projektitileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="7f9bf-124">Tilin tyyppi on Toimittaja</span><span class="sxs-lookup"><span data-stu-id="7f9bf-124">Account type is Vendor</span></span>

<span data-ttu-id="7f9bf-125">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Toimittaja**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="7f9bf-126">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat toimittajatileille.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="7f9bf-127">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="7f9bf-128">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="7f9bf-129">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="7f9bf-130">•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="7f9bf-131">Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="7f9bf-132">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-132">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat toimittajatileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="7f9bf-134">Tilin tyyppi on Asiakas</span><span class="sxs-lookup"><span data-stu-id="7f9bf-134">Account type is Customer</span></span>

<span data-ttu-id="7f9bf-135">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Asiakas**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="7f9bf-136">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat asiakastileille.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="7f9bf-137">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="7f9bf-138">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="7f9bf-139">•   Jos arvonlisävero on käänteinen veloitus, arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="7f9bf-140">Muussa tapauksessa arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="7f9bf-141">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-141">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat asiakastileille](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="7f9bf-143">Tilin tyyppi on Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="7f9bf-143">Account type is Ledger</span></span>

<span data-ttu-id="7f9bf-144">Seuraavassa kuvassa esitetään sääntö, jota käytetään, kun tositteessa on vain kirjauskansiorivejä, joissa tilin tyyppi **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="7f9bf-145">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="7f9bf-146">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="7f9bf-147">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="7f9bf-148">Muussa tapauksessa, jos kirjauskansion summa on debet (positiivinen), arvonlisäveron suunta on Saatava arvonlisävero. Jos kirjauskansion summa on kredit (negatiivinen), arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="7f9bf-149">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-149">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat kirjanpitotileille](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="7f9bf-151">Korvaa arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="7f9bf-151">Override the sales tax direction</span></span>

<span data-ttu-id="7f9bf-152">Voit korvata arvonlisäveron suunnan, kun tosite sisältää vain rivejä, jossa tilin tyyppi on **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="7f9bf-153">Siirry kohtaan **Kirjanpito \> Tilikartta \> Tilit \> Päätilit** ja valitse **Yrityksen ohitukset** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="7f9bf-154">Määritä arvonlisäveron summa</span><span class="sxs-lookup"><span data-stu-id="7f9bf-154">Determine the sales tax amount</span></span>

<span data-ttu-id="7f9bf-155">Tässä osiossa kuvataan, miten arvonlisäveron summan etumerkki lasketaan.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Arvonlisäverotapahtumat-sivu](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="7f9bf-157">Seuraavassa taulukossa esitetään yleinen sääntö, joka määrittää arvonlisäveron summien etumerkin väliaikaisessa arvonlisäveron taulussa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="7f9bf-158">Kirjauskansiorivin summa</span><span class="sxs-lookup"><span data-stu-id="7f9bf-158">Journal line amount</span></span> | <span data-ttu-id="7f9bf-159">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="7f9bf-159">Sales tax direction</span></span>  | <span data-ttu-id="7f9bf-160">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="7f9bf-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="7f9bf-161">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-161">Positive</span></span>            | <span data-ttu-id="7f9bf-162">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-162">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-163">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-163">Positive</span></span>              |
| <span data-ttu-id="7f9bf-164">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-164">Positive</span></span>            | <span data-ttu-id="7f9bf-165">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-165">Sales Tax Payable</span></span>    | <span data-ttu-id="7f9bf-166">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-166">Negative</span></span>              |
| <span data-ttu-id="7f9bf-167">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-167">Negative</span></span>            | <span data-ttu-id="7f9bf-168">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-168">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-169">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-169">Negative</span></span>              |
| <span data-ttu-id="7f9bf-170">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-170">Negative</span></span>            | <span data-ttu-id="7f9bf-171">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-171">Sales Tax Payable</span></span>    | <span data-ttu-id="7f9bf-172">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-172">Positive</span></span>              |

<span data-ttu-id="7f9bf-173">Tositteilla, joilla on vain **Projekti**- tai **Kirjanpito**-rivejä, on erityissääntö, kun **Kirjanpito**-riville on valittu arvonlisäveroryhmä tai nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="7f9bf-174">Tätä sääntöä ohjaa yleisten kirjauskansioiden Ota käyttöön itsenäinen arvonlisäveron laskeminen -toiminto.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="7f9bf-175">Kun tämä toiminto ei ole käytössä, **Kirjanpito**-rivin veron summa käyttää **Projekti**-rivin debet/kredit-suuntaa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="7f9bf-176">Kun tämä toiminto on käytössä, **Kirjanpito**-rivin veron summa käyttää sen omaa debet/kredit-suuntaa.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="7f9bf-177">Seuraava taulukko esittää säännön molemmille skenaariolle.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="7f9bf-178">**Sääntö, kun toiminto on käytössä**</span><span class="sxs-lookup"><span data-stu-id="7f9bf-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="7f9bf-179">Kirjauskansiorivin projektin summa</span><span class="sxs-lookup"><span data-stu-id="7f9bf-179">Journal line amount of project</span></span> | <span data-ttu-id="7f9bf-180">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="7f9bf-180">Sales tax direction</span></span>  | <span data-ttu-id="7f9bf-181">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="7f9bf-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="7f9bf-182">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-182">Positive</span></span>                       | <span data-ttu-id="7f9bf-183">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-183">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-184">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-184">Positive</span></span>              |
| <span data-ttu-id="7f9bf-185">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-185">Negative</span></span>                       | <span data-ttu-id="7f9bf-186">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-186">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-187">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-187">Negative</span></span>              |

<span data-ttu-id="7f9bf-188">**Sääntö, kun toiminto ei ole käytössä**</span><span class="sxs-lookup"><span data-stu-id="7f9bf-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="7f9bf-189">Kirjauskansiorivin kirjanpidon summa</span><span class="sxs-lookup"><span data-stu-id="7f9bf-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="7f9bf-190">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="7f9bf-190">Sales tax direction</span></span>  | <span data-ttu-id="7f9bf-191">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="7f9bf-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="7f9bf-192">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-192">Positive</span></span>                       | <span data-ttu-id="7f9bf-193">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-193">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-194">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-194">Positive</span></span>              |
| <span data-ttu-id="7f9bf-195">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-195">Negative</span></span>                       | <span data-ttu-id="7f9bf-196">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-196">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-197">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="7f9bf-198">Määritä arvonlisäveron summa ja tositteessa oleva tili</span><span class="sxs-lookup"><span data-stu-id="7f9bf-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="7f9bf-199">Kun kirjaat arvonlisäveroja, päätili haetaan kirjanpidon kirjausryhmän profiilista.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="7f9bf-200">Kun arvonlisäverot ovat saatavia, järjestelmä käyttää profiilissa määritettyä Saatava arvonlisävero -tiliä.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="7f9bf-201">Kun arvonlisäverot ovat maksettavia, järjestelmä käyttää profiilissa määritettyä Maksettava arvonlisävero -tiliä.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="7f9bf-202">Seuraavassa taulukossa kuvataan yleinen sääntö.</span><span class="sxs-lookup"><span data-stu-id="7f9bf-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="7f9bf-203">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="7f9bf-203">Sales tax direction</span></span>  | <span data-ttu-id="7f9bf-204">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="7f9bf-204">Sales tax amount sign</span></span> | <span data-ttu-id="7f9bf-205">Arvonlisäverotili</span><span class="sxs-lookup"><span data-stu-id="7f9bf-205">Sales tax account</span></span>      | <span data-ttu-id="7f9bf-206">Tositteen summa</span><span class="sxs-lookup"><span data-stu-id="7f9bf-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="7f9bf-207">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-207">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-208">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-208">Positive</span></span>              | <span data-ttu-id="7f9bf-209">Saatava vero -tili</span><span class="sxs-lookup"><span data-stu-id="7f9bf-209">Tax Receivable Account</span></span> | <span data-ttu-id="7f9bf-210">Positiivinen (debet)</span><span class="sxs-lookup"><span data-stu-id="7f9bf-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="7f9bf-211">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-211">Sales Tax Receivable</span></span> | <span data-ttu-id="7f9bf-212">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-212">Negative</span></span>              | <span data-ttu-id="7f9bf-213">Saatava vero -tili</span><span class="sxs-lookup"><span data-stu-id="7f9bf-213">Tax Receivable Account</span></span> | <span data-ttu-id="7f9bf-214">Negatiivinen (kredit)</span><span class="sxs-lookup"><span data-stu-id="7f9bf-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="7f9bf-215">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-215">Sales Tax Payable</span></span>    | <span data-ttu-id="7f9bf-216">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-216">Positive</span></span>              | <span data-ttu-id="7f9bf-217">Maksettava vero -tili</span><span class="sxs-lookup"><span data-stu-id="7f9bf-217">Tax Payable Account</span></span>    | <span data-ttu-id="7f9bf-218">Negatiivinen (kredit)</span><span class="sxs-lookup"><span data-stu-id="7f9bf-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="7f9bf-219">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="7f9bf-219">Sales Tax Payable</span></span>    | <span data-ttu-id="7f9bf-220">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="7f9bf-220">Negative</span></span>              | <span data-ttu-id="7f9bf-221">Maksettava vero -tili</span><span class="sxs-lookup"><span data-stu-id="7f9bf-221">Tax Payable Account</span></span>    | <span data-ttu-id="7f9bf-222">Positiivinen (debet)</span><span class="sxs-lookup"><span data-stu-id="7f9bf-222">Positive (Debit)</span></span>  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]