---
title: Seulontatyypit
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb99c2fb57df883ab376c7f6aab547073bd0ff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058293"
---
# <a name="screening-types"></a><span data-ttu-id="3f945-103">Seulontatyypit</span><span class="sxs-lookup"><span data-stu-id="3f945-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f945-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Seulontatyypit-yksikköä.</span><span class="sxs-lookup"><span data-stu-id="3f945-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3f945-105">Fyysinen nimi: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="3f945-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="3f945-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="3f945-106">Description</span></span>

<span data-ttu-id="3f945-107">Tässä yksikössä kuvataan seulontatyypit, jotka yritys on määrittänyt työsuhdetta edeltäville ja meneillään olevien työsuhteiden seulontaprosesseihin.</span><span class="sxs-lookup"><span data-stu-id="3f945-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3f945-108">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="3f945-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="3f945-109">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="3f945-109">Properties</span></span>

| <span data-ttu-id="3f945-110">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="3f945-110">Property</span></span><br><span data-ttu-id="3f945-111">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="3f945-111">**Physical name**</span></span><br><span data-ttu-id="3f945-112">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="3f945-112">**_Type_**</span></span> | <span data-ttu-id="3f945-113">Käytä</span><span class="sxs-lookup"><span data-stu-id="3f945-113">Use</span></span> | <span data-ttu-id="3f945-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="3f945-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3f945-115">**Seulontatyypin yksikön tunnus**</span><span class="sxs-lookup"><span data-stu-id="3f945-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="3f945-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="3f945-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="3f945-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3f945-117">*GUID*</span></span> | <span data-ttu-id="3f945-118">Vain luku</span><span class="sxs-lookup"><span data-stu-id="3f945-118">Read-only</span></span><br><span data-ttu-id="3f945-119">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="3f945-119">Required</span></span><br><span data-ttu-id="3f945-120">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="3f945-120">System-generated</span></span> | <span data-ttu-id="3f945-121">Seulontatyypin tietueen yksilöivä ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="3f945-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="3f945-122">**Seulontatyypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="3f945-122">**Screening Type ID**</span></span><br><span data-ttu-id="3f945-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="3f945-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="3f945-124">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="3f945-124">*String*</span></span> | <span data-ttu-id="3f945-125">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="3f945-125">Read/write</span></span><br><span data-ttu-id="3f945-126">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="3f945-126">Required</span></span> | <span data-ttu-id="3f945-127">Käyttäjän määrittämä seulontatyypin yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="3f945-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="3f945-128">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="3f945-128">**Description**</span></span><br><span data-ttu-id="3f945-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3f945-129">mshr_description</span></span><br><span data-ttu-id="3f945-130">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="3f945-130">*String*</span></span> | <span data-ttu-id="3f945-131">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="3f945-131">Read/write</span></span><br><span data-ttu-id="3f945-132">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="3f945-132">Required</span></span> | <span data-ttu-id="3f945-133">Seulontatyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3f945-133">The description of the screening type.</span></span> |
| <span data-ttu-id="3f945-134">**Tiheyden yksikkö**</span><span class="sxs-lookup"><span data-stu-id="3f945-134">**Frequency Unit**</span></span><br><span data-ttu-id="3f945-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="3f945-135">mshr_frequencyunit</span></span><br><span data-ttu-id="3f945-136">*mshr_hcmfrequencyunit-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="3f945-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="3f945-137">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="3f945-137">Read/write</span></span><br><span data-ttu-id="3f945-138">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="3f945-138">Required</span></span> | <span data-ttu-id="3f945-139">Kuvaa, millä tiheydellä seulonta on suoritettava määritetylle henkilölle.</span><span class="sxs-lookup"><span data-stu-id="3f945-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="3f945-140">**Luo kohteesta**</span><span class="sxs-lookup"><span data-stu-id="3f945-140">**Generate From**</span></span><br><span data-ttu-id="3f945-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="3f945-141">mshr_generatefrom</span></span><br><span data-ttu-id="3f945-142">*mshr_hcmfrequencygeneratefrom-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="3f945-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="3f945-143">Luku-Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="3f945-143">Read-write</span></span><br><span data-ttu-id="3f945-144">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="3f945-144">Required</span></span> | <span data-ttu-id="3f945-145">Jos Tiheys-arvo on jokin muu kuin "Vain kerran", GenerateFrom-arvo määrittää päivämäärän, josta seuraava seulontatapahtuma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="3f945-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="3f945-146">**Tiheysväli**</span><span class="sxs-lookup"><span data-stu-id="3f945-146">**Frequency Interval**</span></span><br><span data-ttu-id="3f945-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="3f945-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="3f945-148">*Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="3f945-148">*Integer*</span></span> | <span data-ttu-id="3f945-149">Luku-Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="3f945-149">Read-write</span></span><br><span data-ttu-id="3f945-150">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="3f945-150">Required</span></span> | <span data-ttu-id="3f945-151">Jos Tiheys-arvo on jokin muu kuin "Vain kerran", sinun on määritettävä seulontatapahtumien välisten aikayksiköiden aikaväli.</span><span class="sxs-lookup"><span data-stu-id="3f945-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3f945-152">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3f945-152">See also</span></span>

[<span data-ttu-id="3f945-153">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="3f945-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3f945-154">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="3f945-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]