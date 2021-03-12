---
title: Vaihda työpoolia työssä
description: Tässä ohjeaiheessa käsitellään aiemmin luodun työn työpoolin vaihtaminen käyttämällä työnimikkeiden Vaihda työpoolia -painikkeella.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001146"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="daa79-103">Vaihda työpoolia työssä</span><span class="sxs-lookup"><span data-stu-id="daa79-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="daa79-104">Voit järjestää työn ryhmiin työpoolien avulla.</span><span class="sxs-lookup"><span data-stu-id="daa79-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="daa79-105">Voit esimerkiksi luoda työpoolin luokitellaksesi työn, joka tapahtuu tietyssä varastosijainnissa.</span><span class="sxs-lookup"><span data-stu-id="daa79-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="daa79-106">*Vaihda työpoolia työssä* -toiminto lisää **Vaihda työpoolia** painikkeen työnimikkeiden toimintoruutuun.</span><span class="sxs-lookup"><span data-stu-id="daa79-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="daa79-107">Varastopäälliköiden onkin helppo vaihtaa aiemmin luodun työn työpoolia.</span><span class="sxs-lookup"><span data-stu-id="daa79-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="daa79-108">Päälliköt voivat reagoida nopeasti tällä toiminnolla varaston tuotannossa tapahtuviin muutoksiin. Se myös parantaa heidän mahdollisuuksia sopeutua muuttuviin tilanteisiin ja tarpeeseen siirtää työ toiseen työpooliin.</span><span class="sxs-lookup"><span data-stu-id="daa79-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="daa79-109">Vaihda työpoolia työssä -toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="daa79-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="daa79-110">Varmista ennen toiminnon määrittämistä tai käyttämistä, että se on saatavana järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="daa79-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="daa79-111">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="daa79-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="daa79-112">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="daa79-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="daa79-113">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="daa79-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="daa79-114">**Toiminnon nimi:** *Vaihda työpoolia työssä*</span><span class="sxs-lookup"><span data-stu-id="daa79-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="daa79-115">Vaihda työpoolia työssä -toiminnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="daa79-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="daa79-116">Toiminnon käyttö edellyttää, että muutamia työpooleja on määritetty.</span><span class="sxs-lookup"><span data-stu-id="daa79-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="daa79-117">Myös työmallit voidaan määrittää siten, että ne määrittävät poolin automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="daa79-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="daa79-118">Jos haluat kokeilla tässä aiheessa myöhemmin esiteltävää esimerkkitilannetta, määritä järjestelmäsi tämän osion ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="daa79-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="daa79-119">Työpoolien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="daa79-119">Set up work pools</span></span>

<span data-ttu-id="daa79-120">Työnimikkeet voidaan järjestää tyypin mukaan työpoolien avulla.</span><span class="sxs-lookup"><span data-stu-id="daa79-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="daa79-121">*Vaihda työpoolia työssä* -toiminnon käyttöä varten käytettävissä on oltava vähintään kaksi työpoolia.</span><span class="sxs-lookup"><span data-stu-id="daa79-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="daa79-122">Työpooleja voi tarkastella ja lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="daa79-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="daa79-123">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työpoolit**.</span><span class="sxs-lookup"><span data-stu-id="daa79-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="daa79-124">Jos käytät **USMF**-yrityksen esittelytietoja ja tässä aiheessa jäljempänä olevaa esimerkkiskenaariota, lisää kaksi työpoolia, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="daa79-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="daa79-125">Työpooli 1:</span><span class="sxs-lookup"><span data-stu-id="daa79-125">Work pool 1:</span></span>

        - <span data-ttu-id="daa79-126">**Työpoolin tunnus:** *WebShop*</span><span class="sxs-lookup"><span data-stu-id="daa79-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="daa79-127">**Kuvaus:** *Verkkokauppa*</span><span class="sxs-lookup"><span data-stu-id="daa79-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="daa79-128">Työpooli 2:</span><span class="sxs-lookup"><span data-stu-id="daa79-128">Work pool 2:</span></span>

        - <span data-ttu-id="daa79-129">**Työpoolin tunnus:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="daa79-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="daa79-130">**Kuvaus:** *Puhelinkeskus*</span><span class="sxs-lookup"><span data-stu-id="daa79-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="daa79-131">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="daa79-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="daa79-132">Määritä työmallit</span><span class="sxs-lookup"><span data-stu-id="daa79-132">Set up work templates</span></span>

