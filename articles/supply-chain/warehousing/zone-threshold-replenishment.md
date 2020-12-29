---
title: Vyöhykkeen rajatäydennys
description: Vyöhykkeeseen perustuva täydennys käyttää minimi/maksimi (min/max) täydennysstrategiaa, mutta se arvioi koko varastovyöhykkeet yksittäisten sijaintien sijaan. Tämän vuoksi varastopäälliköt voivat oppia nopeammin, kun poimintavyöhykkeellä tarvitaan lisävarastoa.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6f4ddd03ec16ac43b007b904eb688563735e0941
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654169"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="b2fae-104">Vyöhykkeen rajatäydennys</span><span class="sxs-lookup"><span data-stu-id="b2fae-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2fae-105">Vyöhykkeeseen perustuva täydennys käyttää minimi/maksimi (min/max) [täydennys](replenishment.md)-strategiaa, mutta se arvioi koko varastovyöhykkeet yksittäisten sijaintien sijaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="b2fae-106">Tämän vuoksi varastopäälliköt voivat oppia nopeammin, kun poimintavyöhykkeellä tarvitaan lisävarastoa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="b2fae-107">Tämän ominaisuuden määritys muistuttaa sijaintiin perustuvan täydennyksen asetuksia.</span><span class="sxs-lookup"><span data-stu-id="b2fae-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="b2fae-108">Kun määrität mallin min.-/max.-täydennykseen, voit myös määrittää, lasketaanko raja-arvo sijaintia vai vyöhykettä kohden.</span><span class="sxs-lookup"><span data-stu-id="b2fae-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="b2fae-109">Jos määrität vyöhykkeisiin perustuvan arvioinnin, vyöhykkeen valintakyselyyn on lisättävä tietyt vyöhykkeet.</span><span class="sxs-lookup"><span data-stu-id="b2fae-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="b2fae-110">Kuten sijaintiin perustuva min.-/max.-täydennys, vyöhykkeeseen perustuva min-/max-täydennys perustuu varaston vähimmäiskynnyksen määritykseen, joka käynnistää valittujen nimikkeiden täydennystöiden luomisen.</span><span class="sxs-lookup"><span data-stu-id="b2fae-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="b2fae-111">Tämä täydennystyö kasvattaa varastoa määritetyn vyöhykkeen enimmäisrajan mukaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="b2fae-112">Nykyisessä versiossa ei tueta tuotevariantin vyöhykkeen täydennysprosesseja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="b2fae-113">Toisin kuin sijaintiin perustuvaa min.-/max.-täydennystä, vyöhykkeeseen perustuva min.-/max.-täydennys ei vaadi varastopaikkoja arvioimaan, pitäisikö sijaintien tallentaa tietty nimike.</span><span class="sxs-lookup"><span data-stu-id="b2fae-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="b2fae-114">Tämän vuoksi aluevyöhykkeeseen perustuvassa täydennyksessä voit käyttää min.-/max.-täydennystä, vaikka sinulla ei olisikaan varastossa kunkin nimikkeen tai nimikevariantin varastopaikkoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="b2fae-115">Kun vyöhykkeen määrä alittaa määritetyn minimirajan, täydennystyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="b2fae-116">Sijaintidirektiivien avulla määritetään, mihin tiettyyn sijaintiin varasto tulisi ottaa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="b2fae-117">Vyöhykeraja-arvon täydennysominaisuuden käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="b2fae-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="b2fae-118">Ennen kuin voit käyttää *Vyöhykeraja-arvon täydennys* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b2fae-119">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b2fae-120">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="b2fae-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b2fae-121">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="b2fae-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b2fae-122">**Toiminnon nimi:** *Vyöhykeraja-arvon täydennys*</span><span class="sxs-lookup"><span data-stu-id="b2fae-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="b2fae-123">Aseta vyöhykkeeseen perustuva täydennys</span><span class="sxs-lookup"><span data-stu-id="b2fae-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="b2fae-124">Jos haluat määrittää vyöhykkeeseen perustuvan täydennyksen, sinun on konfiguroitava useita järjestelmän osia.</span><span class="sxs-lookup"><span data-stu-id="b2fae-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="b2fae-125">Tässä osassa esitellään eri asetukset ja annetaan demoarvot, jotka voit määrittää, jos haluat käsitellä tämän ohjeaiheen lopussa olevaa skenaariota.</span><span class="sxs-lookup"><span data-stu-id="b2fae-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="b2fae-126">Määritä direktiivikoodit</span><span class="sxs-lookup"><span data-stu-id="b2fae-126">Set up directive codes</span></span>

