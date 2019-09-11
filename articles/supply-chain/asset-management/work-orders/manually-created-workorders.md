---
title: Manuaalisesti luodut työtilaukset
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan manuaalisesti käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875629"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="e7dff-103">Manuaalisesti luodut työtilaukset</span><span class="sxs-lookup"><span data-stu-id="e7dff-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e7dff-104">Voit luoda työtilauksia manuaalisesti kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="e7dff-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="e7dff-105">kohdassa **Kaikki työtilaukset** ta **Aktiiviset työtilaukset**</span><span class="sxs-lookup"><span data-stu-id="e7dff-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="e7dff-106">kohdassa **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**</span><span class="sxs-lookup"><span data-stu-id="e7dff-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="e7dff-107">Luo työtilaus</span><span class="sxs-lookup"><span data-stu-id="e7dff-107">Create work order</span></span>

1. <span data-ttu-id="e7dff-108">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e7dff-109">Valitse **Uusi**-painike.</span><span class="sxs-lookup"><span data-stu-id="e7dff-109">Click the **New** button.</span></span>

3. <span data-ttu-id="e7dff-110">Valitse avattavasta **Luo työtilaus** -luettelosta työtilauksen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e7dff-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="e7dff-111">Valitse kuvaus tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="e7dff-111">If required, select a description.</span></span>

