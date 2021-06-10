---
title: Seulonnan tiheys luo kohteesta
description: Tässä aiheessa kuvataan Seulonnan tiheys luo kohteesta -asetusjoukkoa Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054089"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="2ba9e-103">Seulonnan tiheys luo kohteesta</span><span class="sxs-lookup"><span data-stu-id="2ba9e-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2ba9e-104">Tässä aiheessa kuvataan Seulonnan tiheys luo kohteesta -asetusjoukkoa Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="2ba9e-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="2ba9e-105">Fyysinen nimi: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="2ba9e-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="2ba9e-106">Tämä valintalista määrittää asetusjoukon arvoille, jotka määrittävät seuraavan pakollisen seulonnan laskennan aloituspäivän.</span><span class="sxs-lookup"><span data-stu-id="2ba9e-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="2ba9e-107">Arvo</span><span class="sxs-lookup"><span data-stu-id="2ba9e-107">Value</span></span> | <span data-ttu-id="2ba9e-108">Nimiö</span><span class="sxs-lookup"><span data-stu-id="2ba9e-108">Label</span></span> | <span data-ttu-id="2ba9e-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2ba9e-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2ba9e-110">200000000 Ei valittu</span><span class="sxs-lookup"><span data-stu-id="2ba9e-110">200000000 Not selected</span></span> | <span data-ttu-id="2ba9e-111">Arvoa ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="2ba9e-111">No value has been selected.</span></span> |
| <span data-ttu-id="2ba9e-112">200000001 Valmistumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="2ba9e-112">200000001 Date completed</span></span> | <span data-ttu-id="2ba9e-113">Laskenta tehdään edellisestä seulonnan valmistusmispäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="2ba9e-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="2ba9e-114">200000002 Määräpäivä</span><span class="sxs-lookup"><span data-stu-id="2ba9e-114">200000002 Date required</span></span> | <span data-ttu-id="2ba9e-115">Laskenta tehdään edellisestä seulonnan määräpäivästä.</span><span class="sxs-lookup"><span data-stu-id="2ba9e-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="2ba9e-116">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2ba9e-116">See also</span></span>

[<span data-ttu-id="2ba9e-117">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="2ba9e-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="2ba9e-118">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="2ba9e-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]