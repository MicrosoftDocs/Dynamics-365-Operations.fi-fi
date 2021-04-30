---
title: Palkanlaskennan tiedot toimista
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan tiedot toimiyksiköstä Dynamics 365 Human Resourcesissa.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881972"
---
# <a name="payroll-position"></a><span data-ttu-id="99ff5-103">Palkanlaskennan toimi</span><span class="sxs-lookup"><span data-stu-id="99ff5-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="99ff5-104">Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan tiedot toimiyksiköstä Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="99ff5-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="99ff5-105">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="99ff5-105">Properties</span></span>

| <span data-ttu-id="99ff5-106">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="99ff5-106">Property</span></span><br><span data-ttu-id="99ff5-107">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="99ff5-107">**Physical name**</span></span><br><span data-ttu-id="99ff5-108">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="99ff5-108">**_Type_**</span></span> | <span data-ttu-id="99ff5-109">Käytä</span><span class="sxs-lookup"><span data-stu-id="99ff5-109">Use</span></span> | <span data-ttu-id="99ff5-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="99ff5-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="99ff5-111">**Vuosittaiset vakiotunnit**</span><span class="sxs-lookup"><span data-stu-id="99ff5-111">**Annual regular hours**</span></span><br><span data-ttu-id="99ff5-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="99ff5-112">annualregularhours</span></span><br><span data-ttu-id="99ff5-113">*Desimaali*</span><span class="sxs-lookup"><span data-stu-id="99ff5-113">*Decimal*</span></span> | <span data-ttu-id="99ff5-114">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-114">Read-only</span></span><br><span data-ttu-id="99ff5-115">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-115">Required</span></span> | <span data-ttu-id="99ff5-116">Toimessa määritetyt vuosittaiset säännölliset tunnit.</span><span class="sxs-lookup"><span data-stu-id="99ff5-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="99ff5-117">**Palkanlaskennan toimen tiedot -yksikön tunnus**</span><span class="sxs-lookup"><span data-stu-id="99ff5-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="99ff5-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="99ff5-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="99ff5-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="99ff5-119">*Guid*</span></span> | <span data-ttu-id="99ff5-120">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-120">Required</span></span><br><span data-ttu-id="99ff5-121">Järjestelmän luoma.</span><span class="sxs-lookup"><span data-stu-id="99ff5-121">System generated.</span></span> | <span data-ttu-id="99ff5-122">Järjestelmän luoma GUID-arvo, jonka avulla toimi voidaan yksilöivästi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="99ff5-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="99ff5-123">**Ensisijainen kenttä**</span><span class="sxs-lookup"><span data-stu-id="99ff5-123">**Primary field**</span></span><br><span data-ttu-id="99ff5-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="99ff5-124">mshr_primaryfield</span></span><br><span data-ttu-id="99ff5-125">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="99ff5-125">*String*</span></span> | <span data-ttu-id="99ff5-126">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-126">Required</span></span><br><span data-ttu-id="99ff5-127">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="99ff5-127">System generated</span></span> |  |
| <span data-ttu-id="99ff5-128">**Toimen työn tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="99ff5-128">**Position job ID value**</span></span><br><span data-ttu-id="99ff5-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="99ff5-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="99ff5-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="99ff5-130">*GUID*</span></span> | <span data-ttu-id="99ff5-131">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-131">Read-only</span></span><br><span data-ttu-id="99ff5-132">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-132">Required</span></span><br><span data-ttu-id="99ff5-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="99ff5-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="99ff5-134">Toimeen liittyvän työn tunnus.</span><span class="sxs-lookup"><span data-stu-id="99ff5-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="99ff5-135">**Kiinteän kompensaatiosuunnitelman tunnuksen arvo**</span><span class="sxs-lookup"><span data-stu-id="99ff5-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="99ff5-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="99ff5-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="99ff5-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="99ff5-137">*GUID*</span></span> | <span data-ttu-id="99ff5-138">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-138">Read-only</span></span><br><span data-ttu-id="99ff5-139">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-139">Required</span></span><br><span data-ttu-id="99ff5-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="99ff5-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="99ff5-141">Toimeen liittyvän kiinteän kompensaatiosuunnitelman tunnus.</span><span class="sxs-lookup"><span data-stu-id="99ff5-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="99ff5-142">**Maksujakson tunnus**</span><span class="sxs-lookup"><span data-stu-id="99ff5-142">**Pay cycle ID**</span></span><br><span data-ttu-id="99ff5-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="99ff5-143">mshr_primaryfield</span></span><br><span data-ttu-id="99ff5-144">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="99ff5-144">*String*</span></span> | <span data-ttu-id="99ff5-145">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-145">Read-only</span></span><br><span data-ttu-id="99ff5-146">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-146">Required</span></span> | <span data-ttu-id="99ff5-147">Toimessa määritetty maksusykli.</span><span class="sxs-lookup"><span data-stu-id="99ff5-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="99ff5-148">**Yrityksen maksama**</span><span class="sxs-lookup"><span data-stu-id="99ff5-148">**Paid by legal entity**</span></span><br><span data-ttu-id="99ff5-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="99ff5-149">paidbylegalentity</span></span><br><span data-ttu-id="99ff5-150">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="99ff5-150">*String*</span></span> | <span data-ttu-id="99ff5-151">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-151">Read-only</span></span><br><span data-ttu-id="99ff5-152">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-152">Required</span></span> | <span data-ttu-id="99ff5-153">Maksun määräyksestä vastaavassa toimessa määritetty yritys.</span><span class="sxs-lookup"><span data-stu-id="99ff5-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="99ff5-154">**Toimen tunnus**</span><span class="sxs-lookup"><span data-stu-id="99ff5-154">**Position ID**</span></span><br><span data-ttu-id="99ff5-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="99ff5-155">mshr_positionid</span></span><br><span data-ttu-id="99ff5-156">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="99ff5-156">*String*</span></span> | <span data-ttu-id="99ff5-157">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-157">Read-only</span></span><br><span data-ttu-id="99ff5-158">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-158">Required</span></span> | <span data-ttu-id="99ff5-159">Toimen tunnus.</span><span class="sxs-lookup"><span data-stu-id="99ff5-159">The ID of the position.</span></span> |
| <span data-ttu-id="99ff5-160">**Voimassaolo päättyy**</span><span class="sxs-lookup"><span data-stu-id="99ff5-160">**Valid to**</span></span><br><span data-ttu-id="99ff5-161">validto</span><span class="sxs-lookup"><span data-stu-id="99ff5-161">validto</span></span><br><span data-ttu-id="99ff5-162">*Päivämäärä aika siirros*</span><span class="sxs-lookup"><span data-stu-id="99ff5-162">*Date Time Offset*</span></span> | <span data-ttu-id="99ff5-163">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-163">Read-only</span></span><br><span data-ttu-id="99ff5-164">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-164">Required</span></span> |<span data-ttu-id="99ff5-165">Päivämäärä, josta toimitiedot ovat voimassa.</span><span class="sxs-lookup"><span data-stu-id="99ff5-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="99ff5-166">**Voimassaolo alkaa**</span><span class="sxs-lookup"><span data-stu-id="99ff5-166">**Valid from**</span></span><br><span data-ttu-id="99ff5-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="99ff5-167">validfrom</span></span><br><span data-ttu-id="99ff5-168">*Päivämäärä aika siirros*</span><span class="sxs-lookup"><span data-stu-id="99ff5-168">*Date Time Offset*</span></span> | <span data-ttu-id="99ff5-169">Vain luku</span><span class="sxs-lookup"><span data-stu-id="99ff5-169">Read-only</span></span><br><span data-ttu-id="99ff5-170">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="99ff5-170">Required</span></span> |<span data-ttu-id="99ff5-171">Päivämäärä, johon toimitiedot ovat voimassa.</span><span class="sxs-lookup"><span data-stu-id="99ff5-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="99ff5-172">**Kysely**</span><span class="sxs-lookup"><span data-stu-id="99ff5-172">**Query**</span></span>

<span data-ttu-id="99ff5-173">**Pyyntö**</span><span class="sxs-lookup"><span data-stu-id="99ff5-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="99ff5-174">**Vastaus**</span><span class="sxs-lookup"><span data-stu-id="99ff5-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
