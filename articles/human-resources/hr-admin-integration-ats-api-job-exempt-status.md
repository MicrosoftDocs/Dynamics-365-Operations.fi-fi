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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125566"
---
# <a name="job-exempt-status"></a><span data-ttu-id="f2f70-103">Työn vapautustila</span><span class="sxs-lookup"><span data-stu-id="f2f70-103">Job exempt status</span></span>

<span data-ttu-id="f2f70-104">Tässä aiheessa kuvataan Työn vapautustila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="f2f70-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f2f70-105">Fyysinen nimi: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="f2f70-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="f2f70-106">Tämä valintaluettelo määrittää asetusjoukon työn FLSA-vapautustilan arvoille.</span><span class="sxs-lookup"><span data-stu-id="f2f70-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="f2f70-107">Tämä tieto esitetään aiemmin luodussa cdm_jobexemptstatus-asetusjoukossa.</span><span class="sxs-lookup"><span data-stu-id="f2f70-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="f2f70-108">Arvo</span><span class="sxs-lookup"><span data-stu-id="f2f70-108">Value</span></span> | <span data-ttu-id="f2f70-109">Nimiö</span><span class="sxs-lookup"><span data-stu-id="f2f70-109">Label</span></span> | <span data-ttu-id="f2f70-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f2f70-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f2f70-111">200000000</span><span class="sxs-lookup"><span data-stu-id="f2f70-111">200000000</span></span> | <span data-ttu-id="f2f70-112">Veroton</span><span class="sxs-lookup"><span data-stu-id="f2f70-112">Exempt</span></span> | <span data-ttu-id="f2f70-113">Työllä on vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f2f70-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="f2f70-114">200000001</span><span class="sxs-lookup"><span data-stu-id="f2f70-114">200000001</span></span> | <span data-ttu-id="f2f70-115">Ei-vapautustila</span><span class="sxs-lookup"><span data-stu-id="f2f70-115">NonExempt</span></span> | <span data-ttu-id="f2f70-116">Työllä on ei-vapautustila FLSA-ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f2f70-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="f2f70-117">200000002</span><span class="sxs-lookup"><span data-stu-id="f2f70-117">200000002</span></span> | <span data-ttu-id="f2f70-118">Ei koske</span><span class="sxs-lookup"><span data-stu-id="f2f70-118">Does Not Apply</span></span> | <span data-ttu-id="f2f70-119">FLSA-tilan ohjeet eivät koske työtä.</span><span class="sxs-lookup"><span data-stu-id="f2f70-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f2f70-120">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f2f70-120">See also</span></span>

[<span data-ttu-id="f2f70-121">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="f2f70-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f2f70-122">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="f2f70-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
