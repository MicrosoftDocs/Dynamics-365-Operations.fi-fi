---
title: Henkilön seulonta
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125374"
---
# <a name="person-screening"></a><span data-ttu-id="01de0-103">Henkilön seulonta</span><span class="sxs-lookup"><span data-stu-id="01de0-103">Person screening</span></span>

<span data-ttu-id="01de0-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.</span><span class="sxs-lookup"><span data-stu-id="01de0-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="01de0-105">Fyysinen nimi: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="01de0-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="01de0-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="01de0-106">Description</span></span>

<span data-ttu-id="01de0-107">Tässä yksikössä kuvataan seulonnat, jotka hakija on läpäissyt tai jotka hänen pitää läpäistä työpaikkaa varten.</span><span class="sxs-lookup"><span data-stu-id="01de0-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="01de0-108">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="01de0-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="01de0-109">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="01de0-109">Properties</span></span>

| <span data-ttu-id="01de0-110">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="01de0-110">Property</span></span><br><span data-ttu-id="01de0-111">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="01de0-111">**Physical name**</span></span><br><span data-ttu-id="01de0-112">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="01de0-112">**_Type_**</span></span> | <span data-ttu-id="01de0-113">Käytä</span><span class="sxs-lookup"><span data-stu-id="01de0-113">Use</span></span> | <span data-ttu-id="01de0-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="01de0-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="01de0-115">**Henkilön seulonnan yksikkötunnus**</span><span class="sxs-lookup"><span data-stu-id="01de0-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="01de0-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="01de0-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="01de0-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="01de0-117">*GUID*</span></span> | <span data-ttu-id="01de0-118">Vain luku</span><span class="sxs-lookup"><span data-stu-id="01de0-118">Read-only</span></span><br><span data-ttu-id="01de0-119">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="01de0-119">Required</span></span><br><span data-ttu-id="01de0-120">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="01de0-120">System-generated</span></span> | <span data-ttu-id="01de0-121">Henkilön seulontatietueen yksilöivä ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="01de0-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="01de0-122">**Osapuolinumero**</span><span class="sxs-lookup"><span data-stu-id="01de0-122">**Party Number**</span></span><br><span data-ttu-id="01de0-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="01de0-123">mshr_partynumber</span></span><br><span data-ttu-id="01de0-124">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="01de0-124">*String*</span></span> | <span data-ttu-id="01de0-125">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="01de0-125">Read/write</span></span><br><span data-ttu-id="01de0-126">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="01de0-126">Required</span></span> | <span data-ttu-id="01de0-127">Hakijan osapuolen (henkilön) numero.</span><span class="sxs-lookup"><span data-stu-id="01de0-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="01de0-128">**Henkilötunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="01de0-128">**Person ID Value**</span></span><br><span data-ttu-id="01de0-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="01de0-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="01de0-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="01de0-130">*GUID*</span></span> | <span data-ttu-id="01de0-131">Vain luku</span><span class="sxs-lookup"><span data-stu-id="01de0-131">Read-only</span></span><br><span data-ttu-id="01de0-132">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="01de0-132">Required</span></span><br><span data-ttu-id="01de0-133">Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="01de0-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="01de0-134">Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="01de0-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="01de0-135">**Seulontatyypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="01de0-135">**Screening Type ID**</span></span><br><span data-ttu-id="01de0-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="01de0-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="01de0-137">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="01de0-137">*String*</span></span> | <span data-ttu-id="01de0-138">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="01de0-138">Read/write</span></span><br><span data-ttu-id="01de0-139">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="01de0-139">Required</span></span><br><span data-ttu-id="01de0-140">Viiteavain: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="01de0-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="01de0-141">Human Resourcesin seulontatyypin tunnus.</span><span class="sxs-lookup"><span data-stu-id="01de0-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="01de0-142">**Seulontatyypin tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="01de0-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="01de0-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="01de0-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="01de0-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="01de0-144">*GUID*</span></span> | <span data-ttu-id="01de0-145">Vain luku</span><span class="sxs-lookup"><span data-stu-id="01de0-145">Read-only</span></span><br><span data-ttu-id="01de0-146">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="01de0-146">Required</span></span><br><span data-ttu-id="01de0-147">Viiteavain: mshr_hcmscreeningtypeentity-yksikön mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="01de0-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="01de0-148">Järjestelmän luoma seulontatyypin tietueen tunnus liitetyssä yksikössä.</span><span class="sxs-lookup"><span data-stu-id="01de0-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="01de0-149">**Määräpäivä**</span><span class="sxs-lookup"><span data-stu-id="01de0-149">**Required By**</span></span><br><span data-ttu-id="01de0-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="01de0-150">mshr_requiredby</span></span><br><span data-ttu-id="01de0-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="01de0-151">*Datetime*</span></span> | <span data-ttu-id="01de0-152">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="01de0-152">Read/write</span></span><br><span data-ttu-id="01de0-153">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="01de0-153">Optional</span></span> | <span data-ttu-id="01de0-154">Päivämäärä, johon mennessä seulonnat on suoritettava loppuun.</span><span class="sxs-lookup"><span data-stu-id="01de0-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="01de0-155">**Tila**</span><span class="sxs-lookup"><span data-stu-id="01de0-155">**Status**</span></span><br><span data-ttu-id="01de0-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="01de0-156">mshr_status</span></span><br><span data-ttu-id="01de0-157">*mshr_hcmcompletionstatus-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="01de0-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="01de0-158">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="01de0-158">Read/write</span></span><br><span data-ttu-id="01de0-159">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="01de0-159">Required</span></span> | <span data-ttu-id="01de0-160">Hakijan tila seulonnalle.</span><span class="sxs-lookup"><span data-stu-id="01de0-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="01de0-161">**Valmistumispäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="01de0-161">**Completed Date**</span></span><br><span data-ttu-id="01de0-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="01de0-162">mshr_completeddate</span></span><br><span data-ttu-id="01de0-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="01de0-163">*Datetime*</span></span> | <span data-ttu-id="01de0-164">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="01de0-164">Read/write</span></span><br><span data-ttu-id="01de0-165">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="01de0-165">Optional</span></span> | <span data-ttu-id="01de0-166">Päivämäärä, jolloin seulonta suoritettiin loppuun.</span><span class="sxs-lookup"><span data-stu-id="01de0-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="01de0-167">**Muistiinpanot**</span><span class="sxs-lookup"><span data-stu-id="01de0-167">**Notes**</span></span><br><span data-ttu-id="01de0-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="01de0-168">mshr_note</span></span><br><span data-ttu-id="01de0-169">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="01de0-169">*String*</span></span> | <span data-ttu-id="01de0-170">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="01de0-170">Read/write</span></span><br><span data-ttu-id="01de0-171">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="01de0-171">Optional</span></span> | <span data-ttu-id="01de0-172">Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön.</span><span class="sxs-lookup"><span data-stu-id="01de0-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="01de0-173">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="01de0-173">See also</span></span>

[<span data-ttu-id="01de0-174">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="01de0-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="01de0-175">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="01de0-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

