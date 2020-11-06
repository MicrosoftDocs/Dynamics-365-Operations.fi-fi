---
title: Toimipaikan rekisterikilpien paikannus
description: Toimipaikan rekisterikilpien paikannuksen avulla voit nähdä, missä rekisterikilpi sijaitsee monilavaisessa kokoonpanossa, kuten paikoissa, joissa käytetään syviä lavahyllyjä.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017113"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="f6446-103">Toimipaikan rekisterikilpien paikannus</span><span class="sxs-lookup"><span data-stu-id="f6446-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6446-104">Toimipaikan rekisterikilpien paikannuksen avulla voit nähdä, missä rekisterikilpi sijaitsee monilavaisessa kokoonpanossa, kuten paikoissa, joissa käytetään syviä lavahyllyjä.</span><span class="sxs-lookup"><span data-stu-id="f6446-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="f6446-105">Toiminto lisää järjestysnumeron kuhunkin varastointipaikkaan sijoitettavaan rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="f6446-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="f6446-106">Tämän järjestysnumeron avulla voidaan tilata varastointipaikkaan rekisterikilpiä.</span><span class="sxs-lookup"><span data-stu-id="f6446-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="f6446-107">Niinpä toiminto tukee älykkäästi tilanteita, joissa asiakkaan käyttävät painovoimaan perustuvaa hyllyjärjestelmää ja heidän on tavaroiden varastosta noutoa varten tiedettävä, mikä rekisterikilpi näkyy pakkauksen edestä päin.</span><span class="sxs-lookup"><span data-stu-id="f6446-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="f6446-108">Tässä aiheessa esitellään esimerkkitilanne tämän toiminnon määrittämisestä ja käytöstä.</span><span class="sxs-lookup"><span data-stu-id="f6446-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="f6446-109">Ota Toimipaikan rekisterikilpien paikannustoiminto käyttöön</span><span class="sxs-lookup"><span data-stu-id="f6446-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="f6446-110">Ennen kuin voit käyttää rekisterikilpien paikannusta, toiminnon pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="f6446-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="f6446-111">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="f6446-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f6446-112">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="f6446-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f6446-113">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="f6446-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f6446-114">**Toiminnon nimi:** *Toimipaikan rekisterikilpien paikannus*</span><span class="sxs-lookup"><span data-stu-id="f6446-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f6446-115">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="f6446-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="f6446-116">Ota mallitiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="f6446-116">Make sample data available</span></span>

<span data-ttu-id="f6446-117">Jos haluat käsitellä tätä skenaariota käyttämällä tässä ehdotettuja arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu mallitiedot.</span><span class="sxs-lookup"><span data-stu-id="f6446-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="f6446-118">Sinun on myös valittava **USMF** -yritys ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="f6446-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="f6446-119">Määritä toiminto tälle skenaariolle</span><span class="sxs-lookup"><span data-stu-id="f6446-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="f6446-120">Määritä *Toimipaikan rekisterikilpien paikannus* tässä aiheessa käsiteltävää skenaariota varten suorittamalla seuraavassa esitetyt toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="f6446-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="f6446-121">Sijaintiprofiilit</span><span class="sxs-lookup"><span data-stu-id="f6446-121">Location profiles</span></span>

