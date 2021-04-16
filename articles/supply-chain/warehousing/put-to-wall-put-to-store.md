---
title: Asettaminen seinälle – asettaminen myymälään
description: Tässä ohjeaiheessa käsitellään Asettaminen seinälle – asettaminen myymälään -toimintoa. Tällä toiminnolla voi käsitellä skenaarioita, joissa tuote on konsolidoitava esipakkauksen valmistelualueelle määritettävien ehtojen perusteella. Se auttaa lyhentämään keräilyaikaa, koska keräyksen voi tehdä sen avulla yhden kohderekisterikilven mukaan ja koska siinä voi käyttää enemmän asetuspaikkoja kuin klusterikeräilyssä.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cf34a61d0b3f784b5a424473588d05bf8703635c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823284"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="6abe7-105">Asettaminen seinälle – asettaminen myymälään</span><span class="sxs-lookup"><span data-stu-id="6abe7-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6abe7-106">*Asettaminen seinälle – asettaminen myymälään* -toiminnolla voi käsitellä skenaarioita, joissa tuote on konsolidoitava esipakkauksen valmistelualueelle määritettävien ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="6abe7-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="6abe7-107">Koska keräilyn voi tehdä toiminnolla yhden rekisterikilven mukaan ja koska käytettävissä on enemmän asettamispaikkoja kuin klusterikeräilyssä, myymälöihin toimittaville yrityksillä tai pieniä nimikkeitä käsitteleville yrityksille on hyötyä keräilyajan lyhenemisestä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="6abe7-108">Tämän toiminnon työnkulku ohjaa kerätyn tuotteen lajittelusijaintiin jaettavaksi eri tyyppisiin kontteihin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="6abe7-109">Yleistäen voisi sanoa, että kukin lajittelusijainti sisältää useita lajittelupaikkoja.</span><span class="sxs-lookup"><span data-stu-id="6abe7-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="6abe7-110">Kukin lajittelupaikka määritetään liiketoimintaprosessin määrittämien ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6abe7-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="6abe7-111">Tavallisia ehtoja ovat lopullinen määränpää, lähetys tai kuorma.</span><span class="sxs-lookup"><span data-stu-id="6abe7-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="6abe7-112">Tuote jaetaan saapumisen jälkeen kuhunkin lajittelupaikkaan tilaukseen, määränpäähän, lähetykseen tai kuormaan liitetyn määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="6abe7-113">Kun kontti on täynnä tai valmis, se siirretään liiketoimintaprosessin mukaan väliaikaiseen sijaintiin tai lähetyssijaintiin lisäkäsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="6abe7-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="6abe7-114">Tätä varastointitoimintoa kutsutaan myös valo-ohjatuksi keräilyksi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="6abe7-115">Lähtevän lajittelutoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6abe7-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="6abe7-116">Ennen *Asettaminen seinälle – asettaminen myymälään* -toiminnon käyttöä *Lähtevä lajittelu* on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="6abe7-117">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6abe7-118">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="6abe7-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6abe7-119">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="6abe7-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6abe7-120">**Toiminnon nimi:** *Lähtevä lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="6abe7-121">*Lähtevä lajittelu* -toimintoa voidaan käyttää yhdessä *Organisaationlaajuinen aallon vaihekoodi* -toiminnon kanssa, jos se on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6abe7-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="6abe7-122">Tämä toiminto on otettava käyttöön myös siinä tapauksessa, että käytät aallon vaihekoodeissa määritettäviä esimääritettyjä koodeja.</span><span class="sxs-lookup"><span data-stu-id="6abe7-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="6abe7-123">**Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="6abe7-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="6abe7-124">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="6abe7-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6abe7-125">**Toiminnon nimi:** *Organisaationlaajuinen aallon vaihekoodi*</span><span class="sxs-lookup"><span data-stu-id="6abe7-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="6abe7-126">Määritys</span><span class="sxs-lookup"><span data-stu-id="6abe7-126">Setup</span></span>

<span data-ttu-id="6abe7-127">Tässä esittelyssä käytetään Contoso-vakiotietoja ja varastoa *62*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="6abe7-128">Lisäksi käytetään joitakin myöhemmin mainittavia lisäyksiä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="6abe7-129">Sijainnin tyyppi</span><span class="sxs-lookup"><span data-stu-id="6abe7-129">Location type</span></span>

1. <span data-ttu-id="6abe7-130">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijaintityypit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="6abe7-131">Luo lajittelun sijaintityyppi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="6abe7-132">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-132">Set the following values:</span></span>

    - <span data-ttu-id="6abe7-133">**Sijaintityyppi:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="6abe7-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="6abe7-134">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="6abe7-135">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="6abe7-136">Varastonhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="6abe7-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="6abe7-137">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="6abe7-138">Anna **Yleiset**-välilehden **Sijaintityypit**-pikavälilehden **Lajittelun sijaintityyppi** -kentän arvoksi *LAJITTELU*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="6abe7-139">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="6abe7-140">Sijaintiprofiili</span><span class="sxs-lookup"><span data-stu-id="6abe7-140">Location profile</span></span>

