---
title: Luo uusi varastoasettelu
description: "Tässä kuvataan, miten varaston sijaintien tiedot määritetään."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 11ad27e68e8eb499b2cf8e477d3dbf51d930b736
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="52af0-103">Luo uusi varastoasettelu</span><span class="sxs-lookup"><span data-stu-id="52af0-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52af0-104">Tässä kuvataan, miten varaston sijaintien tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="52af0-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="52af0-105">Tämä koskee vain varastoinninhallintamoduulissa Perusvarastointi-asetuksen avulla luotuja varastoja, ei varastonhallintamoduulissa luotuja varastoja.</span><span class="sxs-lookup"><span data-stu-id="52af0-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="52af0-106">Voit käyttää tätä menettelyä emotietojen yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="52af0-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="52af0-107">Oletussijainnin kapasiteetin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="52af0-107">Set the default location capacity</span></span>
1. <span data-ttu-id="52af0-108">Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="52af0-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="52af0-109">Valitse Sijainnit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="52af0-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="52af0-110">Syötä numero Vakioleveys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="52af0-111">Syötä numero Vakiosyvyys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="52af0-112">Syötä numero Vakiokorkeus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="52af0-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="52af0-113">Click Save.</span></span>
7. <span data-ttu-id="52af0-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="52af0-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="52af0-115">Sijainnin nimen muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="52af0-115">Define the location name format</span></span>
1. <span data-ttu-id="52af0-116">Mene Varastonhallinta > Asetukset > Inventaarioanalyysi > Varastot.</span><span class="sxs-lookup"><span data-stu-id="52af0-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="52af0-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="52af0-117">Click New.</span></span>
3. <span data-ttu-id="52af0-118">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="52af0-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="52af0-120">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="52af0-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="52af0-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="52af0-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="52af0-122">Ota käyttöön Sijainnin nimet -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="52af0-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="52af0-123">Tämän osan valinnat määrittävät sijainnin nimien oletusmuodon.</span><span class="sxs-lookup"><span data-stu-id="52af0-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="52af0-124">Esimerkissä käytetään käytävän, hyllykön ja hyllyn numeroa.</span><span class="sxs-lookup"><span data-stu-id="52af0-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="52af0-125">Määritä Sisällytä käytävä -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="52af0-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="52af0-126">Määritä Sisällytä hyllykkö -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="52af0-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="52af0-127">Kirjoita hyllykön arvo Muoto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="52af0-128">Esimerkki: -##</span><span class="sxs-lookup"><span data-stu-id="52af0-128">For example: -##</span></span>  
11. <span data-ttu-id="52af0-129">Määritä Sisällytä hylly -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="52af0-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="52af0-130">Kirjoita hyllyn arvo Muoto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="52af0-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="52af0-131">Esimerkki: -##</span><span class="sxs-lookup"><span data-stu-id="52af0-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="52af0-132">Varaston sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="52af0-132">Define warehouse locations</span></span>
1. <span data-ttu-id="52af0-133">Valitse toimintoruudussa Varasto.</span><span class="sxs-lookup"><span data-stu-id="52af0-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="52af0-134">Valitse ohjattu sijaintien luontitoiminto.</span><span class="sxs-lookup"><span data-stu-id="52af0-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="52af0-135">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-135">Click Next.</span></span>
4. <span data-ttu-id="52af0-136">Poista Lähtevien laiturit -vaihtoehdon valinta</span><span class="sxs-lookup"><span data-stu-id="52af0-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="52af0-137">Poista Bulkkisijainnit-vaihtoehdon valinta</span><span class="sxs-lookup"><span data-stu-id="52af0-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="52af0-138">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-138">Click Next.</span></span>
7. <span data-ttu-id="52af0-139">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-139">Click Next.</span></span>
8. <span data-ttu-id="52af0-140">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-140">Click Next.</span></span>
9. <span data-ttu-id="52af0-141">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-141">Click Next.</span></span>
10. <span data-ttu-id="52af0-142">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-142">Click Next.</span></span>
11. <span data-ttu-id="52af0-143">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-143">Click Next.</span></span>
12. <span data-ttu-id="52af0-144">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-144">Click Next.</span></span>
    * <span data-ttu-id="52af0-145">Huomaa, että tällä sivulla näkyvät fyysiset dimensiot ovat tämän menettelyn alussa määrittämäsi dimensiot.</span><span class="sxs-lookup"><span data-stu-id="52af0-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="52af0-146">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="52af0-146">Click Next.</span></span>
14. <span data-ttu-id="52af0-147">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="52af0-147">Click Finish.</span></span>
15. <span data-ttu-id="52af0-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="52af0-148">Close the page.</span></span>
16. <span data-ttu-id="52af0-149">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="52af0-149">Refresh the page.</span></span>