<span data-ttu-id="f6446-122">Toiminto on otettava käyttöön kaikkien niiden toimipaikkojen sijaintiprofiileissa, joissa toimintoa käytetään.</span><span class="sxs-lookup"><span data-stu-id="f6446-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="f6446-123">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="f6446-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="f6446-124">Valitse vasemmassa ruudussa olevasta sijaintiprofiilien luettelosta **BULKKI-06**.</span><span class="sxs-lookup"><span data-stu-id="f6446-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="f6446-125">**Yleinen** -pikavälilehdessä näkyviin tulee kaksi uutta vaihtoehtoa toiminnon viereen.</span><span class="sxs-lookup"><span data-stu-id="f6446-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="f6446-126">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-126">Set the following values:</span></span>

    - <span data-ttu-id="f6446-127">**Ota rekisterikilven paikannus käyttöön:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="f6446-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="f6446-128">Kun tämä asetus on *Kyllä* , rekisterikilven sijainti pidetään samana kaikille toimipaikan rekisterikilville.</span><span class="sxs-lookup"><span data-stu-id="f6446-128">When this option is set to *Yes* , the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="f6446-129">**Näytä mobiililaitteen LP-asema:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="f6446-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="f6446-130">Kun tämä asetus on *Kyllä* , rekisterikilven sijainti näkyy mobiililaitteen käyttäjille kilven säädön ja laskennan aikana.</span><span class="sxs-lookup"><span data-stu-id="f6446-130">When this option is set to *Yes* , the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="f6446-131">Voit muuttaa tätä asetusta vain, kun toiminto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="f6446-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="f6446-132">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f6446-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="f6446-133">Sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="f6446-133">Location directives</span></span>

1. <span data-ttu-id="f6446-134">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="f6446-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f6446-135">Varmista, että vasemman ruudun **Työtilauksen tyyppi** -kentän arvo on *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="f6446-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="f6446-136">Valitse sijaintidirektiivien luettelosta **61 SO tilauksen kerääminen**.</span><span class="sxs-lookup"><span data-stu-id="f6446-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="f6446-137">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="f6446-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f6446-138">Valitse **Rivit** -pikavälilehdessä rivi, jonka **Järjestysluku** on *2*.</span><span class="sxs-lookup"><span data-stu-id="f6446-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="f6446-139">Valitse **Sijaintidirektiivin toiminnot** -pikavälilehdessä rivi, jonka **Nimi** -arvo on *Keräys, kun < kuormalava* (tämän pitäisi olla ainoa rivi), ja muuta sen **Järjestysnumeron** arvoksi *2*.</span><span class="sxs-lookup"><span data-stu-id="f6446-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="f6446-140">Lisää uusi sijaintidirektiivin toiminto valitsemalla yllä olevassa ruudukossa kohta **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f6446-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="f6446-141">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f6446-142">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="f6446-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="f6446-143">**Nimi:** *Keräilysijainti 1*</span><span class="sxs-lookup"><span data-stu-id="f6446-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="f6446-144">Kun uusi rivi on vielä valittuna, valitse ruudukon yläpuolelle **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="f6446-145">Valitse **Liitokset** -väli lehti kyselyeditorissa.</span><span class="sxs-lookup"><span data-stu-id="f6446-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="f6446-146">Laajenna **Toimipaikat** -taulun liitos niin, että se tuo näkyviin **Varaston dimensiot** -taulun liitokset.</span><span class="sxs-lookup"><span data-stu-id="f6446-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="f6446-147">Laajenna **Varaston dimensiot** -taulun liitos niin, että se tuo näkyviin **Käytettävissä oleva varasto** -taulun liitokset.</span><span class="sxs-lookup"><span data-stu-id="f6446-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="f6446-148">Valitse **Varaston dimensiot** ja valitse sitten **Lisää taulun liitos**.</span><span class="sxs-lookup"><span data-stu-id="f6446-148">Select **Inventory dimensions** , and then select **Add table join**.</span></span>
1. <span data-ttu-id="f6446-149">Valitse näyttöön tulevan taululuettelon **Suhde** -sarakkeesta **Rekisterikilpi (Rekisterikilpi)**.</span><span class="sxs-lookup"><span data-stu-id="f6446-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="f6446-150">Lisää sitten kohta **Rekisterikilpi** taulukon **Varaston dimensiot** liitokseen valitsemalla **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="f6446-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="f6446-151">Kun **Rekisterikilpi** on valittuna, valitse **Lisää taulun liitos**.</span><span class="sxs-lookup"><span data-stu-id="f6446-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="f6446-152">Valitse näyttöön tulevan taululuettelon **Suhde** -sarakkeesta **Toimipaikan rekisterikilpien paikannus (Rekisterikilpi)**.</span><span class="sxs-lookup"><span data-stu-id="f6446-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="f6446-153">Lisää sitten kohta **Toimipaikan rekisterikilpien paikannus** taulukon **Varaston dimensiot** liitokseen valitsemalla **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="f6446-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="f6446-154">![Taulun liitokset](media/LpTableJoin.png "Taulun liitokset")</span><span class="sxs-lookup"><span data-stu-id="f6446-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="f6446-155">Vahvista päivitetyt liitetyt taulut valitsemalla **OK** ja sulje kyselyeditori.</span><span class="sxs-lookup"><span data-stu-id="f6446-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="f6446-156">Avaa kyselyeditori uudelleen valitsemalla **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="f6446-157">Valitse **Alue** -välilehdessä **Lisää** , jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="f6446-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f6446-158">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f6446-159">**Taulukko:** *Toimipaikan rekisterikilpien paikannus*</span><span class="sxs-lookup"><span data-stu-id="f6446-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="f6446-160">**Johdettu taulukko:** *Toimipaikan rekisterikilpien paikannus*</span><span class="sxs-lookup"><span data-stu-id="f6446-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="f6446-161">**Kenttä:** *LP-sijainti*</span><span class="sxs-lookup"><span data-stu-id="f6446-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="f6446-162">**Ehdot:** *1*</span><span class="sxs-lookup"><span data-stu-id="f6446-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="f6446-163">![Uusi alue](media/LpPositionCriteria.png "Uusi alue")</span><span class="sxs-lookup"><span data-stu-id="f6446-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="f6446-164">Vahvista muutokset valitsemalla **OK** ja sulje kyselyeditori.</span><span class="sxs-lookup"><span data-stu-id="f6446-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="f6446-165">Mallitietojen määrittäminen tälle skenaariolle</span><span class="sxs-lookup"><span data-stu-id="f6446-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="f6446-166">Tässä skenaariossa käyttäjän on kirjauduttava varastoinnin mobiilisovellukseen työntekijänä, joka on määritetty työskentelemään varastolla *61*.</span><span class="sxs-lookup"><span data-stu-id="f6446-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="f6446-167">Myös käyttäjän on suoritettava tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f6446-167">The user must also complete transactions.</span></span>

