---
title: Varastopaikoitus
description: Tässä ohjeaiheessa on tietoja varastopaikoitusta. Varastopaikoituksen avulla voit konsolidoida kysynnän nimikkeen ja mittayksikön mukaan tilauksista, joiden tila on tilattu, varattu tai vapautettu. Sen avulla varastopäälliköt voivat suunnitella poimintasijainnit älykkäästi, ennen kuin ne vapauttavat tilauksia varastoon ja luovat poimintatöitä.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0dd1f42b7bb337ccb65b7e4bdd9d307d074ae0d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838151"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="51c2b-105">Varastopaikoitus</span><span class="sxs-lookup"><span data-stu-id="51c2b-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51c2b-106">Käytettävissä on useita varastopaikoitustoimintoja, joiden avulla varastopäälliköt voivat suunnitella poimintasijainnit älykkäästi, ennen kuin he vapauttavat tilauksia varastoon ja luovat poimintatöitä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="51c2b-107">*Varastopaikoitustoiminnon* avulla voit konsolidoida kysynnän nimikkeen ja mittayksikön mukaan tilauksista, joiden tila on *tilattu*, *varattu* tai *vapautettu*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="51c2b-108">Luotua kysyntää voidaan sitten käyttää poimintaan käytettäviin paikkoihin määrän, yksikön, fyysisten dimensioiden, pysyvien sijaintien ja muiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="51c2b-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="51c2b-109">Kun poistosuunnitelma on luotu, voidaan luoda täydennystöitä, jotka tuovat sopivan määrän varastoa kuhunkin sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="51c2b-110">*Siirtotilausten varastopaikoitustoiminnon* avulla varastopäälliköt voivat täydentää keräilysijainteja sellaisten siirtotilausten kysynnän perusteella, joita ei ole vielä vapautettu varastoon.</span><span class="sxs-lookup"><span data-stu-id="51c2b-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="51c2b-111">Se varmistaa, että keräilysijainnit sisältävät kaikki nimikkeet, joita tarvitaan siirtotilauksissa, kun ne vapautetaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="51c2b-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="51c2b-112">Tämä toiminto edellyttää, että myös *varastopaikoitustoiminto* otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="51c2b-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="51c2b-113">*Varastopaikoituksen kohdistuksen parannustoiminto* lisää asetuksen malliriveille, joita *varaston paikoitustoiminto* käyttää.</span><span class="sxs-lookup"><span data-stu-id="51c2b-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="51c2b-114">Tämän asetuksen ansiosta järjestelmä voi ottaa nykyisen käytettävissä olevan varaston huomioon kohdesijainnissa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="51c2b-115">Tällä tavoin paikoitukselle luodaan ehkä vähemmän täydennyksiä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="51c2b-116">*Varastopaikoituksen kohdistuksen parannustoiminto* edellyttää, että myös *varaston paikoitustoiminto* otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="51c2b-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="51c2b-117">Sitä voidaan valinnaisesti käyttää yhdessä *siirtotilausten varastopaikoitustoiminnon* kanssa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="51c2b-118">Varastopaikoitustoimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="51c2b-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="51c2b-119">Nämä toiminnot otettava käyttöön järjestelmässä, ennen kuin niitä voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="51c2b-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="51c2b-120">Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="51c2b-121">Ota seuraavat toiminnot käyttöön tarpeen mukaan:</span><span class="sxs-lookup"><span data-stu-id="51c2b-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="51c2b-122">Varaston osastointiominaisuus</span><span class="sxs-lookup"><span data-stu-id="51c2b-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="51c2b-123">Siirtotilausten varastopaikoitus</span><span class="sxs-lookup"><span data-stu-id="51c2b-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="51c2b-124">*Varastopaikoitustoiminto* on otettava käyttöön ennen tätä toimintoa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="51c2b-125">Varastopaikoituksen kohdistuksen parannukset</span><span class="sxs-lookup"><span data-stu-id="51c2b-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="51c2b-126">*Varastopaikoitustoiminto* on otettava käyttöön ennen tätä toimintoa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="51c2b-127">Varastopaikoituksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="51c2b-127">Set up warehouse slotting</span></span>

