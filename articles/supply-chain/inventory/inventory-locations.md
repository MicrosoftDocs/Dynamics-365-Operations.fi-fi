---
title: Varastosijainnit
description: Varastopaikkoja käytetään perusvarastoinnin (WMS I) kanssa määrittämään, mihin nimikkeet varastoidaan ja mistä nimikkeet poimitaan WMS I -varastossa.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 490f510ca0a5522d7bc892733ff066ebc65bcd24
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017365"
---
# <a name="inventory-locations"></a><span data-ttu-id="8fdf2-103">Varastosijainnit</span><span class="sxs-lookup"><span data-stu-id="8fdf2-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fdf2-104">Varastopaikkoja käytetään perusvarastoinnin (WMS I) kanssa määrittämään, mihin nimikkeet varastoidaan ja mistä nimikkeet poimitaan WMS I -varastossa.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="8fdf2-105">Tämä ohjeaihe koskee inventaarionhallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="8fdf2-106">Se ei koske varastonhallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="8fdf2-107">Termi sijainti tarkoittaa paikkaa, johon nimikkeet on varastoitu ja josta ne otetaan.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="8fdf2-108">Jokaiselle sijainnille voidaan myös määrittää paikka, johon nimike asetetaan.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="8fdf2-109">Oletusarvon mukaan ovat samat.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-109">By default, they are the same.</span></span> <span data-ttu-id="8fdf2-110">Nimikkeet lisätään ja otetaan tavallisesti sijainnin samalta puolelta, mutta ei kuitenkaan aina.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="8fdf2-111">Esimerkiksi nimikkeet, jotka varastoidaan live-tallennustelineisiin, jotka asetetaan yhdeltä käytävältä ja vedetään toiselta.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="8fdf2-112">Pääsyöte on sijainnin nimi, joka määritetään tavallisesti koordinaattien perusteella: varasto, käytävä, teline, hylly ja lokero.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="8fdf2-113">Tämän nimen tai tunnuksen voi kirjoittaa manuaalisesti, tai sen voi luoda sijaintikoordinaateista; esimerkiksi 01-02-03-4 tarkoittaa käytävää 1, telinettä 2, hyllyä 3 ja lokeroa 4 Varastosijainnit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="8fdf2-114">Varastopaikan ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8fdf2-114">Location properties</span></span>

<span data-ttu-id="8fdf2-115">Varastopaikalla on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="8fdf2-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="8fdf2-116">Koko (korkeus, leveys, syvyys ja siten tilavuus)</span><span class="sxs-lookup"><span data-stu-id="8fdf2-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="8fdf2-117">Varaston, käytävän, telineen, hyllyn ja lokeron sijainti</span><span class="sxs-lookup"><span data-stu-id="8fdf2-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="8fdf2-118">Varastopaikan tyyppi (bulkkisijainti, keräilysijainti, saapuvien laituri, lähtevien laituri, tuotannon varastoinnin sijainti, tarkastussijainti tai kanban-supermarket)</span><span class="sxs-lookup"><span data-stu-id="8fdf2-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="8fdf2-119">Online-järjestelmissä voi tarkistaa tarkistustekstin avulla, että operaattori on valinnut nimikkeelle oikean varastopaikan.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="8fdf2-120">Tarkistustekstin voi luoda manuaalisesti tai automaattisesti oletusarvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="8fdf2-121">Lajittelutunnukset</span><span class="sxs-lookup"><span data-stu-id="8fdf2-121">Sort codes</span></span>
<span data-ttu-id="8fdf2-122">Lajittelutunnusten avulla voit optimoida keräilyrivien käsittelyn. Keräilyriveissä on nimikkeiden varastosta keräämistä varten tarvittavat tiedot, kuten keräilyjärjestys.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="8fdf2-123">Lajittelukoodit voidaan määrittää esimerkiksi käytävittäin, tai manuaalisesti sijainnille.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="8fdf2-124">Varastopaikkojen estot</span><span class="sxs-lookup"><span data-stu-id="8fdf2-124">Blocked locations</span></span>
<span data-ttu-id="8fdf2-125">Joskus varastopaikka on merkittävä suljetuksi joksikin aikaa esimerkiksi korjauksen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="8fdf2-126">Joskus taas voi olla tarpeen estää vain nimikkeiden syöttö varastopaikkaan tai kerääminen sieltä.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="8fdf2-127">Puurakenne</span><span class="sxs-lookup"><span data-stu-id="8fdf2-127">Tree structure</span></span>

<span data-ttu-id="8fdf2-128">Varastosijainnit-sivulla voit tarkastella varaston asettelua puurakenteena, joka perustuu varastopaikkojen koordinaatteihin määritellyssä näyttömuodossa.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="8fdf2-129">Varastosijaintien ylläpito varastolomakkeessa</span><span class="sxs-lookup"><span data-stu-id="8fdf2-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="8fdf2-130">Sijainteja voidaan kopioida varastosta toiseen ja luoda ohjatun toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="8fdf2-131">Ennen ohjatun toiminnon suorittamista varmista, että olet määrittänyt sijainnin oletusnimet Varasto-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8fdf2-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="8fdf2-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8fdf2-132">Additional resources</span></span>
--------

[<span data-ttu-id="8fdf2-133">Luo uusi varastoasettelu</span><span class="sxs-lookup"><span data-stu-id="8fdf2-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)
