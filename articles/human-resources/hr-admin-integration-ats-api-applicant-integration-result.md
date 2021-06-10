---
title: Hakijatoimintojen integraation tulos
description: Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 8bef974abff18d7c07ecd679b7e01b31ea1459c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053896"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="f94e1-103">Hakijatoimintojen integraation tulos</span><span class="sxs-lookup"><span data-stu-id="f94e1-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f94e1-104">Tässä aiheessa kuvataan Hakemuksen yhdistämisen tulos -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="f94e1-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f94e1-105">Fyysinen nimi: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="f94e1-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="f94e1-106">Tämä valintalista antaa hakijan tietueen tilan.</span><span class="sxs-lookup"><span data-stu-id="f94e1-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="f94e1-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="f94e1-107">Value</span></span> | <span data-ttu-id="f94e1-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="f94e1-108">Label</span></span> | <span data-ttu-id="f94e1-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f94e1-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f94e1-110">200000000</span><span class="sxs-lookup"><span data-stu-id="f94e1-110">200000000</span></span> | <span data-ttu-id="f94e1-111">Ei käsitelty</span><span class="sxs-lookup"><span data-stu-id="f94e1-111">Not processed</span></span> | <span data-ttu-id="f94e1-112">Hakijaa harkitaan edelleen.</span><span class="sxs-lookup"><span data-stu-id="f94e1-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="f94e1-113">200000001</span><span class="sxs-lookup"><span data-stu-id="f94e1-113">200000001</span></span> | <span data-ttu-id="f94e1-114">Otettu työhön</span><span class="sxs-lookup"><span data-stu-id="f94e1-114">Hired</span></span> | <span data-ttu-id="f94e1-115">Hakija on palkattu.</span><span class="sxs-lookup"><span data-stu-id="f94e1-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="f94e1-116">200000002</span><span class="sxs-lookup"><span data-stu-id="f94e1-116">200000002</span></span> | <span data-ttu-id="f94e1-117">Ei ole palkattu</span><span class="sxs-lookup"><span data-stu-id="f94e1-117">Not hired</span></span> | <span data-ttu-id="f94e1-118">On tehty päätös siitä, ettei hakijaa palkata.</span><span class="sxs-lookup"><span data-stu-id="f94e1-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="f94e1-119">200000003</span><span class="sxs-lookup"><span data-stu-id="f94e1-119">200000003</span></span> | <span data-ttu-id="f94e1-120">Hylätty</span><span class="sxs-lookup"><span data-stu-id="f94e1-120">Dismissed</span></span> | <span data-ttu-id="f94e1-121">Hakija hylättiin harkinnasta.</span><span class="sxs-lookup"><span data-stu-id="f94e1-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f94e1-122">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f94e1-122">See also</span></span>

[<span data-ttu-id="f94e1-123">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="f94e1-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f94e1-124">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="f94e1-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]