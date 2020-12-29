---
title: Edeltäjän lisääminen tuotantovirran tehtävään
description: Kaikkien tehtävien on oltava järjestyksessä tuotantovirran versiossa.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39cef1174439b42a072bd7fc1ac29ef31ecf864
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426805"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="af3ef-103">Edeltäjän lisääminen tuotantovirran tehtävään</span><span class="sxs-lookup"><span data-stu-id="af3ef-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af3ef-104">Kaikkien tehtävien on oltava järjestyksessä tuotantovirran versiossa.</span><span class="sxs-lookup"><span data-stu-id="af3ef-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="af3ef-105">Tehtävällä voi olla yksi tai useampi edeltäjä tai seuraaja.</span><span class="sxs-lookup"><span data-stu-id="af3ef-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="af3ef-106">Tässä menettelyssä kuvataan, miten liität tehtävään edeltäjän.</span><span class="sxs-lookup"><span data-stu-id="af3ef-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="af3ef-107">Tämän tehtävän suorittamiseen tarvitset tuotantovirran, jossa on luonnosversio, jolla on vähintään kaksi yhdistettävää aktiviteetteihin.</span><span class="sxs-lookup"><span data-stu-id="af3ef-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="af3ef-108">Lisätietoja on mietinnössä Lean-valmistuksen tuotantovirrat ja tehtävät.</span><span class="sxs-lookup"><span data-stu-id="af3ef-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="af3ef-109">Etsi tuotantovirta ja versio</span><span class="sxs-lookup"><span data-stu-id="af3ef-109">Find the production flow and version</span></span>
1. <span data-ttu-id="af3ef-110">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="af3ef-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="af3ef-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="af3ef-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="af3ef-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="af3ef-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="af3ef-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="af3ef-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="af3ef-114">Valitse Tehtävät.</span><span class="sxs-lookup"><span data-stu-id="af3ef-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="af3ef-115">Valitse tehtävä ja lisää edeltäjä</span><span class="sxs-lookup"><span data-stu-id="af3ef-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="af3ef-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="af3ef-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="af3ef-117">Valitse Lisää edeltäjä.</span><span class="sxs-lookup"><span data-stu-id="af3ef-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="af3ef-118">Syötä tai valitse arvo Tehtävä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="af3ef-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="af3ef-119">Lisää Syklin kestojen suhde -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="af3ef-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="af3ef-120">Tehtäväsuhteen oletusarvoinen syklin keston suhde on 1.</span><span class="sxs-lookup"><span data-stu-id="af3ef-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="af3ef-121">Oletuksena on, että molemmat tehtävät suoritetaan samassa tahdissa eli niiden tahtiaika on sama.</span><span class="sxs-lookup"><span data-stu-id="af3ef-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="af3ef-122">Jos edeltäjä suoritetaan suuremmalla nopeudella (alempi tahtiaika), suhteen pitäisi olla pienempi kuin 1; jos edeltäjä suoritetaan hitaammalla nopeudella (korkeampi tahtiaika) syklin kestosuhde on suurempi kuin 1.</span><span class="sxs-lookup"><span data-stu-id="af3ef-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="af3ef-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="af3ef-123">Click OK.</span></span>