5. <span data-ttu-id="e7dff-112">Valitse työtilauksen resurssi sekä ylläpitotyön tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e7dff-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="e7dff-113">Kun valitset resurssin, käytettävissä voi olla kolme välilehteä: **Omat resurssit** -väliehti sisältää resurssit, jotka liittyvät toiminnallisiin sijainteihin, joihin sinut voidaan (järjestelmään kirjautuneena kunnossapitotyöntekijänä) kohdistaa (määritetään kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="e7dff-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="e7dff-114">Jos [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md) -kohdassa ei ole määritetty toiminnallisia sijainteja työntekijälle, **Omat resurssit** -välilehti ei ole näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="e7dff-115">**Aktiiviset resurssit** -välilehti sisältää luettelon kaikista resursseista, joiden elinkaaritila on Aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="e7dff-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="e7dff-116">**Resurssinäkymä** -väli ehdessä näkyy puunäkymä toiminnallisista sijainneista ja näihin sijainteihin asennetuista resursseista.</span><span class="sxs-lookup"><span data-stu-id="e7dff-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="e7dff-117">Valitse tarvittaessa **Ylläpitotyön tyypin variantti** ja **Toimiala**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="e7dff-118">Jos tarpeen, voit muuttaa työtilauksen palvelutasoa **Palvelutaso**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="e7dff-119">Valitse liittyvissä kentissä odotetut alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="e7dff-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="e7dff-120">Luo uusi työtilaus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="e7dff-121">Muokkaa työtilausta kohdassa **Kaikki työtilaukset** tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e7dff-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="e7dff-122">**Kaikki työtilaukset** -kohdassa voit lisätä useita käyttökohteita työtilaukseen Tiedot-näkymässä lisäämällä rivejä **Työtilauksen ylläpitotyöt** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="e7dff-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="e7dff-123">Voit valita resurssille vain ylläpitotyölajit, jotka liittyvät käyttöomaisuuserälle määritetyn resurssityypin asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="e7dff-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="e7dff-124">Jos olet muuttanut käyttöomaisuuden palvelutasoa tai käyttöomaisuuden kriittisyyttä sen jälkeen, kun olet käyttänyt niitä työtilauksessa (katso lisätietoja kohdassa [Resurssien palvelutasot](../setup-for-objects/object-priorities.md) ja [Resurssien kriittisyydet](../setup-for-objects/object-criticalities.md)), työtilauksen palvelutasoa tai kriittisyyttä ei päivitetä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="e7dff-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="e7dff-125">Työtilauksen kriittisyys lasketaan uudelleen aina, kun työtilausivi lisätään työtilaukseen tai poistetaan siitä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="e7dff-126">**Kaikki työtilaukset** -näkymän **Otsikko**-näkymän **Ajoita**-pikavälilehdessä voit valita vastuullisen huoltotyöntekijäryhmän tai vastuulisen kunnossapitotyöntekijän **Vastuullinen ryhmä**- tai **Vastuuhenkilö**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="e7dff-127">Näitä asetuksia voidaan muuttaa niin kauan kuin työtilaus on aktiivinen – esimerkiksi silloin, kun työtilauksen elinkaaren tila muuttuu.</span><span class="sxs-lookup"><span data-stu-id="e7dff-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="e7dff-128">Työtilauksen luonnin yhteydessä tehtävä automaattinen valinta perustuu **Vastaavat ylläpitotyöntekijät** -asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="e7dff-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="e7dff-129">Jos lisäät tai poistat työtilaustöitä työtilauksen luomisen jälkeen ja **Vastaava ryhmä** -kenttä ja **Vastuuhenkilö**-kenttä ovat tyhjiä, kun päivität työtilauksen, käyttöomaisuuden hallinta etsii mahdollisen vastineen asetuslomakkeesta vastuulliskesi huoltotyöntekijäryhmäksi tai vastaavaksi kunnossapitotyöntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="e7dff-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="e7dff-130">Jos **Vastuuryhmä**-kenttä tai **vastuuhenkilö**-kenttä on jo täytetty, kun päivität työtilauksen, muutoksia ei tehdä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="e7dff-131">**Ylläpidon tila** -kohdassa saat laskennan avulla saat yleiskuvan saapuvien ja suoritettujen työtilausten kuormituksesta.</span><span class="sxs-lookup"><span data-stu-id="e7dff-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="e7dff-132">Lisää maantieteelliset koordinaatit työtilaustyössä valitulle käyttöomaisuudelle **Rivin tiedot** -pikavälilehden **Leveysaste**- ja **Pituusaste**-kenttien avulla.</span><span class="sxs-lookup"><span data-stu-id="e7dff-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="e7dff-133">Luo tähän liittyvä työtilaus</span><span class="sxs-lookup"><span data-stu-id="e7dff-133">Create related work order</span></span>

<span data-ttu-id="e7dff-134">Voit luoda liittyvän työtilauksen aiemmin luotuun työtilaukseen, jos haluat käyttää esimerkiksi ensisijaisia ja toissijaisia työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="e7dff-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="e7dff-135">Uusi työtilaus perustuu aiemmin luodun työtilauksen työtilaustyöhön.</span><span class="sxs-lookup"><span data-stu-id="e7dff-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="e7dff-136">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e7dff-137">Valitse työtilaus, jolle haluat tehdä liittyvän työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="e7dff-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="e7dff-138">Valitse **Liittyvä työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="e7dff-139">Valitse avattavasta **Luo liittyvä työtilaus** -valintaikkunasta työtilaustyö, jolle haluat luoda liittyvän työtilauksen **Työtilauksen työ** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="e7dff-140">Valitse ylläpitotyön tyyppi **Ylläpitotyön tyyppi** -kentässä ja tarvittaessa liittyvä kunnossapitotöiden tyypin variantti ja toimiala **Ylläpitotyön tyypin variantti**- ja **Toimiala**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="e7dff-141">Jos kyseessä on ensimmäinen liittyvä työtilaus, napsauta **Uusi työtilaus** -valintanappia.</span><span class="sxs-lookup"><span data-stu-id="e7dff-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="e7dff-142">Valitse **Työtilauksen tyyppi** ja **Kuvaus** liittyvissä kentissä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="e7dff-143">Jos tarpeen, muuta työtilauksen palvelutasoa **Palvelutaso**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="e7dff-144">Lisää liittyvissä kentissä odotetut alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="e7dff-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="e7dff-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-145">Click **OK**.</span></span> <span data-ttu-id="e7dff-146">Uusi liittyvä työtilaus näkyy **Kaikki työtilaukset** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e7dff-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="e7dff-147">Jos luot työtilaukseen liittyvän työtilauksen, johon on jo liitetty työtilauksia, voit lisätä työtilaustyön jo liittyvään työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e7dff-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="e7dff-148">Tämän voi tehdä valitsemalla vaiheessa 6 **Lisää liittyvään työtilaukseen** -valintanappi.</span><span class="sxs-lookup"><span data-stu-id="e7dff-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="e7dff-149">Tämän jälkeen voit valita liittyvän työtilauksen, johon haluat lisätä uuden työtilaustyön.</span><span class="sxs-lookup"><span data-stu-id="e7dff-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="e7dff-150">Muokkaa **Palvelutaso**-, **Odotettu aloitus**- ja **Odotettuja loppu** -kenttiä tarpeen mukaan ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="e7dff-151">Työtilauksen työ lisätään aiemmin luotuun työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e7dff-151">The work order job is added to the existing related work order.</span></span>


![Kuva 1](media/03-work-orders.png)

<span data-ttu-id="e7dff-153">**Huomautus:** Jos olet määrittänyt liittyvän työtilauspeitteen **Resurssienhallinnan parametrit** > **Työtilaukset** -linkki > **Liittyvän työtilauksen peite** -kentässä, työtilaustunnukset luodaan peitteen asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e7dff-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="e7dff-154">Jos liittyvää työtilauksen peitettä ei ole määritetty, seuraavaa käytettävissä olevaa työtilaustunnusta käytetään liittyvissä työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="e7dff-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="e7dff-155">Kopioi työtilaus</span><span class="sxs-lookup"><span data-stu-id="e7dff-155">Copy work order</span></span>

<span data-ttu-id="e7dff-156">Uuden työtilauksen voi luoda nopeasti aiemmin luodusta työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e7dff-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="e7dff-157">Tämä työtilausten käsittelytapa eroaa ylläpitosuunnitelmiin perustuvien työtilausten luonnista.</span><span class="sxs-lookup"><span data-stu-id="e7dff-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="e7dff-158">Siitä on hyötyä esimerkiksi silloin, kun työtilaus sisältää useita työtilaustöitä, joissa on erilaisia töitä, jotka on suoritettava säännöllisin väliajoin.</span><span class="sxs-lookup"><span data-stu-id="e7dff-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="e7dff-159">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e7dff-160">Valitse työtilaus, josta haluat kopioida sisältöä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="e7dff-161">Valitse **Kopioi työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-161">Click **Copy work order**.</span></span> <span data-ttu-id="e7dff-162">Näkyviin tulee valitun työtilauksen asetukset.</span><span class="sxs-lookup"><span data-stu-id="e7dff-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="e7dff-163">Voit tarvittaessa muokata joitakin kenttiä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="e7dff-164">Luo uusi työtilaus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="e7dff-165">Muokkaa työtilausta kohdassa **Kaikki työtilaukset** tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e7dff-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="e7dff-166">Kun uusi työtilaus luodaan, osa tiedoista kopioidaan suoraan olemassa olevasta työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="e7dff-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="e7dff-167">Ennusteita, työkaluja, ylläpidon tarkistuslistoja, toiminnallista sijaintia, osoitteita ja aikataulutusta koskevia tietoja ei kopioida, vaan ne alustetaan käyttöomaisuuden hallinnan nykyisistä asetuksista.</span><span class="sxs-lookup"><span data-stu-id="e7dff-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="e7dff-168">Tämä merkitsee, että jos näihin tietoihin tehdään muutoksia ensimmäisen työtilauksen luomisajan kohdan jälkeen siihen saakka, kun työtilauksen kopio on tehty, muutokset sisällytetään uuteen työtilaukseen, jonka olet luonut.</span><span class="sxs-lookup"><span data-stu-id="e7dff-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="e7dff-169">Esimerkkejä ovat ennusteiden tai päivitettyjen huoltotarkistusluetteloiden muutokset.</span><span class="sxs-lookup"><span data-stu-id="e7dff-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Kuva 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="e7dff-171">Työtilauksen luominen ylläpitopyynnön perusteella</span><span class="sxs-lookup"><span data-stu-id="e7dff-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="e7dff-172">Valitse **Resurssien hallinta**  >  **yhteiset**  >  **Ylläpitopyynnöt**  >  **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="e7dff-173">Valitse ylläpitopyynnöt, joille haluat luoda työtilauksen, ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="e7dff-174">Valitse kohdassa **Kaikki pyynnnöt** **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="e7dff-175">Täytä avattava **Työtilaus**-luettelo.</span><span class="sxs-lookup"><span data-stu-id="e7dff-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="e7dff-176">Jos kunnossapitotyön tyyppi on valittu ylläpitopyynnössä, voit tarvittaessa valita toisen kunnossapitotyön tyypin, kun luot työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="e7dff-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="e7dff-177">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7dff-177">Click **OK**.</span></span> <span data-ttu-id="e7dff-178">Näkyviin tulee sanoma, jossa ilmoitetaan, että työtilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="e7dff-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="e7dff-179">Jos haluat nähdä, mitkä työtilaukset on liitetty ylläpitopyyntöön, valitse ylläpitopyyntö kohdassa **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** ja valitse **Työtilaukset**-painike.</span><span class="sxs-lookup"><span data-stu-id="e7dff-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Kuva 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="e7dff-181">Työtilauksia voi luoda automaattisesti myös määrittämällä ylläpitosuunnitelman työt aikataulutuksen mukaan tai määrittämällä käyttöomaisuuserän huoltosuunnitelmat tai ylläpitokierrokset.</span><span class="sxs-lookup"><span data-stu-id="e7dff-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="e7dff-182">**Ylläpitoaikataulu**-kohdassa lylläpitopyynnöistä uodut työtilaukset luodaan ylläpitopyynnöissä valituilla kunnossapitotöiden tyypeillä.</span><span class="sxs-lookup"><span data-stu-id="e7dff-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