<span data-ttu-id="b2fae-127">[Direktiivikoodien](control-warehouse-location-directives.md) avulla voit olla tarkempi, kun määrität työmallissa käytettävän sijaintimallin.</span><span class="sxs-lookup"><span data-stu-id="b2fae-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="b2fae-128">Kukin koodi muodostaa yhteisen arvon, johon voit viitata, kun määrität kutakin mallityyppiä.</span><span class="sxs-lookup"><span data-stu-id="b2fae-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="b2fae-129">Direktiivikoodien tarkasteleminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-129">View and edit directive codes</span></span>

<span data-ttu-id="b2fae-130">Jos haluat tarkastella tai muokata direktiivikoodeja, siirry kohtaan **Varaston hallinta \> Määritys \> Direktiivikoodit**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="b2fae-131">Demotietodirektiivin koodien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="b2fae-132">Tässä esimerkissä kuvataan, miten direktiivikoodi valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="b2fae-133">Jos aiot käsitellä tämän ohjeaiheen lopussa olevaa skenaariota, käytä tässä annettuja demoarvoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b2fae-134">Muussa tapauksessa käytä omia arvoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b2fae-135">Valitse **USMF**-yritys, joka käyttää demotietoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b2fae-136">Valitse **Varastonhallinta \> Asetukset \> Direktiivikoodit**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="b2fae-137">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-138">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-139">**Direktiivikoodi:** _Vyöhykkeen täyd_</span><span class="sxs-lookup"><span data-stu-id="b2fae-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="b2fae-140">**Direktiivin kuvaus:** _Vyöhykkeen täydennys_</span><span class="sxs-lookup"><span data-stu-id="b2fae-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="b2fae-141">Tallenna uusi koodi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="b2fae-142">Määritä täydennysmallit</span><span class="sxs-lookup"><span data-stu-id="b2fae-142">Set up replenishment templates</span></span>

<span data-ttu-id="b2fae-143">[Vähimmäis- tai enimmäistäydennysmallit](tasks/set-up-min-max-replenishment-process.md) ovat ensisijainen mekanismi optimaalisten tasojen ylläpitämiseksi poimintasijainneissa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="b2fae-144">Näissä malleissa on määritettävä säännöt, joita käytetään varaston täydentämiseen varastossa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="b2fae-145">Täydennys, johon malleja voidaan käyttää, sisältää vyöhykkeeseen perustuvan täydennyksen.</span><span class="sxs-lookup"><span data-stu-id="b2fae-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="b2fae-146">Tarkastele ja muokkaa täydennysmalleja</span><span class="sxs-lookup"><span data-stu-id="b2fae-146">View and edit replenishment templates</span></span>

