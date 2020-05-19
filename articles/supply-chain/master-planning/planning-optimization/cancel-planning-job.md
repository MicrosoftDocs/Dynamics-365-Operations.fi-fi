---
title: Suunnittelutyön peruuttaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön peruuttamista.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323459"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="9028d-103">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="9028d-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9028d-104">Microsoft Dynamics 365 Supply Chain Managementissa voi peruuttaa suunnittelun optimointitoimintoa käyttävän aktiivisen suunnittelutyön.</span><span class="sxs-lookup"><span data-stu-id="9028d-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="9028d-105">Kun valitset **Peruuta** valintaikkunassa, kun suunnittelun optimointityö käynnistetään suoraan käyttöliittymästä (eli sitä ei ajeta taustalla), tämä ei peruuta suunnittelun optimointityötä.</span><span class="sxs-lookup"><span data-stu-id="9028d-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="9028d-106">Vaikka saat varoituksen, kuten Toiminto peruutettu, sinun on silti peruutettava suunnittelutyö suunnittelun optimoinnin avulla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9028d-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="9028d-107">Aktiivinen suunnittelutyö peruutetaan seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="9028d-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="9028d-108">Vain aktiiviset työt voidaan peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="9028d-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="9028d-109">Valitse **Pääsuunnittelu \> Asetukset \> Suunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="9028d-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="9028d-110">Valitse suunnitteluajoon sopiva suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="9028d-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="9028d-111">Valitse **Historia**.</span><span class="sxs-lookup"><span data-stu-id="9028d-111">Select **History**.</span></span>
4. <span data-ttu-id="9028d-112">Valitse peruutettava suunnittelutyö</span><span class="sxs-lookup"><span data-stu-id="9028d-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="9028d-113">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="9028d-113">Select **Cancel**.</span></span>

<span data-ttu-id="9028d-114">Työn tila on **Peruutetaan**, kunnes suunnittelun optimointipalvelu vahvistaa, että työ on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="9028d-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="9028d-115">Tilaksi vaihdetaan sitten **Peruutettu**.</span><span class="sxs-lookup"><span data-stu-id="9028d-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="9028d-116">Tilan muutokset tulevat näkyviin, kun sivu päivitetään **Päivitä**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="9028d-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9028d-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9028d-117">Additional resources</span></span>

[<span data-ttu-id="9028d-118">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="9028d-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="9028d-119">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="9028d-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9028d-120">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="9028d-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="9028d-121">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="9028d-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="9028d-122">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="9028d-122">Apply filters to a plan</span></span>](plan-filters.md)
