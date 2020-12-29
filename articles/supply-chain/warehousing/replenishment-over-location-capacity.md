---
title: Täydennys yli sijainnin kapasiteetin
description: Tässä ohjeaiheessa on tietoja Täydennys sijainnin kapasiteetilla -ominaisuudesta. Tämä ominaisuus ottaa käyttöön kaiken täydennystyön, joka vaaditaan luontipäivänä. Se myös hallitsee täydennystyön käytettävyyttä ja varmistaa näin, että varasto ei koskaan lopu keräilysijainnista eikä kapasiteettia ylitetä.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427463"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="288fe-104">Täydennys yli sijainnin kapasiteetin</span><span class="sxs-lookup"><span data-stu-id="288fe-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="288fe-105">Joidenkin määrältään suurten tai tilarajoitteisten varastojen on lähetettävä nimikettä suurempia määriä päivässä kuin keräilysijaintiin mahtuu.</span><span class="sxs-lookup"><span data-stu-id="288fe-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="288fe-106">*Täydennys sijainnin kapasiteetilla* -ominaisuus ottaa käyttöön kaiken täydennystyön, joka vaaditaan luontipäivänä. Se myös hallitsee täydennystyön käytettävyyttä ja varmistaa näin, että varasto ei koskaan lopu keräilysijainnista eikä kapasiteettia ylitetä.</span><span class="sxs-lookup"><span data-stu-id="288fe-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="288fe-107">Tämän ominaisuuden avulla on mahdollista luoda enemmän täydennystöitä kuin sijaintiin mahtuu. Tämä estää täydennystyön valmistumisen, kun sijainti on täynnä.</span><span class="sxs-lookup"><span data-stu-id="288fe-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="288fe-108">Kun keräilysijainnin varasto laskee alle määritetyn rajan, täydennystyötä määritetään lisää käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="288fe-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="288fe-109">Täydennystyö sijainnin kapasiteetilla -ominaisuuden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="288fe-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="288fe-110">Voit käyttää tätä ominaisuutta ottamalla seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (seuraavassa järjestyksessä):</span><span class="sxs-lookup"><span data-stu-id="288fe-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="288fe-111">Organisaation laajuinen työn esto</span><span class="sxs-lookup"><span data-stu-id="288fe-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="288fe-112">Täydennys yli sijainnin kapasiteetin</span><span class="sxs-lookup"><span data-stu-id="288fe-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="288fe-113">Määritä ominaisuus tälle esimerkkiskenaariolle</span><span class="sxs-lookup"><span data-stu-id="288fe-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="288fe-114">Tässä ohjeaiheessa on ohjeita ja esimerkki, jossa kerrotaan tämä ominaisuuden määrityksestä ja tässä ohjeaiheessa myöhemmin olevan esimerkkiskenaarion näytetietojen valmistelemisesta.</span><span class="sxs-lookup"><span data-stu-id="288fe-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="288fe-115">Mallitietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="288fe-115">Enable sample data</span></span>

