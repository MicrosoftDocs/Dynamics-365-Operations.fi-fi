---
title: Määrä ylittää ylitoimitusprosentin pakkausluettelon luonnin aikana
description: Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää ylitoimitusprosentin.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249094"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="5003b-103">Määrä ylittää ylitoimitusprosentin pakkausluettelon luonnin aikana</span><span class="sxs-lookup"><span data-stu-id="5003b-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="5003b-104">Virhekoodi: SYS24920</span><span class="sxs-lookup"><span data-stu-id="5003b-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="5003b-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="5003b-105">Symptoms</span></span>

<span data-ttu-id="5003b-106">Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää ylitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="5003b-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="5003b-107">Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="5003b-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="5003b-108">Rivin ylitoimitus on %1 prosenttia, mutta sallittu ylitoimitus on vain %2 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="5003b-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="5003b-109">Et siis voi luoda lähetysluetteloa kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="5003b-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="5003b-110">Syy</span><span class="sxs-lookup"><span data-stu-id="5003b-110">Cause</span></span>

<span data-ttu-id="5003b-111">Kuorman tai lähetyksen keräysmäärä on enemmän kuin tilattu määrä eikä se ole ylitoimitusprosentin alueella.</span><span class="sxs-lookup"><span data-stu-id="5003b-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="5003b-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5003b-112">Resolution</span></span>

<span data-ttu-id="5003b-113">Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="5003b-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="5003b-114">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="5003b-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="5003b-115">Muokkaa kuormitusrivin määrää.</span><span class="sxs-lookup"><span data-stu-id="5003b-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="5003b-116">Muokkaa ylitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="5003b-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="5003b-117">Palauta ja tee tarvittavat oikaisut.</span><span class="sxs-lookup"><span data-stu-id="5003b-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="5003b-118">Muokkaa kuormitusrivin määrää</span><span class="sxs-lookup"><span data-stu-id="5003b-118">Adjust the load line quantity</span></span>

<span data-ttu-id="5003b-119">Seuraavia ohjeita noudattamalla voit säätää kuormarivin määrää.</span><span class="sxs-lookup"><span data-stu-id="5003b-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="5003b-120">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="5003b-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5003b-121">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="5003b-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="5003b-122">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="5003b-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="5003b-123">Valitse  **Kuormitusrivit**-välilehdessä nimikkeelle kuormitusrivi, joka ylittää ylitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="5003b-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="5003b-124">Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.</span><span class="sxs-lookup"><span data-stu-id="5003b-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="5003b-125">Valitse  **Rivin erittely** -välilehdessä **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="5003b-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="5003b-126">Määritä **Määrä**-kentässä arvo kerätyksi määräksi (eli **Työn luontimäärä** -kentän arvo), jotta lähetysluettelon luontia voidaan jatkaa.</span><span class="sxs-lookup"><span data-stu-id="5003b-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="5003b-127">Muokkaa ylitoimitusprosenttia</span><span class="sxs-lookup"><span data-stu-id="5003b-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="5003b-128">Seuraavia ohjeita noudattamalla voit säätää ylitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="5003b-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="5003b-129">Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5003b-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="5003b-130">Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.</span><span class="sxs-lookup"><span data-stu-id="5003b-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="5003b-131">Valitse  **Myyntitilausrivit**-välilehdessä nimikkeelle myyntitilausrivi, joka ylittää ylitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="5003b-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="5003b-132">Valitse  **Rivin erittely** -välilehdessä **Toimitus**.</span><span class="sxs-lookup"><span data-stu-id="5003b-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="5003b-133">Määritä **Ylitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysluettelon luonti voi jatkua.</span><span class="sxs-lookup"><span data-stu-id="5003b-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="5003b-134">Palauta ja tee tarvittavat oikaisut</span><span class="sxs-lookup"><span data-stu-id="5003b-134">Reverse and make adjustments</span></span>

<span data-ttu-id="5003b-135">Peruuta kaikki kuormitukselle kirjatut tiedot (esimerkiksi pakkausluettelo, lähetysvahvistus ja työ), tee myyntitilauksen oikaisut, vapauta tilaus uudelleen varastoon ja suorita lähetysmenettely valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="5003b-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="5003b-136">Seuraavia ohjeita noudattamalla voit peruuttaa pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="5003b-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="5003b-137">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="5003b-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5003b-138">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Pakkausluettelon peruutus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="5003b-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="5003b-139">Seuraavia ohjeita noudattamalla voit peruuttaa lähetyksen vahvistuksen.</span><span class="sxs-lookup"><span data-stu-id="5003b-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="5003b-140">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="5003b-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5003b-141">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="5003b-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="5003b-142">Seuraavia ohjeita noudattamalla voit peruuttaa työn.</span><span class="sxs-lookup"><span data-stu-id="5003b-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="5003b-143">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="5003b-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5003b-144">Valitse toimintoruudun  **Kuormitukset**-välilehden  **Työ**-ryhmässä  **Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="5003b-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
