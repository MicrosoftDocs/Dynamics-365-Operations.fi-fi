---
title: Järjestelmäohjattu työjärjestys
description: Tässä ohjeaiheessa on tietoja järjestelmän ohjaamien töiden jaksotuksesta. Tämän toiminnon avulla voit lajitella ja suodattaa ne työtilaukset, jotka järjestelmä esittää käyttäjille suorittamista varten. Se on hyödyllinen tilanteissa, joissa fyysisen varastoinnin poimintaprosessin ajo edellyttää lisäehtoja.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 2884c480d20090266f7cffb5e7d0aca58c1174f0
ms.sourcegitcommit: edb46dce498df42b09e8f5ad6de00f86c8022dfa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534847"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="ffc21-105">Järjestelmäohjattu työjärjestys</span><span class="sxs-lookup"><span data-stu-id="ffc21-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffc21-106">Järjestelmäohjatun työjärjestyksen avulla voit lajitella ja suodattaa ne työtilaukset, jotka järjestelmä esittää käyttäjille suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="ffc21-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="ffc21-107">Se on hyödyllinen tilanteissa, joissa fyysisen varastoinnin poimintaprosessi edellyttää lisäehtoja (kuten lähetysaikaa, poimintavyöhykettä, sijaintiprofiilia tai useiden ehtojen yhdistelmää).</span><span class="sxs-lookup"><span data-stu-id="ffc21-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="ffc21-108">Tämä toiminto laajentaa nykyisiä järjestelmän ohjaamien keräilyn toimintoja lisäämällä järjestelmään perustuvan kyselyjärjestyksen, jossa käyttäjät voivat määrittää sarjan ja vähintään yhden kyselyn, joka arvioi kaikki luodut työtilaukset.</span><span class="sxs-lookup"><span data-stu-id="ffc21-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="ffc21-109">Vain ne työtilaukset, jotka täyttävät mobiililaitteen valikkovaihtoehdon määrityksessä määritetyt ehdot, tallennetaan ja esitetään.</span><span class="sxs-lookup"><span data-stu-id="ffc21-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="ffc21-110">Tämän vuoksi tämän toiminnon avulla voidaan edelleen optimoida varaston poimintaprosesseja, koska se tunnistaa määritettyjä ehtoja vastaavat työtilaukset, liittää ne oikeaan mobiililaitteen valikkokohteeseen ja näyttää ne sitten työntekijälle tietyn osaamisalueen, poimintalaitteiden tai muun tarpeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ffc21-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="ffc21-111">Jos tarvitaan eri ehtoja, on käytettävä useita mobiililaitteiden valikkokohteita.</span><span class="sxs-lookup"><span data-stu-id="ffc21-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="ffc21-112">Ota käyttöön organisaation laajuinen järjestelmäohjattu työjärjestysominaisuus</span><span class="sxs-lookup"><span data-stu-id="ffc21-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="ffc21-113">Ennen kuin voit käyttää järjestelmäohjattua työjärjestystoimintoa, sen pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="ffc21-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="ffc21-114">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="ffc21-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ffc21-115">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="ffc21-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ffc21-116">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="ffc21-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ffc21-117">**Toiminnon nimi:** *Organisaation laajuinen järjestelmäsuunnattu työn sekvensointi*</span><span class="sxs-lookup"><span data-stu-id="ffc21-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="ffc21-118">Määritys</span><span class="sxs-lookup"><span data-stu-id="ffc21-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ffc21-119">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ffc21-119">Make demo data available</span></span>

