--- 
title: "Määritä hankintaluokkahierarkia"
description: "Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="2f9ae-103">Määritä hankintaluokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="2f9ae-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f9ae-104">Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="2f9ae-105">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="2f9ae-106">Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="2f9ae-107">Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="2f9ae-108">Lisää uusi hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="2f9ae-108">Add a new procurement category</span></span>
1. <span data-ttu-id="2f9ae-109">Valitse Hankinta > Hankintaluokat.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="2f9ae-110">Valitse Muokkaa luokkahierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="2f9ae-111">Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="2f9ae-112">Olet muokkaamassa hierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="2f9ae-113">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-113">Click New category node.</span></span>
    * <span data-ttu-id="2f9ae-114">Järjestelmä valitsee oletusarvoisesti ylimmän solmun.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-114">The system selects the top node by default.</span></span> <span data-ttu-id="2f9ae-115">Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="2f9ae-116">Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="2f9ae-117">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2f9ae-118">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2f9ae-119">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="2f9ae-120">Kutsumanimi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-120">The friendly name is optional.</span></span> <span data-ttu-id="2f9ae-121">Se näkyy luokkahauissa yhdessä luokan nimen kanssa.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="2f9ae-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="2f9ae-123">Lisää tuotteita uuteen hankintaluokkaan</span><span class="sxs-lookup"><span data-stu-id="2f9ae-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="2f9ae-124">Valitse Hankinta > Hankintaluokat.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="2f9ae-125">Valitse juuri lisäämäsi solmu.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-125">Select the node you just added.</span></span> <span data-ttu-id="2f9ae-126">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="2f9ae-127">Ota Tuotteet-osion laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="2f9ae-128">Liitä tuotteet hankintaluokkaan valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="2f9ae-129">Valitse hankintaluokkaan lisättävä tuote.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="2f9ae-130">Valitse tuote napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="2f9ae-131">Valitse toinen hankintaluokkaan lisättävä tuote.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="2f9ae-132">Valitse tuote napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="2f9ae-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="2f9ae-134">Lisää hyväksyttyjä tai ensisijaisia toimittajia</span><span class="sxs-lookup"><span data-stu-id="2f9ae-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="2f9ae-135">Ota käyttöön Toimittajat-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="2f9ae-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-136">Click Add.</span></span>
    * <span data-ttu-id="2f9ae-137">Voit lisätä toimittajan hankintaluokkaan ja määrittää, onko toimittaja luokassaan ensisijainen vai luokkaan vain hyväksytty toimittaja.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="2f9ae-138">Kun poistat toimittajan luokasta, toimittajan ja luokan aiempia tapahtumia ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="2f9ae-139">Etsi hankintaluokkaan lisättävä toimittaja.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="2f9ae-140">Valitse toimittaja napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="2f9ae-141">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-141">Click OK.</span></span>
6. <span data-ttu-id="2f9ae-142">Valitse sen toimittajan rivi, jonka tietoja haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="2f9ae-143">Valitse vaihtoehto Toimittajan tila -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="2f9ae-144">Luokan käytäntösäännöissä oleva toimittajan valinta-asetus määrittää, onko ostoehdotuksissa valittavissa ensisijaiset, hyväksytyt vai kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="2f9ae-145">Lisää lisätiedot luokkaan</span><span class="sxs-lookup"><span data-stu-id="2f9ae-145">Add additional information to the category</span></span>
1. <span data-ttu-id="2f9ae-146">Ota Toimittajan arviointiehtoryhmät -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="2f9ae-147">Voit määrittää tässä välilehdessä ehdot, joilla hankintaluokan toimittajat luokitellaan.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="2f9ae-148">Voit tehdä sen valitsemalla ensin Lisää ja valitse sitten sen toimittaja-arviointiryhmän, jonka ehtoja haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="2f9ae-149">Ota Kyselylomakkeet-osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="2f9ae-150">Voit lisätä tässä välilehdessä varasto-ottoehdotuksessa näkyviä kyselylomakkeita, kunhan tehtävän tyypiksi on valittu Varasto-ottoehdotus.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="2f9ae-151">Pyynnön lähettäjän on sitten täytettävä kyselylomake, ennen kuin he voivat lähettää tietyn tuotteen tai hankintaluokan tuotteiden varasto-ottoehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="2f9ae-152">Ota Nimikkeiden arvonlisäveroryhmät -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="2f9ae-153">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä: -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2f9ae-154">Valitse arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="2f9ae-155">Ota Luokkasivu--osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="2f9ae-156">Luokkasivut luodaan Luokkahierarkia-sivulla.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="2f9ae-157">Niissä on esimerkiksi seuraavia tietoja hankintaluokista: tiedot luokan tuotetyypeistä, luokan tuotteiden kuvat ja ilmoitukset, kuten luokassa käytettävissä olevat alennukset.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="2f9ae-158">Luokkasivulla olevat tiedot näytetään ostoehdotuksissa.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="2f9ae-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2f9ae-159">Close the page.</span></span>


