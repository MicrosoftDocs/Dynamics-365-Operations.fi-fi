---
title: Luo useita myyntitarjouksia
description: Tässä menettelyssä käsitellään, miten luodaan tehokkaasti tarjouksia, jotka sisältävät useita monille asiakkaille lähetettäviä tuotteita tai palveluja.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77f7a2df813eb0bf211b72646c1e99306fdf3f88
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148604"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="24dbc-103">Luo useita myyntitarjouksia</span><span class="sxs-lookup"><span data-stu-id="24dbc-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24dbc-104">Tässä menettelyssä käsitellään, miten luodaan tehokkaasti tarjouksia, jotka sisältävät useita monille asiakkaille lähetettäviä tuotteita tai palveluja.</span><span class="sxs-lookup"><span data-stu-id="24dbc-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="24dbc-105">Tämä joukkotarjouksen luonti perustuu tarjousmalleihin.</span><span class="sxs-lookup"><span data-stu-id="24dbc-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="24dbc-106">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="24dbc-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="24dbc-107">Luo tarjousmalli</span><span class="sxs-lookup"><span data-stu-id="24dbc-107">Create a quotation template</span></span>
1. <span data-ttu-id="24dbc-108">Valitse Myynti ja markkinointi > Asetukset > Tarjoukset > Malliryhmät.</span><span class="sxs-lookup"><span data-stu-id="24dbc-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="24dbc-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="24dbc-109">Click New.</span></span>
3. <span data-ttu-id="24dbc-110">Kirjoita Ryhmän tunnus -kenttään haluamasi tunnus.</span><span class="sxs-lookup"><span data-stu-id="24dbc-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="24dbc-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="24dbc-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="24dbc-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="24dbc-112">Click Save.</span></span>
6. <span data-ttu-id="24dbc-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24dbc-113">Close the page.</span></span>
7. <span data-ttu-id="24dbc-114">Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.</span><span class="sxs-lookup"><span data-stu-id="24dbc-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="24dbc-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="24dbc-115">Click New.</span></span>
9. <span data-ttu-id="24dbc-116">Valitse Tilityyppi-kentässä Asiakas.</span><span class="sxs-lookup"><span data-stu-id="24dbc-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="24dbc-117">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="24dbc-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="24dbc-118">Click OK.</span></span>
    * <span data-ttu-id="24dbc-119">Jotta tarjouksesta tulisi malli, sinun on suoritettava tarjouksen otsikon määritysvaiheet.</span><span class="sxs-lookup"><span data-stu-id="24dbc-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="24dbc-120">Se on tehtävä ennen rivien lisäämistä tarjoukseen.</span><span class="sxs-lookup"><span data-stu-id="24dbc-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="24dbc-121">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="24dbc-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="24dbc-122">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-122">Click Change view.</span></span>
