---
title: Luo vapautettu tuote yhdessä yrityksessä
description: Tässä menettelyssä kerrotaan, miten yksittäinen vapautettu tuote luodaan yksittäisessä yrityksessä.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90924c853793a3d70f2f2d46d8a154a19bd7d6bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427066"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="57ced-103">Luo vapautettu tuote yhdessä yrityksessä</span><span class="sxs-lookup"><span data-stu-id="57ced-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57ced-104">Tässä menettelyssä kerrotaan, miten yksittäinen vapautettu tuote luodaan yksittäisessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="57ced-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="57ced-105">Kun vapautettu tuote on luotu, se on heti käytettävissä vain tässä yksikössä.</span><span class="sxs-lookup"><span data-stu-id="57ced-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="57ced-106">Voit suorittaa tämän menettelyn esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="57ced-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="57ced-107">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="57ced-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="57ced-108">Vapautetun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="57ced-108">Create a released product</span></span>
1. <span data-ttu-id="57ced-109">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="57ced-109">Go to Released products.</span></span>
2. <span data-ttu-id="57ced-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="57ced-110">Click New.</span></span>
3. <span data-ttu-id="57ced-111">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="57ced-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="57ced-112">Jos tuotenumeroa ei automaattisesti syötetä Tuotenumero-kenttään, kirjoita yksilöivä tuotenumero.</span><span class="sxs-lookup"><span data-stu-id="57ced-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="57ced-113">Tämä vaihe vaaditaan vain, jos tuotenumeroille ei ole määritetty numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="57ced-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="57ced-114">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="57ced-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="57ced-115">Tuotenimen oletusarvoksi määritetään hakunimi.</span><span class="sxs-lookup"><span data-stu-id="57ced-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="57ced-116">Tarvittaessa voit muuttaa hakunimen.</span><span class="sxs-lookup"><span data-stu-id="57ced-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="57ced-117">Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-118">Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa.</span><span class="sxs-lookup"><span data-stu-id="57ced-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="57ced-119">Asetukset myös määrittävät, miten nimikkeiden kulutus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="57ced-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="57ced-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="57ced-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="57ced-122">Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-123">Käyttämällä nimikeryhmiä voidaan varastoa hallita jakamalla varastonimikkeet ryhmiin nimikkeiden ominaisuuksien mukaan.</span><span class="sxs-lookup"><span data-stu-id="57ced-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="57ced-124">Voit esimerkiksi hallinnoida sitä, miten tiedot kirjataan päätileille, luomalla erilaisia tiettyihin päätileihin liittyviä nimikeryhmiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="57ced-125">Tämä mahdollistaa nimikkeiden varastoarvon seuraamisen eri vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="57ced-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="57ced-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="57ced-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="57ced-128">Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-129">Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä.</span><span class="sxs-lookup"><span data-stu-id="57ced-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="57ced-130">Varastodimensio voi olla esimerkiksi toimipiste ja varasto.</span><span class="sxs-lookup"><span data-stu-id="57ced-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="57ced-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="57ced-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="57ced-133">Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-134">Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää.</span><span class="sxs-lookup"><span data-stu-id="57ced-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="57ced-135">Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.</span><span class="sxs-lookup"><span data-stu-id="57ced-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="57ced-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="57ced-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="57ced-138">Avaa haku valitsemalla Varastoyksikkö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-139">Varastoyksikkö määrittää, kuinka tuote mitataan, kun se varastoidaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="57ced-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="57ced-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="57ced-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="57ced-142">Avaa haku valitsemalla Ostoyksikkö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-143">Ostoyksikkö määrittää, kuinka tuote mitataan, kun se on ostettu toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="57ced-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="57ced-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="57ced-145">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="57ced-146">Avaa haku valitsemalla Myyntiyksikkö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-147">Myyntiyksikkö määrittää, kuinka tuote mitataan, kun se myydään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="57ced-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="57ced-148">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="57ced-149">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="57ced-150">Avaa haku valitsemalla Tuoterakenteen yksikkö -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-151">Tuoterakenneyksikkö määrittää, kuinka tuote mitataan, kun se sisällytetään tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="57ced-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="57ced-152">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="57ced-153">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="57ced-154">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-155">Nimikkeen arvonlisäveroryhmä Myynnin verotus -ryhmässä määrittää, miten arvonlisävero lasketaan kullekin nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="57ced-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="57ced-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="57ced-157">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="57ced-158">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="57ced-159">Nimikkeen arvonlisäveroryhmä Ostojen verotus -ryhmässä määrittää, miten oston vero lasketaan kullekin nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="57ced-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="57ced-160">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="57ced-161">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="57ced-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="57ced-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="57ced-163">Tuotteen fyysisten ominaisuuksien lisääminen</span><span class="sxs-lookup"><span data-stu-id="57ced-163">Add product characteristics</span></span>
1. <span data-ttu-id="57ced-164">Laajenna tai tiivistä Varastonhallinta-osa.</span><span class="sxs-lookup"><span data-stu-id="57ced-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="57ced-165">Syötä Nettopaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="57ced-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="57ced-166">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="57ced-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="57ced-167">Syötä Bruttosyvyys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="57ced-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="57ced-168">Syötä Bruttoleveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="57ced-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="57ced-169">Syötä Bruttokorkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="57ced-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="57ced-170">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="57ced-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="57ced-171">Taloushallinnon dimensioiden lisääminen</span><span class="sxs-lookup"><span data-stu-id="57ced-171">Add financial dimensions</span></span>
1. <span data-ttu-id="57ced-172">Laajenna tai tiivistä Taloushallinnon dimensiot -osa.</span><span class="sxs-lookup"><span data-stu-id="57ced-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="57ced-173">Avaa haku valitsemalla BusinessUnit-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="57ced-174">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="57ced-175">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="57ced-176">Avaa haku valitsemalla CostCenter-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="57ced-177">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="57ced-178">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="57ced-179">Avaa haku valitsemalla Osasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="57ced-180">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="57ced-181">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="57ced-182">Avaa haku valitsemalla ItemGroup-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="57ced-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="57ced-183">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="57ced-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="57ced-184">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="57ced-184">In the list, click the link in the selected row.</span></span>

