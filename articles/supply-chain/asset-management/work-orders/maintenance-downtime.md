---
title: Ylläpidon käyttökatko
description: Tässä ohjeaiheessa kuvataan ylläpidon käyttökatkoja resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918241"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="700b1-103">Ylläpidon käyttökatko</span><span class="sxs-lookup"><span data-stu-id="700b1-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="700b1-104">Voit luoda huoltoseisokkien rekisteröintejä työtilauksessa valitulle käyttöomaisuudelle.</span><span class="sxs-lookup"><span data-stu-id="700b1-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="700b1-105">Tästä on hyötyä, jos haluat rekisteröidä huoltoseisokit yhdelle tai useammalle tuotantoalueen koneelle.</span><span class="sxs-lookup"><span data-stu-id="700b1-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="700b1-106">Ensin luodaan huoltoseisokkien syykoodit, joita haluat käyttää, esimerkiksi erittely ja suunniteltu pysähdys.</span><span class="sxs-lookup"><span data-stu-id="700b1-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="700b1-107">Tämä tehdään kohdassa **Ylläpidon käyttökatkon syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="700b1-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="700b1-108">Seuraavaksi voit luoda kunnossapitoseisokkeja koskevia rekisteröintejä **Ylläpidon käyttökatko** -kohdassa ja lisätä tarvittavat syykoodit.</span><span class="sxs-lookup"><span data-stu-id="700b1-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="700b1-109">Kunnossapitoseisokkien syykoodien luominen</span><span class="sxs-lookup"><span data-stu-id="700b1-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="700b1-110">Valitse **Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Ylläpidon käyttökatkon syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="700b1-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="700b1-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="700b1-111">Click **New**.</span></span>

3. <span data-ttu-id="700b1-112">Lisää tunnus **Ylläpidon käyttökatkon syykoodi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="700b1-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="700b1-113">Kirjoita **Nimi**-kenttään syykoodin nimi.</span><span class="sxs-lookup"><span data-stu-id="700b1-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="700b1-114">Valitse **KPI, sisällytä** -valintaruutu, jos syykoodi sisällytetään käyttöomaisuuden KPI-laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="700b1-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="700b1-115">Suunniteltuja tuotanto pysähdyksiä ei yleensä sisällytetä KPI-laskelmiin, koska ne eivät vaikuta odotettuun suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="700b1-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="700b1-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="700b1-116">Click **Save**.</span></span>

![Kuva 1](media/15-work-orders.png)


<span data-ttu-id="700b1-118">Kun olet luonut huoltoseisokkien syykoodit, joita haluat käyttää, voit luoda työtilauksille ja käyttöomaisuudelle kunnossapitoseisokkimerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="700b1-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="700b1-119">Kunnossapitoseisokkien reskiteröintien luominen</span><span class="sxs-lookup"><span data-stu-id="700b1-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="700b1-120">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="700b1-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="700b1-121">Valitse työtilaus ja valitse **Ylläpidon käyttökatko**.</span><span class="sxs-lookup"><span data-stu-id="700b1-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="700b1-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="700b1-122">Click **New**.</span></span>

4. <span data-ttu-id="700b1-123">Lisää huoltoseisokkien rekisteröimisen päivämäärä ja aika **Alkaen**- ja **Asti**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="700b1-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="700b1-124">Kun poistut **Asti**-kentästä, kesto tunteina lisätään automaattisesti **Kesto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="700b1-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="700b1-125">Valitse syykoodi **Ylläpidon käyttökatkon syykoodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="700b1-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="700b1-126">Toista vaiheet 3-6, jos haluat lisätä uusia rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="700b1-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="700b1-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="700b1-127">Click **Save**.</span></span>


![Kuva 2](media/16-work-orders.png)


<span data-ttu-id="700b1-129">Ylläpitoseisokkien rekisteröintien laskennassa käytettävä kalenteri määräytyy resurssi- ja parametriasetusten valinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="700b1-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="700b1-130">Jos resurssi on valittuna resurssille kohdassa **Kaikki resurssit** > **Käyttöomaisuus-** pikavälilehden **Resurssi**-kentässä, käytetään liittyvän resurssiryhmän kalenteria, joka näkyy seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="700b1-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Kuva 3](media/17-work-orders.png)


<span data-ttu-id="700b1-132">Jos käyttöomaisuudelle ei ole valittu resurssia, käytetään **Resurssienhallinnan parametrit** -kohdassa valittua vakiokalenteria seuraavassa kuvassa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="700b1-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Kuva 4](media/18-work-orders.png)


<span data-ttu-id="700b1-134">Näet yhteenvedon kaikista käyttökatkorekisteröinneistä valitsemalla **Yrityksen resurssien hallinta** > **Kyselyt** > **Ylläpidon käyttökatko**.</span><span class="sxs-lookup"><span data-stu-id="700b1-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="700b1-135">Kaikki **Resurssien hallinta** -moduulissa käytettävät kalenterit määritetään kohdassa **Organisaation hallinto** > **Asetukset** > **Kalenterit** > **Kalenterit**.</span><span class="sxs-lookup"><span data-stu-id="700b1-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

