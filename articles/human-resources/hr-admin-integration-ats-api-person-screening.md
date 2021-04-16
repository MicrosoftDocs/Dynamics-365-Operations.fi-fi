---
title: Henkilön seulonta
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798030"
---
# <a name="person-screening"></a><span data-ttu-id="5605c-103">Henkilön seulonta</span><span class="sxs-lookup"><span data-stu-id="5605c-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5605c-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön seulonta -yksikköä.</span><span class="sxs-lookup"><span data-stu-id="5605c-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5605c-105">Fyysinen nimi: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="5605c-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="5605c-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="5605c-106">Description</span></span>

<span data-ttu-id="5605c-107">Tässä yksikössä kuvataan seulonnat, jotka hakija on läpäissyt tai jotka hänen pitää läpäistä työpaikkaa varten.</span><span class="sxs-lookup"><span data-stu-id="5605c-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5605c-108">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="5605c-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="5605c-109">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5605c-109">Properties</span></span>

| <span data-ttu-id="5605c-110">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="5605c-110">Property</span></span><br><span data-ttu-id="5605c-111">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="5605c-111">**Physical name**</span></span><br><span data-ttu-id="5605c-112">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="5605c-112">**_Type_**</span></span> | <span data-ttu-id="5605c-113">Käytä</span><span class="sxs-lookup"><span data-stu-id="5605c-113">Use</span></span> | <span data-ttu-id="5605c-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="5605c-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5605c-115">**Henkilön seulonnan yksikkötunnus**</span><span class="sxs-lookup"><span data-stu-id="5605c-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="5605c-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="5605c-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="5605c-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5605c-117">*GUID*</span></span> | <span data-ttu-id="5605c-118">Vain luku</span><span class="sxs-lookup"><span data-stu-id="5605c-118">Read-only</span></span><br><span data-ttu-id="5605c-119">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="5605c-119">Required</span></span><br><span data-ttu-id="5605c-120">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="5605c-120">System-generated</span></span> | <span data-ttu-id="5605c-121">Henkilön seulontatietueen yksilöivä ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="5605c-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="5605c-122">**Osapuolinumero**</span><span class="sxs-lookup"><span data-stu-id="5605c-122">**Party Number**</span></span><br><span data-ttu-id="5605c-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="5605c-123">mshr_partynumber</span></span><br><span data-ttu-id="5605c-124">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="5605c-124">*String*</span></span> | <span data-ttu-id="5605c-125">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="5605c-125">Read/write</span></span><br><span data-ttu-id="5605c-126">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="5605c-126">Required</span></span> | <span data-ttu-id="5605c-127">Hakijan osapuolen (henkilön) numero.</span><span class="sxs-lookup"><span data-stu-id="5605c-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="5605c-128">**Henkilötunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="5605c-128">**Person ID Value**</span></span><br><span data-ttu-id="5605c-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="5605c-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="5605c-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5605c-130">*GUID*</span></span> | <span data-ttu-id="5605c-131">Vain luku</span><span class="sxs-lookup"><span data-stu-id="5605c-131">Read-only</span></span><br><span data-ttu-id="5605c-132">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="5605c-132">Required</span></span><br><span data-ttu-id="5605c-133">Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="5605c-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="5605c-134">Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="5605c-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="5605c-135">**Seulontatyypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="5605c-135">**Screening Type ID**</span></span><br><span data-ttu-id="5605c-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="5605c-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="5605c-137">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="5605c-137">*String*</span></span> | <span data-ttu-id="5605c-138">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="5605c-138">Read/write</span></span><br><span data-ttu-id="5605c-139">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="5605c-139">Required</span></span><br><span data-ttu-id="5605c-140">Viiteavain: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="5605c-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="5605c-141">Human Resourcesin seulontatyypin tunnus.</span><span class="sxs-lookup"><span data-stu-id="5605c-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="5605c-142">**Seulontatyypin tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="5605c-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="5605c-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="5605c-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="5605c-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5605c-144">*GUID*</span></span> | <span data-ttu-id="5605c-145">Vain luku</span><span class="sxs-lookup"><span data-stu-id="5605c-145">Read-only</span></span><br><span data-ttu-id="5605c-146">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="5605c-146">Required</span></span><br><span data-ttu-id="5605c-147">Viiteavain: mshr_hcmscreeningtypeentity-yksikön mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="5605c-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="5605c-148">Järjestelmän luoma seulontatyypin tietueen tunnus liitetyssä yksikössä.</span><span class="sxs-lookup"><span data-stu-id="5605c-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="5605c-149">**Määräpäivä**</span><span class="sxs-lookup"><span data-stu-id="5605c-149">**Required By**</span></span><br><span data-ttu-id="5605c-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="5605c-150">mshr_requiredby</span></span><br><span data-ttu-id="5605c-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="5605c-151">*Datetime*</span></span> | <span data-ttu-id="5605c-152">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="5605c-152">Read/write</span></span><br><span data-ttu-id="5605c-153">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="5605c-153">Optional</span></span> | <span data-ttu-id="5605c-154">Päivämäärä, johon mennessä seulonnat on suoritettava loppuun.</span><span class="sxs-lookup"><span data-stu-id="5605c-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="5605c-155">**Tila**</span><span class="sxs-lookup"><span data-stu-id="5605c-155">**Status**</span></span><br><span data-ttu-id="5605c-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="5605c-156">mshr_status</span></span><br><span data-ttu-id="5605c-157">*mshr_hcmcompletionstatus-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="5605c-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="5605c-158">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="5605c-158">Read/write</span></span><br><span data-ttu-id="5605c-159">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="5605c-159">Required</span></span> | <span data-ttu-id="5605c-160">Hakijan tila seulonnalle.</span><span class="sxs-lookup"><span data-stu-id="5605c-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="5605c-161">**Valmistumispäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="5605c-161">**Completed Date**</span></span><br><span data-ttu-id="5605c-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="5605c-162">mshr_completeddate</span></span><br><span data-ttu-id="5605c-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="5605c-163">*Datetime*</span></span> | <span data-ttu-id="5605c-164">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="5605c-164">Read/write</span></span><br><span data-ttu-id="5605c-165">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="5605c-165">Optional</span></span> | <span data-ttu-id="5605c-166">Päivämäärä, jolloin seulonta suoritettiin loppuun.</span><span class="sxs-lookup"><span data-stu-id="5605c-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="5605c-167">**Muistiinpanot**</span><span class="sxs-lookup"><span data-stu-id="5605c-167">**Notes**</span></span><br><span data-ttu-id="5605c-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="5605c-168">mshr_note</span></span><br><span data-ttu-id="5605c-169">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="5605c-169">*String*</span></span> | <span data-ttu-id="5605c-170">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="5605c-170">Read/write</span></span><br><span data-ttu-id="5605c-171">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="5605c-171">Optional</span></span> | <span data-ttu-id="5605c-172">Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5605c-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5605c-173">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="5605c-173">See also</span></span>

[<span data-ttu-id="5605c-174">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="5605c-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5605c-175">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="5605c-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]