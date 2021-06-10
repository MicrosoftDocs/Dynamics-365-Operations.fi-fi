---
title: Etujen päättymispäivien hallinta
description: Tässä menettelyssä kerrotaan, miten etu vanhenee tai miten sitä laajennetaan, sekä miten etuun rekisteröityneiden työntekijöiden rekisteröitymispäivämääriä hallitaan.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefit, HcmMassBenefitExpiration, HcmMassBenefitExpirationResults, HcmWorker, HcmWorkerEnrollment, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 153982c926980236d13f09d2de0b9f1bb5038e42
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053030"
---
# <a name="manage-benefit-expiration-dates"></a><span data-ttu-id="85c9b-103">Etujen päättymispäivien hallinta</span><span class="sxs-lookup"><span data-stu-id="85c9b-103">Manage benefit expiration dates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="85c9b-104">Tässä menettelyssä kerrotaan, miten etu vanhenee tai miten sitä laajennetaan, sekä miten etuun rekisteröityneiden työntekijöiden rekisteröitymispäivämääriä hallitaan.</span><span class="sxs-lookup"><span data-stu-id="85c9b-104">This procedure shows how you can expire or extend a benefit, and manage the enrollment dates of workers that are enrolled in the benefit.</span></span> <span data-ttu-id="85c9b-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="85c9b-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="benefit-expiration-dates"></a><span data-ttu-id="85c9b-106">Etujen päättymispäivät</span><span class="sxs-lookup"><span data-stu-id="85c9b-106">Benefit expiration dates</span></span>

1. <span data-ttu-id="85c9b-107">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="85c9b-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="85c9b-108">Laajenna Rekisteröityneet työntekijät -tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="85c9b-108">Expand the Enrolled workers FactBox.</span></span>
3. <span data-ttu-id="85c9b-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="85c9b-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="85c9b-110">Valitse toimintoruudussa Etu.</span><span class="sxs-lookup"><span data-stu-id="85c9b-110">On the Action Pane, click Benefit.</span></span>
5. <span data-ttu-id="85c9b-111">Valitse Päätä tai laajenna etuja.</span><span class="sxs-lookup"><span data-stu-id="85c9b-111">Click Expire or extend benefits.</span></span>
6. <span data-ttu-id="85c9b-112">Syötä päivämäärä ja kellonaika Uusi edun päättymispäivä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="85c9b-112">In the New benefit expiration date field, enter a date and time.</span></span>
7. <span data-ttu-id="85c9b-113">Valitse Päätä.</span><span class="sxs-lookup"><span data-stu-id="85c9b-113">Click Expire.</span></span>
8. <span data-ttu-id="85c9b-114">Valitse toimintoruudussa Etu.</span><span class="sxs-lookup"><span data-stu-id="85c9b-114">On the Action Pane, click Benefit.</span></span>
9. <span data-ttu-id="85c9b-115">Valitse Edun päättämisen ja laajennuksen tulokset.</span><span class="sxs-lookup"><span data-stu-id="85c9b-115">Click Benefit expiration and extension results.</span></span>
10. <span data-ttu-id="85c9b-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85c9b-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="85c9b-117">Valitse luettelosta Työntekijät, joihin vaikutus kohdistui -linkki.</span><span class="sxs-lookup"><span data-stu-id="85c9b-117">In the list, click the Workers affected link.</span></span>
12. <span data-ttu-id="85c9b-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="85c9b-118">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="85c9b-119">Valitse Henkilöstönumero-kentän linkki.</span><span class="sxs-lookup"><span data-stu-id="85c9b-119">Click to follow the link in the Personnel number field.</span></span>
14. <span data-ttu-id="85c9b-120">Laajenna Henkilökohtaiset tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="85c9b-120">Expand the Personal information section.</span></span>
15. <span data-ttu-id="85c9b-121">Valitse Edut.</span><span class="sxs-lookup"><span data-stu-id="85c9b-121">Click Benefits.</span></span>
16. <span data-ttu-id="85c9b-122">Etsi luettelosta etu ja valitse tietue.</span><span class="sxs-lookup"><span data-stu-id="85c9b-122">In the list, find the benefit and select the record.</span></span> <span data-ttu-id="85c9b-123">Ota huomioon uusi kattavuuden päättymispäivä.</span><span class="sxs-lookup"><span data-stu-id="85c9b-123">Note the new coverage end date.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]