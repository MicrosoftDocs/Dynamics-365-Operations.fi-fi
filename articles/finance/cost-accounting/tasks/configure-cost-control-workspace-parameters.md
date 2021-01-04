---
title: Määritä kustannusseurannan työtilan parametrit
description: Tämän menettelyn avulla voi määrittää kustannusseurannan työtilan niin, että organisaation eri tasojen esimiehet voivat tarkastella kustannusobjektejaan, kuten kustannuspaikkoja ja tuoteryhmiä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca05f6174541a6e97ec94db209a99424a87550eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442917"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="929cd-103">Määritä kustannusseurannan työtilan parametrit</span><span class="sxs-lookup"><span data-stu-id="929cd-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="929cd-104">Tämän menettelyn avulla voi määrittää kustannusseurannan työtilan niin, että organisaation eri tasojen esimiehet voivat tarkastella kustannusobjektejaan, kuten kustannuspaikkoja ja tuoteryhmiä.</span><span class="sxs-lookup"><span data-stu-id="929cd-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="929cd-105">Tämän tallenteen luomisessa käytetty demoyritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="929cd-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="929cd-106">Valitse Kustannuslaskenta > Asetukset > Kustannusseurannan työtilan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="929cd-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="929cd-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="929cd-107">Click New.</span></span>
3. <span data-ttu-id="929cd-108">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="929cd-109">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="929cd-110">Valitse Julkaistu-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="929cd-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="929cd-111">Jos määrität tämän asetuksen arvoksi Kyllä, käyttäjät, joille on delegoitu jokin näistä rooleista, näkevät raportin kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija, kustannuslaskijan apulainen tai kustannusobjektin vastuuhenkilö.</span><span class="sxs-lookup"><span data-stu-id="929cd-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="929cd-112">Jos määrität tämän asetuksen arvoksi Ei, vain käyttäjät, joille on delegoitu jokin näistä rooleista, näkevät raportin kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija tai kustannuslaskijan apulainen.</span><span class="sxs-lookup"><span data-stu-id="929cd-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="929cd-113">Laajenna Tietojen suodattaminen -osa.</span><span class="sxs-lookup"><span data-stu-id="929cd-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="929cd-114">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="929cd-115">Anna tai valitse arvo Budjetin alkuperäinen versio -kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="929cd-116">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="929cd-117">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="929cd-118">Laajenna Määritä laskentatietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="929cd-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="929cd-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="929cd-119">Click New.</span></span>
13. <span data-ttu-id="929cd-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="929cd-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="929cd-121">Syötä tai valitse arvo Kirjanpidon vuosikalenterin kausi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="929cd-122">Anna tai valitse arvo Todellinen versio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="929cd-123">Laajenna Tilikausia sarakkeessa -osa.</span><span class="sxs-lookup"><span data-stu-id="929cd-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="929cd-124">Valitse Nykyinen kausi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="929cd-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="929cd-125">Laajenna Kustannusten näytettävät sarakkeet -osa.</span><span class="sxs-lookup"><span data-stu-id="929cd-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="929cd-126">Valitse Kiinteä kustannus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="929cd-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="929cd-127">Valitse Muuttuva kustannus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="929cd-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="929cd-128">Valitse Kokonaiskustannukset-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="929cd-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="929cd-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="929cd-129">Click Save.</span></span>
23. <span data-ttu-id="929cd-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="929cd-130">Close the page.</span></span>
24. <span data-ttu-id="929cd-131">Valitse Kustannuslaskenta > Työtilat > Kustannusseuranta.</span><span class="sxs-lookup"><span data-stu-id="929cd-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="929cd-132">Valitse ilmoitus, kun haluat nähdä valittujen tilikausien kiinteät, muuttuvat ja luokittelemattomat kustannukset sekä kokonaiskustannukset.</span><span class="sxs-lookup"><span data-stu-id="929cd-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="929cd-133">Syötä tai valitse arvo Kirjanpidon vuosikalenterin kausi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="929cd-134">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="929cd-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="929cd-135">Kun olet valinnut kustannusobjektin dimensiohierarkian, laajenna kustannustason dimensiohierarkia ja katsele haluamiesi kustannusten arvoja.</span><span class="sxs-lookup"><span data-stu-id="929cd-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="929cd-136">Voit esimerkiksi laajentaa valmistuksen yleiskustannusten hierarkian, kun haluat tarkastella arvoa.</span><span class="sxs-lookup"><span data-stu-id="929cd-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

