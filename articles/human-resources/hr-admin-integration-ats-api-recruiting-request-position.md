---
title: Työhönottopyynnön toimi
description: Tässä aiheessa kuvataan työhönottopyynnön toimen yksikköä Dynamics 365 Human Resourcesissa.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01d73d390f72343c7498ccbb99838d38be45a19e
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126023"
---
# <a name="recruiting-request-position"></a><span data-ttu-id="f96fd-103">Työhönottopyynnön toimi</span><span class="sxs-lookup"><span data-stu-id="f96fd-103">Recruiting request position</span></span>

<span data-ttu-id="f96fd-104">Tässä aiheessa kuvataan työhönottopyynnön toimen yksikköä Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="f96fd-104">This topic describes the Recruiting request position entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f96fd-105">Fyysinen nimi: mshr_hcmrecruitingrequestpositionentity</span><span class="sxs-lookup"><span data-stu-id="f96fd-105">Physical name: mshr_hcmrecruitingrequestpositionentity</span></span>

### <a name="description"></a><span data-ttu-id="f96fd-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f96fd-106">Description</span></span>

<span data-ttu-id="f96fd-107">Kuvaa työhönottopyynnön toimen tai toimet.</span><span class="sxs-lookup"><span data-stu-id="f96fd-107">Describes the position or positions to fill for a recruiting request.</span></span> <span data-ttu-id="f96fd-108">Toimen lisääminen työhönottopyyntöön on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="f96fd-108">Adding a position to the recruiting request is optional.</span></span> <span data-ttu-id="f96fd-109">Toimen ominaisuudet ovat vain luku -ominaisuuksia, koska työhönottopyynnön toimen ominaisuudet eivät voi olla erilaiset kuin ne ovat toimen päätietueessa.</span><span class="sxs-lookup"><span data-stu-id="f96fd-109">The properties of the position are read-only, as the position properties shouldn't be different on the recruiting request than they are on the position master record.</span></span> <span data-ttu-id="f96fd-110">Jos ominaisuuksia on tarve muuttaaa, se tulee tehdä toimen päätietueessa, ennen kuin toimi lisätään työhönottopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="f96fd-110">If the properties need to change, it should be done on the position master record before adding the position to the recruiting request.</span></span>

### <a name="json-representation"></a><span data-ttu-id="f96fd-111">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="f96fd-111">JSON representation</span></span>
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="f96fd-112">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f96fd-112">Properties</span></span>