1. <span data-ttu-id="6abe7-141">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="6abe7-142">Luo lajittelusijainnin sijaintiprofiili valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="6abe7-143">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="6abe7-144">**Sijaintiprofiilin tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-145">**Nimi:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="6abe7-146">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6abe7-147">**Sijainnin muoto:** *PAKKAUS*</span><span class="sxs-lookup"><span data-stu-id="6abe7-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="6abe7-148">**Sijaintityyppi:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="6abe7-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="6abe7-149">**Käytä rekisterikilven seurantaa:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="6abe7-150">**Salli yhdistetyt nimikkeet:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="6abe7-151">**Salli yhdistetyt varastotilat:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="6abe7-152">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="6abe7-153">Sijainnit</span><span class="sxs-lookup"><span data-stu-id="6abe7-153">Locations</span></span>

1. <span data-ttu-id="6abe7-154">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="6abe7-155">Poista **Luo tarkistusnumeroita sijaintiin** -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="6abe7-156">Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="6abe7-157">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="6abe7-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="6abe7-158">**Sijainti:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-159">**Sijaintiprofiilin tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="6abe7-160">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="6abe7-161">Pakkausprofiilit</span><span class="sxs-lookup"><span data-stu-id="6abe7-161">Packing profiles</span></span>

1. <span data-ttu-id="6abe7-162">Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="6abe7-163">Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="6abe7-164">**Pakkausprofiilin tunnus:** *Lajitteli*</span><span class="sxs-lookup"><span data-stu-id="6abe7-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-165">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-166">**Kontin pakkauskäytäntö:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="6abe7-167">**Konttitunnuksen tila:** *Automaattinen*</span><span class="sxs-lookup"><span data-stu-id="6abe7-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="6abe7-168">**Kontin tyyppi:** *KUORMALAVA 48X48*</span><span class="sxs-lookup"><span data-stu-id="6abe7-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="6abe7-169">**Luo kontti automaattisesti kontin sulkemisessa:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="6abe7-170">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="6abe7-171">Aallon vaihekoodit</span><span class="sxs-lookup"><span data-stu-id="6abe7-171">Wave step codes</span></span>

<span data-ttu-id="6abe7-172">Jos *Organisaationlaajuinen aallon vaihekoodi* -toiminto on otettu käyttöön, määritä seuraava koodi:</span><span class="sxs-lookup"><span data-stu-id="6abe7-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="6abe7-173">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="6abe7-174">Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="6abe7-175">**Aallon vaihekoodi:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-176">**Aallon vaihekuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-177">**Aalto vaihetyyppi:** *Lajittelumalli*</span><span class="sxs-lookup"><span data-stu-id="6abe7-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="6abe7-178">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="6abe7-179">Lähtevien lajittelumalli</span><span class="sxs-lookup"><span data-stu-id="6abe7-179">Outbound sorting template</span></span>

