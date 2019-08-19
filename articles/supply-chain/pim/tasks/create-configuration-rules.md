---
title: Luo konfiguraatiosäännöt
description: Tässä menetelmässä luodaan konfigurointisäännöt, joita voidaan käyttää dimensioihin perustuvassa konfiguraatiossa pakottamaan tai estämään tietyt tuoterakenneriviyhdistelmät.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f15c0328e391d81c4c977f974553ae9135b207c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844894"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="30fe4-103">Luo konfiguraatiosäännöt</span><span class="sxs-lookup"><span data-stu-id="30fe4-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30fe4-104">Tässä menetelmässä luodaan konfigurointisäännöt, joita voidaan käyttää dimensioihin perustuvassa konfiguraatiossa pakottamaan tai estämään tietyt tuoterakenneriviyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="30fe4-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="30fe4-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="30fe4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="30fe4-106">Tämä on seitsemäs kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan.</span><span class="sxs-lookup"><span data-stu-id="30fe4-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="30fe4-107">Valitse Tuotetietojen hallinta > Tuoterakenteet ja kaavat > Tuoterakenteet.</span><span class="sxs-lookup"><span data-stu-id="30fe4-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="30fe4-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="30fe4-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="30fe4-109">Etsi ja valitse dimensioihin perustuvan konfiguraation tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="30fe4-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="30fe4-110">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="30fe4-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="30fe4-111">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-111">Click Change view.</span></span>
5. <span data-ttu-id="30fe4-112">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-112">Click Header view.</span></span>
    * <span data-ttu-id="30fe4-113">Pääset konfiguraatioreitin pikavälilehteen avaamalla otsikkonäkymän.</span><span class="sxs-lookup"><span data-stu-id="30fe4-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="30fe4-114">Laajenna tai tiivistä Konfiguraatioreitti-osa.</span><span class="sxs-lookup"><span data-stu-id="30fe4-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="30fe4-115">Konfiguraatioreitin pikavälilehti on laajennettava</span><span class="sxs-lookup"><span data-stu-id="30fe4-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="30fe4-116">Valitse Konfiguraatiosäännöt.</span><span class="sxs-lookup"><span data-stu-id="30fe4-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="30fe4-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="30fe4-117">Click New.</span></span>
9. <span data-ttu-id="30fe4-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="30fe4-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="30fe4-119">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="30fe4-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="30fe4-120">Nykyisen konfiguraatioryhmän nimikkeen näkyvät.</span><span class="sxs-lookup"><span data-stu-id="30fe4-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="30fe4-121">Valitse säännön ehto vastaava nimike.</span><span class="sxs-lookup"><span data-stu-id="30fe4-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="30fe4-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="30fe4-123">Valitse vaihtoehto Menetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="30fe4-124">Nimikkeen valinta toisesta konfigurointiryhmästä tai sen valinnan poisto voidaan pakottaa.</span><span class="sxs-lookup"><span data-stu-id="30fe4-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="30fe4-125">Avaa haku napsauttamalla Johdannaisryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="30fe4-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="30fe4-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="30fe4-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="30fe4-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30fe4-128">Valitse haluttu konfiguraatioryhmä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="30fe4-129">Avaa haku valitsemalla Johdettu nimiketunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="30fe4-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="30fe4-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="30fe4-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30fe4-131">Valitse nimiketunnus, joka valitaan tai jonka valinta poistetaan valitun menetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="30fe4-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="30fe4-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="30fe4-132">Close the page.</span></span>

