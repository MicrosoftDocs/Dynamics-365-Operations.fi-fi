---
title: Keräilyrivin ryhmittely
description: Tässä ohjeaiheessa on keräilyrivin yhteenveto.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ab8cdd7cad5420aca0de53e59220da9e230d411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234630"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="85592-103">Keräilyrivin ryhmittely</span><span class="sxs-lookup"><span data-stu-id="85592-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85592-104">Keräilyrivin ryhmittelyssä useita työrivejä, joilla on sama nimike ja sijainti, voidaan yhdistää yhdeksi keräilyksi, joka näytetään käyttäjälle mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="85592-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="85592-105">Tämän vuoksi varastotyöntekijät voivat saada mahdollisimman tehokkaat ohjeet samalla, kun tarvittava työrivien erottelu (esimerkiksi eri kontteihin ja tilauksiin) voidaan säilyttää järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="85592-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="85592-106">Työn keräilyrivien ryhmittelytoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="85592-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="85592-107">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="85592-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="85592-108">Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa toiminnon tilan ja ottaa sen tarvittaessa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="85592-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="85592-109">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="85592-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="85592-110">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="85592-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="85592-111">**Toiminnon nimi:** *Keräilyrivin ryhmittely*</span><span class="sxs-lookup"><span data-stu-id="85592-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="85592-112">Määritä keräilyrivin ryhmittely</span><span class="sxs-lookup"><span data-stu-id="85592-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="85592-113">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="85592-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="85592-114">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="85592-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="85592-115">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="85592-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="85592-116">Valitse **Valikkovaihtoehdon nimi** -kenttä ja anna *Myyntiryhmän rivikeräily*.</span><span class="sxs-lookup"><span data-stu-id="85592-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="85592-117">Valitse **Otsikko** -kenttä ja anna *Myyntiryhmän rivikeräily*.</span><span class="sxs-lookup"><span data-stu-id="85592-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="85592-118">Tämä otsikko näkyy matkalaitteen valikossa.</span><span class="sxs-lookup"><span data-stu-id="85592-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="85592-119">Valitse **Tila**-kentässä *Työ*.</span><span class="sxs-lookup"><span data-stu-id="85592-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="85592-120">Valitse **Käytä nykyistä työtä** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="85592-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="85592-121">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="85592-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="85592-122">Valitse **Ohjaaja**-kentässä *Järjestelmäohjattu*.</span><span class="sxs-lookup"><span data-stu-id="85592-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="85592-123">Määritä **Luo rekisterikilpi** -valinnan asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="85592-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="85592-124">Määritä **Ryhmäkeräily** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="85592-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="85592-125">Hyväksy jäljellä olevien vaihtoehtojen oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="85592-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="85592-126">Määritä mobiililaitteen valikkovaihtoehdon kelvolliset työluokat seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85592-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="85592-127">Valitse **Työluokat**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="85592-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="85592-128">**Työluokan tunnus** -kentässä voi valita joko *Myynti* tai *Myyntitilauksen keräily* sen mukaan, mikä varasto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="85592-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="85592-129">Valitse tässä skenaariossa *Myyntitilauksen keräily*.</span><span class="sxs-lookup"><span data-stu-id="85592-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="85592-130">**Työtilaustyyppi**-kentän arvoksi määritetään automaattisesti *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="85592-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="85592-131">Määritä varaston mobiililaitteen valikko</span><span class="sxs-lookup"><span data-stu-id="85592-131">Set up a mobile device menu</span></span>

