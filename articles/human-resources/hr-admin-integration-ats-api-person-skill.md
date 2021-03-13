---
title: Henkilön osaamisalue
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön osaamisalue -yksikköä.
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
ms.openlocfilehash: b6bcbbd1203f4e9e80f6c5264cf4d5ea7d0970fc
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126095"
---
# <a name="person-skill"></a><span data-ttu-id="4ce30-103">Henkilön osaamisalue</span><span class="sxs-lookup"><span data-stu-id="4ce30-103">Person skill</span></span>

<span data-ttu-id="4ce30-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön osaamisalue -yksikköä.</span><span class="sxs-lookup"><span data-stu-id="4ce30-104">This topic describes the Person skill entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4ce30-105">Fyysinen nimi: mshr_hcmpersonskillentity</span><span class="sxs-lookup"><span data-stu-id="4ce30-105">Physical name: mshr_hcmpersonskillentity</span></span>

## <a name="description"></a><span data-ttu-id="4ce30-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4ce30-106">Description</span></span>

<span data-ttu-id="4ce30-107">Tämä yksikkö kuvaa hakijan osaamisalueita.</span><span class="sxs-lookup"><span data-stu-id="4ce30-107">This entity describes the skills of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4ce30-108">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="4ce30-108">JSON representation</span></span>

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="4ce30-109">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4ce30-109">Properties</span></span>