<span data-ttu-id="51c2b-128">Varastopaikoitusta voi käyttää sen jälkeen, kun seuraavat elementit on määritetty järjestelmässä:</span><span class="sxs-lookup"><span data-stu-id="51c2b-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="51c2b-129">Paikoituksen mittayksikkötasot</span><span class="sxs-lookup"><span data-stu-id="51c2b-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="51c2b-130">Direktiivikoodit</span><span class="sxs-lookup"><span data-stu-id="51c2b-130">Directive codes</span></span>
- <span data-ttu-id="51c2b-131">Paikoitusmallit</span><span class="sxs-lookup"><span data-stu-id="51c2b-131">Slotting templates</span></span>
- <span data-ttu-id="51c2b-132">Sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="51c2b-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="51c2b-133">Mittayksikön määrittämistasojen luominen paikoitusta varten</span><span class="sxs-lookup"><span data-stu-id="51c2b-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="51c2b-134">Mittayksikön yksiköt mahdollistavat useiden mittayksiköiden ryhmittelyn paikoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="51c2b-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="51c2b-135">Jos esimerkiksi saman ruudun poiminta-alueelta poimitaan useita ruutuja, kullekin koolle voidaan määrittää yksi taso.</span><span class="sxs-lookup"><span data-stu-id="51c2b-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="51c2b-136">**Kullekin tasoyksikölle on luotava rivi jokaista mittayksikköä varten.**</span><span class="sxs-lookup"><span data-stu-id="51c2b-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="51c2b-137">Siirry kohtaan **Varaston hallinta \> Asetukset \> Täydennys \> Paikoituksen mittayksikkö tasot**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="51c2b-138">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-138">Select **New**.</span></span>
1. <span data-ttu-id="51c2b-139">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="51c2b-140">**Mittayksikön taso:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="51c2b-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="51c2b-141">**Kuvaus:** *Jokainen laatikkokuormalava*</span><span class="sxs-lookup"><span data-stu-id="51c2b-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="51c2b-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-142">Select **Save**.</span></span>
1. <span data-ttu-id="51c2b-143">Lisää uusi rivi ruudukkoon **Mittayksiköt**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="51c2b-144">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-145">**Yksikkö:** *Laatikko*</span><span class="sxs-lookup"><span data-stu-id="51c2b-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="51c2b-146">**Kuvaus:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="51c2b-147">Se täytetään automaattisesti, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="51c2b-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="51c2b-148">**Yksikköluokka:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="51c2b-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="51c2b-149">Valitse **Uusi** lisätäksesi toisen rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="51c2b-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="51c2b-150">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-151">**Yksikkö:** *ea*</span><span class="sxs-lookup"><span data-stu-id="51c2b-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="51c2b-152">**Kuvaus:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="51c2b-153">Se täytetään automaattisesti, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="51c2b-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="51c2b-154">**Yksikköluokka:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="51c2b-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="51c2b-155">Valitse **Uusi** lisätäksesi kolmannen rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="51c2b-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="51c2b-156">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-157">**Yksikkö:** *PL*</span><span class="sxs-lookup"><span data-stu-id="51c2b-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="51c2b-158">**Kuvaus:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="51c2b-159">Se täytetään automaattisesti, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="51c2b-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="51c2b-160">**Yksikköluokka:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="51c2b-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="51c2b-161">Tallenna taso valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="51c2b-162">Direktiivikoodin luominen paikoitusta varten</span><span class="sxs-lookup"><span data-stu-id="51c2b-162">Create a directive code for slotting</span></span>

<span data-ttu-id="51c2b-163">Sinun on valittava malliin liitettävä direktiivikoodi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="51c2b-164">Valitse **Varastonhallinta \> Asetukset \> Direktiivikoodit**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="51c2b-165">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="51c2b-166">Syötä **Direktiivikoodi**-kenttään koodi *Paikoitus*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="51c2b-167">Syötä **Direktiivin kuvaus** -kenttään koodi *Paikoitus*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="51c2b-168">Paikoituksen mallien käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="51c2b-168">Set up slotting templates</span></span>

<span data-ttu-id="51c2b-169">Kukin paikoitusmalli määrittää, miten varasto määritetään tietyn varaston sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="51c2b-170">Jokaisessa mallissa on oltava rivi kutakin paikoitusmääritystä varten.</span><span class="sxs-lookup"><span data-stu-id="51c2b-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="51c2b-171">Tämän osan ohjeiden avulla voit määrittää paikoitusmallien asetukset.</span><span class="sxs-lookup"><span data-stu-id="51c2b-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="51c2b-172">Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Paikotusmallit**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="51c2b-173">Luo malli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-173">Select **New** to create a template.</span></span>