<span data-ttu-id="6abe7-180">Lajittelumalli määrittää, luodaanko lajittelupaikat, mitä ehtoja käytetään ja mitkä ovat lajitteluprosessin muut määritteet.</span><span class="sxs-lookup"><span data-stu-id="6abe7-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="6abe7-181">Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevä lajittelumalli**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="6abe7-182">Valitse toimintoruudussa **Uusi** ja luo lajittelumalli.</span><span class="sxs-lookup"><span data-stu-id="6abe7-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="6abe7-183">Määritä uuden mallin ylätunnisteessa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="6abe7-184">**Lähtevän lajittelumallin tunnus:** *Aaltolajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="6abe7-185">**Kuvaus:** *Aaltolajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="6abe7-186">**Lajittelumallin tyyppi:** *Aallon kysyntä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="6abe7-187">Tämä kenttä määrittää käsittelyn, jossa lajittelumallia käytetään.</span><span class="sxs-lookup"><span data-stu-id="6abe7-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="6abe7-188">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-188">The following values are available:</span></span>

        - <span data-ttu-id="6abe7-189">**Aallon kysyntä** – Lajittelumallia käytetään *Asettaminen seinälle* -prosessissa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="6abe7-190">Tätä mallityyppiä käytetään ohittamaan pakkausasema ja käsittelemään varastoa suoraan aallosta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="6abe7-191">Tätä tyyppiä voi käyttää vain, jos **lajittelu** sisältyy aallon käsittelymenetelmänä aaltomalliin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="6abe7-192">**Kontti** – Tätä lajittelumallia käytetään *Kuormalavan luonti pakkauksen jälkeen* -prosessissa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="6abe7-193">Tätä mallityyppiä käytetään pakkausasemalla suljettujen ja kuormalavoille lajiteltavien konttien käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="6abe7-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="6abe7-194">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="6abe7-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="6abe7-195">**Sijainti:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="6abe7-196">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6abe7-197">**Lajittelun tarkistus:** *Sijainnin tarkistus*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="6abe7-198">Tämä kenttä määrittää lajittelun aikana tehtävän tarkistuksen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="6abe7-199">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-199">The following values are available:</span></span>

        - <span data-ttu-id="6abe7-200">None</span><span class="sxs-lookup"><span data-stu-id="6abe7-200">None</span></span>
        - <span data-ttu-id="6abe7-201">Rekisterikilven skannaus</span><span class="sxs-lookup"><span data-stu-id="6abe7-201">License plate scan</span></span>
        - <span data-ttu-id="6abe7-202">Toimen skannaus</span><span class="sxs-lookup"><span data-stu-id="6abe7-202">Position scan</span></span>

    - <span data-ttu-id="6abe7-203">**Luo työ paikkaan suljettaessa:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="6abe7-204">Jos tämän vaihtoehdon arvona on *Kyllä*, kun paikka luodaan, työ luodaan siirtämään varasto lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="6abe7-205">Jos vaihtoehdon arvona on *Ei*, varasto kerätään tilaukseen heti, kun paikka suljetaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="6abe7-206">**Paikan määritys:** *Manuaalinen*</span><span class="sxs-lookup"><span data-stu-id="6abe7-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="6abe7-207">Tämä kenttä määrittää paikan määrityksen tyypin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="6abe7-208">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-208">The following values are available:</span></span>

        - <span data-ttu-id="6abe7-209">**Manuaalinen** – käyttäjän on aina ilmaistava, mihin paikkaan varasto lajitellaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="6abe7-210">**Automaattinen** – järjestelmä ohjaa mahdollisuuksien mukaan varaston automaattisesti paikkaan lajittelumallin keskeytysten perusteella.</span><span class="sxs-lookup"><span data-stu-id="6abe7-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="6abe7-211">**Määritä lajittelupaikan ehdot:** *Käytä vian tyhjää paikkaa*</span><span class="sxs-lookup"><span data-stu-id="6abe7-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="6abe7-212">Tämä kenttää määrittää, otetaanko lajittelupaikoissa jo oleva varasto otetaan huomioon, kun paikka määritetään kysynnälle.</span><span class="sxs-lookup"><span data-stu-id="6abe7-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="6abe7-213">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-213">The following values are available:</span></span>

        - <span data-ttu-id="6abe7-214">**Käytä vain tyhjää paikkaa** – paikkoja, joihin on jo liitetty varastoa, ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="6abe7-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="6abe7-215">**Oletetaan paikka tyhjäksi** – Paikassa jo oleva varasto ohitetaan määrityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="6abe7-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="6abe7-216">Kaikkia käytettävissä olevia paikkoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="6abe7-216">All available positions will be used.</span></span>

    - <span data-ttu-id="6abe7-217">**Aallon vaihekoodi:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="6abe7-218">Jos *Organisaationlaajuinen aallon vaihekoodi* -toiminto on otettu käyttöön, myös *Lajittelu*-aallon vaihekoodi on määritettävä aallon vaihekoodeissa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="6abe7-219">**Sulje lajittelupaikka automaattisesti:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="6abe7-220">Jos tässä vaihtoehdossa on valittu *Kyllä*, lajittelupaikka suljetaan automaattisesti, kun kaikki sijaintiin tulevat työt on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="6abe7-221">**Lajittelusijaintien määrä:** *3*</span><span class="sxs-lookup"><span data-stu-id="6abe7-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="6abe7-222">Tämä kenttää määrittää suurimman lajittelupaikkojen määrän, jonka järjestelmän voi luoda.</span><span class="sxs-lookup"><span data-stu-id="6abe7-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="6abe7-223">**Lajittelupaikan etuliite:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="6abe7-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="6abe7-224">Tämä kenttää määrittää etuliitteen, jonka järjestelmä määrittää edeltämään paikkanumeroa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="6abe7-225">**Pakkaa lajittelupaikka automaattisesti:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6abe7-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="6abe7-226">Jos tämä vaihtoehto on *Kyllä*, lajittelupaikan varasto pakataan konttiin, kun paikka suljetaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="6abe7-227">**Pakkausprofiilin tunnus:** *Lajitteli*</span><span class="sxs-lookup"><span data-stu-id="6abe7-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="6abe7-228">Tämä kenttä määrittää pakkausprofiilin, jota käytetään, kun lajittelupaikka pakataan konttiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="6abe7-229">Määritä tässä lajittelumallissa käytettävät ehdot valitsemalla toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="6abe7-230">Lisää rivi valitsemalla kyselyn valintaikkunan **Lajittelu**-välilehdessä **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="6abe7-231">**Taulukko:** *Kuorman tiedot*</span><span class="sxs-lookup"><span data-stu-id="6abe7-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="6abe7-232">**Johdettu taulukko:** *Kuorman tiedot*</span><span class="sxs-lookup"><span data-stu-id="6abe7-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="6abe7-233">**Kenttä:** *Lähetyksen tunnus*</span><span class="sxs-lookup"><span data-stu-id="6abe7-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="6abe7-234">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="6abe7-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="6abe7-235">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-235">Select **OK**.</span></span>
1. <span data-ttu-id="6abe7-236">Näyttö voi tulla seuraava sanoma: Ryhmittely nollataan. Haluatko jatkaa?"</span><span class="sxs-lookup"><span data-stu-id="6abe7-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="6abe7-237">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-237">Select **Yes**.</span></span>

    <span data-ttu-id="6abe7-238">**Lähtevän lajittelun mallivaihdot** -painike tulee näkyviin toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="6abe7-239">Valitse toimintoruudussa **Lähtevän lajittelun mallivaihdot**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="6abe7-240">Käytä ryhmitykseen lähetyksen tunnusta valitsemalla **Ryhmittele kentän mukaan** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="6abe7-241">Tämä asetus luo kullekin lähetykselle yhden sijainnin, joka on aallon kontti.</span><span class="sxs-lookup"><span data-stu-id="6abe7-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="6abe7-242">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="6abe7-243">Aallon käsittelymenetelmät</span><span class="sxs-lookup"><span data-stu-id="6abe7-243">Wave process methods</span></span>

1. <span data-ttu-id="6abe7-244">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="6abe7-245">Valitse toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="6abe7-246">**Lajittelumenetelmä** lisätään käytettävissä olevien menetelmien luetteloon ja sille valitaan *Lähetys*-aallon mallityyppi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="6abe7-247">Aaltomallit</span><span class="sxs-lookup"><span data-stu-id="6abe7-247">Wave templates</span></span>

