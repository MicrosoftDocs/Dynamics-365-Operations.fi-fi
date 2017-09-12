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
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: fi-fi
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="3a7c8-103">Materiaalikulutuksen rekisteröinti mobiililaitteella</span><span class="sxs-lookup"><span data-stu-id="3a7c8-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="3a7c8-104">Tässä ohjeaiheessa käsitellään työnkulkua, jolla tuotannossa kulutettavat raaka-aineet voidaan rekisteröidä kämmenlaitteella.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="3a7c8-105">Johdanto</span><span class="sxs-lookup"><span data-stu-id="3a7c8-105">Introduction</span></span>
------------

<span data-ttu-id="3a7c8-106">Tämä työnkulku on hyödyllinen, jos materiaalin tarkka seuranta on välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="3a7c8-107">Näissä tilanteissa materiaalin jäljitettävyyden ylläpito edellyttää kulutuksen tarkan ajan ja määrän ilmoittamista.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="3a7c8-108">Tämä prosessi voidaan nähdä esi- tai jälkipoiston peilikuvana, sillä näissä toiminnoissa rekisteröinnin ajankohta ja varsinaisen kulutuksen ajankohta poikkeavat toisistaan.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="3a7c8-109">Tämän vuoksi automaattista kulutusstrategiaa ei voi käyttää joissakin materiaaleissa, joissa on edellytyksenä jäljitettävyys.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="3a7c8-110">Tarkastellaan yksinkertainen skenaariota, joka selittää, miten määritetään työnkulku tuotannossa tapahtuvan raaka-aineiden kulutuksen rekisteröintiin kämmenlaitteella.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="3a7c8-111">Skenaarion tiedot</span><span class="sxs-lookup"><span data-stu-id="3a7c8-111">Scenario details</span></span>

<span data-ttu-id="3a7c8-112">Jatkuva tuotantoprosessi (5) kuluttaa eräohjattua raaka-ainetta RM-100.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="3a7c8-113">Materiaali on käytettävissä varaston sijainnissa Bulk-001 (1), rekisterikilpi on PL-1 ja siinä on kaksi erää B1 ja B2, joiden kummankin määrä 100 lbs.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="3a7c8-114">RM-100:n varastotyö (2) vapautetaan ja käsitellään. Materiaali kerätään sijainnista Bulk-001 tuotannon varastoinnin sijaintiin PIL-01 (3), joka on määritetty rekisterikilpiohjatuksi sijainniksi.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="3a7c8-115">Koneenkäyttäjä punnitsee materiaalin tuotannon varastointisijainnissa (3) ja rekisteröi painon. Eränumero on kulutettu (4).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="3a7c8-116">Osa materiaalista lisätään tuotannon varastoinnin sijainnista tuotantoprosessiin määritetyin aikavälein.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="3a7c8-117">Kun koneenkäyttäjä lisää materiaalia, se punnitaan vaa'alla ja eränumero rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="3a7c8-118">Työnkulun määrittäminen rekisteröimään kulutus kämmenlaitteella</span><span class="sxs-lookup"><span data-stu-id="3a7c8-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="3a7c8-119">Luo valmis tuote, FG 100, tuoterakenteella, jossa on eräohjattua raaka-ainetta RM-100.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="3a7c8-120">Lisää RM-100:n kaksi erää, B1 ja B2, joissa on määrä 100, sijaintiin Bulk-001, jossa on rekisterikilpi PL-1.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="3a7c8-121">RM-100:n tuoterakennerivin materiaaliottosäännöksi on valittu **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="3a7c8-122">Määritä tuotannon varastoinnin sijainniksi PIL-01.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="3a7c8-123">Voit tehdä sen valitsemalla tämän sijainnin tuotannon varastoinnin oletussijainniksi varastossa 51.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="3a7c8-124">Luo uusi mobiililaitteen valikkovaihtoehto:</span><span class="sxs-lookup"><span data-stu-id="3a7c8-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="3a7c8-125">**Valikkovaihtoehdon nimi** – Rekisteröi materiaalikulutus.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="3a7c8-126">**Ruutu** – Rekisteröi materiaalikulutus.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="3a7c8-127">**Menetelmä** – Epäsuora.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="3a7c8-128">**Toimintokoodi** – Rekisteröi materiaalikulutus.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="3a7c8-129">Lisää valikkovaihtoehto **tuotannon mobiililaitteen** valikkoon.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="3a7c8-130">Luo valmiin tuotteen tuotantotilaus:</span><span class="sxs-lookup"><span data-stu-id="3a7c8-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="3a7c8-131">**Nimiketunnus** – FG-100</span><span class="sxs-lookup"><span data-stu-id="3a7c8-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="3a7c8-132">**Toimipaikka** – 5</span><span class="sxs-lookup"><span data-stu-id="3a7c8-132">**Site** - 5</span></span> 
-    <span data-ttu-id="3a7c8-133">**Varasto** – 51</span><span class="sxs-lookup"><span data-stu-id="3a7c8-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="3a7c8-134">**Määrä** – 150</span><span class="sxs-lookup"><span data-stu-id="3a7c8-134">**Quantity** - 150</span></span>

