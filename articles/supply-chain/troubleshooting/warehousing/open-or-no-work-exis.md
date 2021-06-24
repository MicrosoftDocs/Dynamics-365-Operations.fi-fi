---
title: Lähetystä ei voi vahvistaa keskeneräisen tai puuttuvan työn vuoksi
description: Lähetystä ei voi vahvistaa keskeneräisen tai puuttuvan työn vuoksi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123840"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="7cfc6-103">Lähetystä ei voi vahvistaa keskeneräisen tai puuttuvan työn vuoksi</span><span class="sxs-lookup"><span data-stu-id="7cfc6-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="7cfc6-104">Virhekoodi: WAX515</span><span class="sxs-lookup"><span data-stu-id="7cfc6-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="7cfc6-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="7cfc6-105">Symptoms</span></span>

<span data-ttu-id="7cfc6-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="7cfc6-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7cfc6-107">Kuorman %1 lähetystä ei voitu vahvistaa, koska kuorman kaiken työn on oltava valmis.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="7cfc6-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7cfc6-109">Syy</span><span class="sxs-lookup"><span data-stu-id="7cfc6-109">Cause</span></span>

<span data-ttu-id="7cfc6-110">Kuorma tai lähetys on tilassa, jossa lähetysvahvistus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="7cfc6-111">Ennen lähetyksen vahvistusta kuormitukselle on oltava tehtynä edes vähän työtä, ja työn tilan on oltava *Suljettu* tai *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="7cfc6-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="7cfc6-112">Resolution</span></span>

<span data-ttu-id="7cfc6-113">Tarkista kuormitukseen tai lähetykseen liittyvät myyntitilaukset tai siirtotilaukset ja varmista, että kaikki asiaan liittyvät työt on tehty tai peruutettu.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="7cfc6-114">Voit käyttää lähetyksiä ja kuormituksia useilla sivuilla.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="7cfc6-115">Seuraavissa aliosissa on esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="7cfc6-116">Kaikki kuormat -sivu</span><span class="sxs-lookup"><span data-stu-id="7cfc6-116">All loads page</span></span>

1. <span data-ttu-id="7cfc6-117">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7cfc6-118">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7cfc6-119">Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="7cfc6-120">Tarkista kunkin työtunnuksen tila.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="7cfc6-121">Seuraa jokaista työtunnusta, jonka tilana ei ole *Suljettu* tai *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="7cfc6-122">Kun jokaisen työtunnuksen tila on *Suljettu* tai *Peruutettu*, vahvista lähetys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="7cfc6-123">Kaikki lähetykset -sivu</span><span class="sxs-lookup"><span data-stu-id="7cfc6-123">All shipments page</span></span>

1. <span data-ttu-id="7cfc6-124">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="7cfc6-125">Valitse lähetys, jota ei voi vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="7cfc6-126">Valitse toimintoruudun **Lähetykset**-välilehden **Työ**-ryhmässä **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="7cfc6-127">Tarkista kunkin työtunnuksen tila.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="7cfc6-128">Seuraa jokaista työtunnusta, jonka tilana ei ole *Suljettu* tai *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="7cfc6-129">Kun jokaisen työtunnuksen tila on *Suljettu* tai *Peruutettu*, vahvista lähetys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="7cfc6-130">Kaikki työt -sivut</span><span class="sxs-lookup"><span data-stu-id="7cfc6-130">All work page</span></span>

1. <span data-ttu-id="7cfc6-131">Valitse **Varastonhallinta \> Työ\> Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="7cfc6-132">Valitse sen tilausnumeron työ, jonka lähetystä ei voi vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7cfc6-133">Valitse toimintoruudun **Lähetys** -välilehden **Lähetys**-ryhmässä **Vahvista lähetys**.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="7cfc6-134">Tarkista kunkin työtunnuksen tila.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="7cfc6-135">Seuraa jokaista työtunnusta, jonka tilana ei ole *Suljettu* tai *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="7cfc6-136">Kun jokaisen työtunnuksen tila on *Suljettu* tai *Peruutettu*, vahvista lähetys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7cfc6-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
