---
title: Lähtevä lajittelu
description: Tässä ohjeaiheessa on tietoja lähtevästä lajittelusta. Tämä toiminto helpottaa pienien konttien käsittelyä ja auttaa varastotyöntekijöitä parantamaan kuorma-auton kuormalavakapasiteetin suunnittelua ja järjestämistä.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017687"
---
# <a name="outbound-sorting"></a><span data-ttu-id="b8e8b-104">Lähtevä lajittelu</span><span class="sxs-lookup"><span data-stu-id="b8e8b-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8e8b-105">Tämä toiminto helpottaa pienien konttien käsittelyä ja auttaa varastotyöntekijöitä parantamaan kuorma-auton kuormalavakapasiteetin suunnittelua ja järjestämistä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="b8e8b-106">Lähtevää lajittelua käytettäessä pakatut kontit voidaan lajitella oikealle kuormalavalle pakkausasemalta.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="b8e8b-107">Myös pakkaushierarkia voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="b8e8b-108">Tämän toiminnon avulla pakatuista konteista voidaan luoda kuormalavoja pakkaustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="b8e8b-109">Konttia ei lähetetä lopulliseen toimitussijaintiin, sillä se on alkuperäisessä pakkaustyönkulussa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="b8e8b-110">Työntekijät voivat sen sijaan sulkea kontin ja siirtää sen lajittelutyypin sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="b8e8b-111">He voivat sitten lajitella kontit paikkoihin, joissa kussakin on rekisterikilpi (RK).</span><span class="sxs-lookup"><span data-stu-id="b8e8b-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="b8e8b-112">Konttien lajittelemisen jälkeen voidaan luoda työ, jolla koko rekisterikilpi lähetetään lopulliselle lähetyslaiturille tai väliaikaisiin sijainteihin sijaintidirektiivien tai omien tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="b8e8b-113">Lisäksi lajittelupaikan sulkeminen siirtää varaston heti lopulliselle lähetyslaiturille tilaukseen kerättäväksi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="b8e8b-114">Lähtevän lajittelutoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b8e8b-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="b8e8b-115">Ennen kuin käytät toimintoa, se on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="b8e8b-116">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b8e8b-117">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b8e8b-118">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b8e8b-119">**Toiminnon nimi:** *Lähtevä lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="b8e8b-120">Määritys</span><span class="sxs-lookup"><span data-stu-id="b8e8b-120">Setup</span></span>

<span data-ttu-id="b8e8b-121">Tässä skenaariossa on käytettävä **USMF** -vakioesittelytietoja ja varastoa *62*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="b8e8b-122">Lisäksi on suoritettava seuraavissa alaosioissa käsitellyt määritykset.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="b8e8b-123">Aaltomallin asetuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-123">Set up a wave template</span></span>

<span data-ttu-id="b8e8b-124">Tämä määritys käsittelee automaattisesti aallon ja luoda työn, kun rivi vapautetaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="b8e8b-125">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b8e8b-126">Valitse malliluettelossa **Varasto 62**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="b8e8b-127">Varmista **Yleiset** -pikavälilehdessä, että **Käsittele aalto, kun se vapautetaan varastoon** -vaihtoehtona on *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="b8e8b-128">Työntekijän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-128">Set up a worker</span></span>

<span data-ttu-id="b8e8b-129">Pakkausasemaa pidetään sijaintina.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-129">The packing station is considered a location.</span></span> <span data-ttu-id="b8e8b-130">Pakkausasemaan kirjautuvat varastotyöntekijät näkevät ja voivat käsitellä vain kyseiseen pakkaussijaintiin suunniteltuja lähetyksiä ja kontteja.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="b8e8b-131">Microsoft Dynamics 365:n kirjautuvan käyttäjän on oltava määritetty työntekijäksi varastonhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="b8e8b-132">Jos käyttäjän nimi ei ole työn käyttäjäluettelossa, lisää se käyttämällä seuraavaa menettelyä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="b8e8b-133">Näissä ohjeissa oletetaan, että käyttäjä on jo järjestelmässä ja että hänet on liitetty omana työntekijänä tai työntekijänä **Human Resources** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="b8e8b-134">Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="b8e8b-135">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-135">Select **New**.</span></span>
1. <span data-ttu-id="b8e8b-136">Valitse **Työntekijä** -kentässä kohdekäyttäjä työntekijäluettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="b8e8b-137">Valitse **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-137">Select **Select**.</span></span>
1. <span data-ttu-id="b8e8b-138">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b8e8b-139">Luo mobiililaitetili valitsemalla **Käyttäjät** -pikavälilehdessä **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-140">**Käyttäjätunnus:** anna yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="b8e8b-141">**Käyttäjänimi:** anna tunnukselle nimi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="b8e8b-142">**Oletusvarasto:** *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-143">**Valikon nimi:** *Pää*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="b8e8b-144">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b8e8b-145">Voit luoda avautuvassa **Määritä salasana** -valintaikkunassa yksinkertaisen salasanan, jolla käyttäjä voi kirjautua mobiilisovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="b8e8b-146">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-146">Set the following values:</span></span>

    - <span data-ttu-id="b8e8b-147">**Salasana:** anna yksinkertainen salasana.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="b8e8b-148">**Vahvista salasana:** anna sama salasana uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="b8e8b-149">Valitse **Määritä salasana**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-149">Select **Set password**.</span></span>

    <span data-ttu-id="b8e8b-150">Toimintokeskuksessa on ilmoitus, joka ilmaisee, että luodulle käyttäjälle on määritetty salasana.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="b8e8b-151">Sijaintityypin luonti</span><span class="sxs-lookup"><span data-stu-id="b8e8b-151">Create a location type</span></span>