<span data-ttu-id="ffc21-120">Jos haluat käsitellä skenaariota käyttämällä tässä aiheessa esitettyjä arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu vakiodemotiedot.</span><span class="sxs-lookup"><span data-stu-id="ffc21-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="ffc21-121">Sinun on myös valittava **USMF**-yritys.</span><span class="sxs-lookup"><span data-stu-id="ffc21-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="ffc21-122">Skenaario käyttää varastoa *51* demotiedoista.</span><span class="sxs-lookup"><span data-stu-id="ffc21-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffc21-123">Ennen kuin vapautat tilaukset varastoon, varmista, että poiminnan sijainneissa on tarpeeksi varastoa tilausten kaikille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="ffc21-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="ffc21-124">Oletusarvoiset USMF-tiedot tukevat tätä skenaariota.</span><span class="sxs-lookup"><span data-stu-id="ffc21-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="ffc21-125">Mikäli et käytä demodataa, tarkista **Toimipaikkadirektiivi**-asetus nähdäksesi mitä keräilysijainteja myyntitilausten keräilyyn käytetään.</span><span class="sxs-lookup"><span data-stu-id="ffc21-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="ffc21-126">Jos sinun on muokattava varastoa, voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai mitä tahansa muuta virtausta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="ffc21-127">Määritä varaston mobiililaitteen valikkonimike</span><span class="sxs-lookup"><span data-stu-id="ffc21-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="ffc21-128">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ffc21-129">Valitse mobiililaitteen valikkovaihtoehtojen luettelosta **Myyntikeräily – Järjestelmä**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="ffc21-130">Tarvittava valikkovaihtoehto on jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="ffc21-131">Vahvista seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ffc21-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="ffc21-132">**Yleinen**-pikavälilehdessä **Ohjaus**-kentän arvoksi tulee määrittää *Järjestelmäohjattu*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="ffc21-133">**Työluokat**-pikavälilehdessä pitäisi näkyä seuraavat asetukset.</span><span class="sxs-lookup"><span data-stu-id="ffc21-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="ffc21-134">Työluokan tunnus</span><span class="sxs-lookup"><span data-stu-id="ffc21-134">Work class ID</span></span> | <span data-ttu-id="ffc21-135">Työtilaustyyppi</span><span class="sxs-lookup"><span data-stu-id="ffc21-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="ffc21-136">Sales</span><span class="sxs-lookup"><span data-stu-id="ffc21-136">Sales</span></span> | <span data-ttu-id="ffc21-137">Myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="ffc21-137">Sales orders</span></span> |
        | <span data-ttu-id="ffc21-138">Myyntitilauksen keräily</span><span class="sxs-lookup"><span data-stu-id="ffc21-138">SO Pick</span></span> | <span data-ttu-id="ffc21-139">Myyntitilaukset</span><span class="sxs-lookup"><span data-stu-id="ffc21-139">Sales orders</span></span> |

