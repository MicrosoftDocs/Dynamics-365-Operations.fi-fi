---
title: Työtilausten ylläpidon käyttökatko
description: Tässä aiheessa on tietoja ylläpidon käyttökatkojen rekisteröinneistä työtilauksessa valitulle resurssille.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba24ae9e82debf9a67761e4e2ca0817e1645db28
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209728"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="9c002-103">Työtilausten ylläpidon käyttökatko</span><span class="sxs-lookup"><span data-stu-id="9c002-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="9c002-104">Voit luoda ylläpidon käyttökatkojen rekisteröintejä työtilauksessa valitulle resurssille.</span><span class="sxs-lookup"><span data-stu-id="9c002-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="9c002-105">Tästä on hyötyä, jos haluat rekisteröidä ylläpidon käyttökatkoja yhdelle tai useammalle tuotantoalueen koneelle.</span><span class="sxs-lookup"><span data-stu-id="9c002-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="9c002-106">Ensin luodaan ylläpidon käyttökatkon syykoodit, joita haluat käyttää, kuten **Erittely** ja **Suunniteltu pysäytys**.</span><span class="sxs-lookup"><span data-stu-id="9c002-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="9c002-107">Tämä tehdään sivulla **Ylläpidon käyttökatkon syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="9c002-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="9c002-108">Seuraavaksi voit luoda kunnossapitoseisokkeja koskevia rekisteröintejä **Ylläpidon käyttökatko** -sivulla ja lisätä tarvittavat ylläpidon käyttökatkon syykoodit.</span><span class="sxs-lookup"><span data-stu-id="9c002-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="9c002-109">Kunnossapitoseisokkien syykoodien luominen</span><span class="sxs-lookup"><span data-stu-id="9c002-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="9c002-110">Valitse **Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Ylläpidon käyttökatkon syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="9c002-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="9c002-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9c002-111">Select **New**.</span></span>

3. <span data-ttu-id="9c002-112">Syötä **Ylläpidon käyttökatkon syykoodi** -kenttään tunnus ylläpidon käyttökatkon syykoodille.</span><span class="sxs-lookup"><span data-stu-id="9c002-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="9c002-113">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9c002-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="9c002-114">Valitse **KPI, sisällytä** -valintaruutu, jos syykoodi on tarkoitus ottaa huomioon resurssin suorituskykyilmaisimien (KPI) laskennassa.</span><span class="sxs-lookup"><span data-stu-id="9c002-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="9c002-115">Yleisesti ottaen suunniteltuja tuotantokatkoja ei pitäisi sisällyttää KPI-laskelmiin, koska ne eivät vaikuta odotettuun suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="9c002-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="9c002-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9c002-116">Select **Save**.</span></span>

<span data-ttu-id="9c002-117">Alla olevassa kuvassa on esimerkki **Ylläpidon käyttökatkon syykoodit** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="9c002-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Kuva 1](media/15-work-orders.png)

<span data-ttu-id="9c002-119">Kun olet luonut ylläpidon käyttökatkon syykoodit, joita haluat käyttää, voit luoda työtilauksille ja käyttöomaisuudelle ylläpidon käyttökatkorekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="9c002-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="9c002-120">Kunnossapitoseisokkien reskiteröintien luominen</span><span class="sxs-lookup"><span data-stu-id="9c002-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="9c002-121">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="9c002-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9c002-122">Valitse työtilaus luettelosta ja sitten toimintoruudun **Työtilaus**-välilehden **Resurssi**-ryhmässä **Ylläpidon käyttökatko**.</span><span class="sxs-lookup"><span data-stu-id="9c002-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="9c002-123">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9c002-123">Select **New**.</span></span>

4. <span data-ttu-id="9c002-124">Lisää ylläpidon käyttökatkojen rekisteröinnin päivämäärä- ja aikaväli kenttiin **Alkaen** ja **Asti**.</span><span class="sxs-lookup"><span data-stu-id="9c002-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="9c002-125">Kun poistut **Asti**-kentästä, kesto tunteina lisätään automaattisesti **Kesto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9c002-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="9c002-126">Valitse syykoodi **Ylläpidon käyttökatkon syykoodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="9c002-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="9c002-127">Voit lisätä rekisteröintejä toistamalla kohtien 3–5 toimet.</span><span class="sxs-lookup"><span data-stu-id="9c002-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="9c002-128">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9c002-128">Select **Save**.</span></span>

<span data-ttu-id="9c002-129">Alla olevassa kuvassa näkyy esimerkki ylläpidon käyttökatkon rekisteröinnistä.</span><span class="sxs-lookup"><span data-stu-id="9c002-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Kuva 2](media/16-work-orders.png)

<span data-ttu-id="9c002-131">Ylläpidon käyttökatkojen rekisteröintien laskennassa käytettävä kalenteri määräytyy resurssi- ja parametriasetusten valinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="9c002-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="9c002-132">Jos resurssi on valittuna resurssille **Kaikki resurssit** -sivun **Käyttöomaisuus**-pikavälilehden **Resurssi**-kentässä, käytetään liittyvän resurssiryhmän kalenteria, joka näkyy seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="9c002-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Kuva 3](media/17-work-orders.png)

<span data-ttu-id="9c002-134">Jos käyttöomaisuudelle ei ole valittu resurssia, käytetään **Resurssienhallinnan parametrit** -sivulla valittua vakiokalenteria seuraavassa kuvassa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="9c002-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Kuva 4](media/18-work-orders.png)

<span data-ttu-id="9c002-136">Näet yhteenvedon kaikista ylläpidon käyttökatkojen rekisteröinneistä valitsemalla **Resurssienhallinta** > **Kyselyt** > **Ylläpidon käyttökatko**.</span><span class="sxs-lookup"><span data-stu-id="9c002-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="9c002-137">Kaikki **Resurssien hallinta** -moduulissa käytettävät kalenterit määritetään kohdassa **Organisaation hallinto** > **Asetukset** > **Kalenterit** > **Kalenterit**.</span><span class="sxs-lookup"><span data-stu-id="9c002-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]