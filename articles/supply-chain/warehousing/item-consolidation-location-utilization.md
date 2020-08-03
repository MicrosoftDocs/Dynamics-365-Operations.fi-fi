---
title: Nimikkeen konsolidointi – sijainnin käyttöaste
description: Tässä aiheessa käsitellään toimintoja, joiden avulla varastopäälliköiden on helppo tarkastella ja suodattaa varaston sijaintien tilavuusperusteista käyttöastetta. Päälliköt voivat valita sijainteja ja luoda varaston siirtotyön suoraan Nimikkeen konsolidointi -sivulla nimikkeiden konsolidointi varten, mikä parantaa varastotilan käyttöä.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5e4172a8d3f82e6eeb8868aac87abd183a94c088
ms.sourcegitcommit: 14b554b43b9d86152ef27fdde6141589bcaf1161
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2020
ms.locfileid: "3598782"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="ac009-104">Nimikkeen konsolidointi – sijainnin käyttöaste</span><span class="sxs-lookup"><span data-stu-id="ac009-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac009-105">Tässä aiheessa käsitellään toimintoja, joiden avulla varastopäälliköiden on helppo tarkastella ja suodattaa varaston sijaintien tilavuusperusteista käyttöastetta.</span><span class="sxs-lookup"><span data-stu-id="ac009-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="ac009-106">Päälliköt voivat valita sijainteja ja luoda varaston siirtotyön suoraan **Nimikkeen konsolidointi** -sivulla nimikkeiden konsolidointi varten, mikä parantaa varastotilan käyttöä.</span><span class="sxs-lookup"><span data-stu-id="ac009-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="ac009-107">Toimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ac009-107">Turn on the features</span></span>

<span data-ttu-id="ac009-108">Ennen tässä aiheessa käsiteltyjen toimintojen käyttöä ne on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="ac009-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="ac009-109">Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="ac009-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="ac009-110">Ota seuraavat toiminnot käyttöön ilmoitetussa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="ac009-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="ac009-111">(Molemmat toiminnot ovat **Varastonhallinta**-moduulissa.)</span><span class="sxs-lookup"><span data-stu-id="ac009-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="ac009-112">Varastosijainnin tila</span><span class="sxs-lookup"><span data-stu-id="ac009-112">Warehouse location status</span></span>
2. <span data-ttu-id="ac009-113">Nimikkeen konsolidointisijainnin käyttöaste</span><span class="sxs-lookup"><span data-stu-id="ac009-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="ac009-114">Varastosijainnin tila</span><span class="sxs-lookup"><span data-stu-id="ac009-114">Warehouse location status</span></span>

