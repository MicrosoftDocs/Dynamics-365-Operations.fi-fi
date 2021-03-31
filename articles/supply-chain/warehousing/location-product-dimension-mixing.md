---
title: Tuotedimensioiden yhdistäminen sijainnissa
description: Tässä ohjeaiheessa on tietoja tuotteiden useiden eri mittojen yhtäaikaisesta käytöstä samassa toimipaikassa. Tämä toimipaikkaprofiilin toiminto auttaa parantamaan toimipaikan varastonhallintaa, kun tuotteesta on varastossa useita variantteja tai tuotteiden ominaisuudet vaihtelevat, kuten muotiteollisuudessa. Sen avulla voit määrittää, voidaanko toimipaikkaprofiilissa sekoittaa tuotteita kokoonpanon, värin, tyylin ja värin mukaan vai voidaanko samassa toimipaikassa varastoida vain yhtä tietyn ominaisuuden tai ominaisuusyhdistelmän tuotetta.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b0309c7a7240d7cac9e5b5724a028f2dc70199e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217026"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="866bc-105">Tuotedimensioiden yhdistäminen sijainnissa</span><span class="sxs-lookup"><span data-stu-id="866bc-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="866bc-106">Tuotedimensioiden yhdistäminen sijainnissa on toimipaikkaprofiilin toiminto, joka auttaa parantamaan toimipaikan varastonhallintaa, kun tuotteesta on varastossa useita variantteja tai tuotteiden mitat vaihtelevat, kuten muotiteollisuudessa.</span><span class="sxs-lookup"><span data-stu-id="866bc-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="866bc-107">Sen avulla voit määrittää, voidaanko toimipaikkaprofiilissa sekoittaa tuotteita kokoonpanon, värin, tyylin ja värin mukaan vai voidaanko samassa toimipaikassa varastoida vain yhtä tietyn ominaisuuden tai ominaisuusyhdistelmän tuotetta.</span><span class="sxs-lookup"><span data-stu-id="866bc-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="866bc-108">Ota Tuotedimensioiden yhdistäminen sijainnissa käyttöön</span><span class="sxs-lookup"><span data-stu-id="866bc-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="866bc-109">Ennen kuin voit käyttää tuotedimensioiden sekoitusta, toiminnon pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="866bc-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="866bc-110">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="866bc-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="866bc-111">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="866bc-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="866bc-112">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="866bc-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="866bc-113">**Toiminnon nimi:** *Tuotedimensioiden yhdistäminen sijainnissa*</span><span class="sxs-lookup"><span data-stu-id="866bc-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="866bc-114">Määritys</span><span class="sxs-lookup"><span data-stu-id="866bc-114">Setup</span></span>

