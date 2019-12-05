---
title: Suunnittelutyön peruuttaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön peruuttamista.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773952"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="c8c62-103">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="c8c62-103">Cancel a planning job</span></span>

<span data-ttu-id="c8c62-104">Microsoft Dynamics 365 Supply Chain Managementissa voi peruuttaa suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön.</span><span class="sxs-lookup"><span data-stu-id="c8c62-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="c8c62-105">Aktiivinen suunnittelutyö peruutetaan seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="c8c62-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c62-106">Vain aktiiviset työt voidaan peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="c8c62-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="c8c62-107">Valitse **Pääsuunnittelu \> Asetukset \> Suunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="c8c62-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="c8c62-108">Valitse suunnitteluajoon sopiva suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="c8c62-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="c8c62-109">Valitse **Historia**.</span><span class="sxs-lookup"><span data-stu-id="c8c62-109">Select **History**.</span></span>
4. <span data-ttu-id="c8c62-110">Valitse peruutettava suunnittelutyö</span><span class="sxs-lookup"><span data-stu-id="c8c62-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="c8c62-111">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="c8c62-111">Select **Cancel**.</span></span>

<span data-ttu-id="c8c62-112">Työn tila on **Peruutetaan**, kunnes suunnittelun optimointipalvelu vahvistaa, että työ on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="c8c62-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="c8c62-113">Tilaksi vaihdetaan sitten **Peruutettu**.</span><span class="sxs-lookup"><span data-stu-id="c8c62-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c62-114">Tilan muutokset tulevat näkyviin, kun sivu päivitetään **Päivitä**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="c8c62-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c8c62-115">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="c8c62-115">Related resources</span></span>

[<span data-ttu-id="c8c62-116">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="c8c62-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c8c62-117">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="c8c62-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c8c62-118">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="c8c62-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c8c62-119">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="c8c62-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c8c62-120">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="c8c62-120">Apply filters to a plan</span></span>](plan-filters.md)
