---
title: Kerätyt määrät eivät riitä pakkausluettelon luonnin aikana
description: Kun luot pakkausluettelon, lähtevä kuorma sisältää kerätyn määrän, joka ei vastaa kuormituslinjalla luotua työmäärää.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249096"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="cd26c-103">Kerätyt määrät eivät riitä pakkausluettelon luonnin aikana</span><span class="sxs-lookup"><span data-stu-id="cd26c-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="cd26c-104">Virhekoodi: SYS54073</span><span class="sxs-lookup"><span data-stu-id="cd26c-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="cd26c-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="cd26c-105">Symptoms</span></span>

<span data-ttu-id="cd26c-106">Kun luot pakkausluettelon, lähtevä kuorma sisältää kerätyn määrän, joka ei vastaa kuormituslinjalla luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="cd26c-107">Kun yrität luoda lähetysluettelon, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="cd26c-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="cd26c-108">Koska %1 on keräily, kohteen %2 päivittäminen ei riitä, jos jäännöksen on oltava %3.</span><span class="sxs-lookup"><span data-stu-id="cd26c-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="cd26c-109">Et siis voi luoda lähetysluetteloa kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="cd26c-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="cd26c-110">Syy</span><span class="sxs-lookup"><span data-stu-id="cd26c-110">Cause</span></span>

<span data-ttu-id="cd26c-111">Pakkausluetteloa ei voi luoda nykyisessä tilassaan, koska jokin seuraavista ehdoista voi olla olemassa:</span><span class="sxs-lookup"><span data-stu-id="cd26c-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="cd26c-112">Liittyvää työtä ei ole vielä kerätty ja siirretty lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="cd26c-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="cd26c-113">Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="cd26c-114">Kuormituslinjan määrä, työn luoma määrä ja poimittu määrä eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="cd26c-115">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="cd26c-115">Resolution</span></span>

<span data-ttu-id="cd26c-116">Kuorma tai lähetys on tilassa, jossa lähetysluettelon luonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="cd26c-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="cd26c-117">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="cd26c-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="cd26c-118">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="cd26c-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="cd26c-119">Muokkaa kuormitusrivin määrää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="cd26c-120">Palauta kaikki keräilymerkinnät ja tee keräys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="cd26c-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="cd26c-121">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat</span><span class="sxs-lookup"><span data-stu-id="cd26c-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="cd26c-122">Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="cd26c-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="cd26c-123">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="cd26c-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cd26c-124">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="cd26c-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd26c-125">Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="cd26c-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="cd26c-126">Huomioi **Työn luontimäärä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="cd26c-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="cd26c-127">Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="cd26c-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="cd26c-128">Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="cd26c-129">Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="cd26c-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="cd26c-130">Muokkaa kuormitusrivin määrää</span><span class="sxs-lookup"><span data-stu-id="cd26c-130">Adjust the load line quantity</span></span>

<span data-ttu-id="cd26c-131">Seuraavia ohjeita noudattamalla voit säätää kuormarivin määrää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="cd26c-132">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="cd26c-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cd26c-133">Valitse kuorma, jota varten pakkausluetteloa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="cd26c-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd26c-134">Valitse toimintoruudun  **Lähetys ja vastaanotto** -välilehden  **Käänteisen lähetyksen vahvistus**  **Käänteinen**-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="cd26c-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="cd26c-135">Valitse  **Kuormitusrivit**-välilehdessä kuormitusrivi nimikkeelle, joka aiheuttaa ongelman.</span><span class="sxs-lookup"><span data-stu-id="cd26c-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="cd26c-136">Valitse **Vähennä kerättyä määrää** säätääksesi keräysmäärää.</span><span class="sxs-lookup"><span data-stu-id="cd26c-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="cd26c-137">Määritä **Pienennä kuormitusrivi** -kenttä vastaamaan kuormitusrivin oikaisuja.</span><span class="sxs-lookup"><span data-stu-id="cd26c-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="cd26c-138">Palauta kaikki keräilymerkinnät ja tee keräys uudelleen</span><span class="sxs-lookup"><span data-stu-id="cd26c-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="cd26c-139">Ongelma saattaa ilmetä, koska henkilö on käyttänyt valintarekisteröintiä kuormarivin sulkemiseen ilman työtä.</span><span class="sxs-lookup"><span data-stu-id="cd26c-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="cd26c-140">Tässä tapauksessa manuaalinen keräilyrekisteröinti on peruutettava, ja keräily on sitten suoritettava käyttämällä Warehouse Management -mobiilisovellusta.</span><span class="sxs-lookup"><span data-stu-id="cd26c-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="cd26c-141">Seuraavia ohjeita noudattamalla voit peruuttaa keräilyrekisteröinnin.</span><span class="sxs-lookup"><span data-stu-id="cd26c-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="cd26c-142">Valitse **Myyntireskontra \> Tilaukset \> Kaikki tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cd26c-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="cd26c-143">Valitse myyntitilaus, jolle et voi kirjata pakkausluetteloa kuormalle.</span><span class="sxs-lookup"><span data-stu-id="cd26c-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="cd26c-144">Valitse  **Myyntitilausrivit**-välilehdestä myyntitilausrivi, jota varten rekisteröinti on tehty.</span><span class="sxs-lookup"><span data-stu-id="cd26c-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="cd26c-145">Voit poistaa nimikkeet valitsemalla **Päivitä rivi \> Kerää**.</span><span class="sxs-lookup"><span data-stu-id="cd26c-145">Select **Update line \> Pick** to unpick the items.</span></span>