<span data-ttu-id="b2fae-147">Täydennysmalli on sääntöjoukko, joka määrittää, milloin ja miten sijaintia täydennetään.</span><span class="sxs-lookup"><span data-stu-id="b2fae-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="b2fae-148">Voit valita mallin, jolla ohjataan, milloin ja miten täydennys tehdään.</span><span class="sxs-lookup"><span data-stu-id="b2fae-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="b2fae-149">Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit** tarkastellaksesi tai muokataksesi täydennysmallejasi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="b2fae-150">Demotietojen täydennysmallin valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="b2fae-151">Tässä esimerkissä kuvataan, miten täydennysmalli valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="b2fae-152">Jos aiot käsitellä tämän ohjeaiheen lopussa olevaa skenaariota, käytä tässä annettuja demoarvoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b2fae-153">Muussa tapauksessa käytä omia arvoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b2fae-154">Valitse **USMF**-yritys, joka käyttää demotietoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b2fae-155">Valitse **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="b2fae-156">Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="b2fae-157">Lisää **Yleiskatsaus**-ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="b2fae-158">Aseta uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="b2fae-158">In the new row, set the following values.</span></span> <span data-ttu-id="b2fae-159">Hyväksy oletusarvot kaikille muille kentille.</span><span class="sxs-lookup"><span data-stu-id="b2fae-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b2fae-160">**Täydennysmalli:** _Vyöhyke min./max. täyd_</span><span class="sxs-lookup"><span data-stu-id="b2fae-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="b2fae-161">**Kuvaus:** _Vyöhykkeen min./max. täydennys_</span><span class="sxs-lookup"><span data-stu-id="b2fae-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="b2fae-162">**Täydennystyyppi:** _Vähimmäis- tai enimmäisarvo_</span><span class="sxs-lookup"><span data-stu-id="b2fae-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="b2fae-163">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-163">Select **Save**.</span></span>
1. <span data-ttu-id="b2fae-164">Kun uusi rivi on yhä valittuna **Yhteenveto**-ruudukossa, lisää juuri luomaasi *Vyöhyke min.-/max. täyd.*-täydennysmalli valitsemalla **Täydennysmallin tiedot**-ruudukon yläpuolella oleva **Uusi**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="b2fae-165">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-166">**Järjestysnumero:** Syötä _1_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b2fae-167">**Kuvaus:** Syötä _Poimintavyöhykkeen täydennys_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="b2fae-168">**Täydennysyksikkö:** Valitse _kpl_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="b2fae-169">**Pyyntötyyppi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2fae-170">**Direktiivikoodi:** Tämä kenttä linkittää täydennysmallin sijaintidirektiiviin.</span><span class="sxs-lookup"><span data-stu-id="b2fae-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="b2fae-171">Valitse aiemmin luomasi demotietodirektiivin koodi (_Vyöhyketäyd._).</span><span class="sxs-lookup"><span data-stu-id="b2fae-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="b2fae-172">**Työmalli:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2fae-173">**Minimimäärä:** Tämä kenttä määrittää määrän, jonka täydennys käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="b2fae-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="b2fae-174">Syötä _50_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-174">Enter _50_.</span></span>
    - <span data-ttu-id="b2fae-175">**Enimmäismäärä:** Tämä kenttä määrittää nimikkeen enimmäismäärän, joka voidaan esittää vyöhykkeessä.</span><span class="sxs-lookup"><span data-stu-id="b2fae-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="b2fae-176">Luotu täydennystyö lisää varaston määrää tähän määrään.</span><span class="sxs-lookup"><span data-stu-id="b2fae-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="b2fae-177">Syötä _150_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-177">Enter _150_.</span></span>
    - <span data-ttu-id="b2fae-178">**Yksikkö:** Tässä kentässä määritetään vähimmäis- ja enimmäisarvojen yksikkö.</span><span class="sxs-lookup"><span data-stu-id="b2fae-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="b2fae-179">Valitse _kpl_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-179">Select _ea_.</span></span>
    - <span data-ttu-id="b2fae-180">**Kysynnän lisäys:** Valitse _Pyöristä ylöspäin_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="b2fae-181">**Täydennä tyhjät kiinteät sijainnit:** Valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="b2fae-182">**Täydennä vain kiinteät sijainnit:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-183">**Tuotekyselytila:** Valitse _tuotekysely_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="b2fae-184">**Täydennyksen raja-alue:** Tässä kentässä määritetään, arvioiko malli alueen vai määritetyn sijainnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="b2fae-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="b2fae-185">Valitse _Vyöhyke_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-185">Select _Zone_.</span></span>
    - <span data-ttu-id="b2fae-186">**Varasto:** Valitse _61_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="b2fae-187">Valitse **Täydennysmallin tiedot** -ruudukon yläpuolelta **Valitse tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b2fae-188">Lisää ruudukkoon rivi valitsemalla **Tuotekysely**-valintaruudun **Alue**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-189">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-190">**Taulukko:** _Nimikkeet_</span><span class="sxs-lookup"><span data-stu-id="b2fae-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="b2fae-191">**Johdettu taulu:** _Nimikkeet_</span><span class="sxs-lookup"><span data-stu-id="b2fae-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="b2fae-192">**Kenttä:** _Nimiketunnus_</span><span class="sxs-lookup"><span data-stu-id="b2fae-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="b2fae-193">**Kriteerit:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="b2fae-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="b2fae-194">Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b2fae-195">Valitse **Täydennysmallin tiedot** -ruudukon yläpuolelta **Valitse täydennettävät vyöhykkeet**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b2fae-196">Lisää ruudukkoon rivi **Vyöhykekysely** -valintaruudun **Alue**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="b2fae-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-197">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-198">**Taulu:** _Varastovyöhyke_</span><span class="sxs-lookup"><span data-stu-id="b2fae-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b2fae-199">**Johdettu taulu:** _Varastovyöhyke_</span><span class="sxs-lookup"><span data-stu-id="b2fae-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b2fae-200">**Kenttä:** _Alueen tunnus_</span><span class="sxs-lookup"><span data-stu-id="b2fae-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b2fae-201">**Kriteerit:** _LATTIA_</span><span class="sxs-lookup"><span data-stu-id="b2fae-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b2fae-202">Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="b2fae-203">Määritä sijaintidirektiivit</span><span class="sxs-lookup"><span data-stu-id="b2fae-203">Set up location directives</span></span>