<span data-ttu-id="288fe-116">[Esimerkkiskenaarion](#example-scenario) käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon [vakiodemotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="288fe-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="288fe-117">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="288fe-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="288fe-118">Sijaintiprofiili</span><span class="sxs-lookup"><span data-stu-id="288fe-118">Location profile</span></span>

<span data-ttu-id="288fe-119">Ota käyttöön Täydennys kapasiteetilla -ominaisuus sijaintiprofiilissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="288fe-120">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintien profiilit**.</span><span class="sxs-lookup"><span data-stu-id="288fe-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="288fe-121">Valitse vasemmasta ruudusta **POIMINTA-06**.</span><span class="sxs-lookup"><span data-stu-id="288fe-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="288fe-122">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="288fe-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="288fe-123">Määritä **Täydennys**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="288fe-124">**Ylittää sijaintikapasiteetin:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="288fe-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="288fe-125">Kun otettu käyttöön, täydennystyö saa ylittää sijainnin enimmäiskapasiteetin.</span><span class="sxs-lookup"><span data-stu-id="288fe-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="288fe-126">Tämä ottaa käyttöön myös muut **Täydennys**-pikavälilehden kentät.</span><span class="sxs-lookup"><span data-stu-id="288fe-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="288fe-127">**Työn käytettävyyden rajatyyppi:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="288fe-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="288fe-128">Tämä kenttä määrittää menetelmän, jota käytetään lisätyön vapauttamisen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="288fe-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="288fe-129">Vapautus voidaan tehdä määrän tai prosenttiosuuden mukaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="288fe-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="288fe-130">*Prosenttiosuus* – Valitse tämä vaihtoehto, jos haluat käyttää prosenttiosuuden kapasiteettia, joka perustuu varastointirajoituksiin tai tilavuustietoihin.</span><span class="sxs-lookup"><span data-stu-id="288fe-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="288fe-131">Tämän vaihtoehdon avulla voidaan ottaa käyttöön **Ylivuotoprosentti**-kenttä. Se poistaa käytöstä kaksi määrään liittyvää kenttää, jotka ovat **Ylivuotomäärä** ja **Ylivuotoyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="288fe-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="288fe-132">Voit käyttää tätä vaihtoehtoa, jos keräilysijainneissa on käytössä tilavuustiedot.</span><span class="sxs-lookup"><span data-stu-id="288fe-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="288fe-133">Jos tämä vaihtoehto on valittuna, määritä **Ylivuotoprosentti**-kentän arvoksi prosenttiluku, jonka yhteydessä määritetään lisää täydennystyötä käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="288fe-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="288fe-134">*Määrä* – Valitse tämä vaihtoehto, jos haluat käyttää tiettyä määräarvoa.</span><span class="sxs-lookup"><span data-stu-id="288fe-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="288fe-135">Tämän vaihtoehdon avulla poistaa käytöstä **Ylivuotoprosentti**-kenttä. Se ottaa käyttöön **Ylivuotomäärä**- ja **Ylivuotoyksikkö**-kentät.</span><span class="sxs-lookup"><span data-stu-id="288fe-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="288fe-136">Käytä tätä vaihtoehtoa, jos et käytä tilavuustietoja täydennettäville sijainneille, tai jos sinulla on yhdenmukaisia määriä, joista haluat tuoda lisää varastoa sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="288fe-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="288fe-137">Jos tämä vaihtoehto on valittuna, määritä sen määrän ja yksikön **Ylivuotomäärä**- ja **Ylivuotoyksikkö**-kentät, jolle määritetään lisää täydennystyötä käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="288fe-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="288fe-138">**Ylivuotomäärä:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="288fe-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="288fe-139">Tämä kenttä määrittää määrän, jolloin sijainnissa on ylivuoto.</span><span class="sxs-lookup"><span data-stu-id="288fe-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="288fe-140">Työ on käytettävissä aina, kun sijainnin varastosaldon ja työn määrien summa alittaa tämän arvon.</span><span class="sxs-lookup"><span data-stu-id="288fe-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="288fe-141">Mahdollinen täydennystyö, joka on yli tämän arvon, estetään, ja se on vapautettava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="288fe-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="288fe-142">Sijainnin varastointirajoitukset otetaan huomioon, kun työmäärää lasketaan.</span><span class="sxs-lookup"><span data-stu-id="288fe-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="288fe-143">**Ylivuotoyksikkö:** *KL*</span><span class="sxs-lookup"><span data-stu-id="288fe-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="288fe-144">Tässä kentässä määritetään ylivuotomäärään liittyvä yksikkö.</span><span class="sxs-lookup"><span data-stu-id="288fe-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="288fe-145">Tässä tapauksessa käytettävissä on enemmän täydennystyötä, kun sijainnissa on alle 0,65 kuormalavaa (KL).</span><span class="sxs-lookup"><span data-stu-id="288fe-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="288fe-146">**Ylivuotoprosentti**</span><span class="sxs-lookup"><span data-stu-id="288fe-146">**Overflow percentage**</span></span>

        <span data-ttu-id="288fe-147">Tämä kenttä määrittää prosenttiosuuden, jolloin sijainnissa on ylivuoto.</span><span class="sxs-lookup"><span data-stu-id="288fe-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="288fe-148">Työ on käytettävissä aina, kun sijainnin varastosaldon ja työn määrien summa alittaa tämän prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="288fe-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="288fe-149">Mahdollinen täydennystyön määräprosentti, joka on yli tämän arvon, estetään, ja se on vapautettava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="288fe-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="288fe-150">Sijainnin varastointirajoitukset otetaan huomioon, kun työmäärän prosenttiosuutta lasketaan.</span><span class="sxs-lookup"><span data-stu-id="288fe-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="288fe-151">Jos sijainnin varastointirajoituksia ei ole määritetty, työmääräprosentti lasketaan tilavuuden mukaan, jos tilavuusrajoitteita on määritetty sijaintiprofiilissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="288fe-152">Jos käytössä ovat **USMF**-yrityksen esittelytiedot ja aiemmin käyttöönotettu *Sijainnin rekisterikilven paikannus* -ominaisuus, poista **Ota käyttöön rekisterikilven paikannus** -asetus käytöstä **BULKKI-06**-sijaintiprofiilissa ja tee mobiilisovelluksen vaiheet valmiiksi esimerkkiskenaariossa.</span><span class="sxs-lookup"><span data-stu-id="288fe-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="288fe-153">Aallon vaihekoodi</span><span class="sxs-lookup"><span data-stu-id="288fe-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="288fe-154">Jos haluat määrittää aallon vaihekoodin tässä määritetyllä tavalla, ensin on ehkä käytettävä [ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja otettava käyttöön ominaisuus, jonka nimi on *Organisaationlaajuinen aallon vaihekoodi*.</span><span class="sxs-lookup"><span data-stu-id="288fe-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="288fe-155">Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**.</span><span class="sxs-lookup"><span data-stu-id="288fe-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="288fe-156">Valitse **Uusi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="288fe-157">**Aallon vaihekoodi:** *Täydennä*</span><span class="sxs-lookup"><span data-stu-id="288fe-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="288fe-158">**Aallon vaihekuvaus:** *Täydennys*</span><span class="sxs-lookup"><span data-stu-id="288fe-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="288fe-159">**Aalto vaihetyyppi:** *Täydennys*</span><span class="sxs-lookup"><span data-stu-id="288fe-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="288fe-160">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="288fe-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="288fe-161">Täydennysmalli</span><span class="sxs-lookup"><span data-stu-id="288fe-161">Replenishment template</span></span>

<span data-ttu-id="288fe-162">Täydennysmallit ovat sääntöjoukko, joka määrittää, milloin ja miten sijaintia täydennetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="288fe-163">Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit**.</span><span class="sxs-lookup"><span data-stu-id="288fe-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="288fe-164">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="288fe-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="288fe-165">Valitse **Yleiskatsaus**-osassa rivi, jolla **Täydennysmalli**-kentän arvoksi on määritetty *Vaadi täydennystä*.</span><span class="sxs-lookup"><span data-stu-id="288fe-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="288fe-166">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-166">Set the following values:</span></span>

    - <span data-ttu-id="288fe-167">**Aallon vaihekoodi:** *Täydennä*</span><span class="sxs-lookup"><span data-stu-id="288fe-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="288fe-168">**Salli aaltokysynnän käyttää varauksettoman määrän:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="288fe-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="288fe-169">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="288fe-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="288fe-170">Aaltomalli</span><span class="sxs-lookup"><span data-stu-id="288fe-170">Wave template</span></span>

1. <span data-ttu-id="288fe-171">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="288fe-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="288fe-172">Aseta vasemmassa ruudussa **Aaltomallityyppi**-kentän arvoksi *Lähetys*.</span><span class="sxs-lookup"><span data-stu-id="288fe-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="288fe-173">Valitse luettelosta **61 - lähetys** -malli.</span><span class="sxs-lookup"><span data-stu-id="288fe-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="288fe-174">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="288fe-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="288fe-175">Määritä **Yleiset**-pikavälilehden **Automatisoi täydennystyön vapautus** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="288fe-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="288fe-176">Jos määrität tämän vaihtoehdon arvoksi *Kyllä*, voit luoda täydennystyön tarpeen mukaan ja vapauttaa sen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="288fe-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="288fe-177">Sinun on lisättävä täydennyksen aaltomenetelmä aaltomalliin ja luotava täydennysmalli, jonka tyyppi on **Aallon kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="288fe-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="288fe-178">Määritä täydennysmalli **Täydennysmallit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="288fe-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="288fe-179">Jos haluat määrittää täydennysmallin, lisää täydennysmenetelmä aaltomalliin.</span><span class="sxs-lookup"><span data-stu-id="288fe-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="288fe-180">Etsi **Menetelmät**-välilehden **Valitut menetelmät**-sarakkeesta seuraava rivi:</span><span class="sxs-lookup"><span data-stu-id="288fe-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="288fe-181">**Menetelmän nimi:** *täydennä*</span><span class="sxs-lookup"><span data-stu-id="288fe-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="288fe-182">**Nimi:** *Täydennys*</span><span class="sxs-lookup"><span data-stu-id="288fe-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="288fe-183">Määritä **Aallon vaihekoodi** -kentän arvoksi tälle riville *Täydennä*.</span><span class="sxs-lookup"><span data-stu-id="288fe-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="288fe-184">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="288fe-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="288fe-185">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="288fe-185">Example scenario</span></span>

<span data-ttu-id="288fe-186">Kun olet tehnyt kaikki edellä mainitut näytetiedot käytettäviksi ja määrittänyt ne, voit käyttää tätä skenaariota ja kokeilla *Täydennys sijainnin kapasiteetilla* -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="288fe-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="288fe-187">Tämän skenaarion arvoissa oletetaan, että käsittelet vakionäytetietoja, valittuna on **USMF**-yritys ja että aiemmin tässä ohjeaiheessa kuvatut näytetietueet on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="288fe-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="288fe-188">Tämä skenaario on myös esimerkki siitä, miten ominaisuutta voidaan käyttää tuotannon määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="288fe-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="288fe-189">Luo täydennystyö</span><span class="sxs-lookup"><span data-stu-id="288fe-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="288fe-190">Luo myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="288fe-190">Create sales order 1</span></span>

1. <span data-ttu-id="288fe-191">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="288fe-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="288fe-192">Valitse toimintoruudussa **Uusi** ja avaa valintaikkuna luodaksesi uuden myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="288fe-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="288fe-193">Lisää valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="288fe-194">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="288fe-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="288fe-195">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="288fe-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="288fe-196">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="288fe-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="288fe-197">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="288fe-197">The new sales order is opened.</span></span> <span data-ttu-id="288fe-198">**Myyntitilausrivit**-pikavälilehti sisältää uuden, tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="288fe-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="288fe-199">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="288fe-200">**Nimiketunnus:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="288fe-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="288fe-201">**Määrä** *40*</span><span class="sxs-lookup"><span data-stu-id="288fe-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="288fe-202">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="288fe-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="288fe-203">Valitse **Varaus**-sivun kohta **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="288fe-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="288fe-204">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="288fe-204">Close the page.</span></span>
1. <span data-ttu-id="288fe-205">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="288fe-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="288fe-206">Näyttöön tulevat tietosanomat ilmaisevat luodun aallon ja lähetyksen tunnukset.</span><span class="sxs-lookup"><span data-stu-id="288fe-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="288fe-207">Myös täydennysaalto luodaan.</span><span class="sxs-lookup"><span data-stu-id="288fe-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="288fe-208">Näyttöön tulee myös seuraava varoitussanoma: "Työtä, jonka tunnus on XXXX, ei voi vapauttaa, koska sillä on keskeneräistä täydennystyötä.</span><span class="sxs-lookup"><span data-stu-id="288fe-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="288fe-209">Luo myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="288fe-209">Create sales order 2</span></span>

1. <span data-ttu-id="288fe-210">Valitse **Kaikki myyntitilaukset** -sivun toimintoruudussa **Uusi**, jos haluat avata valintaikkunan ja luoda uuden myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="288fe-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="288fe-211">Lisää valintaikkunassa seuraava arvo:</span><span class="sxs-lookup"><span data-stu-id="288fe-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="288fe-212">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="288fe-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="288fe-213">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="288fe-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="288fe-214">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="288fe-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="288fe-215">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="288fe-215">The new sales order is opened.</span></span> <span data-ttu-id="288fe-216">**Myyntitilausrivit**-pikavälilehti sisältää uuden, tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="288fe-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="288fe-217">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="288fe-218">**Nimiketunnus:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="288fe-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="288fe-219">**Määrä** *60*</span><span class="sxs-lookup"><span data-stu-id="288fe-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="288fe-220">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="288fe-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="288fe-221">Valitse **Varaus**-sivun kohta **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="288fe-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="288fe-222">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="288fe-222">Close the page.</span></span>
1. <span data-ttu-id="288fe-223">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="288fe-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="288fe-224">Näyttöön tulevat tietosanomat ilmaisevat luodun aallon ja lähetyksen tunnukset.</span><span class="sxs-lookup"><span data-stu-id="288fe-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="288fe-225">Myös täydennysaalto luodaan.</span><span class="sxs-lookup"><span data-stu-id="288fe-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="288fe-226">Näyttöön tulee myös seuraava varoitussanoma: "Työtä, jonka tunnus on XXXX, ei voi vapauttaa, koska sillä on keskeneräistä täydennystyötä.</span><span class="sxs-lookup"><span data-stu-id="288fe-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="288fe-227">Luo myyntitilaus 3</span><span class="sxs-lookup"><span data-stu-id="288fe-227">Create sales order 3</span></span>

1. <span data-ttu-id="288fe-228">Valitse **Kaikki myyntitilaukset** -sivun toimintoruudussa **Uusi**, jos haluat avata valintaikkunan ja luoda uuden myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="288fe-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="288fe-229">Lisää valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="288fe-230">**Asiakastili:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="288fe-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="288fe-231">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="288fe-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="288fe-232">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="288fe-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="288fe-233">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="288fe-233">The new sales order is opened.</span></span> <span data-ttu-id="288fe-234">**Myyntitilausrivit**-pikavälilehti sisältää uuden, tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="288fe-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="288fe-235">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="288fe-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="288fe-236">**Nimiketunnus:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="288fe-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="288fe-237">**Määrä** *30*</span><span class="sxs-lookup"><span data-stu-id="288fe-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="288fe-238">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="288fe-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="288fe-239">Valitse **Varaus**-sivun kohta **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="288fe-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="288fe-240">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="288fe-240">Close the page.</span></span>
1. <span data-ttu-id="288fe-241">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="288fe-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="288fe-242">Näyttöön tulevat tietosanomat ilmaisevat luodun aallon ja lähetyksen tunnukset.</span><span class="sxs-lookup"><span data-stu-id="288fe-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="288fe-243">Myös täydennysaalto luodaan.</span><span class="sxs-lookup"><span data-stu-id="288fe-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="288fe-244">Näyttöön tulee myös seuraava varoitussanoma: "Työtä, jonka tunnus on XXXX, ei voi vapauttaa, koska sillä on keskeneräistä täydennystyötä.</span><span class="sxs-lookup"><span data-stu-id="288fe-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="288fe-245">Näytä työn tiedot</span><span class="sxs-lookup"><span data-stu-id="288fe-245">View work details</span></span>

1. <span data-ttu-id="288fe-246">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="288fe-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="288fe-247">Suodata **Yleiskatsaus**-osassa **Varasto**-sarake varastolle *61*.</span><span class="sxs-lookup"><span data-stu-id="288fe-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="288fe-248">Näkyvissä pitäisi olla tieto siitä, että kolmelle kysynnän myyntitilaukselle luotiin seitsemän työtunnusta.</span><span class="sxs-lookup"><span data-stu-id="288fe-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="288fe-249">Kolmella seitsemästä työtunnuksesta on **Työtilaustyyppi**-kohdan arvona *Täydennys* ja neljällä **Työtilaustyyppi**-kohdan arvona *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="288fe-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="288fe-250">Kaikilla kolmella työtilauksella, joiden **Työtilaustyyppi**-kohdan arvo on *Täydennys*, on sama *keräily*- ja *hyllytyssijainti* **Rivit osassa**.</span><span class="sxs-lookup"><span data-stu-id="288fe-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="288fe-251">**Keräily:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="288fe-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="288fe-252">**Hyllytys:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="288fe-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="288fe-253">Myyntitilaukselle 1 on luotu kaksi työtunnusta.</span><span class="sxs-lookup"><span data-stu-id="288fe-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="288fe-254">Merkitse kaikkien myyntitilausten työtunnukset muistiin.</span><span class="sxs-lookup"><span data-stu-id="288fe-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="288fe-255">Käytettävissä olevista määristä riippuen luodut työmäärät voivat olla hieman erilaisia.</span><span class="sxs-lookup"><span data-stu-id="288fe-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="288fe-256">Yleisesti luotujen työotsikoiden tulisi kuitenkin vastata tämän skenaarion esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="288fe-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="288fe-257">Käytettävissä olevan varaston rekisterikilven tunnus</span><span class="sxs-lookup"><span data-stu-id="288fe-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="288fe-258">Myöhemmin tässä skenaariossa käytetään varastosovellusta (tai emulaattoria), jossa sinun on tunnistettava rekisterikilpi keräilyn ja täydennyksen skenaarioiden viimeistelemistä varten.</span><span class="sxs-lookup"><span data-stu-id="288fe-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="288fe-259">Voit etsiä myöhemmin tarvittavat rekisterikilven tunnukset alla olevien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="288fe-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="288fe-260">Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.</span><span class="sxs-lookup"><span data-stu-id="288fe-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="288fe-261">Avaa suodatinruutu valitsemalla **Näytä suodattimet** -painike.</span><span class="sxs-lookup"><span data-stu-id="288fe-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="288fe-262">Anna seuraavat suodatusehdot, jos haluat hakea skenaarion rekisterikilvet.</span><span class="sxs-lookup"><span data-stu-id="288fe-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="288fe-263">Käytä *alkaa*-suodatinta.</span><span class="sxs-lookup"><span data-stu-id="288fe-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="288fe-264">**Nimiketunnus:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="288fe-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="288fe-265">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="288fe-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="288fe-266">Valitse **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="288fe-266">Select **Apply**.</span></span>
1. <span data-ttu-id="288fe-267">Valitse toimintoruudussa **Dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="288fe-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="288fe-268">Valitse **Dimensioiden näyttö** -valintaruudussa **Tallennusdimensiot**-osassa kaikki arvot.</span><span class="sxs-lookup"><span data-stu-id="288fe-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="288fe-269">Valitse **Tapahtumat**-osassa **nimikenumeroksi** ja **määräksi \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="288fe-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="288fe-270">Kun olet valmis, sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="288fe-271">**Käytettävissä oleva** -ruudukossa on rekisterikilpien numerot nimikkeelle *T0100* kaikissa sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="288fe-272">Merkitse muistiin kussakin sijainnissa oleva rekisterikilpi, koska tarvitset näitä tietoja myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="288fe-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="288fe-273">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="288fe-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="288fe-274">Prosessivaiheet</span><span class="sxs-lookup"><span data-stu-id="288fe-274">Process steps</span></span>

<span data-ttu-id="288fe-275">Suorita varastosijainnin täydennys kahdelle ensimmäiselle työtunnukselle.</span><span class="sxs-lookup"><span data-stu-id="288fe-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="288fe-276">Kolmannen täydennystyön työ estetään siihen asti, kunnes varastotaso keräilysijainnissa on alle rajan.</span><span class="sxs-lookup"><span data-stu-id="288fe-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="288fe-277">Täydennys</span><span class="sxs-lookup"><span data-stu-id="288fe-277">Replenishment</span></span>

1. <span data-ttu-id="288fe-278">Kirjaudu varastosovellukseen käyttäjänä varastossa *61*.</span><span class="sxs-lookup"><span data-stu-id="288fe-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="288fe-279">(Anna käyttäjätunnukseksi *61* ja salasanaksi *1*.)</span><span class="sxs-lookup"><span data-stu-id="288fe-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="288fe-280">Siirry kohtaan **Varasto \> Täydennys**.</span><span class="sxs-lookup"><span data-stu-id="288fe-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="288fe-281">Sinua pyydetään suorittamaan ensimmäinen täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="288fe-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="288fe-282">Näkyvissä ovat nimiketunnus, määrä ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="288fe-283">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="288fe-284">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="288fe-285">Järjestelmä luo kohderekisterinumeron keräiltävän nimikkeen uudelle rekisterikilvelle.</span><span class="sxs-lookup"><span data-stu-id="288fe-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="288fe-286">Vahvista arvo valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="288fe-287">Näkyviin tulee työ, joka kehottaa käyttäjää asettamaan kohderekisterikilven täydennyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="288fe-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="288fe-288">*Keräilysijainnin* on oltava **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="288fe-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="288fe-289">Vahvista keräilyn tiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="288fe-290">Näyttöön tulee Työ valmis -sanoma ja seuraavan täydennyskeräilytehtävän tiedot: nimikenumero, määrä ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="288fe-291">Keräilysijainti on sama kuin ensimmäinen täydennyssijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="288fe-292">Tämän vuoksi rekisterikilvellä on sama rekisterikilven tunnus, jota käytettiin ensimmäisessä täydennystyötehtävässä.</span><span class="sxs-lookup"><span data-stu-id="288fe-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="288fe-293">Suorita toisen työtehtävän täydennystyöt toistamalla edellä kuvatut vaiheet.</span><span class="sxs-lookup"><span data-stu-id="288fe-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="288fe-294">Määrä- ja kohderekisterikilpi eroavat ensimmäisen työtehtävän määrä- ja kohderekisterikilvestä.</span><span class="sxs-lookup"><span data-stu-id="288fe-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="288fe-295">Kun toinen täydennystyö on valmis, näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="288fe-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="288fe-296">Mobiililaite ilmoittaa myös, jos työtä ei ole saatavissa, vaikka täydennystyötä olisi jäljellä.</span><span class="sxs-lookup"><span data-stu-id="288fe-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="288fe-297">Tämä johtuu siitä, että täydennystyön saatavuuden tila on *Pidossa* ja sen vuoksi se saa merkinnän **Estetty**.</span><span class="sxs-lookup"><span data-stu-id="288fe-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="288fe-298">*Pidossa*-tila käynnistettiin, koska sen keräilysijaintiin liitetyn työn sijaintiprofiilin **Ylivuotomäärä**-kohdan arvo on *0,65 KL*.</span><span class="sxs-lookup"><span data-stu-id="288fe-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="288fe-299">Kaksi edellistä täydennystyötehtävää täyttivät nimikkeen *T0100* lähes ylivuotorajaan asti.</span><span class="sxs-lookup"><span data-stu-id="288fe-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="288fe-300">(Nimikkeen yksikkömuunnos on *1 KL = 100 kpl*.) Tämän vuoksi jäljellä oleva täydennystyö voi aiheuttaa sijainnin ylivuotorajan ylityksen.</span><span class="sxs-lookup"><span data-stu-id="288fe-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="288fe-301">Tämä täydennystyö pysyy estettynä niin kauan, kunnes sijainnista kerätään tarpeeksi varastoa ja mobiililaitteen valikkovaihtoehdon työn vapautuksen raja alittuu.</span><span class="sxs-lookup"><span data-stu-id="288fe-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="288fe-302">Myyntitilauksen keräily</span><span class="sxs-lookup"><span data-stu-id="288fe-302">Sales order pick</span></span>

<span data-ttu-id="288fe-303">Ennen kuin jäljellä oleva täydennystyötehtävä voidaan viimeistellä, keräilysijainnin varaston tason on oltava niin alhainen, että jäljellä oleva täydennystyö voidaan vapauttaa.</span><span class="sxs-lookup"><span data-stu-id="288fe-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="288fe-304">Toisin sanoen käytettävissä olevan varaston kokonaismäärä sijainnissa ja täydennysmäärä eivät saa ylittää **ylivuotomäärän** arvoa.</span><span class="sxs-lookup"><span data-stu-id="288fe-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="288fe-305">Kun tämä summa on pienempi kuin ylivuotomäärä, jäljelle jäävä täydennystyö vapautetaan.</span><span class="sxs-lookup"><span data-stu-id="288fe-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="288fe-306">Kirjaudu varastosovellukseen käyttäjänä varastossa *61*.</span><span class="sxs-lookup"><span data-stu-id="288fe-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="288fe-307">(Anna käyttäjätunnukseksi *61* ja salasanaksi *1*.)</span><span class="sxs-lookup"><span data-stu-id="288fe-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="288fe-308">Siirry kohtaan **Lähtevät \> Myynnin keräily**.</span><span class="sxs-lookup"><span data-stu-id="288fe-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="288fe-309">Anna myyntitilauksen 1 ensimmäinen työtunnus.</span><span class="sxs-lookup"><span data-stu-id="288fe-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="288fe-310">Katso **Työn tiedot** -sivulta niiden myyntitilausten työtunnukset, jotka kirjoitit muistiin aiemmin.</span><span class="sxs-lookup"><span data-stu-id="288fe-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="288fe-311">Tässä annettava työtunnus luo keräilytyön 10 kappaleen määrälle kahdessa eri sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="288fe-312">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-312">Select **OK**.</span></span>

    <span data-ttu-id="288fe-313">**Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja ensimmäisen sijainnin keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="288fe-314">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="288fe-315">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="288fe-316">**Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja seuraavan sijainnin keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="288fe-317">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="288fe-318">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="288fe-319">**Myyntitilaukset: Hyllytys** -sivulla on ohjeita molempien valmiiden keräilytöiden hyllytyksestä lähtevien väliaikaiseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="288fe-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="288fe-320">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-320">Select **OK**.</span></span>

    <span data-ttu-id="288fe-321">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="288fe-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="288fe-322">Anna myyntitilauksen 1 toinen työtunnus.</span><span class="sxs-lookup"><span data-stu-id="288fe-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="288fe-323">Tällä työtunnuksella on vain yksi keräilytehtävä.</span><span class="sxs-lookup"><span data-stu-id="288fe-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="288fe-324">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-324">Select **OK**.</span></span>

    <span data-ttu-id="288fe-325">**Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="288fe-326">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="288fe-327">Määritettävä rekisterikilpi tulee olemaan eräs järjestelmän luomista rekisterikilvistä täydennystyötehtävissä.</span><span class="sxs-lookup"><span data-stu-id="288fe-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="288fe-328">Voit varmistaa, että tallennat oikean rekisterikilven tunnuksen, tarkistamalla varaston **Käytettävissä olevien luettelo** -sivulla nimikkeen, sijainnin ja määrän osalta.</span><span class="sxs-lookup"><span data-stu-id="288fe-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="288fe-329">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="288fe-330">Vahvista hyllytystehtävän ohjeet lähtevien väliaikaisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="288fe-331">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-331">Select **OK**.</span></span>

    <span data-ttu-id="288fe-332">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="288fe-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="288fe-333">Myyntitilauksen 2 keräily on estetty, koska linkitettyä täydennystyötä ei ole viimeistelty.</span><span class="sxs-lookup"><span data-stu-id="288fe-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="288fe-334">Tällä hetkellä keräilysijainnissa on yhä 30 kappaleen määrä, ja myyntitilauksen 2 täydennysmäärä on 60 kpl.</span><span class="sxs-lookup"><span data-stu-id="288fe-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="288fe-335">Käytettävissä olevan varaston summa ja täydennysvarasto (90 kpl) ylittää ylivuotomäärän 0,65 KL (tai 65 kpl).</span><span class="sxs-lookup"><span data-stu-id="288fe-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="288fe-336">Myyntitilaus 3 on keräiltävä, ennen kuin täydennystyö voidaan viimeistellä.</span><span class="sxs-lookup"><span data-stu-id="288fe-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="288fe-337">Anna myyntitilauksen 3 työtunnus.</span><span class="sxs-lookup"><span data-stu-id="288fe-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="288fe-338">Tällä työtunnuksella on vain yksi keräilytehtävä.</span><span class="sxs-lookup"><span data-stu-id="288fe-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="288fe-339">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-339">Select **OK**.</span></span>

    <span data-ttu-id="288fe-340">**Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="288fe-341">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="288fe-342">Määritettävä rekisterikilpi tulee olemaan eräs järjestelmän luomista rekisterikilvistä täydennystyötehtävissä.</span><span class="sxs-lookup"><span data-stu-id="288fe-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="288fe-343">Voit varmistaa, että tallennat oikean rekisterikilven tunnuksen, tarkistamalla varaston **Käytettävissä olevien luettelo** -sivulla nimikkeen, sijainnin ja määrän osalta.</span><span class="sxs-lookup"><span data-stu-id="288fe-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="288fe-344">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="288fe-345">Vahvista hyllytystehtävän ohjeet lähtevien väliaikaisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="288fe-346">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-346">Select **OK**.</span></span>

    <span data-ttu-id="288fe-347">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="288fe-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="288fe-348">Heti, kun käytettävissä olevan varaston summa keräilysijainnissa ja täydennysmäärä ovat alle rajan, voit käsitellä jäljellä olevan täydennystyön.</span><span class="sxs-lookup"><span data-stu-id="288fe-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="288fe-349">Palaa **Työn tiedot** -sivulla ja ota huomioon, että täydennystyön käytettävyys täydennyksen viimeisessä osassa (myyntitilaukselle 2) on *Avoin*, koska sijainnissa on nyt tarpeeksi tilaa täydennyksen hyväksymiseksi.</span><span class="sxs-lookup"><span data-stu-id="288fe-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="288fe-350">Voit nyt käsitellä täydennystyötä mobiililaitteen kautta.</span><span class="sxs-lookup"><span data-stu-id="288fe-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="288fe-351">Siirry kohtaan **Varasto \> Täydennys**.</span><span class="sxs-lookup"><span data-stu-id="288fe-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="288fe-352">Sinua pyydetään suorittamaan jäljellä oleva täydennystyö.</span><span class="sxs-lookup"><span data-stu-id="288fe-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="288fe-353">Näkyvissä ovat nimiketunnus, määrä ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="288fe-354">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="288fe-355">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="288fe-356">Järjestelmä luo kohderekisterinumeron keräiltävän nimikkeen uudelle rekisterikilvelle.</span><span class="sxs-lookup"><span data-stu-id="288fe-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="288fe-357">Vahvista arvo valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="288fe-358">Näkyviin tulee työ, joka kehottaa käyttäjää asettamaan kohderekisterikilven täydennyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="288fe-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="288fe-359">*Keräilysijainnin* on oltava **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="288fe-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="288fe-360">Vahvista keräilyn tiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="288fe-361">Näyttöön tulee Työ valmis- ja Työtä ei saatavissa -viestit.</span><span class="sxs-lookup"><span data-stu-id="288fe-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="288fe-362">Seuraavaksi voit kerätä myyntitilauksen 2.</span><span class="sxs-lookup"><span data-stu-id="288fe-362">You can now pick sales order 2.</span></span> <span data-ttu-id="288fe-363">Se vapautettiin, kun myyntitilaukseen linkitetty täydennystyö viimeisteltiin.</span><span class="sxs-lookup"><span data-stu-id="288fe-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="288fe-364">Anna myyntitilauksen 2 työtunnus.</span><span class="sxs-lookup"><span data-stu-id="288fe-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="288fe-365">Tällä työtunnuksella on vain yksi keräilytehtävä.</span><span class="sxs-lookup"><span data-stu-id="288fe-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="288fe-366">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-366">Select **OK**.</span></span>

    <span data-ttu-id="288fe-367">**Myyntitilaukset: Keräily** -tehtävän sivulla ovat nimikenumero, määrä ja keräilysijainti.</span><span class="sxs-lookup"><span data-stu-id="288fe-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="288fe-368">Anna **RK**-kenttään sen nimikkeen rekisterinumero, jonka sijainti näytetään.</span><span class="sxs-lookup"><span data-stu-id="288fe-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="288fe-369">Määritettävä rekisterikilpi tulee olemaan järjestelmän luoma rekisterikilpi täydennystyötehtävässä.</span><span class="sxs-lookup"><span data-stu-id="288fe-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="288fe-370">Voit varmistaa, että tallennat oikean rekisterikilven tunnuksen, tarkistamalla varaston **Käytettävissä olevien luettelo** -sivulla nimikkeen, sijainnin ja määrän osalta.</span><span class="sxs-lookup"><span data-stu-id="288fe-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="288fe-371">Valitse **OK**-painike (valintamerkkisymboli).</span><span class="sxs-lookup"><span data-stu-id="288fe-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="288fe-372">Vahvista hyllytystehtävän ohjeet lähtevien väliaikaisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="288fe-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="288fe-373">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="288fe-373">Select **OK**.</span></span>

    <span data-ttu-id="288fe-374">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="288fe-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="288fe-375">Huomautuksia ja vihjeitä</span><span class="sxs-lookup"><span data-stu-id="288fe-375">Notes and tips</span></span>

- <span data-ttu-id="288fe-376">Tätä toimintoa voi käyttää kaikissa täydennystyypeissä, esimerkiksi aallon kysynnässä, vähimmäis- tai enimmäistäydennyksessä, kuorman kysynnässä ja paikoituksessa.</span><span class="sxs-lookup"><span data-stu-id="288fe-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="288fe-377">Voit ohittaa halutessasi täydennystyön saatavuuden manuaalisesti jokaisen työotsikon kohdalla **Työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="288fe-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="288fe-378">Kun järjestelmä määrittää täydennystyön saatavuuden, se ottaa huomioon varaston, joka on jo sijainnissa ennen töiden valmistumista.</span><span class="sxs-lookup"><span data-stu-id="288fe-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="288fe-379">Jokainen myyntitilaustyö on linkitetty tiettyyn täydennystyöhön.</span><span class="sxs-lookup"><span data-stu-id="288fe-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="288fe-380">Vastaavaa myyntityön saatavuuden toimintoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="288fe-380">There is no corresponding sales work availability functionality.</span></span>
