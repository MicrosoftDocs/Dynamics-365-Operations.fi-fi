---
title: Hyllytysklusterit
description: Hyllytysklusterit ovat tapa, jolla voi kerätä samanaikaisesti useita rekisterikilpiä viedä sitten hyllytettäviksi eri sijainteihin. Ne voivat olla erittäin käteviä vähittäismyynnissä, jossa rekisterikilvet eivät yleensä ole täysiä kuormalavoja.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a330ddccbd17c92443232fc8488e36a59235773
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512327"
---
# <a name="putaway-clusters"></a><span data-ttu-id="841fc-104">Hyllytysklusterit</span><span class="sxs-lookup"><span data-stu-id="841fc-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="841fc-105">Hyllytysklusterit ovat tapa, jolla voi kerätä samanaikaisesti useita rekisterikilpiä viedä sitten hyllytettäviksi eri sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="841fc-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="841fc-106">Tätä prosessi on kuin *jakelureitti*.</span><span class="sxs-lookup"><span data-stu-id="841fc-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="841fc-107">Hyllytysklusterit voivat olla erittäin käteviä vähittäismyynnissä, jossa rekisterikilvet eivät yleensä ole täysiä kuormalavoja.</span><span class="sxs-lookup"><span data-stu-id="841fc-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="841fc-108">Klusterihyllytystoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="841fc-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="841fc-109">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="841fc-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="841fc-110">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="841fc-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="841fc-111">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="841fc-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="841fc-112">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="841fc-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="841fc-113">**Toiminnon nimi:** *Klusterihyllytystoiminto*</span><span class="sxs-lookup"><span data-stu-id="841fc-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="841fc-114">Esimerkkiskenaarion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="841fc-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="841fc-115">Klusteriprofiilit</span><span class="sxs-lookup"><span data-stu-id="841fc-115">Cluster profiles</span></span>