1. <span data-ttu-id="b8e8b-152">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijaintityypit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="b8e8b-153">Luo sijaintityyppi valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-154">**Sijaintityyppi:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="b8e8b-155">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="b8e8b-156">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="b8e8b-157">Varastonhallinnan parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="b8e8b-158">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="b8e8b-159">Valitse **Yleiset** -välilehden **Sijaintityypit** -pikavälilehden **Lajittelun sijaintityyppi** -kentän arvoksi *LAJITTELU*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="b8e8b-160">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="b8e8b-161">Sijaintiprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-161">Set up a location profile</span></span>

1. <span data-ttu-id="b8e8b-162">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b8e8b-163">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-164">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-165">**Sijaintiprofiilin tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="b8e8b-166">**Nimi:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="b8e8b-167">Määritä **Yleiset** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-168">**Sijainnin muoto:** *ASRB* (käytävä-teline-hylly-lokero)</span><span class="sxs-lookup"><span data-stu-id="b8e8b-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="b8e8b-169">**Sijaintityyppi:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="b8e8b-170">**Käytä rekisterikilven seurantaa:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="b8e8b-171">**Salli yhdistetyt nimikkeet:** *Kyllä* (Kun arvoksi valitaan *Kyllä* , **Salli yhdistetyt varastoerät** -asetukseksi määritetään automaattisesti *Kyllä* eikä tätä asetusta voi muuttaa erikseen.)</span><span class="sxs-lookup"><span data-stu-id="b8e8b-171">**Allow mixed items:** *Yes* (When you set this option to *Yes* , the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="b8e8b-172">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="b8e8b-173">Sijainnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-173">Set up a location</span></span>

1. <span data-ttu-id="b8e8b-174">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="b8e8b-175">Poista ylätunnisteessa **Luo tarkistusnumeroita sijaintiin** -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="b8e8b-176">Luo sijainti valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-177">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-178">**Sijainti:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="b8e8b-179">**Sijaintiprofiilin tunnus:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="b8e8b-180">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="b8e8b-181">Lähtevän lajittelumallin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="b8e8b-182">Lähtevä lajittelumalli määrittää, luodaanko työ lajittelusijainnin ulkopuolella ja tehdäänkö lajittelu manuaalisesti vai automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="b8e8b-183">Tässä skenaariossa luodaan lähtevä lajittelumalli luomaan kuormalavat pakkausaseman jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="b8e8b-184">Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevät lajittelumallit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="b8e8b-185">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-186">Määritä uuden mallin ylätunnisteessa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-187">**Lähtevän lajittelumallin tunnus:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="b8e8b-188">**Kuvaus:** *Automaattisen työn luonti*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="b8e8b-189">**Lähtevän lajittelumallin tyyppi:** *Kontti*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="b8e8b-190">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-191">**Sijainti:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="b8e8b-192">Määritä **Yleiset** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-193">**Lajittelun tarkistus:** *Sijainnin tarkistus*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="b8e8b-194">**Luo työ paikkaan suljettaessa:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="b8e8b-195">Jos tämän vaihtoehdon arvona on *Kyllä* , kun paikka luodaan, työ luodaan siirtämään varasto lopulliseen lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-195">If this option is set to *Yes* , when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="b8e8b-196">Jos vaihtoehdon arvona on *Ei* , varasto kerätään tilaukseen heti, kun paikka suljetaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-196">If it's set to *No* , inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="b8e8b-197">**Paikan määritys:** *Automaattinen*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="b8e8b-198">Jos kentässä on valittu *Manuaalinen* , käyttäjän on aina ilmaistava, mihin paikkaan varasto lajitellaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-198">If this field is set to *Manual* , the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="b8e8b-199">Jos kentässä on valittu *Automaattinen* , järjestelmä ohjaa mahdollisuuksien mukaan varaston automaattisesti sijaintiin lajittelumallin taukojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-199">If it's set to *Automatic* , the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="b8e8b-200">Valitse **Tallenna** , jolloin **Muokkaa kyselyä** -painike tulee näkyviin toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="b8e8b-201">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="b8e8b-202">Lisää kyselyeditorin **Lajittelu** -välilehdessä rivi, jolla on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="b8e8b-203">**Taulukko:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b8e8b-204">**Johdettu taulu:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b8e8b-205">**Kenttä:** *Rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="b8e8b-206">Kun olet valinnut tämän arvon, näyttöön saattaa tulla seuraava sanoma: "Rahdinkuljetuspalvelukenttä ei ole indeksikenttä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="b8e8b-207">Haluatko lisätä lajittelun tähän? "</span><span class="sxs-lookup"><span data-stu-id="b8e8b-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="b8e8b-208">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-208">Select **Yes**.</span></span>

    - <span data-ttu-id="b8e8b-209">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b8e8b-210">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-210">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-211">Näyttö voi tulla seuraava sanoma: Ryhmittely nollataan. Haluatko jatkaa?"</span><span class="sxs-lookup"><span data-stu-id="b8e8b-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="b8e8b-212">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-212">Select **Yes**.</span></span>

    <span data-ttu-id="b8e8b-213">**Lähtevän lajittelun mallivaihdot** -painike tulee näkyviin toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="b8e8b-214">Valitse toimintoruudussa **Lähtevän lajittelun mallivaihdot**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="b8e8b-215">Määritä **Lähtevien lajitteluehdot** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-216">**Viitetaulukon nimi:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="b8e8b-217">**Viitekentän nimi:** *Rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="b8e8b-218">**Ryhmittele kentän mukaan:** Ryhmittele lähetykset rahdinkuljettajapalvelun mukaan valitsemalla tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="b8e8b-219">Valitse **OK** tallentaaksesi asetukset ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="b8e8b-220">Kontin pakkauskäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-220">Set up container packing policies</span></span>

