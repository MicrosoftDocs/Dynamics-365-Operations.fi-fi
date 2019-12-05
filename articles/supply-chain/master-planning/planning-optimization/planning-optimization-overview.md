---
title: Suunnittelun optimoinnin yleiskuvaus
description: Tässä ohjeaiheessa on suunnittelun optimoinnin toimintojen yleiskatsaus.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: aae9ea56fc2174df56274776993c68b11c0521d0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773948"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="planning-optimization-overview"></a><span data-ttu-id="7a6f5-103">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7a6f5-103">Planning Optimization overview</span></span>

<span data-ttu-id="7a6f5-104">Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosan avulla pääsuunnittelulaskelma voidaan tehdä Dynamics 365 Supply Chain Managementin ja liittyvän SQL-tietokannan ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="7a6f5-105">Suunnittelun optimointitoimintoon liittyviä etuja ovat esimerkiksi suorituskyvyn parantuminen ja pääsuunnitteluajon vähäinen vaikutus SQL-tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="7a6f5-106">Nopeita suunnitteluajoja voidaan tehdä myös työaikana, joten suunnittelijat voivat reagoida heti kysynnän tai parametrin muutoksiin.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="7a6f5-107">Suunnittelun optimoinnin käyttöä varten on asennettava suunnittelun optimoinnin lisäosa Microsoft Dynamics Lifecycle Servicesin (LCS) projektista ja otettava suunnittelun optimointitoiminto käyttöön Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="7a6f5-108">Lisätietoja on kohdassa [Suunnittelun optimoinnin käytön aloittaminen](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="7a6f5-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="7a6f5-109">Seuraava kuva osoittaa suunnittelun optimoinnin työaikana tapahtuvan käytön edut.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Suunnittelun optimoinnin työaikana tapahtuvan käytön edut](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="7a6f5-111">Parantunut suorituskyky</span><span class="sxs-lookup"><span data-stu-id="7a6f5-111">Improved performance</span></span>

<span data-ttu-id="7a6f5-112">Suunnittelun optimointia voidaan käyttää pitkäkestoisia pääsuunnitelmia sisältävissä skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="7a6f5-113">Se on suunniteltu erityisesti erittäin nopeisiin laskelmiin, joissa käytetään erittäin suuria tietomääriä.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="7a6f5-114">Koska on muodostettu äärimmäisen skaalautuvana monen vuokraajan palveluna, suunnitelman laskemiseen voidaan käyttää samanaikaisesti useita yhdessä työskenteleviä esiintymiä.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="7a6f5-115">Suunnittelupalvelu poistaa lisäksi pääsuunnittelun kuormituksen järjestelmästä ja käyttää palvelinkuormituksen minimoivaa tietovirtaa.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="7a6f5-116">Suunnittelun optimointi auttaa saavuttamaan seuraavat tavoitteet:</span><span class="sxs-lookup"><span data-stu-id="7a6f5-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="7a6f5-117">Lyhentynyt ajoaika parantaa suunnittelun suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="7a6f5-118">Pienentynyt vaikutus muihin prosesseihin pääsuunnitteluajon aikana.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="7a6f5-119">Suunnitteluajojen välit lyhenevät.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-119">Do more frequent planning runs.</span></span> <span data-ttu-id="7a6f5-120">(Ajot eivät rajoitus yhteen kertaan päivässä.)</span><span class="sxs-lookup"><span data-stu-id="7a6f5-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="7a6f5-121">Tieto siitä, että yrityksen kasvu tulevaisuudessa ei ylikuormita suunnittelujärjestelmää.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="7a6f5-122">Arkkitehtuuri ja tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="7a6f5-122">Architecture and data flow</span></span>

<span data-ttu-id="7a6f5-123">Kun suunnittelun optimoinnin lisäosa asennetaan LCS:stä, suunnittelun optimointipalveluun muodostetaan suojattu yhteys.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="7a6f5-124">Palvelu sijaitsee samassa maassa tai samalla alueella olevassa palvelinkeskuksessa kuin liittyvä Supply Chain Management -esiintymä.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="7a6f5-125">Suunnittelun optimoinnin määrittämisen jälkeen päätiedot ja tapahtumatiedot lähetetään pääsuunnittelun suorittamisen aikana Supply Chain Managementista suunnittelun optimointipalveluun.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="7a6f5-126">Jos suunnittelun optimoinnin lisäosan asennus poistetaan, kaikki suunnittelun optimointipalveluun liittyvät tiedot poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="7a6f5-127">Uudelleenluontiajojen korkean tason tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="7a6f5-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="7a6f5-128">Supply Chain Management -asiakasohjelma lähettää signaalin, jolla pyydetään suunnitteluajoa suunnittelun optimoinnista.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="7a6f5-129">Suunnittelun optimointi pyytää tarvittavia tietoja integroidun yhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="7a6f5-130">SQL-tietokanta lähettää pyydetyt asetuksia sekä pää- ja tapahtumatietoja koskevat tiedot suunnittelun optimointiin yhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="7a6f5-131">Yhdistin kääntää tiedot Supply Chain Managementin ja suunnittelun optimointipalvelun välillä.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="7a6f5-132">Suunnittelun optimointipalvelu säilyttää suunnitteluun liittyvät tiedot muistissa ja tekee pyydetyt laskutoimitukset.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="7a6f5-133">Suunnittelun tulos lähetetään Supply Chain Management -tietokantaa yhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="7a6f5-134">Tuloksissa on tietoja esimerkiksi suunnitteluista tilauksista ja tarvekohdistuksesta.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="7a6f5-135">Suunnittelun optimoinnin Supply Chain Managementiin lähettämä signaali ilmaisee, että suunnitteluajo on valmis.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="7a6f5-136">Se lähettää myös mahdolliset liittyvät sanomat ja varoitukset.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="7a6f5-137">Seuraavassa kuvassa näkyy tiedonkulku.</span><span class="sxs-lookup"><span data-stu-id="7a6f5-137">The following illustration shows the data flow.</span></span>

![Uudelleenluontiajojen tiedonkulku](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="7a6f5-139">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="7a6f5-139">Related resources</span></span>

[<span data-ttu-id="7a6f5-140">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="7a6f5-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="7a6f5-141">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="7a6f5-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="7a6f5-142">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="7a6f5-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="7a6f5-143">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="7a6f5-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="7a6f5-144">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="7a6f5-144">Cancel a planning job</span></span>](cancel-planning-job.md)