<span data-ttu-id="866bc-115">Jokaisella varastosijainnilla on oltava oma sijaintiprofiili, joka määrittää sijainnin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="866bc-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="866bc-116">Tämän vuoksi kaikissa samaa sijaintiprofiilia käyttävissä sijainneissa voidaan sallia tuotedimensioiden yhdistäminen, kun se on määritetty sijaintiprofiiliin.</span><span class="sxs-lookup"><span data-stu-id="866bc-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="866bc-117">Salli tuotedimensioiden yhdistäminen määrittämällä sijaintiprofiilit</span><span class="sxs-lookup"><span data-stu-id="866bc-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="866bc-118">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="866bc-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="866bc-119">Valitse sijaintiprofiilien luettelosta **BULKKI**.</span><span class="sxs-lookup"><span data-stu-id="866bc-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="866bc-120">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="866bc-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="866bc-121">Määritä **Yleinen**-pikavälilehdessä **Ota käyttöön tuotedimensioiden yhdistäminen sijainnissa** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="866bc-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="866bc-122">Voit määrittää tämän asetuksen arvoksi *Kyllä* vain, jos **Salli yhdistetyt nimikkeet** -asetuksen arvoksi on määritetty *Ei*.</span><span class="sxs-lookup"><span data-stu-id="866bc-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="866bc-123">Määritä **Sallitut tuotedimensioiden yhdistämiset** -pikavälilehdessä asetuksen **Koko** arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="866bc-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="866bc-124">Tässä ohjeaiheessa kuvatussa skenaariossa voidaan yhdistää vain tuotteita, joiden **Koko**-dimensiot eroavat toisistaan.</span><span class="sxs-lookup"><span data-stu-id="866bc-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="866bc-125">Myös muita asetuksia on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="866bc-125">However, other options are also available.</span></span>
1. <span data-ttu-id="866bc-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="866bc-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="866bc-127">Luo uusi päätuote ja tuotevariantit</span><span class="sxs-lookup"><span data-stu-id="866bc-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="866bc-128">Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**.</span><span class="sxs-lookup"><span data-stu-id="866bc-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="866bc-129">Valitse toimintoruudussa **Uusi** ja luo päätuote.</span><span class="sxs-lookup"><span data-stu-id="866bc-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="866bc-130">Aseta **Uusi tuote** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="866bc-131">**Tuotetyyppi:** *Nimike*</span><span class="sxs-lookup"><span data-stu-id="866bc-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="866bc-132">**Tuotteen alatyyppi:** *Päätuote*</span><span class="sxs-lookup"><span data-stu-id="866bc-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="866bc-133">**Tuotenumero:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="866bc-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="866bc-134">**Tuotenimi:** *B0001 Koko*</span><span class="sxs-lookup"><span data-stu-id="866bc-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="866bc-135">**Tuotedimensioryhmä:** *Koko*</span><span class="sxs-lookup"><span data-stu-id="866bc-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="866bc-136">**Määritysmenetelmä:** *Ennalta määritetty variantti*</span><span class="sxs-lookup"><span data-stu-id="866bc-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="866bc-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="866bc-137">Select **OK**.</span></span>
1. <span data-ttu-id="866bc-138">Määritä **Tuotteen tiedot** -sivun **Yleinen**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="866bc-139">**Luo variantit automaattisesti:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="866bc-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="866bc-140">**Kokoryhmä:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="866bc-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="866bc-141">Voit tarkastella ennalta määritettyjä variantteja valitsemalla toimintoruudussa **Tuotevariantit**.</span><span class="sxs-lookup"><span data-stu-id="866bc-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="866bc-142">Näkyviin tulee **Tuotevariantit**-sivu, jossa näkyy luettelo kokoryhmälle määritetyistä varianteista.</span><span class="sxs-lookup"><span data-stu-id="866bc-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="866bc-143">Vapauta tuotteet USMF-yritykselle</span><span class="sxs-lookup"><span data-stu-id="866bc-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="866bc-144">Valitse toimintoruudussa **Vapauta tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="866bc-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="866bc-145">Tarkista **Valitse vapautettavat tuotteet** -sivulla, että tuotenumero *B0001* on luettelossa ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="866bc-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="866bc-146">Vahvista vapautettavat tuotevariantit valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="866bc-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="866bc-147">Valitse **Valitse yritykset, joihin vapautetaan** -sivulla *USMF* ja vahvista valinta valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="866bc-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="866bc-148">Viimeistele vapauttaminen valitsemalla **Vahvista valinta** -sivulla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="866bc-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="866bc-149">Näyttöön tulee Toiminto valmis -ilmoitus.</span><span class="sxs-lookup"><span data-stu-id="866bc-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="866bc-150">Vapautetun tuotteen päivittäminen USMF-yrityksessä</span><span class="sxs-lookup"><span data-stu-id="866bc-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="866bc-151">Varmista, että olet kirjautunut **USMF**-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="866bc-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="866bc-152">Viimeistele vapautetun tuotteen luominen valitsemalla **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="866bc-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="866bc-153">Etsi ja valitse nimikenumero *B0001*, joka avaa **Vapautetun tuotteen tiedot** -sivun.</span><span class="sxs-lookup"><span data-stu-id="866bc-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="866bc-154">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="866bc-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="866bc-155">Varmista **Yleinen**-pikavälilehdessä, että **Nimikemalliryhmä**-kentän arvoksi on määritetty *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="866bc-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="866bc-156">Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Dimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="866bc-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="866bc-157">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-157">Set the following values:</span></span>

    - <span data-ttu-id="866bc-158">**Varastodimensioryhmä:** *Kauppatavara*</span><span class="sxs-lookup"><span data-stu-id="866bc-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="866bc-159">**Seurantadimensioryhmä:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="866bc-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="866bc-160">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="866bc-160">Select **OK**.</span></span>
