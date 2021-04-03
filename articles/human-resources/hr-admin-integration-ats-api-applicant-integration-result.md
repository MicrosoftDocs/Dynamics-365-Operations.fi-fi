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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467550"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="d53e5-103">Hakijatoimintojen integraation tulos</span><span class="sxs-lookup"><span data-stu-id="d53e5-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d53e5-104">Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="d53e5-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d53e5-105">Fyysinen nimi: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="d53e5-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="d53e5-106">Tämä valintalista antaa hakijan tietueen tilan.</span><span class="sxs-lookup"><span data-stu-id="d53e5-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="d53e5-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="d53e5-107">Value</span></span> | <span data-ttu-id="d53e5-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="d53e5-108">Label</span></span> | <span data-ttu-id="d53e5-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d53e5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d53e5-110">200000000</span><span class="sxs-lookup"><span data-stu-id="d53e5-110">200000000</span></span> | <span data-ttu-id="d53e5-111">Ei käsitelty</span><span class="sxs-lookup"><span data-stu-id="d53e5-111">Not processed</span></span> | <span data-ttu-id="d53e5-112">Hakijaa harkitaan edelleen.</span><span class="sxs-lookup"><span data-stu-id="d53e5-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="d53e5-113">200000001</span><span class="sxs-lookup"><span data-stu-id="d53e5-113">200000001</span></span> | <span data-ttu-id="d53e5-114">Otettu työhön</span><span class="sxs-lookup"><span data-stu-id="d53e5-114">Hired</span></span> | <span data-ttu-id="d53e5-115">Hakija on palkattu.</span><span class="sxs-lookup"><span data-stu-id="d53e5-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="d53e5-116">200000002</span><span class="sxs-lookup"><span data-stu-id="d53e5-116">200000002</span></span> | <span data-ttu-id="d53e5-117">Ei ole palkattu</span><span class="sxs-lookup"><span data-stu-id="d53e5-117">Not hired</span></span> | <span data-ttu-id="d53e5-118">On tehty päätös siitä, ettei hakijaa palkata.</span><span class="sxs-lookup"><span data-stu-id="d53e5-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="d53e5-119">200000003</span><span class="sxs-lookup"><span data-stu-id="d53e5-119">200000003</span></span> | <span data-ttu-id="d53e5-120">Hylätty</span><span class="sxs-lookup"><span data-stu-id="d53e5-120">Dismissed</span></span> | <span data-ttu-id="d53e5-121">Hakija hylättiin harkinnasta.</span><span class="sxs-lookup"><span data-stu-id="d53e5-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d53e5-122">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="d53e5-122">See also</span></span>

[<span data-ttu-id="d53e5-123">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="d53e5-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d53e5-124">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="d53e5-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]