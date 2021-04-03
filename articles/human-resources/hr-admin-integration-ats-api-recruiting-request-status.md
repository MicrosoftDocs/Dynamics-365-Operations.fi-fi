---
title: Työhönottopyynnön tila
description: Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464643"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="e9127-103">Työhönottopyynnön tila</span><span class="sxs-lookup"><span data-stu-id="e9127-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9127-104">Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="e9127-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e9127-105">Fyysinen nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="e9127-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="e9127-106">Tämä valintalista määrittää työhönottopyynnön tilan arvojen asetusjoukon.</span><span class="sxs-lookup"><span data-stu-id="e9127-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="e9127-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="e9127-107">Value</span></span> | <span data-ttu-id="e9127-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="e9127-108">Label</span></span> | <span data-ttu-id="e9127-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e9127-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e9127-110">200000000</span><span class="sxs-lookup"><span data-stu-id="e9127-110">200000000</span></span> | <span data-ttu-id="e9127-111">Luonnos</span><span class="sxs-lookup"><span data-stu-id="e9127-111">Draft</span></span> | <span data-ttu-id="e9127-112">Pyyntö on luonnos eikä se ole valmis aktiiviseen työhönottoon.</span><span class="sxs-lookup"><span data-stu-id="e9127-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="e9127-113">200000001</span><span class="sxs-lookup"><span data-stu-id="e9127-113">200000001</span></span> | <span data-ttu-id="e9127-114">Tarkistuksessa</span><span class="sxs-lookup"><span data-stu-id="e9127-114">In Review</span></span> | <span data-ttu-id="e9127-115">Pyyntö on lähetetty, ja se reititetään hyväksyttäväksi työnkulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="e9127-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="e9127-116">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e9127-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e9127-117">200000002</span><span class="sxs-lookup"><span data-stu-id="e9127-117">200000002</span></span> | <span data-ttu-id="e9127-118">Odottava</span><span class="sxs-lookup"><span data-stu-id="e9127-118">Pending</span></span> | <span data-ttu-id="e9127-119">Pyyntö odottaa työnkulkutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="e9127-119">The request is pending workflow action.</span></span> <span data-ttu-id="e9127-120">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e9127-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e9127-121">200000003</span><span class="sxs-lookup"><span data-stu-id="e9127-121">200000003</span></span> | <span data-ttu-id="e9127-122">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="e9127-122">Canceled</span></span> | <span data-ttu-id="e9127-123">Pyyntö on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="e9127-123">The request has been canceled.</span></span> <span data-ttu-id="e9127-124">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e9127-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e9127-125">200000004</span><span class="sxs-lookup"><span data-stu-id="e9127-125">200000004</span></span> | <span data-ttu-id="e9127-126">Kielletty</span><span class="sxs-lookup"><span data-stu-id="e9127-126">Denied</span></span> | <span data-ttu-id="e9127-127">Pyyntö on hylätty.</span><span class="sxs-lookup"><span data-stu-id="e9127-127">The request has been denied.</span></span> <span data-ttu-id="e9127-128">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="e9127-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="e9127-129">200000005</span><span class="sxs-lookup"><span data-stu-id="e9127-129">200000005</span></span> | <span data-ttu-id="e9127-130">Käytössä</span><span class="sxs-lookup"><span data-stu-id="e9127-130">Active</span></span> | <span data-ttu-id="e9127-131">Kaikki työnkulut on suoritettu ja hyväksytty, ja pyyntö on valmis aktiiviseen työhönottoon.</span><span class="sxs-lookup"><span data-stu-id="e9127-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="e9127-132">200000006</span><span class="sxs-lookup"><span data-stu-id="e9127-132">200000006</span></span> | <span data-ttu-id="e9127-133">Valmis</span><span class="sxs-lookup"><span data-stu-id="e9127-133">Closed</span></span> | <span data-ttu-id="e9127-134">Työhönottopyyntö on suljettu.</span><span class="sxs-lookup"><span data-stu-id="e9127-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e9127-135">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e9127-135">See also</span></span>

[<span data-ttu-id="e9127-136">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="e9127-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e9127-137">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="e9127-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]