<span data-ttu-id="51c2b-174">Seuraavaksi on määritettävä mallin ylätunniste, paikoitusmäärittelyt ja paikkadirektiivit, jotka on selitetty seuraavissa alikohdissa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="51c2b-175">Siirtotilausten paikoituksen määritys muistuttaa myyntitilausten paikoituksen määritystä, mutta **Kysyntätyyppi**-kentän asetus on *Siirtotilaukset* eikä *Myyntilaus*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="51c2b-176">Myyntitilauksen paikoitusmallin otsikon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="51c2b-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="51c2b-177">Määritä mallin otsikossa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="51c2b-178">**Paikoitusmalli:** _61_</span><span class="sxs-lookup"><span data-stu-id="51c2b-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="51c2b-179">**Kuvaus:** _61_</span><span class="sxs-lookup"><span data-stu-id="51c2b-179">**Description:** _61_</span></span>
    - <span data-ttu-id="51c2b-180">**Kysyntätyyppi:** *Myyntitilaus*</span><span class="sxs-lookup"><span data-stu-id="51c2b-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="51c2b-181">Tällä *myyntitilaukset* ja *siirtotilaukset* ovat ainoat tuetut kysyntätyypit.</span><span class="sxs-lookup"><span data-stu-id="51c2b-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="51c2b-182">Voit valita *Siirtotilaukset* vain, jos *Siirtotilausten varastopaikoitus* -toiminto on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="51c2b-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="51c2b-183">**Kysyntästrategia:** _Tilattu_</span><span class="sxs-lookup"><span data-stu-id="51c2b-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="51c2b-184">Tässä kentässä käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="51c2b-185">**Tilattu** – Myyntitilauksen koko tilatun määrän pitää olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="51c2b-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="51c2b-186">**Varattu** – Ainoastaan ne myyntitilausrivin määrät, jotka on varattu (fyysinen ja tilattu), pitää vaatia.</span><span class="sxs-lookup"><span data-stu-id="51c2b-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="51c2b-187">**Vapautettu** – vapautettua määrää on pidettävä kysyntänä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="51c2b-188">**Varasto**: _61_</span><span class="sxs-lookup"><span data-stu-id="51c2b-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="51c2b-189">**Salli aaltokysynnän käyttää varauksettoman määrän:** _Kyllä_</span><span class="sxs-lookup"><span data-stu-id="51c2b-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="51c2b-190">Voit myös määrittää kyselyn, joka rajaa arvioitavan kysynnän laajuuden.</span><span class="sxs-lookup"><span data-stu-id="51c2b-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="51c2b-191">Määritä paikoitusmääritykset kullekin mallille</span><span class="sxs-lookup"><span data-stu-id="51c2b-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="51c2b-192">Voit lisätä kullekin luotavalle myyntitilausmallille rivin kutakin paikoitusmääritystä varten seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="51c2b-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="51c2b-193">Lisää uusi mallirivi valitsemalla **Paikoitusmallin tiedot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="51c2b-194">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-195">**Järjestys:** _1_</span><span class="sxs-lookup"><span data-stu-id="51c2b-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="51c2b-196">**Kuvaus:** _Kiinteä sijainti_</span><span class="sxs-lookup"><span data-stu-id="51c2b-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="51c2b-197">**Vähimmäismäärä:** _1_</span><span class="sxs-lookup"><span data-stu-id="51c2b-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="51c2b-198">Tämä kenttä määrittää riville vaaditun kysynnän vähimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="51c2b-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="51c2b-199">**Enimmäismäärä** _1000000_</span><span class="sxs-lookup"><span data-stu-id="51c2b-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="51c2b-200">Tämä kenttä määrittää riville kelvollisen kysynnän enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="51c2b-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="51c2b-201">**Yksikkö:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="51c2b-202">Tämä kenttä määrittää mittayksikön, johon vähimmäis- ja enimmäismäärät viittaavat.</span><span class="sxs-lookup"><span data-stu-id="51c2b-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="51c2b-203">**Mittayksikön taso:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="51c2b-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="51c2b-204">Tämä kenttä määrittää riville kelvolliset kysynnän mittayksiköt.</span><span class="sxs-lookup"><span data-stu-id="51c2b-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="51c2b-205">(Lisätietoja on aiemmin tässä ohjeaiheessa olevassa [Määritä paikoituksen mittayksikön tasot](#unit-tiers) -osassa.)</span><span class="sxs-lookup"><span data-stu-id="51c2b-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="51c2b-206">**Määritä paikan kriteerit:** _Harkitse määrä_</span><span class="sxs-lookup"><span data-stu-id="51c2b-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="51c2b-207">Tässä kentässä käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="51c2b-208">**Oletetaan tyhjäksi** – Järjestelmä olettaa, että kaikki poiminta-alueen sijainnit ovat tyhjiä, eikä niiden pitäisi tarkistaa varastopaikkoja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="51c2b-209">**Tarkastele määrää** – Järjestelmän tulisi tarkistaa poiminta-alueen sijainnit varaston varalta ja sen tulisi ohittaa ne sijainnit, jotka eivät ole tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="51c2b-210">**Ota varastosaldo huomioon** – Järjestelmän on tarkistettava, onko missään kohdesijainnissa varaamattomia määriä kysyntärivin nimikettä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="51c2b-211">Jos määrä on riittävän suuri tyydyttämään aikakin yhden kysyntärivin yksikön, käytettävissä oleva määrä vähennetään luodusta paikoitussuunnitelmatietueesta.</span><span class="sxs-lookup"><span data-stu-id="51c2b-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="51c2b-212">Jos kysyntä on esimerkiksi 10 laatikkoa ja varastosaldo on yksi laatikko, etsittävä kysyntä on yhdeksän laatikkoa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="51c2b-213">Jos kysyntä on 10 laatikkoa ja varastosaldo on yksi kutakin, etsittävä kysyntä on 10 laatikkoa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="51c2b-214">Tämä arvo on käytettävissä vain, kun *Varastopaikoituksen kohdistuksen parannukset* -toiminto on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="51c2b-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="51c2b-215">**Direktiivikoodi:** _Paikoitus_</span><span class="sxs-lookup"><span data-stu-id="51c2b-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="51c2b-216">Tämä kenttä määrittää sijaintidirektiivin, jota käytetään täydennystyön poimintasijainnin etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="51c2b-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="51c2b-217">**Ylivuotosijainti:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="51c2b-218">Tämä kenttä määrittää sijainnin, johon varasto kohdistetaan, jos määrälle ei löydy sijaintia rivin käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="51c2b-219">**Salli päästää ylös:** _Kyllä_</span><span class="sxs-lookup"><span data-stu-id="51c2b-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="51c2b-220">Kun tämän vaihtoehdon arvoksi on asetettu *Kyllä*, jos mitään kysyntää ei voi paikoittaa, siirtotyöt luodaan, jotta voidaan ottaa varasto pois sijainneista, joissa on varasto, mutta joissa mitään ei paikoitettu.</span><span class="sxs-lookup"><span data-stu-id="51c2b-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="51c2b-221">Malli suoritetaan sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="51c2b-221">The template is then run again.</span></span> <span data-ttu-id="51c2b-222">Tällä kertaa se ohittaa sijaintien varaston.</span><span class="sxs-lookup"><span data-stu-id="51c2b-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="51c2b-223">Tämä toiminto toimii parhaiten, kun **Määritä lähtöpaikkakriteerit** -kentän arvoksi on määritetty _Harkitse määrä_.</span><span class="sxs-lookup"><span data-stu-id="51c2b-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="51c2b-224">**Kiinteän sijainnin käyttö:** _Vain tuotteen kiinteät sijainnit_</span><span class="sxs-lookup"><span data-stu-id="51c2b-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="51c2b-225">Tässä kentässä käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="51c2b-226">**Kiinteät ja ei-vahvistetut sijainnit** – Järjestelmä ei saa rajoittua käyttämään vain kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="51c2b-227">**Vain tuotteen kiinteät sijainnit** – Järjestelmän tulisi paikoittaa vain sellaisia sijainteja, jotka ovat tuotteen kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="51c2b-228">**Vain tuotevariantin kiinteät sijainnit** – Järjestelmän tulisi paikoittaa vain sellaisia sijainteja, jotka ovat tuotevariantin kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="51c2b-229">Jos paikoitusmallissa on ainakin yksi rivi, jossa **Määritä paikan ehdot** -kentän asetuksena on *Ota varastosaldo huomioon*, helpotuksia ei enää sallita millään mallin rivillä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="51c2b-230">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-230">Select **Save**.</span></span>
