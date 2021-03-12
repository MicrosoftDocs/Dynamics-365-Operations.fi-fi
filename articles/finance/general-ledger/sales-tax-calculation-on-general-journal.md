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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e420632c248b5b43d4983c5eb483cac580e67f20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975555"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="a2b5d-103">Yleisten kirjauskansioiden rivien arvonlisäveron laskeminen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2b5d-104">Tässä aiheessa selitetään, miten arvonlisäverot lasketaan erityyppisille tileille (toimittaja, asiakas, kirjanpito ja projekti) yleisen kirjauskansioiden riveille.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="a2b5d-105">Prosessi voidaan jakaa kolmeen vaiheeseen:</span><span class="sxs-lookup"><span data-stu-id="a2b5d-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="a2b5d-106">Määritä arvonlisäveron suunta.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="a2b5d-107">Määritä arvonlisäveron summa, joka tallennetaan väliaikaiseen arvonlisäveron tauluun.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="a2b5d-108">Määritä arvonlisäveron summa ja tositteessa oleva tili.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="a2b5d-109">Määritä arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="a2b5d-109">Determine the sales tax direction</span></span>

<span data-ttu-id="a2b5d-110">Arvonlisäveron suunnan määritystapa riippuu tositteessa olevan tilin tyypistä.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="a2b5d-111">Arvonlisäveron suunta määräytyy tilin tyypin ja arvonlisäverokoodin yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="a2b5d-112">Seuraavat osiot selittävät vaihtoehdot yksityiskohtaisemmin.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="a2b5d-113">Tilin tyyppi on Projekti</span><span class="sxs-lookup"><span data-stu-id="a2b5d-113">Account type is Project</span></span>

<span data-ttu-id="a2b5d-114">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Projekti**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="a2b5d-115">Sääntö esitellään seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-115">The following illustration shows the rule.</span></span> <span data-ttu-id="a2b5d-116">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat projektitileille.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="a2b5d-117">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="a2b5d-118">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a2b5d-119">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a2b5d-120">•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a2b5d-121">Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a2b5d-122">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-122">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat projektitileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="a2b5d-124">Tilin tyyppi on Toimittaja</span><span class="sxs-lookup"><span data-stu-id="a2b5d-124">Account type is Vendor</span></span>

<span data-ttu-id="a2b5d-125">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Toimittaja**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="a2b5d-126">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat toimittajatileille.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="a2b5d-127">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="a2b5d-128">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a2b5d-129">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a2b5d-130">•   Jos arvonlisäverokoodi on käänteinen veloitus, arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a2b5d-131">Muussa tapauksessa arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a2b5d-132">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-132">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat toimittajatileille](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="a2b5d-134">Tilin tyyppi on Asiakas</span><span class="sxs-lookup"><span data-stu-id="a2b5d-134">Account type is Customer</span></span>

<span data-ttu-id="a2b5d-135">Jos tositteessa on kirjauskansiorivi, jossa tilin tyyppinä on **Asiakas**, kaikki tositteen kirjauskansiorivit käyttävät samaa veron suuntaa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="a2b5d-136">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat asiakastileille.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="a2b5d-137">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a2b5d-138">•   Jos arvonlisäverokoodi on EU:n sisäinen ALV, arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a2b5d-139">•   Jos arvonlisävero on käänteinen veloitus, arvonlisäveron suunta on Saatava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a2b5d-140">Muussa tapauksessa arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a2b5d-141">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-141">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat asiakastileille](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="a2b5d-143">Tilin tyyppi on Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="a2b5d-143">Account type is Ledger</span></span>

<span data-ttu-id="a2b5d-144">Seuraavassa kuvassa esitetään sääntö, jota käytetään, kun tositteessa on vain kirjauskansiorivejä, joissa tilin tyyppi **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="a2b5d-145">Seuraavissa kohdissa näytetään mahdolliset verojen suunnat kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="a2b5d-146">•   Jos arvonlisäverokoodi on käyttövero, arvonlisäveron suunta on Käyttövero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="a2b5d-147">•   Jos arvonlisäverokoodi on verovapaus, arvonlisäveron suunta on Verovapaa osto.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a2b5d-148">Muussa tapauksessa, jos kirjauskansion summa on debet (positiivinen), arvonlisäveron suunta on Saatava arvonlisävero. Jos kirjauskansion summa on kredit (negatiivinen), arvonlisäveron suunta on Maksettava arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a2b5d-149">Seuraava kaavio kuvaa säännön graafisesti.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-149">The following diagram illustrates the rule graphically.</span></span>