<span data-ttu-id="b2fae-204">Toisin kuin sijaintiin perustuva min.-/max.-täydennys, vyöhykkeisiin perustuva min./max.-täydennys edellyttää, että määrität sekä keräilysijaintidirektiivit että varastopaikkadirektiivit, koska järjestelmä laskee koko vyöhykkeen sen sijaan, että se olisi vain lähtevien töiden poimintasijainti.</span><span class="sxs-lookup"><span data-stu-id="b2fae-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="b2fae-205">Sijaintidirektiivien tarkasteleminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-205">View and edit location directives</span></span>

<span data-ttu-id="b2fae-206">Jos haluat tarkastella tai muokata sijaintidirektiivejä, siirry kohtaan **Varaston hallinta \> Määritys \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="b2fae-207">Seuraavassa osassa on esimerkkejä siitä, miten voit luoda tarvittavat poimintasijaintidirektiivit ja sijoittaa sijaintidirektiivejä asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="b2fae-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="b2fae-208">Demotietosijaintidirektiivien valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-208">Prepare demo data location directives</span></span>

<span data-ttu-id="b2fae-209">Jos haluat valmistella demotietoja, jotta sitä voidaan käyttää tämän ohjeaiheen lopussa olevassa skenaariossa, sinun on luotava kaksi sijaintidirektiiviä: yksi poimintaa ja yksi hyllytystä varten.</span><span class="sxs-lookup"><span data-stu-id="b2fae-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="b2fae-210">Luo täydennyspoimintadirektiivi</span><span class="sxs-lookup"><span data-stu-id="b2fae-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="b2fae-211">Valitse **USMF**-yritys, joka käyttää demotietoja.</span><span class="sxs-lookup"><span data-stu-id="b2fae-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b2fae-212">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b2fae-213">Aseta vasemmassa ruudussa **Työtilaustyyppi**-kentän arvoksi _Täydennys_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="b2fae-214">Valitse toimintoruudussa **Uusi** luodaksesi uuden direktiivin.</span><span class="sxs-lookup"><span data-stu-id="b2fae-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="b2fae-215">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-215">Set the following values:</span></span>

    - <span data-ttu-id="b2fae-216">**Järjestysnumero:** Hyväksy oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="b2fae-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b2fae-217">**Nimi:** Syötä _vyöhykkeen poiminta_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="b2fae-218">**Työtyyppi:** Valitse _Poiminta_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="b2fae-219">**Toimipaikka:** Valitse _6_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b2fae-220">**Varasto:** Valitse _61_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b2fae-221">**Direktiivikoodi:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2fae-222">**Useita varastointiyksiköitä:** Määritä tämän vaihtoehdon arvoksi _Ei_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b2fae-223">Valitse **Tallenna**, jos haluat luoda direktiivin, jossa on tähän mennessä määritetyt asetukset.</span><span class="sxs-lookup"><span data-stu-id="b2fae-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b2fae-224">Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2fae-225">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2fae-226">**Järjestysnumero:** Syötä _1_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b2fae-227">**Määrästä:** Syötä _0_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b2fae-228">**Määrään:** Syötä _10000000_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b2fae-229">**Yksikkö:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2fae-230">**Etsi määrä:** Valitse _ei mitään_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b2fae-231">**Rajoita yksikön mukaan:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-232">**Pyöristä ylös yksikköön:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-233">**Etsi pakkausmäärä:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-234">**Salli jakaminen:** Valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b2fae-235">Tallenna uusi rivi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b2fae-236">Kun uusi rivi on edelleen valittuna **Rivit**-ruudukossa, lisää rivi ruudukkoon valitsemalla **Sijaintidirektiivin toimenpiteet** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-237">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-238">**Järjestysnumero:** Syötä _1_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b2fae-239">**Nimi:** Syötä _Poiminta bulkkina_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="b2fae-240">**Kiinteän sijainnin käyttö:** Valitse _Kiinteät ja muut kuin kiinteät sijainnit_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b2fae-241">**Salli negatiivinen varasto:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-242">**Erä käytössä:** Tyhjennä tämä valinta ruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-243">**Strategia:** Valitse _Ei mitään_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="b2fae-244">Tallenna uusi toiminto valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b2fae-245">Kun uusi toiminto on edelleen valittuna, valitse **Sijaintidirektiivin toiminnot** -ruudukon yläpuolella oleva **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b2fae-246">Näyttöön tulee kyselyvalintaikkuna, jossa voit valita varastopaikat, joita haluat täydentää.</span><span class="sxs-lookup"><span data-stu-id="b2fae-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="b2fae-247">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="b2fae-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-248">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-249">**Taulu:** _Sijainnit_</span><span class="sxs-lookup"><span data-stu-id="b2fae-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b2fae-250">**Johdettu taulu:** _Sijainnit_</span><span class="sxs-lookup"><span data-stu-id="b2fae-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b2fae-251">**Kenttä:** _Alueen tunnus_</span><span class="sxs-lookup"><span data-stu-id="b2fae-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b2fae-252">**Kriteerit:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="b2fae-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="b2fae-253">Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b2fae-254">Tallenna sijaintidirektiivi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="b2fae-255">Luo täydennyshyllytysdirektiivi</span><span class="sxs-lookup"><span data-stu-id="b2fae-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="b2fae-256">Varmista **Sijaintidirektiivit**-sivun vasemmasta ruudusta, että **Työtilauksen tyyppi** -kentän arvoksi on edelleen määritetty _Täydennys_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="b2fae-257">Valitse toimintoruudussa **Uusi** luodaksesi toisen uuden direktiivin.</span><span class="sxs-lookup"><span data-stu-id="b2fae-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="b2fae-258">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-258">Set the following values:</span></span>

    - <span data-ttu-id="b2fae-259">**Järjestysnumero:** Hyväksy oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="b2fae-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b2fae-260">**Nimi:** Syötä _vyöhykkeen hyllytys_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b2fae-261">**Työtilauksen tyyppi:** Valitse _Hyllytys_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="b2fae-262">**Toimipaikka:** Valitse _6_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b2fae-263">**Varasto:** Valitse _61_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b2fae-264">**Direktiivin koodi:** Valitse _Vyöhykkeen täyd_, jos haluat linkittää tämän sijaintidirektiivin aiemmin luomaasi täydennysmalliin käyttämällä aiemmin luomaasi koodia.</span><span class="sxs-lookup"><span data-stu-id="b2fae-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="b2fae-265">**Useita varastointiyksiköitä:** Määritä tämän vaihtoehdon arvoksi _Ei_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b2fae-266">Valitse **Tallenna**, jos haluat luoda direktiivin, jossa on tähän mennessä määritetyt asetukset.</span><span class="sxs-lookup"><span data-stu-id="b2fae-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b2fae-267">Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2fae-268">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2fae-269">**Järjestysnumero:** Syötä _1_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b2fae-270">**Määrästä:** Syötä _0_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b2fae-271">**Määrään:** Syötä _10000000_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b2fae-272">**Yksikkö:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2fae-273">**Etsi määrä:** Valitse _ei mitään_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b2fae-274">**Rajoita yksikön mukaan:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-275">**Pyöristä ylös yksikköön:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-276">**Etsi pakkausmäärä:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-277">**Salli jakaminen:** Valitse tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b2fae-278">Tallenna uusi rivi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b2fae-279">Kun uusi rivi on edelleen valittuna **Rivit**-ruudukossa, lisää rivi ruudukkoon valitsemalla **Sijaintidirektiivin toimenpiteet** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-280">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-281">**Järjestysnumero:** Syötä _1_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b2fae-282">**Nimi:** Syötä _vyöhykkeen hyllytys_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b2fae-283">**Kiinteän sijainnin käyttö:** Valitse _Kiinteät ja muut kuin kiinteät sijainnit_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b2fae-284">**Salli negatiivinen varasto:** Tyhjennä tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-285">**Erä käytössä:** Tyhjennä tämä valinta ruutu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b2fae-286">**Strategia:** Valitse _Konsolidoi_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="b2fae-287">Tallenna uusi toiminto valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b2fae-288">Kun uusi toiminto on edelleen valittuna, valitse **Sijaintidirektiivin toiminnot** -ruudukon yläpuolella oleva **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b2fae-289">Näyttöön tulee kyselyvalintaikkuna, jossa voit valita vyöhykkeet, joita haluat täydentää.</span><span class="sxs-lookup"><span data-stu-id="b2fae-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="b2fae-290">Tämän vyöhykkeen tulee olla sama alue, joka on määritetty täydennysmallissa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="b2fae-291">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="b2fae-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b2fae-292">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b2fae-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b2fae-293">**Taulu:** _Sijainnit_</span><span class="sxs-lookup"><span data-stu-id="b2fae-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b2fae-294">**Johdettu taulu:** _Sijainnit_</span><span class="sxs-lookup"><span data-stu-id="b2fae-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b2fae-295">**Kenttä:** _Alueen tunnus_</span><span class="sxs-lookup"><span data-stu-id="b2fae-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b2fae-296">**Kriteerit:** _LATTIA_</span><span class="sxs-lookup"><span data-stu-id="b2fae-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b2fae-297">Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b2fae-298">Tallenna sijaintidirektiivi valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="b2fae-299">Skenaario</span><span class="sxs-lookup"><span data-stu-id="b2fae-299">Scenario</span></span>

