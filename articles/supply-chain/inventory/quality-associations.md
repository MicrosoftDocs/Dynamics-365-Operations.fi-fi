---
title: Laatuliitokset
description: Tässä aiheessa kuvataan, kuinka voit käyttää laatuliitoksia Microsoft Dynamics 365 Supply Chain Managementissa luodaksesi automaattisesti myynti-, osto- ja tuotantoprosesseihin liittyviä laatutilauksia.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956636"
---
# <a name="quality-associations"></a><span data-ttu-id="8ec97-103">Laatuliitokset</span><span class="sxs-lookup"><span data-stu-id="8ec97-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ec97-104">Tässä aiheessa kuvataan, kuinka voit käyttää laatuliitoksia Microsoft Dynamics 365 Supply Chain Managementissa luodaksesi automaattisesti myynti-, osto- ja tuotantoprosesseihin liittyviä laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="8ec97-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="8ec97-105">Laatuliitos määrittää kaikki seuraavat muodostettavan laatutilauksen tiedot:</span><span class="sxs-lookup"><span data-stu-id="8ec97-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="8ec97-106">Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="8ec97-106">The transaction event</span></span>
- <span data-ttu-id="8ec97-107">Nimikkeissä suoritettavat testit</span><span class="sxs-lookup"><span data-stu-id="8ec97-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="8ec97-108">Hyväksyttävän laadun taso (AQL)</span><span class="sxs-lookup"><span data-stu-id="8ec97-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="8ec97-109">Otantasuunnitelma</span><span class="sxs-lookup"><span data-stu-id="8ec97-109">The sampling plan</span></span>

<span data-ttu-id="8ec97-110">Laatuliitos on määritettävä kutakin sellaista liiketoimintaprosessin muutosta varten, joka edellyttää automaattista laatutilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="8ec97-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="8ec97-111">Laatutilaus voidaan esimerkiksi muodostaa ostotilausten, karanteenitilausten, myyntitilausten ja tuotantotilausten liiketoimintaprosesseille.</span><span class="sxs-lookup"><span data-stu-id="8ec97-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="8ec97-112">Laatuliitosten käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="8ec97-112">Working with quality associations</span></span>