| <span data-ttu-id="4ce30-110">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="4ce30-110">Property</span></span><br><span data-ttu-id="4ce30-111">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="4ce30-111">**Physical name**</span></span><br><span data-ttu-id="4ce30-112">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="4ce30-112">**_Type_**</span></span> | <span data-ttu-id="4ce30-113">Käytä</span><span class="sxs-lookup"><span data-stu-id="4ce30-113">Use</span></span> | <span data-ttu-id="4ce30-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4ce30-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4ce30-115">**Henkilön osaamisalueen yksikkötunnus**</span><span class="sxs-lookup"><span data-stu-id="4ce30-115">**Person Skill Entity ID**</span></span><br><span data-ttu-id="4ce30-116">mshr_hcmpersonskillentityid</span><span class="sxs-lookup"><span data-stu-id="4ce30-116">mshr_hcmpersonskillentityid</span></span><br><span data-ttu-id="4ce30-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ce30-117">*GUID*</span></span> | <span data-ttu-id="4ce30-118">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-118">Read-only</span></span><br><span data-ttu-id="4ce30-119">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-119">Required</span></span> | <span data-ttu-id="4ce30-120">Järjestelmän luoma yksikkötietueen yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="4ce30-121">**Osapuolinumero**</span><span class="sxs-lookup"><span data-stu-id="4ce30-121">**Party Number**</span></span><br><span data-ttu-id="4ce30-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="4ce30-122">mshr_partynumber</span></span><br><span data-ttu-id="4ce30-123">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-123">*String*</span></span> | <span data-ttu-id="4ce30-124">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-124">Read/write</span></span><br><span data-ttu-id="4ce30-125">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-125">Required</span></span> |   <span data-ttu-id="4ce30-126">Liittyvän osapuolen (henkilön) tietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-126">The ID of the associated party (person) record.</span></span> |
| <span data-ttu-id="4ce30-127">**Henkilötunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="4ce30-127">**Person ID Value**</span></span><br><span data-ttu-id="4ce30-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="4ce30-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="4ce30-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ce30-129">*GUID*</span></span> | <span data-ttu-id="4ce30-130">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-130">Read-only</span></span><br><span data-ttu-id="4ce30-131">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-131">Required</span></span><br><span data-ttu-id="4ce30-132">Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="4ce30-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="4ce30-133">Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="4ce30-134">**Sertifioija**</span><span class="sxs-lookup"><span data-stu-id="4ce30-134">**Certifier**</span></span><br><span data-ttu-id="4ce30-135">mshr_certifier</span><span class="sxs-lookup"><span data-stu-id="4ce30-135">mshr_certifier</span></span><br><span data-ttu-id="4ce30-136">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-136">*String*</span></span> | <span data-ttu-id="4ce30-137">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-137">Read/write</span></span><br><span data-ttu-id="4ce30-138">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="4ce30-138">Optional</span></span> | <span data-ttu-id="4ce30-139">Osaamisalueen todentaneen työntekijän henkilökuntanumero.</span><span class="sxs-lookup"><span data-stu-id="4ce30-139">The personnel number of the worker who certified this skill.</span></span> |
| <span data-ttu-id="4ce30-140">**Sertifioijan tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="4ce30-140">**Certifier ID Value**</span></span><br><span data-ttu-id="4ce30-141">_mshr_fk_certifier_id_value</span><span class="sxs-lookup"><span data-stu-id="4ce30-141">_mshr_fk_certifier_id_value</span></span><br><span data-ttu-id="4ce30-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ce30-142">*GUID*</span></span> | <span data-ttu-id="4ce30-143">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-143">Read-only</span></span><br><span data-ttu-id="4ce30-144">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="4ce30-144">Optional</span></span><br><span data-ttu-id="4ce30-145">Viiteavain: mshr_hcmworkerentity-yksikön mshr_hcmworkerentityid</span><span class="sxs-lookup"><span data-stu-id="4ce30-145">Foreign key: mshr_hcmworkerentityid of mshr_hcmworkerentity</span></span> | <span data-ttu-id="4ce30-146">Osaamisalueen todentaneen työntekijän tietueen järjestelmän luoma yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-146">System-generated unique identifier of the worker record for the worker who certified the skill.</span></span> |
| <span data-ttu-id="4ce30-147">**Osaamisaluetunnus**</span><span class="sxs-lookup"><span data-stu-id="4ce30-147">**Skill ID**</span></span><br><span data-ttu-id="4ce30-148">mshr_skillid</span><span class="sxs-lookup"><span data-stu-id="4ce30-148">mshr_skillid</span></span><br><span data-ttu-id="4ce30-149">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-149">*String*</span></span> | <span data-ttu-id="4ce30-150">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-150">Read/write</span></span><br><span data-ttu-id="4ce30-151">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-151">Required</span></span> | <span data-ttu-id="4ce30-152">Human Resourcesin osaamisalueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-152">The identifier of the skill defined in Human Resources.</span></span> |
| <span data-ttu-id="4ce30-153">**Osaamisaluetunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="4ce30-153">**Skill ID Value**</span></span><br><span data-ttu-id="4ce30-154">_mshr_fk_skill_id_value</span><span class="sxs-lookup"><span data-stu-id="4ce30-154">_mshr_fk_skill_id_value</span></span><br><span data-ttu-id="4ce30-155">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ce30-155">*GUID*</span></span> | <span data-ttu-id="4ce30-156">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-156">Read-only</span></span><br><span data-ttu-id="4ce30-157">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-157">Required</span></span><br><span data-ttu-id="4ce30-158">Viiteavain: mshr_hcmskillentity-yksikön mshr_hcmskillentityid</span><span class="sxs-lookup"><span data-stu-id="4ce30-158">Foreign key: mshr_hcmskillentityid of mshr_hcmskillentity</span></span> | <span data-ttu-id="4ce30-159">Järjestelmän luoma valitun osaamisalueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-159">The system-generated identifier of the selected skill.</span></span> |
| <span data-ttu-id="4ce30-160">**Kokemus vuosina**</span><span class="sxs-lookup"><span data-stu-id="4ce30-160">**Years of Experience**</span></span><br><span data-ttu-id="4ce30-161">mshr_yearsofexperience</span><span class="sxs-lookup"><span data-stu-id="4ce30-161">mshr_yearsofexperience</span></span><br><span data-ttu-id="4ce30-162">*Desimaali*</span><span class="sxs-lookup"><span data-stu-id="4ce30-162">*Decimal*</span></span> | <span data-ttu-id="4ce30-163">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-163">Read/write</span></span><br><span data-ttu-id="4ce30-164">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="4ce30-164">Optional</span></span> | <span data-ttu-id="4ce30-165">Hakijan tämän osaamisalueen kokemus vuosina.</span><span class="sxs-lookup"><span data-stu-id="4ce30-165">The years of experience the candidate has in this skill.</span></span> |
| <span data-ttu-id="4ce30-166">**Luokitustunnus**</span><span class="sxs-lookup"><span data-stu-id="4ce30-166">**Rating ID**</span></span><br><span data-ttu-id="4ce30-167">mshr_ratingid</span><span class="sxs-lookup"><span data-stu-id="4ce30-167">mshr_ratingid</span></span><br><span data-ttu-id="4ce30-168">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-168">*String*</span></span> | <span data-ttu-id="4ce30-169">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-169">Read/write</span></span><br><span data-ttu-id="4ce30-170">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-170">Required</span></span> | <span data-ttu-id="4ce30-171">Arviointiasteikon tyyppi.</span><span class="sxs-lookup"><span data-stu-id="4ce30-171">The rating scale type.</span></span> <span data-ttu-id="4ce30-172">Tälle yksikölle arvo on **Osaamisalueet**.</span><span class="sxs-lookup"><span data-stu-id="4ce30-172">For this entity, the value is **Skills**.</span></span> |
| <span data-ttu-id="4ce30-173">**Tasotyyppi**</span><span class="sxs-lookup"><span data-stu-id="4ce30-173">**Level Type**</span></span><br><span data-ttu-id="4ce30-174">mshr_leveltype</span><span class="sxs-lookup"><span data-stu-id="4ce30-174">mshr_leveltype</span></span><br><span data-ttu-id="4ce30-175">*mshr_hrmskillleveltype-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="4ce30-175">*mshr_hrmskillleveltype option set*</span></span> | <span data-ttu-id="4ce30-176">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-176">Read/write</span></span><br><span data-ttu-id="4ce30-177">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-177">Required</span></span> | <span data-ttu-id="4ce30-178">Osaamisaluetasolle määritetty tyyppiluokitus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-178">A type categorization for the level assigned to the skill.</span></span> |
| <span data-ttu-id="4ce30-179">**Tason tunnus**</span><span class="sxs-lookup"><span data-stu-id="4ce30-179">**Level ID**</span></span><br><span data-ttu-id="4ce30-180">mshr_levelid</span><span class="sxs-lookup"><span data-stu-id="4ce30-180">mshr_levelid</span></span><br><span data-ttu-id="4ce30-181">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-181">*String*</span></span> | <span data-ttu-id="4ce30-182">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-182">Read/write</span></span><br><span data-ttu-id="4ce30-183">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-183">Required</span></span> | <span data-ttu-id="4ce30-184">Sen luokitustason tunnus, jolla hakijalla on tämä osaamisalue.</span><span class="sxs-lookup"><span data-stu-id="4ce30-184">The ID of the Rating Level the candidate has for this skill.</span></span> |
| <span data-ttu-id="4ce30-185">**Luokitustason tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="4ce30-185">**Rating Level ID Value**</span></span><br><span data-ttu-id="4ce30-186">_mshr_fk_ratinglevel_id_value</span><span class="sxs-lookup"><span data-stu-id="4ce30-186">_mshr_fk_ratinglevel_id_value</span></span><br><span data-ttu-id="4ce30-187">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ce30-187">*GUID*</span></span> | <span data-ttu-id="4ce30-188">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-188">Read-only</span></span><br><span data-ttu-id="4ce30-189">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-189">Required</span></span><br><span data-ttu-id="4ce30-190">Viiteavain: mshr_hcmratinglevelentity-yksikön mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="4ce30-190">Foreign key: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity</span></span> | <span data-ttu-id="4ce30-191">Järjestelmän luoma luokitustason tunnus.</span><span class="sxs-lookup"><span data-stu-id="4ce30-191">The system-generated identifier of the rating level.</span></span> |
| <span data-ttu-id="4ce30-192">**Tason päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="4ce30-192">**Level Date**</span></span><br><span data-ttu-id="4ce30-193">mshr_leveldate</span><span class="sxs-lookup"><span data-stu-id="4ce30-193">mshr_leveldate</span></span><br><span data-ttu-id="4ce30-194">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="4ce30-194">*Datetime*</span></span> | <span data-ttu-id="4ce30-195">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-195">Read/write</span></span><br><span data-ttu-id="4ce30-196">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-196">Required</span></span> | <span data-ttu-id="4ce30-197">Päivämäärä, jolloin hakijan osaamisalue on luokiteltu.</span><span class="sxs-lookup"><span data-stu-id="4ce30-197">The date at which the candidate was rated in the skill.</span></span> |
| <span data-ttu-id="4ce30-198">**Luokitustason tarkastaja**</span><span class="sxs-lookup"><span data-stu-id="4ce30-198">**Rating Level Examiner**</span></span><br><span data-ttu-id="4ce30-199">mshr_ratinglevelexaminer</span><span class="sxs-lookup"><span data-stu-id="4ce30-199">mshr_ratinglevelexaminer</span></span><br><span data-ttu-id="4ce30-200">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-200">*String*</span></span> | <span data-ttu-id="4ce30-201">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-201">Read/write</span></span><br><span data-ttu-id="4ce30-202">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="4ce30-202">Optional</span></span> | <span data-ttu-id="4ce30-203">Ehdokkaan luokitelleen työntekijän henkilökuntanumero.</span><span class="sxs-lookup"><span data-stu-id="4ce30-203">The personnel number of the worker who rated the candidate.</span></span> |
| <span data-ttu-id="4ce30-204">**Luokitustason tarkastajan tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="4ce30-204">**Rating Level Examiner ID Value**</span></span><br><span data-ttu-id="4ce30-205">_mshr_fk_ratinglevelexaminer_id_value</span><span class="sxs-lookup"><span data-stu-id="4ce30-205">_mshr_fk_ratinglevelexaminer_id_value</span></span><br><span data-ttu-id="4ce30-206">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ce30-206">*GUID*</span></span> | <span data-ttu-id="4ce30-207">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-207">Read-only</span></span><br><span data-ttu-id="4ce30-208">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="4ce30-208">Optional</span></span><br><span data-ttu-id="4ce30-209">Viiteavain: mshr_hcmworkerentity-yksikön mshr_hcmworkerentityid</span><span class="sxs-lookup"><span data-stu-id="4ce30-209">Foreign key: mshr_hcmworkerentityid of mshr_hcmworkerentity</span></span> | <span data-ttu-id="4ce30-210">Järjestelmän luoma sen työntekijän tunnus, joka tarkasti hakijan osaamistason.</span><span class="sxs-lookup"><span data-stu-id="4ce30-210">The system-generated identifier of the worker who examined the candidate’s skill level.</span></span> |
| <span data-ttu-id="4ce30-211">**Tarkistettu**</span><span class="sxs-lookup"><span data-stu-id="4ce30-211">**Verified**</span></span><br><span data-ttu-id="4ce30-212">mshr_verified</span><span class="sxs-lookup"><span data-stu-id="4ce30-212">mshr_verified</span></span><br><span data-ttu-id="4ce30-213">*mshr_noyes-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="4ce30-213">*mshr_noyes option set*</span></span> | <span data-ttu-id="4ce30-214">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="4ce30-214">Read/write</span></span><br><span data-ttu-id="4ce30-215">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-215">Required</span></span> | <span data-ttu-id="4ce30-216">Ilmaisee, onko arvioitu osaamisaluetaso varmennettu.</span><span class="sxs-lookup"><span data-stu-id="4ce30-216">Indicates whether the assessed skill level has been verified.</span></span> |
| <span data-ttu-id="4ce30-217">**Ensisijainen kenttä**</span><span class="sxs-lookup"><span data-stu-id="4ce30-217">**Primary Field**</span></span><br><span data-ttu-id="4ce30-218">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="4ce30-218">mshr_primaryfield</span></span><br><span data-ttu-id="4ce30-219">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4ce30-219">*String*</span></span> | <span data-ttu-id="4ce30-220">Vain luku</span><span class="sxs-lookup"><span data-stu-id="4ce30-220">Read-only</span></span><br><span data-ttu-id="4ce30-221">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="4ce30-221">Required</span></span> | <span data-ttu-id="4ce30-222">Kenttä, jota käytetään yksikkötietueen tunnuksena.</span><span class="sxs-lookup"><span data-stu-id="4ce30-222">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="4ce30-223">Osapuolen numeron, tason tyypin, osaamisaluetunnuksen ja tason päivämäärän yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="4ce30-223">Combination of party number, level type, skill ID, and level date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4ce30-224">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4ce30-224">See also</span></span>

[<span data-ttu-id="4ce30-225">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="4ce30-225">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4ce30-226">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="4ce30-226">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
