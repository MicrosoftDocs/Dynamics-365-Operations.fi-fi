---
title: Työn vapautustila
description: Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798294"
---
# <a name="job-exempt-status"></a><span data-ttu-id="af242-103">Työn vapautustila</span><span class="sxs-lookup"><span data-stu-id="af242-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="af242-104">Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="af242-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="af242-105">Fyysinen nimi: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="af242-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="af242-106">Tämä valintaluettelo määrittää asetusjoukon työn FLSA-vapautustilan arvoille.</span><span class="sxs-lookup"><span data-stu-id="af242-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="af242-107">Tämä tieto esitetään aiemmin luodussa cdm_jobexemptstatus-asetusjoukossa.</span><span class="sxs-lookup"><span data-stu-id="af242-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="af242-108">Arvo</span><span class="sxs-lookup"><span data-stu-id="af242-108">Value</span></span> | <span data-ttu-id="af242-109">Nimiö</span><span class="sxs-lookup"><span data-stu-id="af242-109">Label</span></span> | <span data-ttu-id="af242-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="af242-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="af242-111">200000000</span><span class="sxs-lookup"><span data-stu-id="af242-111">200000000</span></span> | <span data-ttu-id="af242-112">Veroton</span><span class="sxs-lookup"><span data-stu-id="af242-112">Exempt</span></span> | <span data-ttu-id="af242-113">Työllä on vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="af242-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="af242-114">200000001</span><span class="sxs-lookup"><span data-stu-id="af242-114">200000001</span></span> | <span data-ttu-id="af242-115">Ei-vapautustila</span><span class="sxs-lookup"><span data-stu-id="af242-115">NonExempt</span></span> | <span data-ttu-id="af242-116">Työllä on ei-vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="af242-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="af242-117">200000002</span><span class="sxs-lookup"><span data-stu-id="af242-117">200000002</span></span> | <span data-ttu-id="af242-118">Ei koske</span><span class="sxs-lookup"><span data-stu-id="af242-118">Does Not Apply</span></span> | <span data-ttu-id="af242-119">FLSA-tilan ohjeet eivät koske työtä.</span><span class="sxs-lookup"><span data-stu-id="af242-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="af242-120">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="af242-120">See also</span></span>

[<span data-ttu-id="af242-121">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="af242-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="af242-122">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="af242-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]