<span data-ttu-id="f6446-168">Koska *Toimipaikan rekisterikilven paikannus* -toiminto lisää uuden tunnisteen rekisterikilpien paikoille toimipaikoissa, sinun on ensin luotava joitakin tietoja skenaarion tueksi.</span><span class="sxs-lookup"><span data-stu-id="f6446-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="f6446-169">Ensimmäisen sijainnin pisteinventointi</span><span class="sxs-lookup"><span data-stu-id="f6446-169">Spot-count the first location</span></span>

1. <span data-ttu-id="f6446-170">Avaa in varastointisovellus ja kirjaudu siihen varastossa *61*.</span><span class="sxs-lookup"><span data-stu-id="f6446-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="f6446-171">Siirry kohtaan **Varasto \>Pisteinventointi**.</span><span class="sxs-lookup"><span data-stu-id="f6446-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="f6446-172">Aseta **Pisteinventointi** -sivulla kentän **Sijainti** arvoksi *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="f6446-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="f6446-173">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-173">Select **OK**.</span></span>

    <span data-ttu-id="f6446-174">Sivulla näkyy antamasi sijainti.</span><span class="sxs-lookup"><span data-stu-id="f6446-174">The page shows the location that you entered.</span></span> <span data-ttu-id="f6446-175">Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"</span><span class="sxs-lookup"><span data-stu-id="f6446-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f6446-176">Lisää luku sijaintiin valitsemalla **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="f6446-177">Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **Nimike** -kenttä ja kirjoita siihen arvo *A0001*.</span><span class="sxs-lookup"><span data-stu-id="f6446-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="f6446-178">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-178">Select **OK**.</span></span>