1. <span data-ttu-id="866bc-161">Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Varaushierarkia**.</span><span class="sxs-lookup"><span data-stu-id="866bc-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="866bc-162">Määritä **Varaushierarkia**-kentän arvoksi *Oletus* ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="866bc-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="866bc-163">Tarkista, että valintasi ovat päivittyneet **Yleinen**-pikavälilehden **Hallinta**-osaan.</span><span class="sxs-lookup"><span data-stu-id="866bc-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="866bc-164">Kirjoita **Osto**-pikavälilehden **Hinta** -kenttään *10*.</span><span class="sxs-lookup"><span data-stu-id="866bc-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="866bc-165">Kirjoita **Kustannusten hallinta** -pikavälilehden **Nimikeryhmä**-kenttään *Audio*.</span><span class="sxs-lookup"><span data-stu-id="866bc-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="866bc-166">Kirjoita **Osto**-pikavälilehden **Hinta** -kenttään *10*.</span><span class="sxs-lookup"><span data-stu-id="866bc-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="866bc-167">Kirjoita **Varasto**-pikavälilehden **Yksikön sarjaryhmän tunnus** -kenttään *ea*.</span><span class="sxs-lookup"><span data-stu-id="866bc-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="866bc-168">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="866bc-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="866bc-169">Luo toimipaikkadirektiivi</span><span class="sxs-lookup"><span data-stu-id="866bc-169">Create a location directive</span></span>

1. <span data-ttu-id="866bc-170">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="866bc-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="866bc-171">Valitse vasemman ruudun **Työtilaustyyppi**-kentässä *Ostotilaukset*.</span><span class="sxs-lookup"><span data-stu-id="866bc-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="866bc-172">Valitse luettelosta sijaintidirektiivi, jonka nimi on *24 PO Direct*.</span><span class="sxs-lookup"><span data-stu-id="866bc-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="866bc-173">Lisää uusi rivi ruudukkoon **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="866bc-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="866bc-174">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="866bc-175">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="866bc-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="866bc-176">Uuden rivin on oltava aiemmin luodun rivin edessä.</span><span class="sxs-lookup"><span data-stu-id="866bc-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="866bc-177">Voit tehdä muutoksen käyttämällä työkalurivin **Siirry ylös** - ja **Siirry alas** -painikkeita tai muuttamalla aiemmin luodun rivin **Järjestysnumero**-kentän arvoksi *2*.</span><span class="sxs-lookup"><span data-stu-id="866bc-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="866bc-178">**Nimi:** *Siirrä BULKKI-sijaintiprofiiliin*</span><span class="sxs-lookup"><span data-stu-id="866bc-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="866bc-179">**Kiinteän sijainnin käyttö:** *Kiinteät ja muut kuin kiinteät sijainnit*</span><span class="sxs-lookup"><span data-stu-id="866bc-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="866bc-180">**Salli negatiivinen varasto:** *Tyhjennä tämä valinta ruutu (= ei)*</span><span class="sxs-lookup"><span data-stu-id="866bc-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="866bc-181">**Erä käytössä:** *Tyhjennä tämä valinta ruutu (= ei)*</span><span class="sxs-lookup"><span data-stu-id="866bc-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="866bc-182">**Strategia:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="866bc-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="866bc-183">Kun uusi rivi on vielä valittuna, valitse ruudukon yläpuolelle **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="866bc-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="866bc-184">Lisää ruudukkoon rivi valitsemalla kyselyn valintaruudun **Alue**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="866bc-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="866bc-185">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="866bc-186">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="866bc-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="866bc-187">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="866bc-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="866bc-188">**Kenttä:** *Sijaintiprofiilin tunnus*</span><span class="sxs-lookup"><span data-stu-id="866bc-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="866bc-189">**Kriteerit:** *BULKKI*</span><span class="sxs-lookup"><span data-stu-id="866bc-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="866bc-190">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="866bc-190">Select **OK**.</span></span>
1. <span data-ttu-id="866bc-191">Valitse **Sijaintidirektiivit**-sivun toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="866bc-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="866bc-192">Jos käytät **Sijaintidirektiivin toiminnot** -pikavälilehden **Strategia**-kentässä asetusta *Konsolidoi*, **Sallitut tuotedimensioiden yhdistämiset** -välilehden **Sijaintiprofiilit**-asetus ohitetaan ja nimikkeet sijoitetaan samaan sijaintiin, vaikka tätä ei ole sallittu asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="866bc-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="866bc-193">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="866bc-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="866bc-194">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="866bc-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="866bc-195">Luo lajitteluun käytettävä valikkonimike valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="866bc-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="866bc-196">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="866bc-197">**Valikkokohteen nimi:** *Ostotilausrivien vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="866bc-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="866bc-198">**Otsikko:** *Ostotilausrivien vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="866bc-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="866bc-199">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="866bc-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="866bc-200">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="866bc-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="866bc-201">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="866bc-202">**Työn luomisprosessi:** *Ostotilausrivien vastaanotto ja hyllytys*</span><span class="sxs-lookup"><span data-stu-id="866bc-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="866bc-203">**Luo rekisterikilpi:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="866bc-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="866bc-204">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="866bc-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="866bc-205">Mobiililaitteen valikon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="866bc-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="866bc-206">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="866bc-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="866bc-207">Valitse valikkoluettelosta **Saapuvat**.</span><span class="sxs-lookup"><span data-stu-id="866bc-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="866bc-208">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="866bc-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="866bc-209">Etsi ja valitse **Käytettävissä olevat valikot ja valikkokohteet** -luettelosta **Ostotilausrivien vastaanotto** -valikkokohta.</span><span class="sxs-lookup"><span data-stu-id="866bc-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="866bc-210">Siirrä **Ostotilausrivien vastaanotto** -valikkokohta **Valikkorakenne** -luetteloon painamalla oikeaa nuolipainiketta.</span><span class="sxs-lookup"><span data-stu-id="866bc-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="866bc-211">Tällä tavoin voit lisätä uuden valikkokohdan valittuun valikkoon.</span><span class="sxs-lookup"><span data-stu-id="866bc-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="866bc-212">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="866bc-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="866bc-213">Skenaario</span><span class="sxs-lookup"><span data-stu-id="866bc-213">Scenario</span></span>

