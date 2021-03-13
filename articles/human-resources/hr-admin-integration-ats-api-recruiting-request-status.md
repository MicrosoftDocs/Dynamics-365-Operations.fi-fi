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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125951"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="56564-103">Työhönottopyynnön tila</span><span class="sxs-lookup"><span data-stu-id="56564-103">Recruiting request status</span></span>

<span data-ttu-id="56564-104">Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="56564-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="56564-105">Fyysinen nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="56564-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="56564-106">Tämä valintalista määrittää työhönottopyynnön tilan arvojen asetusjoukon.</span><span class="sxs-lookup"><span data-stu-id="56564-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="56564-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="56564-107">Value</span></span> | <span data-ttu-id="56564-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="56564-108">Label</span></span> | <span data-ttu-id="56564-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="56564-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="56564-110">200000000</span><span class="sxs-lookup"><span data-stu-id="56564-110">200000000</span></span> | <span data-ttu-id="56564-111">Luonnos</span><span class="sxs-lookup"><span data-stu-id="56564-111">Draft</span></span> | <span data-ttu-id="56564-112">Pyyntö on luonnos eikä se ole valmis aktiiviseen työhönottoon.</span><span class="sxs-lookup"><span data-stu-id="56564-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="56564-113">200000001</span><span class="sxs-lookup"><span data-stu-id="56564-113">200000001</span></span> | <span data-ttu-id="56564-114">Tarkistuksessa</span><span class="sxs-lookup"><span data-stu-id="56564-114">In Review</span></span> | <span data-ttu-id="56564-115">Pyyntö on lähetetty, ja se reititetään hyväksyttäväksi työnkulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="56564-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="56564-116">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="56564-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="56564-117">200000002</span><span class="sxs-lookup"><span data-stu-id="56564-117">200000002</span></span> | <span data-ttu-id="56564-118">Odottava</span><span class="sxs-lookup"><span data-stu-id="56564-118">Pending</span></span> | <span data-ttu-id="56564-119">Pyyntö odottaa työnkulkutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="56564-119">The request is pending workflow action.</span></span> <span data-ttu-id="56564-120">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="56564-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="56564-121">200000003</span><span class="sxs-lookup"><span data-stu-id="56564-121">200000003</span></span> | <span data-ttu-id="56564-122">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="56564-122">Canceled</span></span> | <span data-ttu-id="56564-123">Pyyntö on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="56564-123">The request has been canceled.</span></span> <span data-ttu-id="56564-124">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="56564-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="56564-125">200000004</span><span class="sxs-lookup"><span data-stu-id="56564-125">200000004</span></span> | <span data-ttu-id="56564-126">Kielletty</span><span class="sxs-lookup"><span data-stu-id="56564-126">Denied</span></span> | <span data-ttu-id="56564-127">Pyyntö on hylätty.</span><span class="sxs-lookup"><span data-stu-id="56564-127">The request has been denied.</span></span> <span data-ttu-id="56564-128">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="56564-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="56564-129">200000005</span><span class="sxs-lookup"><span data-stu-id="56564-129">200000005</span></span> | <span data-ttu-id="56564-130">Käytössä</span><span class="sxs-lookup"><span data-stu-id="56564-130">Active</span></span> | <span data-ttu-id="56564-131">Kaikki työnkulut on suoritettu ja hyväksytty, ja pyyntö on valmis aktiiviseen työhönottoon.</span><span class="sxs-lookup"><span data-stu-id="56564-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="56564-132">200000006</span><span class="sxs-lookup"><span data-stu-id="56564-132">200000006</span></span> | <span data-ttu-id="56564-133">Valmis</span><span class="sxs-lookup"><span data-stu-id="56564-133">Closed</span></span> | <span data-ttu-id="56564-134">Työhönottopyyntö on suljettu.</span><span class="sxs-lookup"><span data-stu-id="56564-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="56564-135">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="56564-135">See also</span></span>

[<span data-ttu-id="56564-136">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="56564-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="56564-137">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="56564-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
