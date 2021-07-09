---
title: Fyysisen päivitysmäärän desimaalipyöristys on virheellinen
description: Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ei vastaa yksikön määrittämää desimaalitarkkuutta.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248779"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="ccaae-103">Fyysisen päivitysmäärän desimaalipyöristys on virheellinen</span><span class="sxs-lookup"><span data-stu-id="ccaae-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="ccaae-104">Virhekoodi: SYS19589</span><span class="sxs-lookup"><span data-stu-id="ccaae-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="ccaae-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="ccaae-105">Symptoms</span></span>

<span data-ttu-id="ccaae-106">Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ei vastaa yksikön määrittämää desimaalitarkkuutta.</span><span class="sxs-lookup"><span data-stu-id="ccaae-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="ccaae-107">Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="ccaae-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="ccaae-108">Yksikön %1 fyysisen päivitysmäärän desimaalipyöristys on virheellinen.</span><span class="sxs-lookup"><span data-stu-id="ccaae-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="ccaae-109">Et siis voi luoda lähetysluetteloa kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="ccaae-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="ccaae-110">Syy</span><span class="sxs-lookup"><span data-stu-id="ccaae-110">Cause</span></span>

<span data-ttu-id="ccaae-111">Järjestelmä arvioi, vastaako lähetysmäärän desimaalipyöristys lähetysyksikölle määritettyä desimaalitarkkuutta.</span><span class="sxs-lookup"><span data-stu-id="ccaae-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="ccaae-112">Kun järjestelmä pyöristää lähetysmäärän määritettyyn desimaalien määrään ja havaitsee, että pyöristetty lähetysmäärä ei vastaa varsinaista lähetysmäärää, pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="ccaae-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="ccaae-113">Tämä ongelma voi ilmetä esimerkiksi silloin, kun myyntimäärä on 1,75 kilogrammaa (kg), mutta desimaalitarkkuus on *1*.</span><span class="sxs-lookup"><span data-stu-id="ccaae-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ccaae-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ccaae-114">Resolution</span></span>

<span data-ttu-id="ccaae-115">Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="ccaae-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="ccaae-116">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="ccaae-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="ccaae-117">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa.</span><span class="sxs-lookup"><span data-stu-id="ccaae-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="ccaae-118">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.</span><span class="sxs-lookup"><span data-stu-id="ccaae-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="ccaae-119">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa</span><span class="sxs-lookup"><span data-stu-id="ccaae-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="ccaae-120">Tarkista seuraavan ohjeen avulla kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa</span><span class="sxs-lookup"><span data-stu-id="ccaae-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="ccaae-121">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="ccaae-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ccaae-122">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="ccaae-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="ccaae-123">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="ccaae-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="ccaae-124">Valitse  **Kuormitusrivit**-välilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.</span><span class="sxs-lookup"><span data-stu-id="ccaae-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="ccaae-125">Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.</span><span class="sxs-lookup"><span data-stu-id="ccaae-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="ccaae-126">Valitse  **Rivin erittely** -välilehdessä **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="ccaae-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="ccaae-127">Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -kentän arvo), jotta lähetysluettelon luontia voidaan jatkaa.</span><span class="sxs-lookup"><span data-stu-id="ccaae-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="ccaae-128">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla</span><span class="sxs-lookup"><span data-stu-id="ccaae-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="ccaae-129">Käytä seuraavia vaiheita tarkistaaksesi kuormarivit ja tehdäksesi tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.</span><span class="sxs-lookup"><span data-stu-id="ccaae-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="ccaae-130">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="ccaae-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ccaae-131">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="ccaae-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="ccaae-132">Valitse **Kuormitusrivit**-pikavälilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.</span><span class="sxs-lookup"><span data-stu-id="ccaae-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="ccaae-133">Huomioi **Määrä**- ja **Yksikkö**-kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="ccaae-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="ccaae-134">Valitse **Organisaation hallinta \> Yksiköt \> Yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="ccaae-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="ccaae-135">Valitse yksikkö, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="ccaae-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="ccaae-136">Säädä **desimaalitarkkuus**-kentän arvoa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="ccaae-136">Adjust the value of the **Decimal precision** field as required.</span></span>
