---
title: Valmistumisen tila
description: Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: e9024e00b5d25117fd255084609c4f8db9284f32
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125686"
---
# <a name="completion-status"></a><span data-ttu-id="655ab-103">Valmistumisen tila</span><span class="sxs-lookup"><span data-stu-id="655ab-103">Completion status</span></span>

<span data-ttu-id="655ab-104">Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="655ab-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="655ab-105">Fyysinen nimi: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="655ab-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="655ab-106">Tämä valintalista määrittää hakijan seulontojen tilan arvojen asetusjoukon.</span><span class="sxs-lookup"><span data-stu-id="655ab-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="655ab-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="655ab-107">Value</span></span> | <span data-ttu-id="655ab-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="655ab-108">Label</span></span> | <span data-ttu-id="655ab-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="655ab-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="655ab-110">200000000</span><span class="sxs-lookup"><span data-stu-id="655ab-110">200000000</span></span> | <span data-ttu-id="655ab-111">Ei valmis</span><span class="sxs-lookup"><span data-stu-id="655ab-111">Not Complete</span></span> | <span data-ttu-id="655ab-112">Hakija ei ole vielä suorittanut seulontaa loppuun.</span><span class="sxs-lookup"><span data-stu-id="655ab-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="655ab-113">200000001</span><span class="sxs-lookup"><span data-stu-id="655ab-113">200000001</span></span> | <span data-ttu-id="655ab-114">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="655ab-114">Pass</span></span> | <span data-ttu-id="655ab-115">Hakija läpäisi seulonnan.</span><span class="sxs-lookup"><span data-stu-id="655ab-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="655ab-116">200000002</span><span class="sxs-lookup"><span data-stu-id="655ab-116">200000002</span></span> | <span data-ttu-id="655ab-117">Epäonnistuminen</span><span class="sxs-lookup"><span data-stu-id="655ab-117">Fail</span></span> | <span data-ttu-id="655ab-118">Hakija ei läpäissyt seulontaa.</span><span class="sxs-lookup"><span data-stu-id="655ab-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="655ab-119">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="655ab-119">See also</span></span>

[<span data-ttu-id="655ab-120">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="655ab-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="655ab-121">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="655ab-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