1. <span data-ttu-id="51c2b-231">Luo toinen mallirivi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="51c2b-232">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-233">**Järjestys:** _2_</span><span class="sxs-lookup"><span data-stu-id="51c2b-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="51c2b-234">**Kuvaus:** _Muut_</span><span class="sxs-lookup"><span data-stu-id="51c2b-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="51c2b-235">**Vähimmäismäärä:** _1_</span><span class="sxs-lookup"><span data-stu-id="51c2b-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="51c2b-236">**Enimmäismäärä:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="51c2b-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="51c2b-237">**Yksikkö:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="51c2b-238">**Mittayksikön taso:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="51c2b-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="51c2b-239">**Määritä paikan kriteerit:** _Harkitse määrä_</span><span class="sxs-lookup"><span data-stu-id="51c2b-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="51c2b-240">**Direktiivikoodi:** _Paikoitus_</span><span class="sxs-lookup"><span data-stu-id="51c2b-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="51c2b-241">**Ylivuotosijainti:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="51c2b-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="51c2b-242">**Salli päästää ylös:** _Kyllä_</span><span class="sxs-lookup"><span data-stu-id="51c2b-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="51c2b-243">**Käytä kiinteitä sijainteja:** _Kiinteät ja muut kuin kiinteät sijainnit_</span><span class="sxs-lookup"><span data-stu-id="51c2b-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="51c2b-244">Toisen rivin kyselyssä määritetään nyt ehdot, joiden perusteella voidaan määrittää, mihin sijainteihin kyseisen rivin kysyntä voidaan paikoittaa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="51c2b-245">Valitse rivi, jonka **Järjestys**-kentän arvoksi on määritetty *2*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="51c2b-246">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="51c2b-247">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="51c2b-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="51c2b-248">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-249">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="51c2b-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="51c2b-250">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="51c2b-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="51c2b-251">**Kenttä:** *Sijaintiprofiilin tunnus*</span><span class="sxs-lookup"><span data-stu-id="51c2b-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="51c2b-252">**Ehdot:** *Poiminta-06* (Valitse kentässä kaksinkertainen plusmerkki \[**++**\] laajentaaksesi luettelon ja valitse sitten *Poiminta-06* - *Poimintatoimipaikka 6*.)</span><span class="sxs-lookup"><span data-stu-id="51c2b-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="51c2b-253">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="51c2b-254">Määritä sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="51c2b-254">Set up location directives</span></span>