<span data-ttu-id="daa79-133">Kullekin työmallille voi määrittää tarpeen mukaan oletustyöpoolin.</span><span class="sxs-lookup"><span data-stu-id="daa79-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="daa79-134">Kussakin soveltuvassa mallissa työpooli määritetään **Työpoolin tunnus** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="daa79-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="daa79-135">Tässä tapauksessa kaikki työnimikkeet luodaan siten, että annettu malli perii automaattisesti määritetyn työpoolin.</span><span class="sxs-lookup"><span data-stu-id="daa79-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="daa79-136">Jos käytät **USMF**-yrityksen esittelytietoja ja tässä aiheessa jäljempänä olevaa esimerkkiskenaariota, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="daa79-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="daa79-137">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="daa79-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="daa79-138">Siirrä sivu muokkaustilaan valitsemalla toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="daa79-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="daa79-139">Muokkaa mallia määrittämällä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="daa79-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="daa79-140">**Työmalli:** *62 Kerää pakettiin*</span><span class="sxs-lookup"><span data-stu-id="daa79-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="daa79-141">**Työpoolin tunnus:** *WebShop*</span><span class="sxs-lookup"><span data-stu-id="daa79-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="daa79-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="daa79-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="daa79-143">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="daa79-143">Example scenario</span></span>

<span data-ttu-id="daa79-144">Tämä skenaario näyttää, miten aiemmin luodun työnimikkeen käsittelyvirtaa muutetaan muuttamalla sen työpoolia.</span><span class="sxs-lookup"><span data-stu-id="daa79-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="daa79-145">Se käyttää **USMF**-yrityksen esittelytietoja ja aiemmin tässä ohjeaiheessa suositeltuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="daa79-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="daa79-146">Myyntitilauksen luominen ja sen vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="daa79-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="daa79-147">Vahvista, että nimikkeitä *A0001* ja *A0002* käytettävissä oleva varasto on riittävä varastossa *62*.</span><span class="sxs-lookup"><span data-stu-id="daa79-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="daa79-148">Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastoluettelo** ja muokkaa suodattimet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="daa79-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="daa79-149">**Varasto**-arvon alussa on *62*.</span><span class="sxs-lookup"><span data-stu-id="daa79-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="daa79-150">**Nimiketunnus** on joko *A001* tai *A002*.</span><span class="sxs-lookup"><span data-stu-id="daa79-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="daa79-151">Esimerkkitiedoissa kummankin määrän on oltava 10.</span><span class="sxs-lookup"><span data-stu-id="daa79-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="daa79-152">Seuraavaksi on luotava myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="daa79-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="daa79-153">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="daa79-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="daa79-154">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="daa79-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="daa79-155">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="daa79-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="daa79-156">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="daa79-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="daa79-157">**Varasto**: *62*</span><span class="sxs-lookup"><span data-stu-id="daa79-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="daa79-158">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="daa79-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="daa79-159">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="daa79-159">The new sales order is opened.</span></span> <span data-ttu-id="daa79-160">**Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi.</span><span class="sxs-lookup"><span data-stu-id="daa79-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="daa79-161">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="daa79-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="daa79-162">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="daa79-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="daa79-163">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="daa79-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="daa79-164">Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="daa79-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="daa79-165">Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="daa79-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="daa79-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="daa79-166">Close the page.</span></span>
1. <span data-ttu-id="daa79-167">Lisää toinen rivi myyntitilaukseen valitsemalla **Myyntitilausrivit**-pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="daa79-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="daa79-168">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="daa79-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="daa79-169">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="daa79-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="daa79-170">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="daa79-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="daa79-171">Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="daa79-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="daa79-172">Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="daa79-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="daa79-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="daa79-173">Close the page.</span></span>
1. <span data-ttu-id="daa79-174">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="daa79-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="daa79-175">Näyttöön tulee tiedotteita, joissa kerrotaan, että vapautuksesta luotiin aallon tunnus ja lähetystunnus.</span><span class="sxs-lookup"><span data-stu-id="daa79-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="daa79-176">Kirjoita aallon tunnus muistiin.</span><span class="sxs-lookup"><span data-stu-id="daa79-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="daa79-177">Lähtevän aallon tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="daa79-177">Review the outbound wave</span></span>

