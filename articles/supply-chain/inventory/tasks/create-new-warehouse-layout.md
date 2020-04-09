---
title: Luo uusi varastoasettelu
description: Tässä ohjeaiheessa kuvataan, kuinka voit varastosijainteihin liittyvät tiedot.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399c87c2e5ad26d5ccc1618cfb6520de3fcdc644
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145660"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="aabb0-103">Luo uusi varastoasettelu</span><span class="sxs-lookup"><span data-stu-id="aabb0-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aabb0-104">Tässä ohjeaiheessa kuvataan, kuinka voit varastosijainteihin liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="aabb0-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="aabb0-105">Tämä koskee vain varastoinninhallintamoduulissa Perusvarastointi-asetuksen avulla luotuja varastoja, ei varastonhallintamoduulissa luotuja varastoja.</span><span class="sxs-lookup"><span data-stu-id="aabb0-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="aabb0-106">Voit käyttää tätä menettelyä emotietojen yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="aabb0-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="aabb0-107">Oletussijainnin kapasiteetin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aabb0-107">Set the default location capacity</span></span>
1. <span data-ttu-id="aabb0-108">Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="aabb0-109">Valitse **Sijainnit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="aabb0-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="aabb0-110">Syötä numero **Vakioleveys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="aabb0-111">Syötä numero **Vakiosyvyys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="aabb0-112">Syötä numero **Vakiokorkeus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="aabb0-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-113">Select **Save**.</span></span>
7. <span data-ttu-id="aabb0-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aabb0-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="aabb0-115">Sijainnin nimen muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aabb0-115">Define the location name format</span></span>
1. <span data-ttu-id="aabb0-116">Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Varastoerittely > Varastot**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="aabb0-117">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-117">Select **New**.</span></span>
3. <span data-ttu-id="aabb0-118">Kirjoita arvo **Varasto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="aabb0-119">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="aabb0-120">Valitse **Toimipaikka**-kentän valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="aabb0-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="aabb0-121">Ota käyttöön **Sijainnin nimet** -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="aabb0-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="aabb0-122">Tämän osan valinnat määrittävät sijainnin nimien oletusmuodon.</span><span class="sxs-lookup"><span data-stu-id="aabb0-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="aabb0-123">Esimerkissä käytetään käytävän, hyllykön ja hyllyn numeroa.</span><span class="sxs-lookup"><span data-stu-id="aabb0-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="aabb0-124">Määritä **Sisällytä käytävä** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="aabb0-125">Määritä **Sisällytä hyllykkö** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="aabb0-126">Kirjoita hyllykön arvo **Muoto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="aabb0-127">Määritä **Sisällytä hylly** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="aabb0-128">Kirjoita hyllyn arvo **Muoto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aabb0-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="aabb0-129">Varaston sijaintien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aabb0-129">Define warehouse locations</span></span>
1. <span data-ttu-id="aabb0-130">Valitse toimintoruudussa **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="aabb0-131">Valitse **Ohjattu sijaintien luontitoiminto**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="aabb0-132">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="aabb0-132">Select **Next**.</span></span>
4. <span data-ttu-id="aabb0-133">Poista **Lähtevien laiturit** -vaihtoehdon valinta</span><span class="sxs-lookup"><span data-stu-id="aabb0-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="aabb0-134">Poista **Bulkkisijainnit**-vaihtoehdon valinta</span><span class="sxs-lookup"><span data-stu-id="aabb0-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="aabb0-135">Valitse **Seuraava**, kunnes valitset **Valmis**-vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="aabb0-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="aabb0-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aabb0-136">Close the page.</span></span>
8. <span data-ttu-id="aabb0-137">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="aabb0-137">Refresh the page.</span></span>

