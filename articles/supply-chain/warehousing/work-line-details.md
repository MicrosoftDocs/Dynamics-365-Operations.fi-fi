---
title: Työrivin tiedot
description: Tässä ohjeaiheessa on tietoja Työrivin tiedot -sivusta, joka sisältää kattavan, lajiteltavissa olevan luettelon sekä suodatettavissa olevan luettelon järjestelmäsi yksittäisistä työriveistä.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245103"
---
# <a name="work-line-details"></a><span data-ttu-id="57f26-103">Työrivin tiedot</span><span class="sxs-lookup"><span data-stu-id="57f26-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57f26-104">**Työrivin tiedot** -sivu sisältää kattavan, lajiteltavissa olevan luettelon sekä suodatettavissa olevan luettelon järjestelmäsi yksittäisistä työriveistä.</span><span class="sxs-lookup"><span data-stu-id="57f26-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="57f26-105">Se sisältää kattavan yhteenvedon työstä, jota suunnitellaan ja suoritetaan varastossa.</span><span class="sxs-lookup"><span data-stu-id="57f26-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="57f26-106">Voit helposti vaihtaa kaikkien työrivien tarkastelemisen ja vain avointen työrivien tarkastelemisen välillä.</span><span class="sxs-lookup"><span data-stu-id="57f26-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="57f26-107">Kunkin rivin tietoihin sisältyvät työn tila, nimiketunnus, sijainti, työmäärä, kuormituksen tunnus ja lähetystunnus.</span><span class="sxs-lookup"><span data-stu-id="57f26-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="57f26-108">Työrivin erittelytoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="57f26-108">Turn on the work line details feature</span></span>

<span data-ttu-id="57f26-109">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="57f26-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="57f26-110">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="57f26-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="57f26-111">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="57f26-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="57f26-112">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="57f26-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="57f26-113">**Ominaisuuden nimi:** *Työrivin tiedot*</span><span class="sxs-lookup"><span data-stu-id="57f26-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="57f26-114">Työrivin tiedot -sivun avaaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="57f26-114">Open and use the Work line details page</span></span>

<span data-ttu-id="57f26-115">Jos haluat tarkastella työrivin tietojen luetteloa, siirry kohtaan **Varastonhallinta \> Työ \> Työrivin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="57f26-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="57f26-116">Tässä voit myös tehdä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="57f26-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="57f26-117">**Suodatin**-kentän avulla voit etsiä rivejä, joilla on tietty arvo mille tahansa käytettävissä olevalle parametrille.</span><span class="sxs-lookup"><span data-stu-id="57f26-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="57f26-118">(Käytettävissä olevat parametrit sisältävät useita parametreja, joita ei näytetä ruudukon sarakkeina.)</span><span class="sxs-lookup"><span data-stu-id="57f26-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="57f26-119">**Näytä suljettu** -valintaruudun avulla voit näyttää tai piilottaa suljetut rivit.</span><span class="sxs-lookup"><span data-stu-id="57f26-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="57f26-120">Valitsemalla **Näytä dimensiot** voit avata **Dimensioiden näyttö** -valintaikkunan, jossa voit halutessasi näyttää tai piilottaa ruudukon eri dimensiosarakkeet.</span><span class="sxs-lookup"><span data-stu-id="57f26-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="57f26-121">Valitse mikä tahansa sarakeotsikko, jos haluat avata valikon, jossa voit lajitella tai suodattaa luettelon kyseisen sarakkeen arvojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="57f26-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="57f26-122">Valitse työrivi ja avaa sitten valintaikkuna, jossa voit muuttaa kyseisen työrivin sijaintia, valitsemalla **Vaihda sijainti**.</span><span class="sxs-lookup"><span data-stu-id="57f26-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="57f26-123">Määrittämäsi sijainti korvaa sijaintidirektiivin määritykset.</span><span class="sxs-lookup"><span data-stu-id="57f26-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="57f26-124">Valitse työrivi ja valitse sitten **Peruuta työrivi**, niin näyttöön tulee valintaikkuna, jossa voit vähentää kyseisen työrivin määrää osittain tai kokonaan.</span><span class="sxs-lookup"><span data-stu-id="57f26-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="57f26-125">Oikaise määrät.</span><span class="sxs-lookup"><span data-stu-id="57f26-125">Adjust quantities.</span></span>
- <span data-ttu-id="57f26-126">Näytä minkä tahansa työrivin takana olevat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="57f26-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="57f26-127">Kokeile toimintoa</span><span class="sxs-lookup"><span data-stu-id="57f26-127">Try out the feature</span></span>

