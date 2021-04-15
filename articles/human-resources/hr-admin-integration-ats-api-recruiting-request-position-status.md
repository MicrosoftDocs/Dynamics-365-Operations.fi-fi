---
title: Työhönottopyynnön toimen tila
description: Tässä aiheessa kuvataan työhönottopyynnön toimen asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789729"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="24fab-103">Työhönottopyynnön toimen tila</span><span class="sxs-lookup"><span data-stu-id="24fab-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="24fab-104">Tässä aiheessa kuvataan työhönottopyynnön toimen asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="24fab-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="24fab-105">Fyysinen nimi: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="24fab-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="24fab-106">Tämä valintalista määrittää työhönottopyynnön kunkin toimen tilan arvojen asetusjoukon RecruitingRequestPosition-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="24fab-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="24fab-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="24fab-107">Value</span></span> | <span data-ttu-id="24fab-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="24fab-108">Label</span></span> | <span data-ttu-id="24fab-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="24fab-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="24fab-110">200000000</span><span class="sxs-lookup"><span data-stu-id="24fab-110">200000000</span></span> | <span data-ttu-id="24fab-111">Julkaise</span><span class="sxs-lookup"><span data-stu-id="24fab-111">Open</span></span> | <span data-ttu-id="24fab-112">Työhönottopyynnön toimi on avoin työhönottoa varten.</span><span class="sxs-lookup"><span data-stu-id="24fab-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="24fab-113">Tämä ei ilmaise, että toimelle ei ole tällä hetkellä aktiivista toimen määritystä.</span><span class="sxs-lookup"><span data-stu-id="24fab-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="24fab-114">Toimelle voi olla työntekijä työhönoton aikana.</span><span class="sxs-lookup"><span data-stu-id="24fab-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="24fab-115">Se ilmaisee vain, että toimi on käytettävissä työhönottoa varten työhönottopyynnön kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="24fab-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="24fab-116">200000001</span><span class="sxs-lookup"><span data-stu-id="24fab-116">200000001</span></span> | <span data-ttu-id="24fab-117">Täytetty</span><span class="sxs-lookup"><span data-stu-id="24fab-117">Filled</span></span> | <span data-ttu-id="24fab-118">Työntekijä on valittu määritettäväksi toimeen.</span><span class="sxs-lookup"><span data-stu-id="24fab-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="24fab-119">200000002</span><span class="sxs-lookup"><span data-stu-id="24fab-119">200000002</span></span> | <span data-ttu-id="24fab-120">Peruutettu</span><span class="sxs-lookup"><span data-stu-id="24fab-120">Canceled</span></span> | <span data-ttu-id="24fab-121">Tämän toimen työhönottopyyntö on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="24fab-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="24fab-122">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="24fab-122">See also</span></span>

[<span data-ttu-id="24fab-123">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="24fab-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="24fab-124">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="24fab-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]