<span data-ttu-id="ac009-115">*Varastosijainnin tila* -toiminto lisää **Sijainnit**-sivulle neljä uutta kenttää, joilla voi seurata lisätietoja sijainnin nykyisestä tilasta:</span><span class="sxs-lookup"><span data-stu-id="ac009-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="ac009-116">**Nimiketunnus** – Nimike, joka on tällä hetkellä sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="ac009-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="ac009-117">Jos sijainnissa on useita nimikkeitä, tämä kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="ac009-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="ac009-118">**Viimeinen tehtävän päivämäärä ja kellonaika** – Viimeistä varastopaikkaa vasten suoritetun fyysisen varastoinnin tapahtuman aikaleima.</span><span class="sxs-lookup"><span data-stu-id="ac009-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="ac009-119">**Erääntymispäivämäärä** – Päivämäärä, jolloin varastosijainti tuotiin varastoon.</span><span class="sxs-lookup"><span data-stu-id="ac009-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="ac009-120">Tämä päivämäärä lasketaan rekisterikilven erääntymispäivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="ac009-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="ac009-121">Vaikka tämä päivämäärä tarkka sellaisissa sijainneissa, joissa on rekisterikilpiseuranta, se ei ehkä ole tarkka sellaisissa sijainneissa, jotka eivät ole rekisterikilpiseurannassa.</span><span class="sxs-lookup"><span data-stu-id="ac009-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="ac009-122">**Sijainnin tila** – Sijainnin tila.</span><span class="sxs-lookup"><span data-stu-id="ac009-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="ac009-123">Käytettävissä on neljä arvoa:</span><span class="sxs-lookup"><span data-stu-id="ac009-123">Four values are available:</span></span>

    - <span data-ttu-id="ac009-124">**Määrittelemätön** – Sijaintiprofiili ei voi jäljittää tilaa.</span><span class="sxs-lookup"><span data-stu-id="ac009-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="ac009-125">Näin ollen nykyistä tilaa ei tunneta.</span><span class="sxs-lookup"><span data-stu-id="ac009-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="ac009-126">**Tyhjä** – sijainnissa ei ole varastoa.</span><span class="sxs-lookup"><span data-stu-id="ac009-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="ac009-127">**Keräys** – lähtevät tapahtumat on suoritettu sijainnille sen jälkeen, kun se oli viimeksi tyhjä.</span><span class="sxs-lookup"><span data-stu-id="ac009-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="ac009-128">**Varasto** – Vain saapuvat tapahtumat on suoritettu sen jälkeen, kun sijainti oli viimeksi tyhjä.</span><span class="sxs-lookup"><span data-stu-id="ac009-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="ac009-129">Näiden kenttien avulla varastopäälliköt saavat paremman yleiskuvan varaston sijaintien tilasta.</span><span class="sxs-lookup"><span data-stu-id="ac009-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="ac009-130">Ne mahdollistavat myös kehittyneet raportointi- ja suodatusasetukset.</span><span class="sxs-lookup"><span data-stu-id="ac009-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="ac009-131">Nimikkeen konsolidointi ja sijainnin käyttöasteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ac009-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="ac009-132">Tässä osassa käsitellään järjestelmän valmistelemista käyttämään nimikkeen konsolidointia ja sijainnin käyttöastetta.</span><span class="sxs-lookup"><span data-stu-id="ac009-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="ac009-133">Menettelyssä käytetään vakioesittelytietojen näytearvoja.</span><span class="sxs-lookup"><span data-stu-id="ac009-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="ac009-134">Jos aiot käyttää myöhemmin tässä ohjeaiheessa käsiteltyä esimerkkiskenaariota, valitse **USMF**-yritys (joka sisältää vakioesittelytiedot) ja luo jokainen tässä osassa kuvattu tietue.</span><span class="sxs-lookup"><span data-stu-id="ac009-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="ac009-135">Jos et aio käyttää esimerkkiskenaariota, tässä annettuja arvoja voi pitää esimerkkeinä asetustyypeistä, jotka on tehtävä toimintojen käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="ac009-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="ac009-136">Vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="ac009-136">Released product</span></span>

1. <span data-ttu-id="ac009-137">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="ac009-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ac009-138">Valitse **Nimiketunnus**-kentässä *M9201* ja avaa tietosivu.</span><span class="sxs-lookup"><span data-stu-id="ac009-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="ac009-139">Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset mitat**.</span><span class="sxs-lookup"><span data-stu-id="ac009-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="ac009-140">Valitse **Fyysiset mitat** -sivun toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ac009-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="ac009-141">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ac009-141">A new line is added to the grid.</span></span> <span data-ttu-id="ac009-142">**Nimiketunnus**-kenttä on määritetty valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="ac009-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="ac009-143">Valitse **Yksikkö**-kentässä *kpl*.</span><span class="sxs-lookup"><span data-stu-id="ac009-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="ac009-144">Muut rivin kentät määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ac009-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="ac009-145">Valitse **Tallenna** ja sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ac009-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="ac009-146">Sijaintiprofiili</span><span class="sxs-lookup"><span data-stu-id="ac009-146">Location profile</span></span>