1. <span data-ttu-id="f6446-179">Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **LP** -kenttä ja kirjoita siihen arvo *LP1001* (tai mikä tahansa muu haluamasi rekisterinumero).</span><span class="sxs-lookup"><span data-stu-id="f6446-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="f6446-180">**Syklin laskenta: Lisää uusi LP tai nimike** -sivulla näkyy **Rekisterikilven sijainti 1**.</span><span class="sxs-lookup"><span data-stu-id="f6446-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="f6446-181">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-181">Select **OK**.</span></span>

    <span data-ttu-id="f6446-182">Sinun on nyt asetettava rekisterikilvessä mainittujen nimikkeiden lukumäärä.</span><span class="sxs-lookup"><span data-stu-id="f6446-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="f6446-183">Aseta **Määrä** -kentän arvoksi *10*.</span><span class="sxs-lookup"><span data-stu-id="f6446-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="f6446-184">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-184">Select **OK**.</span></span>

    <span data-ttu-id="f6446-185">Sivulla näkyy antamasi sijainti.</span><span class="sxs-lookup"><span data-stu-id="f6446-185">The page shows the location that you entered.</span></span> <span data-ttu-id="f6446-186">Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"</span><span class="sxs-lookup"><span data-stu-id="f6446-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f6446-187">Lisää toinen luku sijaintiin valitsemalla **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="f6446-188">Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **Nimike** -kenttä ja kirjoita siihen arvo *A0002*.</span><span class="sxs-lookup"><span data-stu-id="f6446-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="f6446-189">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-189">Select **OK**.</span></span>
1. <span data-ttu-id="f6446-190">Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **LP** -kenttä ja kirjoita sitten arvo *LP1002* (tai mikä tahansa muu haluamasi rekisterinumero, joka eroaa aiemmin määrittämästäsi rekisterinumerosta).</span><span class="sxs-lookup"><span data-stu-id="f6446-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="f6446-191">Muuta rekisterikilven paikkaa asettamalla **LP-sijainti** -kentän arvoksi *2*.</span><span class="sxs-lookup"><span data-stu-id="f6446-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="f6446-192">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-192">Select **OK**.</span></span>
1. <span data-ttu-id="f6446-193">Määritä rekisterikilvessä mainittujen nimikkeiden lukumäärä asettamalla **Määrä** -kentän arvoksi *10*.</span><span class="sxs-lookup"><span data-stu-id="f6446-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="f6446-194">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-194">Select **OK**.</span></span>

    <span data-ttu-id="f6446-195">Sivulla näkyy antamasi sijainti.</span><span class="sxs-lookup"><span data-stu-id="f6446-195">The page shows the location that you entered.</span></span> <span data-ttu-id="f6446-196">Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"</span><span class="sxs-lookup"><span data-stu-id="f6446-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f6446-197">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-197">Select **OK**.</span></span>

<span data-ttu-id="f6446-198">Työ on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="f6446-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="f6446-199">Toisen sijainnin pisteinventointi</span><span class="sxs-lookup"><span data-stu-id="f6446-199">Spot-count the second location</span></span>

1. <span data-ttu-id="f6446-200">Aseta **Pisteinventointi** -sivulla kentän **Sijainti** arvoksi *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="f6446-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="f6446-201">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-201">Select **OK**.</span></span>

    <span data-ttu-id="f6446-202">Sivulla näkyy antamasi sijainti.</span><span class="sxs-lookup"><span data-stu-id="f6446-202">The page shows the location that you entered.</span></span> <span data-ttu-id="f6446-203">Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"</span><span class="sxs-lookup"><span data-stu-id="f6446-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f6446-204">Lisää luku sijaintiin valitsemalla **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="f6446-205">Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **Nimike** -kenttä ja kirjoita siihen arvo *A0002*.</span><span class="sxs-lookup"><span data-stu-id="f6446-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="f6446-206">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-206">Select **OK**.</span></span>
