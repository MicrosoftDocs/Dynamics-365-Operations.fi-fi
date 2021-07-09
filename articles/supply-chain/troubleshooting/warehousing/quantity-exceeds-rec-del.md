---
title: Päivitettävä määrä ylittää vastaanotettavan/toimitetun määrän.
description: Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ylittää työmäärän, joka oli kerätty ja varattu myyntitilaukselle.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249097"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="a1064-103">Päivitettävä määrä ylittää vastaanotettavan/toimitetun määrän</span><span class="sxs-lookup"><span data-stu-id="a1064-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="a1064-104">Virhekoodi: SYS7676</span><span class="sxs-lookup"><span data-stu-id="a1064-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="a1064-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="a1064-105">Symptoms</span></span>

<span data-ttu-id="a1064-106">Kun luot pakkausluettelon, lähtevä kuorma sisältää määrän, joka ylittää työmäärän, joka oli kerätty ja varattu myyntitilaukselle.</span><span class="sxs-lookup"><span data-stu-id="a1064-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="a1064-107">Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="a1064-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="a1064-108">Määrä, jota yrität päivittää, ylittää vastaanotetun/toimitetun määrän.</span><span class="sxs-lookup"><span data-stu-id="a1064-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="a1064-109">Et siis voi luoda lähetysluetteloa kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="a1064-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a1064-110">Syy</span><span class="sxs-lookup"><span data-stu-id="a1064-110">Cause</span></span>

<span data-ttu-id="a1064-111">Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="a1064-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="a1064-112">Tämä ongelma voi ilmetä esimerkiksi silloin, kun kuormarivin määrä, luodun määrän tai kerätty määrä ei ole oikein.</span><span class="sxs-lookup"><span data-stu-id="a1064-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1064-113">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="a1064-113">Resolution</span></span>

<span data-ttu-id="a1064-114">Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="a1064-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="a1064-115">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="a1064-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="a1064-116">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="a1064-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="a1064-117">Muokkaa kuormitusrivin määrää.</span><span class="sxs-lookup"><span data-stu-id="a1064-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="a1064-118">Palauta kaikki keräilymerkinnät ja tee keräys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a1064-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="a1064-119">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat</span><span class="sxs-lookup"><span data-stu-id="a1064-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="a1064-120">Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="a1064-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="a1064-121">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="a1064-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a1064-122">Valitse kuormitus, jolle ei voi luoda lähetystä.</span><span class="sxs-lookup"><span data-stu-id="a1064-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="a1064-123">Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a1064-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="a1064-124">Huomioi **Työn luontimäärä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="a1064-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="a1064-125">Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="a1064-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="a1064-126">Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="a1064-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="a1064-127">Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="a1064-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="a1064-128">Muokkaa kuormitusrivin määrää</span><span class="sxs-lookup"><span data-stu-id="a1064-128">Adjust the load line quantity</span></span>

<span data-ttu-id="a1064-129">Seuraavia ohjeita noudattamalla voit säätää kuormarivin määrää.</span><span class="sxs-lookup"><span data-stu-id="a1064-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="a1064-130">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="a1064-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a1064-131">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="a1064-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="a1064-132">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="a1064-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="a1064-133">Valitse  **Kuormitusrivit**-välilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.</span><span class="sxs-lookup"><span data-stu-id="a1064-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="a1064-134">Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.</span><span class="sxs-lookup"><span data-stu-id="a1064-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="a1064-135">Määritä **Pienennä kuormitusrivi** -kenttä vastaamaan kuormitusrivin oikaisuja.</span><span class="sxs-lookup"><span data-stu-id="a1064-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="a1064-136">Palauta kaikki keräilymerkinnät ja tee keräys uudelleen</span><span class="sxs-lookup"><span data-stu-id="a1064-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="a1064-137">Jos joku käyttää keräysrekisteröintiä kuormarivin sulkemiseen ilman työtä, kuormarivin määrän ja kerätyn määrän välillä voi olla ristiriita.</span><span class="sxs-lookup"><span data-stu-id="a1064-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="a1064-138">Tässä tapauksessa manuaalinen keräilyrekisteröinti on peruutettava, ja keräily on sitten suoritettava käyttämällä Warehouse Management -mobiilisovellusta.</span><span class="sxs-lookup"><span data-stu-id="a1064-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="a1064-139">Seuraavia ohjeita noudattamalla voit peruuttaa keräilyrekisteröinnin.</span><span class="sxs-lookup"><span data-stu-id="a1064-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="a1064-140">Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="a1064-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="a1064-141">Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.</span><span class="sxs-lookup"><span data-stu-id="a1064-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="a1064-142">Valitse  **Myyntitilausrivit**-välilehdestä myyntitilausrivi, jota varten rekisteröinti on tehty.</span><span class="sxs-lookup"><span data-stu-id="a1064-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="a1064-143">Voit poistaa nimikkeet valitsemalla **Päivitä rivi \> Kerää**.</span><span class="sxs-lookup"><span data-stu-id="a1064-143">Select **Update line \> Pick** to unpick the items.</span></span>