1. <span data-ttu-id="ac009-147">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="ac009-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="ac009-148">Valitse sijaintiprofiililuettelossa **KERROS-05**.</span><span class="sxs-lookup"><span data-stu-id="ac009-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="ac009-149">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ac009-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ac009-150">Varmista **Yleiset**-pikavälilehdessä seuraavissa asetuksissa on valittu *Kyllä*:</span><span class="sxs-lookup"><span data-stu-id="ac009-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="ac009-151">Ota käyttöön nimike sijainnissa</span><span class="sxs-lookup"><span data-stu-id="ac009-151">Enable item in location</span></span>
    - <span data-ttu-id="ac009-152">Ota käyttöön sijaintitila</span><span class="sxs-lookup"><span data-stu-id="ac009-152">Enable location status</span></span>

1. <span data-ttu-id="ac009-153">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ac009-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ac009-154">Jos **Ota nimike sijainnissa käyttöön**- ja **Ota käyttöön sijaintitila** -asetusten arvo on jo *Kyllä*, siirry vaiheeseen 10, jossa on **Dimensiot**-pikavälilehden määritysohjeet.</span><span class="sxs-lookup"><span data-stu-id="ac009-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="ac009-155">Jos asetusten arvona ei ole vielä *Kyllä*, tee **Varastonhallinta**-moduulin yhdenmukaisuustarkistus sen jälkeen, kun asetukset on määritetty manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ac009-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="ac009-156">Jatka siinä tapauksessa Jatka seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="ac009-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="ac009-157">Suorita yhdenmukaisuustarkistus valitsemalla **Järjestelmän hallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus**.</span><span class="sxs-lookup"><span data-stu-id="ac009-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="ac009-158">Määritä seuraavat arvot **Yhdenmukaisuustarkistus**-valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="ac009-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ac009-159">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="ac009-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="ac009-160">**Tarkista/korjaa:** *Tarkista*</span><span class="sxs-lookup"><span data-stu-id="ac009-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="ac009-161">**Päivämäärästä:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="ac009-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="ac009-162">**Varaston sijainnin tilan yhdenmukaisuustarkistus:** Valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ac009-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="ac009-163">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac009-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="ac009-164">Saat ilmoituksen, kun yhdenmukaisuustarkistus on valmis.</span><span class="sxs-lookup"><span data-stu-id="ac009-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="ac009-165">Voit lukea viestin avaamalla [toimintokeskuksen](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications).</span><span class="sxs-lookup"><span data-stu-id="ac009-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="ac009-166">Voit katsoa tiedot valitsemalla **Sanoman tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ac009-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="ac009-167">Jos yhdenmukaisuustarkistuksen sanoma on Virheelliset sijaintitilatiedot löydetty sijainnille XXXX varastossa XX, yhdenmukaisuustarkistus on suoritettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ac009-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="ac009-168">Valitse tällä kertaa **Tarkista/korjaa**-kentässä *Korjaa virhe*.</span><span class="sxs-lookup"><span data-stu-id="ac009-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="ac009-169">Tarkista sanomista, että virheitä ei löytynyt.</span><span class="sxs-lookup"><span data-stu-id="ac009-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="ac009-170">Viimeistele sijaintiprofiilin määritykset.</span><span class="sxs-lookup"><span data-stu-id="ac009-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="ac009-171">Valitse taas **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**, valitse sitten sijaintiprofiili **KERROS-05** ja valitse lopuksi toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ac009-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ac009-172">Määritä **Dimensiot**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ac009-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ac009-173">**Tilavuuden käyttöasteprosentti:** *100*</span><span class="sxs-lookup"><span data-stu-id="ac009-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="ac009-174">**Varastosijainnissa käytettävä tilavuuden mittausmenetelmä:** *Käytä sijainnin tilavuutta*</span><span class="sxs-lookup"><span data-stu-id="ac009-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="ac009-175">**Sijainnin todellinen korkeus:** *10*</span><span class="sxs-lookup"><span data-stu-id="ac009-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="ac009-176">**Sijainnin todellinen leveys:** *10*</span><span class="sxs-lookup"><span data-stu-id="ac009-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="ac009-177">**Sijainnin todellinen syvyys:** *10*</span><span class="sxs-lookup"><span data-stu-id="ac009-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="ac009-178">**Enimmäispaino;** *100*</span><span class="sxs-lookup"><span data-stu-id="ac009-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="ac009-179">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ac009-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="ac009-180">Mobiililaitteen valikkovaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="ac009-180">Mobile device menu items</span></span>

