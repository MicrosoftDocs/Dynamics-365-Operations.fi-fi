---
title: Kanban-siirron taulun tuki viivakoodinlukijoille
description: "Kanban-siirron taulu tukee skannerin toimia aina pienoisohjelman viivakoodiskannerista kanban-työn valitsemiseen, käynnistämiseen, päättämiseen ja tyhjentämiseen."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 29ad077cd10b0fa5967d145740f63051b05ad009
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="a1731-103">Kanban-siirron taulun tuki viivakoodinlukijoille</span><span class="sxs-lookup"><span data-stu-id="a1731-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1731-104">Kanban-siirron taulu tukee skannerin toimia aina pienoisohjelman viivakoodiskannerista kanban-työn valitsemiseen, käynnistämiseen, päättämiseen ja tyhjentämiseen.</span><span class="sxs-lookup"><span data-stu-id="a1731-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="a1731-105">Rekisteröintitilat</span><span class="sxs-lookup"><span data-stu-id="a1731-105">Registration modes</span></span>
------------------

<span data-ttu-id="a1731-106">**Skannerin rekisteröinti** -pikavälilehdessä voit valita rekisteröintitilan, joka ohjaa toimintoa, kun skannaat kanban-kortin numeron tai kirjoitat numeron manuaalisesti Kanban-kortin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a1731-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="a1731-107">Määritä rekisteröintitila</span><span class="sxs-lookup"><span data-stu-id="a1731-107">Set registration mode</span></span> | <span data-ttu-id="a1731-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a1731-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1731-109">Aloitus</span><span class="sxs-lookup"><span data-stu-id="a1731-109">Start</span></span>                 | <span data-ttu-id="a1731-110">Rekisteröi Kanban-siirtotyön käsittelyssä olevaksi.</span><span class="sxs-lookup"><span data-stu-id="a1731-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="a1731-111">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="a1731-111">Complete</span></span>              | <span data-ttu-id="a1731-112">Rekisteröi Kanban-siirtotyön valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="a1731-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="a1731-113">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="a1731-113">Empty</span></span>                 | <span data-ttu-id="a1731-114">Rekisteröi materiaalia käsittelevän yksikön, johon Kanban-kortti viittaa, tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="a1731-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="a1731-115">Valitse</span><span class="sxs-lookup"><span data-stu-id="a1731-115">Select</span></span>                | <span data-ttu-id="a1731-116">Rekisteröi Kanban-kortin numeron ja valitsee viitatun työn automaattisesti Kanban-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="a1731-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="a1731-117">Rekisteröintitilan valinta</span><span class="sxs-lookup"><span data-stu-id="a1731-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="a1731-118">Kun käytät viivakoodinlukijaa työn valintaan, kanban-taulun näyttötila muuttuu.</span><span class="sxs-lookup"><span data-stu-id="a1731-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="a1731-119">Tässä tilassa seuraavien ehtojen on täytyttävä:</span><span class="sxs-lookup"><span data-stu-id="a1731-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="a1731-120">Vain skannattu kanban-työ tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="a1731-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="a1731-121">Valitun tehtävän tiedot näkyvät **Tiedot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a1731-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="a1731-122">**Sanomat**-pikavälilehdessä näkyvät vain valitun työn sanomat.</span><span class="sxs-lookup"><span data-stu-id="a1731-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="a1731-123">Voit muuttaa työn tilaa toimintoruudun toiminnoilla.</span><span class="sxs-lookup"><span data-stu-id="a1731-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="a1731-124">Kanban-siirron taulussa näkyy edelleen vain yksi työ.</span><span class="sxs-lookup"><span data-stu-id="a1731-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="a1731-125">Voit päivittää tiedot työluetteloon manuaalisesti valitsemalla **Päivitä** (Vaihto+F5) toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="a1731-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="a1731-126">Kun olet päivittänyt tiedot, työn suodattimen kaikki tulokset näytetään uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a1731-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="a1731-127">Työn tila ja mahdolliset toiminnot</span><span class="sxs-lookup"><span data-stu-id="a1731-127">Job status and possible actions</span></span>
<span data-ttu-id="a1731-128">Valitun työn tila sekä tapahtumien kanbanien tarvekohdistettujen töiden tila määrittävät, voidaanko työtä käsitellä lisää.</span><span class="sxs-lookup"><span data-stu-id="a1731-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="a1731-129">Seuraavassa taulukossa on tietoja näistä tiloista ja tehtävistä:</span><span class="sxs-lookup"><span data-stu-id="a1731-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="a1731-130">Töille tai niiden viittaamille käsittely-yksiköille valittavissa olevat tilat.</span><span class="sxs-lookup"><span data-stu-id="a1731-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="a1731-131">Työlle suoritettavissa olevat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="a1731-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="a1731-132">Työlaji</span><span class="sxs-lookup"><span data-stu-id="a1731-132">Job type</span></span></th>
<th><span data-ttu-id="a1731-133">Työn tila tai käsittely-yksikön tila</span><span class="sxs-lookup"><span data-stu-id="a1731-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="a1731-134">Päivitä keräysluettelo</span><span class="sxs-lookup"><span data-stu-id="a1731-134">Update picking list</span></span></th>
<th><span data-ttu-id="a1731-135">Aloitus</span><span class="sxs-lookup"><span data-stu-id="a1731-135">Start</span></span></th>
<th><span data-ttu-id="a1731-136">Päivitä rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="a1731-136">Update registration</span></span></th>
<th><span data-ttu-id="a1731-137">Täydellinen</span><span class="sxs-lookup"><span data-stu-id="a1731-137">Complete</span></span></th>
<th><span data-ttu-id="a1731-138">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="a1731-138">Empty</span></span></th>
<th><span data-ttu-id="a1731-139">Luo tapahtuma-kanbaneita</span><span class="sxs-lookup"><span data-stu-id="a1731-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1731-140">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="a1731-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="a1731-141">Ei suunniteltu</span><span class="sxs-lookup"><span data-stu-id="a1731-141">Not planned</span></span></li>
<li><span data-ttu-id="a1731-142">Ei tarvekohdistettuja töitä, tai tarvekohdistetut työt on suoritettu</span><span class="sxs-lookup"><span data-stu-id="a1731-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="a1731-143">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-143">Yes</span></span></td>
<td><span data-ttu-id="a1731-144">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-144">Yes</span></span></td>
<td><span data-ttu-id="a1731-145">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-145">Yes</span></span></td>
<td><span data-ttu-id="a1731-146">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-146">Yes</span></span></td>
<td><span data-ttu-id="a1731-147">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-147">No</span></span></td>
<td><span data-ttu-id="a1731-148">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1731-149">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="a1731-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="a1731-150">Ei suunniteltu</span><span class="sxs-lookup"><span data-stu-id="a1731-150">Not planned</span></span></li>
<li><span data-ttu-id="a1731-151">Tarvekohdistettu työ on kesken</span><span class="sxs-lookup"><span data-stu-id="a1731-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="a1731-152">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-152">Yes</span></span></td>
<td><span data-ttu-id="a1731-153">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-153">No</span></span></td>
<td><span data-ttu-id="a1731-154">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-154">Yes</span></span></td>
<td><span data-ttu-id="a1731-155">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-155">No</span></span></td>
<td><span data-ttu-id="a1731-156">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-156">No</span></span></td>
<td><span data-ttu-id="a1731-157">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1731-158">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="a1731-158">Transfer</span></span></td>
<td><span data-ttu-id="a1731-159">Käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="a1731-159">In progress</span></span></td>
<td><span data-ttu-id="a1731-160">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-160">Yes</span></span></td>
<td><span data-ttu-id="a1731-161">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-161">No</span></span></td>
<td><span data-ttu-id="a1731-162">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-162">Yes</span></span></td>
<td><span data-ttu-id="a1731-163">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-163">Yes</span></span></td>
<td><span data-ttu-id="a1731-164">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-164">No</span></span></td>
<td><span data-ttu-id="a1731-165">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1731-166">Varastosiirto</span><span class="sxs-lookup"><span data-stu-id="a1731-166">Transfer</span></span></td>
<td><span data-ttu-id="a1731-167">Valmis</span><span class="sxs-lookup"><span data-stu-id="a1731-167">Completed</span></span></td>
<td><span data-ttu-id="a1731-168">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-168">No</span></span></td>
<td><span data-ttu-id="a1731-169">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-169">No</span></span></td>
<td><span data-ttu-id="a1731-170">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-170">No</span></span></td>
<td><span data-ttu-id="a1731-171">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-171">No</span></span></td>
<td><span data-ttu-id="a1731-172">Kyllä</span><span class="sxs-lookup"><span data-stu-id="a1731-172">Yes</span></span></td>
<td><span data-ttu-id="a1731-173">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1731-174">Siirto tai käsittely</span><span class="sxs-lookup"><span data-stu-id="a1731-174">Transfer or process</span></span></td>
<td><span data-ttu-id="a1731-175">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="a1731-175">Empty</span></span></td>
<td><span data-ttu-id="a1731-176">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-176">No</span></span></td>
<td><span data-ttu-id="a1731-177">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-177">No</span></span></td>
<td><span data-ttu-id="a1731-178">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-178">No</span></span></td>
<td><span data-ttu-id="a1731-179">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-179">No</span></span></td>
<td><span data-ttu-id="a1731-180">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-180">No</span></span></td>
<td><span data-ttu-id="a1731-181">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1731-182">Siirto tai käsittely</span><span class="sxs-lookup"><span data-stu-id="a1731-182">Transfer or process</span></span></td>
<td><span data-ttu-id="a1731-183">Kanban-korttia ei löydy</span><span class="sxs-lookup"><span data-stu-id="a1731-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="a1731-184">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-184">No</span></span></td>
<td><span data-ttu-id="a1731-185">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-185">No</span></span></td>
<td><span data-ttu-id="a1731-186">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-186">No</span></span></td>
<td><span data-ttu-id="a1731-187">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-187">No</span></span></td>
<td><span data-ttu-id="a1731-188">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-188">No</span></span></td>
<td><span data-ttu-id="a1731-189">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1731-190">Siirto tai käsittely</span><span class="sxs-lookup"><span data-stu-id="a1731-190">Transfer or process</span></span></td>
<td><span data-ttu-id="a1731-191">Kanban-kortti löytyy, mutta sitä ei ole liitetty kanbaniin</span><span class="sxs-lookup"><span data-stu-id="a1731-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="a1731-192">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-192">No</span></span></td>
<td><span data-ttu-id="a1731-193">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-193">No</span></span></td>
<td><span data-ttu-id="a1731-194">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-194">No</span></span></td>
<td><span data-ttu-id="a1731-195">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-195">No</span></span></td>
<td><span data-ttu-id="a1731-196">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-196">No</span></span></td>
<td><span data-ttu-id="a1731-197">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1731-198">Prosessoi</span><span class="sxs-lookup"><span data-stu-id="a1731-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="a1731-199">Ei suunniteltu</span><span class="sxs-lookup"><span data-stu-id="a1731-199">Not planned</span></span></li>
<li><span data-ttu-id="a1731-200">Valmisteltu</span><span class="sxs-lookup"><span data-stu-id="a1731-200">Prepared</span></span></li>
<li><span data-ttu-id="a1731-201">Käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="a1731-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="a1731-202">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-202">No</span></span></td>
<td><span data-ttu-id="a1731-203">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-203">No</span></span></td>
<td><span data-ttu-id="a1731-204">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-204">No</span></span></td>
<td><span data-ttu-id="a1731-205">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-205">No</span></span></td>
<td><span data-ttu-id="a1731-206">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-206">No</span></span></td>
<td><span data-ttu-id="a1731-207">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1731-208">Prosessoi</span><span class="sxs-lookup"><span data-stu-id="a1731-208">Process</span></span></td>
<td><span data-ttu-id="a1731-209">Valmis</span><span class="sxs-lookup"><span data-stu-id="a1731-209">Completed</span></span></td>
<td><span data-ttu-id="a1731-210">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-210">No</span></span></td>
<td><span data-ttu-id="a1731-211">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-211">No</span></span></td>
<td><span data-ttu-id="a1731-212">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-212">No</span></span></td>
<td><span data-ttu-id="a1731-213">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-213">No</span></span></td>
<td><span data-ttu-id="a1731-214">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-214">No</span></span></td>
<td><span data-ttu-id="a1731-215">Ei</span><span class="sxs-lookup"><span data-stu-id="a1731-215">No</span></span></td>
</tr>
</tbody>
</table>






