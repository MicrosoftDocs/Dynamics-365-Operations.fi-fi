---
title: MyLeaveRequests – yleiskatsaus
description: Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092034"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="462e4-103">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="462e4-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="462e4-104">Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="462e4-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="462e4-105">Avain</span><span class="sxs-lookup"><span data-stu-id="462e4-105">Key</span></span>

  | <span data-ttu-id="462e4-106">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="462e4-106">Property Name</span></span> | <span data-ttu-id="462e4-107">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="462e4-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="462e4-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="462e4-108">dataAreaId</span></span>    | <span data-ttu-id="462e4-109">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-109">String</span></span>    |
  | <span data-ttu-id="462e4-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="462e4-110">RequestId</span></span>     | <span data-ttu-id="462e4-111">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-111">String</span></span>    |
  | <span data-ttu-id="462e4-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="462e4-112">LeaveType</span></span>     | <span data-ttu-id="462e4-113">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-113">String</span></span>    |
  | <span data-ttu-id="462e4-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="462e4-114">LeaveDate</span></span>     | <span data-ttu-id="462e4-115">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="462e4-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="462e4-116">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="462e4-116">Properties</span></span>

  | <span data-ttu-id="462e4-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="462e4-117">Property Name</span></span>     | <span data-ttu-id="462e4-118">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="462e4-118">Data Type</span></span> | <span data-ttu-id="462e4-119">Tarvitaan</span><span class="sxs-lookup"><span data-stu-id="462e4-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="462e4-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="462e4-120">dataAreaId</span></span>        | <span data-ttu-id="462e4-121">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-121">String</span></span>    | <span data-ttu-id="462e4-122">X</span><span class="sxs-lookup"><span data-stu-id="462e4-122">X</span></span>        |
  | <span data-ttu-id="462e4-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="462e4-123">RequestId</span></span>         | <span data-ttu-id="462e4-124">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-124">String</span></span>    | <span data-ttu-id="462e4-125">X</span><span class="sxs-lookup"><span data-stu-id="462e4-125">X</span></span>        |
  | <span data-ttu-id="462e4-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="462e4-126">LeaveType</span></span>         | <span data-ttu-id="462e4-127">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-127">String</span></span>    | <span data-ttu-id="462e4-128">X</span><span class="sxs-lookup"><span data-stu-id="462e4-128">X</span></span>        |
  | <span data-ttu-id="462e4-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="462e4-129">LeaveDate</span></span>         | <span data-ttu-id="462e4-130">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="462e4-130">Date</span></span>      | <span data-ttu-id="462e4-131">X</span><span class="sxs-lookup"><span data-stu-id="462e4-131">X</span></span>        |
  | <span data-ttu-id="462e4-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="462e4-132">ReasonCodeId</span></span>      | <span data-ttu-id="462e4-133">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-133">String</span></span>    |          |
  | <span data-ttu-id="462e4-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="462e4-134">PersonnelNumber</span></span>   | <span data-ttu-id="462e4-135">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-135">String</span></span>    | <span data-ttu-id="462e4-136">X</span><span class="sxs-lookup"><span data-stu-id="462e4-136">X</span></span>        |
  | <span data-ttu-id="462e4-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="462e4-137">RequestDate</span></span>       | <span data-ttu-id="462e4-138">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="462e4-138">Date</span></span>      | <span data-ttu-id="462e4-139">X</span><span class="sxs-lookup"><span data-stu-id="462e4-139">X</span></span>        |
  | <span data-ttu-id="462e4-140">Kommentti</span><span class="sxs-lookup"><span data-stu-id="462e4-140">Comment</span></span>           | <span data-ttu-id="462e4-141">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="462e4-141">String</span></span>    |          |
  | <span data-ttu-id="462e4-142">Tila</span><span class="sxs-lookup"><span data-stu-id="462e4-142">Status</span></span>            | <span data-ttu-id="462e4-143">Valintalista</span><span class="sxs-lookup"><span data-stu-id="462e4-143">Enum</span></span>      | <span data-ttu-id="462e4-144">X</span><span class="sxs-lookup"><span data-stu-id="462e4-144">X</span></span>        |
  | <span data-ttu-id="462e4-145">Määrä</span><span class="sxs-lookup"><span data-stu-id="462e4-145">Amount</span></span>            | <span data-ttu-id="462e4-146">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="462e4-146">Real</span></span>      |          |
  | <span data-ttu-id="462e4-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="462e4-147">HalfDayDefinition</span></span> | <span data-ttu-id="462e4-148">Valintalista</span><span class="sxs-lookup"><span data-stu-id="462e4-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="462e4-149">Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="462e4-149">Actions</span></span>

 | <span data-ttu-id="462e4-150">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="462e4-150">Action Name</span></span>                               | <span data-ttu-id="462e4-151">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="462e4-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="462e4-152">lähetä</span><span class="sxs-lookup"><span data-stu-id="462e4-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="462e4-153">Lähetä pyyntö, jota työnkulku käsittelee.</span><span class="sxs-lookup"><span data-stu-id="462e4-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="462e4-154">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="462e4-154">See also</span></span>

- [<span data-ttu-id="462e4-155">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="462e4-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="462e4-156">Todennus</span><span class="sxs-lookup"><span data-stu-id="462e4-156">Authentication</span></span>](hr-developer-api-authentication.md)