<span data-ttu-id="841fc-116">Hyllytyksen klusteriprofiili määrittää, mihin nimike sijoitetaan, sen sijainnin perusteella, joka nimikkeelle määritettiin vastaanoton yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="841fc-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="841fc-117">Jos tarvitaan eri klustereita, kullekin mobiililaitteen valikkonimikkeelle on luotava yksi erillinen hyllytysklusteri.</span><span class="sxs-lookup"><span data-stu-id="841fc-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="841fc-118">Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Klusteriprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="841fc-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="841fc-119">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="841fc-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="841fc-120">Määritä **Otsikko**-näkymässä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="841fc-121">**Hyllytyksen klusteriprofiilin tunnus:** *Klusterihyllytys*</span><span class="sxs-lookup"><span data-stu-id="841fc-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="841fc-122">**Hyllytyksen klusteriprofiilin nimi:** *Klusterihyllytys*</span><span class="sxs-lookup"><span data-stu-id="841fc-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="841fc-123">**Klusterityyppi:** *Hyllytys*</span><span class="sxs-lookup"><span data-stu-id="841fc-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="841fc-124">**Järjestysnumero:** Hyväksy oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="841fc-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="841fc-125">Valitsemalla **Tallenna** voit ottaa pakolliset kentät käyttöön **Yleinen**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="841fc-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="841fc-126">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="841fc-127">**Klusterimäärityksen ajoitus:** *Vastaanotossa*</span><span class="sxs-lookup"><span data-stu-id="841fc-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="841fc-128">Tämä kenttää määrittää, määritetäänkö hyllytysklusteri heti, kun varasto vastaanotetaan, vai lajitellaanko se myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="841fc-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="841fc-129">**Klusterin määrityssääntö:** *Manuaalinen*</span><span class="sxs-lookup"><span data-stu-id="841fc-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="841fc-130">Tämä kenttä määrittää, onko järjestelmän määritettävä klusterimääritys automaattisesti vai määrittääkö käyttäjä sen manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="841fc-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="841fc-131">**Direktiivikoodi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="841fc-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="841fc-132">**Hyllytysklusterin paikannus:** *Vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="841fc-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="841fc-133">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-133">The following values are available:</span></span>

        - <span data-ttu-id="841fc-134">**Vastaanotto** – sijainti löydetään heti vastaanoton aikana.</span><span class="sxs-lookup"><span data-stu-id="841fc-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="841fc-135">**Klusteria suljettaessa** – sijainti löydetään klusteria suljettaessa.</span><span class="sxs-lookup"><span data-stu-id="841fc-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="841fc-136">**Käyttäjäohjattu** – Sijainti löydetään, kun rekisterikilpi kerätään klusterista hyllytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="841fc-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="841fc-137">Tässä tapauksessa sijaintia ei määritetä, kun hyllytystyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="841fc-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="841fc-138">Käyttäjän on käynnistettävä sijoitusvaihe skannaamalla rekisterikilpi tai työtunnus hyllytyksen aikana.</span><span class="sxs-lookup"><span data-stu-id="841fc-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="841fc-139">Järjestelmä etsii sitten hyllytyssijainnin ja kertoo käyttäjälle, mihin kerätty määrä asetetaan.</span><span class="sxs-lookup"><span data-stu-id="841fc-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="841fc-140">**Käyttäjäkohtainen hyllytysklusteri:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="841fc-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="841fc-141">Tämä kenttä määrittää, onko kukin klusteri käyttäjäkohtainen, kun klustereita määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="841fc-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="841fc-142">Se on käytettävissä vain, kun **Klusterin määrityssääntö** -kentän asetuksena on *Automaattinen*.</span><span class="sxs-lookup"><span data-stu-id="841fc-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="841fc-143">**Yksikkörajoitus:** jätä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="841fc-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="841fc-144">Tämä kenttä määrittää yksikön, joka on vastaanotettava, jotta profiili on kelvollinen.</span><span class="sxs-lookup"><span data-stu-id="841fc-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="841fc-145">Jos jätetään tyhjäksi, kaikki yksiköt ovat kelvollisia.</span><span class="sxs-lookup"><span data-stu-id="841fc-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="841fc-146">**Työyksikön vaihto:** *Yksittäinen*</span><span class="sxs-lookup"><span data-stu-id="841fc-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="841fc-147">Tämä kenttä määrittää, konsolidoidaanko koko varasto (käyttämällä klusterin tunnusta ja rekisterikilpeä) yhteen rekisterikilpeen, kun klusteri suljetaan, ja hyllytetäänkö se yhtenä rekisterikilpenä vai erikseen vastaanotettuina rekisterikilpinä.</span><span class="sxs-lookup"><span data-stu-id="841fc-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="841fc-148">Tämä kenttä ei ole käytettävissä, kun **Hyllytysklusterin paikannus** -kentän asetuksena on *Vastaanotto*.</span><span class="sxs-lookup"><span data-stu-id="841fc-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="841fc-149">**Klusteri säilyy päärekisterikilpenä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="841fc-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="841fc-150">Jos tässä on asetuksena *Kyllä*, asetusvaiheen suorittamisen jälkeen klusterin tunnuksesta tulee päärekisterikilpi ja kaikki klusteritunnuksen nimikkeet linkitetään kyseiseen päärekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="841fc-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="841fc-151">Hyllytyksen lajitteluehdot määritetään **Klusterin lajittelu** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="841fc-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="841fc-152">Lisää rivi valitsemalla työkalurivillä **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="841fc-153">**Järjestysnumero:** Hyväksy oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="841fc-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="841fc-154">**Kentän nimi:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="841fc-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="841fc-155">Tämä kenttä määrittää kentän, jota tämän rivin on käytettävä lajitteluehtona.</span><span class="sxs-lookup"><span data-stu-id="841fc-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="841fc-156">**Lajittelu:** *Nouseva*</span><span class="sxs-lookup"><span data-stu-id="841fc-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="841fc-157">Tässä kentässä määritetään, tehdäänkö lajittelu nousevassa vai laskevassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="841fc-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="841fc-158">Lisää rivi valitsemalla **Klusterin työmalli** -pikavälilehden työkalurivillä **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="841fc-159">**Työtilaustyyppi:** *Ostotilaukset*</span><span class="sxs-lookup"><span data-stu-id="841fc-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="841fc-160">**Työmalli:** *61 - ostotilaus, suora*</span><span class="sxs-lookup"><span data-stu-id="841fc-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="841fc-161">Valitse toimintoruudussa ensin **Tallenna** ja sitten **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="841fc-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="841fc-162">Lisää kyselyyn toinen rivi valitsemalla **Klusterihyllytys**-valintaikkunan **Alue**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="841fc-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="841fc-163">Päivitä sitten kyselyn rivit seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="841fc-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="841fc-164">Taulu</span><span class="sxs-lookup"><span data-stu-id="841fc-164">Table</span></span> | <span data-ttu-id="841fc-165">Johdettu taulu</span><span class="sxs-lookup"><span data-stu-id="841fc-165">Derived table</span></span> | <span data-ttu-id="841fc-166">Kenttä</span><span class="sxs-lookup"><span data-stu-id="841fc-166">Field</span></span> | <span data-ttu-id="841fc-167">Kriteeri</span><span class="sxs-lookup"><span data-stu-id="841fc-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="841fc-168">Työ</span><span class="sxs-lookup"><span data-stu-id="841fc-168">Work</span></span> | <span data-ttu-id="841fc-169">Työ</span><span class="sxs-lookup"><span data-stu-id="841fc-169">Work</span></span> | <span data-ttu-id="841fc-170">Varasto</span><span class="sxs-lookup"><span data-stu-id="841fc-170">Warehouse</span></span> | <span data-ttu-id="841fc-171">*61*</span><span class="sxs-lookup"><span data-stu-id="841fc-171">*61*</span></span> |
    | <span data-ttu-id="841fc-172">Työ</span><span class="sxs-lookup"><span data-stu-id="841fc-172">Work</span></span> | <span data-ttu-id="841fc-173">Työ</span><span class="sxs-lookup"><span data-stu-id="841fc-173">Work</span></span> | <span data-ttu-id="841fc-174">Työ tunnus</span><span class="sxs-lookup"><span data-stu-id="841fc-174">Work ID</span></span> | <span data-ttu-id="841fc-175">Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="841fc-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="841fc-176">Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="841fc-177">Valitse toimintoruudussa **Tallenna** ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="841fc-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="841fc-178">Klusteriprofiilissa himmennettyinä näkyvät kentät, kun **Luo klusterin tunnus** -asetuksena on *Kyllä*, eivät ole käytettävissä eikä niitä oteta huomioon tätä ominaisuutta käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="841fc-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="841fc-179">Mobiililaitteen valikkovaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="841fc-179">Mobile device menu items</span></span>

