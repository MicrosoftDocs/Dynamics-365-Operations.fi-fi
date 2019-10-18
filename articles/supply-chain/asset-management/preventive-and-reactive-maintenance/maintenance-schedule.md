---
title: Ylläpitoaikataulu
description: Tässä ohjeaiheessa kerrotaan ylläpitoaikataulusta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af2152b334b51db48b60aa966ab49bf480c29bbc
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922134"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="9d10f-103">Ylläpitoaikataulu</span><span class="sxs-lookup"><span data-stu-id="9d10f-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9d10f-104">Huoltoaikataulu sisältää luettelon kaikista odotetuista ennaltaehkäisevistä huoltosuunnitelmista, huoltopyynnöistä ja huoltokierroksista. Jotkin aikataulurivit on saatettu muuntaa työtilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="9d10f-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="9d10f-105">Huoltoaikataulun neljä näkymää ovat hieman erilaiset sen mukaan, mitä kunnossapitoaikataulurivejä haluat nähdä.</span><span class="sxs-lookup"><span data-stu-id="9d10f-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="9d10f-106">Valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="9d10f-106">Menu item</span></span>                  | <span data-ttu-id="9d10f-107">Sisällön kuvaus</span><span class="sxs-lookup"><span data-stu-id="9d10f-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d10f-108">Kaikki ylläpitoaikataulut</span><span class="sxs-lookup"><span data-stu-id="9d10f-108">All maintenance schedule</span></span>       | <span data-ttu-id="9d10f-109">Kaikki huoltoaikataulurivit näkyvät.</span><span class="sxs-lookup"><span data-stu-id="9d10f-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="9d10f-110">Oma resurssiaikataulu</span><span class="sxs-lookup"><span data-stu-id="9d10f-110">My asset schedule</span></span>        | <span data-ttu-id="9d10f-111">Tässä luettelossa näkyvät kaikki huoltoaikataulurivit, jotka sisältävät käyttökohteita, jotka on asennettu toiminnallisiin siajinteihin, joihin olet yhteydessä työntekijänä ([Kunnossapitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="9d10f-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="9d10f-112">Avaa ylläpitoaikataulun rivit</span><span class="sxs-lookup"><span data-stu-id="9d10f-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="9d10f-113">Tässä luettelossa näkyvät ylläpitoaikataulurivit, joiden tila on Luotu, eli niitä ei ole vielä muunnettu työtilaukseksi tai hylätty.</span><span class="sxs-lookup"><span data-stu-id="9d10f-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="9d10f-114">Avaa ylläpitoaikataulun poolit</span><span class="sxs-lookup"><span data-stu-id="9d10f-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="9d10f-115">Tässä luettelossa näkyvät työtilauspooliin liittyvät huollonajoitusrivit.</span><span class="sxs-lookup"><span data-stu-id="9d10f-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="9d10f-116">Jos huoltoaikataulurivi sisältyy useisiin työtilauspooleihin (lisätietoja on kohdassa [Työtilauspoolit](../work-orders/work-order-pools.md)), kullekin poolille näytetään yksi tietue kohdassa **Avoimet ylläpitoaikataulupoolit**.</span><span class="sxs-lookup"><span data-stu-id="9d10f-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="9d10f-117">Tämä tehdään työtilauspoolien suodatusasetusten optimoimiseksi.</span><span class="sxs-lookup"><span data-stu-id="9d10f-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="9d10f-118">Ylläpitoaikataulun avaaminen:</span><span class="sxs-lookup"><span data-stu-id="9d10f-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="9d10f-119">Valitse **Resurssien hallinta** > **Yhteiset** > **Ylläpitoaikataulu** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit**.</span><span class="sxs-lookup"><span data-stu-id="9d10f-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="9d10f-120">Päivitä ylläpitoaikataulu valitsemalla **Ylläpitosuunnitelma** tai **Ylläpitokierrokset.**</span><span class="sxs-lookup"><span data-stu-id="9d10f-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="9d10f-121">Voit muokata huoltoaikataulun riviä valitsemalla sen ja valitsemalla sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="9d10f-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="9d10f-122">Voit esimerkiksi päivittää helposti palvelutason tai työntekijän, joka vastaa työstä.</span><span class="sxs-lookup"><span data-stu-id="9d10f-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="9d10f-123">Voit muokata vain sellaisia ylläpitoaikataulurivejä, joita ei ole vielä liitetty työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="9d10f-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="9d10f-124">Voit poistaa huoltoaikataulurivin valitsemalla sen luettelosivulta ja valitsemalla sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9d10f-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="9d10f-125">Voit hylätä huoltoaikataulurivin valitsemalla sen luettelosivulta ja valitsemalla sitten **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="9d10f-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="9d10f-126">Tämä toiminto on hyödyllinen esimerkiksi silloin, kun käyttöomaisuuserään liittyy 2 000 km huoltosuunnitelma ja 10 000 km huoltosuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="9d10f-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="9d10f-127">Tämän jälkeen voit hylätä 2 000 km huoltosuunnitelmasta luodun rivin, kun se on sama kuin 10 000 km, 20 000 km, 30 000 km huollossa ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="9d10f-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="9d10f-128">Jos hylkäät huoltosuunnitelmaan liittyvän huoltoaikataulurivin, kyseinen rivi ei enää tule näkyviin, kun huoltosuunnitelma ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="9d10f-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="9d10f-129">Voit valita huoltoaikataulurivien määrän kaikissa valitsemalla **Kaikki ylläpitoaikataulut** -kohdassa **Työtilauspooli**, jos haluat, että kaikki valitut rivit sisällytetään samaan työtilauspooliin.</span><span class="sxs-lookup"><span data-stu-id="9d10f-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="9d10f-130">Voit valita huoltoaikataulu rivien määrän kohdassa **Kaikki ylläpitoaikataulut**, **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit** ja napsauttamalla **Säädä aikataulua**, jos haluat tehdä samat muutokset useille riveille.</span><span class="sxs-lookup"><span data-stu-id="9d10f-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="9d10f-131">Voit muuttaa valittuihin huoltoaikataulu riveihin liittyviä alkamis- ja päättymispäiviä, palvelutasoa ja vastuullista ylläpitotyöntekijäryhmää tai vastuullista kunnossapitotyöntekijää.</span><span class="sxs-lookup"><span data-stu-id="9d10f-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="9d10f-132">Kun kunnossapitoaikataulun rivi on liitetty työtilaukseen, työtilauksen tunnus näkyy **Työtilaus-** kentässä.</span><span class="sxs-lookup"><span data-stu-id="9d10f-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="9d10f-133">**Kaikki resurssit** -tietonäkymän **Resurssin ylläpitosuunnitelmat** -pikavälilehdessä voit valita omaisuuserän ylläpitosuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="9d10f-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="9d10f-134">Jos myöhemmin poistat resurssiiin liittyvän ylläpitosuunnitelman rivin **Kaikki resurssit** -kohdassa, poistat myös automaattisesti kaikki kunnossapitoaikataulurivit, joiden tila on Luotu ja jotka on luotu kyseisen ylläpitosuunnitelman perusteella.</span><span class="sxs-lookup"><span data-stu-id="9d10f-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="9d10f-135">Katso myös [Luo resurssi](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="9d10f-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="9d10f-136">Alla olevassa kuvassa näkyy **Kaikki ylläpitoaikataulut** -luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="9d10f-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Kuva 1](media/16-preventive-maintenance.png)

