---
title: Asiakkaan omistamien resurssien ylläpidon laskuttaminen
description: Tässä aiheessa käsitellään asiakkaiden omistamien resurssien ylläpitotyön luontia, käsittelyä ja laskuttamista.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500451"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="2d9c5-103">Asiakkaan omistamien resurssien ylläpidon laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="2d9c5-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="2d9c5-104">*Työtilauksen laskutus* -toiminnolla voi luoda, käsitellä ja laskuttaa asiakkaan omistamia resursseja koskevan ylläpitotyön.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="2d9c5-105">Toiminnolla voi suorittaa seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="2d9c5-106">Asiakkaiden yhdistäminen asiakkaan omistamiin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="2d9c5-107">Asiakkaan valitseminen ja asiakkaan omistamien resurssien tarkasteleminen työtilausta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="2d9c5-108">Pääprojektin määrittäminen kullekin asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="2d9c5-109">Työtilaukseen perustuvien tuntien, nimikkeiden, kulujen ja maksujen kirjaaminen sekä laskuehdotuksen luominen asiakkaalle myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="2d9c5-110">Toiminnossa on lisäksi seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="2d9c5-111">Projektisopimus kopioidaan automaattisesti asiakkaan pääprojektista asianmukaiseen työtilauksenprojektiin.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="2d9c5-112">Resurssien hallinta voi nyt käyttää *lisämaksu*-projektitapahtumatyyppiä sekä työtilauksen ennusteissa että työtilauksen kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="2d9c5-113">Asiakkaan laskutustoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="2d9c5-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="2d9c5-114">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2d9c5-115">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="2d9c5-116">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2d9c5-117">**Moduuli:** *Projektinhallinta ja kirjanpito*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="2d9c5-118">**Toiminnon nimi:** *Työtilauksen laskutus*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2d9c5-119">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="2d9c5-119">Example scenario</span></span>