1. <span data-ttu-id="ffc21-140">Valitse Toimintoruudussa **Järjestelmäohjattu työsarjakysely**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="ffc21-141">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-141">Select **Edit**.</span></span>
1. <span data-ttu-id="ffc21-142">Poista aiemmin luotu rivi ja vahvista toiminto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="ffc21-143">Valitse toimintoruudussa **Uusi** ja luo rivi.</span><span class="sxs-lookup"><span data-stu-id="ffc21-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="ffc21-144">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffc21-145">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="ffc21-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ffc21-146">**Kuvauskenttä:** *Työn määrä alle 20 ja laskeva*</span><span class="sxs-lookup"><span data-stu-id="ffc21-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="ffc21-147">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-147">Select **Save**.</span></span>
1. <span data-ttu-id="ffc21-148">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="ffc21-149">Laajenna **Liitokset**-välilehdessä liitoshierarkia näyttämään **Työrivit**-taulu.</span><span class="sxs-lookup"><span data-stu-id="ffc21-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="ffc21-150">Valitse **Työrivit**-taululiitos.</span><span class="sxs-lookup"><span data-stu-id="ffc21-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="ffc21-151">Valitse **Lisää taulun liitos**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="ffc21-152">Etsi näyttöön tulevasta luettelosta rivi, jolla on seuraavat asetukset, ja valitse se:</span><span class="sxs-lookup"><span data-stu-id="ffc21-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="ffc21-153">**Liitostila:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="ffc21-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="ffc21-154">**Suhde:** *Sijainnit (sijainti)*</span><span class="sxs-lookup"><span data-stu-id="ffc21-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="ffc21-155">Valitse **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-155">Select **Select**.</span></span>

    <span data-ttu-id="ffc21-156">Sijainnit lisätään taululiitokseen.</span><span class="sxs-lookup"><span data-stu-id="ffc21-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="ffc21-157">Valitse **Lajittelu**-välilehdessä **Lisää**, jos haluat lisätä rivin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="ffc21-158">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffc21-159">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ffc21-160">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ffc21-161">**Kenttä:** *Työmäärä* (Valitse näkyviin tulevassa sanomaruudussa **Kyllä**, jos haluat lisätä lajittelun tähän kenttään.)</span><span class="sxs-lookup"><span data-stu-id="ffc21-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="ffc21-162">**Hakusuunta:** *Nouseva*</span><span class="sxs-lookup"><span data-stu-id="ffc21-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="ffc21-163">Valitse **Alue**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ffc21-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="ffc21-164">Jos sekvensointi-kohtaan sisällytetään vain tietyt työehdot, voit määrittää ne **Alue**-välilehdessä. Tässä esimerkissä haluat sisällyttää vain työn, jonka määrä on pienempi kuin 20 kpl (alin mittayksikkö).</span><span class="sxs-lookup"><span data-stu-id="ffc21-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="ffc21-165">Huomaa, että jotkin rivit ovat jo mukana.</span><span class="sxs-lookup"><span data-stu-id="ffc21-165">Notice that some lines are already included.</span></span> <span data-ttu-id="ffc21-166">Näitä rivejä ei saa poistaa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="ffc21-167">Lisää rivi valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="ffc21-168">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffc21-169">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ffc21-170">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ffc21-171">**Kenttä:** *Varastotyön määrä*</span><span class="sxs-lookup"><span data-stu-id="ffc21-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="ffc21-172">**Kriteerit:** *\<20* (alle 20)</span><span class="sxs-lookup"><span data-stu-id="ffc21-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="ffc21-173">Lisää toinen rivi valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="ffc21-174">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffc21-175">**Taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ffc21-176">**Johdettu taulu:** *Työrivit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ffc21-177">**Kenttä:** *Työtyyppi*</span><span class="sxs-lookup"><span data-stu-id="ffc21-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="ffc21-178">**Ehdot:** *Keräily*</span><span class="sxs-lookup"><span data-stu-id="ffc21-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="ffc21-179">Lisää toinen rivi valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="ffc21-180">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ffc21-181">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ffc21-182">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="ffc21-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="ffc21-183">**Kenttä:** *Sijaintiprofiilin tunnus*</span><span class="sxs-lookup"><span data-stu-id="ffc21-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="ffc21-184">**Ehdot:** *!VAIHE*</span><span class="sxs-lookup"><span data-stu-id="ffc21-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="ffc21-185">Muista sisällyttää huutomerkki (*!*) *VAIHE*-ehdon eteen.</span><span class="sxs-lookup"><span data-stu-id="ffc21-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="ffc21-186">Valitse **OK** tallentaaksesi ja sulkeaksesi kyselyn.</span><span class="sxs-lookup"><span data-stu-id="ffc21-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="ffc21-187">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-187">Select **Save**.</span></span>
1. <span data-ttu-id="ffc21-188">Palaa **Mobiililaitteen valikkokohteet** -sivulle sulkemalla sivu.</span><span class="sxs-lookup"><span data-stu-id="ffc21-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="ffc21-189">Tämä asetus määrittää kriteerit, joita käytetään tukikelpoisen työn syöttämisille mobiililaitteen valikkokohteeseen.</span><span class="sxs-lookup"><span data-stu-id="ffc21-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="ffc21-190">Jos lisäät kyselyyn ehtoja, järjestelmä käyttää kyselyriviä, jonka järjestysnumero on pienin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="ffc21-191">Toisin sanoen kaikki sarjanumeron 1 tukikelpoiset työt esitetään käyttäjälle ensin ja kaikki järjestysnumeron 2 työt sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ffc21-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="ffc21-192">Näin ollen, jos tiettyä aluetta ja lajittelua on käytettävä yhdessä, ne on määritettävä samassa järjestelmäohjatussa työsarjakyselyssä.</span><span class="sxs-lookup"><span data-stu-id="ffc21-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="ffc21-193">Tämä asetus poimii kaikki työt, joilla on vähintään yksi rivi, jonka määrä on pienempi kuin 20 kpl:tta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="ffc21-194">Jos työssä on rivi, jossa määrä on tasan 20 kpl:tta tai yli 20 kpl:tta, se on voimassa, jos sillä on myös vähintään yksi rivi, jossa määrä on pienempi kuin 20 kpl:tta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="ffc21-195">Sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="ffc21-195">Location directives</span></span>