<span data-ttu-id="866bc-214">Tässä esimerkkiskenaariossa esitellään, kuinka kaksi eri tuotevarianttia voidaan sijoittaa samaan sijaintiin, vaikka sijaintiprofiili ei salli yhdistettyjä nimikkeitä, mutta *Tuotedimensioiden yhdistäminen sijainnissa* -toiminto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="866bc-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="866bc-215">Tässä tapauksessa ehtona käytetään **Koko**-varianttia.</span><span class="sxs-lookup"><span data-stu-id="866bc-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="866bc-216">Varmista ennen aloittamista, että varastossa *24* on tyhjiä sijainteja, joissa käytetään *BULKKI*-sijaintiprofiilia.</span><span class="sxs-lookup"><span data-stu-id="866bc-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="866bc-217">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="866bc-217">Create a purchase order</span></span>

<span data-ttu-id="866bc-218">Luot ostotilauksen, jossa on kolme riviä: kaksi riviä samalle tuotenumerolle, mutta eri **Koko**-varianteille, ja kolmas rivi eri tuotteelle, jolla ei ole variantteja.</span><span class="sxs-lookup"><span data-stu-id="866bc-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="866bc-219">Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="866bc-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="866bc-220">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="866bc-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="866bc-221">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="866bc-222">**Toimittajan tili:** *1001*</span><span class="sxs-lookup"><span data-stu-id="866bc-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="866bc-223">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="866bc-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="866bc-224">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="866bc-224">Select **OK**.</span></span>
1. <span data-ttu-id="866bc-225">Ostotilaus luodaan ja uusi rivi lisätään **Ostotilausrivit**-pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="866bc-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="866bc-226">Kirjoita ostotilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="866bc-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="866bc-227">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="866bc-228">**Nimiketunnus:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="866bc-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="866bc-229">**Koko** *L*</span><span class="sxs-lookup"><span data-stu-id="866bc-229">**Size** *L*</span></span>
    - <span data-ttu-id="866bc-230">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="866bc-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="866bc-231">Lisää toinen ostotilausrivi valitsemalla ruudukon yläpuolelta **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="866bc-232">**Nimiketunnus:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="866bc-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="866bc-233">**Koko** *XL*</span><span class="sxs-lookup"><span data-stu-id="866bc-233">**Size** *XL*</span></span>
    - <span data-ttu-id="866bc-234">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="866bc-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="866bc-235">Lisää kolmas ostotilausrivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="866bc-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="866bc-236">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="866bc-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="866bc-237">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="866bc-237">**Quantity:** *1*</span></span>

