---
title: MyLeaveRequests – yleiskatsaus
description: Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115533"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="5157e-103">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5157e-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="5157e-104">Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="5157e-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="5157e-105">Avain</span><span class="sxs-lookup"><span data-stu-id="5157e-105">Key</span></span>

  | <span data-ttu-id="5157e-106">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5157e-106">Property Name</span></span> | <span data-ttu-id="5157e-107">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="5157e-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="5157e-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5157e-108">dataAreaId</span></span>    | <span data-ttu-id="5157e-109">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-109">String</span></span>    |
  | <span data-ttu-id="5157e-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="5157e-110">RequestId</span></span>     | <span data-ttu-id="5157e-111">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-111">String</span></span>    |
  | <span data-ttu-id="5157e-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5157e-112">LeaveType</span></span>     | <span data-ttu-id="5157e-113">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-113">String</span></span>    |
  | <span data-ttu-id="5157e-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5157e-114">LeaveDate</span></span>     | <span data-ttu-id="5157e-115">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="5157e-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="5157e-116">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5157e-116">Properties</span></span>

  | <span data-ttu-id="5157e-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5157e-117">Property Name</span></span>     | <span data-ttu-id="5157e-118">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="5157e-118">Data Type</span></span> | <span data-ttu-id="5157e-119">Tarvitaan</span><span class="sxs-lookup"><span data-stu-id="5157e-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="5157e-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5157e-120">dataAreaId</span></span>        | <span data-ttu-id="5157e-121">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-121">String</span></span>    | <span data-ttu-id="5157e-122">X</span><span class="sxs-lookup"><span data-stu-id="5157e-122">X</span></span>        |
  | <span data-ttu-id="5157e-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="5157e-123">RequestId</span></span>         | <span data-ttu-id="5157e-124">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-124">String</span></span>    | <span data-ttu-id="5157e-125">X</span><span class="sxs-lookup"><span data-stu-id="5157e-125">X</span></span>        |
  | <span data-ttu-id="5157e-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5157e-126">LeaveType</span></span>         | <span data-ttu-id="5157e-127">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-127">String</span></span>    | <span data-ttu-id="5157e-128">X</span><span class="sxs-lookup"><span data-stu-id="5157e-128">X</span></span>        |
  | <span data-ttu-id="5157e-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5157e-129">LeaveDate</span></span>         | <span data-ttu-id="5157e-130">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="5157e-130">Date</span></span>      | <span data-ttu-id="5157e-131">X</span><span class="sxs-lookup"><span data-stu-id="5157e-131">X</span></span>        |
  | <span data-ttu-id="5157e-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="5157e-132">ReasonCodeId</span></span>      | <span data-ttu-id="5157e-133">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-133">String</span></span>    |          |
  | <span data-ttu-id="5157e-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="5157e-134">PersonnelNumber</span></span>   | <span data-ttu-id="5157e-135">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-135">String</span></span>    | <span data-ttu-id="5157e-136">X</span><span class="sxs-lookup"><span data-stu-id="5157e-136">X</span></span>        |
  | <span data-ttu-id="5157e-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="5157e-137">RequestDate</span></span>       | <span data-ttu-id="5157e-138">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="5157e-138">Date</span></span>      | <span data-ttu-id="5157e-139">X</span><span class="sxs-lookup"><span data-stu-id="5157e-139">X</span></span>        |
  | <span data-ttu-id="5157e-140">Kommentti</span><span class="sxs-lookup"><span data-stu-id="5157e-140">Comment</span></span>           | <span data-ttu-id="5157e-141">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="5157e-141">String</span></span>    |          |
  | <span data-ttu-id="5157e-142">Tila</span><span class="sxs-lookup"><span data-stu-id="5157e-142">Status</span></span>            | <span data-ttu-id="5157e-143">Valintalista</span><span class="sxs-lookup"><span data-stu-id="5157e-143">Enum</span></span>      | <span data-ttu-id="5157e-144">X</span><span class="sxs-lookup"><span data-stu-id="5157e-144">X</span></span>        |
  | <span data-ttu-id="5157e-145">Määrä</span><span class="sxs-lookup"><span data-stu-id="5157e-145">Amount</span></span>            | <span data-ttu-id="5157e-146">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="5157e-146">Real</span></span>      |          |
  | <span data-ttu-id="5157e-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="5157e-147">HalfDayDefinition</span></span> | <span data-ttu-id="5157e-148">Valintalista</span><span class="sxs-lookup"><span data-stu-id="5157e-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="5157e-149">Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="5157e-149">Actions</span></span>

 | <span data-ttu-id="5157e-150">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="5157e-150">Action Name</span></span>                               | <span data-ttu-id="5157e-151">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5157e-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="5157e-152">lähetä</span><span class="sxs-lookup"><span data-stu-id="5157e-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="5157e-153">Lähetä pyyntö, jota työnkulku käsittelee.</span><span class="sxs-lookup"><span data-stu-id="5157e-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5157e-154">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="5157e-154">See also</span></span>

- [<span data-ttu-id="5157e-155">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="5157e-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="5157e-156">Todennus</span><span class="sxs-lookup"><span data-stu-id="5157e-156">Authentication</span></span>](hr-developer-api-authentication.md)