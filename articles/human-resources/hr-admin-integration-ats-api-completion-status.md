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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468200"
---
# <a name="completion-status"></a><span data-ttu-id="15c5f-103">Valmistumisen tila</span><span class="sxs-lookup"><span data-stu-id="15c5f-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="15c5f-104">Tässä aiheessa kuvataan Valmistumisen tila -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="15c5f-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="15c5f-105">Fyysinen nimi: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="15c5f-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="15c5f-106">Tämä valintalista määrittää hakijan seulontojen tilan arvojen asetusjoukon.</span><span class="sxs-lookup"><span data-stu-id="15c5f-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="15c5f-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="15c5f-107">Value</span></span> | <span data-ttu-id="15c5f-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="15c5f-108">Label</span></span> | <span data-ttu-id="15c5f-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="15c5f-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="15c5f-110">200000000</span><span class="sxs-lookup"><span data-stu-id="15c5f-110">200000000</span></span> | <span data-ttu-id="15c5f-111">Ei valmis</span><span class="sxs-lookup"><span data-stu-id="15c5f-111">Not Complete</span></span> | <span data-ttu-id="15c5f-112">Hakija ei ole vielä suorittanut seulontaa loppuun.</span><span class="sxs-lookup"><span data-stu-id="15c5f-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="15c5f-113">200000001</span><span class="sxs-lookup"><span data-stu-id="15c5f-113">200000001</span></span> | <span data-ttu-id="15c5f-114">Hyväksy</span><span class="sxs-lookup"><span data-stu-id="15c5f-114">Pass</span></span> | <span data-ttu-id="15c5f-115">Hakija läpäisi seulonnan.</span><span class="sxs-lookup"><span data-stu-id="15c5f-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="15c5f-116">200000002</span><span class="sxs-lookup"><span data-stu-id="15c5f-116">200000002</span></span> | <span data-ttu-id="15c5f-117">Epäonnistuminen</span><span class="sxs-lookup"><span data-stu-id="15c5f-117">Fail</span></span> | <span data-ttu-id="15c5f-118">Hakija ei läpäissyt seulontaa.</span><span class="sxs-lookup"><span data-stu-id="15c5f-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="15c5f-119">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="15c5f-119">See also</span></span>

[<span data-ttu-id="15c5f-120">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="15c5f-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="15c5f-121">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="15c5f-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]