<span data-ttu-id="ffc21-196">Jos käytät Contoso-oletustietoja, sijaintidirektiivitoiminnon kysely ei edellytä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="ffc21-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="ffc21-197">Voit kuitenkin varmistaa, että sijaintidirektiivit keräävät myyntitilausten nimikkeet, kun käytät ominaisuutta muussa kuin Contoso-ympäristössä, luomalla uuden sijaintidirektiivin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="ffc21-198">Voit tarkistaa asetukset demoympäristössä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ffc21-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="ffc21-199">Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="ffc21-200">Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="ffc21-201">Valitse sijaintidirektiivi, jonka nimi on *Poiminta 51*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="ffc21-202">Valitse **Sijaintidirektiivin toiminnot** -pikavälilehdessä rivi **Poiminta**-toiminnolle.</span><span class="sxs-lookup"><span data-stu-id="ffc21-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="ffc21-203">Valitse ruudukon yläpuolelta **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="ffc21-204">Tarkista **Alue**-kysely.</span><span class="sxs-lookup"><span data-stu-id="ffc21-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="ffc21-205">Etsi rivi, jonka **Kenttä**-kentän arvoksi on määritetty *Sijainti*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="ffc21-206">Varmista, että **Ehto**-kenttä on tyhjä (rajoituksia ei ole).</span><span class="sxs-lookup"><span data-stu-id="ffc21-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="ffc21-207">Skenaario</span><span class="sxs-lookup"><span data-stu-id="ffc21-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="ffc21-208">Myyntitilauksen keräystyön luominen</span><span class="sxs-lookup"><span data-stu-id="ffc21-208">Create sales order picking work</span></span>

<span data-ttu-id="ffc21-209">Ennen järjestelmän ohjaamaa keräilyä on luotava jokin lähtevä työ.</span><span class="sxs-lookup"><span data-stu-id="ffc21-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="ffc21-210">Tässä skenaariossa luodaan neljä myyntitilausta, jotka perustuvat määritettyihin järjestelmäohjattuihin työsarjakyselyihin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="ffc21-211">Kullekin myyntitilaukselle varataan varastomäärät.</span><span class="sxs-lookup"><span data-stu-id="ffc21-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="ffc21-212">Tästä syystä varattua varastoa ei voida käyttää varastosta muita tilauksia varten, jollei varausta tai osaa siitä peruta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="ffc21-213">Tämän jälkeen kukin myyntitilaus vapautetaan varastoon, jotta lähtevä työ voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="ffc21-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="ffc21-214">Myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="ffc21-214">Sales order 1</span></span>

1. <span data-ttu-id="ffc21-215">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ffc21-216">Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 1.</span><span class="sxs-lookup"><span data-stu-id="ffc21-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="ffc21-217">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffc21-218">Aseta **Asiakas**-osassa **Asiakastili**-kentän arvoksi *US-004*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="ffc21-219">Aseta **Yleinen**-osassa **Varasto**-kentässä arvoksi *51*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="ffc21-220">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffc21-221">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffc21-222">Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-223">**Nimiketunnus:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffc21-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffc21-224">**Määrä** *20*</span><span class="sxs-lookup"><span data-stu-id="ffc21-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="ffc21-225">Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="ffc21-226">Valitse **Varaus**-sivulla **Varaa erä** voidaksesi tehdä varauksia varastosta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="ffc21-227">Sulje **Varaus**-sivu.</span><span class="sxs-lookup"><span data-stu-id="ffc21-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="ffc21-228">Luo työ varastolle valitsemalla toimintoruudun **Varasto**-välilehdessä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="ffc21-229">Näyttöön tulee tiedotteita, joissa kerrotaan, että tilaukselle on luotu aallon tunnus ja lähetystunnus.</span><span class="sxs-lookup"><span data-stu-id="ffc21-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="ffc21-230">Myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="ffc21-230">Sales order 2</span></span>