1. <span data-ttu-id="b8e8b-221">Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin pakkauskäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="b8e8b-222">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-223">Määritä uuden käytännön ylätunnisteessa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-224">**Kontin pakkauskäytäntö:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-225">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="b8e8b-226">Määritä **Yleiset** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-227">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-228">**Lajittelun oletussijainti:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="b8e8b-229">**Painoyksikkö:** *kg*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="b8e8b-230">**Kontin sulkemiskäytäntö:** *Automaattinen vapautus*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="b8e8b-231">**Kontin vapautuskäytäntö:** *Säilön määrittäminen lähtevään lajittelusijaintiin*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="b8e8b-232">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="b8e8b-233">Määritä pakkausprofiilit</span><span class="sxs-lookup"><span data-stu-id="b8e8b-233">Set up packing profiles</span></span>

<span data-ttu-id="b8e8b-234">Luo uusi lajittelutoiminnon kanssa yhdessä käytettävä pakkausprofiili.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="b8e8b-235">Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="b8e8b-236">Luo rivi valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-237">**Pakkausprofiilin tunnus:** *Lajitteli*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-238">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-239">**Kontin pakkauskäytäntö:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-240">**Konttitunnuksen tila:** *Automaattinen*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="b8e8b-241">**Kontin tyyppi:** *Laatikko-suuri*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="b8e8b-242">**Luo kontti automaattisesti, kun kontti suljetaan:** Tyhjennetty (= *Ei* )</span><span class="sxs-lookup"><span data-stu-id="b8e8b-242">**Auto create container at container close:** Cleared (= *No* )</span></span>

1. <span data-ttu-id="b8e8b-243">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="b8e8b-244">Työluokkien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-244">Set up work classes</span></span>

<span data-ttu-id="b8e8b-245">Määritä yhdessä lajittelun kanssa käytettävä työluokka.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="b8e8b-246">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b8e8b-247">Luo lajittelu työluokka valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-248">**Työluokan tunnus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-249">**Kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-250">**Työtilauksen tyyppi:** *Lajiteltu varastokeräily*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="b8e8b-251">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="b8e8b-252">Mobiililaitteen valikkovaihtoehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="b8e8b-253">Uuden kuormalavan valikkovaihtoehdon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="b8e8b-254">Luo mobiililaitteen valikkovaihtoehto lajittelun aikana tapahtuvalla kuormalavojen luonnille.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="b8e8b-255">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b8e8b-256">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-257">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-258">**Valikkovaihtoehdon nimi:** *Kuormalavan luonti*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="b8e8b-259">**Otsikko:** *Kuormalavan luonti*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="b8e8b-260">**Tila:** *Epäsuora*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="b8e8b-261">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="b8e8b-262">Määritä **Yleiset** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-263">**Tehtäväkoodi:** *Lähtevä lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="b8e8b-264">Kun tämän kentän asetuksena on *Lähtevä lajittelu* , **Lähtevän lajittelumallin tunnus** -kenttä on näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-264">When this field is set to *Outbound sorting* , the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="b8e8b-265">**Käytä prosessiopasta:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="b8e8b-266">Kun **Tehtäväkoodi** -kentän asetuksena *Lähtevä lajittelu* , tämän asetuksen määrityksenä on automaattisesti *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-266">When the **Activity code** field is set to *Outbound sorting* , this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="b8e8b-267">**Lähtevän lajittelumallin tunnus:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="b8e8b-268">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="b8e8b-269">Uuden kuormaamisen valikkovaihtoehdon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-269">Set up a new loading menu item</span></span>

<span data-ttu-id="b8e8b-270">Luo seuraavaksi valikkovaihtoehto, jolla käyttäjät voivat siirtää lajitellut varastonimikkeet lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="b8e8b-271">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b8e8b-272">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-273">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-274">**Valikkovaihtoehdon nimi:** *Kuormaus lajittelusta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="b8e8b-275">**Otsikko:** *Kuormaus lajittelusta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="b8e8b-276">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="b8e8b-277">**Käytä aiemmin luotua työtä:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="b8e8b-278">Määritä **Yleinen** -pikavälilehden **Ohjaus** -kentän arvoksi *Käyttäjäohjattu*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="b8e8b-279">Valitse **Työluokat** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-279">On the **Work classes** FastTab, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="b8e8b-280">**Työluokan tunnus:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="b8e8b-281">**Työtilauksen tyyppi:** *Lajiteltu varastokeräily*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="b8e8b-282">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="b8e8b-283">Mobiililaitteen valikon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-283">Set up the mobile device menu</span></span>

<span data-ttu-id="b8e8b-284">Uudet valikkovaihtoehdot on nyt lisättävä mobiililaitteen valikkoon.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="b8e8b-285">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="b8e8b-286">Valitse **Lähtevä** -valikko.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="b8e8b-287">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b8e8b-288">Etsi ja valitse **Kuormalavan luonti** **Käytettävissä olevat valikot ja valikkovaihtoehdot** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="b8e8b-289">Siirrä **Kuormalavan luonti** oikealla nuolipainikkeella **Valikon rakenne** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="b8e8b-290">Siirrä **Kuormalavan luonti** -valikkovaihtoehto ylä- ja alanuolipainikkeilla sopivaan paikkaan mobiililaitteen valikossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="b8e8b-291">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-291">Select **Save**.</span></span>
1. <span data-ttu-id="b8e8b-292">Lisää **Kuormaus lajittelusta** -valikkovaihtoehto **Lähtevät** -valikkoon vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="b8e8b-293">Määritä sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="b8e8b-293">Set up location directives</span></span>