<span data-ttu-id="6abe7-248">Muokkaa aallon kysynnän lajittelussa käytettävää aaltomallia.</span><span class="sxs-lookup"><span data-stu-id="6abe7-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="6abe7-249">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="6abe7-250">Valitse **Aaltomallin tyyppi** -kentässä *Lähetys*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="6abe7-251">Valitse aiemmin luotu **62 Lähetysoletus** -malli.</span><span class="sxs-lookup"><span data-stu-id="6abe7-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="6abe7-252">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6abe7-253">Tee **Yleiset**-pikavälilehdessä seuraavat muutokset:</span><span class="sxs-lookup"><span data-stu-id="6abe7-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="6abe7-254">Määritä **Käsittele aalto, kun se vapautetaan varastoon** -asetuksen arvoksi *Ei*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="6abe7-255">Määritä **Määritä avoimiin aaltoihin** -vaihtoehdon arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="6abe7-256">Määritä **Lajittelu**-menetelmä **Menetelmät**-pikavälilehdessä:</span><span class="sxs-lookup"><span data-stu-id="6abe7-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="6abe7-257">Valitse **Jäljellä olevat menetelmät** -ruudukossa **lajittelu**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="6abe7-258">Siirrä **lajittelu**-menetelmä **Valitut menetelmät** -ruudukkoon oikealla nuolipainikkeella.</span><span class="sxs-lookup"><span data-stu-id="6abe7-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="6abe7-259">Valitse **Valitut menetelmät** -ruudukossa **lajittelu**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="6abe7-260">Määritä **Aallon vaihekoodi** -kentän arvoksi *Lajittelu*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="6abe7-261">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="6abe7-262">Mobiililaitteen valikkovaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="6abe7-262">Mobile device menu items</span></span>

1. <span data-ttu-id="6abe7-263">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6abe7-264">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6abe7-265">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="6abe7-266">**Valikkovaihtoehdon nimi:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-267">**Otsikko:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="6abe7-268">**Tila:** *Epäsuora*</span><span class="sxs-lookup"><span data-stu-id="6abe7-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="6abe7-269">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="6abe7-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="6abe7-270">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6abe7-271">**Tehtäväkoodi:** *Lähtevä lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="6abe7-272">**Käytä prosessiopasta:** *Kyllä* (oletusarvo)</span><span class="sxs-lookup"><span data-stu-id="6abe7-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="6abe7-273">**Lähtevän lajittelumallin tunnus:** *Aaltolajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="6abe7-274">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="6abe7-275">Mobiililaitevalikko</span><span class="sxs-lookup"><span data-stu-id="6abe7-275">Mobile device menu</span></span>

1. <span data-ttu-id="6abe7-276">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="6abe7-277">Valitse valikkoluettelosta **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="6abe7-278">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6abe7-279">Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -ruudukossa juuri luotu **Lajittelu**-valikkovaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="6abe7-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="6abe7-280">Siirrä **Lajittelu** oikealla nuolipainikkeella **Valikon rakenne** -ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="6abe7-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="6abe7-281">Voit lisätä tällä tavoin valikkovaihtoehdon **Lähtevä**-valikkoon.</span><span class="sxs-lookup"><span data-stu-id="6abe7-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="6abe7-282">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="6abe7-283">Sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="6abe7-283">Location directives</span></span>

<span data-ttu-id="6abe7-284">Sijaintidirektiivejä on luotava ohjaamaan lajittelun valmistelun jälkeen luotua työtä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="6abe7-285">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="6abe7-286">Valitse **Työtilaustyyppi**-kentässä *Lajiteltu varastokeräily*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="6abe7-287">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6abe7-288">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="6abe7-289">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="6abe7-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="6abe7-290">**Nimi:** *Aseta lastausovelle*</span><span class="sxs-lookup"><span data-stu-id="6abe7-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="6abe7-291">Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6abe7-292">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="6abe7-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6abe7-293">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="6abe7-293">**Site:** *6*</span></span>
    - <span data-ttu-id="6abe7-294">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="6abe7-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="6abe7-295">**Direktiivikoodi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="6abe7-296">**Useita varastointiyksiköitä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="6abe7-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="6abe7-297">Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="6abe7-298">Valitse **Rivit**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="6abe7-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="6abe7-299">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="6abe7-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="6abe7-300">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="6abe7-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6abe7-301">**Määrästä:** *0*</span><span class="sxs-lookup"><span data-stu-id="6abe7-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="6abe7-302">**Määrälle:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="6abe7-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="6abe7-303">Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="6abe7-304">Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="6abe7-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="6abe7-305">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="6abe7-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="6abe7-306">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="6abe7-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6abe7-307">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="6abe7-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="6abe7-308">Valitse **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -pikavälilehden **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="6abe7-309">Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="6abe7-310">Etsi kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jonka **Kenttä**-kentän asetuksena on *Sijainti*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="6abe7-311">Määritä tämän rivin **Ehdot**-kentän arvoksi *Lastauspaikan ovi*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="6abe7-312">Vahvista muokkaus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="6abe7-313">Työluokat</span><span class="sxs-lookup"><span data-stu-id="6abe7-313">Work classes</span></span>

1. <span data-ttu-id="6abe7-314">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="6abe7-315">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6abe7-316">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="6abe7-317">**Työluokan tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="6abe7-318">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="6abe7-319">**Työtilauksen tyyppi:** *Lajiteltu varastokeräily*</span><span class="sxs-lookup"><span data-stu-id="6abe7-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="6abe7-320">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="6abe7-321">Työmallit</span><span class="sxs-lookup"><span data-stu-id="6abe7-321">Work templates</span></span>

