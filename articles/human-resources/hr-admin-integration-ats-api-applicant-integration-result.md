---
title: Hakijatoimintojen integraation tulos
description: Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 157864cd0eee879013724615ce31306c99c5aa68
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125806"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="b0c16-103">Hakijatoimintojen integraation tulos</span><span class="sxs-lookup"><span data-stu-id="b0c16-103">Applicant integration result</span></span>

<span data-ttu-id="b0c16-104">Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="b0c16-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b0c16-105">Fyysinen nimi: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="b0c16-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="b0c16-106">Tämä valintalista antaa hakijan tietueen tilan.</span><span class="sxs-lookup"><span data-stu-id="b0c16-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="b0c16-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="b0c16-107">Value</span></span> | <span data-ttu-id="b0c16-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="b0c16-108">Label</span></span> | <span data-ttu-id="b0c16-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="b0c16-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b0c16-110">200000000</span><span class="sxs-lookup"><span data-stu-id="b0c16-110">200000000</span></span> | <span data-ttu-id="b0c16-111">Ei käsitelty</span><span class="sxs-lookup"><span data-stu-id="b0c16-111">Not processed</span></span> | <span data-ttu-id="b0c16-112">Hakijaa harkitaan edelleen.</span><span class="sxs-lookup"><span data-stu-id="b0c16-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="b0c16-113">200000001</span><span class="sxs-lookup"><span data-stu-id="b0c16-113">200000001</span></span> | <span data-ttu-id="b0c16-114">Otettu työhön</span><span class="sxs-lookup"><span data-stu-id="b0c16-114">Hired</span></span> | <span data-ttu-id="b0c16-115">Hakija on palkattu.</span><span class="sxs-lookup"><span data-stu-id="b0c16-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="b0c16-116">200000002</span><span class="sxs-lookup"><span data-stu-id="b0c16-116">200000002</span></span> | <span data-ttu-id="b0c16-117">Ei ole palkattu</span><span class="sxs-lookup"><span data-stu-id="b0c16-117">Not hired</span></span> | <span data-ttu-id="b0c16-118">On tehty päätös siitä, ettei hakijaa palkata.</span><span class="sxs-lookup"><span data-stu-id="b0c16-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="b0c16-119">200000003</span><span class="sxs-lookup"><span data-stu-id="b0c16-119">200000003</span></span> | <span data-ttu-id="b0c16-120">Hylätty</span><span class="sxs-lookup"><span data-stu-id="b0c16-120">Dismissed</span></span> | <span data-ttu-id="b0c16-121">Hakija hylättiin harkinnasta.</span><span class="sxs-lookup"><span data-stu-id="b0c16-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b0c16-122">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="b0c16-122">See also</span></span>

[<span data-ttu-id="b0c16-123">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="b0c16-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b0c16-124">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="b0c16-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