<span data-ttu-id="841fc-180">Tässä toiminnossa on kaksi uutta mobiililaitteen valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="841fc-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="841fc-181">**Vastaanotto ja klusterilajittelu** -valikkovaihtoehdolla lajitellaan vastaanotettu varasto hyllytysklusteriin vastaanotettaessa.</span><span class="sxs-lookup"><span data-stu-id="841fc-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="841fc-182">**Klusterihyllytys**-valikkovaihtoehdolla klusteri hyllytetään määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="841fc-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="841fc-183">Vastaanotto ja klusterilajittelu</span><span class="sxs-lookup"><span data-stu-id="841fc-183">Receive and sort cluster</span></span>

<span data-ttu-id="841fc-184">Luo uusi mobiililaitteen valikkovaihtoehto varaston vastaanottamiseen ja lajitteluun klusteriin.</span><span class="sxs-lookup"><span data-stu-id="841fc-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="841fc-185">Tämä valikkovaihtoehto luo saapuvan työn varaston vastaanoton jälkeen, ja se ilmaisee, että vastaanoton valikkovaihtoehtoja käytetään hyllytysklustereissa.</span><span class="sxs-lookup"><span data-stu-id="841fc-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="841fc-186">**Vastaanotto ja klusterilajittelu** -valikkovaihtoehtoa voidaan käyttää vastaanoton seuraavien valikkovaihtoehtojen kanssa:</span><span class="sxs-lookup"><span data-stu-id="841fc-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="841fc-187">Ostotilausrivin vastaanotto</span><span class="sxs-lookup"><span data-stu-id="841fc-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="841fc-188">Ostotilausnimikkeen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="841fc-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="841fc-189">Kuorman nimikkeen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="841fc-189">Load item receiving</span></span>

