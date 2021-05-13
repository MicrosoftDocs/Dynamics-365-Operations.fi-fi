---
title: Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.
description: Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.
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
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938460"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="38cf2-103">Et voi vahvistaa lähetystä, koska määrä ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="38cf2-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="38cf2-104">Virhekoodi: WAX1687</span><span class="sxs-lookup"><span data-stu-id="38cf2-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="38cf2-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="38cf2-105">Symptoms</span></span>

<span data-ttu-id="38cf2-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="38cf2-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="38cf2-107">Kuormituksen %1 lähetystä ei voitu vahvistaa, koska nimikkeen %2 määrä ylittää alitoimitukselle määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="38cf2-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="38cf2-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="38cf2-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="38cf2-109">Syy</span><span class="sxs-lookup"><span data-stu-id="38cf2-109">Cause</span></span>

<span data-ttu-id="38cf2-110">Kuormituksen tai lähetyksen määrä on kerätty vain osittain.</span><span class="sxs-lookup"><span data-stu-id="38cf2-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="38cf2-111">Määrä alittaa tällä hetkellä kerätyn määrän prosenttiosuutena, joka on sallitun alitoimitusprosentin ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="38cf2-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="38cf2-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="38cf2-112">Resolution</span></span>

<span data-ttu-id="38cf2-113">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="38cf2-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="38cf2-114">Määritä kuormitusrivin määrä.</span><span class="sxs-lookup"><span data-stu-id="38cf2-114">Set the load line quantity.</span></span>
- <span data-ttu-id="38cf2-115">Määritä alitoimitusprosentti.</span><span class="sxs-lookup"><span data-stu-id="38cf2-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="38cf2-116">Määritä kuormitusrivin määrä</span><span class="sxs-lookup"><span data-stu-id="38cf2-116">Set the load line quantity</span></span>

<span data-ttu-id="38cf2-117">Voit määrittää kuormitusrivin määrän noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="38cf2-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="38cf2-118">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="38cf2-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="38cf2-119">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="38cf2-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="38cf2-120">Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="38cf2-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="38cf2-121">Valitse **Rivin erittely** -pikavälilehdessä **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="38cf2-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="38cf2-122">Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -arvoksi), jotta lähetysvahvistus voi tapahtua.</span><span class="sxs-lookup"><span data-stu-id="38cf2-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="38cf2-123">Määritä alitoimitusprosentti</span><span class="sxs-lookup"><span data-stu-id="38cf2-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="38cf2-124">Voit määrittää alitoimitusprosentin noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="38cf2-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="38cf2-125">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="38cf2-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="38cf2-126">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="38cf2-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="38cf2-127">Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="38cf2-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="38cf2-128">Valitse **Rivin erittely** -pikavälilehdessä **Yleinen**.</span><span class="sxs-lookup"><span data-stu-id="38cf2-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="38cf2-129">Määritä **Alitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysvahvistus voi tapahtua.</span><span class="sxs-lookup"><span data-stu-id="38cf2-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