<span data-ttu-id="866bc-238">1. Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="866bc-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="866bc-239">Ostotilausrivien vastaanottaminen varasto-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="866bc-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="866bc-240">Kirjaudu varastosovellukseen käyttäjänä, joka on otettu käyttöön varastossa *24*.</span><span class="sxs-lookup"><span data-stu-id="866bc-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="866bc-241">Valitse **Saapuvat**-valikko.</span><span class="sxs-lookup"><span data-stu-id="866bc-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="866bc-242">Valitse **Ostotilausrivien vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="866bc-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="866bc-243">Valitse **PUNUM**-kenttä ja syötä ostotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="866bc-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="866bc-244">Vahvista kirjaus valitsemalla Vahvista-painike (✔) sivun alareunasta.</span><span class="sxs-lookup"><span data-stu-id="866bc-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="866bc-245">Syötä vastaanotettavan ostotilauksen rivinumero.</span><span class="sxs-lookup"><span data-stu-id="866bc-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="866bc-246">Valitse **LINENUM**-kenttä ja syötä numero näppäimistön avulla *1*.</span><span class="sxs-lookup"><span data-stu-id="866bc-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="866bc-247">Vahvista kirjaus.</span><span class="sxs-lookup"><span data-stu-id="866bc-247">Confirm your entry.</span></span>
1. <span data-ttu-id="866bc-248">Syötä vastaanotettava määrä.</span><span class="sxs-lookup"><span data-stu-id="866bc-248">Enter the quantity to receive.</span></span> <span data-ttu-id="866bc-249">Paina plusmerkki ( **+**) -painiketta kaksi kertaa, jos haluat suurentaa **Määrä**-kentän arvon arvoon *2*.</span><span class="sxs-lookup"><span data-stu-id="866bc-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="866bc-250">Rekisteröi merkintäsi valitsemalla sivun alareunasta (✔) -painike ja vahvista sitten kirjaus valitsemalla painike (✔) uudelleen.</span><span class="sxs-lookup"><span data-stu-id="866bc-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="866bc-251">Tarkastele tietoja **Ostotilaukset: hyllytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="866bc-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="866bc-252">Tällä sivulla näkyvät hyllytystä varten luodut työt (työ 1).</span><span class="sxs-lookup"><span data-stu-id="866bc-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="866bc-253">Näkyviin tulee sijainti, johon vastaanotettu nimike hyllytetään ja juuri valmiiksi saamasi **Ostotilausrivien vastaanotto** -tehtävän rekisterikilpi, nimike, koko ja määrä.</span><span class="sxs-lookup"><span data-stu-id="866bc-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="866bc-254">Vahvista hyllytystyö.</span><span class="sxs-lookup"><span data-stu-id="866bc-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="866bc-255">Toista vaiheet 4–11 ostotilausriville 2.</span><span class="sxs-lookup"><span data-stu-id="866bc-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="866bc-256">Määritä kuitenkin vaiheessa 8 määräksi *1*.</span><span class="sxs-lookup"><span data-stu-id="866bc-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="866bc-257">Uusi hyllytystyö (työ 2) luodaan samalle sijainnille kuin työ 1.</span><span class="sxs-lookup"><span data-stu-id="866bc-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="866bc-258">Toista vaiheet 4–11 uudelleen ostotilausriville 2.</span><span class="sxs-lookup"><span data-stu-id="866bc-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="866bc-259">Määritä vaiheessa 8 jäljellä olevaksi määräksi *1*.</span><span class="sxs-lookup"><span data-stu-id="866bc-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="866bc-260">Uusi hyllytystyö (työ 3) luodaan samalle sijainnille kuin työ 1 ja työ 2.</span><span class="sxs-lookup"><span data-stu-id="866bc-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="866bc-261">Tämä aiheutuu siitä, että sijaintidirektiivin strategiaksi on asetettu *Konsolidoi* ja **Sallitut tuotedimensioiden yhdistämiset** -pikavälilehden *Bulkki* **Sijaintiprofiilit** -asetus mahdollistaa eri **Koko**-variantin nimikkeiden varastoimisen tähän sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="866bc-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="866bc-262">Toista vaiheet 4–11 ostotilausriville 3.</span><span class="sxs-lookup"><span data-stu-id="866bc-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="866bc-263">Määritä vaiheessa 8 nimikenumeron *A0001* määräksi *1*.</span><span class="sxs-lookup"><span data-stu-id="866bc-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="866bc-264">Uusi hyllytystyö (työ 4) luodaan eri sijainnille kuin ostotilausriveille 1 ja 2 käytettävä sijainti.</span><span class="sxs-lookup"><span data-stu-id="866bc-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="866bc-265">Näin käy, koska sijaintiprofiilissa ei sallita tuotteiden yhdistämistä, mutta saman päätuotteen eri dimensiot on sallittu.</span><span class="sxs-lookup"><span data-stu-id="866bc-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="866bc-266">Valitse sivun yläreunassa oleva valikkopainike (jota kutsutaan joskus nimellä hampurilainen tai Hamburger-painike) ja poistu **Ostotilausrivin vastaanotto** -tilasta valitsemalla **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="866bc-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="866bc-267">Voit toistaa tämän skenaarion, mutta tällä kertaa määritä **Koko**-kentän arvoksi  - *Ei* **Salli tuotedimensioiden yhdistäminen**-pikavälilehden kohdassa *BULKKI* **Sijaintiprofiilit**, jolloin mitään tuotedimensioita ei voi varastoida samaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="866bc-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="866bc-268">Tällöin kun vastaanotat ostotilauksen, jokainen tuotevariantti sijoitetaan uuteen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="866bc-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]