![Verojen mahdolliset suunnat kirjanpitotileille](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="a2b5d-151">Korvaa arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="a2b5d-151">Override the sales tax direction</span></span>

<span data-ttu-id="a2b5d-152">Voit korvata arvonlisäveron suunnan, kun tosite sisältää vain rivejä, jossa tilin tyyppi on **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="a2b5d-153">Siirry kohtaan **Kirjanpito \> Tilikartta \> Tilit \> Päätilit** ja valitse **Yrityksen ohitukset** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="a2b5d-154">Määritä arvonlisäveron summa</span><span class="sxs-lookup"><span data-stu-id="a2b5d-154">Determine the sales tax amount</span></span>

<span data-ttu-id="a2b5d-155">Tässä osiossa kuvataan, miten arvonlisäveron summan etumerkki lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Arvonlisäverotapahtumat-sivu](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="a2b5d-157">Seuraavassa taulukossa esitetään yleinen sääntö, joka määrittää arvonlisäveron summien etumerkin väliaikaisessa arvonlisäveron taulussa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="a2b5d-158">Kirjauskansiorivin summa</span><span class="sxs-lookup"><span data-stu-id="a2b5d-158">Journal line amount</span></span> | <span data-ttu-id="a2b5d-159">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="a2b5d-159">Sales tax direction</span></span>  | <span data-ttu-id="a2b5d-160">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="a2b5d-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="a2b5d-161">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-161">Positive</span></span>            | <span data-ttu-id="a2b5d-162">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-162">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-163">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-163">Positive</span></span>              |
| <span data-ttu-id="a2b5d-164">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-164">Positive</span></span>            | <span data-ttu-id="a2b5d-165">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-165">Sales Tax Payable</span></span>    | <span data-ttu-id="a2b5d-166">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-166">Negative</span></span>              |
| <span data-ttu-id="a2b5d-167">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-167">Negative</span></span>            | <span data-ttu-id="a2b5d-168">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-168">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-169">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-169">Negative</span></span>              |
| <span data-ttu-id="a2b5d-170">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-170">Negative</span></span>            | <span data-ttu-id="a2b5d-171">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-171">Sales Tax Payable</span></span>    | <span data-ttu-id="a2b5d-172">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-172">Positive</span></span>              |

<span data-ttu-id="a2b5d-173">Tositteilla, joilla on vain **Projekti**- tai **Kirjanpito**-rivejä, on erityissääntö, kun **Kirjanpito**-riville on valittu arvonlisäveroryhmä tai nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="a2b5d-174">Tätä sääntöä ohjaa yleisten kirjauskansioiden Ota käyttöön itsenäinen arvonlisäveron laskeminen -toiminto.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="a2b5d-175">Kun tämä toiminto ei ole käytössä, **Kirjanpito**-rivin veron summa käyttää **Projekti**-rivin debet/kredit-suuntaa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="a2b5d-176">Kun tämä toiminto on käytössä, **Kirjanpito**-rivin veron summa käyttää sen omaa debet/kredit-suuntaa.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="a2b5d-177">Seuraava taulukko esittää säännön molemmille skenaariolle.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="a2b5d-178">**Sääntö, kun toiminto on käytössä**</span><span class="sxs-lookup"><span data-stu-id="a2b5d-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="a2b5d-179">Kirjauskansiorivin projektin summa</span><span class="sxs-lookup"><span data-stu-id="a2b5d-179">Journal line amount of project</span></span> | <span data-ttu-id="a2b5d-180">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="a2b5d-180">Sales tax direction</span></span>  | <span data-ttu-id="a2b5d-181">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="a2b5d-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="a2b5d-182">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-182">Positive</span></span>                       | <span data-ttu-id="a2b5d-183">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-183">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-184">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-184">Positive</span></span>              |
| <span data-ttu-id="a2b5d-185">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-185">Negative</span></span>                       | <span data-ttu-id="a2b5d-186">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-186">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-187">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-187">Negative</span></span>              |

<span data-ttu-id="a2b5d-188">**Sääntö, kun toiminto ei ole käytössä**</span><span class="sxs-lookup"><span data-stu-id="a2b5d-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="a2b5d-189">Kirjauskansiorivin kirjanpidon summa</span><span class="sxs-lookup"><span data-stu-id="a2b5d-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="a2b5d-190">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="a2b5d-190">Sales tax direction</span></span>  | <span data-ttu-id="a2b5d-191">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="a2b5d-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="a2b5d-192">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-192">Positive</span></span>                       | <span data-ttu-id="a2b5d-193">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-193">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-194">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-194">Positive</span></span>              |
| <span data-ttu-id="a2b5d-195">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-195">Negative</span></span>                       | <span data-ttu-id="a2b5d-196">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-196">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-197">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="a2b5d-198">Määritä arvonlisäveron summa ja tositteessa oleva tili</span><span class="sxs-lookup"><span data-stu-id="a2b5d-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="a2b5d-199">Kun kirjaat arvonlisäveroja, päätili haetaan kirjanpidon kirjausryhmän profiilista.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="a2b5d-200">Kun arvonlisäverot ovat saatavia, järjestelmä käyttää profiilissa määritettyä Saatava arvonlisävero -tiliä.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="a2b5d-201">Kun arvonlisäverot ovat maksettavia, järjestelmä käyttää profiilissa määritettyä Maksettava arvonlisävero -tiliä.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="a2b5d-202">Seuraavassa taulukossa kuvataan yleinen sääntö.</span><span class="sxs-lookup"><span data-stu-id="a2b5d-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="a2b5d-203">Arvonlisäveron suunta</span><span class="sxs-lookup"><span data-stu-id="a2b5d-203">Sales tax direction</span></span>  | <span data-ttu-id="a2b5d-204">Arvonlisäveron summan etumerkki</span><span class="sxs-lookup"><span data-stu-id="a2b5d-204">Sales tax amount sign</span></span> | <span data-ttu-id="a2b5d-205">Arvonlisäverotili</span><span class="sxs-lookup"><span data-stu-id="a2b5d-205">Sales tax account</span></span>      | <span data-ttu-id="a2b5d-206">Tositteen summa</span><span class="sxs-lookup"><span data-stu-id="a2b5d-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="a2b5d-207">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-207">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-208">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-208">Positive</span></span>              | <span data-ttu-id="a2b5d-209">Saatava vero -tili</span><span class="sxs-lookup"><span data-stu-id="a2b5d-209">Tax Receivable Account</span></span> | <span data-ttu-id="a2b5d-210">Positiivinen (debet)</span><span class="sxs-lookup"><span data-stu-id="a2b5d-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="a2b5d-211">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-211">Sales Tax Receivable</span></span> | <span data-ttu-id="a2b5d-212">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-212">Negative</span></span>              | <span data-ttu-id="a2b5d-213">Saatava vero -tili</span><span class="sxs-lookup"><span data-stu-id="a2b5d-213">Tax Receivable Account</span></span> | <span data-ttu-id="a2b5d-214">Negatiivinen (kredit)</span><span class="sxs-lookup"><span data-stu-id="a2b5d-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="a2b5d-215">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-215">Sales Tax Payable</span></span>    | <span data-ttu-id="a2b5d-216">Positiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-216">Positive</span></span>              | <span data-ttu-id="a2b5d-217">Maksettava vero -tili</span><span class="sxs-lookup"><span data-stu-id="a2b5d-217">Tax Payable Account</span></span>    | <span data-ttu-id="a2b5d-218">Negatiivinen (kredit)</span><span class="sxs-lookup"><span data-stu-id="a2b5d-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="a2b5d-219">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a2b5d-219">Sales Tax Payable</span></span>    | <span data-ttu-id="a2b5d-220">Negatiivinen</span><span class="sxs-lookup"><span data-stu-id="a2b5d-220">Negative</span></span>              | <span data-ttu-id="a2b5d-221">Maksettava vero -tili</span><span class="sxs-lookup"><span data-stu-id="a2b5d-221">Tax Payable Account</span></span>    | <span data-ttu-id="a2b5d-222">Positiivinen (debet)</span><span class="sxs-lookup"><span data-stu-id="a2b5d-222">Positive (Debit)</span></span>  |