<span data-ttu-id="57f26-128">Tässä osassa on kolmiosainen esittely, jossa kerrotaan, miten työrivin tietoja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="57f26-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="57f26-129">Ota mallitiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="57f26-129">Make sample data available</span></span>

<span data-ttu-id="57f26-130">Tämän demon käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="57f26-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="57f26-131">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="57f26-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="57f26-132">Voit hyödyntää tätä esittelyä myös ohjeena, kun työskentelet tuotantojärjestelmän parissa.</span><span class="sxs-lookup"><span data-stu-id="57f26-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="57f26-133">Sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.</span><span class="sxs-lookup"><span data-stu-id="57f26-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="57f26-134">Vahvista, että tilanteen määrittämiseen on riittävästi käytettävissä olevaa varastoa</span><span class="sxs-lookup"><span data-stu-id="57f26-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="57f26-135">Jos käytät **USMF**-esittelytietoja, sinun tulisi ensin varmistaa järjestelmäsi asetukset ja se, että kaikissa oleellisissa poimintasijanneissa on saatavilla tarpeeksi varastoa.</span><span class="sxs-lookup"><span data-stu-id="57f26-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="57f26-136">Tätä esittelyä varten seuraavan varastomäärän on oltava sinulla vapaana varastossa:</span><span class="sxs-lookup"><span data-stu-id="57f26-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="57f26-137">**Nimike M9200:** 45 kpl.</span><span class="sxs-lookup"><span data-stu-id="57f26-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="57f26-138">(tai enemmän)</span><span class="sxs-lookup"><span data-stu-id="57f26-138">(or more)</span></span>
- <span data-ttu-id="57f26-139">**Nimike M9202:** 10 kpl.</span><span class="sxs-lookup"><span data-stu-id="57f26-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="57f26-140">(tai enemmän)</span><span class="sxs-lookup"><span data-stu-id="57f26-140">(or more)</span></span>

