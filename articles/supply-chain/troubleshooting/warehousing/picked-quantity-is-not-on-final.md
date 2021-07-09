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
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301302"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="7c8d1-103">Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="7c8d1-104">Virhekoodi: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="7c8d1-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="7c8d1-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="7c8d1-105">Symptoms</span></span>

<span data-ttu-id="7c8d1-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="7c8d1-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7c8d1-107">Osaa kuormaan %1 tarvittavista nimikkeistä ei ole vielä kerätty eikä siirretty lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="7c8d1-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7c8d1-109">Syy</span><span class="sxs-lookup"><span data-stu-id="7c8d1-109">Cause</span></span>

<span data-ttu-id="7c8d1-110">Kuormitusta tai lähetystä ei voi vahvistaa nykyisessä tilassaan, koska jokin seuraavista ehdoista voi olla olemassa:</span><span class="sxs-lookup"><span data-stu-id="7c8d1-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="7c8d1-111">Liittyvää työtä ei ole vielä kerätty ja siirretty lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="7c8d1-112">Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="7c8d1-113">Sijaintidirektiivi on määritetty pakkauspaikaksi lopulliseksi toimituspaikaksi aaltomallin säiliöintiä käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="7c8d1-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="7c8d1-114">Resolution</span></span>

<span data-ttu-id="7c8d1-115">Kuorma tai lähetys on tilassa, jossa lähetysvahvistus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="7c8d1-116">Voit korjata ongelman tekemällä yhden seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="7c8d1-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="7c8d1-117">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="7c8d1-118">Peruuta työtunnukset, jotka on luotu pakkaussijainniksi lopulliseksi toimitussijainniksi, konfiguroi sijaintitiedot uudelleen ja aseta kuormitus uudelleen.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="7c8d1-119">Tarkista kuormarivit ja varmista, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat</span><span class="sxs-lookup"><span data-stu-id="7c8d1-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="7c8d1-120">Käytä seuraavaa menettelyä tarkistaaksesi kuormarivit ja varmistaaksesi, että kaikki asiaan liittyvät työt on suoritettu lopullisessa toimituspaikassa ja että määrät vastaavat.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="7c8d1-121">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7c8d1-122">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7c8d1-123">Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="7c8d1-124">Huomioi **Työn luontimäärä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="7c8d1-125">Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="7c8d1-126">Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="7c8d1-127">Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="7c8d1-128">Peruuta työtunnukset, jotka on luotu pakkaussijainniksi lopulliseksi toimitussijainniksi, konfiguroi sijaintitiedot uudelleen ja aseta kuormitus uudelleen</span><span class="sxs-lookup"><span data-stu-id="7c8d1-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="7c8d1-129">Noudata seuraavaa menettelyä peruuttaaksesi työtunnukset, joissa pakkauspaikka on viimeinen sijoituspaikka, kun automaattinen säilytys on paikallaan.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="7c8d1-130">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="7c8d1-131">Näyttöön tulee **Peruuta työ** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="7c8d1-132">Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="7c8d1-133">Valitun työtunnuksen **työtilan** arvona on oltava *Avoin*, *Käynnissä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="7c8d1-134">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-134">Select **OK**.</span></span>
1. <span data-ttu-id="7c8d1-135">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="7c8d1-136">Toista nämä vaiheet tarvittaessa muille työtunnuksille.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="7c8d1-137">Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="7c8d1-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="7c8d1-138">Seuraavia ohjeita noudattamalla voit määrittää sijaintitiedot uudelleen, jotta pakkaussijaintia ei voi käyttää lopullisena lähetyssijainnina, kun mallille määritetään automaattinen konttimääritys.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="7c8d1-139">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="7c8d1-140">Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="7c8d1-141">Valitse sijaintidirektiivi, jota käytät automaattista konttiinpakkausta varten.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="7c8d1-142">Valitse **Sijaintidirektiivitoiminnot**-pikavälilehden työkalupalkista **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="7c8d1-143">Etsi kyselyeditorin valintaikkunassa **Alue**-välilehdestä rivi, jonka **kentän** arvoksi on määritetty *Sijaintiprofiili*, ja varmista, että rivin **kriteeri**-kenttää ei ole määritetty sijaintiprofiiliksi, jonka **sijaintityyppinä** on *Pakkaus*.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="7c8d1-144">Korjaa lopullinen hyllysijainti muokkaamalla **Kriteeri**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="7c8d1-145">Seuraavia ohjeita noudattamalla voit ottaa kuorman uudelleen käyttöön ja luoda työtunnukset, joilla on oikea lopullinen toimitussijainti.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="7c8d1-146">Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="7c8d1-147">Etsi **Kuormitukset**-osassa vapautettava kuormitus.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="7c8d1-148">Vapauta valittu kuorma varastoon valitsemalla **Kuormat**-osan työkalupalkista **Vapautus \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="7c8d1-149">Toista nämä vaiheet tarvittaessa muille kuormituksille.</span><span class="sxs-lookup"><span data-stu-id="7c8d1-149">Repeat this procedure for the other loads as needed.</span></span>
