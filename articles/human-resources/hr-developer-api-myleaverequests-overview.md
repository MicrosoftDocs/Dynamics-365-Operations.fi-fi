---
title: MyLeaveRequests – yleiskatsaus
description: Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054953"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="67ece-103">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="67ece-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="67ece-104">Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="67ece-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="67ece-105">Avain</span><span class="sxs-lookup"><span data-stu-id="67ece-105">Key</span></span>

  | <span data-ttu-id="67ece-106">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="67ece-106">Property Name</span></span> | <span data-ttu-id="67ece-107">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="67ece-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="67ece-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="67ece-108">dataAreaId</span></span>    | <span data-ttu-id="67ece-109">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-109">String</span></span>    |
  | <span data-ttu-id="67ece-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="67ece-110">RequestId</span></span>     | <span data-ttu-id="67ece-111">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-111">String</span></span>    |
  | <span data-ttu-id="67ece-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="67ece-112">LeaveType</span></span>     | <span data-ttu-id="67ece-113">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-113">String</span></span>    |
  | <span data-ttu-id="67ece-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="67ece-114">LeaveDate</span></span>     | <span data-ttu-id="67ece-115">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="67ece-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="67ece-116">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="67ece-116">Properties</span></span>

  | <span data-ttu-id="67ece-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="67ece-117">Property Name</span></span>     | <span data-ttu-id="67ece-118">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="67ece-118">Data Type</span></span> | <span data-ttu-id="67ece-119">Tarvitaan</span><span class="sxs-lookup"><span data-stu-id="67ece-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="67ece-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="67ece-120">dataAreaId</span></span>        | <span data-ttu-id="67ece-121">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-121">String</span></span>    | <span data-ttu-id="67ece-122">X</span><span class="sxs-lookup"><span data-stu-id="67ece-122">X</span></span>        |
  | <span data-ttu-id="67ece-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="67ece-123">RequestId</span></span>         | <span data-ttu-id="67ece-124">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-124">String</span></span>    | <span data-ttu-id="67ece-125">X</span><span class="sxs-lookup"><span data-stu-id="67ece-125">X</span></span>        |
  | <span data-ttu-id="67ece-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="67ece-126">LeaveType</span></span>         | <span data-ttu-id="67ece-127">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-127">String</span></span>    | <span data-ttu-id="67ece-128">X</span><span class="sxs-lookup"><span data-stu-id="67ece-128">X</span></span>        |
  | <span data-ttu-id="67ece-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="67ece-129">LeaveDate</span></span>         | <span data-ttu-id="67ece-130">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="67ece-130">Date</span></span>      | <span data-ttu-id="67ece-131">X</span><span class="sxs-lookup"><span data-stu-id="67ece-131">X</span></span>        |
  | <span data-ttu-id="67ece-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="67ece-132">ReasonCodeId</span></span>      | <span data-ttu-id="67ece-133">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-133">String</span></span>    |          |
  | <span data-ttu-id="67ece-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="67ece-134">PersonnelNumber</span></span>   | <span data-ttu-id="67ece-135">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-135">String</span></span>    | <span data-ttu-id="67ece-136">X</span><span class="sxs-lookup"><span data-stu-id="67ece-136">X</span></span>        |
  | <span data-ttu-id="67ece-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="67ece-137">RequestDate</span></span>       | <span data-ttu-id="67ece-138">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="67ece-138">Date</span></span>      | <span data-ttu-id="67ece-139">X</span><span class="sxs-lookup"><span data-stu-id="67ece-139">X</span></span>        |
  | <span data-ttu-id="67ece-140">Kommentti</span><span class="sxs-lookup"><span data-stu-id="67ece-140">Comment</span></span>           | <span data-ttu-id="67ece-141">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="67ece-141">String</span></span>    |          |
  | <span data-ttu-id="67ece-142">Tila</span><span class="sxs-lookup"><span data-stu-id="67ece-142">Status</span></span>            | <span data-ttu-id="67ece-143">Valintalista</span><span class="sxs-lookup"><span data-stu-id="67ece-143">Enum</span></span>      | <span data-ttu-id="67ece-144">X</span><span class="sxs-lookup"><span data-stu-id="67ece-144">X</span></span>        |
  | <span data-ttu-id="67ece-145">Määrä</span><span class="sxs-lookup"><span data-stu-id="67ece-145">Amount</span></span>            | <span data-ttu-id="67ece-146">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="67ece-146">Real</span></span>      |          |
  | <span data-ttu-id="67ece-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="67ece-147">HalfDayDefinition</span></span> | <span data-ttu-id="67ece-148">Valintalista</span><span class="sxs-lookup"><span data-stu-id="67ece-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="67ece-149">Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="67ece-149">Actions</span></span>

 | <span data-ttu-id="67ece-150">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="67ece-150">Action Name</span></span>                               | <span data-ttu-id="67ece-151">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="67ece-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="67ece-152">lähetä</span><span class="sxs-lookup"><span data-stu-id="67ece-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="67ece-153">Lähetä pyyntö, jota työnkulku käsittelee.</span><span class="sxs-lookup"><span data-stu-id="67ece-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="67ece-154">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="67ece-154">See also</span></span>

- [<span data-ttu-id="67ece-155">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="67ece-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="67ece-156">Todennus</span><span class="sxs-lookup"><span data-stu-id="67ece-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]