1. <span data-ttu-id="ffc21-231">Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 2.</span><span class="sxs-lookup"><span data-stu-id="ffc21-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="ffc21-232">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffc21-233">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="ffc21-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="ffc21-234">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="ffc21-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ffc21-235">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffc21-236">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffc21-237">Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-238">**Nimiketunnus:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffc21-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffc21-239">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="ffc21-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="ffc21-240">Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-241">**Nimiketunnus:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="ffc21-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="ffc21-242">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="ffc21-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="ffc21-243">Molempien rivien varausvarasto.</span><span class="sxs-lookup"><span data-stu-id="ffc21-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="ffc21-244">Tilauksen vapauttaminen varastoon.</span><span class="sxs-lookup"><span data-stu-id="ffc21-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="ffc21-245">Myyntitilaus 3</span><span class="sxs-lookup"><span data-stu-id="ffc21-245">Sales order 3</span></span>

1. <span data-ttu-id="ffc21-246">Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 3.</span><span class="sxs-lookup"><span data-stu-id="ffc21-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="ffc21-247">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffc21-248">**Asiakastili:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="ffc21-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="ffc21-249">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="ffc21-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ffc21-250">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffc21-251">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffc21-252">Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-253">**Nimiketunnus:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffc21-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffc21-254">**Määrä** *7*</span><span class="sxs-lookup"><span data-stu-id="ffc21-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="ffc21-255">Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-256">**Nimiketunnus:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="ffc21-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="ffc21-257">**Määrä** *8*</span><span class="sxs-lookup"><span data-stu-id="ffc21-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="ffc21-258">Molempien rivien varausvarasto.</span><span class="sxs-lookup"><span data-stu-id="ffc21-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="ffc21-259">Tilauksen vapauttaminen varastoon.</span><span class="sxs-lookup"><span data-stu-id="ffc21-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="ffc21-260">Myyntitilaus 4</span><span class="sxs-lookup"><span data-stu-id="ffc21-260">Sales order 4</span></span>