1. <span data-ttu-id="841fc-190">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="841fc-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="841fc-191">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="841fc-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="841fc-192">Määritä **Otsikko**-näkymässä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="841fc-193">**Valikkovaihtoehdon nimi:** *Vastaanotto ja klusterilajittelu*</span><span class="sxs-lookup"><span data-stu-id="841fc-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="841fc-194">**Otsikko:** *Vastaanotto ja klusterilajittelu*</span><span class="sxs-lookup"><span data-stu-id="841fc-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="841fc-195">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="841fc-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="841fc-196">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="841fc-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="841fc-197">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="841fc-198">**Työn luontiprosessi:** *Ostotilausnimikkeen vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="841fc-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="841fc-199">**Luo rekisterikilpi:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="841fc-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="841fc-200">**Määritä hyllytysklusteri:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="841fc-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="841fc-201">**Määritä hyllytysklusteri** -asetus on käytettävissä vain vastaanoton yksivaiheisessa *Työn luontiprosessi* -tehtävässä.</span><span class="sxs-lookup"><span data-stu-id="841fc-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="841fc-202">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="841fc-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="841fc-203">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="841fc-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="841fc-204">Klusterin varastointi</span><span class="sxs-lookup"><span data-stu-id="841fc-204">Cluster putaway</span></span>

<span data-ttu-id="841fc-205">Luo uusi mobiililaitteen valikkovaihto klusterin hyllytykseen sen jälkeen, kun se on määritetty.</span><span class="sxs-lookup"><span data-stu-id="841fc-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="841fc-206">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="841fc-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="841fc-207">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="841fc-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="841fc-208">Määritä **Otsikko**-näkymässä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="841fc-209">**Valikkovaihtoehdon nimi:** *Klusterihyllytys*</span><span class="sxs-lookup"><span data-stu-id="841fc-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="841fc-210">**Otsikko:** *Klusterihyllytys*</span><span class="sxs-lookup"><span data-stu-id="841fc-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="841fc-211">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="841fc-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="841fc-212">**Käytä aiemmin luotua työtä:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="841fc-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="841fc-213">Määritä **Yleinen**-pikavälilehden **Ohjaus**-kentän arvoksi *Klusterihyllytys*.</span><span class="sxs-lookup"><span data-stu-id="841fc-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="841fc-214">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="841fc-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="841fc-215">Määritä **Työluokat**-pikavälilehdessä kelvollinen työluokka tälle mobiililaitteen valikkovaihtoehdolle:</span><span class="sxs-lookup"><span data-stu-id="841fc-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="841fc-216">**Työluokan tunnus:** *Osto*</span><span class="sxs-lookup"><span data-stu-id="841fc-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="841fc-217">**Työtilaustyyppi:** *Ostotilaukset*</span><span class="sxs-lookup"><span data-stu-id="841fc-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="841fc-218">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="841fc-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="841fc-219">Mobiililaitevalikko</span><span class="sxs-lookup"><span data-stu-id="841fc-219">Mobile device menu</span></span>