1. <span data-ttu-id="f6446-207">Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **LP** -kenttä ja kirjoita sitten arvo *LP1003* (tai mikä tahansa muu haluamasi rekisterinumero, joka eroaa aiemmassa toimenpiteessä määrittämistäsi rekisterinumeroista).</span><span class="sxs-lookup"><span data-stu-id="f6446-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="f6446-208">**Syklin laskenta: Lisää uusi LP tai nimike** -sivulla näkyy **Rekisterikilven sijainti 1**.</span><span class="sxs-lookup"><span data-stu-id="f6446-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="f6446-209">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-209">Select **OK**.</span></span>
1. <span data-ttu-id="f6446-210">Määritä rekisterikilvessä mainittujen nimikkeiden lukumäärä asettamalla **Määrä** -kentän arvoksi *10*.</span><span class="sxs-lookup"><span data-stu-id="f6446-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="f6446-211">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-211">Select **OK**.</span></span>

    <span data-ttu-id="f6446-212">Sivulla näkyy antamasi sijainti.</span><span class="sxs-lookup"><span data-stu-id="f6446-212">The page shows the location that you entered.</span></span> <span data-ttu-id="f6446-213">Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"</span><span class="sxs-lookup"><span data-stu-id="f6446-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="f6446-214">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-214">Select **OK**.</span></span>

<span data-ttu-id="f6446-215">Työ on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="f6446-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="f6446-216">Työn tiedot</span><span class="sxs-lookup"><span data-stu-id="f6446-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="f6446-217">Mobiilisovelluksen pisteinventoinnit luovat inventoinnin arvoksi Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f6446-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="f6446-218">Työ edellyttää, että inventoinnit hyväksytään, ennen kuin ne kirjataan varastoon.</span><span class="sxs-lookup"><span data-stu-id="f6446-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="f6446-219">Kirjaudu sisään Dynamics 365 Supply Chain Management -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="f6446-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="f6446-220">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f6446-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="f6446-221">Etsi **Yleiskatsaus** -välilehdestä rivit, joilla on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="f6446-222">**Työtilauksen tyyppi:** *Inventointi*</span><span class="sxs-lookup"><span data-stu-id="f6446-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="f6446-223">**Varasto** : *61*</span><span class="sxs-lookup"><span data-stu-id="f6446-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f6446-224">**Työn tila:** *Odottaa arvostelua*</span><span class="sxs-lookup"><span data-stu-id="f6446-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="f6446-225">Näille riveille pitäisi olla luotuna kaksi työtunnusta.</span><span class="sxs-lookup"><span data-stu-id="f6446-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="f6446-226">Näiden molempien työtunnusten määrät on hyväksyttävä.</span><span class="sxs-lookup"><span data-stu-id="f6446-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="f6446-227">Valitse ruudukossa ensimmäinen työtunnus *Inventointi* -työtilauksen tyypiksi.</span><span class="sxs-lookup"><span data-stu-id="f6446-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="f6446-228">Valitse toimintoruudun **Työ** -välilehden **Työ** -ryhmässä **Inventointi**.</span><span class="sxs-lookup"><span data-stu-id="f6446-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="f6446-229">Näkyviin tulee kaksi riviä, yksi kullekin nimikkeelle ja rekisterikilvelle.</span><span class="sxs-lookup"><span data-stu-id="f6446-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="f6446-230">**Inventoitu määrä** -, **Toimipiste** -, **Rekisterikilpi** - ja **Nimike** -kenttien arvojen on vastattava mobiililaitteella luotuja arvoja.</span><span class="sxs-lookup"><span data-stu-id="f6446-230">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="f6446-231">Jos jokin näistä kentistä ei ole näkyvissä, lisää ne ruudukkoon valitsemalla toimintoruudussa **Näytä dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="f6446-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="f6446-232">Valitse molemmat rivit.</span><span class="sxs-lookup"><span data-stu-id="f6446-232">Select both lines.</span></span>
1. <span data-ttu-id="f6446-233">Valitse toimintoruudussa **Hyväksy määrä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="f6446-234">Näyttöön tulee viesti "Lähetetään – kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="f6446-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="f6446-235">Voit tarkastella kirjattua kirjauskansion numeroa valitsemalla **Viestin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f6446-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="f6446-236">Sulje viestin tiedot.</span><span class="sxs-lookup"><span data-stu-id="f6446-236">Close the message details.</span></span>
1. <span data-ttu-id="f6446-237">Päivitä **Työ** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f6446-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="f6446-238">Ensimmäinen työtunnus on suljettu, eikä se enää näy.</span><span class="sxs-lookup"><span data-stu-id="f6446-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="f6446-239">Jos haluat tarkastella suljettua työtä, valitse ruudukon yläpuolella oleva **Näytä suljetut** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f6446-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="f6446-240">Voit nyt hyväksyä työn rekisterikilvelle toimipaikassa *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="f6446-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="f6446-241">Valitse **Yleiskatsaus** -välilehdessä toinen työtunnus *Inventointi* -työtilauksen tyypiksi.</span><span class="sxs-lookup"><span data-stu-id="f6446-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="f6446-242">Valitse toimintoruudun **Työ** -välilehden **Työ** -ryhmässä **Inventointi**.</span><span class="sxs-lookup"><span data-stu-id="f6446-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="f6446-243">Näkyviin tulee yksi rivi, jossa on nimike ja rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="f6446-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="f6446-244">**Inventoitu määrä** -, **Toimipiste** -, **Rekisterikilpi** - ja **Nimike** -kenttien arvojen on vastattava mobiililaitteella luotuja arvoja.</span><span class="sxs-lookup"><span data-stu-id="f6446-244">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="f6446-245">Valitse rivi.</span><span class="sxs-lookup"><span data-stu-id="f6446-245">Select the line.</span></span>
1. <span data-ttu-id="f6446-246">Valitse toimintoruudussa **Hyväksy määrä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="f6446-247">Näyttöön tulee viesti "Lähetetään – kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="f6446-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="f6446-248">Voit tarkastella kirjattua kirjauskansion numeroa valitsemalla **Viestin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f6446-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="f6446-249">Sulje viestin tiedot.</span><span class="sxs-lookup"><span data-stu-id="f6446-249">Close the message details.</span></span>
1. <span data-ttu-id="f6446-250">Päivitä **Työ** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f6446-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="f6446-251">Toinen työtunnus on suljettu, eikä se enää näy.</span><span class="sxs-lookup"><span data-stu-id="f6446-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="f6446-252">Jos haluat tarkastella suljettua työtä, valitse ruudukon yläpuolella oleva **Näytä suljetut** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f6446-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="f6446-253">Varastosaldo sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="f6446-253">On-hand by location</span></span>