1. <span data-ttu-id="ffc21-261">Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 4.</span><span class="sxs-lookup"><span data-stu-id="ffc21-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="ffc21-262">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ffc21-263">**Asiakastili:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="ffc21-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="ffc21-264">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="ffc21-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ffc21-265">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="ffc21-266">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="ffc21-267">Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-268">**Nimiketunnus:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="ffc21-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="ffc21-269">**Määrä** *25*</span><span class="sxs-lookup"><span data-stu-id="ffc21-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="ffc21-270">Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ffc21-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="ffc21-271">**Nimiketunnus:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="ffc21-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="ffc21-272">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="ffc21-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="ffc21-273">Molempien rivien varausvarasto.</span><span class="sxs-lookup"><span data-stu-id="ffc21-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="ffc21-274">Tilauksen vapauttaminen varastoon.</span><span class="sxs-lookup"><span data-stu-id="ffc21-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="ffc21-275">Hanki luotujen töiden työtunnukset</span><span class="sxs-lookup"><span data-stu-id="ffc21-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="ffc21-276">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ffc21-277">Suodata **Varasto**-kenttä niin, että vain varasto *51* on näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="ffc21-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="ffc21-278">Luotuja työtunnuksia on oltava neljä.</span><span class="sxs-lookup"><span data-stu-id="ffc21-278">Four work IDs should have been created.</span></span> <span data-ttu-id="ffc21-279">Merkitse kunkin myyntitilauksen työtunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="ffc21-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="ffc21-280">Myyntitilauksen tunnus</span><span class="sxs-lookup"><span data-stu-id="ffc21-280">Sales order ID</span></span> | <span data-ttu-id="ffc21-281">Työ tunnus</span><span class="sxs-lookup"><span data-stu-id="ffc21-281">Work ID</span></span> | <span data-ttu-id="ffc21-282">Työn määrä</span><span class="sxs-lookup"><span data-stu-id="ffc21-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="ffc21-283">Myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="ffc21-283">Sales Order 1</span></span> | <span data-ttu-id="ffc21-284">Työtunnus 1</span><span class="sxs-lookup"><span data-stu-id="ffc21-284">Work ID 1</span></span> | <span data-ttu-id="ffc21-285">20 kpl:tta</span><span class="sxs-lookup"><span data-stu-id="ffc21-285">20 ea</span></span> |
    | <span data-ttu-id="ffc21-286">Myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="ffc21-286">Sales Order 2</span></span> | <span data-ttu-id="ffc21-287">Työtunnus 2</span><span class="sxs-lookup"><span data-stu-id="ffc21-287">Work ID 2</span></span> | <span data-ttu-id="ffc21-288">6 kpl:tta (molempien rivien summa)</span><span class="sxs-lookup"><span data-stu-id="ffc21-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="ffc21-289">Myyntitilaus 3</span><span class="sxs-lookup"><span data-stu-id="ffc21-289">Sales Order 3</span></span> | <span data-ttu-id="ffc21-290">Työtunnus 3</span><span class="sxs-lookup"><span data-stu-id="ffc21-290">Work ID 3</span></span> | <span data-ttu-id="ffc21-291">15 kpl:tta (molempien rivien summa)</span><span class="sxs-lookup"><span data-stu-id="ffc21-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="ffc21-292">Myyntitilaus 4</span><span class="sxs-lookup"><span data-stu-id="ffc21-292">Sales Order 4</span></span> | <span data-ttu-id="ffc21-293">Työtunnus 4</span><span class="sxs-lookup"><span data-stu-id="ffc21-293">Work ID 4</span></span> | <span data-ttu-id="ffc21-294">35 kpl:tta (molempien rivien summa)</span><span class="sxs-lookup"><span data-stu-id="ffc21-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="ffc21-295">Ennen kuin suoritat työnkulun mobiililaitteessa, varmista, että vain luomasi työ on *Avoin*-tilassa varastossa *51* ja työtilaustyyppi on *Myyntitilaus*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="ffc21-296">Muussa tapauksessa testin tulokset voivat vaihdella, koska järjestelmän suora poiminta sisältää kaikki tukikelpoiset työt.</span><span class="sxs-lookup"><span data-stu-id="ffc21-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="ffc21-297">Siirry kohtaan **Varaston hallinta \> Työ \> Lähtevä \> Avoin myyntityö**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="ffc21-298">Suodata **Avoin myyntityö** -ruudukossa **Varasto**-kenttä niin, että vain varasto *51* on näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="ffc21-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="ffc21-299">Vahvista, että vain aiemmin luomasi neljä työtunnusta näytetään.</span><span class="sxs-lookup"><span data-stu-id="ffc21-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="ffc21-300">Sulje **Työ**-sivu.</span><span class="sxs-lookup"><span data-stu-id="ffc21-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="ffc21-301">Mobiililaitteen työnkulun suoritus</span><span class="sxs-lookup"><span data-stu-id="ffc21-301">Mobile device flow execution</span></span>

<span data-ttu-id="ffc21-302">Järjestelmä syöttää asetusten perusteella käyttäjän työt, jotka lajitellaan suurimmasta työrivin määrästä pienimpään.</span><span class="sxs-lookup"><span data-stu-id="ffc21-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="ffc21-303">Jokaisella rivillä oleva määrä on pienempi kuin 20 kpl:tta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="ffc21-304">Muista, että tämä asetus poimii kaikki työt, joilla on vähintään yksi rivi, jonka määrä on pienempi kuin 20 kpl:tta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="ffc21-305">Jos työllä on toinen rivi, jossa määrä on tasan 20 kpl:tta tai yli 20 kpl:tta, se on myös voimassa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="ffc21-306">Mobiilisovellus</span><span class="sxs-lookup"><span data-stu-id="ffc21-306">Mobile app</span></span>