<span data-ttu-id="841fc-220">Lisää juuri luodut valikkovaihtoehdot mobiilisovelluksen saapuvien valikkoon.</span><span class="sxs-lookup"><span data-stu-id="841fc-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="841fc-221">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="841fc-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="841fc-222">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="841fc-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="841fc-223">Valitse valikkoluettelossa **Saapuvat**.</span><span class="sxs-lookup"><span data-stu-id="841fc-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="841fc-224">Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelossa **Vastaanotto ja klusterilajittelu**.</span><span class="sxs-lookup"><span data-stu-id="841fc-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="841fc-225">Siirrä valittu valikkovaihtoehto **Valikkorakenne**-luetteloon valitsemalla oikea nuolipainike.</span><span class="sxs-lookup"><span data-stu-id="841fc-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="841fc-226">Siirrä valikkovaihtoehto haluttuun kohtaan valikossa ylä- tai alanuolipainikkeella.</span><span class="sxs-lookup"><span data-stu-id="841fc-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="841fc-227">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="841fc-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="841fc-228">Lisää loput valikkovaihtoehdot toistamalla vaiheet 4–7:</span><span class="sxs-lookup"><span data-stu-id="841fc-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="841fc-229">Määritä klusteri</span><span class="sxs-lookup"><span data-stu-id="841fc-229">Assign cluster</span></span>
    - <span data-ttu-id="841fc-230">Klusterin varastointi</span><span class="sxs-lookup"><span data-stu-id="841fc-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="841fc-231">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="841fc-231">Example scenario</span></span>

<span data-ttu-id="841fc-232">Tämä skenaario simuloi hyllytysklusterin käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="841fc-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="841fc-233">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="841fc-233">Create a purchase order</span></span>

