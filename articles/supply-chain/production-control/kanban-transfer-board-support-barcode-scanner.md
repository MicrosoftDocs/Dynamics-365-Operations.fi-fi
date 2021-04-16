---
title: Kanban-siirron taulun tuki viivakoodinlukijoille
description: Kanban-siirron taulu tukee skannerin toimia aina pienoisohjelman viivakoodiskannerista kanban-työn valitsemiseen, käynnistämiseen, päättämiseen ja tyhjentämiseen.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a7073fb5d77e2d11569e86b92433864371f0e1d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825864"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="6d9e6-103">Kanban-siirron taulun tuki viivakoodinlukijoille</span><span class="sxs-lookup"><span data-stu-id="6d9e6-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d9e6-104">Kanban-siirron taulu tukee skannerin toimia aina pienoisohjelman viivakoodiskannerista kanban-työn valitsemiseen, käynnistämiseen, päättämiseen ja tyhjentämiseen.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="6d9e6-105">Rekisteröintitilat</span><span class="sxs-lookup"><span data-stu-id="6d9e6-105">Registration modes</span></span>
------------------

<span data-ttu-id="6d9e6-106">**Skannerin rekisteröinti** -pikavälilehdessä voit valita rekisteröintitilan, joka ohjaa toimintoa, kun skannaat kanban-kortin numeron tai kirjoitat numeron manuaalisesti Kanban-kortin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="6d9e6-107">Määritä rekisteröintitila</span><span class="sxs-lookup"><span data-stu-id="6d9e6-107">Set registration mode</span></span> | <span data-ttu-id="6d9e6-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6d9e6-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9e6-109">Aloitus</span><span class="sxs-lookup"><span data-stu-id="6d9e6-109">Start</span></span>                 | <span data-ttu-id="6d9e6-110">Rekisteröi Kanban-siirtotyön käsittelyssä olevaksi.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="6d9e6-111">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="6d9e6-111">Complete</span></span>              | <span data-ttu-id="6d9e6-112">Rekisteröi Kanban-siirtotyön valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="6d9e6-113">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-113">Empty</span></span>                 | <span data-ttu-id="6d9e6-114">Rekisteröi materiaalia käsittelevän yksikön, johon Kanban-kortti viittaa, tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="6d9e6-115">Valitse</span><span class="sxs-lookup"><span data-stu-id="6d9e6-115">Select</span></span>                | <span data-ttu-id="6d9e6-116">Rekisteröi Kanban-kortin numeron ja valitsee viitatun työn automaattisesti Kanban-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="6d9e6-117">Rekisteröintitilan valinta</span><span class="sxs-lookup"><span data-stu-id="6d9e6-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="6d9e6-118">Kun käytät viivakoodinlukijaa työn valintaan, kanban-taulun näyttötila muuttuu.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="6d9e6-119">Tässä tilassa seuraavien ehtojen on täytyttävä:</span><span class="sxs-lookup"><span data-stu-id="6d9e6-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="6d9e6-120">Vain skannattu kanban-työ tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="6d9e6-121">Valitun tehtävän tiedot näkyvät **Tiedot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="6d9e6-122">**Sanomat**-pikavälilehdessä näkyvät vain valitun työn sanomat.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="6d9e6-123">Voit muuttaa työn tilaa toimintoruudun toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="6d9e6-124">Kanban-siirron taulussa näkyy edelleen vain yksi työ.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="6d9e6-125">Voit päivittää tiedot työluetteloon manuaalisesti valitsemalla **Päivitä** (Vaihto+F5) toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="6d9e6-126">Kun olet päivittänyt tiedot, työn suodattimen kaikki tulokset näytetään uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="6d9e6-127">Työn tila ja mahdolliset toiminnot</span><span class="sxs-lookup"><span data-stu-id="6d9e6-127">Job status and possible actions</span></span>
<span data-ttu-id="6d9e6-128">Valitun työn tila sekä tapahtumien kanbanien tarvekohdistettujen töiden tila määrittävät, voidaanko työtä käsitellä lisää.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="6d9e6-129">Seuraavassa taulukossa on tietoja näistä tiloista ja tehtävistä:</span><span class="sxs-lookup"><span data-stu-id="6d9e6-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="6d9e6-130">Töille tai niiden viittaamille käsittely-yksiköille valittavissa olevat tilat.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="6d9e6-131">Työlle suoritettavissa olevat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="6d9e6-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d9e6-132">Työlaji</span><span class="sxs-lookup"><span data-stu-id="6d9e6-132">Job type</span></span></th>
<th><span data-ttu-id="6d9e6-133">Työn tila tai käsittely-yksikön tila</span><span class="sxs-lookup"><span data-stu-id="6d9e6-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="6d9e6-134">Päivitä keräysluettelo</span><span class="sxs-lookup"><span data-stu-id="6d9e6-134">Update picking list</span></span></th>
<th><span data-ttu-id="6d9e6-135">Aloitus</span><span class="sxs-lookup"><span data-stu-id="6d9e6-135">Start</span></span></th>
<th><span data-ttu-id="6d9e6-136">Päivitä rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="6d9e6-136">Update registration</span></span></th>
<th><span data-ttu-id="6d9e6-137">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="6d9e6-137">Complete</span></span></th>
<th><span data-ttu-id="6d9e6-138">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-138">Empty</span></span></th>
<th><span data-ttu-id="6d9e6-139">Luo tapahtuma-kanbaneita</span><span class="sxs-lookup"><span data-stu-id="6d9e6-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d9e6-140">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="6d9e6-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="6d9e6-141">Ei suunniteltu</span><span class="sxs-lookup"><span data-stu-id="6d9e6-141">Not planned</span></span></li>
<li><span data-ttu-id="6d9e6-142">Ei tarvekohdistettuja töitä, tai tarvekohdistetut työt on suoritettu</span><span class="sxs-lookup"><span data-stu-id="6d9e6-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="6d9e6-143">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-143">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-144">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-144">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-145">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-145">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-146">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-146">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-147">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-147">No</span></span></td>
<td><span data-ttu-id="6d9e6-148">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d9e6-149">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="6d9e6-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="6d9e6-150">Ei suunniteltu</span><span class="sxs-lookup"><span data-stu-id="6d9e6-150">Not planned</span></span></li>
<li><span data-ttu-id="6d9e6-151">Tarvekohdistettu työ on kesken</span><span class="sxs-lookup"><span data-stu-id="6d9e6-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="6d9e6-152">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-152">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-153">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-153">No</span></span></td>
<td><span data-ttu-id="6d9e6-154">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-154">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-155">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-155">No</span></span></td>
<td><span data-ttu-id="6d9e6-156">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-156">No</span></span></td>
<td><span data-ttu-id="6d9e6-157">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d9e6-158">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="6d9e6-158">Transfer</span></span></td>
<td><span data-ttu-id="6d9e6-159">Käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-159">In progress</span></span></td>
<td><span data-ttu-id="6d9e6-160">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-160">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-161">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-161">No</span></span></td>
<td><span data-ttu-id="6d9e6-162">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-162">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-163">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-163">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-164">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-164">No</span></span></td>
<td><span data-ttu-id="6d9e6-165">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d9e6-166">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="6d9e6-166">Transfer</span></span></td>
<td><span data-ttu-id="6d9e6-167">Valmis</span><span class="sxs-lookup"><span data-stu-id="6d9e6-167">Completed</span></span></td>
<td><span data-ttu-id="6d9e6-168">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-168">No</span></span></td>
<td><span data-ttu-id="6d9e6-169">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-169">No</span></span></td>
<td><span data-ttu-id="6d9e6-170">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-170">No</span></span></td>
<td><span data-ttu-id="6d9e6-171">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-171">No</span></span></td>
<td><span data-ttu-id="6d9e6-172">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-172">Yes</span></span></td>
<td><span data-ttu-id="6d9e6-173">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d9e6-174">Siirto tai käsittely</span><span class="sxs-lookup"><span data-stu-id="6d9e6-174">Transfer or process</span></span></td>
<td><span data-ttu-id="6d9e6-175">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-175">Empty</span></span></td>
<td><span data-ttu-id="6d9e6-176">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-176">No</span></span></td>
<td><span data-ttu-id="6d9e6-177">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-177">No</span></span></td>
<td><span data-ttu-id="6d9e6-178">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-178">No</span></span></td>
<td><span data-ttu-id="6d9e6-179">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-179">No</span></span></td>
<td><span data-ttu-id="6d9e6-180">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-180">No</span></span></td>
<td><span data-ttu-id="6d9e6-181">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d9e6-182">Siirto tai käsittely</span><span class="sxs-lookup"><span data-stu-id="6d9e6-182">Transfer or process</span></span></td>
<td><span data-ttu-id="6d9e6-183">Kanban-korttia ei löydy</span><span class="sxs-lookup"><span data-stu-id="6d9e6-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="6d9e6-184">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-184">No</span></span></td>
<td><span data-ttu-id="6d9e6-185">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-185">No</span></span></td>
<td><span data-ttu-id="6d9e6-186">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-186">No</span></span></td>
<td><span data-ttu-id="6d9e6-187">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-187">No</span></span></td>
<td><span data-ttu-id="6d9e6-188">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-188">No</span></span></td>
<td><span data-ttu-id="6d9e6-189">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d9e6-190">Siirto tai käsittely</span><span class="sxs-lookup"><span data-stu-id="6d9e6-190">Transfer or process</span></span></td>
<td><span data-ttu-id="6d9e6-191">Kanban-kortti löytyy, mutta sitä ei ole liitetty kanbaniin</span><span class="sxs-lookup"><span data-stu-id="6d9e6-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="6d9e6-192">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-192">No</span></span></td>
<td><span data-ttu-id="6d9e6-193">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-193">No</span></span></td>
<td><span data-ttu-id="6d9e6-194">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-194">No</span></span></td>
<td><span data-ttu-id="6d9e6-195">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-195">No</span></span></td>
<td><span data-ttu-id="6d9e6-196">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-196">No</span></span></td>
<td><span data-ttu-id="6d9e6-197">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d9e6-198">Prosessoi</span><span class="sxs-lookup"><span data-stu-id="6d9e6-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="6d9e6-199">Ei suunniteltu</span><span class="sxs-lookup"><span data-stu-id="6d9e6-199">Not planned</span></span></li>
<li><span data-ttu-id="6d9e6-200">Valmisteltu</span><span class="sxs-lookup"><span data-stu-id="6d9e6-200">Prepared</span></span></li>
<li><span data-ttu-id="6d9e6-201">Käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="6d9e6-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="6d9e6-202">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-202">No</span></span></td>
<td><span data-ttu-id="6d9e6-203">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-203">No</span></span></td>
<td><span data-ttu-id="6d9e6-204">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-204">No</span></span></td>
<td><span data-ttu-id="6d9e6-205">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-205">No</span></span></td>
<td><span data-ttu-id="6d9e6-206">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-206">No</span></span></td>
<td><span data-ttu-id="6d9e6-207">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d9e6-208">Prosessoi</span><span class="sxs-lookup"><span data-stu-id="6d9e6-208">Process</span></span></td>
<td><span data-ttu-id="6d9e6-209">Valmis</span><span class="sxs-lookup"><span data-stu-id="6d9e6-209">Completed</span></span></td>
<td><span data-ttu-id="6d9e6-210">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-210">No</span></span></td>
<td><span data-ttu-id="6d9e6-211">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-211">No</span></span></td>
<td><span data-ttu-id="6d9e6-212">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-212">No</span></span></td>
<td><span data-ttu-id="6d9e6-213">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-213">No</span></span></td>
<td><span data-ttu-id="6d9e6-214">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-214">No</span></span></td>
<td><span data-ttu-id="6d9e6-215">Ei</span><span class="sxs-lookup"><span data-stu-id="6d9e6-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]