1. <span data-ttu-id="ffc21-307">Kirjaudu varastosovellukseen käyttäjänä varastossa *51*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="ffc21-308">Siirry kohtaan **Lähtevä \> Myynnin keräys - Järjestelmä**.</span><span class="sxs-lookup"><span data-stu-id="ffc21-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="ffc21-309">Poimintavaihe työtunnukselle *4* on esitetty.</span><span class="sxs-lookup"><span data-stu-id="ffc21-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="ffc21-310">Tämä työtunnus esitetään ensimmäisenä, koska järjestelmän ohjaama kyselyjärjestys on määritetty ja määrität, että työ on jaksotettava laskeutuvan työrivin määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="ffc21-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="ffc21-311">Täytä vaadittu poiminta ja aseta työtunnus suljettaessa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="ffc21-312">Seuraavaksi esitetään työtunnus *3*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="ffc21-313">Yksi sen työriveistä on seuraava järjestyksessä työrivin määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="ffc21-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="ffc21-314">Täytä poiminta ja aseta työtunnus suljettaessa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="ffc21-315">Seuraavaksi esitetään työtunnus *2*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="ffc21-316">Tämän työn poimintarivi on seuraava järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="ffc21-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="ffc21-317">Täytä poiminta ja aseta työtunnus suljettaessa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="ffc21-318">Lisätyötä ei tule esittää teille.</span><span class="sxs-lookup"><span data-stu-id="ffc21-318">No further work should be presented to you.</span></span> <span data-ttu-id="ffc21-319">Työtunnus *1* ei ole oikeutettu tähän mobiililaitteen valikkokohteeseen, koska kysely määrittää, että työotsikot otetaan huomioon vain, jos työrivien määrä on alle 20 kpl:tta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="ffc21-320">Vihjeitä</span><span class="sxs-lookup"><span data-stu-id="ffc21-320">Tips</span></span>

<span data-ttu-id="ffc21-321">Järjestelmän ohjaamat työsarjakyselyt ovat *sisältyviä*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="ffc21-322">On tärkeää, että muistat tämän seikan joissakin asennuksissa.</span><span class="sxs-lookup"><span data-stu-id="ffc21-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="ffc21-323">Haluat esimerkiksi, että tietty valikkovaihtoehto käsittelee vain työtä, jossa työyksikkö on *kpl*, ja määrität rajoituksen kyselyn **Alue**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ffc21-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="ffc21-324">Tässä tapauksessa kaikki työt, joissa vähintään yhden työrivin työyksiköksi on määritetty *kpl* syötetään työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="ffc21-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="ffc21-325">Tämän vuoksi työhön voi kuulua myös työ, jossa työriveillä on jokin muu työyksikkö kuin *kpl* (esimerkiksi *laatikko* tai *kuormalava*).</span><span class="sxs-lookup"><span data-stu-id="ffc21-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="ffc21-326">Kysely jättää pois vain sellaiset työt, joissa työyksiköksi ei ole määritetty *kpl*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="ffc21-327">Tämän skenaarion esimerkissä myös kysely kaappasi työtunnuksen *4*.</span><span class="sxs-lookup"><span data-stu-id="ffc21-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="ffc21-328">Kun se luotiin, lisättiin kaksi riviä: yksi 25 kpl:tta ja toinen 10 kpl:tta varten.</span><span class="sxs-lookup"><span data-stu-id="ffc21-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="ffc21-329">Työ on vielä esitetty käyttäjälle, koska vähintään yhden työrivin määrä on pienempi kuin 20 kpl:tta.</span><span class="sxs-lookup"><span data-stu-id="ffc21-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="ffc21-330">Skenaarion mukaan voit estää tämän ongelman käyttämällä työtaukoja.</span><span class="sxs-lookup"><span data-stu-id="ffc21-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