<span data-ttu-id="b2fae-300">Tässä osassa on esimerkkiskenaario, jossa kerrotaan, kuinka toimintoa käytetään.</span><span class="sxs-lookup"><span data-stu-id="b2fae-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="b2fae-301">Esimerkkiskenaarion mukaisten esimerkkiskenaarioiden valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="b2fae-302">Ennen kuin aloitat skenaarion käsittelyn, sinun on aktivoitava mallitiedot ja määritettävä ominaisuus tässä osassa ja aiemmissa tämän ohjeaiheen osissa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b2fae-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="b2fae-303">Käytä USFM-yritystä</span><span class="sxs-lookup"><span data-stu-id="b2fae-303">Use the USMF legal entity</span></span>

<span data-ttu-id="b2fae-304">Tämän skenaarion käyttäminen määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="b2fae-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b2fae-305">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="b2fae-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="b2fae-306">Lisä mallitietojen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b2fae-306">Prepare additional sample data</span></span>

<span data-ttu-id="b2fae-307">Kun olet valinnut **USMF**-yrityksen, lisää tarvittavat näytetiedot, jotka on kuvattu aiemmin tämän ohjeaiheen kohdassa [Määritä vyöhykkeeseen perustuva täydennys](#setup) -osa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="b2fae-308">Tarkista käytettävissä olevat varastosi</span><span class="sxs-lookup"><span data-stu-id="b2fae-308">Check your on-hand inventory</span></span>

<span data-ttu-id="b2fae-309">Seuraavien vaiheiden avulla voit varmistaa, että järjestelmä sisältää riittävän varaston, joka tukee esimerkkiskenaariota.</span><span class="sxs-lookup"><span data-stu-id="b2fae-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="b2fae-310">Varmista, että nimike *A0001* on käytettävissä oleva varasto kahdessa eri paikassa täydennysmallissa määritetyssä poimintavyöhykkeessä (*LATTIA*).</span><span class="sxs-lookup"><span data-stu-id="b2fae-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="b2fae-311">Kokonaisvaraston on kuitenkin oltava pienempi kuin vaadittu vähimmäismäärä (*50*), joka on määritetty täydennysmallissa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="b2fae-312">Näin voit simuloida, miten laskeminen tapahtuu koko vyöhykkeelle yhden ainoan sijainnin asemesta.</span><span class="sxs-lookup"><span data-stu-id="b2fae-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="b2fae-313">**Voit muuttaa varastoa tarpeen mukaan käyttämällä mitä tahansa varastoprosessia.**</span><span class="sxs-lookup"><span data-stu-id="b2fae-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="b2fae-314">Varmista, että nimikkeelle *A0001* on riittävästi varastoa varastopaikan keräilysijaintidirektiivissä määritetyssä bulkkisijainnissa, jossa täydennystyön tulisi poimia nimikkeet vyöhykkeen tunnuksesta *BULKKI*.</span><span class="sxs-lookup"><span data-stu-id="b2fae-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="b2fae-315">Kokonaisvaraston on oltava suurempi kuin vaadittu enimmäismäärä (*150*), joka on määritetty täydennysmallissa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="b2fae-316">Valinnainen mutta suositeltava: Luo varaston oikaisukirjauskansio noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="b2fae-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="b2fae-317">Valitse **Varastonhallinta \> Kirjauskansioviennit \> Nimikkeet \> Varaston oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="b2fae-318">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-318">Select **New**.</span></span>
    1. <span data-ttu-id="b2fae-319">Valitse **Luo varastokirjauskansio** -valintaikkunan **Varasto**-kentässä *61*.</span><span class="sxs-lookup"><span data-stu-id="b2fae-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="b2fae-320">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-320">Select **OK**.</span></span>
    1. <span data-ttu-id="b2fae-321">Lisää ruudukkoon kolme riviä käyttämällä **Uusi**-painiketta **Kirjauskansion rivit**-pikavälilehdessä ja määritä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="b2fae-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="b2fae-322">Kun olet määrittänyt jokaisen rivin, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="b2fae-323">**Rivi 1:**</span><span class="sxs-lookup"><span data-stu-id="b2fae-323">**Line 1:**</span></span>

            - <span data-ttu-id="b2fae-324">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b2fae-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b2fae-325">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="b2fae-325">**Site:** *6*</span></span>
            - <span data-ttu-id="b2fae-326">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="b2fae-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b2fae-327">**Sijainti:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b2fae-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="b2fae-328">**Rekisterikilpi:** Valitse luettelosta aiemmin luotu rekisterikilpi tai luo uusi rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b2fae-329">**Määrä** *1000*</span><span class="sxs-lookup"><span data-stu-id="b2fae-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="b2fae-330">**Rivi 2:**</span><span class="sxs-lookup"><span data-stu-id="b2fae-330">**Line 2:**</span></span>

            - <span data-ttu-id="b2fae-331">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b2fae-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b2fae-332">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="b2fae-332">**Site:** *6*</span></span>
            - <span data-ttu-id="b2fae-333">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="b2fae-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b2fae-334">**Sijainti:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="b2fae-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="b2fae-335">**Rekisterikilpi:** Valitse luettelosta aiemmin luotu rekisterikilpi tai luo uusi rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b2fae-336">**Määrä** *15*</span><span class="sxs-lookup"><span data-stu-id="b2fae-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="b2fae-337">**Rivi 3:**</span><span class="sxs-lookup"><span data-stu-id="b2fae-337">**Line 3:**</span></span>

            - <span data-ttu-id="b2fae-338">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b2fae-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b2fae-339">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="b2fae-339">**Site:** *6*</span></span>
            - <span data-ttu-id="b2fae-340">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="b2fae-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b2fae-341">**Sijainti:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b2fae-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="b2fae-342">**Rekisterikilpi:** Valitse luettelosta aiemmin luotu rekisterikilpi tai luo uusi rekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="b2fae-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b2fae-343">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="b2fae-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="b2fae-344">Valitse toimintoruudussa **Validoi**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="b2fae-345">Voit korjata mahdolliset virheet, jotka löytyvät ennen seuraavaan vaiheeseen siirtymistä.</span><span class="sxs-lookup"><span data-stu-id="b2fae-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="b2fae-346">Vahvista varaston kirjaus valitsemalla toimintoruudussa **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="b2fae-347">Esimerkkiskenaario: Suorita vyöhykkeeseen perustuva min.-/max.-täydennys</span><span class="sxs-lookup"><span data-stu-id="b2fae-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="b2fae-348">Kun kaikki vaaditut mallitiedot on luotu, voit käynnistää täydennyksen noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b2fae-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="b2fae-349">Valitse **Varastonhallinta \> Täydennys \> Täydennykset**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="b2fae-350">Avaa **Täydennys**-valintaikkuna valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="b2fae-351">Muokkaa oletustaulukon riviä **Kysely**-valintaikkunan **Alue**-välilehdessä seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="b2fae-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="b2fae-352">**Taulu:** Valitse _Täydennysmallit_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b2fae-353">**Johdettu taulu:** Valitse _Täydennysmallit_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b2fae-354">**Kenttä:** Valitse _Täydennysmalli_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="b2fae-355">**Ehdot:** Valitse _Vyöhykkeen min./max. täyd_.</span><span class="sxs-lookup"><span data-stu-id="b2fae-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="b2fae-356">Tämä täydennysmalli on täydennysmalli, jonka loit tämän skenaarion demotietojen valmistelun aikana.</span><span class="sxs-lookup"><span data-stu-id="b2fae-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="b2fae-357">Tallenna kysely ja palaa **Täydennys**-valintaikkunaan valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="b2fae-358">Suorita täydennysmalli valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fae-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="b2fae-359">Täydennystyöt luodaan nyt, kun varasto kerätään *BULKKI*-vyöhykkeestä ja se lisätään *LATTIA*-vyöhykkeeseen.</span><span class="sxs-lookup"><span data-stu-id="b2fae-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="b2fae-360">Huomautuksia ja vihjeitä</span><span class="sxs-lookup"><span data-stu-id="b2fae-360">Notes and tips</span></span>

<span data-ttu-id="b2fae-361">Seuraavassa on muutamia huomautuksia ja vihjeitä toiminnon käyttämisestä:</span><span class="sxs-lookup"><span data-stu-id="b2fae-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="b2fae-362">Jos haluat määrittää täydennystyöt, jotka menevät haluamallesi vyöhykkeelle, voit linkittää täydennysmallin rivit ja sijaintidirektiivit jommallakummalla seuraavista tavoista:</span><span class="sxs-lookup"><span data-stu-id="b2fae-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="b2fae-363">Muokkaa sijaintidirektiivin otsikkokyselyä ja suodata valittuja täydennysmallin rivejä.</span><span class="sxs-lookup"><span data-stu-id="b2fae-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="b2fae-364">Käytä täydennysmallirivillä direktiivikoodia ja vastaa sitä hyllytyssijaintidirektiiviin.</span><span class="sxs-lookup"><span data-stu-id="b2fae-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="b2fae-365">Jos käytät dynaamisia sijainteja, täydennystyöt luodaan joko ensimmäiselle käytettävissä olevalle sijainnille tai sijainnille, joissa on jo varasto, jos sijaintidirektiivitoimenpide on määritetty käyttämään **Konsolidoi**-strategiaa.</span><span class="sxs-lookup"><span data-stu-id="b2fae-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="b2fae-366">Jos käytät paikkoja, joissa käytetään vyöhykkeitä, käytä [normaalia min.-/max.-täydennystä](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="b2fae-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
