--- 
title: "Toimien määrittäminen"
description: "Toimet ovat organisaatiohierarkian alemman tason tärkeä osa."
author: DarinKramer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5d69e6b926a047888a162dae1cdc870718d8f945
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-positions"></a><span data-ttu-id="76074-103">Toimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="76074-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76074-104">Toimet ovat organisaatiohierarkian alemman tason tärkeä osa.</span><span class="sxs-lookup"><span data-stu-id="76074-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="76074-105">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="76074-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="76074-106">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="76074-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="76074-107">Toimi sijoittuu osastoille, ja sen voi määrittää vain yhdelle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="76074-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="76074-108">Tässä tehtävässä käydään läpi toimen luomiseen vaadittavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="76074-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="76074-109">Menettely on tarkoitettu henkilöstöhallinnon asiantuntijalle.</span><span class="sxs-lookup"><span data-stu-id="76074-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="76074-110">Valitse Työvoiman hallinta.</span><span class="sxs-lookup"><span data-stu-id="76074-110">Click Workforce management.</span></span>
2. <span data-ttu-id="76074-111">Napsauta Avoimet toimet.</span><span class="sxs-lookup"><span data-stu-id="76074-111">Click Open positions.</span></span>
3. <span data-ttu-id="76074-112">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="76074-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="76074-113">Syötä tai valitse arvo Työ-kenttään.</span><span class="sxs-lookup"><span data-stu-id="76074-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="76074-114">Työnkuvauksen otsikko ja kokopäivätyötä vastaava työsuhdekerroin kopioidaan automaattisesti valitusta työstä oikeaan kohtaan.</span><span class="sxs-lookup"><span data-stu-id="76074-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="76074-115">Ratkaise muutokset työssä.</span><span class="sxs-lookup"><span data-stu-id="76074-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="76074-116">Napsauta Luo toimi.</span><span class="sxs-lookup"><span data-stu-id="76074-116">Click Create position.</span></span>
7. <span data-ttu-id="76074-117">Syötä tai valitse Osasto-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="76074-118">Anna tai valitse Toimityyppi-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="76074-119">Syötä tai valitse Kompensaatioalue-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="76074-120">Kompensaatioalue-kenttä määrittää kompensaation oikeutussäännöt ja kiinteät lisäysbudjetit, jotka koskevat kyseisessä toimessa olevaa työntekijää.</span><span class="sxs-lookup"><span data-stu-id="76074-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="76074-121">Syötä päivämäärä ja kellonaika Käytettävissä toimeksiantoa varten -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76074-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="76074-122">Laajenna Toimen kesto -osa.</span><span class="sxs-lookup"><span data-stu-id="76074-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="76074-123">Toimen kesto syötetään oletusarvoisesti aiemmin annettujen aktivointi- ja päättymispäivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="76074-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="76074-124">Laajenna Raportoi toimelle -osa.</span><span class="sxs-lookup"><span data-stu-id="76074-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="76074-125">Kun määrität työntekijän toimeen, joka raportoi toiselle toimelle, luot näihin kahteen toimeen määritettyjen työntekijöiden välisen suoran raportointisuhteen.</span><span class="sxs-lookup"><span data-stu-id="76074-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="76074-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="76074-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="76074-127">Anna tai valitse Raportoi:-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="76074-128">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="76074-128">Click Create.</span></span>
16. <span data-ttu-id="76074-129">Laajenna Työntekijän tehtävä -osa.</span><span class="sxs-lookup"><span data-stu-id="76074-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="76074-130">Laajenna Suhteet-osa.</span><span class="sxs-lookup"><span data-stu-id="76074-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="76074-131">Jos organisaatio käyttää matriisihierarkiaan tai jotakin toista mukautettua hierarkiaa, voit määrittää toimien hierarkiatyypit ja lisätä sitten toimiin raportointisuhteet jokaiselle määrittämällesi hierarkiatyypille.</span><span class="sxs-lookup"><span data-stu-id="76074-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="76074-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="76074-132">Click Add.</span></span>
19. <span data-ttu-id="76074-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="76074-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="76074-134">Anna tai valitse Hierarkian nimi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="76074-135">Anna tai valitse Raportoi toimelle -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="76074-136">Laajenna Palkanlaskenta-osa.</span><span class="sxs-lookup"><span data-stu-id="76074-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="76074-137">Syötä tai valitse arvo Maksujakso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="76074-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="76074-138">Syötä tai valitse Maksaja-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="76074-139">Lisää Vuosittaiset vakiotunnit -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="76074-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="76074-140">Tämä on säännöllisesti maksettujen työtuntien määrä, jonka toimessa olevan työntekijän odotetaan työskentelevän vuosittain.</span><span class="sxs-lookup"><span data-stu-id="76074-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="76074-141">Laajenna Ammattijärjestö-osa.</span><span class="sxs-lookup"><span data-stu-id="76074-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="76074-142">Tiivistä Ammattijärjestö-osa.</span><span class="sxs-lookup"><span data-stu-id="76074-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="76074-143">Laajenna Taloushallinnon dimensiot -osa.</span><span class="sxs-lookup"><span data-stu-id="76074-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="76074-144">Syötä tai valitse Jakomalli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="76074-145">Syötä tai valitse Osasto-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="76074-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="76074-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="76074-146">Click Save.</span></span>


