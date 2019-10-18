---
title: Ylläpitoennusteet
description: Tässä ohjeaiheessa kerrotaan ylläpitoennusteista resurssien hallinnassa.
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
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024496"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="f9fb8-103">Ylläpitoennusteet</span><span class="sxs-lookup"><span data-stu-id="f9fb8-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="f9fb8-104">Kun luot työtilauksen, luot työtilaustyöt, joissa on vastaavat käyttöomaisuudet ja kunnossapitotyölajit.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="f9fb8-105">Kun huoltoennusteita sisältävä kunnossapitotöiden tyyppi valitaan, ennusteet kopioidaan automaattisesti työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="f9fb8-106">Voit ehkä lisätä tai poistaa työtilauksen ennusterivejä.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f9fb8-107">Työtilauksen elinkaaritilan, siihen liittyvän projektityypin ja projektityyppiin liittyvien vaihesääntöjen määrittäminen määrittää, voitko lisätä tai muokata ennusterivejä.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="f9fb8-108">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f9fb8-109">Valitse työtilaus luettelosta ja valitse sitten **Ennuste.**</span><span class="sxs-lookup"><span data-stu-id="f9fb8-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="f9fb8-110">**Työtilauksen ylläpitoennuste** -kohdassa näytetään työtilaustyössä valitun ylläpitotyön tyypin ennusterivit.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="f9fb8-111">Lisää tuntiennuste työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="f9fb8-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="f9fb8-112">Valitse työtilaustyö, johon haluat lisätä ennusteen.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f9fb8-113">Luo uusi rivi napsauttamalla **Tunnit**-pikavälilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="f9fb8-114">Valitse luokka **Luokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="f9fb8-115">Lisää ennustettujen tuntien määrä **Tunnit**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="f9fb8-116">Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="f9fb8-117">Lisää nimike-ennuste työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="f9fb8-117">Add items forecast to a work order</span></span>

<span data-ttu-id="f9fb8-118">Voit lisätä nimikkeitä työtilauksen ylläpitoennusteeseen kolmella tavalla: Voit luoda rivejä nimikkeille (varaosille), jotka eivät sisälly varaosaluetteloon tai käyttöomaisuuden tuoterakenteeseen, voit valita varaosia hyväksytystä varaosaluettelosta ja voit valita nimikkeitä resurssin tuoterakenteesta.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="f9fb8-119">Valitse työtilaustyö, johon haluat lisätä ennusteen.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f9fb8-120">Valitse **Nimikkeet**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="f9fb8-121">Valitse **Lisää**, jos haluat luoda uuden rivin varaosalle, joka ei ole varaosaluettelossa tai käyttöomaisuuden tuoterakenneluettelossa.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="f9fb8-122">Valitse **Nimiketunnus**-kentässä nimike.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="f9fb8-123">Lisää määrä **Myyntimäärä**-kenttään ja valitse määrän yksikkö **Yksikkö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="f9fb8-124">Lisää kustannushinta ja valuutta asianmukaisiin kenttiin ja valitse **Rivin ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="f9fb8-125">Jos haluat muuttaa nimikeriveillä näkyvien dimensioiden luetteloa, valitse **Varasto** > **Näytä dimensiot**, valitse dimensiot ja valitse sitten **Tallenna asetukset** -vaihtopainikkeessa Kyllä.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="f9fb8-126">Jos haluat lisätä huoltoennusteeseen hyväksytyn varaosan, valitse **Lisää varaosia**, valitse varaosa, muokkaa tietoja tarvittaessa ja valitse **OK.**</span><span class="sxs-lookup"><span data-stu-id="f9fb8-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="f9fb8-127">Jos haluat lisätä käyttöomaisuuden tuoterakennenimikkeitä ennusteeseen, valitse **Lisää tuoterakennenimikkeitä**, valitse nimike, muokkaa siihen liittyviä tietoja tarvittaessa ja valitse **OK.**</span><span class="sxs-lookup"><span data-stu-id="f9fb8-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="f9fb8-128">Valitse **Nimike, missä käytetty**saadaksesi yleiskatsauksen siitä, missä resurssien hallinnassa valitulla rivillä olevaa nimikettä käytetään suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="f9fb8-129">Lisää kuluennuste työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="f9fb8-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="f9fb8-130">Tässä ohjeaiheessa selitetään, kuinka voit lisätä kuluennusteen työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="f9fb8-131">Valitse lomakkeen vasemmasta reunasta työtilaustyö, johon haluat lisätä ennusteen.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f9fb8-132">Valitse **Kulu**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="f9fb8-133">Luo uusi rivi valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="f9fb8-134">Valitse luokka **Luokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="f9fb8-135">Anna määrä **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="f9fb8-136">Lisää kustannushinta, myyntivaluutta ja myyntihinta asianmukaisiin kenttiin.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="f9fb8-137">Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="f9fb8-138">**Ylläpitoennusteen summat** -pikavälilehdessä näkyy yhteenveto kussakin välilehdessä luotujen rivien määrästä valitussa työtilaustyössä ja työtilauksessa.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="f9fb8-139">Voit myös tarkastella työtilaustyön ja työtilauksen ennustettujen työtuntien summaa.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Kuva 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="f9fb8-141">Työtilausennusteiden automaattinen päivitys</span><span class="sxs-lookup"><span data-stu-id="f9fb8-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="f9fb8-142">Resurssien hallinnassa voit päivittää automaattisesti työtilausten ennusteiden muutokset, jotka koskevat tuntikustannuksia, nimikekustannuksia ja kuluja, jotka on päivitetty muissa moduuleissa.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="f9fb8-143">Näin varmistat, että viimeisimpiä kustannushintoja käytetään aina työtilausennusteissa.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="f9fb8-144">Samanlaisia päivityksiä voidaan tehdä myös [kunnossapitotöiden tyyppien ennusteille.](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)</span><span class="sxs-lookup"><span data-stu-id="f9fb8-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="f9fb8-145">Valitse **Resurssien hallinta** > **Kausittainen** > **Ennuste** > **Päivitä työtilauksen ennuste**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="f9fb8-146">Avattavassa **Päivitä työtilauksen ennuste** -valintaikkunassa voit lisätä tarvittaessa tiettyjä työtilauksia tai työtilaustöitä koskevia valintoja.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="f9fb8-147">Tee haluamasi valinnat valitsemalla **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="f9fb8-148">**Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="f9fb8-149">Käynnistä ennusteen päivitys valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9fb8-149">Click **OK** to start the forecast update.</span></span>


![Kuva 2](media/07-work-orders.png)