1. <span data-ttu-id="6abe7-322">Valitse **Varastonhallinta \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6abe7-323">Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="6abe7-324">Valitse ruudukossa **62 Kerää pakettiin** -työmalli.</span><span class="sxs-lookup"><span data-stu-id="6abe7-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="6abe7-325">Valitse toimintoruudussa **Työn otsikoiden katkaisut**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="6abe7-326">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6abe7-327">Poista **Ryhmittele tämän kentän mukaan** -valintaruudun valinta sillä rivillä, jossa **Kentän nimi** -kentän asetuksena *Lähetyksen tunnus*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="6abe7-328">Valitse **Tallenna** ja sulje sitten **Työn otsikoiden katkaisut** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="6abe7-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="6abe7-329">Valitse **Työtilaustyyppi**-kentässä *Lajiteltu varastokeräily*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="6abe7-330">Luo työmalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="6abe7-331">Määritä **Yleiset**-osassa seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="6abe7-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="6abe7-332">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="6abe7-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="6abe7-333">**Työmalli:** *Lajiteltu keräily*</span><span class="sxs-lookup"><span data-stu-id="6abe7-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="6abe7-334">**Työmallin kuvaus:** *Lajiteltu keräily*</span><span class="sxs-lookup"><span data-stu-id="6abe7-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="6abe7-335">Valitse **Tallenna**, jos haluat, että **Työmallin tiedot** -osa on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="6abe7-336">**Työmallin tiedot** -osassa luodaan kaksi riviä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="6abe7-337">Valitse **Uusi** ja määritä sitten seuraavat arvot riville 1:</span><span class="sxs-lookup"><span data-stu-id="6abe7-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="6abe7-338">**Työtyyppi:** *Poiminta*</span><span class="sxs-lookup"><span data-stu-id="6abe7-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="6abe7-339">**Pakollinen:** valittu (= *Kyllä*)</span><span class="sxs-lookup"><span data-stu-id="6abe7-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="6abe7-340">**Työluokan tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="6abe7-341">Valitse **Uusi** uudelleen ja määritä sitten seuraavat arvot riville 2:</span><span class="sxs-lookup"><span data-stu-id="6abe7-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="6abe7-342">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="6abe7-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6abe7-343">**Pakollinen:** valittu (= *Kyllä*)</span><span class="sxs-lookup"><span data-stu-id="6abe7-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="6abe7-344">**Työluokan tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="6abe7-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="6abe7-345">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="6abe7-346">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="6abe7-346">Example scenario</span></span>

<span data-ttu-id="6abe7-347">Tässä skenaariossa simuloidaan tilanne, jossa pieniä nimikkeitä varastoidaan varastossa sijainteihin ja jotka on pakattava laatikoihin ennen lähetystä, sekä tilannetta, johon pakkausasematoiminto ei sovi hyvin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="6abe7-348">Työntekijät keräävät samalla kertaa tilauksia useille asiakkaille ja eri osoitteisiin keräilyn nopeuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="6abe7-349">Kun keräily on valmis, työntekijät saapuvat lajittelusijaintiin, jossa kerätyt nimikkeet lajitellaan oikeaan laatikkoon vaadittujen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6abe7-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="6abe7-350">Tässä esimerkissä oikea laatikko määritetään lähetyksen tunnuksen avulla, sillä jokaisella toimituksella on eri osoite.</span><span class="sxs-lookup"><span data-stu-id="6abe7-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="6abe7-351">Kun kaikki kuorman nimikkeet on pakattu ja lajiteltu lähetyksen mukaan, laatikot siirretään valmistelualueelle ja lastataan lopuksi ajoneuvoon.</span><span class="sxs-lookup"><span data-stu-id="6abe7-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="6abe7-352">Varmista ennen tämän skenaarion aloittamista, että varaston kaikki vakiotoiminnot on määritetty oikein varastossa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="6abe7-353">Tätä tarkoitusta varten käytetään Contoson vakiovarastoa *62*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="6abe7-354">Vakiomäärityksiä ei ole muutettu lukuun ottamatta asetuksissa kuvattuja tilanteita.</span><span class="sxs-lookup"><span data-stu-id="6abe7-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="6abe7-355">Luo kysyntää</span><span class="sxs-lookup"><span data-stu-id="6abe7-355">Create demand</span></span>

