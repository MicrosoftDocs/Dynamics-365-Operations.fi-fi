---
title: MyLeaveRequests – yleiskatsaus
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008879"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="45e64-102">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="45e64-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="45e64-103">Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="45e64-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="45e64-104">Avain</span><span class="sxs-lookup"><span data-stu-id="45e64-104">Key</span></span>

  | <span data-ttu-id="45e64-105">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="45e64-105">Property Name</span></span> | <span data-ttu-id="45e64-106">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="45e64-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="45e64-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="45e64-107">dataAreaId</span></span>    | <span data-ttu-id="45e64-108">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-108">String</span></span>    |
  | <span data-ttu-id="45e64-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="45e64-109">RequestId</span></span>     | <span data-ttu-id="45e64-110">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-110">String</span></span>    |
  | <span data-ttu-id="45e64-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="45e64-111">LeaveType</span></span>     | <span data-ttu-id="45e64-112">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-112">String</span></span>    |
  | <span data-ttu-id="45e64-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="45e64-113">LeaveDate</span></span>     | <span data-ttu-id="45e64-114">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="45e64-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="45e64-115">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="45e64-115">Properties</span></span>

  | <span data-ttu-id="45e64-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="45e64-116">Property Name</span></span>     | <span data-ttu-id="45e64-117">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="45e64-117">Data Type</span></span> | <span data-ttu-id="45e64-118">Tarvitaan</span><span class="sxs-lookup"><span data-stu-id="45e64-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="45e64-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="45e64-119">dataAreaId</span></span>        | <span data-ttu-id="45e64-120">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-120">String</span></span>    | <span data-ttu-id="45e64-121">X</span><span class="sxs-lookup"><span data-stu-id="45e64-121">X</span></span>        |
  | <span data-ttu-id="45e64-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="45e64-122">RequestId</span></span>         | <span data-ttu-id="45e64-123">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-123">String</span></span>    | <span data-ttu-id="45e64-124">X</span><span class="sxs-lookup"><span data-stu-id="45e64-124">X</span></span>        |
  | <span data-ttu-id="45e64-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="45e64-125">LeaveType</span></span>         | <span data-ttu-id="45e64-126">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-126">String</span></span>    | <span data-ttu-id="45e64-127">X</span><span class="sxs-lookup"><span data-stu-id="45e64-127">X</span></span>        |
  | <span data-ttu-id="45e64-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="45e64-128">LeaveDate</span></span>         | <span data-ttu-id="45e64-129">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="45e64-129">Date</span></span>      | <span data-ttu-id="45e64-130">X</span><span class="sxs-lookup"><span data-stu-id="45e64-130">X</span></span>        |
  | <span data-ttu-id="45e64-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="45e64-131">ReasonCodeId</span></span>      | <span data-ttu-id="45e64-132">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-132">String</span></span>    |          |
  | <span data-ttu-id="45e64-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="45e64-133">PersonnelNumber</span></span>   | <span data-ttu-id="45e64-134">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-134">String</span></span>    | <span data-ttu-id="45e64-135">X</span><span class="sxs-lookup"><span data-stu-id="45e64-135">X</span></span>        |
  | <span data-ttu-id="45e64-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="45e64-136">RequestDate</span></span>       | <span data-ttu-id="45e64-137">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="45e64-137">Date</span></span>      | <span data-ttu-id="45e64-138">X</span><span class="sxs-lookup"><span data-stu-id="45e64-138">X</span></span>        |
  | <span data-ttu-id="45e64-139">Kommentti</span><span class="sxs-lookup"><span data-stu-id="45e64-139">Comment</span></span>           | <span data-ttu-id="45e64-140">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="45e64-140">String</span></span>    |          |
  | <span data-ttu-id="45e64-141">Tila</span><span class="sxs-lookup"><span data-stu-id="45e64-141">Status</span></span>            | <span data-ttu-id="45e64-142">Valintalista</span><span class="sxs-lookup"><span data-stu-id="45e64-142">Enum</span></span>      | <span data-ttu-id="45e64-143">X</span><span class="sxs-lookup"><span data-stu-id="45e64-143">X</span></span>        |
  | <span data-ttu-id="45e64-144">Määrä</span><span class="sxs-lookup"><span data-stu-id="45e64-144">Amount</span></span>            | <span data-ttu-id="45e64-145">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="45e64-145">Real</span></span>      |          |
  | <span data-ttu-id="45e64-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="45e64-146">HalfDayDefinition</span></span> | <span data-ttu-id="45e64-147">Valintalista</span><span class="sxs-lookup"><span data-stu-id="45e64-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="45e64-148">Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="45e64-148">Actions</span></span>

 | <span data-ttu-id="45e64-149">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="45e64-149">Action Name</span></span>                               | <span data-ttu-id="45e64-150">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="45e64-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="45e64-151">lähetä</span><span class="sxs-lookup"><span data-stu-id="45e64-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="45e64-152">Lähetä pyyntö, jota työnkulku käsittelee.</span><span class="sxs-lookup"><span data-stu-id="45e64-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="45e64-153">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="45e64-153">See also</span></span>

- [<span data-ttu-id="45e64-154">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="45e64-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="45e64-155">Todennus</span><span class="sxs-lookup"><span data-stu-id="45e64-155">Authentication</span></span>](hr-developer-api-authentication.md)