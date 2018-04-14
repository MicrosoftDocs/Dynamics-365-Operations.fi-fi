--- 
title: "Luo vapautettu tuote yhdessä yrityksessä"
description: "Tässä menettelyssä kerrotaan, miten yksittäinen vapautettu tuote luodaan yksittäisessä yrityksessä."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ced48377f8f6cfdf416bcaf5e2b5e6473998ea91
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="35a93-103">Luo vapautettu tuote yhdessä yrityksessä</span><span class="sxs-lookup"><span data-stu-id="35a93-103">Create a released product for a single company</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35a93-104">Tässä menettelyssä kerrotaan, miten yksittäinen vapautettu tuote luodaan yksittäisessä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="35a93-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="35a93-105">Kun vapautettu tuote on luotu, se on heti käytettävissä vain tässä yksikössä.</span><span class="sxs-lookup"><span data-stu-id="35a93-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="35a93-106">Voit suorittaa tämän menettelyn esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="35a93-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="35a93-107">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="35a93-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="35a93-108">Vapautetun tuotteen luominen</span><span class="sxs-lookup"><span data-stu-id="35a93-108">Create a released product</span></span>
1. <span data-ttu-id="35a93-109">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="35a93-109">Go to Released products.</span></span>
2. <span data-ttu-id="35a93-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="35a93-110">Click New.</span></span>
3. <span data-ttu-id="35a93-111">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a93-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="35a93-112">Jos tuotenumeroa ei automaattisesti syötetä Tuotenumero-kenttään, kirjoita yksilöivä tuotenumero.</span><span class="sxs-lookup"><span data-stu-id="35a93-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="35a93-113">Tämä vaihe vaaditaan vain, jos tuotenumeroille ei ole määritetty numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="35a93-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="35a93-114">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="35a93-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="35a93-115">Tuotenimen oletusarvoksi määritetään hakunimi.</span><span class="sxs-lookup"><span data-stu-id="35a93-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="35a93-116">Tarvittaessa voit muuttaa hakunimen.</span><span class="sxs-lookup"><span data-stu-id="35a93-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="35a93-117">Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-118">Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa.</span><span class="sxs-lookup"><span data-stu-id="35a93-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="35a93-119">Asetukset myös määrittävät, miten nimikkeiden kulutus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="35a93-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="35a93-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="35a93-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="35a93-122">Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-123">Käyttämällä nimikeryhmiä voidaan varastoa hallita jakamalla varastonimikkeet ryhmiin nimikkeiden ominaisuuksien mukaan.</span><span class="sxs-lookup"><span data-stu-id="35a93-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="35a93-124">Voit esimerkiksi hallinnoida sitä, miten tiedot kirjataan päätileille, luomalla erilaisia tiettyihin päätileihin liittyviä nimikeryhmiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="35a93-125">Tämä mahdollistaa nimikkeiden varastoarvon seuraamisen eri vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="35a93-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="35a93-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="35a93-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="35a93-128">Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-129">Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä.</span><span class="sxs-lookup"><span data-stu-id="35a93-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="35a93-130">Varastodimensio voi olla esimerkiksi toimipiste ja varasto.</span><span class="sxs-lookup"><span data-stu-id="35a93-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="35a93-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="35a93-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="35a93-133">Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-134">Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää.</span><span class="sxs-lookup"><span data-stu-id="35a93-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="35a93-135">Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.</span><span class="sxs-lookup"><span data-stu-id="35a93-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="35a93-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="35a93-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="35a93-138">Avaa haku valitsemalla Varastoyksikkö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-139">Varastoyksikkö määrittää, kuinka tuote mitataan, kun se varastoidaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="35a93-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="35a93-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="35a93-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="35a93-142">Avaa haku valitsemalla Ostoyksikkö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-143">Ostoyksikkö määrittää, kuinka tuote mitataan, kun se on ostettu toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="35a93-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="35a93-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="35a93-145">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="35a93-146">Avaa haku valitsemalla Myyntiyksikkö-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-147">Myyntiyksikkö määrittää, kuinka tuote mitataan, kun se myydään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="35a93-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="35a93-148">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="35a93-149">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="35a93-150">Avaa haku valitsemalla Tuoterakenteen yksikkö -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-151">Tuoterakenneyksikkö määrittää, kuinka tuote mitataan, kun se sisällytetään tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="35a93-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="35a93-152">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="35a93-153">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="35a93-154">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-155">Nimikkeen arvonlisäveroryhmä Myynnin verotus -ryhmässä määrittää, miten arvonlisävero lasketaan kullekin nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="35a93-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="35a93-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="35a93-157">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="35a93-158">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35a93-159">Nimikkeen arvonlisäveroryhmä Ostojen verotus -ryhmässä määrittää, miten oston vero lasketaan kullekin nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="35a93-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="35a93-160">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="35a93-161">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="35a93-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="35a93-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="35a93-163">Tuotteen fyysisten ominaisuuksien lisääminen</span><span class="sxs-lookup"><span data-stu-id="35a93-163">Add product characteristics</span></span>
1. <span data-ttu-id="35a93-164">Laajenna tai tiivistä Varastonhallinta-osa.</span><span class="sxs-lookup"><span data-stu-id="35a93-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="35a93-165">Syötä Nettopaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35a93-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="35a93-166">Syötä Taarapaino-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35a93-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="35a93-167">Syötä Bruttosyvyys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35a93-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="35a93-168">Syötä Bruttoleveys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35a93-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="35a93-169">Syötä Bruttokorkeus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35a93-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="35a93-170">Syötä Tilavuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35a93-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="35a93-171">Taloushallinnon dimensioiden lisääminen</span><span class="sxs-lookup"><span data-stu-id="35a93-171">Add financial dimensions</span></span>
1. <span data-ttu-id="35a93-172">Laajenna tai tiivistä Taloushallinnon dimensiot -osa.</span><span class="sxs-lookup"><span data-stu-id="35a93-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="35a93-173">Avaa haku valitsemalla BusinessUnit-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="35a93-174">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="35a93-175">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="35a93-176">Avaa haku valitsemalla CostCenter-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="35a93-177">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="35a93-178">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="35a93-179">Avaa haku valitsemalla Osasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="35a93-180">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="35a93-181">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="35a93-182">Avaa haku valitsemalla ItemGroup-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="35a93-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="35a93-183">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35a93-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="35a93-184">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35a93-184">In the list, click the link in the selected row.</span></span>


