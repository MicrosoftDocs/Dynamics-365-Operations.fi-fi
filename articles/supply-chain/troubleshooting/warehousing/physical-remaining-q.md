---
title: Fyysisen jäljelle jäävän määrän yksikkö ei saa olla nolla
description: Kun luot pakkausluettelon, sen tietojen varastomäärä on muu kuin nolla mutta myyntimäärä on nolla.
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
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248778"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="443e1-103">Fyysisen jäljelle jäävän määrän yksikkö ei saa olla nolla</span><span class="sxs-lookup"><span data-stu-id="443e1-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="443e1-104">Virhekoodi: SYS19591</span><span class="sxs-lookup"><span data-stu-id="443e1-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="443e1-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="443e1-105">Symptoms</span></span>

<span data-ttu-id="443e1-106">Kun luot pakkausluettelon, sen tietojen varastomäärä on muu kuin nolla mutta myyntimäärä on nolla.</span><span class="sxs-lookup"><span data-stu-id="443e1-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="443e1-107">Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="443e1-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="443e1-108">Fyysisen jäännösmäärän yksikössä %1 täytyy olla muu kuin nolla.</span><span class="sxs-lookup"><span data-stu-id="443e1-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="443e1-109">Et siis voi luoda lähetysluetteloa kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="443e1-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="443e1-110">Syy</span><span class="sxs-lookup"><span data-stu-id="443e1-110">Cause</span></span>

<span data-ttu-id="443e1-111">Järjestelmä arvioi fyysisen jäljellä olevan määrän varastoyksikköinä ja fyysisen jäljellä olevan määrän lähetysyksikössä.</span><span class="sxs-lookup"><span data-stu-id="443e1-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="443e1-112">Jos järjestelmä havaitsee, että lähetysyksikön fyysinen jäljellä oleva määrä on 0 (nolla), mutta varastoyksikön fyysinen jäljellä oleva määrä ei ole 0, pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="443e1-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="443e1-113">Tämä ongelma voi ilmetä esimerkiksi silloin, kun nimikkeen myyntiyksikkö ja varastoyksikkö eivät ole oikein eikä yksiköiden välinen muunnos ole oikein.</span><span class="sxs-lookup"><span data-stu-id="443e1-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="443e1-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="443e1-114">Resolution</span></span>

<span data-ttu-id="443e1-115">Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="443e1-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="443e1-116">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="443e1-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="443e1-117">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="443e1-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="443e1-118">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa.</span><span class="sxs-lookup"><span data-stu-id="443e1-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="443e1-119">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.</span><span class="sxs-lookup"><span data-stu-id="443e1-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="443e1-120">Varmista, että varaston mittayksikkö on pienempi kuin myynnin mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="443e1-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="443e1-121">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat</span><span class="sxs-lookup"><span data-stu-id="443e1-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="443e1-122">Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="443e1-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="443e1-123">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="443e1-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="443e1-124">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="443e1-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="443e1-125">Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="443e1-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="443e1-126">Huomioi **Työn luontimäärä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="443e1-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="443e1-127">Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="443e1-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="443e1-128">Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="443e1-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="443e1-129">Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="443e1-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="443e1-130">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman desimaalinumeroiden ja minkä tahansa muun pyöristysongelmaa</span><span class="sxs-lookup"><span data-stu-id="443e1-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="443e1-131">Tarkista seuraavan ohjeen avulla kuormarivit ja tee tarvittavat korjaukset, jotta määrä voidaan muuntaa puhtaasti ilman pyöristysongelmia.</span><span class="sxs-lookup"><span data-stu-id="443e1-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="443e1-132">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="443e1-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="443e1-133">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="443e1-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="443e1-134">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="443e1-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="443e1-135">Valitse  **Kuormitusrivit**-välilehdessä nimikkeelle kuormitusrivi, joka ylittää ylitoimituksen.</span><span class="sxs-lookup"><span data-stu-id="443e1-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="443e1-136">Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.</span><span class="sxs-lookup"><span data-stu-id="443e1-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="443e1-137">Valitse  **Rivin erittely** -välilehdessä **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="443e1-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="443e1-138">Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -kentän arvo), jotta lähetysluettelon luontia voidaan jatkaa.</span><span class="sxs-lookup"><span data-stu-id="443e1-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="443e1-139">Tarkista kuormarivit ja tee tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla</span><span class="sxs-lookup"><span data-stu-id="443e1-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="443e1-140">Käytä seuraavia vaiheita tarkistaaksesi kuormarivit ja tehdäksesi tarvittavat korjaukset, jotta yksikkö ja määrä ovat yksikön desimaalitarkkuuden tasalla.</span><span class="sxs-lookup"><span data-stu-id="443e1-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="443e1-141">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="443e1-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="443e1-142">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="443e1-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="443e1-143">Valitse **Kuormitusrivit**-pikavälilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.</span><span class="sxs-lookup"><span data-stu-id="443e1-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="443e1-144">Huomioi **Määrä**- ja **Yksikkö**-kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="443e1-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="443e1-145">Valitse **Organisaation hallinta \> Yksiköt \> Yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="443e1-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="443e1-146">Valitse yksikkö, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="443e1-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="443e1-147">Säädä **desimaalitarkkuus**-kentän arvoa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="443e1-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="443e1-148">Varmista, että varaston mittayksikkö on pienempi kuin myynnin mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="443e1-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="443e1-149">Varmista, että varaston mittayksikkö on pienempi kuin myynnin mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="443e1-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="443e1-150">Harkitse mittayksikön määrittämistä uudelleen nimikkeelle tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="443e1-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