<span data-ttu-id="b8e8b-294">*Sijaintidirektiivit* ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="b8e8b-295">Nyt on luotava sääntö, jolla lajittelutyötä hallitaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="b8e8b-296">Yhden varastointiyksikön direktiivin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="b8e8b-297">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b8e8b-298">Muuta vasemmassa ruudussa **Työtilauksen tyyppi** -kentän arvoksi *Lajiteltu varastokeräily*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="b8e8b-299">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-300">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-301">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b8e8b-302">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="b8e8b-303">Määritä **Sijaintidirektiivit** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-304">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b8e8b-305">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-305">**Site:** *6*</span></span>
    - <span data-ttu-id="b8e8b-306">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-307">**Useita varastointiyksiköitä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="b8e8b-308">Valitsemalla **Tallenna** voit ottaa **Rivit** -pikavälilehden työkalurivin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b8e8b-309">Valitse **Rivit** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-309">On the **Lines** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="b8e8b-310">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b8e8b-311">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b8e8b-312">**Alku:** *0*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-312">**From:** *0*</span></span>
    - <span data-ttu-id="b8e8b-313">**Loppu:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="b8e8b-314">Valitsemalla **Tallenna** voit ottaa **Sijaintidirektiivitoiminnot** -pikavälilehden työkalurivin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b8e8b-315">Valitse **Sijaintidirektiivitoiminnot** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-315">On the **Location Directive Actions** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="b8e8b-316">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b8e8b-317">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b8e8b-318">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="b8e8b-319">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-319">Select **Save**.</span></span>
1. <span data-ttu-id="b8e8b-320">Valitse **Sijaintidirektiivitoiminnot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="b8e8b-321">Etsi kyselyeditoriin **Alue** -välilehdessä rivi, jonka **Kenttä** -kentän asetuksena on *Sijainti*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="b8e8b-322">Määritä tämän rivin **Ehdot** -kentän arvoksi *Lastauspaikan ovi*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="b8e8b-323">Tallenna asetukset valitsemalla **OK** ja sulje kyselyeditori.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="b8e8b-324">Usean varastointiyksikön direktiivin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="b8e8b-325">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b8e8b-326">Muuta vasemmassa ruudussa **Työtilauksen tyyppi** -kentän arvoksi *Lajiteltu varastokeräily*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="b8e8b-327">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-328">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-329">**Järjestys:** *2*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="b8e8b-330">**Nimi:** *Monta lastausovea*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="b8e8b-331">Määritä **Sijaintidirektiivit** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-332">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b8e8b-333">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-333">**Site:** *6*</span></span>
    - <span data-ttu-id="b8e8b-334">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-335">**Useita varastointiyksiköitä:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="b8e8b-336">Valitsemalla **Tallenna** voit ottaa **Rivit** -pikavälilehden työkalurivin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b8e8b-337">Valitse **Rivit** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-337">On the **Lines** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="b8e8b-338">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b8e8b-339">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b8e8b-340">**Alku:** *0*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-340">**From:** *0*</span></span>
    - <span data-ttu-id="b8e8b-341">**Loppu:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="b8e8b-342">Valitsemalla **Tallenna** voit ottaa **Sijaintidirektiivitoiminnot** -pikavälilehden työkalurivin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b8e8b-343">Valitse **Sijaintidirektiivitoiminnot** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-343">On the **Location Directive Actions** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="b8e8b-344">Hyväksy kaikkien muiden kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b8e8b-345">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b8e8b-346">**Nimi:** *Monta lastausovea*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="b8e8b-347">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-347">Select **Save**.</span></span>
1. <span data-ttu-id="b8e8b-348">Valitse **Sijaintidirektiivitoiminnot** -pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="b8e8b-349">Etsi kyselyeditoriin **Alue** -välilehdessä rivi, jonka **Kenttä** -kentän asetuksena on *Sijainti*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="b8e8b-350">Määritä tämän rivin **Ehdot** -kentän arvoksi *Lastauspaikan ovi*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="b8e8b-351">Tallenna asetukset valitsemalla **OK** ja sulje kyselyeditori.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="b8e8b-352">Määritä työmallit</span><span class="sxs-lookup"><span data-stu-id="b8e8b-352">Set up work templates</span></span>

1. <span data-ttu-id="b8e8b-353">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b8e8b-354">Muuta **Työtilauksen tyyppi** -kentän arvoksi *Lajiteltu varastokeräily*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="b8e8b-355">Valitse toimintoruudussa **Uusi** ja luo työmalli.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="b8e8b-356">Määritä **Yleiskatsaus** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-357">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b8e8b-358">**Työmalli:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="b8e8b-359">**Työmallin kuvaus:** *Lajittelu*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="b8e8b-360">Valitse **Tallenna** , jos haluat, että **Työmallin tiedot** -pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b8e8b-361">Lisää rivi valitsemalla **Työmallin tiedot** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-362">**Työtyyppi:** *Poiminta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b8e8b-363">**Työluokan tunnus:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="b8e8b-364">Lisää toinen rivi valitsemalla **Uusi** uudelleen ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="b8e8b-365">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b8e8b-366">**Työluokan tunnus:** *LAJITTELU*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="b8e8b-367">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b8e8b-368">Skenaario</span><span class="sxs-lookup"><span data-stu-id="b8e8b-368">Scenario</span></span>

<span data-ttu-id="b8e8b-369">Tämä skenaario simuloi tilannetta, jossa pakatut kontit on lajiteltava pakkausaseman jälkeen automaattisesti eri paikkoihin (kuormalavoille) rahdinkuljetuspalvelun mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="b8e8b-370">Kun kaikki kuorman nimikkeet on pakattu ja lajiteltu osoitteen mukaan, kuormalavat siirretään lastausovelle.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="b8e8b-371">Myyntitilausten ja keräystyön luominen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="b8e8b-372">Luo myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="b8e8b-372">Create sales order 1</span></span>

