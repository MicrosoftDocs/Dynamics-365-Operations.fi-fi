---
title: Määritä Lean-aikatauluryhmät
description: Lean-aikatauluryhmät on määritetty ryhmittelemään ja erottamaan kanban-ajoituksen tuotteet.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 647e721a0616ceae387322517f2955d75c06bfd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828751"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="3057d-103">Määritä Lean-aikatauluryhmät</span><span class="sxs-lookup"><span data-stu-id="3057d-103">Define lean schedule groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3057d-104">Lean-aikatauluryhmät on määritetty ryhmittelemään ja erottamaan kanban-ajoituksen tuotteet.</span><span class="sxs-lookup"><span data-stu-id="3057d-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="3057d-105">Ryhmittely voidaan tehdä yleisenä yrityskohtaisena liitoksena tai työsolukohtaisena liitoksena.</span><span class="sxs-lookup"><span data-stu-id="3057d-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="3057d-106">Kullekin ryhmälle määritetään väri, jolla se tunnistetaan kanban-ajoituksen luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="3057d-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="3057d-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="3057d-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="3057d-108">Määritä Lean-aikatauluryhmä</span><span class="sxs-lookup"><span data-stu-id="3057d-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="3057d-109">Valitse Tuotetietojen hallinta > Lean-valmistus > Lean-aikatauluryhmät.</span><span class="sxs-lookup"><span data-stu-id="3057d-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="3057d-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3057d-110">Click New.</span></span>
3. <span data-ttu-id="3057d-111">Kirjoita arvo Aikatauluryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3057d-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="3057d-112">Aikatauluryhmä voidaan määrittää yleisenä tai työsolukohtaisena ryhmänä.</span><span class="sxs-lookup"><span data-stu-id="3057d-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="3057d-113">Tässä yksinkertaisessa esimerkissä määritetään yleinen ryhmä määrittää ja työsolu jää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="3057d-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="3057d-114">Tämän ryhmän asetuksia käytetään kaikissa työsoluissa, joille ei ole määritettyjä aikatauluryhmiä.</span><span class="sxs-lookup"><span data-stu-id="3057d-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="3057d-115">Valitse väri värivalikoimasta.</span><span class="sxs-lookup"><span data-stu-id="3057d-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="3057d-116">Kanban-aikataulun luettelosivun tai kanban-prosessitaulun työt korostetaan värien avulla.</span><span class="sxs-lookup"><span data-stu-id="3057d-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="3057d-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3057d-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="3057d-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3057d-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="3057d-119">Liitä tuote</span><span class="sxs-lookup"><span data-stu-id="3057d-119">Associate product</span></span>
1. <span data-ttu-id="3057d-120">Liitä tietty tuote</span><span class="sxs-lookup"><span data-stu-id="3057d-120">Associate a specific product</span></span>
    * <span data-ttu-id="3057d-121">Tuotteet voidaan liittää Lean-aikatauluryhmään kahdella tavalla: kyse voi olla joko määritetystä tuotteesta (nimikkeen suhdetyyppi = nimike) tai tuotteet ovat osa nimikkeenkohdistustunnusta (nimikkeen suhdetyyppi = ryhmä).</span><span class="sxs-lookup"><span data-stu-id="3057d-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="3057d-122">Valitse Nimikkeen suhdetyyppi -kentässä Nimike.</span><span class="sxs-lookup"><span data-stu-id="3057d-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="3057d-123">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3057d-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="3057d-124">Lisää numero Tuotantokapasiteetin suhdeluku -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3057d-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="3057d-125">Tuotantokapasiteetin oletusaste on 1, jolloin liittyvät tuotteet kuluttavat täsmälleen tuotantovirtojen prosessitehtävissä määritetyn kapasiteetin.</span><span class="sxs-lookup"><span data-stu-id="3057d-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="3057d-126">Jos tuotantokapasiteettiaste on > 1, resursseja kulutetaan enemmän, ja jos tuotantokapasiteettiaste on < 1, resursseja kulutetaan vähemmän.</span><span class="sxs-lookup"><span data-stu-id="3057d-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="3057d-127">Astetta käytetään kustannuslaskennassa ja kanban-työn kulutuksen laskennassa.</span><span class="sxs-lookup"><span data-stu-id="3057d-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="3057d-128">Liitä nimikkeen kohdistustunnus</span><span class="sxs-lookup"><span data-stu-id="3057d-128">Associate item allocation key</span></span>
1. <span data-ttu-id="3057d-129">Liitä nimikkeen kohdistustunnus.</span><span class="sxs-lookup"><span data-stu-id="3057d-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="3057d-130">Lisää liitos nimikkeenkohdistustunnukseen käyttämällä käyttäen nimikkeen suhdetyyppinä ryhmää.</span><span class="sxs-lookup"><span data-stu-id="3057d-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="3057d-131">Huomaa, että tätä prosessia varten tietoihin on määritettävä ennusteen nimikkeenkohdistustunnus.</span><span class="sxs-lookup"><span data-stu-id="3057d-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="3057d-132">Valitse Nimikkeen suhdetyyppi -kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="3057d-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="3057d-133">Avaa haku napsauttamalla Nimikkeenkohdistustunnus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="3057d-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3057d-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3057d-134">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]