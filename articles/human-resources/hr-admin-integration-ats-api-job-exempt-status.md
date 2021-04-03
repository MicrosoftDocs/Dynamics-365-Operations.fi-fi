---
title: Työn vapautustila
description: Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464449"
---
# <a name="job-exempt-status"></a><span data-ttu-id="faee2-103">Työn vapautustila</span><span class="sxs-lookup"><span data-stu-id="faee2-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="faee2-104">Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="faee2-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="faee2-105">Fyysinen nimi: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="faee2-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="faee2-106">Tämä valintaluettelo määrittää asetusjoukon työn FLSA-vapautustilan arvoille.</span><span class="sxs-lookup"><span data-stu-id="faee2-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="faee2-107">Tämä tieto esitetään aiemmin luodussa cdm_jobexemptstatus-asetusjoukossa.</span><span class="sxs-lookup"><span data-stu-id="faee2-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="faee2-108">Arvo</span><span class="sxs-lookup"><span data-stu-id="faee2-108">Value</span></span> | <span data-ttu-id="faee2-109">Nimiö</span><span class="sxs-lookup"><span data-stu-id="faee2-109">Label</span></span> | <span data-ttu-id="faee2-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="faee2-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="faee2-111">200000000</span><span class="sxs-lookup"><span data-stu-id="faee2-111">200000000</span></span> | <span data-ttu-id="faee2-112">Veroton</span><span class="sxs-lookup"><span data-stu-id="faee2-112">Exempt</span></span> | <span data-ttu-id="faee2-113">Työllä on vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="faee2-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="faee2-114">200000001</span><span class="sxs-lookup"><span data-stu-id="faee2-114">200000001</span></span> | <span data-ttu-id="faee2-115">Ei-vapautustila</span><span class="sxs-lookup"><span data-stu-id="faee2-115">NonExempt</span></span> | <span data-ttu-id="faee2-116">Työllä on ei-vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="faee2-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="faee2-117">200000002</span><span class="sxs-lookup"><span data-stu-id="faee2-117">200000002</span></span> | <span data-ttu-id="faee2-118">Ei koske</span><span class="sxs-lookup"><span data-stu-id="faee2-118">Does Not Apply</span></span> | <span data-ttu-id="faee2-119">FLSA-tilan ohjeet eivät koske työtä.</span><span class="sxs-lookup"><span data-stu-id="faee2-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="faee2-120">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="faee2-120">See also</span></span>

[<span data-ttu-id="faee2-121">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="faee2-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="faee2-122">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="faee2-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]