1. <span data-ttu-id="b8e8b-373">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b8e8b-374">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-375">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-376">**Asiakastili:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="b8e8b-377">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b8e8b-378">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="b8e8b-379">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="b8e8b-380">Vaihda **Otsikko** -näkymään.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b8e8b-381">Määritä **Toimitus** -pikavälilehden **Kuljetus** -osassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-382">**Rahdinkuljettaja:** *Lentorahti*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="b8e8b-383">**Rahdinkuljetuspalvelu:** *Ilma*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="b8e8b-384">Siirry **Rivit** -näkymään.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="b8e8b-385">Jos uutta tyhjää riviä ei lisätä automaattisesti ruudukkoon, lisää se valitsemalla **Myyntitilausrivit** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="b8e8b-386">Määritä seuraavat arvot uudella tilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-387">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b8e8b-388">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b8e8b-389">Kun uusi rivi on edelleen valittuna **Myyntitilausrivit** -pikavälilehdessä, valitse ruudukon yläpuolella olevassa **Varasto** -valikossa **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b8e8b-390">Valitse **Varaus** -sivulla **Varaa erä** , jos haluat varata valitun rivin koko määrän varastossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b8e8b-391">Palaa myyntitilaukseen sulkemalla **Varaus** -sivun.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b8e8b-392">Valitse toimintoruudussa **Varasto** -välilehden **Toiminnot** -ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b8e8b-393">Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b8e8b-394">Kirjoita muistiin aallon ja lähetyksen tunnusnumerot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="b8e8b-395">Myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="b8e8b-395">Sales order 2</span></span>

1. <span data-ttu-id="b8e8b-396">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b8e8b-397">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b8e8b-398">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-399">**Asiakastili:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="b8e8b-400">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b8e8b-401">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="b8e8b-402">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-402">The new sales order is opened.</span></span> <span data-ttu-id="b8e8b-403">**Myyntitilausrivit** -pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b8e8b-404">Määritä seuraavat arvot kyseisellä tilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="b8e8b-405">**Nimike:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="b8e8b-406">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b8e8b-407">Määritä **Rivitiedot** -pikavälilehden **Toimitus** -välilehden **Toimitustapa** -kentän arvoksi *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="b8e8b-408">Valitse **Myyntitilausrivit** -pikavälilehdessä **Lisää rivi** ja määritä sitten seuraavat arvot toisella tilausrivillä:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-408">On the **Sales order lines** FastTab, select **Add line** , and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="b8e8b-409">**Nimike:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="b8e8b-410">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b8e8b-411">Vaihda **Rivitiedot** -pikavälilehden **Toimitus** -välilehden **Toimitustapa** -kentän arvoksi *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="b8e8b-412">Valitse ensimmäinen tilausrivi **Myyntitilausrivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="b8e8b-413">Valitse sitten ruudukon yläpuolella olevassa **Varasto** -valikossa **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b8e8b-414">Valitse **Varaus** -sivulla **Varaa erä** , jos haluat varata valitun rivin koko määrän varastossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b8e8b-415">Palaa myyntitilaukseen sulkemalla **Varaus** -sivun.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b8e8b-416">Valitse toinen tilausrivi **Myyntitilausrivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="b8e8b-417">Valitse sitten ruudukon yläpuolella olevassa **Varasto** -valikossa **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b8e8b-418">Valitse **Varaus** -sivulla **Varaa erä** , jos haluat varata valitun rivin koko määrän varastossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b8e8b-419">Palaa myyntitilaukseen sulkemalla **Varaus** -sivun.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b8e8b-420">Valitse toimintoruudussa **Varasto** -välilehden **Toiminnot** -ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b8e8b-421">Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b8e8b-422">Näet, että kaksi aallon tunnuslukua ja kaksi lähetyksen tunnuslukua on luotu; yksi kummallekin myyntitilausrivien toimitustavalle.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="b8e8b-423">Työtunnusten hakeminen työn tiedoista</span><span class="sxs-lookup"><span data-stu-id="b8e8b-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="b8e8b-424">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b8e8b-425">-Sivulla näkyvät työtunnukset, jotka on luotu myynti tilauksista.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="b8e8b-426">Etsi kummankin aallon ja lähetyksen työtunnus käyttämällä luotujen myyntitilausten aallon ja lähetyksen tunnuksia.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="b8e8b-427">Kirjoita nämä työtunnukset muistiin, sillä niitä tarvitaan seuraavissa vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="b8e8b-428">Näet, että toiselle myyntitilaukselle luotiin kaksi työtunnusta.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="b8e8b-429">Erilliset työtunnukset luodaan, jos eri sijainneista kerätään eri nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="b8e8b-430">Nimikkeiden keräily myyntitilauksia varten</span><span class="sxs-lookup"><span data-stu-id="b8e8b-430">Pick items for the sales orders</span></span>

