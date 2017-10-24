--- 
title: "Määritä kustannusseurannan työtilan parametrit"
description: "Tämän menettelyn avulla voi määrittää kustannusseurannan työtilan niin, että organisaation eri tasojen esimiehet voivat tarkastella kustannusobjektejaan, kuten kustannuspaikkoja ja tuoteryhmiä."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8ede40951d08e159358b713fc3dde46576a1b4e3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="09ce2-103">Määritä kustannusseurannan työtilan parametrit</span><span class="sxs-lookup"><span data-stu-id="09ce2-103">Configure cost control workspace parameters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09ce2-104">Tämän menettelyn avulla voi määrittää kustannusseurannan työtilan niin, että organisaation eri tasojen esimiehet voivat tarkastella kustannusobjektejaan, kuten kustannuspaikkoja ja tuoteryhmiä.</span><span class="sxs-lookup"><span data-stu-id="09ce2-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="09ce2-105">Tämän tallenteen luomisessa käytetty demoyritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="09ce2-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="09ce2-106">Valitse Kustannuslaskenta > Asetukset > Kustannusseurannan työtilan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="09ce2-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="09ce2-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="09ce2-107">Click New.</span></span>
3. <span data-ttu-id="09ce2-108">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="09ce2-109">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09ce2-110">Valitse Julkaistu-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="09ce2-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="09ce2-111">Jos määrität tämän asetuksen arvoksi Kyllä, käyttäjät, joille on delegoitu jokin näistä rooleista, näkevät raportin kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija, kustannuslaskijan apulainen tai kustannusobjektin vastuuhenkilö.</span><span class="sxs-lookup"><span data-stu-id="09ce2-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="09ce2-112">Jos määrität tämän asetuksen arvoksi Ei, vain käyttäjät, joille on delegoitu jokin näistä rooleista, näkevät raportin kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija tai kustannuslaskijan apulainen.</span><span class="sxs-lookup"><span data-stu-id="09ce2-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="09ce2-113">Laajenna Tietojen suodattaminen -osa.</span><span class="sxs-lookup"><span data-stu-id="09ce2-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="09ce2-114">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="09ce2-115">Anna tai valitse arvo Budjetin alkuperäinen versio -kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="09ce2-116">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="09ce2-117">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="09ce2-118">Laajenna Määritä laskentatietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="09ce2-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="09ce2-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="09ce2-119">Click New.</span></span>
13. <span data-ttu-id="09ce2-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="09ce2-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="09ce2-121">Syötä tai valitse arvo Kirjanpidon vuosikalenterin kausi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="09ce2-122">Anna tai valitse arvo Todellinen versio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="09ce2-123">Laajenna Tilikausia sarakkeessa -osa.</span><span class="sxs-lookup"><span data-stu-id="09ce2-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="09ce2-124">Valitse Nykyinen kausi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="09ce2-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="09ce2-125">Laajenna Kustannusten näytettävät sarakkeet -osa.</span><span class="sxs-lookup"><span data-stu-id="09ce2-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="09ce2-126">Valitse Kiinteä kustannus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="09ce2-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="09ce2-127">Valitse Muuttuva kustannus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="09ce2-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="09ce2-128">Valitse Kokonaiskustannukset-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="09ce2-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="09ce2-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="09ce2-129">Click Save.</span></span>
23. <span data-ttu-id="09ce2-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="09ce2-130">Close the page.</span></span>
24. <span data-ttu-id="09ce2-131">Valitse Kustannuslaskenta > Työtilat > Kustannusseuranta.</span><span class="sxs-lookup"><span data-stu-id="09ce2-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="09ce2-132">Valitse ilmoitus, kun haluat nähdä valittujen tilikausien kiinteät, muuttuvat ja luokittelemattomat kustannukset sekä kokonaiskustannukset.</span><span class="sxs-lookup"><span data-stu-id="09ce2-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="09ce2-133">Syötä tai valitse arvo Kirjanpidon vuosikalenterin kausi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="09ce2-134">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="09ce2-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="09ce2-135">Kun olet valinnut kustannusobjektin dimensiohierarkian, laajenna kustannustason dimensiohierarkia ja katsele haluamiesi kustannusten arvoja.</span><span class="sxs-lookup"><span data-stu-id="09ce2-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="09ce2-136">Voit esimerkiksi laajentaa valmistuksen yleiskustannusten hierarkian, kun haluat tarkastella arvoa.</span><span class="sxs-lookup"><span data-stu-id="09ce2-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  


