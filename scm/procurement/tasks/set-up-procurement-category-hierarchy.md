--- 
title: "Määritä hankintaluokkahierarkia"
description: "Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään."
author: mkirknel
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
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="6819e-103">Määritä hankintaluokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="6819e-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6819e-104">Tässä menettelyssä selvitetään, miten voit luoda uusia solmuja hankintaluokkahierarkiaan ja miten hankintaprosessissa käytettävä hankintaluokka määritetään.</span><span class="sxs-lookup"><span data-stu-id="6819e-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="6819e-105">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="6819e-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="6819e-106">Ennen menettelyn aloittamista on oltava Hankita-tyyppinen luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="6819e-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="6819e-107">Jos käytössä on demotietoyritys, voit suorittaa tämän menettelyn USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6819e-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="6819e-108">Lisää uusi hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="6819e-108">Add a new procurement category</span></span>
1. <span data-ttu-id="6819e-109">Valitse Hankinta > ..</span><span class="sxs-lookup"><span data-stu-id="6819e-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="6819e-110">> Hankintaluokat.</span><span class="sxs-lookup"><span data-stu-id="6819e-110">> Procurement categories.</span></span>
2. <span data-ttu-id="6819e-111">Valitse Muokkaa luokkahierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="6819e-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="6819e-112">Nykyisen hankintaluokkahierarkia näkyy sivun vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="6819e-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="6819e-113">Olet muokkaamassa hierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="6819e-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="6819e-114">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="6819e-114">Click New category node.</span></span>
    * <span data-ttu-id="6819e-115">Järjestelmä valitsee oletusarvoisesti ylimmän solmun.</span><span class="sxs-lookup"><span data-stu-id="6819e-115">The system selects the top node by default.</span></span> <span data-ttu-id="6819e-116">Jos käytät menettelyä tehtävän ohjauksena, voit napsauttaa Poista lukitus -painiketta ja valita toisen pääsolmun, johon voit lisätä uuden solmun.</span><span class="sxs-lookup"><span data-stu-id="6819e-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="6819e-117">Kun tämä on tehty, lukitse tehtäväopas uudelleen ja napsauta Uusi luokka -solmua.</span><span class="sxs-lookup"><span data-stu-id="6819e-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="6819e-118">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6819e-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6819e-119">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6819e-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="6819e-120">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6819e-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="6819e-121">Kutsumanimi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="6819e-121">The friendly name is optional.</span></span> <span data-ttu-id="6819e-122">Se näkyy luokkahauissa yhdessä luokan nimen kanssa.</span><span class="sxs-lookup"><span data-stu-id="6819e-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="6819e-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6819e-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="6819e-124">Lisää tuotteita uuteen hankintaluokkaan</span><span class="sxs-lookup"><span data-stu-id="6819e-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="6819e-125">Valitse Hankinta > ..</span><span class="sxs-lookup"><span data-stu-id="6819e-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="6819e-126">> Hankintaluokat.</span><span class="sxs-lookup"><span data-stu-id="6819e-126">> Procurement categories.</span></span>
    * <span data-ttu-id="6819e-127">Valitse juuri lisäämäsi solmu.</span><span class="sxs-lookup"><span data-stu-id="6819e-127">Select the node you just added.</span></span> <span data-ttu-id="6819e-128">Jos käytät menettelyä tehtävän ohjauksena, sinun on ehkä poistettava lukitus, ennen kuin voit valita solmun.</span><span class="sxs-lookup"><span data-stu-id="6819e-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="6819e-129">Ota Tuotteet-osion laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6819e-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="6819e-130">Liitä tuotteet hankintaluokkaan valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="6819e-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="6819e-131">Valitse hankintaluokkaan lisättävä tuote.</span><span class="sxs-lookup"><span data-stu-id="6819e-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="6819e-132">Valitse tuote napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="6819e-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="6819e-133">Valitse toinen hankintaluokkaan lisättävä tuote.</span><span class="sxs-lookup"><span data-stu-id="6819e-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="6819e-134">Valitse tuote napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="6819e-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="6819e-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6819e-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="6819e-136">Lisää hyväksyttyjä tai ensisijaisia toimittajia</span><span class="sxs-lookup"><span data-stu-id="6819e-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="6819e-137">Ota käyttöön Toimittajat-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="6819e-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="6819e-138">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="6819e-138">Click Add.</span></span>
    * <span data-ttu-id="6819e-139">Voit lisätä toimittajan hankintaluokkaan ja määrittää, onko toimittaja luokassaan ensisijainen vai luokkaan vain hyväksytty toimittaja.</span><span class="sxs-lookup"><span data-stu-id="6819e-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="6819e-140">Kun poistat toimittajan luokasta, toimittajan ja luokan aiempia tapahtumia ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="6819e-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="6819e-141">Etsi hankintaluokkaan lisättävä toimittaja.</span><span class="sxs-lookup"><span data-stu-id="6819e-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="6819e-142">Valitse toimittaja napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="6819e-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="6819e-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6819e-143">Click OK.</span></span>
6. <span data-ttu-id="6819e-144">Valitse sen toimittajan rivi, jonka tietoja haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="6819e-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="6819e-145">Valitse vaihtoehto Toimittajan tila -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6819e-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="6819e-146">Luokan käytäntösäännöissä oleva toimittajan valinta-asetus määrittää, onko ostoehdotuksissa valittavissa ensisijaiset, hyväksytyt vai kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="6819e-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="6819e-147">Lisää lisätiedot luokkaan</span><span class="sxs-lookup"><span data-stu-id="6819e-147">Add additional information to the category</span></span>
1. <span data-ttu-id="6819e-148">Ota Toimittajan arviointiehtoryhmät -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6819e-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="6819e-149">Voit määrittää tässä välilehdessä ehdot, joilla hankintaluokan toimittajat luokitellaan.</span><span class="sxs-lookup"><span data-stu-id="6819e-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="6819e-150">Voit tehdä sen valitsemalla ensin Lisää ja valitse sitten sen toimittaja-arviointiryhmän, jonka ehtoja haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="6819e-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="6819e-151">Ota Kyselylomakkeet-osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6819e-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="6819e-152">Voit lisätä tässä välilehdessä varasto-ottoehdotuksessa näkyviä kyselylomakkeita, kunhan tehtävän tyypiksi on valittu Varasto-ottoehdotus.</span><span class="sxs-lookup"><span data-stu-id="6819e-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="6819e-153">Pyynnön lähettäjän on sitten täytettävä kyselylomake, ennen kuin he voivat lähettää tietyn tuotteen tai hankintaluokan tuotteiden varasto-ottoehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="6819e-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="6819e-154">Ota Nimikkeiden arvonlisäveroryhmät -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6819e-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="6819e-155">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä: -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6819e-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6819e-156">Valitse arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="6819e-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="6819e-157">Ota Luokkasivu--osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6819e-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="6819e-158">Luokkasivut luodaan Luokkahierarkia-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6819e-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="6819e-159">Niissä on esimerkiksi seuraavia tietoja hankintaluokista: tiedot luokan tuotetyypeistä, luokan tuotteiden kuvat ja ilmoitukset, kuten luokassa käytettävissä olevat alennukset.</span><span class="sxs-lookup"><span data-stu-id="6819e-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="6819e-160">Luokkasivulla olevat tiedot näytetään ostoehdotuksissa.</span><span class="sxs-lookup"><span data-stu-id="6819e-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="6819e-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6819e-161">Close the page.</span></span>