<span data-ttu-id="b8e8b-431">Tee luotu työ loppuun siirtämällä nimikkeet pakkausasemalle mobiililaitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="b8e8b-432">Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).</span><span class="sxs-lookup"><span data-stu-id="b8e8b-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b8e8b-433">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b8e8b-434">Valitse **Lähtevä** -valikossa **Myynnin keräily**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="b8e8b-435">Anna **Tunnus** -kenttään myyntitilaukselle 1 luotu työtunnus.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="b8e8b-436">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-436">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-437">Anna **Myyntitilaukset – keräily** -sivulla myyntitilaukselle 1 luotu kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="b8e8b-438">Huomaa, että keräilysijainti ( *joukko-001* ), nimike ( *A0001* ) ja määrä ( *2 kpl* ) ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-438">Notice that the picking location ( *bulk-001* ), item ( *A0001* ), and quantity ( *2 pcs* ) are shown.</span></span>
1. <span data-ttu-id="b8e8b-439">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-439">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-440">Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="b8e8b-441">**Sijainti** -kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *Pakkaus* -sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="b8e8b-442">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-442">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-443">**Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma, joka ilmaisee, myyntitilauksen 1 työtunnus on valmistunut.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="b8e8b-444">Seuraavaksi kerätään myyntitilaus 2.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="b8e8b-445">Anna **Tunnus** -kenttään työtunnus, joka luotiin myyntitilaukselle 2 ja jossa rivillä 1 on nimike *A0001*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="b8e8b-446">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-446">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-447">Anna **Myyntilaukset – keräily** -sivulla kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="b8e8b-448">Huomaa, että keräilysijainti ( *joukko-001* ), nimike ( *A0001* ) ja määrä ( *1 kpl* ) ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-448">Notice that the picking location ( *bulk-001* ), item ( *A0001* ), and quantity ( *1 pcs* ) are shown.</span></span>
1. <span data-ttu-id="b8e8b-449">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-449">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-450">Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="b8e8b-451">**Sijainti** -kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *Pakkaus* -sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="b8e8b-452">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-452">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-453">**Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b8e8b-454">Sanoma ilmaisee, että myyntilauksen 2 rivin 1 työtunnus on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="b8e8b-455">Anna **Tunnus** -kenttään työtunnus, joka luotiin myyntitilaukselle 2 ja jossa rivillä 2 on nimike *A0002*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="b8e8b-456">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-456">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-457">Anna **Myyntilaukset – keräily** -sivulla kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="b8e8b-458">Huomaa, että keräilysijainti ( *joukko-002* ), nimike ( *A0001* ) ja määrä ( *1 kpl* ) ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-458">Notice that the picking location ( *bulk-002* ), item ( *A0001* ), and quantity ( *1 pcs* ) are shown.</span></span>
1. <span data-ttu-id="b8e8b-459">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-459">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-460">Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="b8e8b-461">**Sijainti** -kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *Pakkaus* -sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="b8e8b-462">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-462">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-463">**Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b8e8b-464">Sanoma ilmaisee, että myyntilauksen 2 rivin 2 työtunnus on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="b8e8b-465">Myyntitilausten pakkaaminen kontteihin</span><span class="sxs-lookup"><span data-stu-id="b8e8b-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="b8e8b-466">Myyntitilauksen 1 pakkaaminen kontteihin</span><span class="sxs-lookup"><span data-stu-id="b8e8b-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="b8e8b-467">Valitse **Varastoinhallinta \> Pakkaus ja konttiinpakkaus \> Pakkaus**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="b8e8b-468">**Valitse pakkausasema** -valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="b8e8b-469">**Työntekijä** -kentässä pitäisi oletusarvoisesti olla aiemmin määritetyn työntekijän nimi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="b8e8b-470">Määritä seuraavat arvot tiettyyn pakkaussijaintiin suunniteltujen lähetysten ja konttien tarkastelua ja käsittelyä varten:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="b8e8b-471">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-471">**Site:** *6*</span></span>
    - <span data-ttu-id="b8e8b-472">**Varasto** : *62*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b8e8b-473">**Sijainti:** *Pakkaus*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="b8e8b-474">**Pakkausprofiilin tunnus:** *Lajitteli*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="b8e8b-475">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="b8e8b-476">Anna **Pakkaus** -sivun **Rekisterikilpi tai lähetys** -kenttään myyntitilauksen 1 kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="b8e8b-477">Siirry sitten kentästä pois painamalla **Sarkain** - tai **Enter** -näppäintä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="b8e8b-478">Valitse toimintoruudussa **Uusi kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b8e8b-479">Hyväksy kaikki oletusasetukset ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b8e8b-480">Kirjoita kontin tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b8e8b-481">Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-482">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b8e8b-483">**Tunniste:** nimike *A0001*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="b8e8b-484">Valitse toimintoruudussa **Sulje kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b8e8b-485">Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino** , jolloin järjestelmä päivittää **Bruttopaino** -kentän.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b8e8b-486">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-486">Select **OK**.</span></span> <span data-ttu-id="b8e8b-487">Kontti siirretään *LAJITTELU* -sijaintiin ja on valmis lajiteltavaksi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="b8e8b-488">Lisää toinen myyntilauksen 1 rekisterikilven nimike uuteen konttiin luomalla toinen kontti.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="b8e8b-489">Valitse toimintoruudussa **Uusi kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b8e8b-490">Hyväksy kaikki oletusasetukset ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b8e8b-491">Kirjoita kontin tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b8e8b-492">Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-493">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b8e8b-494">**Tunniste:** nimike *A0001*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="b8e8b-495">Valitse toimintoruudussa **Sulje kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b8e8b-496">Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino** , jolloin järjestelmä päivittää **Bruttopaino** -kentän.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b8e8b-497">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-497">Select **OK**.</span></span> <span data-ttu-id="b8e8b-498">Kontti siirretään *LAJITTELU* -sijaintiin ja on valmis lajiteltavaksi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="b8e8b-499">Myyntitilauksen 2 pakkaaminen kontteihin</span><span class="sxs-lookup"><span data-stu-id="b8e8b-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="b8e8b-500">Anna **Pakkaus** -sivun **Rekisterikilpi tai lähetys** -kenttään myyntitilauksen 2 rivin 1 kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="b8e8b-501">Siirry sitten kentästä pois painamalla **Sarkain** - tai **Enter** -näppäintä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="b8e8b-502">Valitse toimintoruudussa **Uusi kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b8e8b-503">Hyväksy kaikki oletusasetukset ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b8e8b-504">Kirjoita kontin tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b8e8b-505">Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-506">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b8e8b-507">**Tunniste:** nimike *A0001*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="b8e8b-508">Valitse toimintoruudussa **Sulje kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b8e8b-509">Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino** , jolloin järjestelmä päivittää **Bruttopaino** -kentän.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b8e8b-510">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-510">Select **OK**.</span></span> <span data-ttu-id="b8e8b-511">Kontti siirretään *LAJITTELU* -sijaintiin ja on valmis lajiteltavaksi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="b8e8b-512">**Rekisterikilpi tai lähetys** -kenttään myyntitilauksen 2 rivin 2 kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="b8e8b-513">Siirry sitten kentästä pois painamalla **Sarkain** - tai **Enter** -näppäintä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="b8e8b-514">Valitse toimintoruudussa **Uusi kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b8e8b-515">Hyväksy kaikki oletusasetukset ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b8e8b-516">Kirjoita kontin tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b8e8b-517">Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b8e8b-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b8e8b-518">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b8e8b-519">**Tunnistekenttä:** nimike *A0002*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="b8e8b-520">Valitse toimintoruudussa **Sulje kontti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b8e8b-521">Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino** , jolloin järjestelmä päivittää **Bruttopaino** -kentän.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b8e8b-522">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-522">Select **OK**.</span></span> <span data-ttu-id="b8e8b-523">Kontti siirretään *LAJITTELU* -sijaintiin ja on valmis lajiteltavaksi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="b8e8b-524">Voit tarkastella kontin tietoja valitsemalla **Varastonhallinta \> Pakkaus ja konttiinpakkaus \> Kontit** ja hakemalla pakkauksen aikana luodut konttitunnukset.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers** , and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="b8e8b-525">Konttien lajittelu</span><span class="sxs-lookup"><span data-stu-id="b8e8b-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8e8b-526">Kun teet lähtevän lajittelun käyttämällä **Kuormalavan luonti** -valikkovaihtoehtoa mobiilisovelluksessa, näkyviin tulee **Täysi** -painike.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="b8e8b-527">*Älä käytä **Täysi** -painiketta lajittelun tai paikan sulkemiseen.*</span><span class="sxs-lookup"><span data-stu-id="b8e8b-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="b8e8b-528">**Täysi** -painike on oletusarvo eikä sitä voi poistaa käytöstä tai poistaa sivulta.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="b8e8b-529">Sitä ei käytetä *Lähtevä lajittelu* -toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="b8e8b-530">Ensimmäisen kontin lajittelu</span><span class="sxs-lookup"><span data-stu-id="b8e8b-530">Sort the first container</span></span>