1. <span data-ttu-id="ac009-181">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="ac009-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ac009-182">Luo lajittelun valikkovaihtoehto valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ac009-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="ac009-183">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ac009-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="ac009-184">**Valikkovaihtoehdon nimi:** *Oikaisu sisään*</span><span class="sxs-lookup"><span data-stu-id="ac009-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="ac009-185">**Otsikko:** *Oikaisu sisään*</span><span class="sxs-lookup"><span data-stu-id="ac009-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="ac009-186">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="ac009-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ac009-187">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="ac009-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="ac009-188">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ac009-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ac009-189">**Työn luontiprosessi:** *Oikaisu sisään*</span><span class="sxs-lookup"><span data-stu-id="ac009-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="ac009-190">**Varasto-oikaisutyypit:** *Oikaisu sisään*</span><span class="sxs-lookup"><span data-stu-id="ac009-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="ac009-191">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ac009-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="ac009-192">Mobiililaitevalikko</span><span class="sxs-lookup"><span data-stu-id="ac009-192">Mobile device menu</span></span>

1. <span data-ttu-id="ac009-193">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="ac009-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ac009-194">Valitse valikkoluettelosta **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="ac009-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="ac009-195">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ac009-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ac009-196">Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelosta **Oikaisu sisään** -valikkovaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ac009-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="ac009-197">Siirrä **Oikaisu sisään**oikealla nuolipainikkeella **Valikon rakenne** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="ac009-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="ac009-198">Uusi valikkovaihtoehto lisätään tällä tavoin valittuun valikkoon.</span><span class="sxs-lookup"><span data-stu-id="ac009-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="ac009-199">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ac009-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="ac009-200">Siirtotapahtuman tyypit</span><span class="sxs-lookup"><span data-stu-id="ac009-200">Movement types</span></span>

1. <span data-ttu-id="ac009-201">Valitse **Varastonhallinta \> Määritys \> Varasto \> Siirtotapahtuman tyypit**.</span><span class="sxs-lookup"><span data-stu-id="ac009-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="ac009-202">Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ac009-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="ac009-203">**Siirtotapahtumatyypin koodi:** *KONSOLIDOI*</span><span class="sxs-lookup"><span data-stu-id="ac009-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="ac009-204">**Kuvaus:** *Konsolidoi sijainnit*</span><span class="sxs-lookup"><span data-stu-id="ac009-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="ac009-205">**Työluokan tunnus:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="ac009-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="ac009-206">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ac009-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ac009-207">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="ac009-207">Example scenario</span></span>

<span data-ttu-id="ac009-208">Seuraavassa skenaariossa käytetään varastosovellusta mobiililaitteessa tekemään varaston *oikaisu sisään* varaston kahdessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="ac009-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="ac009-209">Varaston lisääminen sijainteihin</span><span class="sxs-lookup"><span data-stu-id="ac009-209">Add inventory to locations</span></span>