14. <span data-ttu-id="24dbc-123">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-123">Click Header view.</span></span>
15. <span data-ttu-id="24dbc-124">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="24dbc-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="24dbc-125">anna tai valitse Ryhmän tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="24dbc-126">Syötä Mallin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="24dbc-127">Valitse Aktiivinen-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="24dbc-128">Kun uuteen myyntitarjoukseen käytetään malleja, vain aktiivisia malleja voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="24dbc-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="24dbc-129">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="24dbc-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="24dbc-130">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-130">Click Change view.</span></span>
21. <span data-ttu-id="24dbc-131">Valitse Rivinäkymä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-131">Click Line view.</span></span>
22. <span data-ttu-id="24dbc-132">Anna tai valitse Nimike-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="24dbc-133">Kirjoita Nimike-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="24dbc-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24dbc-134">Close the page.</span></span>
25. <span data-ttu-id="24dbc-135">Lisää Alennusprosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="24dbc-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="24dbc-136">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="24dbc-136">Click Add line.</span></span>
27. <span data-ttu-id="24dbc-137">Anna tai valitse Nimike-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="24dbc-138">Kirjoita Nimike-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="24dbc-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24dbc-139">Close the page.</span></span>
30. <span data-ttu-id="24dbc-140">Anna Yksikköhinta-kentässä uusi hinta tai vaihda nykyistä hintaa.</span><span class="sxs-lookup"><span data-stu-id="24dbc-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="24dbc-141">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="24dbc-141">Click Add line.</span></span>
32. <span data-ttu-id="24dbc-142">Anna tai valitse Nimike-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="24dbc-143">Kirjoita Nimike-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="24dbc-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24dbc-144">Close the page.</span></span>
35. <span data-ttu-id="24dbc-145">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="24dbc-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="24dbc-146">Lisää Alennus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="24dbc-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="24dbc-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="24dbc-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="24dbc-148">Luo mallilla yksittäinen tarjous</span><span class="sxs-lookup"><span data-stu-id="24dbc-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="24dbc-149">Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.</span><span class="sxs-lookup"><span data-stu-id="24dbc-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="24dbc-150">Huomaa, että juuri luomasi tarjous on merkitty malliksi.</span><span class="sxs-lookup"><span data-stu-id="24dbc-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="24dbc-151">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="24dbc-151">Click New.</span></span>
3. <span data-ttu-id="24dbc-152">Valitse Tilityyppi-kentässä Asiakas.</span><span class="sxs-lookup"><span data-stu-id="24dbc-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="24dbc-153">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="24dbc-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="24dbc-154">Laajenna Malli-osa.</span><span class="sxs-lookup"><span data-stu-id="24dbc-154">Expand the Template section.</span></span>
6. <span data-ttu-id="24dbc-155">anna tai valitse Ryhmän tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="24dbc-156">Anna tai valitse Mallin nimi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="24dbc-157">Valitse Laskentatapa-kentässä Mallin arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="24dbc-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="24dbc-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="24dbc-158">Click OK.</span></span>
    * <span data-ttu-id="24dbc-159">Uusi tarjous on nyt luotu mallin tietojen ja ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="24dbc-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="24dbc-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24dbc-160">Close the page.</span></span>
11. <span data-ttu-id="24dbc-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24dbc-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="24dbc-162">Luo mallilla useita tarjouksia</span><span class="sxs-lookup"><span data-stu-id="24dbc-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="24dbc-163">Valitse Myynti ja markkinointi > Myyntitarjoukset > Tarjouksen päivittäminen > Luo useita tarjouksia.</span><span class="sxs-lookup"><span data-stu-id="24dbc-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="24dbc-164">Valitse Tilityyppi-kentässä Asiakas.</span><span class="sxs-lookup"><span data-stu-id="24dbc-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="24dbc-165">anna tai valitse Ryhmän tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="24dbc-166">Anna tai valitse Mallin nimi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="24dbc-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="24dbc-167">Valitse Laskentatapa-kentässä Mallin arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="24dbc-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="24dbc-168">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="24dbc-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="24dbc-169">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="24dbc-169">Click Filter.</span></span>
8. <span data-ttu-id="24dbc-170">Määritä Ehdot-kentässä suodatin kattamaan ne asiakkaat, jotka haluat sisällyttää tähän useiden tarjousten luontiin.</span><span class="sxs-lookup"><span data-stu-id="24dbc-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="24dbc-171">Käytä muotoa Asiakas1...AsiakasN.</span><span class="sxs-lookup"><span data-stu-id="24dbc-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="24dbc-172">Voit esimerkiksi määrittää suodattimeksi US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="24dbc-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="24dbc-173">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="24dbc-173">Click OK.</span></span>
10. <span data-ttu-id="24dbc-174">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="24dbc-174">Click OK.</span></span>
11. <span data-ttu-id="24dbc-175">Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.</span><span class="sxs-lookup"><span data-stu-id="24dbc-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="24dbc-176">Varmista, että tarjoukset on luotu valitun mallin perusteella kaikille joukkopäivitysrutiinissa määritetyille asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="24dbc-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