1. <span data-ttu-id="b8e8b-531">Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).</span><span class="sxs-lookup"><span data-stu-id="b8e8b-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b8e8b-532">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b8e8b-533">Valitse **Lähtevä** -valikossa **Kuormalavan luonti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="b8e8b-534">Anna **Rekisterikilpi/kontti** -kenttään myyntilaukseen 1 liitetyn ensimmäisen kontin tunnus.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="b8e8b-535">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-535">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-536">Koska lajittelua ei tällä hetkellä ole, sellainen on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="b8e8b-537">Anna **Lajittelupaikan tunnus** -kenttään *SP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="b8e8b-538">Koska lajittelupaikkaan *SP01* ei ole tällä hetkellä liitetty rekisterikilpeä, se on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-538">Because no LP is currently associated with sort position *SP01* , you must specify one.</span></span> <span data-ttu-id="b8e8b-539">Anna **RK** -kentässä *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="b8e8b-540">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-540">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-541">Koska lajittelupaikan vahvistus on otettu käyttöön, lajittelupaikan tunnus on annettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="b8e8b-542">Anna **Lajittelupaikan tunnus** -kenttään *SP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="b8e8b-543">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-543">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-544">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="b8e8b-545">Voit tarkastella lajittelupaikkaa ja siinä oleva rekisterikilpeä valitsemalla **Varastohallinta \> Pakkaus ja konttiinpakkaus \> Lähtevän lajittelupaikan määritykset**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="b8e8b-546">**Lähtevän lajittelupaikan määritykset** -sivulla näkyy kaikki tällä hetkellä aktiivisena olevat lajittelupaikat.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="b8e8b-547">**Lajittelupaikan tapahtumat** -kentässä näkyy rekisterikilpi, joka on liitetty kuhunkin lajittelupaikkaan ja lajittelupaikassa oleviin kontteihin.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="b8e8b-548">Huomaa, että yksi lajittelupaikka on luotu jo aiemmin ja että **Sijainnin lajitteluehdot** -pikavälilehdessä on **Lähetys – rahdinkuljettaja – ilma** -kohdan ehdot.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="b8e8b-549">Jäljellä olevien konttien lajittelu</span><span class="sxs-lookup"><span data-stu-id="b8e8b-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="b8e8b-550">Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).</span><span class="sxs-lookup"><span data-stu-id="b8e8b-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b8e8b-551">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b8e8b-552">Valitse **Lähtevä** -valikossa **Kuormalavan luonti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="b8e8b-553">Anna **Rekisterikilpi/kontti** -kenttään myyntilaukseen 1 liitetyn toisen kontin tunnus.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="b8e8b-554">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-554">Select **OK**.</span></span> <span data-ttu-id="b8e8b-555">Koska lajittelumalli on määritetty tekemään lajittelu automaattisesti ja olemassa on ehdot täyttävä lajittelupaikka, ohjaus oikeaan lajittelupaikkaan tehdään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="b8e8b-556">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-556">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-557">Lajittelupaikan tunnuksen vahvistaminen osoittaa, että varasto on oikeassa paikassa.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="b8e8b-558">Anna **Lajittelupaikan tunnus** -kenttään *SP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="b8e8b-559">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-559">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-560">Myyntitilauksen 1 toisen kontin työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="b8e8b-561">Seuraavaksi lajitellaan myyntitilauksen 2 jäljellä olevat kontit.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="b8e8b-562">Anna **Rekisterikilpi/kontti** -kentässä sen myyntitilauksen 2 kontin konttitunnus, jossa nimike *A0001* on.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="b8e8b-563">Koska rahdinkuljettaja ei ole sama, sinua pyydetään antamaan uusi lajittelupaikka ja määrittämään rekisterikilpi kyseiseen paikkaan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="b8e8b-564">Käytä lajittelupaikkaa *SP02* ja rekisterikilpeä *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="b8e8b-565">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-565">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-566">Vahvista lajittelupaikka antamalla *SP02* **Lajittelupaikan tunnus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="b8e8b-567">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-567">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-568">Kontin työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="b8e8b-569">Anna **Rekisterikilpi/kontti** -kentässä sen myyntitilauksen 2 jäljellä olevan kontin konttitunnus, jossa nimike *A0002* on.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="b8e8b-570">Koska rahdinkuljettaja on sama kuin myyntitilauksen 1 rahdinkuljettaja, järjestelmä näyttää aiemmin luodun ehdot täyttävän lajittelupaikan.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="b8e8b-571">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-571">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-572">Vahvista lajittelupaikka antamalla *SP01* **Lajittelupaikan tunnus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="b8e8b-573">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-573">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-574">Kontin työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="b8e8b-575">Lähtevien lajittelupaikkojen sulkeminen</span><span class="sxs-lookup"><span data-stu-id="b8e8b-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="b8e8b-576">Kun koko varasto on lajiteltu, työtä ei voi luoda, ennen kuin paikka on suljettu.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="b8e8b-577">Lajitellun varaston keräilytyö luodaan siirtämään varasto lastausovelle.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="b8e8b-578">Paikan sulkeminen mobiililaitteessa</span><span class="sxs-lookup"><span data-stu-id="b8e8b-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="b8e8b-579">Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).</span><span class="sxs-lookup"><span data-stu-id="b8e8b-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b8e8b-580">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b8e8b-581">Valitse **Lähtevä** -valikossa **Kuormalavan luonti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="b8e8b-582">Anna **Rekisterikilpi/kontti** -kentässä sen kontin tunnus, joka lajiteltiin lajittelupaikkaan *SP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="b8e8b-583">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-583">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-584">Näyttöön avautuvan sanoman mukaan kontti on jo lajiteltu paikkaan SP01.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="b8e8b-585">Suljetaanko sijainti?</span><span class="sxs-lookup"><span data-stu-id="b8e8b-585">Close the position?"</span></span> <span data-ttu-id="b8e8b-586">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-586">Select **Close**.</span></span>

    <span data-ttu-id="b8e8b-587">Työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="b8e8b-588">Paikan sulkeminen lähtevän lajittelupaikan määrityksistä</span><span class="sxs-lookup"><span data-stu-id="b8e8b-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="b8e8b-589">Valitse **Varastohallinta \> Pakkaus ja konttiinpakkaus \> Lähtevän lajittelupaikan määritykset**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="b8e8b-590">Valitse vasemmasta sarakkeessa **SP02**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="b8e8b-591">Tämä lähtevä lajittelupaikan rivi on suljettava rivi.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="b8e8b-592">Valitse toimintoruudussa **Sulje sijainti**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="b8e8b-593">Lajittelusijaintitietue suljetaan, eikä se enää ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="b8e8b-594">Voit näyttää kaikki suljetut sijaintitietueet valitsemalla **Näytä suljetut** -valintaruudun.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="b8e8b-595">Lajiteltu varaston keräily</span><span class="sxs-lookup"><span data-stu-id="b8e8b-595">Sorted inventory picking</span></span>