<span data-ttu-id="51c2b-255">On määritettävä vähintään yksi sijaintidirektiivi, joka tukee paikoituksen poimintoja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="51c2b-256">Tässä osassa olevien ohjeiden avulla voit määrittää uuden *Varastopoimintojen täydennyssijaintidirektiivin*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="51c2b-257">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="51c2b-258">Valitse vasemman ruudun **Työtilaustyyppi**-kentässä *Täydennys*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="51c2b-259">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="51c2b-260">Kirjoita uuden sijaintidirektiivin otsikkoon **Nimi**-kenttään *61 paikoituspoiminta*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="51c2b-261">Hyväksy **Järjestysnumero**-kentässä oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="51c2b-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="51c2b-262">Määritä Sijaintidirektiivit-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="51c2b-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="51c2b-263">Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="51c2b-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="51c2b-264">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="51c2b-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="51c2b-265">**Työtyyppi:** _Poiminta_</span><span class="sxs-lookup"><span data-stu-id="51c2b-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="51c2b-266">**Toimipaikka:** _6_</span><span class="sxs-lookup"><span data-stu-id="51c2b-266">**Site:** _6_</span></span>
    - <span data-ttu-id="51c2b-267">**Varasto**: _61_</span><span class="sxs-lookup"><span data-stu-id="51c2b-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="51c2b-268">**Direktiivikoodi:** _Paikoitus_</span><span class="sxs-lookup"><span data-stu-id="51c2b-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="51c2b-269">Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="51c2b-270">Määritä Rivit-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="51c2b-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="51c2b-271">Luo uusi rivi valitsemalla **Rivit**-pikavälilehdellä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="51c2b-272">Määritä uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="51c2b-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="51c2b-273">**Määrästä:** _0_</span><span class="sxs-lookup"><span data-stu-id="51c2b-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="51c2b-274">**Määrälle:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="51c2b-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="51c2b-275">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="51c2b-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="51c2b-276">Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="51c2b-277">Määritä Direktiivitoiminnot-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="51c2b-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="51c2b-278">Luo uusi rivi valitsemalla **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="51c2b-279">Määritä uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="51c2b-279">On the new line, set the following values.</span></span> <span data-ttu-id="51c2b-280">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="51c2b-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="51c2b-281">**Järjestysnumero:** Hyväksy oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="51c2b-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="51c2b-282">**Nimi:** _Bulkki_</span><span class="sxs-lookup"><span data-stu-id="51c2b-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="51c2b-283">**Strategia:** _Ei mitään_</span><span class="sxs-lookup"><span data-stu-id="51c2b-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="51c2b-284">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="51c2b-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="51c2b-285">Valitse **Tallenna**, jos haluat, että **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="51c2b-286">Muokkaa kyselyä</span><span class="sxs-lookup"><span data-stu-id="51c2b-286">Edit the query</span></span>

