---
title: Luokitustaso
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Luokitustaso-yksikköä.
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
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800330"
---
# <a name="rating-level"></a><span data-ttu-id="9969c-103">Luokitustaso</span><span class="sxs-lookup"><span data-stu-id="9969c-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9969c-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Luokitustaso-yksikköä.</span><span class="sxs-lookup"><span data-stu-id="9969c-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9969c-105">Fyysinen nimi: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="9969c-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="9969c-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="9969c-106">Description</span></span>

<span data-ttu-id="9969c-107">Tämä yksikkö tarjoaa käytettävissä olevat osaamisalueluokituksen tasot.</span><span class="sxs-lookup"><span data-stu-id="9969c-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="9969c-108">Luokitustasoja käytetään kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="9969c-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9969c-109">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="9969c-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="9969c-110">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="9969c-110">Properties</span></span>

| <span data-ttu-id="9969c-111">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="9969c-111">Property</span></span><br><span data-ttu-id="9969c-112">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="9969c-112">**Physical name**</span></span><br><span data-ttu-id="9969c-113">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="9969c-113">**_Type_**</span></span> | <span data-ttu-id="9969c-114">Käytä</span><span class="sxs-lookup"><span data-stu-id="9969c-114">Use</span></span> | <span data-ttu-id="9969c-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="9969c-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9969c-116">**Luokitustason yksikön tunnus**</span><span class="sxs-lookup"><span data-stu-id="9969c-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="9969c-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="9969c-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="9969c-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9969c-118">*GUID*</span></span> | <span data-ttu-id="9969c-119">Vain luku</span><span class="sxs-lookup"><span data-stu-id="9969c-119">Read-only</span></span><br><span data-ttu-id="9969c-120">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-120">Required</span></span><br><span data-ttu-id="9969c-121">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="9969c-121">System-generated</span></span> | <span data-ttu-id="9969c-122">Järjestelmän luoma tason yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="9969c-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="9969c-123">**Luokitustason tunnus**</span><span class="sxs-lookup"><span data-stu-id="9969c-123">**Rating Level ID**</span></span><br><span data-ttu-id="9969c-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="9969c-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="9969c-125">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9969c-125">*String*</span></span> | <span data-ttu-id="9969c-126">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="9969c-126">Read/write</span></span><br><span data-ttu-id="9969c-127">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-127">Required</span></span> | <span data-ttu-id="9969c-128">Käyttäjän luettava tason yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="9969c-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="9969c-129">**Luokitusmallin tunnus**</span><span class="sxs-lookup"><span data-stu-id="9969c-129">**Rating Model ID**</span></span><br><span data-ttu-id="9969c-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="9969c-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="9969c-131">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9969c-131">*String*</span></span> | <span data-ttu-id="9969c-132">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="9969c-132">Read/write</span></span><br><span data-ttu-id="9969c-133">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-133">Required</span></span> | <span data-ttu-id="9969c-134">Luokitusmalli, johon luokitustaso kuuluu.</span><span class="sxs-lookup"><span data-stu-id="9969c-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="9969c-135">**Luokitusmallin yksikön tunnus**</span><span class="sxs-lookup"><span data-stu-id="9969c-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="9969c-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="9969c-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="9969c-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9969c-137">*GUID*</span></span> | <span data-ttu-id="9969c-138">Vain luku</span><span class="sxs-lookup"><span data-stu-id="9969c-138">Read-only</span></span><br><span data-ttu-id="9969c-139">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-139">Required</span></span><br><span data-ttu-id="9969c-140">Viiteavain: mshr_hcmratingmodelentity-yksikön mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="9969c-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="9969c-141">Järjestelmän luoma sen luokitusmallin tunnus, johon luokitustaso kuuluu.</span><span class="sxs-lookup"><span data-stu-id="9969c-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="9969c-142">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="9969c-142">**Description**</span></span><br><span data-ttu-id="9969c-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="9969c-143">mshr_description</span></span><br><span data-ttu-id="9969c-144">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9969c-144">*String*</span></span> | <span data-ttu-id="9969c-145">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="9969c-145">Read/write</span></span><br><span data-ttu-id="9969c-146">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-146">Required</span></span> | <span data-ttu-id="9969c-147">Luokitustason kuvaus.</span><span class="sxs-lookup"><span data-stu-id="9969c-147">The description of the rating level.</span></span> |
| <span data-ttu-id="9969c-148">**Kerroin**</span><span class="sxs-lookup"><span data-stu-id="9969c-148">**Factor**</span></span><br><span data-ttu-id="9969c-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="9969c-149">mshr_factor</span></span><br><span data-ttu-id="9969c-150">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="9969c-150">*Integer*</span></span> | <span data-ttu-id="9969c-151">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="9969c-151">Read/write</span></span><br><span data-ttu-id="9969c-152">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-152">Required</span></span> | <span data-ttu-id="9969c-153">Luokitustason kerroin.</span><span class="sxs-lookup"><span data-stu-id="9969c-153">The factor for the rating level.</span></span> <span data-ttu-id="9969c-154">Kun vertaat nimikkeitä, joissa on eri määrä tasoja, kerrointa käytetään tulosten normalisointiin.</span><span class="sxs-lookup"><span data-stu-id="9969c-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="9969c-155">Arvon on oltava kokonaisluku väliltä 0–9.</span><span class="sxs-lookup"><span data-stu-id="9969c-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="9969c-156">**Huomautus**</span><span class="sxs-lookup"><span data-stu-id="9969c-156">**Note**</span></span><br><span data-ttu-id="9969c-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="9969c-157">mshr_note</span></span><br><span data-ttu-id="9969c-158">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9969c-158">*String*</span></span> | <span data-ttu-id="9969c-159">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="9969c-159">Read/write</span></span><br><span data-ttu-id="9969c-160">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="9969c-160">Optional</span></span> | <span data-ttu-id="9969c-161">Luokitustasoon liittyvät huomautukset.</span><span class="sxs-lookup"><span data-stu-id="9969c-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="9969c-162">**Ensisijainen kenttä**</span><span class="sxs-lookup"><span data-stu-id="9969c-162">**Primary Field**</span></span><br><span data-ttu-id="9969c-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9969c-163">mshr_primaryfield</span></span><br><span data-ttu-id="9969c-164">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="9969c-164">*String*</span></span> | <span data-ttu-id="9969c-165">Vain luku</span><span class="sxs-lookup"><span data-stu-id="9969c-165">Read-only</span></span><br><span data-ttu-id="9969c-166">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="9969c-166">Required</span></span> | <span data-ttu-id="9969c-167">Kenttä, jota käytetään yksikkötietueen tunnuksena.</span><span class="sxs-lookup"><span data-stu-id="9969c-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="9969c-168">Luokitustason tunnuksen ja luokitusmallin tunnuksen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="9969c-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9969c-169">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="9969c-169">See also</span></span>

[<span data-ttu-id="9969c-170">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="9969c-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9969c-171">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="9969c-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]