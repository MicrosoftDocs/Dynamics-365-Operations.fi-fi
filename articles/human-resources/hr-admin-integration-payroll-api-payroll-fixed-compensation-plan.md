---
title: Palkanlaskennan kiinteän kompensaation suunnitelma
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan kiinteän kompensaatiosuunnitelman yksiköstä Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881977"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="74ba9-103">Palkanlaskennan kiinteän kompensaation suunnitelma</span><span class="sxs-lookup"><span data-stu-id="74ba9-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="74ba9-104">Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan kiinteän kompensaatiosuunnitelman yksiköstä Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="74ba9-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="74ba9-105">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="74ba9-105">Properties</span></span>

| <span data-ttu-id="74ba9-106">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="74ba9-106">Property</span></span><br><span data-ttu-id="74ba9-107">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="74ba9-107">**Physical name**</span></span><br><span data-ttu-id="74ba9-108">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="74ba9-108">**_Type_**</span></span> | <span data-ttu-id="74ba9-109">Käytä</span><span class="sxs-lookup"><span data-stu-id="74ba9-109">Use</span></span> | <span data-ttu-id="74ba9-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="74ba9-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="74ba9-111">**Työntekijän tunnus**</span><span class="sxs-lookup"><span data-stu-id="74ba9-111">**Employee ID**</span></span><br><span data-ttu-id="74ba9-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="74ba9-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="74ba9-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="74ba9-113">*GUID*</span></span> | <span data-ttu-id="74ba9-114">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-114">Read-only</span></span><br><span data-ttu-id="74ba9-115">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-115">Required</span></span><br><span data-ttu-id="74ba9-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="74ba9-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="74ba9-117">Työntekijän tunnus</span><span class="sxs-lookup"><span data-stu-id="74ba9-117">Employee ID</span></span> |
| <span data-ttu-id="74ba9-118">**Palkkio**</span><span class="sxs-lookup"><span data-stu-id="74ba9-118">**Pay rate**</span></span><br><span data-ttu-id="74ba9-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="74ba9-119">mshr_payrate</span></span><br><span data-ttu-id="74ba9-120">*Desimaali*</span><span class="sxs-lookup"><span data-stu-id="74ba9-120">*Decimal*</span></span> | <span data-ttu-id="74ba9-121">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-121">Read-only</span></span><br><span data-ttu-id="74ba9-122">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-122">Required</span></span> | <span data-ttu-id="74ba9-123">Kiinteässä kompensaatiosuunnitelmassa määritetty palkkio.</span><span class="sxs-lookup"><span data-stu-id="74ba9-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="74ba9-124">**Suunnitelman tunnus**</span><span class="sxs-lookup"><span data-stu-id="74ba9-124">**Plan ID**</span></span><br><span data-ttu-id="74ba9-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="74ba9-125">mshr_planid</span></span><br><span data-ttu-id="74ba9-126">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="74ba9-126">*String*</span></span> | <span data-ttu-id="74ba9-127">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-127">Read-only</span></span><br><span data-ttu-id="74ba9-128">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-128">Required</span></span> |<span data-ttu-id="74ba9-129">Määrittää kompensaatiosuunnitelman.</span><span class="sxs-lookup"><span data-stu-id="74ba9-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="74ba9-130">**Voimassaolo alkaa**</span><span class="sxs-lookup"><span data-stu-id="74ba9-130">**Valid from**</span></span><br><span data-ttu-id="74ba9-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="74ba9-131">mshr_validfrom</span></span><br><span data-ttu-id="74ba9-132">*Päivämäärä aika siirros*</span><span class="sxs-lookup"><span data-stu-id="74ba9-132">*Date Time Offset*</span></span> |  <span data-ttu-id="74ba9-133">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-133">Read-only</span></span><br><span data-ttu-id="74ba9-134">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-134">Required</span></span> |<span data-ttu-id="74ba9-135">Päivämäärä, josta alkaen työntekijän kiinteä kompensaatio on voimassa.</span><span class="sxs-lookup"><span data-stu-id="74ba9-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="74ba9-136">**Palkanlaskennan kiinteän kompensaatiosuunnitelman yksikkö**</span><span class="sxs-lookup"><span data-stu-id="74ba9-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="74ba9-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="74ba9-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="74ba9-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="74ba9-138">*GUID*</span></span> | <span data-ttu-id="74ba9-139">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-139">Required</span></span><br><span data-ttu-id="74ba9-140">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="74ba9-140">Sytem generated</span></span> | <span data-ttu-id="74ba9-141">Järjestelmän luoma GUID-arvo, jonka avulla kompensaatiosuunnitelma voidaan yksilöivästi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="74ba9-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="74ba9-142">**Maksutiheys**</span><span class="sxs-lookup"><span data-stu-id="74ba9-142">**Pay frequency**</span></span><br><span data-ttu-id="74ba9-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="74ba9-143">mshr_payfrequency</span></span><br><span data-ttu-id="74ba9-144">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="74ba9-144">*String*</span></span> | <span data-ttu-id="74ba9-145">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-145">Read-only</span></span><br><span data-ttu-id="74ba9-146">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-146">Required</span></span> |<span data-ttu-id="74ba9-147">Kuinka usein työntekijälle maksetaan palkkoja.</span><span class="sxs-lookup"><span data-stu-id="74ba9-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="74ba9-148">**Voimassaolo päättyy**</span><span class="sxs-lookup"><span data-stu-id="74ba9-148">**Valid to**</span></span><br><span data-ttu-id="74ba9-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="74ba9-149">mshr_validto</span></span><br><span data-ttu-id="74ba9-150">*Päivämäärä aika siirros*</span><span class="sxs-lookup"><span data-stu-id="74ba9-150">*Date Time Offset*</span></span> | <span data-ttu-id="74ba9-151">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-151">Read-only</span></span> <br><span data-ttu-id="74ba9-152">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-152">Required</span></span> | <span data-ttu-id="74ba9-153">Päivämäärä, johon asti työntekijän kiinteä kompensaatio on voimassa.</span><span class="sxs-lookup"><span data-stu-id="74ba9-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="74ba9-154">**Toimen tunnus**</span><span class="sxs-lookup"><span data-stu-id="74ba9-154">**Position ID**</span></span><br><span data-ttu-id="74ba9-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="74ba9-155">mshr_positionid</span></span><br><span data-ttu-id="74ba9-156">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="74ba9-156">*String*</span></span> | <span data-ttu-id="74ba9-157">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-157">Read-only</span></span> <br><span data-ttu-id="74ba9-158">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-158">Required</span></span> | <span data-ttu-id="74ba9-159">Työntekijän ja kiinteän kompensaatiosuunnitelman rekisteröintiin liittyvä postitustunnus.</span><span class="sxs-lookup"><span data-stu-id="74ba9-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="74ba9-160">**Valuutta**</span><span class="sxs-lookup"><span data-stu-id="74ba9-160">**Currency**</span></span><br><span data-ttu-id="74ba9-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="74ba9-161">mshr_currency</span></span><br><span data-ttu-id="74ba9-162">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="74ba9-162">*String*</span></span> | <span data-ttu-id="74ba9-163">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-163">Read-only</span></span> <br><span data-ttu-id="74ba9-164">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-164">Required</span></span> |<span data-ttu-id="74ba9-165">Kiinteälle kompensaatiosuunnitelmalle määritetty valuutta</span><span class="sxs-lookup"><span data-stu-id="74ba9-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="74ba9-166">**Henkilöstönumero**</span><span class="sxs-lookup"><span data-stu-id="74ba9-166">**Personnel number**</span></span><br><span data-ttu-id="74ba9-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="74ba9-167">mshr_personnelnumber</span></span><br><span data-ttu-id="74ba9-168">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="74ba9-168">*String*</span></span> | <span data-ttu-id="74ba9-169">Vain luku</span><span class="sxs-lookup"><span data-stu-id="74ba9-169">Read-only</span></span><br><span data-ttu-id="74ba9-170">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="74ba9-170">Required</span></span> |<span data-ttu-id="74ba9-171">Työntekijän yksilöivä henkilökuntanumero.</span><span class="sxs-lookup"><span data-stu-id="74ba9-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="74ba9-172">**Kysely**</span><span class="sxs-lookup"><span data-stu-id="74ba9-172">**Query**</span></span>

<span data-ttu-id="74ba9-173">**Pyyntö**</span><span class="sxs-lookup"><span data-stu-id="74ba9-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="74ba9-174">**Vastaus**</span><span class="sxs-lookup"><span data-stu-id="74ba9-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
