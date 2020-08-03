---
title: Varastopaikoitus
description: Tässä ohjeaiheessa on tietoja varastopaikoitusta. Varastopaikoituksen avulla voit konsolidoida kysynnän nimikkeen ja mittayksikön mukaan tilauksista, joiden tila on tilattu, varattu tai vapautettu. Sen avulla varastopäälliköt voivat suunnitella poimintasijainnit älykkäästi, ennen kuin ne vapauttavat tilauksia varastoon ja luovat poimintatöitä.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f6764f8bc082962af37d4775b6fe53d8704658eb
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597455"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="f9bfd-105">Varastopaikoitus</span><span class="sxs-lookup"><span data-stu-id="f9bfd-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9bfd-106">Varastopaikoituksen avulla voit konsolidoida kysynnän nimikkeen ja mittayksikön mukaan tilauksista, joiden tila on *tilattu*, *varattu* tai *vapautettu*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="f9bfd-107">Luotua kysyntää voidaan sitten käyttää poimintaan käytettäviin paikkoihin määrän, yksikön, fyysisten dimensioiden, pysyvien sijaintien ja muiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="f9bfd-108">Kun poistosuunnitelma on luotu, voidaan luoda täydennystöitä, jotka tuovat sopivan määrän varastoa kuhunkin sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="f9bfd-109">Tämän toiminnon avulla varastopäälliköt voivat suunnitella poimintasijainnit älykkäästi, ennen kuin ne vapauttavat tilauksia varastoon ja luovat poimintatöitä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="f9bfd-110">Varastopaikoitusominaisuuden käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f9bfd-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="f9bfd-111">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="f9bfd-112">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f9bfd-113">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f9bfd-114">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f9bfd-115">**Ominaisuuden nimi:** *Varastopaikoitusominaisuus*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="f9bfd-116">Varastopaikoituksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f9bfd-116">Set up warehouse slotting</span></span>

<span data-ttu-id="f9bfd-117">Varastopaikoitusta voi käyttää sen jälkeen, kun seuraavat elementit on määritetty järjestelmässäsi:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="f9bfd-118">Mittayksikön määrittämistasojen luominen paikoitusta varten</span><span class="sxs-lookup"><span data-stu-id="f9bfd-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="f9bfd-119">Mittayksikön yksiköt mahdollistavat useiden mittayksiköiden ryhmittelyn paikoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="f9bfd-120">Jos esimerkiksi saman ruudun poiminta-alueelta poimitaan useita ruutuja, kullekin koolle voidaan määrittää yksi taso.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="f9bfd-121">**Kullekin tasoyksikölle on luotava rivi jokaista mittayksikköä varten.**</span><span class="sxs-lookup"><span data-stu-id="f9bfd-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="f9bfd-122">Siirry kohtaan **Varaston hallinta \> Asetukset \> Täydennys \> Paikoituksen mittayksikkö tasot**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="f9bfd-123">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-123">Select **New**.</span></span>
1. <span data-ttu-id="f9bfd-124">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-125">**Mittayksikön taso:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="f9bfd-126">**Kuvaus:** *Jokainen laatikkokuormalava*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="f9bfd-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-127">Select **Save**.</span></span>
1. <span data-ttu-id="f9bfd-128">Lisää uusi rivi ruudukkoon **Mittayksiköt**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f9bfd-129">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-130">**Yksikkö:** *Laatikko*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="f9bfd-131">**Kuvaus:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f9bfd-132">Se täytetään automaattisesti, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f9bfd-133">**Yksikköluokka:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f9bfd-134">Valitse **Uusi** lisätäksesi toisen rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="f9bfd-135">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-136">**Yksikkö:** *ea*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="f9bfd-137">**Kuvaus:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f9bfd-138">Se täytetään automaattisesti, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f9bfd-139">**Yksikköluokka:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f9bfd-140">Valitse **Uusi** lisätäksesi kolmannen rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="f9bfd-141">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-142">**Yksikkö:** *PL*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="f9bfd-143">**Kuvaus:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="f9bfd-144">Se täytetään automaattisesti, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="f9bfd-145">**Yksikköluokka:** *Määrä*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="f9bfd-146">Tallenna taso valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="f9bfd-147">Direktiivikoodin luominen paikoitusta varten</span><span class="sxs-lookup"><span data-stu-id="f9bfd-147">Create a directive code for slotting</span></span>

