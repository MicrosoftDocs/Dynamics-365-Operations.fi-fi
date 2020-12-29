---
title: Manuaalisesti luodut työtilaukset
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan manuaalisesti käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426890"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="e9ebc-103">Manuaalisesti luodut työtilaukset</span><span class="sxs-lookup"><span data-stu-id="e9ebc-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="e9ebc-104">Voit luoda työtilauksia manuaalisesti kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="e9ebc-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="e9ebc-105">Sivulla **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="e9ebc-106">Sivulla **Kaikki ylläpitopyynnöt**, **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="e9ebc-107">Luo työtilaus</span><span class="sxs-lookup"><span data-stu-id="e9ebc-107">Create work order</span></span>

1. <span data-ttu-id="e9ebc-108">Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9ebc-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-109">Select **New**.</span></span>

3. <span data-ttu-id="e9ebc-110">Valitse työtilaustyyppi **Luo työtilaus**-valintaikkunan **Työtilaustyyppi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="e9ebc-111">Valitse tarvittaessa **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="e9ebc-112">Valitse resurssi **Resurssi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="e9ebc-113">Kun valitset resurssin, avattavassa **Resurssi**-välilehdellä voi olla käytettävissä kolme välilehteä:</span><span class="sxs-lookup"><span data-stu-id="e9ebc-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="e9ebc-114">**Aktiiviset resurssit** – Tämä välilehti sisältää luettelon kaikista resursseista, joiden elinkaaritila on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="e9ebc-115">**Resurssinäkymä** – Tässä välilehdessä näkyy puunäkymä toiminnallisista sijainneista ja niihin asennetuista resursseista.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="e9ebc-116">**Omat resurssit** – Tämä välilehti sisältää resursseja, jotka liittyvät niihin toiminnallisiin sijainteihin, joille sinut (järjestelmään kirjautunut työntekijä) voidaan kohdentaa.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="e9ebc-117">(Lisätietoja määrityksestä esitetään kohdassa [Ylläpitotyöntekijät ja -työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)Jos työntekijälle ei ole määritetty toiminnallisia sijainteja kohdassa [Ylläpitotyöntekijät ja -työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md), **Omat resurssit** -välilehti ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="e9ebc-118">Valitse **Ylläpitotyön tyyppi** -kentässä ylläpitotyön tyyppi työtilaukselle.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="e9ebc-119">Valitse tarvittaessa **Ylläpitotyön tyypin variantti** ja **Toimiala**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="e9ebc-120">Jos tarpeen, voit muuttaa työtilauksen palvelutasoa **Palvelutaso**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="e9ebc-121">Valitse päivämäärät kentissä **Odotettu alku** ja **Odotettu loppu**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="e9ebc-122">Luo työtilaus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="e9ebc-123">**Kaikki työtilaukset** -luettelosivulla voit muokata työtilausta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="e9ebc-124">Huomaa seuraavat seikat:</span><span class="sxs-lookup"><span data-stu-id="e9ebc-124">Note the following points:</span></span>