<span data-ttu-id="8ec97-113">Laatuliitosta käyttävä liiketoimintoprosessi voidaan liittää eri lähdeasiakirjoihin, kuten ostotilauksiin, myyntitilauksiin tai tuotantotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="8ec97-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="8ec97-114">Jokaisessa laatuliitostietueessa määritetään joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, jota käytetään muodostettavissa laatutilauksissa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="8ec97-115">Laatuliitostietue on määritettävä liiketoimintaprosessin jokaiselle muunnokselle.</span><span class="sxs-lookup"><span data-stu-id="8ec97-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="8ec97-116">Voit esimerkiksi määrittää laatuliitoksen, joka muodostaa laatutilauksen, kun ostotilauksen tuotteen vastaanotto päivitetään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="8ec97-117">Toimeenpanosuunnitelman asetusten mukaan itse käynnistysprosessi voidaan estää avoimen laatutilauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8ec97-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="8ec97-118">Vaihtoehtoisesti seuraavat prosessit, kuten ostotilauksen laskutus, voidaan estää.</span><span class="sxs-lookup"><span data-stu-id="8ec97-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="8ec97-119">Jos laatutilauksia on avoinna, varastomäärien otto estetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="8ec97-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="8ec97-120">**Nimikeotanta**-sivun **Täysi esto** -kentän mukaan laatu on joko laatutilauksen määrä tai lähdeasiakirjan rivin määrä.</span><span class="sxs-lookup"><span data-stu-id="8ec97-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="8ec97-121">Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="8ec97-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="8ec97-122">Tietyn liiketoimintaprosessin laatuliitostietue tunnistaa tapahtuman ja ehdot, joille laatutilaus muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="8ec97-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="8ec97-123">Ehdot voivat olla joko toimipaikka- tai yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="8ec97-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="8ec97-124">Tuhoavia testejä sisältävä laatutilaus voidaan muodostaa vain, kun tapahtumalla on käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="8ec97-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="8ec97-125">Voit käyttää laatuliitoksia valitsemalla **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laatuliitokset**.</span><span class="sxs-lookup"><span data-stu-id="8ec97-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="8ec97-126">Seuraavassa esimerkeissä käsitellään, miten laatuliitostietue määritetään kunkin liiketoimintaprosessin variaatioille.</span><span class="sxs-lookup"><span data-stu-id="8ec97-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="8ec97-127">Seuraavassa taulussa on jokaisen esimerkin yhteenveto laatuliitostietueessa määritetyistä tapahtumista ja ehdoista.</span><span class="sxs-lookup"><span data-stu-id="8ec97-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ec97-128">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="8ec97-128">Reference type</span></span></th>
<th><span data-ttu-id="8ec97-129">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="8ec97-129">Event type</span></span></th>
<th><span data-ttu-id="8ec97-130">Suoritus</span><span class="sxs-lookup"><span data-stu-id="8ec97-130">Execution</span></span></th>
<th><span data-ttu-id="8ec97-131">Tapahtuman esto</span><span class="sxs-lookup"><span data-stu-id="8ec97-131">Event blocking</span></span></th>
<th><span data-ttu-id="8ec97-132">Tiedostoviite</span><span class="sxs-lookup"><span data-stu-id="8ec97-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ec97-133">Varasto</span><span class="sxs-lookup"><span data-stu-id="8ec97-133">Inventory</span></span></td>
<td><span data-ttu-id="8ec97-134">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8ec97-134">Not applicable</span></span></td>
<td><span data-ttu-id="8ec97-135">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8ec97-135">Not applicable</span></span></td>
<td><span data-ttu-id="8ec97-136">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-136">None</span></span></td>
<td><span data-ttu-id="8ec97-137">Kaikki</span><span class="sxs-lookup"><span data-stu-id="8ec97-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="8ec97-138">Myynti</span><span class="sxs-lookup"><span data-stu-id="8ec97-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="8ec97-139">Keräysprosessi on ajoitettu</span><span class="sxs-lookup"><span data-stu-id="8ec97-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="8ec97-140">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-140">Before</span></span></td>
<td><span data-ttu-id="8ec97-141">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="8ec97-142">Tietty tunnus, ryhmä tai vain kaikki</span><span class="sxs-lookup"><span data-stu-id="8ec97-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-143">Keräysprosessi</span><span class="sxs-lookup"><span data-stu-id="8ec97-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-144">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="8ec97-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-145">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8ec97-146">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="8ec97-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-147">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-147">Before</span></span></td>
<td><span data-ttu-id="8ec97-148">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-149">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="8ec97-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-150">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="8ec97-151">Osto</span><span class="sxs-lookup"><span data-stu-id="8ec97-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="8ec97-152">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="8ec97-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="8ec97-153">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-153">Before</span></span></td>
<td><span data-ttu-id="8ec97-154">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-155">Vastaanottoluettelo</span><span class="sxs-lookup"><span data-stu-id="8ec97-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-156">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="8ec97-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-157">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8ec97-158">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-158">After</span></span></td>
<td><span data-ttu-id="8ec97-159">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-160">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="8ec97-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-161">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8ec97-162">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="8ec97-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-163">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8ec97-163">Not applicable</span></span></td>
<td><span data-ttu-id="8ec97-164">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-165">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="8ec97-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-166">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8ec97-167">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="8ec97-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-168">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-168">Before</span></span></td>
<td><span data-ttu-id="8ec97-169">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-170">Tuotteen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="8ec97-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-171">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8ec97-172">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-172">After</span></span></td>
<td><span data-ttu-id="8ec97-173">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-174">Lasku</span><span class="sxs-lookup"><span data-stu-id="8ec97-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="8ec97-175">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="8ec97-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-176">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="8ec97-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-177">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8ec97-177">Not applicable</span></span></td>
<td><span data-ttu-id="8ec97-178">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="8ec97-179">Kaikki</span><span class="sxs-lookup"><span data-stu-id="8ec97-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-180">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-181">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8ec97-182">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-183">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-183">Before</span></span></td>
<td><span data-ttu-id="8ec97-184">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-185">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-186">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8ec97-187">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-187">After</span></span></td>
<td><span data-ttu-id="8ec97-188">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8ec97-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-189">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="8ec97-190">Karanteeni</span><span class="sxs-lookup"><span data-stu-id="8ec97-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-191">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="8ec97-192">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-192">Before</span></span></td>
<td><span data-ttu-id="8ec97-193">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-194">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-195">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-195">After</span></span></td>
<td><span data-ttu-id="8ec97-196">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-197">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-197">End</span></span></td>
<td><span data-ttu-id="8ec97-198">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-198">Before</span></span></td>
<td><span data-ttu-id="8ec97-199">Lopeta</span><span class="sxs-lookup"><span data-stu-id="8ec97-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8ec97-200">Reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="8ec97-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-201">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="8ec97-202">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-202">Before</span></span></td>
<td><span data-ttu-id="8ec97-203">None</span><span class="sxs-lookup"><span data-stu-id="8ec97-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-204">Tietty tunnus, ryhmä tai kaikki tai tietty resurssi, ryhmä tai kaikki</span><span class="sxs-lookup"><span data-stu-id="8ec97-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-205">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-206">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-206">After</span></span></td>
<td><span data-ttu-id="8ec97-207">None</span><span class="sxs-lookup"><span data-stu-id="8ec97-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8ec97-208">Oheistuotteen tuotanto</span><span class="sxs-lookup"><span data-stu-id="8ec97-208">Co-product production</span></span></td>
<td><span data-ttu-id="8ec97-209">Rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="8ec97-209">Registration</span></span></td>
<td><span data-ttu-id="8ec97-210">Ei käytettävissä</span><span class="sxs-lookup"><span data-stu-id="8ec97-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-211">None</span><span class="sxs-lookup"><span data-stu-id="8ec97-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="8ec97-212">Kaikki</span><span class="sxs-lookup"><span data-stu-id="8ec97-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8ec97-213">Ilmoita valmiiksi</span><span class="sxs-lookup"><span data-stu-id="8ec97-213">Report as finished</span></span></td>
<td><span data-ttu-id="8ec97-214">Ennen</span><span class="sxs-lookup"><span data-stu-id="8ec97-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-215">Jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8ec97-216">*Varastoprosessien laadunhallinta* -ominaisuus lisää laatutilausten käsittelytoiminnot tuotannoille, joiden **Tapahtumatyyppi**-kentän arvona on *Ilmoita valmiiksi* ja **Suoritus**-kenttä on määritetty arvoon *Jälkeen*, sekä ostoille, joiden **Tapahtumatyyppi**-kentän arvona on *Rekisteröinti*.</span><span class="sxs-lookup"><span data-stu-id="8ec97-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="8ec97-217">Lisätietoja on kohdassa [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="8ec97-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="8ec97-218">Seuraavassa taulussa on lisätietoja laatutilausten muodostamisesta tietyntyyppisille prosesseille.</span><span class="sxs-lookup"><span data-stu-id="8ec97-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="8ec97-219">Prosessin tyyppi</span><span class="sxs-lookup"><span data-stu-id="8ec97-219">Type of process</span></span></th>
<th><span data-ttu-id="8ec97-220">Laatutilausten automaattinen luontiajankohta</span><span class="sxs-lookup"><span data-stu-id="8ec97-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="8ec97-221">Laatutilausten luontiajankohta, jos tuhoava testaus pakollinen</span><span class="sxs-lookup"><span data-stu-id="8ec97-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="8ec97-222">Ehdon tiedot</span><span class="sxs-lookup"><span data-stu-id="8ec97-222">Condition information</span></span></th>
<th><span data-ttu-id="8ec97-223">Manuaalisen luonnin tiedot</span><span class="sxs-lookup"><span data-stu-id="8ec97-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ec97-224">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="8ec97-224">Purchase order</span></span></td>
<td><span data-ttu-id="8ec97-225">Ennen kuin vastaanotetun materiaalin vastaanottoluettelo tai tuotteen vastaanotto on kirjattu tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="8ec97-226">Vastaanotetun materiaalin tuotteen vastaanoton kirjauksen jälkeen, koska materiaalin on oltava käytettävissä tuhoavaa testausta varten</span><span class="sxs-lookup"><span data-stu-id="8ec97-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="8ec97-227">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8ec97-228">Manuaalisesti luotu ostotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-229">Karanteenitilaus</span><span class="sxs-lookup"><span data-stu-id="8ec97-229">Quarantine order</span></span></td>
<td><span data-ttu-id="8ec97-230">Ennen karanteenitilauksen ilmoittamista valmiiksi tai päättyneeksi tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="8ec97-231">Tuhoavia testejä edellyttäviä laatutilauksia ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="8ec97-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="8ec97-232">Karanteenitilaustoiminnon oletetaan käsittelevän tuhottavan materiaalin käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="8ec97-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="8ec97-233">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8ec97-234">Manuaalisesti luotu ostotilaukseen viittaava karanteenitilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-235">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="8ec97-235">Sales order</span></span></td>
<td><span data-ttu-id="8ec97-236">Ennen lähettävien nimikkeiden ajoitettua keräysprosessia tai pakkausluettelon päivitystä</span><span class="sxs-lookup"><span data-stu-id="8ec97-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="8ec97-237">Kaikissa vaiheissa</span><span class="sxs-lookup"><span data-stu-id="8ec97-237">At any step</span></span></td>
<td><span data-ttu-id="8ec97-238">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai asiakkaaseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8ec97-239">Manuaalisesti luotu myyntitilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-240">Tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="8ec97-240">Production order</span></span></td>
<td><span data-ttu-id="8ec97-241">Ennen tuotantotilauksen valmiiksi raportointia tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="8ec97-242">Tuotantotilauksen valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="8ec97-243">Laatutilausvaatimus voi liittyä toimipaikkaan tai nimikkeeseen tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8ec97-244">Manuaalisesti luotu tuotantotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-245">Tuotantotilaus, jossa on reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="8ec97-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="8ec97-246">Ennen työvaiheen raportin valmistumista tai sen jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="8ec97-247">Viimeisen työvaiheen tuotannon valmiiksi raportoinnin jälkeen</span><span class="sxs-lookup"><span data-stu-id="8ec97-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="8ec97-248">Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai operatiiviseen resurssiin tai näiden ehtojen yhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8ec97-249">Manuaalisesti luotu reitityksen työvaiheeseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-250">Varasto</span><span class="sxs-lookup"><span data-stu-id="8ec97-250">Inventory</span></span></td>
<td><span data-ttu-id="8ec97-251">Laatutilausta ei voi luoda automaattisesti varastokirjauskansion tapahtumalle eikä siirtotilaustapahtumille.</span><span class="sxs-lookup"><span data-stu-id="8ec97-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8ec97-252">Laatutilaus on luotava manuaalisesti nimikkeen varastomäärälle.</span><span class="sxs-lookup"><span data-stu-id="8ec97-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="8ec97-253">Fyysistä käytettävissä olevaa varastoa edellytetään.</span><span class="sxs-lookup"><span data-stu-id="8ec97-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="8ec97-254">Esimerkkejä laatutilausten automaattisesta luomisesta</span><span class="sxs-lookup"><span data-stu-id="8ec97-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="8ec97-255">Osto</span><span class="sxs-lookup"><span data-stu-id="8ec97-255">Purchasing</span></span>

<span data-ttu-id="8ec97-256">Jos asetat ostoissa **Tapahtumatyyppi**-kentän arvoksi *Tuotteen vastaanotto* ja **Suoritus**-kentän arvoksi *Jälkeen* **Laatuliitokset**-sivulla, saat seuraavat tulokset:</span><span class="sxs-lookup"><span data-stu-id="8ec97-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="8ec97-257">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Kyllä*, laatutilaus luodaan jokaista vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä sekä nimikeotannan asetukset.</span><span class="sxs-lookup"><span data-stu-id="8ec97-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="8ec97-258">Joka kerta, kun määrä vastaanotetaan ostotilauksen perusteella, luodaaan uusia laatutilauksia juuri saadun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="8ec97-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="8ec97-259">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Ei*, laatutilaus luodaan ensimmäistä vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä.</span><span class="sxs-lookup"><span data-stu-id="8ec97-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="8ec97-260">Lisäksi jäljelle jäävän määrän perusteella luodaan seurantadimensioiden mukaan vähintään yksi laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="8ec97-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="8ec97-261">Laatutilauksia ei luoda ostotilauksen perusteella seuraavien vastaanottojen osalta.</span><span class="sxs-lookup"><span data-stu-id="8ec97-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="8ec97-262">Tuotantoympäristö</span><span class="sxs-lookup"><span data-stu-id="8ec97-262">Production</span></span>

<span data-ttu-id="8ec97-263">Jos asetat tuotannossa **Tapahtumatyyppi**-kentän arvoksi *Ilmoita valmiiksi* ja **Suoritus**-kentän arvoksi *Jälkeen* **Laatuliitokset**-sivulla, saat seuraavat tulokset:</span><span class="sxs-lookup"><span data-stu-id="8ec97-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="8ec97-264">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Kyllä*, laatutilaus luodaan jokaisen valmiin määrän ja nimikeotannan asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="8ec97-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="8ec97-265">Joka kerta, kun määrä ilmoitetaan valmiiksi tuotantotilauksen perusteella, luodaaan uusia laatutilauksia juuri valmiiksi saadun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="8ec97-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="8ec97-266">Tämä luontilogiikka on yhdenmukainen oston kanssa.</span><span class="sxs-lookup"><span data-stu-id="8ec97-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="8ec97-267">Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Ei*, laatutilaus luodaan valmiiksi saadun määrän perusteella ensimmäisellä kerralla, kun määrä ilmoitetaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="8ec97-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="8ec97-268">Lisäksi jäljelle jäävän määrän perusteella luodaan nimikeotannan seurantadimensioiden mukaan vähintään yksi laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="8ec97-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="8ec97-269">Seuraaville valmiille määrille ei luoda laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="8ec97-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ec97-270">Laatumääritys</span><span class="sxs-lookup"><span data-stu-id="8ec97-270">Quality specification</span></span></th>
<th><span data-ttu-id="8ec97-271">Päivitettyä määrää kohden</span><span class="sxs-lookup"><span data-stu-id="8ec97-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="8ec97-272">Seurantadimension mukaan</span><span class="sxs-lookup"><span data-stu-id="8ec97-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="8ec97-273">Tulos</span><span class="sxs-lookup"><span data-stu-id="8ec97-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ec97-274">Prosenttiosuus: 10 %</span><span class="sxs-lookup"><span data-stu-id="8ec97-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="8ec97-275">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8ec97-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="8ec97-276">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="8ec97-276">Batch number: No</span></span></p>
<p><span data-ttu-id="8ec97-277">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="8ec97-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="8ec97-278">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="8ec97-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="8ec97-279">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="8ec97-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="8ec97-280">Laatutilaus 1 määrälle 3 (10 prosenttia 30:stä)</span><span class="sxs-lookup"><span data-stu-id="8ec97-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8ec97-281">Ilmoita valmiiksi 70:n osalta</span><span class="sxs-lookup"><span data-stu-id="8ec97-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="8ec97-282">Laatutilaus 2 määrälle 7 (10 % jäljellä olevasta tilausmäärästä eli 70:stä)</span><span class="sxs-lookup"><span data-stu-id="8ec97-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-283">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="8ec97-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="8ec97-284">Nro</span><span class="sxs-lookup"><span data-stu-id="8ec97-284">No</span></span></td>
<td>
<p><span data-ttu-id="8ec97-285">Eränumero: Ei</span><span class="sxs-lookup"><span data-stu-id="8ec97-285">Batch number: No</span></span></p>
<p><span data-ttu-id="8ec97-286">Sarjanumero: Ei</span><span class="sxs-lookup"><span data-stu-id="8ec97-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="8ec97-287">Tilausmäärä: 100</span><span class="sxs-lookup"><span data-stu-id="8ec97-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="8ec97-288">Ilmoita valmiiksi 30:n osalta</span><span class="sxs-lookup"><span data-stu-id="8ec97-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="8ec97-289">Laatutilaus 1 määrälle 1 (ensimmäiselle valmiiksi ilmoitetulle määrälle, jolla on kiinteä arvo 1)</span><span class="sxs-lookup"><span data-stu-id="8ec97-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="8ec97-290">Laatutilaus 2 määrälle 1 (jäljelle olevalle määrälle, jolla on edelleen kiinteä arvo 1)</span><span class="sxs-lookup"><span data-stu-id="8ec97-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8ec97-291">Ilmoita valmiiksi 10:n osalta</span><span class="sxs-lookup"><span data-stu-id="8ec97-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="8ec97-292">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="8ec97-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8ec97-293">Ilmoita valmiiksi 60:n osalta</span><span class="sxs-lookup"><span data-stu-id="8ec97-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="8ec97-294">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="8ec97-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-295">Kiinteä määrä: 1</span><span class="sxs-lookup"><span data-stu-id="8ec97-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="8ec97-296">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8ec97-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="8ec97-297">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="8ec97-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="8ec97-298">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="8ec97-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="8ec97-299">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="8ec97-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="8ec97-300">Ilmoita valmiiksi 3:n osalta: 1 eränumerolle b1, sarjanumero s1; 1 eränumerolle b2, sarjanumero s2; ja 1 eränumerolle b3, sarjanumero s3</span><span class="sxs-lookup"><span data-stu-id="8ec97-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="8ec97-301">Laatutilaus 1 määrälle 1 eränumerosta b1, sarjanumero s1</span><span class="sxs-lookup"><span data-stu-id="8ec97-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="8ec97-302">Laatutilaus 2 määrälle 1 eränumerosta b2, sarjanumero s2</span><span class="sxs-lookup"><span data-stu-id="8ec97-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="8ec97-303">Laatutilaus 3 määrälle 1 eränumerosta b3, sarjanumero s3</span><span class="sxs-lookup"><span data-stu-id="8ec97-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8ec97-304">Ilmoita valmiiksi 2:n osalta: 1 eränumerolle b4, sarjanumero s4; ja 1 eränumerolle b5, sarjanumero s5</span><span class="sxs-lookup"><span data-stu-id="8ec97-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="8ec97-305">Laatutilaus 4 määrälle 1 eränumerosta b4, sarjanumero s4</span><span class="sxs-lookup"><span data-stu-id="8ec97-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="8ec97-306">Laatutilaus 5 määrälle 1 eränumerosta b5, sarjanumero s5</span><span class="sxs-lookup"><span data-stu-id="8ec97-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="8ec97-307"><strong>Huomautus:</strong> Erää voidaan käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8ec97-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="8ec97-308">Kiinteä määrä: 2</span><span class="sxs-lookup"><span data-stu-id="8ec97-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="8ec97-309">Nro</span><span class="sxs-lookup"><span data-stu-id="8ec97-309">No</span></span></td>
<td>
<p><span data-ttu-id="8ec97-310">Eränumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="8ec97-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="8ec97-311">Sarjanumero: Kyllä</span><span class="sxs-lookup"><span data-stu-id="8ec97-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="8ec97-312">Tilausmäärä: 10</span><span class="sxs-lookup"><span data-stu-id="8ec97-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="8ec97-313">Ilmoita valmiiksi 4:n osalta: 1 eränumerolle b1, sarjanumero s1; 1 eränumerolle b2, sarjanumero s2; 1 eränumerolle b3, sarjanumero s3; ja 1 eränumerolle b4, sarjanumero s4</span><span class="sxs-lookup"><span data-stu-id="8ec97-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="8ec97-314">Laatutilaus 1 määrälle 1 eränumerosta b1, sarjanumero s1</span><span class="sxs-lookup"><span data-stu-id="8ec97-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="8ec97-315">Laatutilaus 2 määrälle 1 eränumerosta b2, sarjanumero s2</span><span class="sxs-lookup"><span data-stu-id="8ec97-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="8ec97-316">Laatutilaus 3 määrälle 1 eränumerosta b3, sarjanumero s3</span><span class="sxs-lookup"><span data-stu-id="8ec97-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="8ec97-317">Laatutilaus 4 määrälle 1 eränumerosta b4, sarjanumero s4</span><span class="sxs-lookup"><span data-stu-id="8ec97-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="8ec97-318">Laatutilaus 5 määrälle 2 ilman viittausta erä- ja sarjanumeroon</span><span class="sxs-lookup"><span data-stu-id="8ec97-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8ec97-319">Ilmoita valmiiksi 6:n osalta: 1 eränumerolle b5, sarjanumero s5; 1 eränumerolle b6, sarjanumero s6; 1 eränumerolle b7, sarjanumero s7; 1 eränumerolle b8, sarjanumero s8; 1 eränumerolle b9, sarjanumero s9; ja 1 eränumerolle b10, sarjanumero s10</span><span class="sxs-lookup"><span data-stu-id="8ec97-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="8ec97-320">Laatutilauksia ei luota.</span><span class="sxs-lookup"><span data-stu-id="8ec97-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="8ec97-321">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8ec97-321">Additional resources</span></span>

- [<span data-ttu-id="8ec97-322">Laadunhallintaprosessit</span><span class="sxs-lookup"><span data-stu-id="8ec97-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="8ec97-323">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="8ec97-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="8ec97-324">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="8ec97-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