| <span data-ttu-id="f96fd-113">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="f96fd-113">Property</span></span><br><span data-ttu-id="f96fd-114">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="f96fd-114">**Physical name**</span></span><br><span data-ttu-id="f96fd-115">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="f96fd-115">**_Type_**</span></span> | <span data-ttu-id="f96fd-116">Käytä</span><span class="sxs-lookup"><span data-stu-id="f96fd-116">Use</span></span> | <span data-ttu-id="f96fd-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f96fd-117">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f96fd-118">**Työhönottopyynnön toimen yksikön tunnus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-118">**Recruiting Request Position Entity ID**</span></span><br><span data-ttu-id="f96fd-119">mshr_hcmrecruitingrequestpositionentityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-119">mshr_hcmrecruitingrequestpositionentityid</span></span><br><span data-ttu-id="f96fd-120">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-120">*GUID*</span></span> | <span data-ttu-id="f96fd-121">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-121">Read-only</span></span><br><span data-ttu-id="f96fd-122">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-122">Required</span></span> |    <span data-ttu-id="f96fd-123">Järjestelmän luoma työhönottopyynnön toimitietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="f96fd-123">System-generated identifier of the recruiting request position record.</span></span> |
| <span data-ttu-id="f96fd-124">**Työhönottopyynnön tunnus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-124">**Recruiting Request ID**</span></span><br><span data-ttu-id="f96fd-125">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="f96fd-125">mshr_recruitingrequestid</span></span><br><span data-ttu-id="f96fd-126">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-126">*String*</span></span> | <span data-ttu-id="f96fd-127">Kirjoita kerran</span><span class="sxs-lookup"><span data-stu-id="f96fd-127">Write-once</span></span><br><span data-ttu-id="f96fd-128">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-128">Required</span></span> | <span data-ttu-id="f96fd-129">Käyttäjän luettava työhönottopyynnön yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="f96fd-129">The user-readable unique identifier of the recruiting request.</span></span> |
| <span data-ttu-id="f96fd-130">**Työhönottopyynnön tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-130">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="f96fd-131">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-131">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="f96fd-132">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-132">*GUID*</span></span> | <span data-ttu-id="f96fd-133">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-133">Read-only</span></span><br><span data-ttu-id="f96fd-134">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-134">Required</span></span><br><span data-ttu-id="f96fd-135">Viiteavain: mshr_hcmrecruitingrequestentity-yksikön mshr_hcmrecruitingrequestentityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-135">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity entity</span></span> | <span data-ttu-id="f96fd-136">Järjestelmän luoma sen työhönottopyynnön tunnus, johon toimi on määritetty.</span><span class="sxs-lookup"><span data-stu-id="f96fd-136">System-generated identifier of the recruiting request to which the position is assigned.</span></span> |
| <span data-ttu-id="f96fd-137">**Toimen tunnus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-137">**Position ID**</span></span><br><span data-ttu-id="f96fd-138">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="f96fd-138">mshr_positionid</span></span><br><span data-ttu-id="f96fd-139">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-139">*String*</span></span> | <span data-ttu-id="f96fd-140">Kirjoita kerran</span><span class="sxs-lookup"><span data-stu-id="f96fd-140">Write-once</span></span><br><span data-ttu-id="f96fd-141">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-141">Required</span></span> | <span data-ttu-id="f96fd-142">Käyttäjän luettava toimen yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="f96fd-142">The user-readable unique identifier of the position.</span></span> |
| <span data-ttu-id="f96fd-143">**Toimen tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-143">**Position ID Value**</span></span><br><span data-ttu-id="f96fd-144">_mshr_fk_position_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-144">_mshr_fk_position_id_value</span></span><br><span data-ttu-id="f96fd-145">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-145">*GUID*</span></span> | <span data-ttu-id="f96fd-146">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-146">Read-only</span></span><br><span data-ttu-id="f96fd-147">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-147">Required</span></span><br><span data-ttu-id="f96fd-148">Viiteavain: mshr_hcmpositionv2entity-yksikön mshr_hcmpositionv2entityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-148">Foreign key: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity entity</span></span> | <span data-ttu-id="f96fd-149">Järjestelmän luoma toimen tunnus.</span><span class="sxs-lookup"><span data-stu-id="f96fd-149">System-generated identifier of the position.</span></span> |
| <span data-ttu-id="f96fd-150">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-150">**Description**</span></span><br><span data-ttu-id="f96fd-151">mshr_description</span><span class="sxs-lookup"><span data-stu-id="f96fd-151">mshr_description</span></span><br><span data-ttu-id="f96fd-152">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-152">*String*</span></span> | <span data-ttu-id="f96fd-153">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-153">Read-only</span></span><br><span data-ttu-id="f96fd-154">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-154">Required</span></span> | <span data-ttu-id="f96fd-155">Toimen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f96fd-155">The position description.</span></span> |
| <span data-ttu-id="f96fd-156">**Toimityypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-156">**Position Type ID**</span></span><br><span data-ttu-id="f96fd-157">mshr_positiontypeid</span><span class="sxs-lookup"><span data-stu-id="f96fd-157">mshr_positiontypeid</span></span><br><span data-ttu-id="f96fd-158">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-158">*String*</span></span> | <span data-ttu-id="f96fd-159">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-159">Read-only</span></span><br><span data-ttu-id="f96fd-160">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-160">Optional</span></span> | <span data-ttu-id="f96fd-161">Käyttäjän luettava toimityypin yksilöivä tunnus tälle toimelle.</span><span class="sxs-lookup"><span data-stu-id="f96fd-161">The user-readable unique identifier of the position type for this position.</span></span> |
| <span data-ttu-id="f96fd-162">**Toimityypin tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-162">**Position Type ID Value**</span></span><br><span data-ttu-id="f96fd-163">_mshr_fk_positiontype_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-163">_mshr_fk_positiontype_id_value</span></span><br><span data-ttu-id="f96fd-164">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-164">*GUID*</span></span> | <span data-ttu-id="f96fd-165">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-165">Read-only</span></span><br><span data-ttu-id="f96fd-166">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-166">Optional</span></span><br><span data-ttu-id="f96fd-167">Viiteavain: mshr_hcmpositiontypeentity-yksikön mshr_hcmpositiontypeentityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-167">Foreign key: mshr_hcmpositiontypeentityid of mshr_hcmpositiontypeentity entity</span></span> | <span data-ttu-id="f96fd-168">Järjestelmän luoma toimityypin yksilöivä tunnus tälle toimelle.</span><span class="sxs-lookup"><span data-stu-id="f96fd-168">A system-generated unique identifier of the position type for this position.</span></span> |
| <span data-ttu-id="f96fd-169">**Tila**</span><span class="sxs-lookup"><span data-stu-id="f96fd-169">**Status**</span></span><br><span data-ttu-id="f96fd-170">mshr_status</span><span class="sxs-lookup"><span data-stu-id="f96fd-170">mshr_status</span></span><br><span data-ttu-id="f96fd-171">*RecruitingRequestPositionStatus*-asetusjoukko</span><span class="sxs-lookup"><span data-stu-id="f96fd-171">*RecruitingRequestPositionStatus* option set</span></span> | <span data-ttu-id="f96fd-172">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="f96fd-172">Read/write</span></span><br><span data-ttu-id="f96fd-173">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-173">Required</span></span> | <span data-ttu-id="f96fd-174">Työhönottopyynnön toimen tila.</span><span class="sxs-lookup"><span data-stu-id="f96fd-174">Status of the position for the recruiting request.</span></span> |
| <span data-ttu-id="f96fd-175">**Osaston numero**</span><span class="sxs-lookup"><span data-stu-id="f96fd-175">**Department Number**</span></span><br><span data-ttu-id="f96fd-176">mshr_departmentnumber</span><span class="sxs-lookup"><span data-stu-id="f96fd-176">mshr_departmentnumber</span></span><br><span data-ttu-id="f96fd-177">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-177">*String*</span></span> | <span data-ttu-id="f96fd-178">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-178">Read-only</span></span><br><span data-ttu-id="f96fd-179">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-179">Optional</span></span><br> | <span data-ttu-id="f96fd-180">Toimen osastonumero.</span><span class="sxs-lookup"><span data-stu-id="f96fd-180">The department number of the position.</span></span> |
| <span data-ttu-id="f96fd-181">**Osastotunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-181">**Department ID Value**</span></span><br><span data-ttu-id="f96fd-182">_mshr_fk_department_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-182">_mshr_fk_department_id_value</span></span><br><span data-ttu-id="f96fd-183">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-183">*GUID*</span></span> | <span data-ttu-id="f96fd-184">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-184">Read-only</span></span><br><span data-ttu-id="f96fd-185">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-185">Optional</span></span><br><span data-ttu-id="f96fd-186">Viiteavain: mshr_omdepartmententity-yksikön mshr_omdepartmententityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-186">Foreign key: mshr_omdepartmententityid of mshr_omdepartmententity entity</span></span> | <span data-ttu-id="f96fd-187">Järjestelmän luoma toimen osaston yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="f96fd-187">System-generated unique identifier of the department of the position.</span></span> |
| <span data-ttu-id="f96fd-188">**Esimiehen toimen tunnus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-188">**Reports To Position ID**</span></span><br><span data-ttu-id="f96fd-189">mshr_reportstopositionid</span><span class="sxs-lookup"><span data-stu-id="f96fd-189">mshr_reportstopositionid</span></span><br><span data-ttu-id="f96fd-190">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-190">*String*</span></span> | <span data-ttu-id="f96fd-191">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-191">Read-only</span></span><br><span data-ttu-id="f96fd-192">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-192">Required</span></span> | <span data-ttu-id="f96fd-193">Sen toimen käyttäjän luettava tunnus, jolle rekrytoitu toimi raportoi organisaatiohierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="f96fd-193">The user-readable ID of the position to which the recruited position reports in the organizational hierarchy.</span></span> |
| <span data-ttu-id="f96fd-194">**Esimiehen toimen tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-194">**Reports To Position ID Value**</span></span><br><span data-ttu-id="f96fd-195">_mshr_fk_reportstoposition_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-195">_mshr_fk_reportstoposition_id_value</span></span><br><span data-ttu-id="f96fd-196">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-196">*GUID*</span></span> | <span data-ttu-id="f96fd-197">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-197">Read-only</span></span><br><span data-ttu-id="f96fd-198">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-198">Required</span></span><br><span data-ttu-id="f96fd-199">Viiteavain: mshr_hcmpositionv2entity-yksikön mshr_hcmpositionv2entityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-199">Foreign key: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity entity</span></span> | <span data-ttu-id="f96fd-200">Järjestelmän luoma sen toimen tunnus, jolle rekrytoitu toimi raportoi.</span><span class="sxs-lookup"><span data-stu-id="f96fd-200">The system-generated ID of the position to which the recruited position reports.</span></span> |
| <span data-ttu-id="f96fd-201">**Esimiehen henkilöstönumero**</span><span class="sxs-lookup"><span data-stu-id="f96fd-201">**Reports To Personnel Number**</span></span><br><span data-ttu-id="f96fd-202">mshr_reportstopersonnelnumber</span><span class="sxs-lookup"><span data-stu-id="f96fd-202">mshr_reportstopersonnelnumber</span></span><br><span data-ttu-id="f96fd-203">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-203">*String*</span></span> | <span data-ttu-id="f96fd-204">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-204">Read-only</span></span><br><span data-ttu-id="f96fd-205">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-205">Required</span></span> | <span data-ttu-id="f96fd-206">Sen työntekijän työntekijätunnus, jolle palkattu hakija raportoi.</span><span class="sxs-lookup"><span data-stu-id="f96fd-206">The worker ID of the worker to which the hired candidate will report.</span></span> |
| <span data-ttu-id="f96fd-207">**Esimiehen työntekijätunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-207">**Reports To Worker ID Value**</span></span><br><span data-ttu-id="f96fd-208">_mshr_fk_reportstoworker_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-208">_mshr_fk_reportstoworker_id_value</span></span><br><span data-ttu-id="f96fd-209">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-209">*GUID*</span></span> | <span data-ttu-id="f96fd-210">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-210">Read-only</span></span><br><span data-ttu-id="f96fd-211">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-211">Required</span></span><br><span data-ttu-id="f96fd-212">Viiteavain: mshr_hcmworkerbaseentity-yksikön mshr_hcmworkerbaseentityid</span><span class="sxs-lookup"><span data-stu-id="f96fd-212">Foreign key: mshr_hcmworkerbaseentityid of mshr_hcmworkerbaseentity entity</span></span> | <span data-ttu-id="f96fd-213">Järjestelmän luoma työntekijän tunnus, jolle palkattu hakija raportoi.</span><span class="sxs-lookup"><span data-stu-id="f96fd-213">System-generated ID of the worker to which the hired candidate will report.</span></span> |
| <span data-ttu-id="f96fd-214">**Taloushallinnon dimensio**</span><span class="sxs-lookup"><span data-stu-id="f96fd-214">**Financial Dimension**</span></span><br><span data-ttu-id="f96fd-215">mshr_financialdimension</span><span class="sxs-lookup"><span data-stu-id="f96fd-215">mshr_financialdimension</span></span><br><span data-ttu-id="f96fd-216">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-216">*String*</span></span> | <span data-ttu-id="f96fd-217">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-217">Read-only</span></span><br><span data-ttu-id="f96fd-218">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-218">Optional</span></span> | <span data-ttu-id="f96fd-219">Toimelle määritetty taloushallinnon dimensio (esimerkiksi kustannuspaikka).</span><span class="sxs-lookup"><span data-stu-id="f96fd-219">The financial dimension (for example, cost center) assigned to the position.</span></span> <span data-ttu-id="f96fd-220">Taloushallinnon dimensio määritetään kullekin toimelle yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="f96fd-220">The financial dimension is assigned for each position per legal entity.</span></span> <span data-ttu-id="f96fd-221">Dimensioissa määritetyt kustannuskeskukset ovat käytettävissä mshr_dimattributeomcostcenterentity-yksikön kautta.</span><span class="sxs-lookup"><span data-stu-id="f96fd-221">Cost centers that are defined in dimensions are accessible through the mshr_dimattributeomcostcenterentity entity.</span></span> |
| <span data-ttu-id="f96fd-222">**Tietoalueen tunnus**</span><span class="sxs-lookup"><span data-stu-id="f96fd-222">**Data Area ID**</span></span><br><span data-ttu-id="f96fd-223">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="f96fd-223">mshr_dataareaid</span></span><br><span data-ttu-id="f96fd-224">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-224">*String*</span></span> | <span data-ttu-id="f96fd-225">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="f96fd-225">Read/write</span></span><br><span data-ttu-id="f96fd-226">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-226">Optional</span></span> | <span data-ttu-id="f96fd-227">Määrittää työhönottopyynnön toimen yrityksen.</span><span class="sxs-lookup"><span data-stu-id="f96fd-227">Specifies the legal entity (company) for the recruiting request position.</span></span> |
| <span data-ttu-id="f96fd-228">**Tietoalueen tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="f96fd-228">**Data Area ID Value**</span></span><br><span data-ttu-id="f96fd-229">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="f96fd-229">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="f96fd-230">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f96fd-230">*GUID*</span></span> | <span data-ttu-id="f96fd-231">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-231">Read-only</span></span><br><span data-ttu-id="f96fd-232">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="f96fd-232">Optional</span></span><br><span data-ttu-id="f96fd-233">Viiteavain: cdm_companyid of cdm_company-yksikkö</span><span class="sxs-lookup"><span data-stu-id="f96fd-233">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="f96fd-234">Järjestelmän luoma GUID-tunnus, joka yksilöi työhönottopyynnön toimen oikeushenkilön (yrityksen).</span><span class="sxs-lookup"><span data-stu-id="f96fd-234">System-generated GUID value identifying the legal entity (company) for the recruiting request position.</span></span> |
| <span data-ttu-id="f96fd-235">**Ensisijainen kenttä**</span><span class="sxs-lookup"><span data-stu-id="f96fd-235">**Primary Field**</span></span><br><span data-ttu-id="f96fd-236">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f96fd-236">mshr_primaryfield</span></span><br><span data-ttu-id="f96fd-237">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f96fd-237">*String*</span></span> | <span data-ttu-id="f96fd-238">Vain luku</span><span class="sxs-lookup"><span data-stu-id="f96fd-238">Read-only</span></span><br><span data-ttu-id="f96fd-239">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="f96fd-239">Required</span></span> | <span data-ttu-id="f96fd-240">Työhönottopyynnön arvon ja toimitunnuksen ketjutus toisena menetelmänä tietueen yksilöiväksi tunnistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f96fd-240">Concatenation of Recruiting Request value and Position ID as another method to uniquely identify the record.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f96fd-241">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f96fd-241">See also</span></span>

[<span data-ttu-id="f96fd-242">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="f96fd-242">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f96fd-243">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="f96fd-243">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