1. <span data-ttu-id="841fc-234">Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="841fc-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="841fc-235">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="841fc-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="841fc-236">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="841fc-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="841fc-237">**Toimittajan tili:** *1001*</span><span class="sxs-lookup"><span data-stu-id="841fc-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="841fc-238">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="841fc-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="841fc-239">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-239">Select **OK**.</span></span>

    <span data-ttu-id="841fc-240">**Kaikki ostotilaukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="841fc-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="841fc-241">Lisää **Kaikki ostotilaukset** -sivun **Ostotilausrivit**-pikavälilehdessä **Lisää rivi** -painikkeella seuraavat rivit:</span><span class="sxs-lookup"><span data-stu-id="841fc-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="841fc-242">Ostotilausrivi 1:</span><span class="sxs-lookup"><span data-stu-id="841fc-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="841fc-243">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="841fc-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="841fc-244">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="841fc-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="841fc-245">Ostotilausrivi 2:</span><span class="sxs-lookup"><span data-stu-id="841fc-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="841fc-246">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="841fc-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="841fc-247">**Määrä** *20*</span><span class="sxs-lookup"><span data-stu-id="841fc-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="841fc-248">Ostotilausrivi 3:</span><span class="sxs-lookup"><span data-stu-id="841fc-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="841fc-249">**Nimiketunnus:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="841fc-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="841fc-250">**Määrä** *30*</span><span class="sxs-lookup"><span data-stu-id="841fc-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="841fc-251">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="841fc-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="841fc-252">Kirjoita ostotilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="841fc-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="841fc-253">Varaston vastaanotto ja hyllytys mobiililaitteella</span><span class="sxs-lookup"><span data-stu-id="841fc-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="841fc-254">Varaston vastaanotto ja lajittelu klusteriin</span><span class="sxs-lookup"><span data-stu-id="841fc-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="841fc-255">Kirjaudu varastosovellukseen käyttäjänä, joka on määritetty varastoon *61*.</span><span class="sxs-lookup"><span data-stu-id="841fc-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="841fc-256">Valitse päävalikossa **Saapuva**.</span><span class="sxs-lookup"><span data-stu-id="841fc-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="841fc-257">Valitse **Saapuva**-valikossa **Vastaanotto ja klusterilajittelu**.</span><span class="sxs-lookup"><span data-stu-id="841fc-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="841fc-258">Anna **Ostotilausnro**-kentässä ostotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="841fc-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="841fc-259">Valitse **OK** (valintamerkkipainike).</span><span class="sxs-lookup"><span data-stu-id="841fc-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="841fc-260">Valitse **Nimike**-kenttä ja anna nimiketunnus *A0001* ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="841fc-261">Valitse **Määrä**-kenttä, anna arvoksi *10* numeronäppäimistöllä ja valitse sitten valintamerkkipainike.</span><span class="sxs-lookup"><span data-stu-id="841fc-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="841fc-262">Vahvista annettu määrä valitsemalla **Määrä**-tehtäväsivulla **OK** (valintamerkkipainike).</span><span class="sxs-lookup"><span data-stu-id="841fc-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="841fc-263">Vahvista valitsemalla **Nimike**-tehtäväsivulla **OK**, että nimike *A0001* annettiin.</span><span class="sxs-lookup"><span data-stu-id="841fc-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="841fc-264">Valitse **Klusterin tunnus** -kenttä ja määritä luotavalle klusterille tunnus antamalla jokin arvo.</span><span class="sxs-lookup"><span data-stu-id="841fc-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="841fc-265">Tässä annettua arvoa käytetään, kun ostotilauksessa jäljellä olevat kaksi nimikettä vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="841fc-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="841fc-266">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-266">Select **OK**.</span></span>

    <span data-ttu-id="841fc-267">**Ostotilausnro**-kenttä avautuu ja siinä on Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="841fc-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="841fc-268">Nimike *A0001* on nyt vastaanotettu *VASTOT*-sijaintiin ja määritetty vaiheessa 10 annettuun klusterin tunnukseen.</span><span class="sxs-lookup"><span data-stu-id="841fc-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="841fc-269">Toista vaiheet 4–11 ostotilauksessa jäljellä olevien nimikkeiden vastaanottamiseen ja klusterin tunnukseen määrittämiseen:</span><span class="sxs-lookup"><span data-stu-id="841fc-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="841fc-270">Nimikkeen *A0002* määrä on *20*</span><span class="sxs-lookup"><span data-stu-id="841fc-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="841fc-271">Nimikkeen *M9215* määrä on *30*</span><span class="sxs-lookup"><span data-stu-id="841fc-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="841fc-272">Klusterin sulkeminen</span><span class="sxs-lookup"><span data-stu-id="841fc-272">Close the cluster</span></span>

