---
title: Näyttöön tulee virheilmoitus, kun käytössä on sisäinen pääsuunnittelumoduuli
description: Saat virheilmoituksen suorittaessasi vanhentuneen sisäisen pääsuunnittelumoduulin.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294066"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="481cd-103">Näyttöön tulee virheilmoitus, kun käytössä on sisäinen pääsuunnittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="481cd-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="481cd-104">Virhekoodi: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="481cd-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="481cd-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="481cd-105">Symptoms</span></span>

<span data-ttu-id="481cd-106">Suorittaessasi vanhentuneen sisäisen pääsuunnittelumoduulin, saat seuraavan virheilmoituksen:</span><span class="sxs-lookup"><span data-stu-id="481cd-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="481cd-107">Tämä virhesanoma avautuu, koska sisäistä suunnittelumoduulia käytettiin suunnittelun optimoinnin tukemissa skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="481cd-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="481cd-108">Suunnittelun optimointiin kannattaa siirtyä nyt, sillä nykyinen sisäinen pääsuunnittelu vanhentuu.</span><span class="sxs-lookup"><span data-stu-id="481cd-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="481cd-109">Huomaa, että pääsuunnittelun suorittaminen onnistui.</span><span class="sxs-lookup"><span data-stu-id="481cd-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="481cd-110">Jos siirrossa on vahvat riippuvuudet odottaviin toimintoihin, voidaan pyytää poikkeusta sisäisen pääsuunnittelumoduulin käytön jatkamista varten.</span><span class="sxs-lookup"><span data-stu-id="481cd-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="481cd-111">Aloita täyttämällä seuraava kyselylomake ja pyydä tarvittaessa poikkeus suunnittelun optimointiin siirtymisessä.</span><span class="sxs-lookup"><span data-stu-id="481cd-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="481cd-112">Suunnittelun optimoinnin siirto- ja poikkeuskyselylomake</span><span class="sxs-lookup"><span data-stu-id="481cd-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="481cd-113">Syy</span><span class="sxs-lookup"><span data-stu-id="481cd-113">Cause</span></span>

<span data-ttu-id="481cd-114">Jos suoritat suunnittelua etkä käytä tuotannon hallintatoimintoja, harkitse tuotannon optimointiin siirtymistä.</span><span class="sxs-lookup"><span data-stu-id="481cd-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="481cd-115">Sisäinen pääsuunnittelumoduuli on vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="481cd-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="481cd-116">Jos haluat jatkaa käyttöä ilman, että saat virhesanoman, sinun on anottava Microsoftilta poikkeusta.</span><span class="sxs-lookup"><span data-stu-id="481cd-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="481cd-117">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="481cd-117">Resolution</span></span>

<span data-ttu-id="481cd-118">Lisätietoja siitä, miten siirryt suunnittelun optimointiin tai miten poikkeusta sovelletaan, jotta voit edelleen käyttää vanhentunutta sisäistä pääsuunnittelumoduulia, on kohdassa [Siirtyminen suunnittelun optimointiin pääsuunnittelua varten](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="481cd-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
