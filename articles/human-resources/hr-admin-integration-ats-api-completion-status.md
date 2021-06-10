---
title: Valmistumisen tila
description: Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055361"
---
# <a name="completion-status"></a><span data-ttu-id="99c58-103">Valmistumisen tila</span><span class="sxs-lookup"><span data-stu-id="99c58-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="99c58-104">Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="99c58-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="99c58-105">Fyysinen nimi: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="99c58-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="99c58-106">Tämä valintalista määrittää hakijan seulontojen tilan arvojen asetusjoukon.</span><span class="sxs-lookup"><span data-stu-id="99c58-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="99c58-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="99c58-107">Value</span></span> | <span data-ttu-id="99c58-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="99c58-108">Label</span></span> | <span data-ttu-id="99c58-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="99c58-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="99c58-110">200000000</span><span class="sxs-lookup"><span data-stu-id="99c58-110">200000000</span></span> | <span data-ttu-id="99c58-111">Ei valmis</span><span class="sxs-lookup"><span data-stu-id="99c58-111">Not Complete</span></span> | <span data-ttu-id="99c58-112">Hakija ei ole vielä suorittanut seulontaa loppuun.</span><span class="sxs-lookup"><span data-stu-id="99c58-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="99c58-113">200000001</span><span class="sxs-lookup"><span data-stu-id="99c58-113">200000001</span></span> | <span data-ttu-id="99c58-114">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="99c58-114">Pass</span></span> | <span data-ttu-id="99c58-115">Hakija läpäisi seulonnan.</span><span class="sxs-lookup"><span data-stu-id="99c58-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="99c58-116">200000002</span><span class="sxs-lookup"><span data-stu-id="99c58-116">200000002</span></span> | <span data-ttu-id="99c58-117">Epäonnistuminen</span><span class="sxs-lookup"><span data-stu-id="99c58-117">Fail</span></span> | <span data-ttu-id="99c58-118">Hakija ei läpäissyt seulontaa.</span><span class="sxs-lookup"><span data-stu-id="99c58-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="99c58-119">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="99c58-119">See also</span></span>

[<span data-ttu-id="99c58-120">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="99c58-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="99c58-121">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="99c58-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]