<span data-ttu-id="841fc-273">Klusteri on suljettava, ennen kuin klusterin nimikkeet voidaan hyllyttää.</span><span class="sxs-lookup"><span data-stu-id="841fc-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="841fc-274">Valitse Supply Chain Managementissa **Varastonhallinta \> Työ \> Lähtevä \> Työklusterit**.</span><span class="sxs-lookup"><span data-stu-id="841fc-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="841fc-275">Hae **Työklusterit**-sivun **Työklusteri**-osan **Klusterin tunnus** -kentässä aiemmin annetun klusterin tunnus.</span><span class="sxs-lookup"><span data-stu-id="841fc-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="841fc-276">Jos klusteri ei ole näkyvissä, se on ehkä jo suljettu.</span><span class="sxs-lookup"><span data-stu-id="841fc-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="841fc-277">Voit selvittää, onko klusteri suljettu, valitsemalla **Näytä suljettu työ** -valintaruutu ja hakemalla aiemmin annettua klusterin tunnusta.</span><span class="sxs-lookup"><span data-stu-id="841fc-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="841fc-278">Toimi sitten jonkin seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="841fc-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="841fc-279">Jos klusteri on suljettu, ohita tämän menettely jäljellä olevat vaiheet ja siirry seuraavaan menettelyyn [Klusterin hyllyttäminen](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="841fc-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="841fc-280">Jos klusteria ei ole suljettu, sulje klusteri manuaalisesti tämän menettelyjä jäljellä olevien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="841fc-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="841fc-281">Siirry sitten seuraavaan menettelyyn.</span><span class="sxs-lookup"><span data-stu-id="841fc-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="841fc-282">Valitse **Työklusteri**-osassa aiemmin annettu klusterin tunnus.</span><span class="sxs-lookup"><span data-stu-id="841fc-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="841fc-283">Valitse toimintoruudussa **Sulje klusteri**.</span><span class="sxs-lookup"><span data-stu-id="841fc-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="841fc-284">Kun klusteri on suljettu, se ei enää näy **Työklusteri**-osassa (ellei **Näytä suljettu työ** -valintaruutua ole valittuna).</span><span class="sxs-lookup"><span data-stu-id="841fc-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="841fc-285">Klusterin hyllyttäminen</span><span class="sxs-lookup"><span data-stu-id="841fc-285">Put the cluster away</span></span>

1. <span data-ttu-id="841fc-286">Kirjaudu varastosovellukseen käyttäjänä, joka on määritetty varastoon *61*.</span><span class="sxs-lookup"><span data-stu-id="841fc-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="841fc-287">Valitse päävalikossa **Saapuva**.</span><span class="sxs-lookup"><span data-stu-id="841fc-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="841fc-288">Valitse **Saapuva**-valikossa **Klusterihyllytys**.</span><span class="sxs-lookup"><span data-stu-id="841fc-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="841fc-289">Valitse **Klusterin tunnus** ja anna aiemmin annettu suljetun klusterin tunnus.</span><span class="sxs-lookup"><span data-stu-id="841fc-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="841fc-290">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-290">Select **OK**.</span></span>

    <span data-ttu-id="841fc-291">**Klusterihyllytys: keräily** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="841fc-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="841fc-292">Siinä näkyy klusterin tunnus, keräilysijainti, nimikkeet (näkyvissä on arvo *Useita*) ja klusterin kerättävä kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="841fc-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="841fc-293">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-293">Select **OK**.</span></span>

    <span data-ttu-id="841fc-294">**Klusterihyllytys: aseta** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="841fc-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="841fc-295">**Aseta**-ohjeet määrittävät klusterin tunnuksen, asetussijainnin, nimikkeet, kokonaismäärän ja klusterissa vastaanotettujen nimikkeiden rekisterikilpitunnukset.</span><span class="sxs-lookup"><span data-stu-id="841fc-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="841fc-296">Voit ohittaa tai hyväksyä tämän vaihtoehdon vakioasetuksilla.</span><span class="sxs-lookup"><span data-stu-id="841fc-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="841fc-297">![Klusterihyllytys: Aseta-sivu](media/Cluster_putaway-Put.png "Klusterihyllytys: Aseta-sivu")</span><span class="sxs-lookup"><span data-stu-id="841fc-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="841fc-298">Vahvista klusterin hyllytys valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="841fc-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="841fc-299">Klusteri on valmis -sanoma tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="841fc-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="841fc-300">Huomautuksia ja vihjeitä</span><span class="sxs-lookup"><span data-stu-id="841fc-300">Notes and tips</span></span>

<span data-ttu-id="841fc-301">Jos klusterin tunnuksesta tulee upotetun kuormalavan päärekisterikilpi, asetussijainti annetaan automaattisesti, kun klusterin tunnus skannataan.</span><span class="sxs-lookup"><span data-stu-id="841fc-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="841fc-302">Muita rekisterikilpiä ei tarvitse skannata, vaikka rekisterikilven luonti olisi määritetty manuaaliseksi.</span><span class="sxs-lookup"><span data-stu-id="841fc-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