<span data-ttu-id="6abe7-356">Ennen kuin toimintoa voidaan esitellä, sitä varten on luotava kysyntää.</span><span class="sxs-lookup"><span data-stu-id="6abe7-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="6abe7-357">Tässä skenaariossa luodaan kolme myyntitilausta kolmelle eri asiakkaalle. Tällä tavoin voidaan simuloida eri toimitusosoitteita.</span><span class="sxs-lookup"><span data-stu-id="6abe7-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="6abe7-358">Tällä tavoin luoda kolme eri lähetystä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="6abe7-359">Varmista ennen myyntitilausten ja lähetysten luontia, että keräilysijaintien varasto riittää kaikkien tilattujen nimikkeiden osalta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="6abe7-360">Vahvista myyntitilauksen keräilyssä käytetyt keräilysijainnit tarkistamalla sijaintidirektiivin asetukset.</span><span class="sxs-lookup"><span data-stu-id="6abe7-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="6abe7-361">Jos sinun on muokattava varastoa, voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai mitä tahansa muuta virtausta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="6abe7-362">Varaa sitten varastoa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="6abe7-363">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6abe7-364">Luo tilauksen 1 myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="6abe7-365">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6abe7-366">**Asiakas:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="6abe7-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="6abe7-367">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="6abe7-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="6abe7-368">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-368">Select **OK**.</span></span>
1. <span data-ttu-id="6abe7-369">**Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6abe7-370">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-370">Set the following values:</span></span>

    - <span data-ttu-id="6abe7-371">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6abe7-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6abe7-372">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="6abe7-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="6abe7-373">Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="6abe7-374">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="6abe7-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="6abe7-375">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="6abe7-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="6abe7-376">Varaa varastoa toistamalla seuraavat vaiheet tilauksen kunkin tilausrivin osalta:</span><span class="sxs-lookup"><span data-stu-id="6abe7-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="6abe7-377">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="6abe7-378">Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="6abe7-379">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-379">Select **Save**.</span></span>

1. <span data-ttu-id="6abe7-380">Luo tilauksen 2 myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="6abe7-381">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6abe7-382">**Asiakas:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="6abe7-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="6abe7-383">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="6abe7-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="6abe7-384">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-384">Select **OK**.</span></span>
1. <span data-ttu-id="6abe7-385">**Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6abe7-386">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-386">Set the following values:</span></span>

    - <span data-ttu-id="6abe7-387">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6abe7-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6abe7-388">**Määrä** *7*</span><span class="sxs-lookup"><span data-stu-id="6abe7-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="6abe7-389">Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="6abe7-390">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="6abe7-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="6abe7-391">**Määrä** *3*</span><span class="sxs-lookup"><span data-stu-id="6abe7-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="6abe7-392">Varaa varastoa toistamalla seuraavat vaiheet tilauksen kunkin tilausrivin osalta:</span><span class="sxs-lookup"><span data-stu-id="6abe7-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="6abe7-393">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="6abe7-394">Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="6abe7-395">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-395">Select **Save**.</span></span>

1. <span data-ttu-id="6abe7-396">Luo tilauksen 3 myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="6abe7-397">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6abe7-398">**Asiakas:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="6abe7-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="6abe7-399">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="6abe7-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="6abe7-400">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-400">Select **OK**.</span></span>
1. <span data-ttu-id="6abe7-401">**Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6abe7-402">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6abe7-402">Set the following values:</span></span>

    - <span data-ttu-id="6abe7-403">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6abe7-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6abe7-404">**Määrä** *8*</span><span class="sxs-lookup"><span data-stu-id="6abe7-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="6abe7-405">Varaa myyntirivin mukainen varasto seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6abe7-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="6abe7-406">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="6abe7-407">Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="6abe7-408">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-408">Select **Save**.</span></span>

<span data-ttu-id="6abe7-409">Vapauta kukin myyntitilaus varastoon seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="6abe7-410">Erillisiä lähetyksiä luodaan kolme.</span><span class="sxs-lookup"><span data-stu-id="6abe7-410">Three different shipments will be created.</span></span> <span data-ttu-id="6abe7-411">Kaikki kolme lähetystä lisätään sitten yhteen uuteen aaltoon.</span><span class="sxs-lookup"><span data-stu-id="6abe7-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="6abe7-412">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6abe7-413">Valitse ruudukossa ensimmäinen luotu myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="6abe7-414">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6abe7-415">Näyttöön tulevat tietosanomat ilmaisevat luodun aallon tunnuksen ja lähetyksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="6abe7-416">Vapauta myyntilaukset 2 ja 3 varastoon toistamalla edelliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6abe7-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="6abe7-417">Huomaa, että saamasi tietosanoma ilmaisee, aaltoon on lisätty lähetys, joka luotiin, kun myyntitilaus 1 vapautettiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="6abe7-418">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="6abe7-419">Avaa **Aallot**-sivu valitsemalla aallon tunnus, joka luotiin myyntitilausten vapauttamisesta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="6abe7-420">Aallon tiedot ovat tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="6abe7-420">This page shows the wave details.</span></span> <span data-ttu-id="6abe7-421">Luodut lähetykset näkyvät **Aallon rivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="6abe7-422">Nyt on luotava työ, jolla nimikkeet tuodaan keräilysijainneista lajittelusijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="6abe7-423">Valitse toimintoruudussa **Käsittely**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="6abe7-424">Lajittelumenetelmä määrittää aallon käsittelyn aikana varaston lajittelupaikkoihin lajittelumallien avulla.</span><span class="sxs-lookup"><span data-stu-id="6abe7-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="6abe7-425">Kun aalto on käsitelty, avautuva tietosanoma ilmoittaa, että aalto on kirjattu ja työ on luotu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="6abe7-426">Voit tarkastella luotua työtä valitsemalla toimintoruudun **Aalto**-välilehden **Liittyvät tiedot** -ryhmässä **Työ**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="6abe7-427">Kirjoita työn tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="6abe7-428">Valitse **Varastohallinta \> Pakkaus ja konttiinpakkaus \> Lähtevän lajittelupaikan määritykset**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="6abe7-429">Vasemmassa sarakkeessa voi tarkastella kullekin lähetykselle luotua lähtevää lajittelupaikkaa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="6abe7-430">Voit tarkastella **Lajittelupaikan ehdot** -pikavälilehdessä kyseisen paikan lähetystunnusta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="6abe7-431">Yksi työtunnus on luotu tuomaan varasto keräilysijainneista lajittelusijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="6abe7-432">Työn viimeistelyyn tarvitaan työtunnus, joka luotiin aallon käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="6abe7-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="6abe7-433">Myyntitilauksen keräys lajittelusijaintiin</span><span class="sxs-lookup"><span data-stu-id="6abe7-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="6abe7-434">Kirjaudu mobiilisovellukseen työntekijänä varastossa *62*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="6abe7-435">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="6abe7-436">Valitse **Lähtevä**-valikossa **Myynnin keräily**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="6abe7-437">Valitse **Tunnus**-kenttä ja anna sitten aallon käsittelystä saatu työtunnus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="6abe7-438">Vahvista kirjaus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-438">Confirm your entry.</span></span>

    <span data-ttu-id="6abe7-439">Seuraavaksi sinua pyydetään antamaan kohderekisterikilpi (RK).</span><span class="sxs-lookup"><span data-stu-id="6abe7-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="6abe7-440">Huomaa, että myyntilauksen 1 rivi 1 ilmaisee, mitä on kerättävä ja lisättävä kohderekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="6abe7-441">Näkyvissä on nimiketunnus, määrä, nimikkeen kuvaus ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="6abe7-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="6abe7-442">Anna kohderekisterikilpi **Kohde-RK**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6abe7-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="6abe7-443">Voit kerätä kaikki käsitellystä aallosta luodut rivit samaan kohderekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="6abe7-444">Vahvista kirjaus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-444">Confirm your entry.</span></span>

    <span data-ttu-id="6abe7-445">Mobiilisovelluksessa on nyt sarja **Keräily**-sivuja, jotka ohjaavat keräilysijaintiin sekä kerättävään nimikkeeseen ja keräysmäärään.</span><span class="sxs-lookup"><span data-stu-id="6abe7-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="6abe7-446">Kun kerätty nimike on rekisterikilpeen, keräilytyö vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="6abe7-447">Viimeinen sivu on työ, jolla kerätyt nimikkeet asetetaan lajittelusijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="6abe7-448">Vahvista ensimmäinen keräilytyö.</span><span class="sxs-lookup"><span data-stu-id="6abe7-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="6abe7-449">Seuraava keräilytyö näytetään.</span><span class="sxs-lookup"><span data-stu-id="6abe7-449">The next pick work is shown.</span></span> <span data-ttu-id="6abe7-450">Vahvista keräily.</span><span class="sxs-lookup"><span data-stu-id="6abe7-450">Confirm the pick.</span></span>