1. <span data-ttu-id="51c2b-287">Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="51c2b-288">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="51c2b-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="51c2b-289">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-290">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="51c2b-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="51c2b-291">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="51c2b-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="51c2b-292">**Kenttä:** *Alueen tunnus*</span><span class="sxs-lookup"><span data-stu-id="51c2b-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="51c2b-293">**Ehdot:** *Bulkki* (Valitse kentässä kaksinkertainen plusmerkki \[**++**\] laajentaaksesi luettelon ja valitse sitten *Bulkki*.)</span><span class="sxs-lookup"><span data-stu-id="51c2b-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="51c2b-294">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="51c2b-295">Skenaario</span><span class="sxs-lookup"><span data-stu-id="51c2b-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="51c2b-296">Määritä skenaario</span><span class="sxs-lookup"><span data-stu-id="51c2b-296">Set up the scenario</span></span>

<span data-ttu-id="51c2b-297">Tässä skenaariossa voit käyttää valmiita mallitietoja ja luoda tässä osassa kuvatut tiedot.</span><span class="sxs-lookup"><span data-stu-id="51c2b-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="51c2b-298">Käytä USMF-mallitietoja</span><span class="sxs-lookup"><span data-stu-id="51c2b-298">Use the USMF sample data</span></span>

<span data-ttu-id="51c2b-299">Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="51c2b-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="51c2b-300">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="51c2b-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="51c2b-301">Luo kysyntää</span><span class="sxs-lookup"><span data-stu-id="51c2b-301">Create demand</span></span>

<span data-ttu-id="51c2b-302">Noudattamalla näitä ohjeita voit luoda kysynnän, johon paikoitus kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="51c2b-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="51c2b-303">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="51c2b-304">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="51c2b-305">Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä _US-007_.</span><span class="sxs-lookup"><span data-stu-id="51c2b-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="51c2b-306">Valitse **Varasto**-kentässä _61_.</span><span class="sxs-lookup"><span data-stu-id="51c2b-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="51c2b-307">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-307">Select **OK**.</span></span>
1. <span data-ttu-id="51c2b-308">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="51c2b-308">The new sales order is opened.</span></span> <span data-ttu-id="51c2b-309">**Myyntitilausrivit**-pikavälilehti sisältää tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="51c2b-310">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-311">**Nimike:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="51c2b-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="51c2b-312">**Määrä** _20_</span><span class="sxs-lookup"><span data-stu-id="51c2b-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="51c2b-313">Lisää uusin rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="51c2b-314">**Nimike:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="51c2b-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="51c2b-315">**Määrä** _8_</span><span class="sxs-lookup"><span data-stu-id="51c2b-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="51c2b-316">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-316">Select **Save**.</span></span>
1. <span data-ttu-id="51c2b-317">Luo toinen myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="51c2b-318">Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä _US-008_.</span><span class="sxs-lookup"><span data-stu-id="51c2b-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="51c2b-319">Valitse **Varasto**-kentässä _61_.</span><span class="sxs-lookup"><span data-stu-id="51c2b-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="51c2b-320">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="51c2b-320">The new sales order is opened.</span></span> <span data-ttu-id="51c2b-321">**Myyntitilausrivit**-pikavälilehti sisältää tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="51c2b-322">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="51c2b-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="51c2b-323">**Nimike:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="51c2b-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="51c2b-324">**Määrä** _1_</span><span class="sxs-lookup"><span data-stu-id="51c2b-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="51c2b-325">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="51c2b-326">Käy läpi tyypillinen paikoitusskenaario</span><span class="sxs-lookup"><span data-stu-id="51c2b-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="51c2b-327">Kun kaikki vaaditut elementit on määritetty edellisessä osassa kuvatulla tavalla, voit kokeilla toimintoa käyttämällä tässä osiossa kuvattuja harjoituksia.</span><span class="sxs-lookup"><span data-stu-id="51c2b-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="51c2b-328">Luo kysyntä</span><span class="sxs-lookup"><span data-stu-id="51c2b-328">Generate demand</span></span>

