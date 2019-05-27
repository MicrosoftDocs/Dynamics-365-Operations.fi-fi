---
title: Poikkeusten tutkiminen ja selvittäminen
description: Toimittajan laskukäytännöt suoritetaan, kun toimittajan lasku kirjataan Toimittajan lasku -sivun avulla ja kun Toimittajan laskukäytäntöjen rikkeet -sivu avataan.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c6f8c8dcf7a301c7fb2d095658ac96cd4a24dff
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567005"
---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="f3e22-103">Poikkeusten tutkiminen ja selvittäminen</span><span class="sxs-lookup"><span data-stu-id="f3e22-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3e22-104">Toimittajan laskukäytännöt suoritetaan, kun toimittajan lasku kirjataan Toimittajan lasku -sivun avulla ja kun Toimittajan laskukäytäntöjen rikkeet -sivu avataan.</span><span class="sxs-lookup"><span data-stu-id="f3e22-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="f3e22-105">Voit myös määrittää toimittajan laskun työnkulun, kun haluat suorittaa toimittajan laskukäytännöt aina, kun lasku lähetetään työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="f3e22-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="f3e22-106">Toimittajan laskukäytännöt eivät koske laskurekisteriin tai laskukirjauskansioon luotuja laskuja.</span><span class="sxs-lookup"><span data-stu-id="f3e22-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="f3e22-107">Laskun täsmäytyksen vahvistuksessa ei käytetä toimittajan laskukäytäntöjä, vaan Ostoreskontran parametrit -määritettyjä käytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="f3e22-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="f3e22-108">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="f3e22-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="f3e22-109">Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.</span><span class="sxs-lookup"><span data-stu-id="f3e22-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="f3e22-110">Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.</span><span class="sxs-lookup"><span data-stu-id="f3e22-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="f3e22-111">Toimittajan laskujen käytäntöjen luomisen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="f3e22-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="f3e22-112">Siirry kohtaan Ostoreskontra > Asetukset > Ostoreskontran parametrit.</span><span class="sxs-lookup"><span data-stu-id="f3e22-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="f3e22-113">Valitse Laskun oikeellisuustarkistus -välilehti.</span><span class="sxs-lookup"><span data-stu-id="f3e22-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="f3e22-114">Valitse Päivitetäänkö laskun otsikon tila automaattisesti -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="f3e22-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="f3e22-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f3e22-115">Click OK.</span></span>
5. <span data-ttu-id="f3e22-116">Valitse Kirjaa lasku, jossa on ristiriitoja -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f3e22-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="f3e22-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f3e22-117">Close the page.</span></span>
7. <span data-ttu-id="f3e22-118">Siirry kohtaan Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt.</span><span class="sxs-lookup"><span data-stu-id="f3e22-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="f3e22-119">Valitse Parametrit.</span><span class="sxs-lookup"><span data-stu-id="f3e22-119">Click Parameters.</span></span>
9. <span data-ttu-id="f3e22-120">Valitse btnAdd.</span><span class="sxs-lookup"><span data-stu-id="f3e22-120">Click btnAdd.</span></span>
10. <span data-ttu-id="f3e22-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f3e22-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="f3e22-122">Toimittajan laskujen käytäntösääntöjen tyyppien luominen</span><span class="sxs-lookup"><span data-stu-id="f3e22-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="f3e22-123">Siirry kohtaan Ostoreskontra > Käytännön asetukset > Toimittajan laskutuskäytännön sääntötyypit.</span><span class="sxs-lookup"><span data-stu-id="f3e22-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="f3e22-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f3e22-124">Click New.</span></span>
3. <span data-ttu-id="f3e22-125">Kirjoita arvo Säännön nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3e22-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="f3e22-126">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3e22-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3e22-127">Avaa haku valitsemalla Kyselyn nimi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f3e22-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f3e22-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f3e22-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f3e22-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f3e22-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f3e22-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f3e22-130">Click Save.</span></span>
9. <span data-ttu-id="f3e22-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f3e22-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="f3e22-132">Toimittajan laskujen käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f3e22-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="f3e22-133">Siirry kohtaan Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt.</span><span class="sxs-lookup"><span data-stu-id="f3e22-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="f3e22-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f3e22-134">Click New.</span></span>
3. <span data-ttu-id="f3e22-135">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3e22-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f3e22-136">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3e22-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3e22-137">Laajenna tai tiivistä Käytännön organisaatiot -osa.</span><span class="sxs-lookup"><span data-stu-id="f3e22-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="f3e22-138">Valitse puussa solmu Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="f3e22-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="f3e22-139">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f3e22-139">Click Add.</span></span>
8. <span data-ttu-id="f3e22-140">Laajenna tai tiivistä Käytäntösäännöt-osa.</span><span class="sxs-lookup"><span data-stu-id="f3e22-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="f3e22-141">Valitse Luo käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="f3e22-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="f3e22-142">Kirjoita Käytäntösääntö-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f3e22-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="f3e22-143">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="f3e22-143">Click Filter.</span></span>
12. <span data-ttu-id="f3e22-144">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f3e22-144">Click Add.</span></span>
13. <span data-ttu-id="f3e22-145">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f3e22-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f3e22-146">Avaa haku valitsemalla Taulu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f3e22-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f3e22-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f3e22-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f3e22-148">Avaa haku valitsemalla Johdettu taulu -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f3e22-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="f3e22-149">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f3e22-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f3e22-150">Avaa haku valitsemalla Kenttä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f3e22-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="f3e22-151">Kirjoita arvo Kenttä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3e22-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="f3e22-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f3e22-152">Close the page.</span></span>
21. <span data-ttu-id="f3e22-153">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3e22-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="f3e22-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f3e22-154">Click OK.</span></span>
23. <span data-ttu-id="f3e22-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f3e22-155">Click OK.</span></span>
24. <span data-ttu-id="f3e22-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f3e22-156">Close the page.</span></span>
25. <span data-ttu-id="f3e22-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f3e22-157">Close the page.</span></span>

