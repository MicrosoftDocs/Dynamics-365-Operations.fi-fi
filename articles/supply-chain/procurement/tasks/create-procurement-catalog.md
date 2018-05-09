--- 
title: Luo hankintaluettelo
description: "Tässä oppaassa näytetään, miten tuotteiden hankintaluettelo luodaan."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2bda068c71b768eb0caadfdbf8b4fe5620bd8eea
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="36e13-103">Luo hankintaluettelo</span><span class="sxs-lookup"><span data-stu-id="36e13-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36e13-104">Tässä oppaassa näytetään, miten tuotteiden hankintaluettelo luodaan.</span><span class="sxs-lookup"><span data-stu-id="36e13-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="36e13-105">Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="36e13-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="36e13-106">Opit myös, miten työntekijät voivat käyttää luetteloa ostoehdotuksien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="36e13-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="36e13-107">Järjestelmässä on oltava hankintaluokkahierarkia ennen luettelon luomista.</span><span class="sxs-lookup"><span data-stu-id="36e13-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="36e13-108">Hierarkia periytyy uuteen luetteloon, kuten myös kaikki hierarkian tuotteet.</span><span class="sxs-lookup"><span data-stu-id="36e13-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="36e13-109">Voit käyttää tätä opasta USMF-demoyrityksessä, jossa hankintaluokkahierarkia sekä menettelyn ohjeissa käytetyt esimerkit ovat saatavilla.</span><span class="sxs-lookup"><span data-stu-id="36e13-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="36e13-110">Varmista, että hankintaluokkahierarkia on olemassa</span><span class="sxs-lookup"><span data-stu-id="36e13-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="36e13-111">Valitse Hankinta > Hankintaluokat.</span><span class="sxs-lookup"><span data-stu-id="36e13-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="36e13-112">Hankintaluokkahierarkia sisältyy USMF-demoyrityksen tietoihin ja tuotteet on lisätty Toimiston koneet/Tietokoneet -luokkaan.</span><span class="sxs-lookup"><span data-stu-id="36e13-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="36e13-113">Jos käytät menettelyä tehtäväoppaana, sinun on ehkä poistettava lukitus, jos haluat selata luokkaa.</span><span class="sxs-lookup"><span data-stu-id="36e13-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="36e13-114">Jos hierarkia ei ole käytettävissä, voit luoda sen napsauttamalla Uusi-painiketta.</span><span class="sxs-lookup"><span data-stu-id="36e13-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="36e13-115">Tämän voi tehdä vain kerran.</span><span class="sxs-lookup"><span data-stu-id="36e13-115">This can only be done once.</span></span>  
2. <span data-ttu-id="36e13-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36e13-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="36e13-117">Luo luettelo</span><span class="sxs-lookup"><span data-stu-id="36e13-117">Create a catalog</span></span>
1. <span data-ttu-id="36e13-118">Siirry kohtaan Hankinta > Luettelot > Tuotteiden hankintaluettelot.</span><span class="sxs-lookup"><span data-stu-id="36e13-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="36e13-119">Avaa valintaikkuna valitsemalla Uusi tuotteiden hankintaluettelo.</span><span class="sxs-lookup"><span data-stu-id="36e13-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="36e13-120">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36e13-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="36e13-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36e13-121">Click OK.</span></span>
5. <span data-ttu-id="36e13-122">Laajenna puussa CORP PROCUREMENT CATEGORIES.</span><span class="sxs-lookup"><span data-stu-id="36e13-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="36e13-123">Laajenna puussa OFFICE MACHINES.</span><span class="sxs-lookup"><span data-stu-id="36e13-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="36e13-124">Valitse puussa "Tietokoneet".</span><span class="sxs-lookup"><span data-stu-id="36e13-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="36e13-125">Hankintaluokan tuotteet näytetään luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36e13-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="36e13-126">Jos haluat lisätä tuotteen luokkaan, tämä on tehtävä Hankintaluokkahierarkia-sivulla tai Nimiketiedot-sivulla.</span><span class="sxs-lookup"><span data-stu-id="36e13-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="36e13-127">Päivityksen oletustyyppi määrittää, ovatko uudet, hankintaluokkahierarkiaan lisätyt tuotteet välittömästi näkyvissä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36e13-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="36e13-128">Jos päivityksen tyyppinä on dynaaminen, muutokset näkyvät heti.</span><span class="sxs-lookup"><span data-stu-id="36e13-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="36e13-129">Jos päivitystyyppi on staattinen, uudet tuotteet näkyvät luettelon käyttäjille vasta, kun se on julkaistu uudelleen.</span><span class="sxs-lookup"><span data-stu-id="36e13-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="36e13-130">Julkaise-toiminto on käytettävissä sivun yläosan toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="36e13-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="36e13-131">Jos tuotteita poistetaan hankintaluokkahierarkiasta, muutos näkyy heti Oletuspäivitystyyppi-kentän arvosta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="36e13-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="36e13-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="36e13-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="36e13-133">Valitse Piilota.</span><span class="sxs-lookup"><span data-stu-id="36e13-133">Click Hide.</span></span>
10. <span data-ttu-id="36e13-134">Valitse toimintoruudussa Luettelonavigointi.</span><span class="sxs-lookup"><span data-stu-id="36e13-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="36e13-135">Valitse Poista käytöstä.</span><span class="sxs-lookup"><span data-stu-id="36e13-135">Click Disable.</span></span>
12. <span data-ttu-id="36e13-136">Valitse toimintoruudussa Luettelonavigointi.</span><span class="sxs-lookup"><span data-stu-id="36e13-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="36e13-137">Napsauta Ota käyttöön.</span><span class="sxs-lookup"><span data-stu-id="36e13-137">Click Enable.</span></span>
14. <span data-ttu-id="36e13-138">Valitse Aktivoi luettelo.</span><span class="sxs-lookup"><span data-stu-id="36e13-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="36e13-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36e13-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="36e13-140">Tee luettelosta näkyvä</span><span class="sxs-lookup"><span data-stu-id="36e13-140">Make the catalog visible</span></span>
1. <span data-ttu-id="36e13-141">Siirry kohtaan Hankinnat > Asetukset > Käytännöt > Ostokäytännöt.</span><span class="sxs-lookup"><span data-stu-id="36e13-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="36e13-142">Valitse hankintakäytäntö USMF.</span><span class="sxs-lookup"><span data-stu-id="36e13-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="36e13-143">Sinun on valittava ostokäytäntö yritykselle, johon käyttäjäprofiiliisi liitetty työntekijä saa tilata tuotteita.</span><span class="sxs-lookup"><span data-stu-id="36e13-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="36e13-144">USMF-demoyrityksen tiedoissa järjestelmänvalvoja on liitetty työntekijään nimeltä Julia Funderburk, joka on USMF:n oletustilaaja tuotteille.</span><span class="sxs-lookup"><span data-stu-id="36e13-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="36e13-145">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="36e13-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="36e13-146">Valitse juuri luomasi luettelo.</span><span class="sxs-lookup"><span data-stu-id="36e13-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="36e13-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36e13-147">Click OK.</span></span>
6. <span data-ttu-id="36e13-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36e13-148">Close the page.</span></span>
7. <span data-ttu-id="36e13-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="36e13-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="36e13-150">Käytä luetteloa</span><span class="sxs-lookup"><span data-stu-id="36e13-150">Use the catalog</span></span>
1. <span data-ttu-id="36e13-151">Siirry kohtaan Hankinta > Ostoehdotukset > Kaikki ostoehdotukset.</span><span class="sxs-lookup"><span data-stu-id="36e13-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="36e13-152">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36e13-152">Click New.</span></span>
3. <span data-ttu-id="36e13-153">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36e13-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="36e13-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36e13-154">Click OK.</span></span>
5. <span data-ttu-id="36e13-155">Valitse Lisää tuotteet.</span><span class="sxs-lookup"><span data-stu-id="36e13-155">Click Add products.</span></span>
6. <span data-ttu-id="36e13-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="36e13-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="36e13-157">Voit käyttää tuotteiden suodattamiseen luokkahierarkiaa vasemmalla tai luettelon yläosassa olevaa suodatinta.</span><span class="sxs-lookup"><span data-stu-id="36e13-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="36e13-158">Valitse Lisää riveihin.</span><span class="sxs-lookup"><span data-stu-id="36e13-158">Click Add to lines.</span></span>
8. <span data-ttu-id="36e13-159">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="36e13-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="36e13-160">Valitse Lisää riveihin.</span><span class="sxs-lookup"><span data-stu-id="36e13-160">Click Add to lines.</span></span>
10. <span data-ttu-id="36e13-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="36e13-161">Click OK.</span></span>


