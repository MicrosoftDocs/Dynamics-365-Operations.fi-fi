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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803630"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="3f673-103">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="3f673-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f673-104">Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="3f673-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="3f673-105">Avain</span><span class="sxs-lookup"><span data-stu-id="3f673-105">Key</span></span>

  | <span data-ttu-id="3f673-106">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="3f673-106">Property Name</span></span> | <span data-ttu-id="3f673-107">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="3f673-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="3f673-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3f673-108">dataAreaId</span></span>    | <span data-ttu-id="3f673-109">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-109">String</span></span>    |
  | <span data-ttu-id="3f673-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="3f673-110">RequestId</span></span>     | <span data-ttu-id="3f673-111">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-111">String</span></span>    |
  | <span data-ttu-id="3f673-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3f673-112">LeaveType</span></span>     | <span data-ttu-id="3f673-113">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-113">String</span></span>    |
  | <span data-ttu-id="3f673-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3f673-114">LeaveDate</span></span>     | <span data-ttu-id="3f673-115">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="3f673-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="3f673-116">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="3f673-116">Properties</span></span>

  | <span data-ttu-id="3f673-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="3f673-117">Property Name</span></span>     | <span data-ttu-id="3f673-118">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="3f673-118">Data Type</span></span> | <span data-ttu-id="3f673-119">Tarvitaan</span><span class="sxs-lookup"><span data-stu-id="3f673-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="3f673-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3f673-120">dataAreaId</span></span>        | <span data-ttu-id="3f673-121">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-121">String</span></span>    | <span data-ttu-id="3f673-122">X</span><span class="sxs-lookup"><span data-stu-id="3f673-122">X</span></span>        |
  | <span data-ttu-id="3f673-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="3f673-123">RequestId</span></span>         | <span data-ttu-id="3f673-124">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-124">String</span></span>    | <span data-ttu-id="3f673-125">X</span><span class="sxs-lookup"><span data-stu-id="3f673-125">X</span></span>        |
  | <span data-ttu-id="3f673-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3f673-126">LeaveType</span></span>         | <span data-ttu-id="3f673-127">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-127">String</span></span>    | <span data-ttu-id="3f673-128">X</span><span class="sxs-lookup"><span data-stu-id="3f673-128">X</span></span>        |
  | <span data-ttu-id="3f673-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3f673-129">LeaveDate</span></span>         | <span data-ttu-id="3f673-130">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="3f673-130">Date</span></span>      | <span data-ttu-id="3f673-131">X</span><span class="sxs-lookup"><span data-stu-id="3f673-131">X</span></span>        |
  | <span data-ttu-id="3f673-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="3f673-132">ReasonCodeId</span></span>      | <span data-ttu-id="3f673-133">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-133">String</span></span>    |          |
  | <span data-ttu-id="3f673-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="3f673-134">PersonnelNumber</span></span>   | <span data-ttu-id="3f673-135">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-135">String</span></span>    | <span data-ttu-id="3f673-136">X</span><span class="sxs-lookup"><span data-stu-id="3f673-136">X</span></span>        |
  | <span data-ttu-id="3f673-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="3f673-137">RequestDate</span></span>       | <span data-ttu-id="3f673-138">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="3f673-138">Date</span></span>      | <span data-ttu-id="3f673-139">X</span><span class="sxs-lookup"><span data-stu-id="3f673-139">X</span></span>        |
  | <span data-ttu-id="3f673-140">Kommentti</span><span class="sxs-lookup"><span data-stu-id="3f673-140">Comment</span></span>           | <span data-ttu-id="3f673-141">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="3f673-141">String</span></span>    |          |
  | <span data-ttu-id="3f673-142">Tila</span><span class="sxs-lookup"><span data-stu-id="3f673-142">Status</span></span>            | <span data-ttu-id="3f673-143">Valintalista</span><span class="sxs-lookup"><span data-stu-id="3f673-143">Enum</span></span>      | <span data-ttu-id="3f673-144">X</span><span class="sxs-lookup"><span data-stu-id="3f673-144">X</span></span>        |
  | <span data-ttu-id="3f673-145">Määrä</span><span class="sxs-lookup"><span data-stu-id="3f673-145">Amount</span></span>            | <span data-ttu-id="3f673-146">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="3f673-146">Real</span></span>      |          |
  | <span data-ttu-id="3f673-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="3f673-147">HalfDayDefinition</span></span> | <span data-ttu-id="3f673-148">Valintalista</span><span class="sxs-lookup"><span data-stu-id="3f673-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="3f673-149">Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="3f673-149">Actions</span></span>

 | <span data-ttu-id="3f673-150">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="3f673-150">Action Name</span></span>                               | <span data-ttu-id="3f673-151">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3f673-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="3f673-152">lähetä</span><span class="sxs-lookup"><span data-stu-id="3f673-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="3f673-153">Lähetä pyyntö, jota työnkulku käsittelee.</span><span class="sxs-lookup"><span data-stu-id="3f673-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3f673-154">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3f673-154">See also</span></span>

- [<span data-ttu-id="3f673-155">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="3f673-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="3f673-156">Todennus</span><span class="sxs-lookup"><span data-stu-id="3f673-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]