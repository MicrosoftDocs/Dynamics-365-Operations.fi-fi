---
title: Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.
description: Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123816"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="fff82-103">Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="fff82-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="fff82-104">Virhekoodi: WAX1686</span><span class="sxs-lookup"><span data-stu-id="fff82-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="fff82-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="fff82-105">Symptoms</span></span>

<span data-ttu-id="fff82-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="fff82-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="fff82-107">Kuormituksen %1 lähetystä ei voitu vahvistaa, koska nimikkeen %2 määrä ylittää alitoimitukselle määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="fff82-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="fff82-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="fff82-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="fff82-109">Syy</span><span class="sxs-lookup"><span data-stu-id="fff82-109">Cause</span></span>

<span data-ttu-id="fff82-110">Kuormituksen tai lähetyksen määrä on kerätty vain osittain.</span><span class="sxs-lookup"><span data-stu-id="fff82-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="fff82-111">Määrä alittaa tällä hetkellä kerätyn määrän prosenttiosuutena, joka on sallitun alitoimitusprosentin ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="fff82-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="fff82-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="fff82-112">Resolution</span></span>

<span data-ttu-id="fff82-113">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="fff82-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="fff82-114">Määritä kuormitusrivin määrä.</span><span class="sxs-lookup"><span data-stu-id="fff82-114">Set the load line quantity.</span></span>
- <span data-ttu-id="fff82-115">Määritä alitoimitusprosentti.</span><span class="sxs-lookup"><span data-stu-id="fff82-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="fff82-116">Määritä kuormitusrivin määrä</span><span class="sxs-lookup"><span data-stu-id="fff82-116">Set the load line quantity</span></span>

<span data-ttu-id="fff82-117">Voit määrittää kuormitusrivin määrän noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="fff82-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="fff82-118">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="fff82-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="fff82-119">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="fff82-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="fff82-120">Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="fff82-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="fff82-121">Valitse **Rivin erittely** -pikavälilehdessä **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="fff82-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="fff82-122">Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -arvoksi), jotta lähetysvahvistus voi tapahtua.</span><span class="sxs-lookup"><span data-stu-id="fff82-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="fff82-123">Määritä alitoimitusprosentti</span><span class="sxs-lookup"><span data-stu-id="fff82-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="fff82-124">Voit määrittää alitoimitusprosentin noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="fff82-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="fff82-125">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="fff82-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="fff82-126">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="fff82-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="fff82-127">Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="fff82-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="fff82-128">Valitse **Rivin erittely** -pikavälilehdessä **Yleinen**.</span><span class="sxs-lookup"><span data-stu-id="fff82-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="fff82-129">Määritä **Alitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysvahvistus voi tapahtua.</span><span class="sxs-lookup"><span data-stu-id="fff82-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
