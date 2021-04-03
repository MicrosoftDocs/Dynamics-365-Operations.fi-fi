---
title: Seulontatyypit
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465915"
---
# <a name="screening-types"></a><span data-ttu-id="091cc-103">Seulontatyypit</span><span class="sxs-lookup"><span data-stu-id="091cc-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="091cc-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.</span><span class="sxs-lookup"><span data-stu-id="091cc-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="091cc-105">Fyysinen nimi: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="091cc-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="091cc-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="091cc-106">Description</span></span>

<span data-ttu-id="091cc-107">Tässä yksikössä kuvataan seulontatyypit, jotka yritys on määrittänyt työsuhdetta edeltäville ja meneillään olevien työsuhteiden seulontaprosesseihin.</span><span class="sxs-lookup"><span data-stu-id="091cc-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="091cc-108">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="091cc-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="091cc-109">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="091cc-109">Properties</span></span>

| <span data-ttu-id="091cc-110">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="091cc-110">Property</span></span><br><span data-ttu-id="091cc-111">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="091cc-111">**Physical name**</span></span><br><span data-ttu-id="091cc-112">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="091cc-112">**_Type_**</span></span> | <span data-ttu-id="091cc-113">Käytä</span><span class="sxs-lookup"><span data-stu-id="091cc-113">Use</span></span> | <span data-ttu-id="091cc-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="091cc-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="091cc-115">**Seulontatyypin yksikön tunnus**</span><span class="sxs-lookup"><span data-stu-id="091cc-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="091cc-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="091cc-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="091cc-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="091cc-117">*GUID*</span></span> | <span data-ttu-id="091cc-118">Vain luku</span><span class="sxs-lookup"><span data-stu-id="091cc-118">Read-only</span></span><br><span data-ttu-id="091cc-119">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="091cc-119">Required</span></span><br><span data-ttu-id="091cc-120">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="091cc-120">System-generated</span></span> | <span data-ttu-id="091cc-121">Seulontatyypin tietueen yksilöivä ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="091cc-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="091cc-122">**Seulontatyypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="091cc-122">**Screening Type ID**</span></span><br><span data-ttu-id="091cc-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="091cc-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="091cc-124">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="091cc-124">*String*</span></span> | <span data-ttu-id="091cc-125">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="091cc-125">Read/write</span></span><br><span data-ttu-id="091cc-126">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="091cc-126">Required</span></span> | <span data-ttu-id="091cc-127">Käyttäjän määrittämä seulontatyypin yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="091cc-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="091cc-128">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="091cc-128">**Description**</span></span><br><span data-ttu-id="091cc-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="091cc-129">mshr_description</span></span><br><span data-ttu-id="091cc-130">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="091cc-130">*String*</span></span> | <span data-ttu-id="091cc-131">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="091cc-131">Read/write</span></span><br><span data-ttu-id="091cc-132">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="091cc-132">Required</span></span> | <span data-ttu-id="091cc-133">Seulontatyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="091cc-133">The description of the screening type.</span></span> |
| <span data-ttu-id="091cc-134">**Tiheyden yksikkö**</span><span class="sxs-lookup"><span data-stu-id="091cc-134">**Frequency Unit**</span></span><br><span data-ttu-id="091cc-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="091cc-135">mshr_frequencyunit</span></span><br><span data-ttu-id="091cc-136">*mshr_hcmfrequencyunit-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="091cc-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="091cc-137">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="091cc-137">Read/write</span></span><br><span data-ttu-id="091cc-138">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="091cc-138">Required</span></span> | <span data-ttu-id="091cc-139">Kuvaa, millä tiheydellä seulonta on suoritettava määritetylle henkilölle.</span><span class="sxs-lookup"><span data-stu-id="091cc-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="091cc-140">**Luo kohteesta**</span><span class="sxs-lookup"><span data-stu-id="091cc-140">**Generate From**</span></span><br><span data-ttu-id="091cc-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="091cc-141">mshr_generatefrom</span></span><br><span data-ttu-id="091cc-142">*mshr_hcmfrequencygeneratefrom-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="091cc-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="091cc-143">Luku-Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="091cc-143">Read-write</span></span><br><span data-ttu-id="091cc-144">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="091cc-144">Required</span></span> | <span data-ttu-id="091cc-145">Jos Tiheys-arvo on jokin muu kuin "Vain kerran", GenerateFrom-arvo määrittää päivämäärän, josta seuraava seulontatapahtuma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="091cc-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="091cc-146">**Tiheysväli**</span><span class="sxs-lookup"><span data-stu-id="091cc-146">**Frequency Interval**</span></span><br><span data-ttu-id="091cc-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="091cc-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="091cc-148">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="091cc-148">*Integer*</span></span> | <span data-ttu-id="091cc-149">Luku-Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="091cc-149">Read-write</span></span><br><span data-ttu-id="091cc-150">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="091cc-150">Required</span></span> | <span data-ttu-id="091cc-151">Jos Tiheys-arvo on jokin muu kuin "Vain kerran", sinun on määritettävä seulontatapahtumien välisten aikayksiköiden aikaväli.</span><span class="sxs-lookup"><span data-stu-id="091cc-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="091cc-152">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="091cc-152">See also</span></span>

[<span data-ttu-id="091cc-153">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="091cc-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="091cc-154">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="091cc-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]