1. <span data-ttu-id="6abe7-451">Jatka jäljellä olevan keräilytyön vahvistamiseen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="6abe7-452">Viimeisenä vaiheena suoritetaan asettamistyö valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-452">The last step is to complete the put work.</span></span> <span data-ttu-id="6abe7-453">Vahvista hyllytys lajittelusijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="6abe7-454">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="6abe7-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="6abe7-455">Lopeta **Myynnin keräily** mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="6abe7-456">Lajittelu / asettaminen seinälle</span><span class="sxs-lookup"><span data-stu-id="6abe7-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="6abe7-457">Nyt kun varasto on asetettu lajittelusijaintiin, se on lajiteltava oikeaan lajittelupaikkaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="6abe7-458">Kirjaudu mobiilisovellukseen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="6abe7-459">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="6abe7-460">Aloita nimikkeiden lajittelu valitsemalla **Lähtevät**-valikossa **Lajittelu**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="6abe7-461">Anna **Rekisterikilpi/kontti**-kentässä valitun myyntitilaustyön kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="6abe7-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="6abe7-462">Vahvista kirjaus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-462">Confirm your entry.</span></span>
1. <span data-ttu-id="6abe7-463">Anna ensimmäinen lajiteltava nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="6abe7-464">Järjestelmä määrittää ensimmäisen näytettävän lajittelupaikan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="6abe7-465">Vahvista lajittelupaikka.</span><span class="sxs-lookup"><span data-stu-id="6abe7-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="6abe7-466">Sinua pyydetään määrittämään rekisterikilpi lajittelupaikkaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="6abe7-467">Valitse **Rekisterikilpi**-kenttä, anna rekisterinumero ja vahvista merkintä sitten.</span><span class="sxs-lookup"><span data-stu-id="6abe7-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="6abe7-468">Koska lajittelupaikka liittyy lähetyksen tunnukseen, kerätyt nimikkeet lajitellaan lähtevää lähetystä ja myyntitilausta koskevaan rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="6abe7-469">Seuraavalla sivulla näkyy nimiketunnus, määrä, lajittelupaikan tunnus sekä lähtevän (keräilyn) ja saapuvan (lajittelun) rekisterikilven tunnukset.</span><span class="sxs-lookup"><span data-stu-id="6abe7-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="6abe7-470">Tämän sivut ohjaavat lajittelemaan määritetyn nimikkeen määrät keräilyn rekisterikilvestä lajittelun rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="6abe7-471">Vahvista lajittelupaikka.</span><span class="sxs-lookup"><span data-stu-id="6abe7-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="6abe7-472">Lajittele ensimmäisen lajittelupaikan nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="6abe7-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="6abe7-473">Kun olet valmis, järjestelmä ohjaa sinut seuraavaan lajittelupaikkaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="6abe7-474">Toista tämä prosessi kaikkien työtilauksen keräiltyrivien osalta.</span><span class="sxs-lookup"><span data-stu-id="6abe7-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="6abe7-475">Tässä prosessia on syytä käyttää myös silloin, kun useilla keräilyriveillä on sama nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="6abe7-476">Kun tämä prosessi toistetaan kaikkien nimikkeiden kohdalla, järjestelmä arvioi seuraavan luetun nimikkeen (työrivin) ehdot ja määrittää, mihin lajittelupaikkaan se asetetaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="6abe7-477">Sinut ohjataan automaattisesti asettamaan nimike oikeaan lajittelupaikkaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="6abe7-478">Vahvistuksen asetusten mukaan sinut ohjataan myös vahvistamaan tämä toiminto antamalla paikkanumero tai rekisterikilven tunnus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6abe7-479">Jos automaattinen lajittelu on otettu käyttöön, manuaalinen ohitus ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="6abe7-480">Kun olet valmis, tarkista paikkojen tila avaamalla Microsoft Dynamics 365 Supply Chain Managementissa **Lähtevät lajittelutoimimääritykset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="6abe7-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="6abe7-481">Jos paikat on suljettu automaattisesti, tuo suljetut paikat näkyviin valitsemalla **Näytä suljetut**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="6abe7-482">Huomaa, että lajittelupaikkatapahtumat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="6abe7-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="6abe7-483">Paikassa käsitelty nimi ja määrä näytetään.</span><span class="sxs-lookup"><span data-stu-id="6abe7-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="6abe7-484">Kun määrität lähtevien lajittelumallin, **Sulje lajittelupaikka automaattisesti** -asetukseksi valitaan *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="6abe7-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="6abe7-485">Tämän vuoksi paikka suljetaan automaattisesti, kun viimeinen odotettu varasto on asetettu siihen.</span><span class="sxs-lookup"><span data-stu-id="6abe7-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="6abe7-486">Lajittelupaikkojen tila on **Suljettu** ja työ on luotu siirtämään lajiteltu varasto *Lastausovi*-sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="6abe7-487">Viimeistely lajiteltu varaston keräilytyö siirtämällä varasto lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6abe7-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="6abe7-488">Kun varasto on valmis, tee sen lähetysvahvistus.</span><span class="sxs-lookup"><span data-stu-id="6abe7-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="6abe7-489">Lajitellun varaston keräilytyön käsittelemisen onnistuminen edellyttää, että mobiililaitteen valikkovaihtoehtoa, jossa työn luokkatunnuksen **Työtilauksen tyyppi** -kentäksi on valittu *Lajiteltu varaston keräily*, käytetään varastonsiirto- ja lastausprosessissa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="6abe7-490">Paikan sulkeminen manuaalisesti (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="6abe7-490">Manually close a position (optional)</span></span>

