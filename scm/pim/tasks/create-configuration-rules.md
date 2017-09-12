--- 
title: "Luo konfiguraatiosäännöt"
description: "Tässä menetelmässä luodaan konfigurointisäännöt, joita voidaan käyttää dimensioihin perustuvassa konfiguraatiossa pakottamaan tai estämään tietyt tuoterakenneriviyhdistelmät."
author: BibiSp
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
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c901ebea4fd7423db61ef2c33689e606e33e2434
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-configuration-rules"></a><span data-ttu-id="4015c-103">Luo konfiguraatiosäännöt</span><span class="sxs-lookup"><span data-stu-id="4015c-103">Create configuration rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4015c-104">Tässä menetelmässä luodaan konfigurointisäännöt, joita voidaan käyttää dimensioihin perustuvassa konfiguraatiossa pakottamaan tai estämään tietyt tuoterakenneriviyhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="4015c-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="4015c-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="4015c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4015c-106">Tämä on seitsemäs kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan.</span><span class="sxs-lookup"><span data-stu-id="4015c-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="4015c-107">Valitse Tuotetietojen hallinta > Tuoterakenteet ja kaavat > Tuoterakenteet.</span><span class="sxs-lookup"><span data-stu-id="4015c-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="4015c-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4015c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4015c-109">Etsi ja valitse dimensioihin perustuvan konfiguraation tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="4015c-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="4015c-110">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="4015c-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="4015c-111">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="4015c-111">Click Change view.</span></span>
5. <span data-ttu-id="4015c-112">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="4015c-112">Click Header view.</span></span>
    * <span data-ttu-id="4015c-113">Pääset konfiguraatioreitin pikavälilehteen avaamalla otsikkonäkymän.</span><span class="sxs-lookup"><span data-stu-id="4015c-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="4015c-114">Laajenna tai tiivistä Konfiguraatioreitti-osa.</span><span class="sxs-lookup"><span data-stu-id="4015c-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="4015c-115">Konfiguraatioreitin pikavälilehti on laajennettava</span><span class="sxs-lookup"><span data-stu-id="4015c-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="4015c-116">Valitse Konfiguraatiosäännöt.</span><span class="sxs-lookup"><span data-stu-id="4015c-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="4015c-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4015c-117">Click New.</span></span>
9. <span data-ttu-id="4015c-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4015c-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="4015c-119">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4015c-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4015c-120">Nykyisen konfiguraatioryhmän nimikkeen näkyvät.</span><span class="sxs-lookup"><span data-stu-id="4015c-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="4015c-121">Valitse säännön ehto vastaava nimike.</span><span class="sxs-lookup"><span data-stu-id="4015c-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="4015c-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4015c-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="4015c-123">Valitse vaihtoehto Menetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4015c-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="4015c-124">Nimikkeen valinta toisesta konfigurointiryhmästä tai sen valinnan poisto voidaan pakottaa.</span><span class="sxs-lookup"><span data-stu-id="4015c-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="4015c-125">Avaa haku napsauttamalla Johdannaisryhmä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4015c-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="4015c-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4015c-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="4015c-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4015c-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4015c-128">Valitse haluttu konfiguraatioryhmä.</span><span class="sxs-lookup"><span data-stu-id="4015c-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="4015c-129">Avaa haku valitsemalla Johdettu nimiketunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4015c-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="4015c-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4015c-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4015c-131">Valitse nimiketunnus, joka valitaan tai jonka valinta poistetaan valitun menetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="4015c-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="4015c-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4015c-132">Close the page.</span></span>


