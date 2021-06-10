---
title: Työhönottopyynnön tila
description: Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059181"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="a8dda-103">Työhönottopyynnön tila</span><span class="sxs-lookup"><span data-stu-id="a8dda-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a8dda-104">Tässä aiheessa kuvataan työhönottopyynnön tilan asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="a8dda-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a8dda-105">Fyysinen nimi: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="a8dda-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="a8dda-106">Tämä valintalista määrittää työhönottopyynnön tilan arvojen asetusjoukon.</span><span class="sxs-lookup"><span data-stu-id="a8dda-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="a8dda-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="a8dda-107">Value</span></span> | <span data-ttu-id="a8dda-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="a8dda-108">Label</span></span> | <span data-ttu-id="a8dda-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="a8dda-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a8dda-110">200000000</span><span class="sxs-lookup"><span data-stu-id="a8dda-110">200000000</span></span> | <span data-ttu-id="a8dda-111">Luonnos</span><span class="sxs-lookup"><span data-stu-id="a8dda-111">Draft</span></span> | <span data-ttu-id="a8dda-112">Pyyntö on luonnos eikä se ole valmis aktiiviseen työhönottoon.</span><span class="sxs-lookup"><span data-stu-id="a8dda-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="a8dda-113">200000001</span><span class="sxs-lookup"><span data-stu-id="a8dda-113">200000001</span></span> | <span data-ttu-id="a8dda-114">Tarkistuksessa</span><span class="sxs-lookup"><span data-stu-id="a8dda-114">In Review</span></span> | <span data-ttu-id="a8dda-115">Pyyntö on lähetetty, ja se reititetään hyväksyttäväksi työnkulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="a8dda-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="a8dda-116">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="a8dda-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a8dda-117">200000002</span><span class="sxs-lookup"><span data-stu-id="a8dda-117">200000002</span></span> | <span data-ttu-id="a8dda-118">Odottava</span><span class="sxs-lookup"><span data-stu-id="a8dda-118">Pending</span></span> | <span data-ttu-id="a8dda-119">Pyyntö odottaa työnkulkutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="a8dda-119">The request is pending workflow action.</span></span> <span data-ttu-id="a8dda-120">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="a8dda-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a8dda-121">200000003</span><span class="sxs-lookup"><span data-stu-id="a8dda-121">200000003</span></span> | <span data-ttu-id="a8dda-122">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="a8dda-122">Canceled</span></span> | <span data-ttu-id="a8dda-123">Pyyntö on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="a8dda-123">The request has been canceled.</span></span> <span data-ttu-id="a8dda-124">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="a8dda-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a8dda-125">200000004</span><span class="sxs-lookup"><span data-stu-id="a8dda-125">200000004</span></span> | <span data-ttu-id="a8dda-126">Kielletty</span><span class="sxs-lookup"><span data-stu-id="a8dda-126">Denied</span></span> | <span data-ttu-id="a8dda-127">Pyyntö on hylätty.</span><span class="sxs-lookup"><span data-stu-id="a8dda-127">The request has been denied.</span></span> <span data-ttu-id="a8dda-128">Käytettävissä vain, kun työnkulku on käytössä.</span><span class="sxs-lookup"><span data-stu-id="a8dda-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="a8dda-129">200000005</span><span class="sxs-lookup"><span data-stu-id="a8dda-129">200000005</span></span> | <span data-ttu-id="a8dda-130">Käytössä</span><span class="sxs-lookup"><span data-stu-id="a8dda-130">Active</span></span> | <span data-ttu-id="a8dda-131">Kaikki työnkulut on suoritettu ja hyväksytty, ja pyyntö on valmis aktiiviseen työhönottoon.</span><span class="sxs-lookup"><span data-stu-id="a8dda-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="a8dda-132">200000006</span><span class="sxs-lookup"><span data-stu-id="a8dda-132">200000006</span></span> | <span data-ttu-id="a8dda-133">Valmis</span><span class="sxs-lookup"><span data-stu-id="a8dda-133">Closed</span></span> | <span data-ttu-id="a8dda-134">Työhönottopyyntö on suljettu.</span><span class="sxs-lookup"><span data-stu-id="a8dda-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a8dda-135">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a8dda-135">See also</span></span>

[<span data-ttu-id="a8dda-136">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="a8dda-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a8dda-137">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="a8dda-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]