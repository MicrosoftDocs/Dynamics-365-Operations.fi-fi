---
title: Luo uusi varastoasettelu
description: Tässä kuvataan, miten varaston sijaintien tiedot määritetään.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572762"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="aa58a-103">Luo uusi varastoasettelu</span><span class="sxs-lookup"><span data-stu-id="aa58a-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa58a-104">Tässä kuvataan, miten varaston sijaintien tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="aa58a-105">Tämä koskee vain varastoinninhallintamoduulissa Perusvarastointi-asetuksen avulla luotuja varastoja, ei varastonhallintamoduulissa luotuja varastoja.</span><span class="sxs-lookup"><span data-stu-id="aa58a-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="aa58a-106">Voit käyttää tätä menettelyä emotietojen yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="aa58a-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="aa58a-107">Oletussijainnin kapasiteetin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa58a-107">Set the default location capacity</span></span>
1. <span data-ttu-id="aa58a-108">Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="aa58a-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="aa58a-109">Valitse Sijainnit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="aa58a-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="aa58a-110">Syötä numero Vakioleveys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="aa58a-111">Syötä numero Vakiosyvyys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="aa58a-112">Syötä numero Vakiokorkeus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="aa58a-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="aa58a-113">Click Save.</span></span>
7. <span data-ttu-id="aa58a-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aa58a-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="aa58a-115">Sijainnin nimen muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa58a-115">Define the location name format</span></span>
1. <span data-ttu-id="aa58a-116">Mene Varastonhallinta > Asetukset > Inventaarioanalyysi > Varastot.</span><span class="sxs-lookup"><span data-stu-id="aa58a-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="aa58a-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa58a-117">Click New.</span></span>
3. <span data-ttu-id="aa58a-118">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="aa58a-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="aa58a-120">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="aa58a-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="aa58a-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="aa58a-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="aa58a-122">Ota käyttöön Sijainnin nimet -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="aa58a-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="aa58a-123">Tämän osan valinnat määrittävät sijainnin nimien oletusmuodon.</span><span class="sxs-lookup"><span data-stu-id="aa58a-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="aa58a-124">Esimerkissä käytetään käytävän, hyllykön ja hyllyn numeroa.</span><span class="sxs-lookup"><span data-stu-id="aa58a-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="aa58a-125">Määritä Sisällytä käytävä -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="aa58a-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="aa58a-126">Määritä Sisällytä hyllykkö -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="aa58a-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="aa58a-127">Kirjoita hyllykön arvo Muoto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="aa58a-128">Esimerkki: -##</span><span class="sxs-lookup"><span data-stu-id="aa58a-128">For example: -##</span></span>  
11. <span data-ttu-id="aa58a-129">Määritä Sisällytä hylly -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="aa58a-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="aa58a-130">Kirjoita hyllyn arvo Muoto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa58a-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="aa58a-131">Esimerkki: -##</span><span class="sxs-lookup"><span data-stu-id="aa58a-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="aa58a-132">Varaston sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa58a-132">Define warehouse locations</span></span>
1. <span data-ttu-id="aa58a-133">Valitse toimintoruudussa Varasto.</span><span class="sxs-lookup"><span data-stu-id="aa58a-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="aa58a-134">Valitse ohjattu sijaintien luontitoiminto.</span><span class="sxs-lookup"><span data-stu-id="aa58a-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="aa58a-135">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-135">Click Next.</span></span>
4. <span data-ttu-id="aa58a-136">Poista Lähtevien laiturit -vaihtoehdon valinta</span><span class="sxs-lookup"><span data-stu-id="aa58a-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="aa58a-137">Poista Bulkkisijainnit-vaihtoehdon valinta</span><span class="sxs-lookup"><span data-stu-id="aa58a-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="aa58a-138">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-138">Click Next.</span></span>
7. <span data-ttu-id="aa58a-139">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-139">Click Next.</span></span>
8. <span data-ttu-id="aa58a-140">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-140">Click Next.</span></span>
9. <span data-ttu-id="aa58a-141">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-141">Click Next.</span></span>
10. <span data-ttu-id="aa58a-142">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-142">Click Next.</span></span>
11. <span data-ttu-id="aa58a-143">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-143">Click Next.</span></span>
12. <span data-ttu-id="aa58a-144">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-144">Click Next.</span></span>
    * <span data-ttu-id="aa58a-145">Huomaa, että tällä sivulla näkyvät fyysiset dimensiot ovat tämän menettelyn alussa määrittämäsi dimensiot.</span><span class="sxs-lookup"><span data-stu-id="aa58a-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="aa58a-146">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="aa58a-146">Click Next.</span></span>
14. <span data-ttu-id="aa58a-147">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="aa58a-147">Click Finish.</span></span>
15. <span data-ttu-id="aa58a-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aa58a-148">Close the page.</span></span>
16. <span data-ttu-id="aa58a-149">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="aa58a-149">Refresh the page.</span></span>

