---
title: Henkilön todistus
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön todistus -yksikköä.
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
ms.openlocfilehash: 796a57a5f97de08ff8c8440bc00d4dc5ced18f58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798126"
---
# <a name="person-certificate"></a><span data-ttu-id="fdd9e-103">Henkilön todistus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fdd9e-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Henkilön todistus -yksikköä.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="fdd9e-105">Fyysinen nimi: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="fdd9e-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="fdd9e-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-106">Description</span></span>

<span data-ttu-id="fdd9e-107">Tämä yksikkö kuvaa hakijan ammattitodistuksia.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fdd9e-108">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="fdd9e-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="fdd9e-109">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="fdd9e-109">Properties</span></span>

| <span data-ttu-id="fdd9e-110">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-110">Property</span></span><br><span data-ttu-id="fdd9e-111">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-111">**Physical name**</span></span><br><span data-ttu-id="fdd9e-112">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-112">**_Type_**</span></span> | <span data-ttu-id="fdd9e-113">Käytä</span><span class="sxs-lookup"><span data-stu-id="fdd9e-113">Use</span></span> | <span data-ttu-id="fdd9e-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fdd9e-115">**Henkilön todistuksen yksikkötunnus**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="fdd9e-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="fdd9e-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="fdd9e-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-117">*GUID*</span></span> | <span data-ttu-id="fdd9e-118">Vain luku</span><span class="sxs-lookup"><span data-stu-id="fdd9e-118">Read-only</span></span><br><span data-ttu-id="fdd9e-119">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-119">Required</span></span> | <span data-ttu-id="fdd9e-120">Järjestelmän luoma henkilön todistuksen yksikkötietueen yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="fdd9e-121">**Osapuolinumero**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-121">**Party Number**</span></span><br><span data-ttu-id="fdd9e-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="fdd9e-122">mshr_partynumber</span></span><br><span data-ttu-id="fdd9e-123">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-123">*String*</span></span> | <span data-ttu-id="fdd9e-124">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-124">Read/write</span></span><br><span data-ttu-id="fdd9e-125">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-125">Required</span></span> | <span data-ttu-id="fdd9e-126">Hakijan osapuolen (henkilön) tunnus.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="fdd9e-127">**Henkilötunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-127">**Person ID Value**</span></span><br><span data-ttu-id="fdd9e-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="fdd9e-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="fdd9e-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-129">*GUID*</span></span> | <span data-ttu-id="fdd9e-130">Vain luku</span><span class="sxs-lookup"><span data-stu-id="fdd9e-130">Read-only</span></span><br><span data-ttu-id="fdd9e-131">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-131">Required</span></span><br><span data-ttu-id="fdd9e-132">Viiteavain: mshr_dirpersonentity-yksikön mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="fdd9e-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="fdd9e-133">Järjestelmän luoma osapuolen (henkilön) yksikkötietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="fdd9e-134">**Todistuksen tyypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-134">**Certificate Type ID**</span></span><br><span data-ttu-id="fdd9e-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="fdd9e-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="fdd9e-136">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-136">*String*</span></span> | <span data-ttu-id="fdd9e-137">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-137">Read/write</span></span><br><span data-ttu-id="fdd9e-138">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-138">Required</span></span> |  <span data-ttu-id="fdd9e-139">Human Resourcesin todistustyypin tunnus.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="fdd9e-140">**Todistuksen tyypin tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="fdd9e-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="fdd9e-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="fdd9e-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-142">*GUID*</span></span> | <span data-ttu-id="fdd9e-143">Vain luku</span><span class="sxs-lookup"><span data-stu-id="fdd9e-143">Read-only</span></span><br><span data-ttu-id="fdd9e-144">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-144">Required</span></span><br><span data-ttu-id="fdd9e-145">Viiteavain: mshr_hcmcertificatetypeentity-yksikön mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="fdd9e-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="fdd9e-146">Järjestelmän luoma todistustyypin tietueen yksilöivä tunnus liitetyssä yksikössä.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="fdd9e-147">**Aloituspäivä**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-147">**Start Date**</span></span><br><span data-ttu-id="fdd9e-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="fdd9e-148">mshr_startdate</span></span><br><span data-ttu-id="fdd9e-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-149">*Datetime*</span></span> | <span data-ttu-id="fdd9e-150">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-150">Read/write</span></span><br><span data-ttu-id="fdd9e-151">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-151">Required</span></span> | <span data-ttu-id="fdd9e-152">Päivä, jolloin todistus myönnettiin.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="fdd9e-153">**Päättymispäivä**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-153">**End Date**</span></span><br><span data-ttu-id="fdd9e-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="fdd9e-154">mshr_enddate</span></span><br><span data-ttu-id="fdd9e-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-155">*Datetime*</span></span> | <span data-ttu-id="fdd9e-156">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-156">Read/write</span></span><br><span data-ttu-id="fdd9e-157">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="fdd9e-157">Optional</span></span> | <span data-ttu-id="fdd9e-158">Päivä, jolloin todistus vanhenee.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="fdd9e-159">**Muistiinpanot**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-159">**Notes**</span></span><br><span data-ttu-id="fdd9e-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="fdd9e-160">mshr_notes</span></span><br><span data-ttu-id="fdd9e-161">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-161">*String*</span></span> | <span data-ttu-id="fdd9e-162">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="fdd9e-162">Read/write</span></span><br><span data-ttu-id="fdd9e-163">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="fdd9e-163">Optional</span></span> | <span data-ttu-id="fdd9e-164">Muistiinpanot rekrytoijan ja työhönottopäällikön käyttöön.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="fdd9e-165">**Ensisijainen kenttä**</span><span class="sxs-lookup"><span data-stu-id="fdd9e-165">**Primary Field**</span></span><br><span data-ttu-id="fdd9e-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="fdd9e-166">mshr_primaryfield</span></span><br><span data-ttu-id="fdd9e-167">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="fdd9e-167">*String*</span></span> | <span data-ttu-id="fdd9e-168">Vain luku</span><span class="sxs-lookup"><span data-stu-id="fdd9e-168">Read-only</span></span><br><span data-ttu-id="fdd9e-169">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="fdd9e-169">Required</span></span> |  <span data-ttu-id="fdd9e-170">Kenttä, jota käytetään yksikkötietueen tunnuksena.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="fdd9e-171">Osapuolen numeron, todistus tyypin tunnuksen ja alkamispäivämäärän yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="fdd9e-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fdd9e-172">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="fdd9e-172">See also</span></span>

[<span data-ttu-id="fdd9e-173">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="fdd9e-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="fdd9e-174">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="fdd9e-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]