- <span data-ttu-id="e9ebc-125">**Kaikki työtilaukset** -luettelosivun tietonäkymässä voit lisätä useita käyttökohteita työtilaukseen lisäämällä rivejä **Työtilauksen ylläpitotyöt** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="e9ebc-126">Resurssille voi valita vain sellaisia ylläpitotyötyyppejä, jotka on määritetty resurssille vallitulle resurssityypille.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="e9ebc-127">Jos muutat resurssin palvelutasoa tai kriittisyyttä sen jälkeen, kun resurssia on käytetty työtilauksessa, työtilauksen palvelutasoa tai kriittisyyttä ei päivitetä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="e9ebc-128">Lisätietoja palvelutasoista ja kriittisyydestä esitetään kohdissa [Resurssien palvelutasot](../setup-for-objects/object-priorities.md) ja [Resurssien kriittisyystyypit](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="e9ebc-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="e9ebc-129">Työtilauksen kriittisyys lasketaan uudelleen aina, kun työtilaustehtävä lisätään työtilaukseen tai poistetaan siitä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="e9ebc-130">Siirry **Kaikki työtilaukset** -tietonäkymän > **Otsikko**-välilehden > **Aikataulu**-pikavälilehteen, jonka kentässä **Vastuuryhmä** tai **Vastuuhenkilö** voit valita vastaavan ylläpitotyöntekijäryhmän tai vastaavan ylläpitotyöntekijän.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="e9ebc-131">Näitä asetuksia voi muuttaa, kun työtilaus on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="e9ebc-132">Niitä voi muuttaa esimerkiksi, kun työtilauksen elinkaaren tila muuttuu.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="e9ebc-133">Työtilauksen luonnin yhteydessä tehtävä automaattinen valinta perustuu **Vastaavat ylläpitotyöntekijät** -sivun määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="e9ebc-134">Jos lisäät tai poistat työtilaustehtäviä työtilauksen luomisen jälkeen ja kentät **Vastuuryhmä** ja **Vastuuhenkilö** ovat tyhjiä, kun päivität työtilauksen, resurssienhallinta etsii määrityssivulta mahdollisen vastineen vastuulliskesi ylläpitotyöntekijäryhmäksi tai vastaavaksi ylläpitopitotyöntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="e9ebc-135">Jos kenttä **Vastuuryhmä** tai **Vastuuhenkilö** on jo määritetty, kun päivität työtilauksen, muutoksia ei tehdä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="e9ebc-136">Lisätietoja vastaavista ylläpitotyöntekijöistä ja työntekijäryhmistä esitetään kohdassa [Vastaavat ylläpitotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="e9ebc-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="e9ebc-137">[Ylläpidon tila](../controlling-and-reporting/maintenance-status.md) -sivulla voit suorittaa laskutoimituksen saadaksesi yleiskuvan saapuvien ja suoritettujen työtilausten kuormituksesta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="e9ebc-138">**Kaikki työtilaukset**-sivun tietonäkymän **Rivitiedot**-pikavälilehdessä voit käyttää kenttiä **Leveyspiiri** ja **Pituuspiiri** lisätäksesi maantieteelliset koordinaatit työtilaustehtävässä valitulle resurssille.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="e9ebc-139">Luo tähän liittyvä työtilaus</span><span class="sxs-lookup"><span data-stu-id="e9ebc-139">Create related work order</span></span>

<span data-ttu-id="e9ebc-140">Voit luoda työtilauksen, joka liittyy olemassa olevaan työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="e9ebc-141">Tämä ominaisuus on käytännöllinen, jos esimerkiksi haluat käyttää ensisijaisia ja toissijaisia työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="e9ebc-142">Uusi työtilaus perustuu aiemmin luodun työtilauksen työtilaustyöhön.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="e9ebc-143">Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9ebc-144">Valitse työtilaus, jolle luodaan liittyvä työtilaus.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="e9ebc-145">Valitse toimintoruudun **Työtilaus**-välilehden **Uusi**-ryhmässä **Liittyvä työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="e9ebc-146">Valitse avattavasta **Luo liittyvä työtilaus** -valintaikkunan **Työtilaustehtävä** -kentässä työtilaustehtävä, jolle haluat luoda liittyvän työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="e9ebc-147">Valitse ylläpitotyön tyyppi **Ylläpitotyön tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="e9ebc-148">Valitse **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä tarpeen mukaan ylläpitotyön tyypin variantti ja toimiala.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="e9ebc-149">Jos tämä työtilaus on ensimmäinen valitulle työtilaukselle luotu liittyvä työtilaus, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e9ebc-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="e9ebc-150">Valitse **Uusi työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="e9ebc-151">Valitse **Työtilaustyyppi**-kentässä työtilauksen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="e9ebc-152">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="e9ebc-153">Muuta tarvittaessa työtilauksen palvelutasoa **Palvelutaso**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="e9ebc-154">Valitse alkamis- ja päättymispäivämäärät kentissä **Odotettu alku** ja **Odotettu loppu**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="e9ebc-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-155">Select **OK**.</span></span> <span data-ttu-id="e9ebc-156">Uusi liittyvä työtilaus näkyy **Kaikki työtilaukset** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="e9ebc-157">Jos työtilauksella, jolle luot liittyvää työtilausta, on jo liittyviä työtilauksia, lisää olemassa olevaan liittyvään työtilaukseen uusi työtilaustehtävä seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="e9ebc-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="e9ebc-158">Valitse **Lisää liittyvään työtilaukseen**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="e9ebc-159">Valitse **Työtilaus**-kentässä se liittyvä työtilaus, jolle lisätään uusi työtilaustehtävä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="e9ebc-160">Muuta tarvittaessa työtilauksen palvelutasoa **Palvelutaso**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="e9ebc-161">Muuta tarvittaessa odotettuja alkamis- ja päättymispäivämääriä kentissä **Odotettu alku** ja **Odotettu loppu**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="e9ebc-162">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-162">Select **OK**.</span></span> <span data-ttu-id="e9ebc-163">Työtilauksen työ lisätään aiemmin luotuun työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="e9ebc-164">Seuraavassa kuvassa on esimerkki **Luo liittyvä työtilaus** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Kuva 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="e9ebc-166">Jos olet määrittänyt liittyvän työtilauspeitteen kentässä **Resurssienhallinnan parametrit** > **Työtilaukset** > **Liittyvä työtilauspeite**, työtilaustunnukset luodaan peitemäärityksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="e9ebc-167">Jos liittyvää työtilauksen peitettä ei ole määritetty, seuraavaa käytettävissä olevaa työtilaustunnusta käytetään liittyvissä työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="e9ebc-168">Työtilauksen kopiointi</span><span class="sxs-lookup"><span data-stu-id="e9ebc-168">Copy a work order</span></span>

<span data-ttu-id="e9ebc-169">Uuden työtilauksen voi luoda nopeasti aiemmin luodusta työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="e9ebc-170">Tämä tapa käyttää työtilauksia eroaa työtilausten luomisesta [ylläpitosuunnitelmien](../preventive-and-reactive-maintenance/maintenance-plans.md) perusteella.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="e9ebc-171">Siitä on hyötyä, jos työtilaus esimerkiksi sisältää useita työtilaustehtäviä ja nämä eri tehtävät on suoritettava eri resursseille säännöllisin väliajoin.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="e9ebc-172">Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9ebc-173">Valitse työtilaus, josta sisältöä kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="e9ebc-174">Valitse toimintoruudun **Työtilaus**-välilehden **Uusi**-ryhmässä **Kopioi työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="e9ebc-175">Näkyviin tulee valitun työtilauksen asetukset.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="e9ebc-176">Voit muokata osaa kentistä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="e9ebc-177">Luo uusi työtilaus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="e9ebc-178">**Kaikki työtilaukset** -luettelosivulla voit muokata työtilausta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="e9ebc-179">Kun uusi työtilaus luodaan, osa tiedoista kopioidaan suoraan olemassa olevasta työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="e9ebc-180">Ennusteita, työkaluja ylläpidon tarkistuslistoja, toiminnallista sijaintia, osoitteita ja aikatauluja koskevia tietoja ei kopioida.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="e9ebc-181">Sen sijaan ne perustuvat resurssienhallinnan kulloisiinkin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="e9ebc-182">Siten, jos kyseisiä tietoja on muutettu ensimmäisen työtilauksen luomisen ja työtilauksen kopioinnin välisenä aikana, muutokset sisällytetään uuteen työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="e9ebc-183">Esimerkkejä ovat muutokset ennusteisiin ja päivitykset ylläpidon tarkistuslistoihin.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="e9ebc-184">Seuraavassa kuvassa on esimerkki **Kopioi työtilaus** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Kuva 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="e9ebc-186">Työtilauksen luominen ylläpitopyynnön perusteella</span><span class="sxs-lookup"><span data-stu-id="e9ebc-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="e9ebc-187">Valitse **Resurssien hallinta** > **Yhteiset** > **Ylläpitopyynnöt** > **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="e9ebc-188">Valitse ylläpitopyyntö, jolle luodaan työtilaus, ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="e9ebc-189">Valitse toimintoruudun **Ylläpitopyyntö**-välilehden **Uusi**-ryhmässä **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="e9ebc-190">Määritä kentät **Työtilaus**-valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="e9ebc-191">Jos ylläpitotyön tyyppi on valittu ylläpitopyynnössä, voit tarvittaessa valita toisen kunnossapitotyön tyypin, kun luot työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="e9ebc-192">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-192">Select **OK**.</span></span> <span data-ttu-id="e9ebc-193">Saat ilmoituksen työtilauksen luomisesta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="e9ebc-194">Valitsemalla ylläpitopyynnön luettelosivulla **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** voit tarkastella ylläpitopyyntöön liittyviä työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="e9ebc-195">Valitse sitten toimintoruudun **Ylläpitopyyntö**-välilehden **Näytä**-ryhmässä **Työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="e9ebc-196">Seuraavassa kuvassa on esimerkki **Luo työtilaus** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Kuva 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="e9ebc-198">Työtilauksia voi luoda automaattisesti myös ajoittamalla ylläpitosuunnitelman töitä tai määrittämällä resurssien [ylläpitosuunnitelmien](../preventive-and-reactive-maintenance/maintenance-plans.md) tai [ylläpitokierrosten](../preventive-and-reactive-maintenance/maintenance-rounds.md) automaattinen luonti.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="e9ebc-199">**Kaikki ylläpitoaikataulut**-luettelosivulla ylläpitopyynnöistä luoduilla työtilauksilla on ylläpitopyynnöissä valitut ylläpitotyötyypit.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

