---
title: Klusterisijainti täynnä
description: Tässä ohjeaiheessa on tietoja Klusterisijainti täynnä -ominaisuudesta. Tämä ominaisuus on vaihtoehto tiukalle työkatkosääntöjen valvonnalle, kun käytössä on klusterikeräily. Tämä johtuu siitä, että ominaisuus mahdollistaa konttien ja kassien tilavuusrajoitteiden aiempaa suuremman virhemarginaalin.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ad0f8e2fa6b3767c6b5d5549a36d52990f871531
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808843"
---
# <a name="cluster-position-full"></a><span data-ttu-id="cfb22-104">Klusterisijainti täynnä</span><span class="sxs-lookup"><span data-stu-id="cfb22-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfb22-105">*Klusterisijainti täynnä* -ominaisuus on vaihtoehto tiukalle työkatkosääntöjen valvonnalle, kun käytössä on klusterikeräily. Tämä johtuu siitä, että ominaisuus mahdollistaa konttien ja kassien tilavuusrajoitteiden aiempaa suuremman virhemarginaalin.</span><span class="sxs-lookup"><span data-stu-id="cfb22-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="cfb22-106">Yleissä skenaariossa kaikki työtilauksen nimikkeet eivät mahdu valittuun konttiin.</span><span class="sxs-lookup"><span data-stu-id="cfb22-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="cfb22-107">Klusterikeräilyä suorittavilla varastotyöntekijöillä on muutama vaihtoehto tässä skenaariossa. He voivat muuttaa suuremman kontin kokoa tai kehittää esimehen kanssa toisenlaisen ratkaisun.</span><span class="sxs-lookup"><span data-stu-id="cfb22-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="cfb22-108">Tämä ominaisuus sisältää mahdollisuuden käyttää **Täysi**-painiketta klusterin yhdessä työyksikössä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="cfb22-109">Vanhemmissa versioissa tämä vaihtoehto oli käytettävissä vain tavallisissa tilauskeräilyssä, ei klusterikeräilyssä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="cfb22-110">Tämä ominaisuus eroaa kuitenkin normaalista **Täysi**-painikkeesta siten, että se peruuttaa jäljellä olevan työn.</span><span class="sxs-lookup"><span data-stu-id="cfb22-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="cfb22-111">Se ei ehdota käyttäjälle toisen lokeron lisäämistä samaan klusteriin eikä luo automaattisesti uutta työtä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="cfb22-112">Klusterisijainti täynnä -ominaisuuden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="cfb22-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="cfb22-113">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="cfb22-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="cfb22-114">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="cfb22-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="cfb22-115">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="cfb22-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="cfb22-116">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="cfb22-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="cfb22-117">**Ominaisuuden nimi:** *Klusterisijainti täynnä*</span><span class="sxs-lookup"><span data-stu-id="cfb22-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="cfb22-118">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="cfb22-118">Setup</span></span>

<span data-ttu-id="cfb22-119">Tässä osassa on ohjeita *Klusterisijainti täynnä* -ominaisuuden määrittämiseksi ja käyttämiseksi sekä ominaisuuden esimerkki.</span><span class="sxs-lookup"><span data-stu-id="cfb22-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="cfb22-120">Ota mallitiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="cfb22-120">Make sample data available</span></span>