1. <span data-ttu-id="f6446-254">Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Varastosaldo sijainnin mukaan**.</span><span class="sxs-lookup"><span data-stu-id="f6446-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="f6446-255">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-255">Set the following values:</span></span>

    - <span data-ttu-id="f6446-256">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="f6446-256">**Site:** *6*</span></span>
    - <span data-ttu-id="f6446-257">**Varasto** : *61*</span><span class="sxs-lookup"><span data-stu-id="f6446-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f6446-258">**Päivitä kaikissa sijainneissa:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="f6446-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="f6446-259">Huomaa, että toimipaikassa *01A01R1S1B* on käytössä kaksi rekisterikilpeä:</span><span class="sxs-lookup"><span data-stu-id="f6446-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="f6446-260">**A0001** , jossa **LP-sijainti** -kentän arvo on *1*</span><span class="sxs-lookup"><span data-stu-id="f6446-260">**A0001** , where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="f6446-261">**A0002** , jossa **LP-sijainti** -kentän arvo on *2*</span><span class="sxs-lookup"><span data-stu-id="f6446-261">**A0002** , where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="f6446-262">Huomaa, että toimipaikassa *01A01R1S2B* on käytössä yksi rekisterikilpi:</span><span class="sxs-lookup"><span data-stu-id="f6446-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="f6446-263">**A0002** , jossa **LP-sijainti** -kentän arvo on *1*</span><span class="sxs-lookup"><span data-stu-id="f6446-263">**A0002** , where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="f6446-264">Myyntitilausskenaario</span><span class="sxs-lookup"><span data-stu-id="f6446-264">Sales order scenario</span></span>