<span data-ttu-id="f9bfd-148">Sinun on valittava malliin liitettävä direktiivikoodi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="f9bfd-149">Valitse **Varastonhallinta \> Asetukset \> Direktiivikoodit**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="f9bfd-150">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f9bfd-151">Syötä **Direktiivikoodi**-kenttään koodi *Paikoitus*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="f9bfd-152">Syötä **Direktiivin kuvaus** -kenttään koodi *Paikoitus*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="f9bfd-153">Paikoituksen mallien käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f9bfd-153">Set up slotting templates</span></span>

<span data-ttu-id="f9bfd-154">Kukin paikoitusmalli määrittää, miten varasto määritetään tietyn varaston sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="f9bfd-155">Jokaisessa mallissa on oltava rivi kutakin paikoitusmääritystä varten.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="f9bfd-156">Tämän osan ohjeiden avulla voit määrittää paikoitusmallien asetukset.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="f9bfd-157">Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Paikotusmallit**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="f9bfd-158">Luo malli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-158">Select **New** to create a template.</span></span>

<span data-ttu-id="f9bfd-159">Seuraavaksi on määritettävä mallin ylätunniste, paikoitusmäärittelyt ja paikkadirektiivit, jotka on selitetty seuraavissa alikohdissa.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="f9bfd-160">Paikoitusmallin otsikon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f9bfd-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="f9bfd-161">Määritä mallin otsikossa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-162">**Paikoitusmalli:** _61_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="f9bfd-163">**Kuvaus:** _61_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-163">**Description:** _61_</span></span>
    - <span data-ttu-id="f9bfd-164">**Kysyntätyyppi:** *Myyntitilaus*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="f9bfd-165">Tällä hetkellä ainoa tuettu vaatimustyyppi on *Myyntitilaus*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="f9bfd-166">**Kysyntästrategia:** _Tilattu_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="f9bfd-167">Tässä kentässä käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="f9bfd-168">**Tilattu** – Myyntitilauksen koko tilatun määrän pitää olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="f9bfd-169">**Varattu** – Ainoastaan ne myyntitilausrivin määrät, jotka on varattu (fyysinen ja tilattu), pitää vaatia.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="f9bfd-170">**Varasto**: _61_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="f9bfd-171">**Salli aaltokysynnän käyttää varauksettoman määrän:** _Kyllä_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="f9bfd-172">Voit myös määrittää kyselyn, joka rajaa arvioitavan kysynnän laajuuden.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="f9bfd-173">Määritä paikoitusmääritykset kullekin mallille</span><span class="sxs-lookup"><span data-stu-id="f9bfd-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="f9bfd-174">Voit lisätä kullekin luotavalle mallille rivin kutakin paikoitusmääritystä varten seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="f9bfd-175">Lisää uusi mallirivi valitsemalla **Paikoitusmallin tiedot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="f9bfd-176">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-177">**Järjestys:** _1_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="f9bfd-178">**Kuvaus:** _Kiinteä sijainti_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="f9bfd-179">**Vähimmäismäärä:** _1_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="f9bfd-180">Tämä kenttä määrittää riville vaaditun kysynnän vähimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="f9bfd-181">**Enimmäismäärä** _1000000_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="f9bfd-182">Tämä kenttä määrittää riville kelvollisen kysynnän enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="f9bfd-183">**Yksikkö:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="f9bfd-184">Tämä kenttä määrittää mittayksikön, johon vähimmäis- ja enimmäismäärät viittaavat.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="f9bfd-185">**Mittayksikön taso:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="f9bfd-186">Tämä kenttä määrittää riville kelvolliset kysynnän mittayksiköt.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="f9bfd-187">(Lisätietoja on aiemmin tässä ohjeaiheessa olevassa [Määritä paikoituksen mittayksikön tasot](#unit-tiers) -osassa.)</span><span class="sxs-lookup"><span data-stu-id="f9bfd-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="f9bfd-188">**Määritä paikan kriteerit:** _Harkitse määrä_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="f9bfd-189">Tässä kentässä käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="f9bfd-190">**Oletetaan tyhjäksi** – Järjestelmä olettaa, että kaikki poiminta-alueen sijainnit ovat tyhjiä, eikä niiden pitäisi tarkistaa varastopaikkoja.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="f9bfd-191">**Tarkastele määrää** – Järjestelmän tulisi tarkistaa poiminta-alueen sijainnit varaston varalta ja sen tulisi ohittaa ne sijainnit, jotka eivät ole tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="f9bfd-192">**Direktiivikoodi:** _Paikoitus_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="f9bfd-193">Tämä kenttä määrittää sijaintidirektiivin, jota käytetään täydennystyön poimintasijainnin etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="f9bfd-194">**Ylivuotosijainti:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="f9bfd-195">Tämä kenttä määrittää sijainnin, johon varasto kohdistetaan, jos määrälle ei löydy sijaintia rivin käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="f9bfd-196">**Salli päästää ylös:** _Kyllä_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="f9bfd-197">Kun tämän vaihtoehdon arvoksi on asetettu *Kyllä*, jos mitään kysyntää ei voi paikoittaa, siirtotyöt luodaan, jotta voidaan ottaa varasto pois sijainneista, joissa on varasto, mutta joissa mitään ei paikoitettu.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="f9bfd-198">Malli suoritetaan sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-198">The template is then run again.</span></span> <span data-ttu-id="f9bfd-199">Tällä kertaa se ohittaa sijaintien varaston.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="f9bfd-200">Tämä toiminto toimii parhaiten, kun **Määritä lähtöpaikkakriteerit** -kentän arvoksi on määritetty _Harkitse määrä_.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="f9bfd-201">**Kiinteän sijainnin käyttö:** _Vain tuotteen kiinteät sijainnit_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="f9bfd-202">Tässä kentässä käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="f9bfd-203">**Kiinteät ja ei-vahvistetut sijainnit** – Järjestelmä ei saa rajoittua käyttämään vain kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="f9bfd-204">**Vain tuotteen kiinteät sijainnit** – Järjestelmän tulisi paikoittaa vain sellaisia sijainteja, jotka ovat tuotteen kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="f9bfd-205">**Vain tuotevariantin kiinteät sijainnit** – Järjestelmän tulisi paikoittaa vain sellaisia sijainteja, jotka ovat tuotevariantin kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="f9bfd-206">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-206">Select **Save**.</span></span>
1. <span data-ttu-id="f9bfd-207">Luo toinen mallirivi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="f9bfd-208">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-209">**Järjestys:** _2_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="f9bfd-210">**Kuvaus:** _Muut_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="f9bfd-211">**Vähimmäismäärä:** _1_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="f9bfd-212">**Enimmäismäärä:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="f9bfd-213">**Yksikkö:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="f9bfd-214">**Mittayksikön taso:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="f9bfd-215">**Määritä paikan kriteerit:** _Harkitse määrä_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="f9bfd-216">**Direktiivikoodi:** _Paikoitus_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="f9bfd-217">**Ylivuotosijainti:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="f9bfd-218">**Salli päästää ylös:** _Kyllä_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="f9bfd-219">**Käytä kiinteitä sijainteja:** _Kiinteät ja muut kuin kiinteät sijainnit_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="f9bfd-220">Toisen rivin kyselyssä määritetään nyt ehdot, joiden perusteella voidaan määrittää, mihin sijainteihin kyseisen rivin kysyntä voidaan paikoittaa.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="f9bfd-221">Valitse rivi, jonka **Järjestys**-kentän arvoksi on määritetty *2*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="f9bfd-222">Valitse **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="f9bfd-223">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f9bfd-224">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-225">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f9bfd-226">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f9bfd-227">**Kenttä:** *Sijaintiprofiilin tunnus*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="f9bfd-228">**Ehdot:** *Poiminta-06* (Valitse kentässä kaksinkertainen plusmerkki \[**++**\] laajentaaksesi luettelon ja valitse sitten *Poiminta-06* - *Poimintatoimipaikka 6*.)</span><span class="sxs-lookup"><span data-stu-id="f9bfd-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="f9bfd-229">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="f9bfd-230">Määritä sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="f9bfd-230">Set up location directives</span></span>

<span data-ttu-id="f9bfd-231">On määritettävä vähintään yksi sijaintidirektiivi, joka tukee paikoituksen poimintoja.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="f9bfd-232">Tässä osassa olevien ohjeiden avulla voit määrittää uuden *Varastopoimintojen täydennyssijaintidirektiivin*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="f9bfd-233">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f9bfd-234">Valitse vasemman ruudun **Työtilaustyyppi**-kentässä *Täydennys*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="f9bfd-235">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f9bfd-236">Kirjoita uuden sijaintidirektiivin otsikkoon **Nimi**-kenttään *61 paikoituspoiminta*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="f9bfd-237">Määritä Sijaintidirektiivit-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="f9bfd-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="f9bfd-238">Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="f9bfd-239">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f9bfd-240">**Työtyyppi:** _Poiminta_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="f9bfd-241">**Toimipaikka:** _6_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-241">**Site:** _6_</span></span>
    - <span data-ttu-id="f9bfd-242">**Varasto**: _61_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="f9bfd-243">**Direktiivikoodi:** _Paikoitus_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="f9bfd-244">Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="f9bfd-245">Määritä Rivit-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="f9bfd-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="f9bfd-246">Luo uusi rivi valitsemalla **Rivit**-pikavälilehdellä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="f9bfd-247">Määritä uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-247">On the new line, set the following values.</span></span> <span data-ttu-id="f9bfd-248">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f9bfd-249">**Määrästä:** _0_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="f9bfd-250">**Määrälle:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="f9bfd-251">Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="f9bfd-252">Määritä Direktiivitoiminnot-pikavälilehti</span><span class="sxs-lookup"><span data-stu-id="f9bfd-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="f9bfd-253">Luo uusi rivi valitsemalla **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="f9bfd-254">Määritä uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-254">On the new line, set the following values.</span></span> <span data-ttu-id="f9bfd-255">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="f9bfd-256">**Nimi:** _Bulkki_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="f9bfd-257">**Strategia:** _Ei mitään_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="f9bfd-258">Valitse **Tallenna**, jos haluat, että **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="f9bfd-259">Muokkaa kyselyä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-259">Edit the query</span></span>

1. <span data-ttu-id="f9bfd-260">Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="f9bfd-261">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="f9bfd-262">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-263">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f9bfd-264">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f9bfd-265">**Kenttä:** *Alueen tunnus*</span><span class="sxs-lookup"><span data-stu-id="f9bfd-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="f9bfd-266">**Ehdot:** *Bulkki* (Valitse kentässä kaksinkertainen plusmerkki \[**++**\] laajentaaksesi luettelon ja valitse sitten *Bulkki*.)</span><span class="sxs-lookup"><span data-stu-id="f9bfd-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="f9bfd-267">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="f9bfd-268">Skenaario</span><span class="sxs-lookup"><span data-stu-id="f9bfd-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="f9bfd-269">Määritä skenaario</span><span class="sxs-lookup"><span data-stu-id="f9bfd-269">Set up the scenario</span></span>

<span data-ttu-id="f9bfd-270">Tässä skenaariossa voit käyttää valmiita mallitietoja ja luoda tässä osassa kuvatut tiedot.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="f9bfd-271">Käytä USMF-mallitietoja</span><span class="sxs-lookup"><span data-stu-id="f9bfd-271">Use the USMF sample data</span></span>

<span data-ttu-id="f9bfd-272">Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f9bfd-273">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="f9bfd-274">Luo kysyntää</span><span class="sxs-lookup"><span data-stu-id="f9bfd-274">Create demand</span></span>

<span data-ttu-id="f9bfd-275">Noudattamalla näitä ohjeita voit luoda kysynnän, johon paikoitus kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="f9bfd-276">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="f9bfd-277">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f9bfd-278">Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä _US-007_.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="f9bfd-279">Valitse **Varasto**-kentässä _61_.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="f9bfd-280">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-280">Select **OK**.</span></span>
1. <span data-ttu-id="f9bfd-281">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-281">The new sales order is opened.</span></span> <span data-ttu-id="f9bfd-282">**Myyntitilausrivit**-pikavälilehti sisältää tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f9bfd-283">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-284">**Nimike:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="f9bfd-285">**Määrä** _20_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="f9bfd-286">Lisää uusin rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="f9bfd-287">**Nimike:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="f9bfd-288">**Määrä** _8_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="f9bfd-289">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-289">Select **Save**.</span></span>
1. <span data-ttu-id="f9bfd-290">Luo toinen myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="f9bfd-291">Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä _US-008_.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="f9bfd-292">Valitse **Varasto**-kentässä _61_.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="f9bfd-293">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-293">The new sales order is opened.</span></span> <span data-ttu-id="f9bfd-294">**Myyntitilausrivit**-pikavälilehti sisältää tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f9bfd-295">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="f9bfd-296">**Nimike:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="f9bfd-297">**Määrä** _1_</span><span class="sxs-lookup"><span data-stu-id="f9bfd-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="f9bfd-298">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="f9bfd-299">Käy läpi tyypillinen paikoitusskenaario</span><span class="sxs-lookup"><span data-stu-id="f9bfd-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="f9bfd-300">Kun kaikki vaaditut elementit on määritetty edellisessä osassa kuvatulla tavalla, voit kokeilla toimintoa käyttämällä tässä osiossa kuvattuja harjoituksia.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="f9bfd-301">Luo kysyntä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-301">Generate demand</span></span>

1. <span data-ttu-id="f9bfd-302">Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Paikoitusmallit** ja valitse paikoitusmalli, jonka loit aiemmin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="f9bfd-303">Valitse toimintoruudussa **Luo kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="f9bfd-304">Tämä komento arvioi kaiken järjestelmässä olevan kysynnän ja joka vastaa paikoitusmallikyselyä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="f9bfd-305">Kaikkien tilausten kokonaiskysyntä yhdistetään sitten yhdelle riville määrää/mittayksikköä kohden.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="f9bfd-306">Kun prosessi on päättynyt, näkyviin tulee tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="f9bfd-307">Paikoituksen kysyntä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-307">Slotting demand</span></span>

<span data-ttu-id="f9bfd-308">*Paikoituskysyntä* näyttää kysynnän luonnin tulokset, jotka perustuvat paikoitusmallin asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="f9bfd-309">Jos haluat tarkastella **Luo kysyntä** -komennon tuloksia, valitse toimintoruudusta **Paikoituskysyntä**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="f9bfd-310">Paikoituskysynnän rivejä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="f9bfd-311">Voit poistaa rivin, lisätä uuden rivin tai muokata rivin tietoja.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="f9bfd-312">Voit muokata kysyntää manuaalisesti tai voit tuoda sen ulkoisesta järjestelmästä käyttämällä tietojen hallintaa.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="f9bfd-313">Mitä paikoituskysynnässä onkaan, sitä käytetään seuraavassa vaiheessa, riippumatta siitä, mistä se on peräisin.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="f9bfd-314">Etsi kysyntä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-314">Locate demand</span></span>

<span data-ttu-id="f9bfd-315">Kun kysyntä on luotu, sinun on luotava *paikoitussuunnitelma* käyttämällä **Paikanna kysyntä** -komentoa.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="f9bfd-316">Valitse toimintoruudussa **Etsi kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="f9bfd-317">Paikoitusprosessi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-317">The slotting process runs.</span></span> <span data-ttu-id="f9bfd-318">Kun prosessi on päättynyt, näkyviin tulee tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="f9bfd-319">Paikoitussuunnitelma</span><span class="sxs-lookup"><span data-stu-id="f9bfd-319">Slotting plan</span></span>

<span data-ttu-id="f9bfd-320">Paikoitussuunnitelmassa näkyy sijainti, johon kukin nimike/määrä on liitetty, riippumatta siitä, oliko ylivuoto käytössä, onko lisätyötä luotu, ja mitä malliriviä on käytetty.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="f9bfd-321">**Kaikki vaatimukset, joita ei ole voitu paikoittaa on korostettu punaisella.**</span><span class="sxs-lookup"><span data-stu-id="f9bfd-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="f9bfd-322">Tarkastele tuloksia valitsemalla Toimintoruudussa **Paikoitussuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="f9bfd-323">Luo täydennys</span><span class="sxs-lookup"><span data-stu-id="f9bfd-323">Create replenishment</span></span>

<span data-ttu-id="f9bfd-324">Kun paikoitussuunnitelma on luotu, suunnitelman perusteella on luotava *Täydennystyöt*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="f9bfd-325">Valitse toimintoruudussa **Suorita täydennykset**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="f9bfd-326">Kun prosessi on päättynyt, näkyviin tulee tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="f9bfd-327">Tämä sanoma ilmaisee työn koontiversiotunnukselle luotujen otsikoiden määrän.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="f9bfd-328">Käytettävät sijaintidirektiivit määritetään kullekin malliriville määritetyn direktiivikoodin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="f9bfd-329">Vihjeitä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="f9bfd-330">Automaattisen paikoituksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f9bfd-330">Set up automatic slotting</span></span>

<span data-ttu-id="f9bfd-331">Kun kaikki vaaditut elementit ovat paikoillaan, voit määrittää tilauksen suoritettavaksi automaattisesti noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="f9bfd-332">Valitse **Varastonhallinta \> Täydennys \> Suorita paikoitus**.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="f9bfd-333">Määritä suoritettavan työn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="f9bfd-334">Valitse yksi tai useampi seuraavista paikoitusvaiheista:</span><span class="sxs-lookup"><span data-stu-id="f9bfd-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="f9bfd-335">Luo kysyntä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-335">Generate demand</span></span>
    - <span data-ttu-id="f9bfd-336">Etsi kysyntä</span><span class="sxs-lookup"><span data-stu-id="f9bfd-336">Locate demand</span></span>
    - <span data-ttu-id="f9bfd-337">Luo täydennystyö</span><span class="sxs-lookup"><span data-stu-id="f9bfd-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9bfd-338">Paikoitusvaiheet ovat edistyksellisiä.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-338">The slotting steps are progressive.</span></span> <span data-ttu-id="f9bfd-339">Jos haluat valita *Paikanna kysyntä*, sinun on ensin valittava *Luo kysyntää*.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="f9bfd-340">Määritä käytettävä paikoitusmalli.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="f9bfd-341">Voit halutessasi määrittää toistuvan ajon automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="f9bfd-342">Jos harjoitteet ovat skenaariossa, **älä** määritä automaattista paikoitusta.</span><span class="sxs-lookup"><span data-stu-id="f9bfd-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
