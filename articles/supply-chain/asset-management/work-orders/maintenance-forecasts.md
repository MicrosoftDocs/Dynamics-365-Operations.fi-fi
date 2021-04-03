---
title: Ylläpitoennusteet
description: Tässä ohjeaiheessa kerrotaan ylläpitoennusteista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5cf1a634ef5ab60707cf471ef017ec167e3013f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263659"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="88bb0-103">Ylläpitoennusteet</span><span class="sxs-lookup"><span data-stu-id="88bb0-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="88bb0-104">Kun luot työtilauksen, luot työtilaustehtäviä, joilla on siihen liittyvät resurssit ja ylläpitotyötyypit.</span><span class="sxs-lookup"><span data-stu-id="88bb0-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="88bb0-105">Kun ylläpitoennusteita sisältävä ylläpitopitotöiden tyyppi valitaan, ennusteet kopioidaan automaattisesti työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="88bb0-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="88bb0-106">Saatat voida lisätä ennusterivejä työtilaukseen tai poistaa niitä työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="88bb0-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="88bb0-107">Työtilauksen elinkaaritilan, siihen liittyvän projektityypin ja projektityyppiin liittyvien vaihesääntöjen määrittäminen määrittää, voitko lisätä tai muokata ennusterivejä.</span><span class="sxs-lookup"><span data-stu-id="88bb0-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="88bb0-108">Lisätietoja työtilausten elinkaaritiloista ja niihin liittyvistä projektin vaiheista on kohdassa [Ennusteet, työtilaukset ja projektit](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="88bb0-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="88bb0-109">Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="88bb0-110">Valitse työtilaus luettelosta ja sitten toimintoruudun > **Työtilaus**-välilehden > **Projekti**-ryhmässä **Ennuste**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="88bb0-111">**Työtilauksen ylläpitoennuste** -sivulla näytetään työtilaustehtävässä valitun ylläpitotyön tyypin ennusterivit.</span><span class="sxs-lookup"><span data-stu-id="88bb0-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="88bb0-112">Tuntiennusteen lisääminen työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="88bb0-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="88bb0-113">Valitse **Työtilauksen ylläpitoennuste** -sivulla työtilaus, jolle lisätään ennuste.</span><span class="sxs-lookup"><span data-stu-id="88bb0-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="88bb0-114">Luo uusi rivi valitsemalla **Tunnit**-pikavälilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="88bb0-115">Valitse luokka **Luokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="88bb0-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="88bb0-116">Lisää ennustettujen tuntien määrä **Tunnit**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="88bb0-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="88bb0-117">Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.</span><span class="sxs-lookup"><span data-stu-id="88bb0-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="88bb0-118">Nimike-ennusteen lisääminen työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="88bb0-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="88bb0-119">Työtilauksen ylläpitoennusteeseen voi lisätä nimikkeitä kolmella tavalla.</span><span class="sxs-lookup"><span data-stu-id="88bb0-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="88bb0-120">Voit luoda rivejä nimikkeille (varaosille), jotka eivät sisälly varaosaluetteloon tai resurssirakenteeseen (BOM), voit valita varaosia hyväksytystä varaosaluettelosta tai voit valita nimikkeitä resurssirakenteesta.</span><span class="sxs-lookup"><span data-stu-id="88bb0-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="88bb0-121">Valitse **Työtilauksen ylläpitoennuste** -sivulla työtilaus, jolle lisätään ennuste.</span><span class="sxs-lookup"><span data-stu-id="88bb0-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="88bb0-122">Lisää **Nimikkeet**-pikavälilehdessä nimikkeitä ylläpitoennusteeseen käyttämällä asianmukaista menetelmää.</span><span class="sxs-lookup"><span data-stu-id="88bb0-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="88bb0-123">Voit luoda rivin varaosalle, joka ei ole varaosaluettelossa tai resurssirakenteessa, seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="88bb0-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="88bb0-124">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-124">Select **Add**.</span></span>
2. <span data-ttu-id="88bb0-125">Valitse **Nimiketunnus**-kentässä nimike.</span><span class="sxs-lookup"><span data-stu-id="88bb0-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="88bb0-126">Syötä määrä **Myyntimäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="88bb0-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="88bb0-127">Valitse määrän mittayksikkö **Yksikkö**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="88bb0-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="88bb0-128">Valitse **Kustannushinta**- ja **Valuutta**-kenttiin asianmukaiset arvot.</span><span class="sxs-lookup"><span data-stu-id="88bb0-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="88bb0-129">Valitse rivin ominaisuus kentästä **Rivin ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="88bb0-130">Jos haluat muuttaa nimikeriveillä näkyvien dimensioiden luetteloa, valitse **Varasto** > **Näytä dimensiot**,valitse dimensiot ja aseta sitten **Tallenna määritys** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="88bb0-131">Voit lisätä varaosan hyväksytystä varaosaluettelosta seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="88bb0-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="88bb0-132">Valitse **Lisää varaosia**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="88bb0-133">Valitse varaosa ja muokkaa siihen liittyviä tietoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="88bb0-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="88bb0-134">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-134">Select **OK**.</span></span>

<span data-ttu-id="88bb0-135">Voit lisätä nimekkeen resurssirakenteesta seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="88bb0-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="88bb0-136">Valitse **Lisää resurssirakennenimikkeitä**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="88bb0-137">Valitse nimike ja muokkaa siihen liittyviä tietoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="88bb0-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="88bb0-138">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-138">Select **OK**.</span></span>

<span data-ttu-id="88bb0-139">Saat yleiskatsauksen siitä, miten valitulla rivillä olevaa nimikettä käytetään resurssienhallinnassa suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="88bb0-140">Lisätietoja tästä yleiskatsauksesta esitetään kohdassa [Nimike, missä käytetty](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="88bb0-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="88bb0-141">Kuluennusteen lisääminen työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="88bb0-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="88bb0-142">Valitse **Työtilauksen ylläpitoennuste** -sivulla työtilaus, jolle lisätään ennuste.</span><span class="sxs-lookup"><span data-stu-id="88bb0-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="88bb0-143">Luo rivi valitsemalla **Kulu**-pikavälilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="88bb0-144">Valitse luokka **Luokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="88bb0-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="88bb0-145">Anna määrä **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="88bb0-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="88bb0-146">Syötä asianmukaiset arvot kenttiin **Kustannushinta**, **Myyntivaluutta** ja **Myyntihinta**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="88bb0-147">Valitse **Rivin ominaisuus** -kentässä rivillä käytettävä kulutyyppi.</span><span class="sxs-lookup"><span data-stu-id="88bb0-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="88bb0-148">**Ylläpitoennusteen summat** -pikavälilehdessä näkyy yhteenveto kussakin pikavälilehdessä luotujen rivien määrästä valitussa työtilaustehtävässä ja työtilauksessa.</span><span class="sxs-lookup"><span data-stu-id="88bb0-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="88bb0-149">Voit myös tarkastella työtilaustyön ja työtilauksen ennustettujen työtuntien summaa.</span><span class="sxs-lookup"><span data-stu-id="88bb0-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="88bb0-150">Seuraavassa kuvassa on esimerkki **Työtilauksen ylläpitoennuste** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="88bb0-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Kuva 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="88bb0-152">Työtilausennusteiden automaattinen päivitys</span><span class="sxs-lookup"><span data-stu-id="88bb0-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="88bb0-153">Jos tuntikustannuksia, nimikekustannuksia ja kuluja päivitetään muissa Microsoft Dynamics 365 for Finance and Operations -moduuleissa, resurssienhallinnan työtilausten ennusteet voidaan päivittää automaattisesti kyseisten muutosten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="88bb0-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="88bb0-154">Tämä ominaisuus auttaa varmistamaan, että työtilausennusteissa käytetään aina viimeisimpiä kustannushintoja.</span><span class="sxs-lookup"><span data-stu-id="88bb0-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="88bb0-155">Samanlaisia päivityksiä voidaan tehdä myös [kunnossapitotöiden tyyppien ennusteille.](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)</span><span class="sxs-lookup"><span data-stu-id="88bb0-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="88bb0-156">Valitse **Resurssienhallinta** > **Kausittainen** > **Ennuste** > **Päivitä työtilauksen ennuste**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="88bb0-157">Voit tarvittaessa lisätä tiettyjä työtilauksia tai työtilaustehtäviä koskevia valintoja **Päivitä työtilauksen ennuste** -valintaikkunan **Sisällytettävät tietueet** -pikavälilehdessä</span><span class="sxs-lookup"><span data-stu-id="88bb0-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="88bb0-158">Tee tarvittavat valinnat valitsemalla **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="88bb0-159">**Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="88bb0-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="88bb0-160">Käynnistä ennusteen päivitys valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="88bb0-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="88bb0-161">Seuraavassa kuvassa on esimerkki **Päivitä työtilauksen ennuste** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="88bb0-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Kuva 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]