<span data-ttu-id="b8e8b-596">Lajitellun varaston keräilytyö on suoritettava loppuun.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="b8e8b-597">Kun se on valmis, varasto kerätään myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="b8e8b-598">Tässä vaiheessa käytetään kaikki muita varastoprosesseja.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="b8e8b-599">Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).</span><span class="sxs-lookup"><span data-stu-id="b8e8b-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b8e8b-600">Valitse päävalikossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b8e8b-601">Valitse **Lähtevä** -valikossa **Kuormaus lajitellusta**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="b8e8b-602">Anna kohderekisterikilven tunnus ensimmäisestä lajittelusijainnista *SP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="b8e8b-603">Määritä **Tunnus** -kentän arvoksi *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="b8e8b-604">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-604">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-605">**Lajitellun varaston keräily: keräys** -sivulla näkyy tehtävä keräilytyö.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="b8e8b-606">Tee keräys *LAJITTELU* -sijainnista ja kohderekisterikilvestä *PLP01* , jossa on useita nimikkeitä ja jonka määrä on *3*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-606">Pick from the *SORT* location and target LP *PLP01* , which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="b8e8b-607">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-607">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-608">**Lajitellun varaston keräily: poispano** -sivulla näkyy tehtävä poispanotyö.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="b8e8b-609">Tee poispano *Lastausovi* -sijaintiin ja kohderekisterikilpeen *PLP01* , jossa on useita nimikkeitä ja jonka määrä on *3*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-609">Put to the *Baydoor* location and target LP *PLP01* , which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="b8e8b-610">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-610">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-611">Työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-611">Work is completed.</span></span>

1. <span data-ttu-id="b8e8b-612">Anna kohderekisterikilven tunnus toisesta lajittelusijainnista *SP02*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="b8e8b-613">Määritä **Tunnus** -kentän arvoksi *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="b8e8b-614">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-614">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-615">**Lajitellun varaston keräily: keräys** -sivulla näkyy tehtävä keräilytyö.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="b8e8b-616">Tee keräys *LAJITTELU* -sijainnista ja kohderekisterikilvestä *PLP02* , jossa on useita nimikkeitä ja jonka määrä on *1*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-616">Pick from the *SORT* location and target LP *PLP02* , which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="b8e8b-617">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-617">Select **OK**.</span></span>
1. <span data-ttu-id="b8e8b-618">**Lajitellun varaston keräily: poispano** -sivulla näkyy tehtävä poispanotyö.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="b8e8b-619">Tee poispano *Lastausovi* -sijaintiin ja kohderekisterikilpeen *PLP02* , jossa on useita nimikkeitä ja jonka määrä on *1*.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-619">Put to the *Baydoor* location and target LP *PLP02* , which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="b8e8b-620">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-620">Select **OK**.</span></span>

    <span data-ttu-id="b8e8b-621">Työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-621">Work is completed.</span></span>

<span data-ttu-id="b8e8b-622">Tästä eteenpäin käytetään kaikki muita varastoprosesseja.</span><span class="sxs-lookup"><span data-stu-id="b8e8b-622">From this point forward, all other warehouse processes apply.</span></span>