<span data-ttu-id="57f26-141">Tarkista, että käytettävissä on riittävästi varastoa, ja tee tarvittavat oikaisut noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="57f26-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="57f26-142">Siirry kohtaan **Varaston hallinta \> Asetukset \> Sijaintidirektiivit** ja määritä, mitä poimintasijainteja käytetään myyntitilausten keräilyyn varastossa 51.</span><span class="sxs-lookup"><span data-stu-id="57f26-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="57f26-143">(Lisätietoja on kohdassa [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="57f26-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="57f26-144">Tarkista varastotasot asianmukaisissa sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="57f26-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="57f26-145">Oikaise varasto tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="57f26-145">Adjust inventory as required.</span></span> <span data-ttu-id="57f26-146">Voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai käyttää mitä tahansa muuta virtausta oikaistaksesi varastoa.</span><span class="sxs-lookup"><span data-stu-id="57f26-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="57f26-147">Osa 1: Luo poimintatyö</span><span class="sxs-lookup"><span data-stu-id="57f26-147">Part 1: Create picking work</span></span>

<span data-ttu-id="57f26-148">Ennen kuin aloitat töiden luomisen, varmista, että varastosi on määritetty vastaamaan työpyyntöihin odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="57f26-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="57f26-149">Seuraa seuraavia ohjeita luodaksesi poimintatyön.</span><span class="sxs-lookup"><span data-stu-id="57f26-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="57f26-150">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="57f26-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="57f26-151">Valitse **Uusi** ja avaa **Luo myyntitilaus**-valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="57f26-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="57f26-152">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="57f26-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="57f26-153">Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi _US-001_.</span><span class="sxs-lookup"><span data-stu-id="57f26-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="57f26-154">Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi _51_.</span><span class="sxs-lookup"><span data-stu-id="57f26-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="57f26-155">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="57f26-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="57f26-156">Uusi myyntitilauksesi avataan.</span><span class="sxs-lookup"><span data-stu-id="57f26-156">Your new sales order is opened.</span></span> <span data-ttu-id="57f26-157">**Myyntitilausrivit**-ruudukko sisältää uuden, tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="57f26-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="57f26-158">Määritä seuraavat arvot tällä tilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="57f26-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="57f26-159">**Nimiketunnus:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="57f26-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="57f26-160">**Määrä** _20_</span><span class="sxs-lookup"><span data-stu-id="57f26-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="57f26-161">**Yksikkö:** _ea_</span><span class="sxs-lookup"><span data-stu-id="57f26-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="57f26-162">Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus** avataksesi **Varaus**-sivun.</span><span class="sxs-lookup"><span data-stu-id="57f26-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="57f26-163">Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.</span><span class="sxs-lookup"><span data-stu-id="57f26-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="57f26-164">Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.</span><span class="sxs-lookup"><span data-stu-id="57f26-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="57f26-165">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="57f26-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="57f26-166">Järjestelmä luo lähetyksen, lisää sen uuteen kuormitukseen ja luo tarvittavat työt.</span><span class="sxs-lookup"><span data-stu-id="57f26-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="57f26-167">Luo toinen myyntitilaus samalle asiakastilille ja varastolle, jota käytettiin ensimmäisessä tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="57f26-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="57f26-168">Lisää seuraavat kaksi tilausriviä tälle tilaukselle:</span><span class="sxs-lookup"><span data-stu-id="57f26-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="57f26-169">**Rivi 1:** Aseta **Nimiketunnus**-kentän arvoksi _M9200_, **Määrä**-kentän arvoksi _25_ ja **Yksikkö**-kentän arvoksi _kpl_.</span><span class="sxs-lookup"><span data-stu-id="57f26-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="57f26-170">**Rivi 2:** Aseta **Nimiketunnus**-kentän arvoksi _M9202_, **Määrä**-kentän arvoksi _10_ ja **Yksikkö**-kentän arvoksi _kpl_.</span><span class="sxs-lookup"><span data-stu-id="57f26-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="57f26-171">Toista vaiheet 6-8, kun haluat varata varaston kullekin tilausriville (yksi kerrallaan) ja vapauttaa sitten tilauksen varastoon toistamalla vaiheen 9.</span><span class="sxs-lookup"><span data-stu-id="57f26-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="57f26-172">Osa 2: Työrivin sijainnin muuttaminen</span><span class="sxs-lookup"><span data-stu-id="57f26-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="57f26-173">Valitse **Varastonhallinta \> Työ \> Työrivin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="57f26-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="57f26-174">Etsi ja valitse jokin tälle demokohteelle luoduista työriveistä.</span><span class="sxs-lookup"><span data-stu-id="57f26-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="57f26-175">Avaa **Valitse uusi sijainti** -valintaikkuna valitsemalla **Vaihda sijainti**.</span><span class="sxs-lookup"><span data-stu-id="57f26-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="57f26-176">Valitse **Uuden sijainnin valitseminen** -valintaikkunan **Sijainti**-kentästä työriville uusi sijainti.</span><span class="sxs-lookup"><span data-stu-id="57f26-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="57f26-177">Ota muutokset käyttöön valitsemalla **OK** ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="57f26-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57f26-178">Voit lähettää sijainnin muutoksia vain, jos uudessa sijainnissa on riittävästi käytettävissä olevaa varastoa (poimintaa varten) tai jos se läpäisee sijaintityypin vahvistuksen (käyttöön).</span><span class="sxs-lookup"><span data-stu-id="57f26-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="57f26-179">Osa 3: Työrivin määrän muuttaminen tai työrivin peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="57f26-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="57f26-180">Valitse **Varastonhallinta \> Työ \> Työrivin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="57f26-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="57f26-181">Etsi ja valitse jokin tälle demokohteelle luoduista työriveistä.</span><span class="sxs-lookup"><span data-stu-id="57f26-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="57f26-182">Huomaa, että voit peruuttaa tai muuttaa määriä vain työriveille, joilla työtyyppi on _poiminta_.</span><span class="sxs-lookup"><span data-stu-id="57f26-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="57f26-183">Avaa **Peruutettava määrä** -valintaikkuna valitsemalla **Peruuta työrivi**.</span><span class="sxs-lookup"><span data-stu-id="57f26-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="57f26-184">Muuta **Peruutettava määrä** -valintaikkunassa **Määrä**-kentän arvoa ja määritä määrä, joka *vähennetään* riville määritettynä määränä.</span><span class="sxs-lookup"><span data-stu-id="57f26-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="57f26-185">Oletusarvon mukaan **Määrä**-kentässä näkyy koko määrä.</span><span class="sxs-lookup"><span data-stu-id="57f26-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="57f26-186">Jos peruutat koko määrän, **Työtilan** arvoksi tulee _peruutettu_, mutta **Työmäärä**-kentässä näkyy edelleen alkuperäinen arvo.</span><span class="sxs-lookup"><span data-stu-id="57f26-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="57f26-187">Jos peruutat vain osan määrästä, **Työmäärä**-kenttä päivitetään uuden arvon näyttämiseksi, mutta **työn tila** -arvo ei muutu.</span><span class="sxs-lookup"><span data-stu-id="57f26-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="57f26-188">Ota muutokset käyttöön valitsemalla **OK** ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="57f26-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57f26-189">Jos peruutat vain osan työrivin määrästä, myös vanhentunut määrä on poistettava kuormarivistä.</span><span class="sxs-lookup"><span data-stu-id="57f26-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="57f26-190">Muussa tapauksessa kuormariviä ei voi vahvistaa, ellei alitoimitus ole määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="57f26-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]