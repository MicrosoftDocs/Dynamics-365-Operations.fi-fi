---
title: "Materiaalikulutuksen rekisteröinti mobiililaitteella"
description: "Tässä ohjeaiheessa käsitellään työnkulkua, jolla tuotannossa kulutettavat raaka-aineet voidaan rekisteröidä kämmenlaitteella."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9f4685a349c79bbb421d4295485923ee151e7b29
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="a80ca-103">Materiaalikulutuksen rekisteröinti mobiililaitteella</span><span class="sxs-lookup"><span data-stu-id="a80ca-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a80ca-104">Tässä ohjeaiheessa käsitellään työnkulkua, jolla tuotannossa kulutettavat raaka-aineet voidaan rekisteröidä kämmenlaitteella.</span><span class="sxs-lookup"><span data-stu-id="a80ca-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="a80ca-105">Johdanto</span><span class="sxs-lookup"><span data-stu-id="a80ca-105">Introduction</span></span>
------------

<span data-ttu-id="a80ca-106">Tämä työnkulku on hyödyllinen, jos materiaalin tarkka seuranta on välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="a80ca-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="a80ca-107">Näissä tilanteissa materiaalin jäljitettävyyden ylläpito edellyttää kulutuksen tarkan ajan ja määrän ilmoittamista.</span><span class="sxs-lookup"><span data-stu-id="a80ca-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="a80ca-108">Tämä prosessi voidaan nähdä esi- tai jälkipoiston peilikuvana, sillä näissä toiminnoissa rekisteröinnin ajankohta ja varsinaisen kulutuksen ajankohta poikkeavat toisistaan.</span><span class="sxs-lookup"><span data-stu-id="a80ca-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="a80ca-109">Tämän vuoksi automaattista kulutusstrategiaa ei voi käyttää joissakin materiaaleissa, joissa on edellytyksenä jäljitettävyys.</span><span class="sxs-lookup"><span data-stu-id="a80ca-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="a80ca-110">Tarkastellaan yksinkertainen skenaariota, joka selittää, miten määritetään työnkulku tuotannossa tapahtuvan raaka-aineiden kulutuksen rekisteröintiin kämmenlaitteella.</span><span class="sxs-lookup"><span data-stu-id="a80ca-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="a80ca-111">[![määritä työnkulku, joka mahdollistaa raaka-aineiden kulutuksen kannettavan laitteen avulla](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="a80ca-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="a80ca-112">Skenaarion tiedot</span><span class="sxs-lookup"><span data-stu-id="a80ca-112">Scenario details</span></span>

<span data-ttu-id="a80ca-113">Jatkuva tuotantoprosessi (5) kuluttaa eräohjattua raaka-ainetta RM-100.</span><span class="sxs-lookup"><span data-stu-id="a80ca-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="a80ca-114">Materiaali on käytettävissä varaston sijainnissa Bulk-001 (1), rekisterikilpi on PL-1 ja siinä on kaksi erää B1 ja B2, joiden kummankin määrä 100 lbs.</span><span class="sxs-lookup"><span data-stu-id="a80ca-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="a80ca-115">RM-100:n varastotyö (2) vapautetaan ja käsitellään. Materiaali kerätään sijainnista Bulk-001 tuotannon varastoinnin sijaintiin PIL-01 (3), joka on määritetty rekisterikilpiohjatuksi sijainniksi.</span><span class="sxs-lookup"><span data-stu-id="a80ca-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="a80ca-116">Koneenkäyttäjä punnitsee materiaalin tuotannon varastointisijainnissa (3) ja rekisteröi painon. Eränumero on kulutettu (4).</span><span class="sxs-lookup"><span data-stu-id="a80ca-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="a80ca-117">Osa materiaalista lisätään tuotannon varastoinnin sijainnista tuotantoprosessiin määritetyin aikavälein.</span><span class="sxs-lookup"><span data-stu-id="a80ca-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="a80ca-118">Kun koneenkäyttäjä lisää materiaalia, se punnitaan vaa'alla ja eränumero rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="a80ca-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="a80ca-119">Työnkulun määrittäminen rekisteröimään kulutus kämmenlaitteella</span><span class="sxs-lookup"><span data-stu-id="a80ca-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="a80ca-120">Luo valmis tuote, FG 100, tuoterakenteella, jossa on eräohjattua raaka-ainetta RM-100.</span><span class="sxs-lookup"><span data-stu-id="a80ca-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="a80ca-121">Lisää RM-100:n kaksi erää, B1 ja B2, joissa on määrä 100, sijaintiin Bulk-001, jossa on rekisterikilpi PL-1.</span><span class="sxs-lookup"><span data-stu-id="a80ca-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="a80ca-122">RM-100:n tuoterakennerivin materiaaliottosäännöksi on valittu **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="a80ca-123">Määritä tuotannon varastoinnin sijainniksi PIL-01.</span><span class="sxs-lookup"><span data-stu-id="a80ca-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="a80ca-124">Voit tehdä sen valitsemalla tämän sijainnin tuotannon varastoinnin oletussijainniksi varastossa 51.</span><span class="sxs-lookup"><span data-stu-id="a80ca-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="a80ca-125">Luo uusi mobiililaitteen valikkovaihtoehto:</span><span class="sxs-lookup"><span data-stu-id="a80ca-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="a80ca-126">**Valikkovaihtoehdon nimi** – Rekisteröi materiaalikulutus.</span><span class="sxs-lookup"><span data-stu-id="a80ca-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="a80ca-127">**Ruutu** – Rekisteröi materiaalikulutus.</span><span class="sxs-lookup"><span data-stu-id="a80ca-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="a80ca-128">**Menetelmä** – Epäsuora.</span><span class="sxs-lookup"><span data-stu-id="a80ca-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="a80ca-129">**Toimintokoodi** – Rekisteröi materiaalikulutus.</span><span class="sxs-lookup"><span data-stu-id="a80ca-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="a80ca-130">Lisää valikkovaihtoehto **tuotannon mobiililaitteen** valikkoon.</span><span class="sxs-lookup"><span data-stu-id="a80ca-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="a80ca-131">Luo valmiin tuotteen tuotantotilaus:</span><span class="sxs-lookup"><span data-stu-id="a80ca-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="a80ca-132">**Nimiketunnus** – FG-100</span><span class="sxs-lookup"><span data-stu-id="a80ca-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="a80ca-133">**Toimipaikka** – 5</span><span class="sxs-lookup"><span data-stu-id="a80ca-133">**Site** - 5</span></span> 
-    <span data-ttu-id="a80ca-134">**Varasto** – 51</span><span class="sxs-lookup"><span data-stu-id="a80ca-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="a80ca-135">**Määrä** – 150</span><span class="sxs-lookup"><span data-stu-id="a80ca-135">**Quantity** - 150</span></span>