1. <span data-ttu-id="daa79-178">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="daa79-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="daa79-179">Hae ruudukossa myyntitilauksen vapautuksesta luotu aallon tunnus.</span><span class="sxs-lookup"><span data-stu-id="daa79-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="daa79-180">Voit tarkastella tietoja valitsemalla aallon tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="daa79-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="daa79-181">Varmista **Aallon rivit** -pikavälilehdessä, että myyntitilauksen lähetystunnus on näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="daa79-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="daa79-182">Jos **Käsittele aalto, kun se vapautetaan varastoon** -asetuksena on *Ei* lähetyksen aaltomallin asetuksissa, aalto on käsiteltävä manuaalisesti valitsemalla **Käsittely** toimintoruudun **Aalto**-välilehdessä ja luomalla työ.</span><span class="sxs-lookup"><span data-stu-id="daa79-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="daa79-183">Varmista, että aalto on käsitelty.</span><span class="sxs-lookup"><span data-stu-id="daa79-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="daa79-184">Tämä käsittely luo vaaditun työn.</span><span class="sxs-lookup"><span data-stu-id="daa79-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="daa79-185">Työn tietojen tarkasteleminen ja työpoolin vaihtaminen</span><span class="sxs-lookup"><span data-stu-id="daa79-185">View work details and change the work pool</span></span>

<span data-ttu-id="daa79-186">Voit tarkastella **Työn tiedot** -sivulla luotua työtä ja hallita työpoolia.</span><span class="sxs-lookup"><span data-stu-id="daa79-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="daa79-187">Valitse **Varastonhallinta \> Työ \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="daa79-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="daa79-188">Valitse juuri luodun työn rivi.</span><span class="sxs-lookup"><span data-stu-id="daa79-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="daa79-189">Myyntitilauksen numero näkyy **Tilausnumero**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="daa79-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="daa79-190">**Työpoolin tunnus** -kenttään määritetään työpoolin tunnus, joka määritettiin työmallissa.</span><span class="sxs-lookup"><span data-stu-id="daa79-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="daa79-191">Jos **Työpoolin tunnus** -kenttä ei ole näkyvissä, lisää sarake ruudukkoon ja päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="daa79-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="daa79-192">Voit vaihtaa työtunnukseen liitetyn työpoolin valitsemalla toimintoruudun **Työ**-välilehdessä **Vaihda työpoolin tunnus**.</span><span class="sxs-lookup"><span data-stu-id="daa79-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="daa79-193">Valitsee **Vaihda työpoolia** -valintaikkunan **Parametrit**-pikavälilehden **Työpoolin tunnus** -kentässä *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="daa79-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="daa79-194">Ota muutos käyttöön valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="daa79-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="daa79-195">Huomaa, että **Työpoolin tunnus** -kentän arvo on nyt *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="daa79-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="daa79-196">Kun **Vaihda työpooli** -valintaikkuna avautuu, **Työpoolin tunnus** -kenttä voi olla oletusarvoisesti tyhjä.</span><span class="sxs-lookup"><span data-stu-id="daa79-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="daa79-197">Jos kenttä on tyhjä, kun ota muutokset käyttöön valitsemalla **OK**, työpooli poistetaan kokonaan työstä.</span><span class="sxs-lookup"><span data-stu-id="daa79-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="daa79-198">Työpoolien vaihtamisen lisäksi työpooli voidaan lisätä tällä menettelyllä mihin tahansa työnimikkeeseen, jossa sitä ei ole, tai poistaa työpoolin mistä tahansa työnimikkeestä, jossa sellainen on.</span><span class="sxs-lookup"><span data-stu-id="daa79-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