<span data-ttu-id="f6446-265">Kun *Toimipaikan rekisterikilven paikannus* -toiminto on määritetty ja varasto on vaiheistettu, luo myyntitilaus, joka luo keräilytyön, jossa varastotyöntekijä kerää nimikkeen *A0002* varastopaikasta, jossa kuormalavan tunnus on paikassa *1*.</span><span class="sxs-lookup"><span data-stu-id="f6446-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="f6446-266">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="f6446-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f6446-267">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f6446-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f6446-268">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f6446-269">**Asiakastili:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="f6446-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="f6446-270">**Varasto** : *61*</span><span class="sxs-lookup"><span data-stu-id="f6446-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="f6446-271">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6446-271">Select **OK**.</span></span>
1. <span data-ttu-id="f6446-272">**Myyntitilausrivit** -pikavälilehden ruudukkoon lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="f6446-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f6446-273">Määritä tälle uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f6446-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="f6446-274">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f6446-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="f6446-275">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="f6446-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="f6446-276">Valitse ruudukon yläpuolella olevasta **Varasto** -valikosta kohta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="f6446-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f6446-277">Varaa varastossa olevat nimikkeet tilausriviä varten **Varaus** -sivun toimintoruudussa valitsemalla **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="f6446-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="f6446-278">Sulje **Varaus** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f6446-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="f6446-279">Valitse toimintoruudussa **Varasto** -välilehden **Toiminnot** -ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="f6446-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f6446-280">Näyttöön tulee tiedote, jossa kerrotaan, että tilaukselle on luotu aallon tunnus ja lähetystunnus.</span><span class="sxs-lookup"><span data-stu-id="f6446-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="f6446-281">Valitse **Myyntitilausrivit** -pikavälilehden ruudukon yläpuolella olevasta **Varasto** -valikosta **Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="f6446-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="f6446-282">Näkyviin tulee **Työ** -sivu, jossa näkyy myyntiriville luotu työ.</span><span class="sxs-lookup"><span data-stu-id="f6446-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="f6446-283">Kirjoita näytössä näkyvä työn tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="f6446-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="f6446-284">Myynnin keräilyskenaario</span><span class="sxs-lookup"><span data-stu-id="f6446-284">Sales picking scenario</span></span>

1. <span data-ttu-id="f6446-285">Avaa mobiilisovellus ja varastoon *61*.</span><span class="sxs-lookup"><span data-stu-id="f6446-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="f6446-286">Siirry kohtaan **Lähtevän \>myynnin keräys**.</span><span class="sxs-lookup"><span data-stu-id="f6446-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="f6446-287">Valitse **Skannaa työn tunnus/rekisterikilven tunnus** sivulla **Tunnus** -kenttä ja kirjoita siihen työn tunnus myyntiriviltä.</span><span class="sxs-lookup"><span data-stu-id="f6446-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="f6446-288">Huomaa, että keräystyö ohjaa sinut keräämään nimikkeen *A0002* toimipaikasta *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="f6446-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="f6446-289">Tämä ohje tulee näyttöön, koska nimike *A0002* on kirjattu rekisterikilpeen, joka on tämän toimipaikan sijainnissa *1*.</span><span class="sxs-lookup"><span data-stu-id="f6446-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="f6446-290">![Sijainti 1 toimipaikassa](media/LocationLicensePlatePositioning.png "Sijainti 1 toimipaikassa")</span><span class="sxs-lookup"><span data-stu-id="f6446-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="f6446-291">Kirjoita toimipaikalle luomasi rekisterikilven tunnus ja kerää myyntitilaus noudattamalla kehotteita.</span><span class="sxs-lookup"><span data-stu-id="f6446-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