<span data-ttu-id="6abe7-491">Jos lajittelupaikat on suljettava manuaalisesti lähtevien lajittelumallin **Sulje lajittelupaikka automaattisesti** -asetuksena on oltava *Ei* ja sulkeminen on tehtävä, ennen kuin varastoa voidaan siirtää lastausovialueelle.</span><span class="sxs-lookup"><span data-stu-id="6abe7-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="6abe7-492">Paikat voidaan sulkea eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="6abe7-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="6abe7-493">Varastonhallinnan mobiilisovelluksen kautta:</span><span class="sxs-lookup"><span data-stu-id="6abe7-493">Via the Warehouse Management mobile app:</span></span>

    - <span data-ttu-id="6abe7-494">Käyttäjä voi lukea jonkin jo paikassa olevan nimikkeet ja sulkea sitten paikan valitsemalla **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="6abe7-495">Jos käyttäjä lukee kontin, joka on jo lajiteltu kontti, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="6abe7-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="6abe7-496">Käyttäjä voi kuitenkin jatkaa paikan sulkemista.</span><span class="sxs-lookup"><span data-stu-id="6abe7-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="6abe7-497">Microsoft Dynamics 365 Supply Chain Managementin **Lähtevät lajittelutoimimääritykset** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="6abe7-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="6abe7-498">Käyttäjä voi valita ensin lähtevien lajittelupaikkatietueen ja sitten toimintoruudussa **Sulje paikka**.</span><span class="sxs-lookup"><span data-stu-id="6abe7-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="6abe7-499">Vihjeitä</span><span class="sxs-lookup"><span data-stu-id="6abe7-499">Tips</span></span>

- <span data-ttu-id="6abe7-500">Nimikkeitä ei voi siirtää paikkojen välillä sen jälkeen, kun ne on määritetty johonkin paikkaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="6abe7-501">Järjestelmä arvioi, kuinka monta kappaletta kutakin nimikettä viedään tiettyyn paikkaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="6abe7-502">Lajittelumalli voidaan määrittää luomaan kontit automaattisesti, kun paikat suljetaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="6abe7-503">Tällä menetelmällä luodaan määritettyyn pakkausprofiiliin perustuva konttitunnuksen vakiorakenne.</span><span class="sxs-lookup"><span data-stu-id="6abe7-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6abe7-504">Kun varastosiirtotyö on luotu lajittelusijainnista, työtä ei saa peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="6abe7-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="6abe7-505">Muussa tapauksessa paikka ja kontit poistetaan järjestelmästä eikä niiden käsittely ole enää mahdollista.</span><span class="sxs-lookup"><span data-stu-id="6abe7-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="6abe7-506">Myös varasto poistetaan.</span><span class="sxs-lookup"><span data-stu-id="6abe7-506">The inventory will also be removed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]