<span data-ttu-id="85592-132">Juuri luotu valikkovaihtoehto lisätään **Lähtevät**-valikkoon seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85592-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="85592-133">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="85592-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="85592-134">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="85592-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="85592-135">Luetteloruudussa näkyy kaikki aiemmin luodut mobiililaitevalikot.</span><span class="sxs-lookup"><span data-stu-id="85592-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="85592-136">Valitse luettelossa *Lähtevät*.</span><span class="sxs-lookup"><span data-stu-id="85592-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="85592-137">Etsi ja valitse juuri luotu *Myyntiryhmän rivikeräily* -valikkovaihtoehto **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="85592-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="85592-138">Siirrä *Myyntiryhmän rivikeräily* -valikkovaihtoehto **Valikkorakenne** -luetteloon oikealla nuolipainikkeella.</span><span class="sxs-lookup"><span data-stu-id="85592-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="85592-139">Siirrä valikkovaihtoehto haluttuun kohtaan valikkorakenteessa ylä- ja alanuolipainikkeella.</span><span class="sxs-lookup"><span data-stu-id="85592-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="85592-140">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="85592-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="85592-141">Määritä työmalli</span><span class="sxs-lookup"><span data-stu-id="85592-141">Set up a work template</span></span>

1. <span data-ttu-id="85592-142">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="85592-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="85592-143">Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="85592-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="85592-144">Etsi ja valitse **Yleiskatsaus**-ruudukossa työmalli, jota on käytettävä tässä toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="85592-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="85592-145">Valitse tässä skenaariossa *51 Poiminta* -malli.</span><span class="sxs-lookup"><span data-stu-id="85592-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="85592-146">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="85592-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="85592-147">Valitse kyselyeditorin valintaikkunan **Lajittelu**-välilehdessä **Lisää** ja määritä sitten seuraavat arvot uudelle riville:</span><span class="sxs-lookup"><span data-stu-id="85592-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="85592-148">Valitse **Taulu**-sarakkeessa *Väliaikaiset työtapahtumat*.</span><span class="sxs-lookup"><span data-stu-id="85592-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="85592-149">Valitse **Johdettu taulu**-sarakkeessa *Väliaikaiset työtapahtumat*.</span><span class="sxs-lookup"><span data-stu-id="85592-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="85592-150">Valitse **Kenttä**-sarakkeessa *Nimikkeen numero*.</span><span class="sxs-lookup"><span data-stu-id="85592-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="85592-151">Valitse **Hakusuunta**-sarakkeessa *Laskeva*.</span><span class="sxs-lookup"><span data-stu-id="85592-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="85592-152">Sulje valintaikkuna ja tallenna valinta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="85592-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="85592-153">Seuraava sanoma avautuu: Ryhmittely nollataan. Haluatko jatkaa?</span><span class="sxs-lookup"><span data-stu-id="85592-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="85592-154">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="85592-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85592-155">Jotta poimintarivin ryhmittelytoiminto toimisi, työrivit on lajiteltava nimiketunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="85592-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="85592-156">Jos rivejä, joilla on samat nimikkeet, ei ole järjestetty yksitellen, niitä ei ryhmitellä.</span><span class="sxs-lookup"><span data-stu-id="85592-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="85592-157">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="85592-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="85592-158">Luo keräystyö</span><span class="sxs-lookup"><span data-stu-id="85592-158">Create picking work</span></span>