<span data-ttu-id="2d9c5-120">Seuraavan esimerkkiskenaarion toteuttaminen auttaa hahmottamaan toiminnon käyttöä.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="2d9c5-121">Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="2d9c5-122">Lisäksi **USMF**-yritys on valittava ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="2d9c5-123">Voit hyödyntää tätä skenaariota myös ohjeena, kun työskentelet tuotantojärjestelmän parissa ja käytät toimintoa.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="2d9c5-124">Tässä tapauksessa sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="2d9c5-125">Vaihe 1: Uuden projektisopimuksen luominen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="2d9c5-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="2d9c5-126">Valitse **Projektinhallinta ja kirjanpito \> Projektit \> Projektisopimukset**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="2d9c5-127">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9c5-128">Määritä **Uusi projektisopimus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2d9c5-129">**Nimi:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="2d9c5-130">**Rahoitustyyppi:** *Asiakas*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="2d9c5-131">**Rahoituslähde:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="2d9c5-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="2d9c5-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="2d9c5-133">Vaihe 2: Uuden pääprojektin luominen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="2d9c5-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="2d9c5-134">Tässä luotavaa pääprojektia käytetään, kun asiakkaalle luodaan työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="2d9c5-135">Valitse **Projektinhallinta ja kirjanpito \> Projektit \> Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="2d9c5-136">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9c5-137">Määritä **Uusi projekti** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2d9c5-138">**Projektityyppi:** *Aika ja materiaali*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="2d9c5-139">**Projektiin nimi:** *Pelican Wholesalesin työtilaukset*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="2d9c5-140">**Projektiryhmä:** *TM*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="2d9c5-141">**Projektisopimuksen tunnus:** *Pelican Wholesales* (aiemmin luotu sopimus)</span><span class="sxs-lookup"><span data-stu-id="2d9c5-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="2d9c5-142">**Alkamispäivä:** valitse kuluva päivä.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="2d9c5-143">Valitse **Luo projekti**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-143">Select **Create project**.</span></span>
1. <span data-ttu-id="2d9c5-144">Uusi projekti avataan.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-144">The new project is opened.</span></span> <span data-ttu-id="2d9c5-145">Kirjoita **Projektitunnus**-arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="2d9c5-146">Se on annettava myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="2d9c5-147">Vaihe 3: Uuden työtilaustyypin luominen resurssien hallinnassa</span><span class="sxs-lookup"><span data-stu-id="2d9c5-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="2d9c5-148">Valitse **Resurssien hallinta \> Asetukset \> Työtilaus \> Työtilaustyypit**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="2d9c5-149">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9c5-150">Uusi tietue lisätään luetteloon.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-150">A new record is added to the list.</span></span> <span data-ttu-id="2d9c5-151">Määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-151">Set the following values for it:</span></span>

    - <span data-ttu-id="2d9c5-152">**Työtilaustyyppi:** *Palvelu*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="2d9c5-153">**Nimi:** *Palvelun työtilaukset*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="2d9c5-154">**Työtilauksen elinkaaren tila:** *Vakio*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="2d9c5-155">Vaihe 4: Asiakastilin linkittäminen pääprojektiin</span><span class="sxs-lookup"><span data-stu-id="2d9c5-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="2d9c5-156">Asiakastili on nyt linkitettävä pääprojektiin resurssien hallinnan projektiasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="2d9c5-157">Valitse **Resurssien hallinta \> Asetukset \> Työtilaukset \> Projektiasetukset**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="2d9c5-158">Lisää rivi valitsemalla **Pääprojekti**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="2d9c5-159">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2d9c5-160">**Asiakastili:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="2d9c5-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="2d9c5-161">**Projektitunnus:** anna aiemmin muistiin kirjoitettu projektitunnus.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="2d9c5-162">Vaihe 5: Projektiryhmän ja tyypin linkittäminen työtilausprojektiin</span><span class="sxs-lookup"><span data-stu-id="2d9c5-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="2d9c5-163">**Projektin määritys** -sivun (**Resurssien hallinta \> Asetukset \> Työtilaukset \> Projektin määritys**) pitäisi olla edelleen avoinna.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="2d9c5-164">Lisää rivi valitsemalla **Projektiryhmä**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="2d9c5-165">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2d9c5-166">**Työtilaustyyppi:** *Palvelu* (aiemmin luotu työtilaustyyppi)</span><span class="sxs-lookup"><span data-stu-id="2d9c5-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="2d9c5-167">**Projektiryhmä:** *TM*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="2d9c5-168">Työtilausprojektin projektisopimus periytyy aina pääprojektista.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="2d9c5-169">Vaihe 6: Resurssin linkittäminen asiakastunnukseen</span><span class="sxs-lookup"><span data-stu-id="2d9c5-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="2d9c5-170">Valitse **Resurssien hallinta \> Resurssit \> Aktiiviset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="2d9c5-171">Anna **Suodatus**-kentässä *VE-102* ja valitse suodatusperusteeksi **Resurssi**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="2d9c5-172">Avaa resurssin asetukset valitsemalla se.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="2d9c5-173">Määritä **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="2d9c5-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="2d9c5-174">*Pelican Wholesales* päivittyy automaattisesti **Nimi**-kentän arvoksi.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="2d9c5-175">Vaihe 7: Uuden työtilaustyypin luominen resurssille</span><span class="sxs-lookup"><span data-stu-id="2d9c5-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="2d9c5-176">Valitse **Resurssien hallinta \> Työtilaukset \> Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="2d9c5-177">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2d9c5-178">Määritä **Luo työtilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2d9c5-179">**Työtilaustyyppi:** *Palvelu*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="2d9c5-180">**Kuvaus:** *Kuorma-auton korjaus*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="2d9c5-181">**Asiakastili:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="2d9c5-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="2d9c5-182">**Resurssi:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="2d9c5-183">Haku näyttää vain valittuun asiakastiliin linkitetyt resurssit.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="2d9c5-184">**Ylläpitotyön tyyppi:** *Korjaus*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="2d9c5-185">**Ammatti:** *Mekaanikko*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="2d9c5-186">**Palvelutaso:** *4*</span><span class="sxs-lookup"><span data-stu-id="2d9c5-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="2d9c5-187">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="2d9c5-188">Vaihe 8: Työtilauksen tarkistaminen ja sen käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="2d9c5-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="2d9c5-189">Tässä osassa käytetään edellisessä osassa luotua työtilausta.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="2d9c5-190">Seuraavien ohjeiden avulla tarkistetaan, että pääprojekti on *Pelican wholesalesin työtilaus* -projekti:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="2d9c5-191">Valitse rivi **Työtilauksen ylläpitotyöt** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="2d9c5-192">Tarkista **Rivin tiedot** -pikavälilehdessä **Projektitunnus**-arvo.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="2d9c5-193">Sen pitäisi olla seuraavanlainen tavuviivalla yhdistetty luku: *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="2d9c5-194">Tämä arvo on linkki.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-194">This value is a link.</span></span>
    1. <span data-ttu-id="2d9c5-195">Valitse projektitunnuksen linkki. Se avaa sivun, jossa on näkyvissä pääprojektin ja projektin nimet.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="2d9c5-196">Valitse toimintoruudun **Työtilaus**-välilehden **Elinkaaren tila** -ryhmässä **Päivitä työtilauksen tila**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="2d9c5-197">Valitse **Päivitä työtilauksen tila** -valintaikkunan **Valitse**-sarakkeessa sen rivin valintaruutu, jonka **Elinkaaren tila** -kentän asetuksena on *Käsittelyssä*.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="2d9c5-198">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-198">Select **OK**.</span></span>
1. <span data-ttu-id="2d9c5-199">Valitse **Elinkaaren tila: Käynnissä** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="2d9c5-200">Vaihe 9: Työtilaukseen kuluneiden tuntien kirjaaminen ja uuden laskuehdotuksen luominen</span><span class="sxs-lookup"><span data-stu-id="2d9c5-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="2d9c5-201">Tässä osassa jatketaan edellisessä osassa luodun työtilauksen käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="2d9c5-202">Valitse toimintoruudun **Työtilaus**-välilehden **Projekti**-ryhmässä **Kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="2d9c5-203">**Työtilauksen kirjauskansiot** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="2d9c5-204">Tällä sivulla voi kirjata työtilaukseen kuluneen ajan.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="2d9c5-205">Valitse **Tunnit**-pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="2d9c5-206">Määritä uuden rivin **Tunnin**-kentän arvoksi *4*.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="2d9c5-207">Valitse toimintoruudussa **Kirjaa kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="2d9c5-208">Palaa työtilaukseen sulkemalla **Työtilauksen kirjauskansiot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="2d9c5-209">Valitse toimintoruudun **Laskutus**-välilehdessä **Uusi laskuehdotus**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="2d9c5-210">Valitse **Luo laskuehdotus** -valintaikkunan **Projektitapahtumat**-osassa jokaisen laskutettavan rivin kohdalla **Valitse**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="2d9c5-211">Sulje valintaikkuna ja tarkastele uutta laskuehdotusta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]