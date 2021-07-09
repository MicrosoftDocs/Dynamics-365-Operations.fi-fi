---
title: Määrä ylittää alitoimitusprosentin pakkausluettelon luonnin aikana
description: Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää alitoimitusprosentin.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249092"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="e100a-103">Määrä ylittää alitoimitusprosentin pakkausluettelon luonnin aikana</span><span class="sxs-lookup"><span data-stu-id="e100a-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="e100a-104">Virhekoodi: SYS24921</span><span class="sxs-lookup"><span data-stu-id="e100a-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="e100a-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="e100a-105">Symptoms</span></span>

<span data-ttu-id="e100a-106">Kun luot pakkausluettelon, lähtevä kuormitus sisältää määrän, joka ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="e100a-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="e100a-107">Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="e100a-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="e100a-108">Rivin alitoimitus on %1 prosenttia, mutta sallittu alitoimitus on vain %2 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="e100a-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="e100a-109">Et siis voi luoda lähetysluetteloa kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="e100a-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e100a-110">Syy</span><span class="sxs-lookup"><span data-stu-id="e100a-110">Cause</span></span>

<span data-ttu-id="e100a-111">Kuorman tai lähetyksen keräysmäärä on vähemmän kuin tilattu määrä eikä se ole alitoimitusprosentin alueella.</span><span class="sxs-lookup"><span data-stu-id="e100a-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="e100a-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e100a-112">Resolution</span></span>

<span data-ttu-id="e100a-113">Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="e100a-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="e100a-114">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="e100a-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="e100a-115">Muokkaa alitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="e100a-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="e100a-116">Palauta ja tee tarvittavat oikaisut.</span><span class="sxs-lookup"><span data-stu-id="e100a-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="e100a-117">Muokkaa alitoimitusprosenttia</span><span class="sxs-lookup"><span data-stu-id="e100a-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="e100a-118">Seuraavia ohjeita noudattamalla voit säätää alitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="e100a-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="e100a-119">Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e100a-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="e100a-120">Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.</span><span class="sxs-lookup"><span data-stu-id="e100a-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="e100a-121">Valitse  **Myyntitilausrivit**-välilehdessä nimikkeelle myyntitilausrivi, joka ylittää alitoimitusprosenttia.</span><span class="sxs-lookup"><span data-stu-id="e100a-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="e100a-122">Valitse  **Rivin erittely** -välilehdessä **Toimitus**.</span><span class="sxs-lookup"><span data-stu-id="e100a-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="e100a-123">Määritä **Alitoimitus**-kentässä arvoksi suurempi prosenttiarvo, joka sopii kerättyyn määrään suhteessa kuormituksen määrään, jotta lähetysluettelon luonti voi jatkua.</span><span class="sxs-lookup"><span data-stu-id="e100a-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="e100a-124">Palauta ja tee tarvittavat oikaisut</span><span class="sxs-lookup"><span data-stu-id="e100a-124">Reverse and make adjustments</span></span>

<span data-ttu-id="e100a-125">Peruuta kaikki kuormitukselle kirjatut tiedot (esimerkiksi pakkausluettelo, lähetysvahvistus ja työ), tee myyntitilauksen oikaisut, vapauta tilaus uudelleen varastoon ja suorita lähetysmenettely valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="e100a-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="e100a-126">Seuraavia ohjeita noudattamalla voit peruuttaa pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="e100a-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="e100a-127">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="e100a-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e100a-128">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Pakkausluettelon peruutus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="e100a-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="e100a-129">Seuraavia ohjeita noudattamalla voit peruuttaa lähetyksen vahvistuksen.</span><span class="sxs-lookup"><span data-stu-id="e100a-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="e100a-130">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="e100a-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e100a-131">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="e100a-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="e100a-132">Seuraavia ohjeita noudattamalla voit peruuttaa työn.</span><span class="sxs-lookup"><span data-stu-id="e100a-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="e100a-133">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="e100a-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e100a-134">Valitse toimintoruudun  **Kuormitukset**-välilehden  **Työ**-ryhmässä  **Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="e100a-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
