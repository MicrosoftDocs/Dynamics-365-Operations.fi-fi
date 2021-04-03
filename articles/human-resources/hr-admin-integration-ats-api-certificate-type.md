---
title: Varmenteen tyyppi
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Todistuksen tyyppi -yksikköä.
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
ms.openlocfilehash: 962bccb3aaab16322d072417660ec3aac821183b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467478"
---
# <a name="certificate-type"></a><span data-ttu-id="eff1b-103">Varmenteen tyyppi</span><span class="sxs-lookup"><span data-stu-id="eff1b-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eff1b-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin Todistuksen tyyppi -yksikköä.</span><span class="sxs-lookup"><span data-stu-id="eff1b-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="eff1b-105">Fyysinen nimi: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="eff1b-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="eff1b-106">kuvaus</span><span class="sxs-lookup"><span data-stu-id="eff1b-106">Description</span></span>

<span data-ttu-id="eff1b-107">Tämä yksikkö määrittää Human Resourcesissa määritettyjen ammatillisten todistustyyppien luettelon.</span><span class="sxs-lookup"><span data-stu-id="eff1b-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="eff1b-108">Yksikkö ei ole yrityskohtainen.</span><span class="sxs-lookup"><span data-stu-id="eff1b-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="eff1b-109">JSON-esitys</span><span class="sxs-lookup"><span data-stu-id="eff1b-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="eff1b-110">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="eff1b-110">Properties</span></span>

| <span data-ttu-id="eff1b-111">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="eff1b-111">Property</span></span><br><span data-ttu-id="eff1b-112">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="eff1b-112">**Physical name**</span></span><br><span data-ttu-id="eff1b-113">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="eff1b-113">**_Type_**</span></span> | <span data-ttu-id="eff1b-114">Käytä</span><span class="sxs-lookup"><span data-stu-id="eff1b-114">Use</span></span> | <span data-ttu-id="eff1b-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="eff1b-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="eff1b-116">**Todistuksen tyypin yksikkötunnus**</span><span class="sxs-lookup"><span data-stu-id="eff1b-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="eff1b-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="eff1b-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="eff1b-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="eff1b-118">*GUID*</span></span> | <span data-ttu-id="eff1b-119">Vain luku</span><span class="sxs-lookup"><span data-stu-id="eff1b-119">Read-only</span></span><br><span data-ttu-id="eff1b-120">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="eff1b-120">Required</span></span> 
<span data-ttu-id="eff1b-121">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="eff1b-121">System-generated</span></span> | <span data-ttu-id="eff1b-122">Todistustyypin yksilöivä ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="eff1b-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="eff1b-123">**Todistuksen tyyppi**</span><span class="sxs-lookup"><span data-stu-id="eff1b-123">**Certificate Type**</span></span><br><span data-ttu-id="eff1b-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="eff1b-124">mshr_certificatetype</span></span><br><span data-ttu-id="eff1b-125">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="eff1b-125">*String*</span></span> | <span data-ttu-id="eff1b-126">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="eff1b-126">Read/write</span></span><br><span data-ttu-id="eff1b-127">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="eff1b-127">Required</span></span> | <span data-ttu-id="eff1b-128">Käyttäjän luettava todistustyypin yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="eff1b-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="eff1b-129">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="eff1b-129">**Description**</span></span><br><span data-ttu-id="eff1b-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="eff1b-130">mshr_description</span></span><br><span data-ttu-id="eff1b-131">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="eff1b-131">*String*</span></span> | <span data-ttu-id="eff1b-132">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="eff1b-132">Read/write</span></span><br><span data-ttu-id="eff1b-133">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="eff1b-133">Required</span></span> | <span data-ttu-id="eff1b-134">Todistustyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="eff1b-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="eff1b-135">**Pakollinen uudistaminen**</span><span class="sxs-lookup"><span data-stu-id="eff1b-135">**Require Renewal**</span></span><br><span data-ttu-id="eff1b-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="eff1b-136">mshr_requirerenewal</span></span><br><span data-ttu-id="eff1b-137">*mshr_noyes-asetusjoukko*</span><span class="sxs-lookup"><span data-stu-id="eff1b-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="eff1b-138">Luku/Kirjoitus</span><span class="sxs-lookup"><span data-stu-id="eff1b-138">Read/write</span></span><br><span data-ttu-id="eff1b-139">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="eff1b-139">Optional</span></span> | <span data-ttu-id="eff1b-140">Osoittaa, vaatiiko todistus uusimista.</span><span class="sxs-lookup"><span data-stu-id="eff1b-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="eff1b-141">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="eff1b-141">See also</span></span>

[<span data-ttu-id="eff1b-142">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="eff1b-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="eff1b-143">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="eff1b-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]