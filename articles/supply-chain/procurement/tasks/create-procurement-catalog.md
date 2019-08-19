---
title: Luo tuotteiden hankintaluettelo
description: Tässä ohjeaiheessa kerrotaan, miten voit luoda hankintaluettelon.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836378"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="00772-103">Luo tuotteiden hankintaluettelo</span><span class="sxs-lookup"><span data-stu-id="00772-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00772-104">Tässä ohjeaiheessa kerrotaan, miten voit luoda hankintaluettelon.</span><span class="sxs-lookup"><span data-stu-id="00772-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="00772-105">Yleensä hankinta-asiantuntijat suorittavat tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="00772-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="00772-106">Opit myös, miten työntekijät voivat käyttää luetteloa ostoehdotuksien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="00772-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="00772-107">Järjestelmässä on oltava hankintaluokkahierarkia ennen luettelon luomista.</span><span class="sxs-lookup"><span data-stu-id="00772-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="00772-108">Hierarkia periytyy uuteen luetteloon, kuten myös kaikki hierarkian tuotteet.</span><span class="sxs-lookup"><span data-stu-id="00772-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="00772-109">Voit käyttää tätä opasta USMF-demoyrityksessä, jossa hankintaluokkahierarkia sekä menettelyn ohjeissa käytetyt esimerkit ovat saatavilla.</span><span class="sxs-lookup"><span data-stu-id="00772-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="00772-110">Varmista, että hankintaluokkahierarkia on olemassa</span><span class="sxs-lookup"><span data-stu-id="00772-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="00772-111">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Hankintaluokat**.</span><span class="sxs-lookup"><span data-stu-id="00772-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="00772-112">Hankintaluokkahierarkia sisältyy USMF-demoyrityksen tietoihin ja tuotteet on lisätty **Toimiston koneet/Tietokoneet** -luokkaan.</span><span class="sxs-lookup"><span data-stu-id="00772-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="00772-113">Jos käytät menettelyä tehtäväoppaana, sinun on ehkä poistettava lukitus, jos haluat selata luokkaa.</span><span class="sxs-lookup"><span data-stu-id="00772-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="00772-114">Jos hierarkia ei ole käytettävissä, voit luoda sen napsauttamalla **Uusi**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="00772-114">If a hierarchy was not available, you’d create it by clicking **New**.</span></span> <span data-ttu-id="00772-115">Tämän voi tehdä vain kerran.</span><span class="sxs-lookup"><span data-stu-id="00772-115">This can only be done once.</span></span>  
2. <span data-ttu-id="00772-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="00772-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="00772-117">Luo luettelo</span><span class="sxs-lookup"><span data-stu-id="00772-117">Create a catalog</span></span>
1. <span data-ttu-id="00772-118">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Luettelot > Hankintaluettelot**.</span><span class="sxs-lookup"><span data-stu-id="00772-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="00772-119">Avaa valintaikkuna valitsemalla **Uusi tuotteiden hankintaluettelo**.</span><span class="sxs-lookup"><span data-stu-id="00772-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="00772-120">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00772-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="00772-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="00772-121">Select **OK**.</span></span>
5. <span data-ttu-id="00772-122">Laajenna puussa **CORP PROCUREMENT CATEGORIES**.</span><span class="sxs-lookup"><span data-stu-id="00772-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="00772-123">Laajenna puussa **OFFICE MACHINES**.</span><span class="sxs-lookup"><span data-stu-id="00772-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="00772-124">Valitse puussa **Tietokoneet**.</span><span class="sxs-lookup"><span data-stu-id="00772-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="00772-125">Hankintaluokan tuotteet näytetään luettelossa.</span><span class="sxs-lookup"><span data-stu-id="00772-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="00772-126">Jos haluat lisätä tuotteen luokkaan, tämä on tehtävä **Hankintaluokkahierarkia**-sivulla tai **Nimiketiedot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="00772-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="00772-127">**Oletus**-päivitystyyppi määrittää, ovatko uudet, hankintaluokkahierarkiaan lisätyt tuotteet välittömästi näkyvissä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="00772-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="00772-128">Jos päivityksen tyyppinä on **Dynaaminen**, muutokset näkyvät heti.</span><span class="sxs-lookup"><span data-stu-id="00772-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="00772-129">Jos päivitystyyppi on **Staattinen**, uudet tuotteet näkyvät luettelon käyttäjille vasta, kun se on julkaistu uudelleen.</span><span class="sxs-lookup"><span data-stu-id="00772-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="00772-130">**Julkaise**-toiminto on käytettävissä sivun yläosan toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="00772-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="00772-131">Jos tuotteita poistetaan hankintaluokkahierarkiasta, muutos näkyy heti **Oletus**-päivitystyypin kentän arvosta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="00772-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="00772-132">Valitse toimintoruudussa **Luettelonavigointi** ja varmista, että **Ota käyttöön** on valittuna.</span><span class="sxs-lookup"><span data-stu-id="00772-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="00772-133">Valitse **Aktivoi luettelo**.</span><span class="sxs-lookup"><span data-stu-id="00772-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="00772-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="00772-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="00772-135">Tee luettelosta näkyvä</span><span class="sxs-lookup"><span data-stu-id="00772-135">Make the catalog visible</span></span>
1. <span data-ttu-id="00772-136">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostokäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="00772-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="00772-137">Valitse **hankintakäytäntö USMF**.</span><span class="sxs-lookup"><span data-stu-id="00772-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="00772-138">Sinun on valittava ostokäytäntö yritykselle, johon käyttäjäprofiiliisi liitetty työntekijä saa tilata tuotteita.</span><span class="sxs-lookup"><span data-stu-id="00772-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="00772-139">USMF-demoyrityksen tiedoissa järjestelmänvalvoja on liitetty työntekijään nimeltä **Julia Funderburk**, joka on USMF:n oletustilaaja tuotteille.</span><span class="sxs-lookup"><span data-stu-id="00772-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="00772-140">Valitse juuri luomasi luettelo.</span><span class="sxs-lookup"><span data-stu-id="00772-140">Select the catalog that you’ve just created.</span></span>
4. <span data-ttu-id="00772-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="00772-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="00772-142">Käytä luetteloa</span><span class="sxs-lookup"><span data-stu-id="00772-142">Use the catalog</span></span>
1. <span data-ttu-id="00772-143">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostoehdotukset > Kaikki ostoehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="00772-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="00772-144">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="00772-144">Select **New**.</span></span>
3. <span data-ttu-id="00772-145">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00772-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="00772-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="00772-146">Select **OK**.</span></span>
5. <span data-ttu-id="00772-147">Valitse **Lisää tuotteita**.</span><span class="sxs-lookup"><span data-stu-id="00772-147">Select **Add products**.</span></span>
6. <span data-ttu-id="00772-148">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="00772-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="00772-149">Voit käyttää tuotteiden suodattamiseen luokkahierarkiaa vasemmalla tai luettelon yläosassa olevaa suodatinta.</span><span class="sxs-lookup"><span data-stu-id="00772-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="00772-150">Valitse **Lisää riveihin**.</span><span class="sxs-lookup"><span data-stu-id="00772-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="00772-151">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="00772-151">Select **OK**.</span></span>

