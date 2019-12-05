---
title: Suodattimien käyttäminen suunnitelmaan
description: Tässä ohjeaiheessa käsitellään suodattimien käyttöä suunnitelmassa suunnittelun optimointitoimintoa käytettäessä.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
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
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773951"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="68051-103">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="68051-103">Apply filters to a plan</span></span>

<span data-ttu-id="68051-104">Kun suunnittelun optimointitoimintoa käytetään, voit käyttää suunnitelmassa suodatinta.</span><span class="sxs-lookup"><span data-stu-id="68051-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="68051-105">Suunnitelman suodatinta käytetään aina pääsuunnitteluajon aikana.</span><span class="sxs-lookup"><span data-stu-id="68051-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="68051-106">Suunnitelman suodattimella voi rajoittaa suunnitelman kätevästi tiettyyn nimikeryhmään ja varmistaa, ettei muita nimikkeitä sisällytetä tuloksena olevaan pääsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="68051-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="68051-107">Jos suunnitelman suodatinta käytetään ja jos pääsuunnitteluajon aikana käytetään myös suorituksenaikaista suodatinta, suunnitteluajossa otetaan huomioon vain kahden suodattimen leikkauskohta.</span><span class="sxs-lookup"><span data-stu-id="68051-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="68051-108">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="68051-108">Example scenario</span></span>

<span data-ttu-id="68051-109">Määritettävä suunnitelman suodatin sisältää nimekkeet A, B ja C. Samalla suunnitelmalle suoritetaan sitten pääsuunnitteluajoja niin, että käytössä on erilaiset suorituksenaikaiset suorittimet:</span><span class="sxs-lookup"><span data-stu-id="68051-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="68051-110">**Suorituksenaikainen suodatin, joka sisältää nimikkeen D**: nimikkeitä ei suunnitella, koska suunnitelman suodattimen ja suorituksenaikaisen suodattimen välillä ei ole leikkauskohtaa.</span><span class="sxs-lookup"><span data-stu-id="68051-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="68051-111">**Suorituksenaikainen suodatin, joka sisältää nimikkeen A ja D**: vain nimike A sisältyy suunnitteluajoon, koska nimike D ei sisälly suunnitelman suodattimeen.</span><span class="sxs-lookup"><span data-stu-id="68051-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="68051-112">**Suorituksenaikainen suodatin, joka sisältää nimikkeen B**: vain nimike B sisältyy suunnitteluajoon ja nimikkeen A edellinen suunnittelutulos säilytetään.</span><span class="sxs-lookup"><span data-stu-id="68051-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="68051-113">**Suorituksenaikainen suodatin, joka sisältää kaikki nimikkeet (tyhjä suodatin)**: nimikkeet A, B ja C sisältyvät suunnitteluajoon ja nimikkeiden A ja B edelliset suunnittelutulokset korvataan.</span><span class="sxs-lookup"><span data-stu-id="68051-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="68051-114">Suunnitelman suodattimen määrittämistä kannattaa välttää, jos suunnitelma on valittu **Pääsuunnittelun parametrit** -sivulla **nykyiseksi dynaamiseksi pääsuunnitelmaksi**.</span><span class="sxs-lookup"><span data-stu-id="68051-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="68051-115">Muussa tapauksessa dynaaminen pääsuunnitelmattoiminto rajoittuu suodatettuihin nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="68051-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="68051-116">Jos esimerkiksi nettotarpeet päivitetään nimikkeelle, joka ei sisälly suunnitelman suodattimeen, tulosta ei muodostu.</span><span class="sxs-lookup"><span data-stu-id="68051-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="68051-117">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="68051-117">Related resources</span></span>

[<span data-ttu-id="68051-118">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="68051-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="68051-119">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="68051-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="68051-120">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="68051-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="68051-121">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="68051-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="68051-122">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="68051-122">Cancel a planning job</span></span>](cancel-planning-job.md)