<span data-ttu-id="a80ca-136">Tuotantotilaus on **arvioitu** ja **vapautettu** ja varastotyö on luotu.</span><span class="sxs-lookup"><span data-stu-id="a80ca-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="a80ca-137">Suorita työ käyttämällä kämmenlaitteelle suunniteltua raaka-aineiden keräilyn työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="a80ca-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="a80ca-138">Työnkulku siirtää materiaalin bulkkisijainnista tuotannon varastoinnin sijaintiin PIL-01.</span><span class="sxs-lookup"><span data-stu-id="a80ca-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="a80ca-139">Kun työ on suoritettu, materiaalin tila on **kerätty tuotannon varastoinnin sijainnissa**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="a80ca-140">Työn käsittelyn jälkeen tila on joko **Keräilty** tai **Varattu fyysinen**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="a80ca-141">Tämä on määritetty parametrilla **Jälkeen-varasto-ottotila viety varastolomakkeeseen**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="a80ca-142">Käynnistä tuotantotilaus asiakasohjelmasta tai kämmenlaitteesta **Tuotannon käynnistys** -valikkovaihtoehdosta.</span><span class="sxs-lookup"><span data-stu-id="a80ca-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="a80ca-143">Kun tuotantotilaus on käynnistetty, voit rekisteröidä materiaalikulutuksen kämmenlaitteen työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="a80ca-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="a80ca-144">Aloitetaan rekisteröimällä 25 lbs:n kulutus erässä B1.</span><span class="sxs-lookup"><span data-stu-id="a80ca-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="a80ca-145">Valitse kämmenlaitteen valikossa **Rekisteröi** **materiaalikulutus** ja anna seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a80ca-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="a80ca-146">Tuotantotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="a80ca-146">The production order number.</span></span> 
-    <span data-ttu-id="a80ca-147">Sijainti, jossa materiaali aiotaan kuluttaa eli tässä tapauksessa PIL-01.</span><span class="sxs-lookup"><span data-stu-id="a80ca-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="a80ca-148">Nimiketunnus RM-100.</span><span class="sxs-lookup"><span data-stu-id="a80ca-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="a80ca-149">Eränumero B1.</span><span class="sxs-lookup"><span data-stu-id="a80ca-149">Batch number B1.</span></span> 
-    <span data-ttu-id="a80ca-150">Määrä 25.</span><span class="sxs-lookup"><span data-stu-id="a80ca-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="a80ca-151">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-151">Select **OK**.</span></span>

<span data-ttu-id="a80ca-152">Huomaa, että näyttöön avautuu sanoma Kirjauskansion rivi on luotu.</span><span class="sxs-lookup"><span data-stu-id="a80ca-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="a80ca-153">Tuotantotilauksessa on avoin nimiketunnuksen RM-100 ja eränumeron B1 kirjauskansio, jonka tyyppi on **Tuotannon keräysluettelo**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="a80ca-154">Voit nyt valita rekisteröinnin jatkamisen esimerkiksi eränumerolla B2. Avoimeen kirjauskansioon lisätään silloin uusi kirjauskansion rivi aina, kun valitset **OK**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="a80ca-155">Kun rekisteröinti on valmis, kirjaa kirjauskansio ja lopeta työnkulku valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="a80ca-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="a80ca-156">Lisäkommentit</span><span class="sxs-lookup"><span data-stu-id="a80ca-156">Additional comments</span></span> 

-   <span data-ttu-id="a80ca-157">Jos käyttäjä peruuttaa työnkulun kirjauskansion rivin luomisen jälkeen, kirjauskansio on kirjaamattomassa tilassa. Jos käyttäjä kuitenkin haluaa myöhemmin käyttää saman tuotantotilauksen työnkulkua, rivit lisätään avoimeen kirjauskansioon eikä uuteen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="a80ca-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="a80ca-158">Uusi työnkulku tukee myös sarjanumeroiden rekisteröintiä.</span><span class="sxs-lookup"><span data-stu-id="a80ca-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="a80ca-159">Nimiketunnus voidaan rekisteröidä vain, jos se on määritetty valitun tuotanto- tai erätilauksen tuoterakenteessa tai kaavassa.</span><span class="sxs-lookup"><span data-stu-id="a80ca-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="a80ca-160">Materiaali voidaan ylikuluttaa.</span><span class="sxs-lookup"><span data-stu-id="a80ca-160">Material can be overconsumed.</span></span> <span data-ttu-id="a80ca-161">Jos esimerkiksi materiaalin kulutusmääräksi arvioidaan 100 lbs, se voidaan sitten ylikuluttaa esimerkiksi määrällä 105 lbs.</span><span class="sxs-lookup"><span data-stu-id="a80ca-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



