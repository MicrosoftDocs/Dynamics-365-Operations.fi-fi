---
title: Suunnitelman historia- ja suunnittelulokien tarkasteleminen
description: Tässä ohjeaiheessa käsitellään, miten suunnittelun optimointitoiminnon käynnistämien suunnittelutöiden historiatietoja tarkastellaan.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187244"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="150b3-103">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="150b3-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="150b3-104">Tässä ohjeaiheessa käsitellään, miten Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimointitoiminnon käynnistämien suunnittelutöiden historiatietoja tarkastellaan.</span><span class="sxs-lookup"><span data-stu-id="150b3-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="150b3-105">Voit tarkastella suunnitelman historiaa avaamalla suunnitelman valitsemalla ensin **Pääsuunnittelu** \> **Asetukset** \> **Suunnitelmat** \> **Pääsuunnitelmat** ja sitten **Historia**.</span><span class="sxs-lookup"><span data-stu-id="150b3-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="150b3-106">Historiatiedoissa on luettelo kaikista valitun suunnitelman töistä.</span><span class="sxs-lookup"><span data-stu-id="150b3-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="150b3-107">Luettelo sisältää valmiit ja aktiiviset työt.</span><span class="sxs-lookup"><span data-stu-id="150b3-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="150b3-108">Suunnittelun optimoinnin pääsuunnittelun ajojen töiden historia sisältää enintään 60 tietuetta pääsuunnitelmaa kohden.</span><span class="sxs-lookup"><span data-stu-id="150b3-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="150b3-109">Kun suoritat uuden pääsuunnittelun laskennan, tämän suunnitelman varhaisin historiatietue poistetaan.</span><span class="sxs-lookup"><span data-stu-id="150b3-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="150b3-110">Töiden alkamisajan ja tilan lisäksi voit tarkastella tietyn työn lokia.</span><span class="sxs-lookup"><span data-stu-id="150b3-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="150b3-111">Loki sisältää lisätietoja ja varoituksia.</span><span class="sxs-lookup"><span data-stu-id="150b3-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="150b3-112">Kaikilla töillä ei ole lokia.</span><span class="sxs-lookup"><span data-stu-id="150b3-112">Not all jobs have a log.</span></span> <span data-ttu-id="150b3-113">Voit tarkastella työn lokia valitsemalla **Loki**.</span><span class="sxs-lookup"><span data-stu-id="150b3-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="150b3-114">Lokimerkinnät tallennetaan vain 30 päivän ajan työn valmistumispäivämäärästä sen jälkeen, kun ne poistetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="150b3-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="150b3-115">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="150b3-115">Related resources</span></span>

- [<span data-ttu-id="150b3-116">Suunnittelun optimoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="150b3-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="150b3-117">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="150b3-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="150b3-118">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="150b3-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="150b3-119">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="150b3-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="150b3-120">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="150b3-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]