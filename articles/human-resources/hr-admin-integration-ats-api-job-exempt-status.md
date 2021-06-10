---
title: Työn vapautustila
description: Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053848"
---
# <a name="job-exempt-status"></a><span data-ttu-id="00d3d-103">Työn vapautustila</span><span class="sxs-lookup"><span data-stu-id="00d3d-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="00d3d-104">Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="00d3d-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="00d3d-105">Fyysinen nimi: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="00d3d-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="00d3d-106">Tämä valintaluettelo määrittää asetusjoukon työn FLSA-vapautustilan arvoille.</span><span class="sxs-lookup"><span data-stu-id="00d3d-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="00d3d-107">Tämä tieto esitetään aiemmin luodussa cdm_jobexemptstatus-asetusjoukossa.</span><span class="sxs-lookup"><span data-stu-id="00d3d-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="00d3d-108">Arvo</span><span class="sxs-lookup"><span data-stu-id="00d3d-108">Value</span></span> | <span data-ttu-id="00d3d-109">Nimiö</span><span class="sxs-lookup"><span data-stu-id="00d3d-109">Label</span></span> | <span data-ttu-id="00d3d-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00d3d-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="00d3d-111">200000000</span><span class="sxs-lookup"><span data-stu-id="00d3d-111">200000000</span></span> | <span data-ttu-id="00d3d-112">Veroton</span><span class="sxs-lookup"><span data-stu-id="00d3d-112">Exempt</span></span> | <span data-ttu-id="00d3d-113">Työllä on vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="00d3d-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="00d3d-114">200000001</span><span class="sxs-lookup"><span data-stu-id="00d3d-114">200000001</span></span> | <span data-ttu-id="00d3d-115">Ei-vapautustila</span><span class="sxs-lookup"><span data-stu-id="00d3d-115">NonExempt</span></span> | <span data-ttu-id="00d3d-116">Työllä on ei-vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="00d3d-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="00d3d-117">200000002</span><span class="sxs-lookup"><span data-stu-id="00d3d-117">200000002</span></span> | <span data-ttu-id="00d3d-118">Ei koske</span><span class="sxs-lookup"><span data-stu-id="00d3d-118">Does Not Apply</span></span> | <span data-ttu-id="00d3d-119">FLSA-tilan ohjeet eivät koske työtä.</span><span class="sxs-lookup"><span data-stu-id="00d3d-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="00d3d-120">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="00d3d-120">See also</span></span>

[<span data-ttu-id="00d3d-121">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="00d3d-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="00d3d-122">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="00d3d-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]