1. <span data-ttu-id="ac009-210">Kirjaudu mobiililaitteeseen käyttäjänä, joka on määritetty varastoon *51*.</span><span class="sxs-lookup"><span data-stu-id="ac009-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="ac009-211">Valitse **Varasto \> Oikaisu sisään**.</span><span class="sxs-lookup"><span data-stu-id="ac009-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="ac009-212">Anna nyt ensimmäinen varaston oikaisu.</span><span class="sxs-lookup"><span data-stu-id="ac009-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="ac009-213">Valitse **Oikaisu sisään** -tehtävässä sijainti, jonka varastoa oikaistaan.</span><span class="sxs-lookup"><span data-stu-id="ac009-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="ac009-214">Valitse **SIJAINTI**-kentässä *RK-001*.</span><span class="sxs-lookup"><span data-stu-id="ac009-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="ac009-215">Vahvista sijainti.</span><span class="sxs-lookup"><span data-stu-id="ac009-215">Confirm the location.</span></span>
1. <span data-ttu-id="ac009-216">Luo sijaintiin lisättävälle nimikkeelle rekisterikilpitunnus.</span><span class="sxs-lookup"><span data-stu-id="ac009-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="ac009-217">Anna **RK**-kentässä *RK00101*.</span><span class="sxs-lookup"><span data-stu-id="ac009-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="ac009-218">Vahvista rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="ac009-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="ac009-219">Kirjoita rekisterikilpeen lisättävä nimike.</span><span class="sxs-lookup"><span data-stu-id="ac009-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="ac009-220">Kirjoita **ITEM**-kenttään *M9201*.</span><span class="sxs-lookup"><span data-stu-id="ac009-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="ac009-221">Vahvista nimike.</span><span class="sxs-lookup"><span data-stu-id="ac009-221">Confirm the item.</span></span>
1. <span data-ttu-id="ac009-222">Anna lisättävän nimikkeen määrä.</span><span class="sxs-lookup"><span data-stu-id="ac009-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="ac009-223">Anna **MÄÄRÄ**-kentässä *10*.</span><span class="sxs-lookup"><span data-stu-id="ac009-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="ac009-224">Vahvista määrä.</span><span class="sxs-lookup"><span data-stu-id="ac009-224">Confirm the quantity.</span></span>

    <span data-ttu-id="ac009-225">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="ac009-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="ac009-226">Anna nyt toinen varaston oikaisu.</span><span class="sxs-lookup"><span data-stu-id="ac009-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="ac009-227">Valitse **Oikaisu sisään** -tehtävässä sijainti, jonka varastoa oikaistaan.</span><span class="sxs-lookup"><span data-stu-id="ac009-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="ac009-228">Valitse **SIJAINTI**-kentässä *RK-002*.</span><span class="sxs-lookup"><span data-stu-id="ac009-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="ac009-229">Vahvista sijainti.</span><span class="sxs-lookup"><span data-stu-id="ac009-229">Confirm the location.</span></span>
1. <span data-ttu-id="ac009-230">Luo sijaintiin lisättävälle nimikkeelle rekisterikilpitunnus.</span><span class="sxs-lookup"><span data-stu-id="ac009-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="ac009-231">Anna **RK**-kentässä *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="ac009-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="ac009-232">Vahvista rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="ac009-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="ac009-233">Kirjoita rekisterikilpeen lisättävä nimike.</span><span class="sxs-lookup"><span data-stu-id="ac009-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="ac009-234">Kirjoita **ITEM**-kenttään *M9201*.</span><span class="sxs-lookup"><span data-stu-id="ac009-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="ac009-235">Vahvista nimike.</span><span class="sxs-lookup"><span data-stu-id="ac009-235">Confirm the item.</span></span>
1. <span data-ttu-id="ac009-236">Anna lisättävän nimikkeen määrä.</span><span class="sxs-lookup"><span data-stu-id="ac009-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="ac009-237">Anna **MÄÄRÄ**-kentässä *15*.</span><span class="sxs-lookup"><span data-stu-id="ac009-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="ac009-238">Vahvista määrä.</span><span class="sxs-lookup"><span data-stu-id="ac009-238">Confirm the quantity.</span></span>

    <span data-ttu-id="ac009-239">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="ac009-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="ac009-240">Valitse valikkopainike (jossa on allekkain useita viivoja) ja lopeta **Oikaisu sisään** -tehtävä valitsemalla **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="ac009-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="ac009-241">Sijaintien konsolidointi</span><span class="sxs-lookup"><span data-stu-id="ac009-241">Consolidate locations</span></span>

