---
title: Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.
description: Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938462"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="d77bf-103">Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.</span><span class="sxs-lookup"><span data-stu-id="d77bf-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="d77bf-104">Virhekoodi: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="d77bf-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="d77bf-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="d77bf-105">Symptoms</span></span>

<span data-ttu-id="d77bf-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="d77bf-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="d77bf-107">Osaa kuormaan %1 tarvittavista nimikkeistä ei ole vielä kerätty eikä siirretty lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d77bf-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="d77bf-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="d77bf-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="d77bf-109">Syy</span><span class="sxs-lookup"><span data-stu-id="d77bf-109">Cause</span></span>

<span data-ttu-id="d77bf-110">Kuormitusta tai lähetystä ei voi vahvistaa nykyisessä tilassaan, koska jokin seuraavista ehdoista voi olla olemassa:</span><span class="sxs-lookup"><span data-stu-id="d77bf-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="d77bf-111">Liittyvää työtä ei ole vielä kerätty ja siirretty lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d77bf-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="d77bf-112">Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="d77bf-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="d77bf-113">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d77bf-113">Resolution</span></span>

<span data-ttu-id="d77bf-114">Tarkista kuormituksen tai lähetyksen liittyvät myyntitilaukset tai siirtotilaukset.</span><span class="sxs-lookup"><span data-stu-id="d77bf-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="d77bf-115">Varmista, että kaikki liittyvä työ on tehty loppuun lopullisessa lähetyssijainnissa ja että määrät vastaavat toisiaan.</span><span class="sxs-lookup"><span data-stu-id="d77bf-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="d77bf-116">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="d77bf-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d77bf-117">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="d77bf-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="d77bf-118">Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d77bf-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="d77bf-119">Huomioi **Työn luontimäärä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="d77bf-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="d77bf-120">Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="d77bf-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="d77bf-121">Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="d77bf-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="d77bf-122">Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="d77bf-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