1. <span data-ttu-id="51c2b-329">Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Paikoitusmallit** ja valitse paikoitusmalli, jonka loit aiemmin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="51c2b-330">Valitse toimintoruudussa **Luo kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="51c2b-331">Tämä komento arvioi kaiken järjestelmässä olevan kysynnän ja joka vastaa paikoitusmallikyselyä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="51c2b-332">Kaikkien tilausten kokonaiskysyntä yhdistetään sitten yhdelle riville määrää/mittayksikköä kohden.</span><span class="sxs-lookup"><span data-stu-id="51c2b-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="51c2b-333">Kun prosessi on päättynyt, näkyviin tulee tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="51c2b-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="51c2b-334">Paikoituksen kysyntä</span><span class="sxs-lookup"><span data-stu-id="51c2b-334">Slotting demand</span></span>

<span data-ttu-id="51c2b-335">*Paikoituskysyntä* näyttää kysynnän luonnin tulokset, jotka perustuvat paikoitusmallin asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="51c2b-336">Jos haluat tarkastella **Luo kysyntä** -komennon tuloksia, valitse toimintoruudusta **Paikoituskysyntä**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="51c2b-337">Paikoituskysynnän rivejä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="51c2b-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="51c2b-338">Voit poistaa rivin, lisätä uuden rivin tai muokata rivin tietoja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="51c2b-339">Voit muokata kysyntää manuaalisesti tai voit tuoda sen ulkoisesta järjestelmästä käyttämällä tietojen hallintaa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="51c2b-340">Mitä paikoituskysynnässä onkaan, sitä käytetään seuraavassa vaiheessa, riippumatta siitä, mistä se on peräisin.</span><span class="sxs-lookup"><span data-stu-id="51c2b-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="51c2b-341">Etsi kysyntä</span><span class="sxs-lookup"><span data-stu-id="51c2b-341">Locate demand</span></span>

<span data-ttu-id="51c2b-342">Kun kysyntä on luotu, sinun on luotava *paikoitussuunnitelma* käyttämällä **Paikanna kysyntä** -komentoa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="51c2b-343">Valitse toimintoruudussa **Etsi kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="51c2b-344">Paikoitusprosessi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="51c2b-344">The slotting process runs.</span></span> <span data-ttu-id="51c2b-345">Kun prosessi on päättynyt, näkyviin tulee tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="51c2b-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="51c2b-346">Paikoitussuunnitelma</span><span class="sxs-lookup"><span data-stu-id="51c2b-346">Slotting plan</span></span>