1. <span data-ttu-id="ac009-242">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Nimikkeen konsolidointi**.</span><span class="sxs-lookup"><span data-stu-id="ac009-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="ac009-243">Valitse ylätunnisteessa konsolidoitava varasto.</span><span class="sxs-lookup"><span data-stu-id="ac009-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="ac009-244">Anna **Varasto**-kentässä *51*.</span><span class="sxs-lookup"><span data-stu-id="ac009-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="ac009-245">Tietue näytetään jokaiselle sijainnille, jossa nimikettä *M9201* säädettiin.</span><span class="sxs-lookup"><span data-stu-id="ac009-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="ac009-246">**Käyttöasteprosentti**-sarake näyttää kunkin sijainnin tilavuusperusteisen käyttöasteen.</span><span class="sxs-lookup"><span data-stu-id="ac009-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="ac009-247">Varasto konsolidoidaan valitsemalla kaikki konsolidoitavat sijainnit ja valitsemalla sitten toimintoruudussa **Konsolidoi varasto**.</span><span class="sxs-lookup"><span data-stu-id="ac009-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="ac009-248">Määritä **Konsolidoi varasto** -valintaikkunassa sijainti ja siirtotapahtuman tyyppi, joiden avulla varaston siirtotapahtuman työ on luotava.</span><span class="sxs-lookup"><span data-stu-id="ac009-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="ac009-249">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ac009-249">Set the following values:</span></span>

    - <span data-ttu-id="ac009-250">**Sijainti:** *RK-001*</span><span class="sxs-lookup"><span data-stu-id="ac009-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="ac009-251">**Siirtotapahtumatyypin koodi:** *KONSOLIDOI*</span><span class="sxs-lookup"><span data-stu-id="ac009-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="ac009-252">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac009-252">Select **OK**.</span></span>
1. <span data-ttu-id="ac009-253">Saat työn siirtotapahtumatyön luonnista ilmoittavan tietosanoman.</span><span class="sxs-lookup"><span data-stu-id="ac009-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="ac009-254">Kirjoita siirtotapahtumatyön tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="ac009-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="ac009-255">Siirtotapahtumatyön näyttäminen</span><span class="sxs-lookup"><span data-stu-id="ac009-255">View movement work</span></span>

1. <span data-ttu-id="ac009-256">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ac009-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ac009-257">Näytä luotu työ.</span><span class="sxs-lookup"><span data-stu-id="ac009-257">View the work that was created.</span></span> <span data-ttu-id="ac009-258">Suodata työruudukkoa tai tee siinä haku käyttämällä varaston konsolidoinnin siirtotapahtumatyön tunnusta.</span><span class="sxs-lookup"><span data-stu-id="ac009-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="ac009-259">Tässä skenaariossa aiemmin luotua sijaintia, jossa oli varastoa, käytetään varaston konsolidointisijaintina.</span><span class="sxs-lookup"><span data-stu-id="ac009-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="ac009-260">Tämän vuoksi vain yksi työtunnus luotiin.</span><span class="sxs-lookup"><span data-stu-id="ac009-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="ac009-261">Järjestelmä luo kullekin suoritettavalle siirrolle yhden työtunnuksen.</span><span class="sxs-lookup"><span data-stu-id="ac009-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="ac009-262">Jos määrität jo varastoa sisältävän sijainnin, vain yksi työtunnus luodaan.</span><span class="sxs-lookup"><span data-stu-id="ac009-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="ac009-263">Jos määritä uuden sijainnin, työtunnuksia luodaan kaksi.</span><span class="sxs-lookup"><span data-stu-id="ac009-263">If you specify a new location, two work IDs are created.</span></span>