<span data-ttu-id="85592-159">Ennen kuin voit määrittää keräilyrivin ryhmittelyn, sinun on luotava joitakin tukikelpoisia lähteviä töitä.</span><span class="sxs-lookup"><span data-stu-id="85592-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="85592-160">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="85592-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="85592-161">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="85592-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="85592-162">Valitse **Asiakastili**-kentässä *US-004*.</span><span class="sxs-lookup"><span data-stu-id="85592-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="85592-163">Valitse **Yleinen**-pikavälilehden **Varasto**-kentässä *51*.</span><span class="sxs-lookup"><span data-stu-id="85592-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="85592-164">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="85592-164">Select **OK**.</span></span>
1. <span data-ttu-id="85592-165">Lisää seuraavat kuusi riviä **Myyntitilausrivit**-pikavälilehdessä:</span><span class="sxs-lookup"><span data-stu-id="85592-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="85592-166">Valitse **Rivi 1:** **Nimikkeen numero** -kentässä *M9200*.</span><span class="sxs-lookup"><span data-stu-id="85592-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="85592-167">Kirjoita **Määrä**-kenttään *3*.</span><span class="sxs-lookup"><span data-stu-id="85592-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="85592-168">Valitse **Rivi 2:** **Nimikkeen numero** -kentässä *M9201*.</span><span class="sxs-lookup"><span data-stu-id="85592-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="85592-169">Kirjoita **Määrä**-kenttään *3*.</span><span class="sxs-lookup"><span data-stu-id="85592-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="85592-170">Valitse **Rivi 3:** **Nimikkeen numero** -kentässä *M9202*.</span><span class="sxs-lookup"><span data-stu-id="85592-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="85592-171">Kirjoita **Määrä**-kenttään *2*.</span><span class="sxs-lookup"><span data-stu-id="85592-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="85592-172">Valitse **Rivi 4:** **Nimikkeen numero** -kentässä *M9200*.</span><span class="sxs-lookup"><span data-stu-id="85592-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="85592-173">Kirjoita **Määrä**-kenttään *1*.</span><span class="sxs-lookup"><span data-stu-id="85592-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="85592-174">Valitse **Rivi 5:** **Nimikkeen numero** -kentässä *M9200*.</span><span class="sxs-lookup"><span data-stu-id="85592-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="85592-175">Kirjoita **Määrä**-kenttään *3*.</span><span class="sxs-lookup"><span data-stu-id="85592-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="85592-176">Valitse **Rivi 6:** **Nimikkeen numero** -kentässä *M9202*.</span><span class="sxs-lookup"><span data-stu-id="85592-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="85592-177">Kirjoita **Määrä**-kenttään *7*.</span><span class="sxs-lookup"><span data-stu-id="85592-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="85592-178">Tässä on yhteenveto kunkin nimikkeen kokonaismääristä:</span><span class="sxs-lookup"><span data-stu-id="85592-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="85592-179">**Nimike M9200:** *7* kpl</span><span class="sxs-lookup"><span data-stu-id="85592-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="85592-180">**Nimike M9201:** *3* kpl</span><span class="sxs-lookup"><span data-stu-id="85592-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="85592-181">**Nimike M9202:** *9* kpl</span><span class="sxs-lookup"><span data-stu-id="85592-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="85592-182">Ennen kuin vapautat tilaukset varastoon, varmista, että poiminnan sijainneissa on tarpeeksi varastoa kaikkien tilausten kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="85592-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="85592-183">Tarkista **Toimipaikkadirektiivin** asetus ja määritä, mitä keräilysijainteja myyntitilausten keräilyyn käytetään.</span><span class="sxs-lookup"><span data-stu-id="85592-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="85592-184">Jos käytössä on varaston *51* Contoso-esittelytietoympäristö, vahvista varaston saatavuus.</span><span class="sxs-lookup"><span data-stu-id="85592-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="85592-185">Kullekin riville on nyt varattava varastoa.</span><span class="sxs-lookup"><span data-stu-id="85592-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="85592-186">Valitse **Myyntitilausrivit**-pikavälilehdessä yksi varattavista riveistä.</span><span class="sxs-lookup"><span data-stu-id="85592-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="85592-187">Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="85592-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="85592-188">Tee varaus valitsemalla **Varaus**-sivun toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="85592-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="85592-189">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="85592-189">Then close the page.</span></span>
1. <span data-ttu-id="85592-190">Toista vaiheet 8–10 muille varattaville riveille.</span><span class="sxs-lookup"><span data-stu-id="85592-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="85592-191">Myyntitilaus on vapautettava varastoon.</span><span class="sxs-lookup"><span data-stu-id="85592-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="85592-192">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="85592-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="85592-193">Avautuva sanoma ilmoittaa, että lähetys ja aalto on luotu ja että aalto on lähetetty suoritettavaksi eränä.</span><span class="sxs-lookup"><span data-stu-id="85592-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="85592-194">Kuun aalto ja kaikki sen jälkeiset työt on suoritettu, työlle luotavassa työtunnuksessa on kuusi riviä.</span><span class="sxs-lookup"><span data-stu-id="85592-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="85592-195">Rivit lajitellaan nimiketunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="85592-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="85592-196">Voit tarkastella luotua työtä valitsemalla **Varastonhallinta \> Työ \> Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="85592-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="85592-197">Kirjoita **Työtunnus**-arvo muistiin, sillä sitä tarvitaan seuraavassa menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="85592-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="85592-198">Keräilyn käynnistäminen mobiililaitteesta</span><span class="sxs-lookup"><span data-stu-id="85592-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="85592-199">Kirjaudu mobiililaitteeseen käyttäjänä, joka on määritetty varastoon *51*.</span><span class="sxs-lookup"><span data-stu-id="85592-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="85592-200">Valitse mobiililaitteessa valikko, joka sisältää uuden mobiililaitteen valikkovaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="85592-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="85592-201">Valitse tässä skenaariossa **Lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="85592-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="85592-202">Käynnistä keräily valitsemalla **Myyntiryhmän rivikeräily** -valikkovaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="85592-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="85592-203">Anna edellisessä menettelyssä muistiin kirjoitettu **Työtunnus**-arvo.</span><span class="sxs-lookup"><span data-stu-id="85592-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="85592-204">Keräilyvaiheen, jossa kaikki nimikkeen *M9200* keräilyrivit on ryhmitelty, pitäisi olla näkyvissä, ja ohjeena pitäisi olla poimia *7* kappaletta nimikettä *M9200*.</span><span class="sxs-lookup"><span data-stu-id="85592-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="85592-205">Kolmen keräilyrivin keräilytyö on koottu käyttäjälle yhdeksi keräilyvaiheeksi mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="85592-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="85592-206">Vahvista ensimmäinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="85592-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="85592-207">Siirry työtunnuksen työsivulla, jossa huomaat, että nimikkeen *M9200* kaikki kolme keräilyriviä suljettiin samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="85592-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="85592-208">Palaa mobiililaitteeseen ja jatka keräämistä.</span><span class="sxs-lookup"><span data-stu-id="85592-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="85592-209">Nimikkeen *M9201* työrivin 4 pitäisi olla esillä.</span><span class="sxs-lookup"><span data-stu-id="85592-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="85592-210">Koska tilauksessa on vain yksi työrivi, mitään koostettavaa ei ole.</span><span class="sxs-lookup"><span data-stu-id="85592-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="85592-211">Vahvista ensimmäinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="85592-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="85592-212">Matkaviestimen viimeinen poimintavaihe kokoaa yhteen kaksi viimeistä poimintariviä työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="85592-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="85592-213">Tee nimikkeen *M9202* *9* kappaleen keräysvaihe.</span><span class="sxs-lookup"><span data-stu-id="85592-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="85592-214">Vahvista laittovaihe ja mahdolliset muut poiminta-/laittovaiheet töiden suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="85592-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="85592-215">Työrivit voidaan ryhmitellä vain, jos ne ovat järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="85592-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="85592-216">Seuraavaa toimintoa ei tueta:</span><span class="sxs-lookup"><span data-stu-id="85592-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="85592-217">Todellisen painon nimikkeet</span><span class="sxs-lookup"><span data-stu-id="85592-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="85592-218">Jos työssä on mitään todellisen painon nimikkeitä, näyttöön tulee virhesanoma, ennen kuin aloitat poiminnan.</span><span class="sxs-lookup"><span data-stu-id="85592-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="85592-219">Kappaleen keräily</span><span class="sxs-lookup"><span data-stu-id="85592-219">Piece picking</span></span>
>   - <span data-ttu-id="85592-220">Työrivit, joilla on keskeneräinen täydennystyö</span><span class="sxs-lookup"><span data-stu-id="85592-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="85592-221">Ylikeräily</span><span class="sxs-lookup"><span data-stu-id="85592-221">Over-picking</span></span>
>   - <span data-ttu-id="85592-222">Nimikkeen uudelleenkohdistaminen lyhyen keräilyn avulla</span><span class="sxs-lookup"><span data-stu-id="85592-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]