<span data-ttu-id="51c2b-347">Paikoitussuunnitelmassa näkyy sijainti, johon kukin nimike/määrä on liitetty, riippumatta siitä, oliko ylivuoto käytössä, onko lisätyötä luotu, ja mitä malliriviä on käytetty.</span><span class="sxs-lookup"><span data-stu-id="51c2b-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="51c2b-348">*Kaikki vaatimukset, joita ei ole voitu paikoittaa on korostettu punaisella.*</span><span class="sxs-lookup"><span data-stu-id="51c2b-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="51c2b-349">Tarkastele tuloksia valitsemalla Toimintoruudussa **Paikoitussuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="51c2b-350">**Luo kysyntä**-, **Etsi kysyntä**- ja **Suorita täydennykset** -prosessit suoritaan nyt eristysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="51c2b-351">(Nämä prosessit ovat käytettävissä **Paikoitusmallit**-sivun toimintoruudussa.)</span><span class="sxs-lookup"><span data-stu-id="51c2b-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="51c2b-352">**Luo kysyntä**-, **Etsi kysyntä**- ja **Suorita täydennykset** -prosessien lukitus varmistaa, että niitä ei käynnistetä samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="51c2b-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="51c2b-353">Muutoin käytetyt tiedot voitaisiin poistaa.</span><span class="sxs-lookup"><span data-stu-id="51c2b-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="51c2b-354">**Luo kysyntä**- ja **Etsi kysyntä** -prosessit näyttävät varoituksen, jos suoritus luonut tietueita tai jos tietueista puuttuu tietoja.</span><span class="sxs-lookup"><span data-stu-id="51c2b-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="51c2b-355">Kun **Paikoitussuunnitelma** valitaan, sivun toimintoruudussa ei ole **Uusi**-, **Muokkaa**- tai **Poista**-painikkeita, koska tietolähdettä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="51c2b-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="51c2b-356">Kun **Suorita täydennykset** valitaan, järjestelmä tarkistaa valitun paikkamallin ja prosessit.</span><span class="sxs-lookup"><span data-stu-id="51c2b-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="51c2b-357">Luo täydennys</span><span class="sxs-lookup"><span data-stu-id="51c2b-357">Create replenishment</span></span>

<span data-ttu-id="51c2b-358">Kun paikoitussuunnitelma on luotu, suunnitelman perusteella on luotava *Täydennystyöt*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="51c2b-359">Valitse toimintoruudussa **Suorita täydennykset**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="51c2b-360">Kun prosessi on päättynyt, näkyviin tulee tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="51c2b-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="51c2b-361">Tämä sanoma ilmaisee työn koontiversiotunnukselle luotujen otsikoiden määrän.</span><span class="sxs-lookup"><span data-stu-id="51c2b-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="51c2b-362">Käytettävät sijaintidirektiivit määritetään kullekin malliriville määritetyn direktiivikoodin perusteella.</span><span class="sxs-lookup"><span data-stu-id="51c2b-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="51c2b-363">Vihjeitä</span><span class="sxs-lookup"><span data-stu-id="51c2b-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="51c2b-364">Automaattisen paikoituksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="51c2b-364">Set up automatic slotting</span></span>

<span data-ttu-id="51c2b-365">Kun kaikki vaaditut elementit ovat paikoillaan, voit määrittää tilauksen suoritettavaksi automaattisesti noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="51c2b-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="51c2b-366">Valitse **Varastonhallinta \> Täydennys \> Suorita paikoitus**.</span><span class="sxs-lookup"><span data-stu-id="51c2b-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="51c2b-367">Määritä suoritettavan työn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="51c2b-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="51c2b-368">Valitse yksi tai useampi seuraavista paikoitusvaiheista:</span><span class="sxs-lookup"><span data-stu-id="51c2b-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="51c2b-369">Luo kysyntä</span><span class="sxs-lookup"><span data-stu-id="51c2b-369">Generate demand</span></span>
    - <span data-ttu-id="51c2b-370">Etsi kysyntä</span><span class="sxs-lookup"><span data-stu-id="51c2b-370">Locate demand</span></span>
    - <span data-ttu-id="51c2b-371">Luo täydennystyö</span><span class="sxs-lookup"><span data-stu-id="51c2b-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="51c2b-372">Paikoitusvaiheet ovat edistyksellisiä.</span><span class="sxs-lookup"><span data-stu-id="51c2b-372">The slotting steps are progressive.</span></span> <span data-ttu-id="51c2b-373">Jos haluat valita *Paikanna kysyntä*, sinun on ensin valittava *Luo kysyntää*.</span><span class="sxs-lookup"><span data-stu-id="51c2b-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="51c2b-374">Määritä käytettävä paikoitusmalli.</span><span class="sxs-lookup"><span data-stu-id="51c2b-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="51c2b-375">Voit halutessasi määrittää toistuvan ajon automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="51c2b-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="51c2b-376">Jos harjoitteet ovat skenaariossa, **älä** määritä automaattista paikoitusta.</span><span class="sxs-lookup"><span data-stu-id="51c2b-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]