<span data-ttu-id="3a7c8-135">Tuotantotilaus on **arvioitu** ja **vapautettu** ja varastotyö on luotu.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="3a7c8-136">Suorita työ käyttämällä kämmenlaitteelle suunniteltua raaka-aineiden keräilyn työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="3a7c8-137">Työnkulku siirtää materiaalin bulkkisijainnista tuotannon varastoinnin sijaintiin PIL-01.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="3a7c8-138">Kun työ on suoritettu, materiaalin tila on **kerätty tuotannon varastoinnin sijainnissa**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="3a7c8-139">Työn käsittelyn jälkeen tila on joko **Keräilty** tai **Varattu fyysinen**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="3a7c8-140">Tämä on määritetty parametrilla **Jälkeen-varasto-ottotila viety varastolomakkeeseen**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="3a7c8-141">Käynnistä tuotantotilaus asiakasohjelmasta tai kämmenlaitteesta **Tuotannon käynnistys** -valikkovaihtoehdosta.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="3a7c8-142">Kun tuotantotilaus on käynnistetty, voit rekisteröidä materiaalikulutuksen kämmenlaitteen työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="3a7c8-143">Aloitetaan rekisteröimällä 25 lbs:n kulutus erässä B1.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="3a7c8-144">Valitse kämmenlaitteen valikossa **Rekisteröi** **materiaalikulutus** ja anna seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="3a7c8-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="3a7c8-145">Tuotantotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-145">The production order number.</span></span> 
-    <span data-ttu-id="3a7c8-146">Sijainti, jossa materiaali aiotaan kuluttaa eli tässä tapauksessa PIL-01.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="3a7c8-147">Nimiketunnus RM-100.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="3a7c8-148">Eränumero B1.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-148">Batch number B1.</span></span> 
-    <span data-ttu-id="3a7c8-149">Määrä 25.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="3a7c8-150">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-150">Select **OK**.</span></span>

<span data-ttu-id="3a7c8-151">Huomaa, että näyttöön avautuu sanoma Kirjauskansion rivi on luotu.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="3a7c8-152">Tuotantotilauksessa on avoin nimiketunnuksen RM-100 ja eränumeron B1 kirjauskansio, jonka tyyppi on **Tuotannon keräysluettelo**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="3a7c8-153">Voit nyt valita rekisteröinnin jatkamisen esimerkiksi eränumerolla B2. Avoimeen kirjauskansioon lisätään silloin uusi kirjauskansion rivi aina, kun valitset **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="3a7c8-154">Kun rekisteröinti on valmis, kirjaa kirjauskansio ja lopeta työnkulku valitsemalla **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="3a7c8-155">Lisäkommentit</span><span class="sxs-lookup"><span data-stu-id="3a7c8-155">Additional comments</span></span> 

-   <span data-ttu-id="3a7c8-156">Jos käyttäjä peruuttaa työnkulun kirjauskansion rivin luomisen jälkeen, kirjauskansio on kirjaamattomassa tilassa. Jos käyttäjä kuitenkin haluaa myöhemmin käyttää saman tuotantotilauksen työnkulkua, rivit lisätään avoimeen kirjauskansioon eikä uuteen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="3a7c8-157">Uusi työnkulku tukee myös sarjanumeroiden rekisteröintiä.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="3a7c8-158">Nimiketunnus voidaan rekisteröidä vain, jos se on määritetty valitun tuotanto- tai erätilauksen tuoterakenteessa tai kaavassa.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="3a7c8-159">Materiaali voidaan ylikuluttaa.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-159">Material can be overconsumed.</span></span> <span data-ttu-id="3a7c8-160">Jos esimerkiksi materiaalin kulutusmääräksi arvioidaan 100 lbs, se voidaan sitten ylikuluttaa esimerkiksi määrällä 105 lbs.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



