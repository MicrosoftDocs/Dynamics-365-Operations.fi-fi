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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465507"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="1fec9-103">MyLeaveRequests – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1fec9-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1fec9-104">Microsoft Dynamics 365 Human Resourcesin MyLeaveRequests-yksikkö sisältää luettelon lomapyynnöistä, jotka on rajattu (rajoitettu)-järjestelmään, jonka avulla käyttäjä voi tehdä kyselyitä entiteetistä.</span><span class="sxs-lookup"><span data-stu-id="1fec9-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="1fec9-105">Avain</span><span class="sxs-lookup"><span data-stu-id="1fec9-105">Key</span></span>

  | <span data-ttu-id="1fec9-106">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="1fec9-106">Property Name</span></span> | <span data-ttu-id="1fec9-107">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="1fec9-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="1fec9-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="1fec9-108">dataAreaId</span></span>    | <span data-ttu-id="1fec9-109">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-109">String</span></span>    |
  | <span data-ttu-id="1fec9-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="1fec9-110">RequestId</span></span>     | <span data-ttu-id="1fec9-111">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-111">String</span></span>    |
  | <span data-ttu-id="1fec9-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="1fec9-112">LeaveType</span></span>     | <span data-ttu-id="1fec9-113">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-113">String</span></span>    |
  | <span data-ttu-id="1fec9-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="1fec9-114">LeaveDate</span></span>     | <span data-ttu-id="1fec9-115">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fec9-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="1fec9-116">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1fec9-116">Properties</span></span>

  | <span data-ttu-id="1fec9-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="1fec9-117">Property Name</span></span>     | <span data-ttu-id="1fec9-118">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="1fec9-118">Data Type</span></span> | <span data-ttu-id="1fec9-119">Tarvitaan</span><span class="sxs-lookup"><span data-stu-id="1fec9-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="1fec9-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="1fec9-120">dataAreaId</span></span>        | <span data-ttu-id="1fec9-121">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-121">String</span></span>    | <span data-ttu-id="1fec9-122">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-122">X</span></span>        |
  | <span data-ttu-id="1fec9-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="1fec9-123">RequestId</span></span>         | <span data-ttu-id="1fec9-124">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-124">String</span></span>    | <span data-ttu-id="1fec9-125">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-125">X</span></span>        |
  | <span data-ttu-id="1fec9-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="1fec9-126">LeaveType</span></span>         | <span data-ttu-id="1fec9-127">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-127">String</span></span>    | <span data-ttu-id="1fec9-128">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-128">X</span></span>        |
  | <span data-ttu-id="1fec9-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="1fec9-129">LeaveDate</span></span>         | <span data-ttu-id="1fec9-130">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fec9-130">Date</span></span>      | <span data-ttu-id="1fec9-131">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-131">X</span></span>        |
  | <span data-ttu-id="1fec9-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="1fec9-132">ReasonCodeId</span></span>      | <span data-ttu-id="1fec9-133">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-133">String</span></span>    |          |
  | <span data-ttu-id="1fec9-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="1fec9-134">PersonnelNumber</span></span>   | <span data-ttu-id="1fec9-135">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-135">String</span></span>    | <span data-ttu-id="1fec9-136">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-136">X</span></span>        |
  | <span data-ttu-id="1fec9-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="1fec9-137">RequestDate</span></span>       | <span data-ttu-id="1fec9-138">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="1fec9-138">Date</span></span>      | <span data-ttu-id="1fec9-139">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-139">X</span></span>        |
  | <span data-ttu-id="1fec9-140">Kommentti</span><span class="sxs-lookup"><span data-stu-id="1fec9-140">Comment</span></span>           | <span data-ttu-id="1fec9-141">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="1fec9-141">String</span></span>    |          |
  | <span data-ttu-id="1fec9-142">Tila</span><span class="sxs-lookup"><span data-stu-id="1fec9-142">Status</span></span>            | <span data-ttu-id="1fec9-143">Valintalista</span><span class="sxs-lookup"><span data-stu-id="1fec9-143">Enum</span></span>      | <span data-ttu-id="1fec9-144">X</span><span class="sxs-lookup"><span data-stu-id="1fec9-144">X</span></span>        |
  | <span data-ttu-id="1fec9-145">Määrä</span><span class="sxs-lookup"><span data-stu-id="1fec9-145">Amount</span></span>            | <span data-ttu-id="1fec9-146">Reaaliluku</span><span class="sxs-lookup"><span data-stu-id="1fec9-146">Real</span></span>      |          |
  | <span data-ttu-id="1fec9-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="1fec9-147">HalfDayDefinition</span></span> | <span data-ttu-id="1fec9-148">Valintalista</span><span class="sxs-lookup"><span data-stu-id="1fec9-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="1fec9-149">Toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="1fec9-149">Actions</span></span>

 | <span data-ttu-id="1fec9-150">Toiminnon nimi</span><span class="sxs-lookup"><span data-stu-id="1fec9-150">Action Name</span></span>                               | <span data-ttu-id="1fec9-151">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1fec9-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="1fec9-152">lähetä</span><span class="sxs-lookup"><span data-stu-id="1fec9-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="1fec9-153">Lähetä pyyntö, jota työnkulku käsittelee.</span><span class="sxs-lookup"><span data-stu-id="1fec9-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1fec9-154">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1fec9-154">See also</span></span>

- [<span data-ttu-id="1fec9-155">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="1fec9-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="1fec9-156">Todennus</span><span class="sxs-lookup"><span data-stu-id="1fec9-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]