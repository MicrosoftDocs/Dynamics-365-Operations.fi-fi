---
title: Valmiin tuotteen luominen (helmikuu 2016)
description: Tämä tehtävä keskittyy valmiin tuotteen luomiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "349719"
---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="33485-103">Valmiin tuotteen luominen (helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="33485-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33485-104">Tämä tehtävä keskittyy valmiin tuotteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="33485-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="33485-105">Se on tuoterakenteen laskentasarjan ensimmäinen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="33485-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="33485-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="33485-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="33485-107">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="33485-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="33485-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="33485-108">Click New.</span></span>
3. <span data-ttu-id="33485-109">Kirjoita arvo Tuotenumero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="33485-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="33485-110">Kirjoita esimerkkiä varten BOM_1.</span><span class="sxs-lookup"><span data-stu-id="33485-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="33485-111">Syötä tai valitse arvo Nimikemalliryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-112">Valitse STD.</span><span class="sxs-lookup"><span data-stu-id="33485-112">Select STD.</span></span> <span data-ttu-id="33485-113">STD standardikustannusta ja on kustannuslaskennassa yleisimmin käytetty malli.</span><span class="sxs-lookup"><span data-stu-id="33485-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="33485-114">Anna tai valitse arvo Nimikeryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-115">Valitse esimerkiksi Audio.</span><span class="sxs-lookup"><span data-stu-id="33485-115">For example, select Audio.</span></span> <span data-ttu-id="33485-116">Se ei vaikuta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="33485-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="33485-117">Syötä tai valitse arvo Varastodimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-118">Valitse SiteWH.</span><span class="sxs-lookup"><span data-stu-id="33485-118">Select SiteWH.</span></span> <span data-ttu-id="33485-119">Esimerkissä käytetään vain toimipaikkaa ja varastoa.</span><span class="sxs-lookup"><span data-stu-id="33485-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="33485-120">Syötä tai valitse arvo Seurantadimensioryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-121">Tässä esimerkissä ei käytetä seurantadimensioita. Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="33485-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="33485-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="33485-122">Click OK.</span></span>
9. <span data-ttu-id="33485-123">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="33485-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="33485-124">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="33485-124">Click Default order settings.</span></span>
11. <span data-ttu-id="33485-125">Valitse Oletusarvoinen tilaustyyppi -kentässä Tuotanto.</span><span class="sxs-lookup"><span data-stu-id="33485-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="33485-126">Koska kyse on valmiista tuotantoon tulevasta tuotteesta, valitse Tuotanto.</span><span class="sxs-lookup"><span data-stu-id="33485-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="33485-127">Anna tai valitse arvo Ostotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-128">Valitse esimerkkiä varten Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="33485-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="33485-129">Anna tai valitse arvo Varastotoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-130">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="33485-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="33485-131">Anna tai valitse arvo Myyntitoimipaikka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="33485-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="33485-132">Valitse tässä esimerkissä Toimipaikka 1.</span><span class="sxs-lookup"><span data-stu-id="33485-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="33485-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="33485-133">Close the page.</span></span>