<span data-ttu-id="cfb22-121">[Esimerkkiskenaarion](#example-scenario) käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon [vakiodemotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="cfb22-122">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="cfb22-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="cfb22-123">Voit hyödyntää esimerkkiskenaariota myös ohjeena, kun käytät tätä ominaisuutta tuotantojärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="cfb22-124">Siinä tapauksessa tässä kuvattujen asetusten omat arvot on korvattava.</span><span class="sxs-lookup"><span data-stu-id="cfb22-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="cfb22-125">Klusteriprofiilit</span><span class="sxs-lookup"><span data-stu-id="cfb22-125">Cluster profiles</span></span>

<span data-ttu-id="cfb22-126">Määritä, milloin klustereiden tunnukset luodaan automaattisesti, miten monta sijaintia käytetään, milloin klusterit rikotaan ja miten keräilytyö järjestetään ja tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="cfb22-127">Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Klusteriprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="cfb22-128">Valitse luetteloruudusta **Luo klusteri** -tietue.</span><span class="sxs-lookup"><span data-stu-id="cfb22-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="cfb22-129">Tarkista **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cfb22-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="cfb22-130">**Luo klusterin tunnus:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="cfb22-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="cfb22-131">**Aktivoi sijainnit:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="cfb22-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="cfb22-132">**Sijaintien määrä:** *2*</span><span class="sxs-lookup"><span data-stu-id="cfb22-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="cfb22-133">**Sijainnin nimi:** *Numeerinen*</span><span class="sxs-lookup"><span data-stu-id="cfb22-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="cfb22-134">**Hajota klusteri:** *Hyllytys*</span><span class="sxs-lookup"><span data-stu-id="cfb22-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="cfb22-135">**Lajittelun tarkistuksen tyyppi:** *Sijainnin tarkistus*</span><span class="sxs-lookup"><span data-stu-id="cfb22-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="cfb22-136">**Klusterin lajittelu** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="cfb22-137">Ruudukon on oltava tyhjä (se ei saa sisältää rivejä).</span><span class="sxs-lookup"><span data-stu-id="cfb22-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="cfb22-138">Työmallit</span><span class="sxs-lookup"><span data-stu-id="cfb22-138">Work templates</span></span>

<span data-ttu-id="cfb22-139">Määritä, miten keräilytyö luodaan klusterin keräilyä varten.</span><span class="sxs-lookup"><span data-stu-id="cfb22-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="cfb22-140">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="cfb22-141">Määritä sivun yläosassa **Työtilauksen tyyppi** -kentän arvoksi *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="cfb22-142">Varmista, että seuraavat esittelytietojen työmallit on luetteloitu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="cfb22-143">Jos ne eivät ole käytettävissä, et voi suorittaa skenaariota loppuun.</span><span class="sxs-lookup"><span data-stu-id="cfb22-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="cfb22-144">61 MT:n vaihe</span><span class="sxs-lookup"><span data-stu-id="cfb22-144">61 SO Stage</span></span>
    - <span data-ttu-id="cfb22-145">61 MT:n klusterin keräily</span><span class="sxs-lookup"><span data-stu-id="cfb22-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="cfb22-146">Sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="cfb22-146">Location directives</span></span>

<span data-ttu-id="cfb22-147">Sinun on määritettävä, mistä nimikkeet kerätään ja mihin ne sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="cfb22-148">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="cfb22-149">Määritä luettelon otsikossa **Työtilaustyyppi**-kentän arvoksi *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="cfb22-150">Varmista, että seuraavat esittelytietojen myyntitilausdirektiivit on luetteloitu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="cfb22-151">Jos ne eivät ole käytettävissä, et voi suorittaa skenaariota loppuun.</span><span class="sxs-lookup"><span data-stu-id="cfb22-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="cfb22-152">61 Klusterin keräily</span><span class="sxs-lookup"><span data-stu-id="cfb22-152">61 Cluster pick</span></span>
    - <span data-ttu-id="cfb22-153">61 MT:n keräilyjärjestys</span><span class="sxs-lookup"><span data-stu-id="cfb22-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="cfb22-154">Mobiililaitteen valikkovaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="cfb22-154">Mobile device menu items</span></span>

<span data-ttu-id="cfb22-155">Määritä mobiililaitteen valikkovaihtoehto käyttämään klusterikeräilyn ohjaamaa työtä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="cfb22-156">Klusterikeräilyn mobiililaitteen valikon vaihtoehdon **Salli työn jakaminen** -parametri on otettava käyttöön ja *Myyntitilauksen keräily* -työluokka on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="cfb22-157">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cfb22-158">Valitse luetteloruudusta **Klusterikeräilyn luominen** -tietue.</span><span class="sxs-lookup"><span data-stu-id="cfb22-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="cfb22-159">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="cfb22-160">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cfb22-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="cfb22-161">**Ohjaaja:** *Klusterikeräily*</span><span class="sxs-lookup"><span data-stu-id="cfb22-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="cfb22-162">**Luo rekisterikilpi:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="cfb22-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="cfb22-163">**Salli työn jakaminen:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="cfb22-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="cfb22-164">**Klusteriprofiilin tunnus:** *Luo klusteri*</span><span class="sxs-lookup"><span data-stu-id="cfb22-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="cfb22-165">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="cfb22-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="cfb22-166">Lisää **Työluokat**-pikavälilehdessä seuraavat kaksi riviä tarvittaessa:</span><span class="sxs-lookup"><span data-stu-id="cfb22-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="cfb22-167">Rivi 1 (yleensä ovat esittelytiedoissa):</span><span class="sxs-lookup"><span data-stu-id="cfb22-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="cfb22-168">**Työluokan tunnus:** *Myynti*</span><span class="sxs-lookup"><span data-stu-id="cfb22-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="cfb22-169">**Työtilauksen tyyppi:** *Myyntitilaukset*</span><span class="sxs-lookup"><span data-stu-id="cfb22-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="cfb22-170">Rivi 2 (todennäköisesti eivät ole esittelytiedoissa):</span><span class="sxs-lookup"><span data-stu-id="cfb22-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="cfb22-171">**Työluokan tunnus:** *Myyntitilauksen keräily*</span><span class="sxs-lookup"><span data-stu-id="cfb22-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="cfb22-172">**Työtilauksen tyyppi:** *Myyntitilaukset*</span><span class="sxs-lookup"><span data-stu-id="cfb22-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="cfb22-173">Siirry toimintoruudun **Työn vahvistusasetukset** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="cfb22-174">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-174">Select **Edit**.</span></span>
1. <span data-ttu-id="cfb22-175">Anna ruudukon riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="cfb22-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="cfb22-176">**Työtyyppi** - *Keräily*</span><span class="sxs-lookup"><span data-stu-id="cfb22-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="cfb22-177">**Tuotteen vahvistus** - *Valitse valintaruutu*</span><span class="sxs-lookup"><span data-stu-id="cfb22-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="cfb22-178">Valitse toimintoruudussa **Tallenna** ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="cfb22-179">Luo keräystyö</span><span class="sxs-lookup"><span data-stu-id="cfb22-179">Create picking work</span></span>

<span data-ttu-id="cfb22-180">Ennen kuin voit aloittaa klusterikeräilyn, sinun on luotava lähtevä työ.</span><span class="sxs-lookup"><span data-stu-id="cfb22-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="cfb22-181">Aiemmin luomasi klusteriprofiili määrittää kaksi klusteripositiota.</span><span class="sxs-lookup"><span data-stu-id="cfb22-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="cfb22-182">Näin ollen myyntitilauksen keräilylle on luotava vähintään kaksi työtunnusta.</span><span class="sxs-lookup"><span data-stu-id="cfb22-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="cfb22-183">Tämän skenaarion tapahtumat ovat varastossa *61* ja tapahtumissa käytetään nimikkeitä *L0101* ja *T0100*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="cfb22-184">Esittelytiedoissa on oltava riittävästi käytettävissä olevaa varastoa näille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="cfb22-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="cfb22-185">Varmista, että sinulla on riittävästi varastoa tapahtumien suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="cfb22-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="cfb22-186">Luo myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="cfb22-186">Create sales order 1</span></span>

1. <span data-ttu-id="cfb22-187">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="cfb22-188">Luo myyntitilaus 1 valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="cfb22-189">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cfb22-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cfb22-190">**Asiakastili:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="cfb22-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="cfb22-191">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="cfb22-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="cfb22-192">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-192">Select **OK**.</span></span>
1. <span data-ttu-id="cfb22-193">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-193">The new sales order is opened.</span></span> <span data-ttu-id="cfb22-194">Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="cfb22-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="cfb22-195">**Nimiketunnus:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="cfb22-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="cfb22-196">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="cfb22-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="cfb22-197">Anna **Toimitus**-välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="cfb22-198">Lisää **Myyntitilausrivit**-pikavälilehdessä toinen rivi, jonka asetukset ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="cfb22-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="cfb22-199">**Nimiketunnus:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="cfb22-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="cfb22-200">**Määrä** *20*</span><span class="sxs-lookup"><span data-stu-id="cfb22-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="cfb22-201">Anna **Toimitus**-välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="cfb22-202">Varaa varastoa jokaiselle lisätylle riville seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="cfb22-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="cfb22-203">Valitse varattava rivi.</span><span class="sxs-lookup"><span data-stu-id="cfb22-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="cfb22-204">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="cfb22-205">Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="cfb22-206">Sulje **Varaus**-sivu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="cfb22-207">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="cfb22-208">Kun vapautus on tehty, näkyviin tulee tietosanomia, jotka sisältävät luodun aallon ja luodut kuormatunnukset.</span><span class="sxs-lookup"><span data-stu-id="cfb22-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="cfb22-209">Luo myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="cfb22-209">Create sales order 2</span></span>

1. <span data-ttu-id="cfb22-210">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="cfb22-211">Luo myyntitilaus 2 valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="cfb22-212">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="cfb22-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cfb22-213">**Asiakastili:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="cfb22-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="cfb22-214">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="cfb22-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="cfb22-215">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-215">Select **OK**.</span></span>
1. <span data-ttu-id="cfb22-216">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-216">The new sales order is opened.</span></span> <span data-ttu-id="cfb22-217">Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="cfb22-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="cfb22-218">**Nimiketunnus:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="cfb22-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="cfb22-219">**Määrä** *20*</span><span class="sxs-lookup"><span data-stu-id="cfb22-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="cfb22-220">Anna **Toimitus**-välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="cfb22-221">Lisää **Myyntitilausrivit**-pikavälilehdessä toinen rivi, jonka asetukset ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="cfb22-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="cfb22-222">**Nimiketunnus:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="cfb22-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="cfb22-223">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="cfb22-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="cfb22-224">Anna **Toimitus**-välilehden **Rivin tiedot** -pikavälilehden **Vahvistettu lähetyspäivämäärä** -kenttään kuluvan päivän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="cfb22-225">Varaa varastoa jokaiselle lisätylle riville seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="cfb22-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="cfb22-226">Valitse varattava rivi.</span><span class="sxs-lookup"><span data-stu-id="cfb22-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="cfb22-227">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="cfb22-228">Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="cfb22-229">Sulje **Varaus**-sivu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="cfb22-230">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="cfb22-231">Kun vapautus on tehty, näkyviin tulee tietosanomia, jotka sisältävät luodun aallon ja luodut kuormatunnukset.</span><span class="sxs-lookup"><span data-stu-id="cfb22-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="cfb22-232">Työtunnusten ja rekisterinumeroiden haku</span><span class="sxs-lookup"><span data-stu-id="cfb22-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="cfb22-233">Luotuna on nyt kaksi työtunnusta. Molemmilla tunnuksilla on kaksi keräilyriviä.</span><span class="sxs-lookup"><span data-stu-id="cfb22-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="cfb22-234">Etsi työtunnukset ja rekisterikilpien toimeksiannot alla olevien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="cfb22-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="cfb22-235">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="cfb22-236">Hae **Yleiskatsaus**-ruudukosta kahden juuri luodun myyntitilauksen **Tilausnumero**-sarake.</span><span class="sxs-lookup"><span data-stu-id="cfb22-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="cfb22-237">Merkitse muistiin kunkin myyntitilauksen vastaava työtunnus.</span><span class="sxs-lookup"><span data-stu-id="cfb22-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="cfb22-238">Valitse kunkin myyntitilauksen rivi, jos haluat nähdä **Rivit**-ruudukon liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="cfb22-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="cfb22-239">Merkitse muistiin kunkin nimikkeen keräyssijainti.</span><span class="sxs-lookup"><span data-stu-id="cfb22-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="cfb22-240">Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="cfb22-241">Valitse toimintoruudussa **Dimensiot** ja avaa **Dimension näyttö**-valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="cfb22-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="cfb22-242">Varmista, että **Rekisterikilpi**-, **Varasto**- ja **Nimikenumero**-valintaruudut on valittu. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="cfb22-243">Määritä **Suodatin**-ruudussa seuraavat suodattimet:</span><span class="sxs-lookup"><span data-stu-id="cfb22-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="cfb22-244">**Nimiketunnus** – **on** *L0101* tai *T100*</span><span class="sxs-lookup"><span data-stu-id="cfb22-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="cfb22-245">**Varasto** – **alkaa numerolla** - *61*</span><span class="sxs-lookup"><span data-stu-id="cfb22-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="cfb22-246">Kirjoita muistiin näkyvissä olevat **rekisterikilven** arvot.</span><span class="sxs-lookup"><span data-stu-id="cfb22-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="cfb22-247">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="cfb22-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="cfb22-248">Mobiililaitteen työnkulun suoritus – Tuotteen työn vahvistuksen määritys</span><span class="sxs-lookup"><span data-stu-id="cfb22-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="cfb22-249">Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä varastossa *61*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-249">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="cfb22-250">Siirry kohtaan **Lähtevät \> Klusterikeräilyn luominen**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="cfb22-251">Näkyviin tulee **TEHTÄVÄ: Liitä työ klusteriin** -sivu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="cfb22-252">Anna myyntitilaukselle 1 työtunnus ja liitä se klusterisijaintiin 1.</span><span class="sxs-lookup"><span data-stu-id="cfb22-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="cfb22-253">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-254">Anna myyntitilaukselle 2 työtunnus ja liitä se klusterisijaintiin 2.</span><span class="sxs-lookup"><span data-stu-id="cfb22-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="cfb22-255">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="cfb22-256">Näkyviin tulee **TEHTÄVÄ: Klusterikeräilyn luominen: Keräily** -sivu, joka sisältää *Nimike L0101 2 PL* -kohdan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="cfb22-257">Koska klusteriprofiili määrittää sijaintien numeroksi 2, järjestelmä ohjaa käyttäjän automaattisesti ensimmäiseen konsolidoituun keräilyyn. Se on nimikkeen *L0101* kaksi kuormalavaa.</span><span class="sxs-lookup"><span data-stu-id="cfb22-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="cfb22-258">Kun noudatat seuraavia ohjeita, voit missä tahansa vaiheessa valita **Tiedot**-välilehden ja katsoa tehtävän lisätietoja, kuten keräilysijainnin.</span><span class="sxs-lookup"><span data-stu-id="cfb22-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="cfb22-259">Määritä **NIMIKE**-kentän arvoksi *L0101*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="cfb22-260">Tämä vahvistaa nimikenumeron, joka vaaditaan tälle valikon vaihtoehdolle (se määritettiin aiemmin valitsemalla **Työn vahvistuksen määritys** **Mobiililaitteen valikon vaihtoehto** -sivulla tämän valikon vaihtoehdon luomisen yhteydessä).</span><span class="sxs-lookup"><span data-stu-id="cfb22-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="cfb22-261">Anna rekisterikilpinumero, joka liittyy keräiltävässä sijainnissa olevaan nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="cfb22-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="cfb22-262">Keräile kaksi kuormalavaa.</span><span class="sxs-lookup"><span data-stu-id="cfb22-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="cfb22-263">Määritä **RK**-kentän arvoksi *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="cfb22-264">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="cfb22-265">**TEHTÄVÄ: Lajittelu: Klusterikeräilyn luominen** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="cfb22-266">Tässä voit lajitella kaksi keräiltyä kuormalavaa keräilysijaintiin.</span><span class="sxs-lookup"><span data-stu-id="cfb22-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="cfb22-267">Tämä sijainti voi olla kassi tai kontti, jota käytetään keräillyn varaston erottelussa myyntitilauksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="cfb22-268">Tarkastele nimikkeelle (*L0101*) ja määrälle (*20* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin (myyntitilaukselle 1).</span><span class="sxs-lookup"><span data-stu-id="cfb22-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="cfb22-269">Määritä **SIJAINTI NA** -kentän arvoksi *1*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="cfb22-270">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-271">Tarkastele nimikkeelle (*L0101*) ja määrälle (*20* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin 2 (myyntitilaukselle 2).</span><span class="sxs-lookup"><span data-stu-id="cfb22-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="cfb22-272">Määritä **SIJAINTI NA** -kentän arvoksi *2*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="cfb22-273">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="cfb22-274">Näkyviin tulee **TEHTÄVÄ: Klusterikeräilyn luominen: Keräily** -sivu, joka sisältää *Nimike T0100 7 kpl* -kohdan.</span><span class="sxs-lookup"><span data-stu-id="cfb22-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="cfb22-275">Tässä skenaariossa sijainti 1 ei voi hyväksyä myyntitilauksen 1 täyttämiseksi keräiltävien nimikkeiden täyttä määrää.</span><span class="sxs-lookup"><span data-stu-id="cfb22-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="cfb22-276">Sijainti on merkittävä täydeksi.</span><span class="sxs-lookup"><span data-stu-id="cfb22-276">A position must be marked as full.</span></span> <span data-ttu-id="cfb22-277">Tässä skenaariossa tehdään toisen nimikkeen osittainen keräily.</span><span class="sxs-lookup"><span data-stu-id="cfb22-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="cfb22-278">Toinen nimike keräillään osittain sijaintiin 1. Luodaan uusi ty, joka keräilee jäljellä olevan nimikkeen tilauksen täyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="cfb22-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="cfb22-279">Valitse valikkopainike (jossa on allekkain useita viivoja) ja lopeta Oikaisu sisään -tehtävä valitsemalla **Sijainti täynnä**.</span><span class="sxs-lookup"><span data-stu-id="cfb22-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="cfb22-280">Määritä täynnä oleva sijainti ja valitse *1*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="cfb22-281">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-282">Anna keräilymäärä, joka on yhä keräiltävissä sijaintiin 1.</span><span class="sxs-lookup"><span data-stu-id="cfb22-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="cfb22-283">Järjestelmä voi määrittää, mitä nimiketunnusta kerätään.</span><span class="sxs-lookup"><span data-stu-id="cfb22-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="cfb22-284">Syötä *2*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-284">Enter *2*.</span></span>
1. <span data-ttu-id="cfb22-285">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-286">Vahvista nimiketunnus, jotta jäljellä olevan nimikkeen keräily voidaan viimeistellä sijaintiin 2.</span><span class="sxs-lookup"><span data-stu-id="cfb22-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="cfb22-287">Määritä **NIMIKE**-kentän arvoksi *T0100*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="cfb22-288">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-289">Anna rekisterikilpi, josta nimike keräillään, määrittämällä **RK**-kentän arvoksi *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="cfb22-290">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-291">Tarkastele nimikkeelle (*T0100*) ja määrälle (*2* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin 2 (myyntitilaukselle 2).</span><span class="sxs-lookup"><span data-stu-id="cfb22-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="cfb22-292">Määritä **SIJAINTI NA** -kentän arvoksi *2*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="cfb22-293">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="cfb22-294">Tarkastele nimikkeelle (*T0100*) ja määrälle (*2* kpl) näytettäviä tietoja. Ne lajitellaan sijaintiin 1 (myyntitilaukselle 1).</span><span class="sxs-lookup"><span data-stu-id="cfb22-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="cfb22-295">Määritä **SIJAINTI NA** -kentän arvoksi *1*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="cfb22-296">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="cfb22-297">**TEHTÄVÄ: Klusterikeräilyn luominen: Hyllytys** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="cfb22-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="cfb22-298">Tässä skenaariossa klusterikeräily on valmis, ja käyttäjä ohjataan hyllyttämään keräillyt nimikkeet sijainnista 1 ja 2 väliaikaiseen sijaintiin *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="cfb22-299">Tarkista sivun tiedot.</span><span class="sxs-lookup"><span data-stu-id="cfb22-299">Review the information on the page.</span></span> <span data-ttu-id="cfb22-300">Se osoittaa, että väliaikaiseen sijaintiin hyllytettävä määrä on yhteensä *44*.</span><span class="sxs-lookup"><span data-stu-id="cfb22-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="cfb22-301">Valitse **OK** (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="cfb22-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="cfb22-302">Näyttöön tulee Klusteri on valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="cfb22-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="cfb22-303">Voit nyt käyttää valikon **Myynnin keräily** -vaihtoehtoa jäljellä olevan määrän keräilemiseksi.</span><span class="sxs-lookup"><span data-stu-id="cfb22-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="cfb22-304">Voit sitten käyttää valikon **Myynnin kuormaus** -vaihtoehtoa ja siirtää nimikkeet väliaikaisesta sijainnista lastauslaituriin.</span><span class="sxs-lookup"><span data-stu-id="cfb22-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]