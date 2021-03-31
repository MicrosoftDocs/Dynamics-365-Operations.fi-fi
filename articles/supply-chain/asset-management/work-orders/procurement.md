---
title: Hankinta
description: Tässä ohjeaiheessa kerrotaan hankinnasta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6ed3bc581c4260ca5b4f673f9f66853f4f6f490b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223503"
---
# <a name="procurement"></a><span data-ttu-id="8a82f-103">Hankinta</span><span class="sxs-lookup"><span data-stu-id="8a82f-103">Procurement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a82f-104">Resurssienhallinnassa voit saada yleiskatsauksen työtilauksiin liittyvistä ostoehdotuksista ja ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="8a82f-104">In Asset Management, you can get an overview of purchase requisitions and purchase orders that are related to work orders.</span></span> <span data-ttu-id="8a82f-105">Voit myös luoda työtilauksesta ostotilauksen tai ostoehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="8a82f-105">You can also create a purchase order or a purchase requisition from a work order.</span></span>

<span data-ttu-id="8a82f-106">**Työtilauksen ostoehdotus** -luettelosivulla (**Resurssien hallinta** > **Yhteiset** > **Hankinta** > **Työtilauksen ostoehdotus**), näkyy luettelo työtilauksiin liittyvistä ostoehdotuksista.</span><span class="sxs-lookup"><span data-stu-id="8a82f-106">The **Work order purchase requisition** list page (**Asset management** > **Common** > **Procurement** > **Work order purchase requisition**) shows a list of purchase requisitions that are related to work orders.</span></span> <span data-ttu-id="8a82f-107">Kun valitset työtilaustehtävän tällä sivulla, voit käyttää **Näytä**-ryhmän painikkeita toimintoruudun **Työtilauksen ostoehdotus** -välilehdessä suorittaaksesi erilaisia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="8a82f-107">When you select a work order job on this page, you can use the buttons in the **Show** group on the **Work order purchase requisition** Action Pane tab to perform various actions:</span></span>

- <span data-ttu-id="8a82f-108">Avaa liittyvä ostoehdotus valitsemalla **Ostoehdotus**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-108">To open the related purchase requisition, select **Purchase requisition**.</span></span> 
- <span data-ttu-id="8a82f-109">Avaa liittyvä työtilaus valitsemalla **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-109">To open the related work order, select **Work order**.</span></span>
- <span data-ttu-id="8a82f-110">Saat yleiskatsauksen siitä, miten valitulla rivillä olevaa nimikettä käytetään resurssienhallinnassa suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-110">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="8a82f-111">Lisätietoja tästä yleiskatsauksesta esitetään kohdassa [Nimike, missä käytetty](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="8a82f-111">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>

<span data-ttu-id="8a82f-112">Seuraavassa kuvassa on esimerkki **Työtilauksen ostoehdotus** -luettelosivusta.</span><span class="sxs-lookup"><span data-stu-id="8a82f-112">The illustration below shows an example of the **Work order purchase requisition** list page.</span></span>

![Kuva 1](media/08-work-orders.png)


<span data-ttu-id="8a82f-114">**Työtilauksen osto** -luettelosivulla (**Resurssien hallinta** > **Yhteiset** > **Hankinta** > **Työtilauksen osto**), näkyy luettelo työtilauksiin liittyvistä ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="8a82f-114">The **Work order purchase** list page (**Asset management** > **Common** > **Procurement** > **Work order purchase**) shows a list of purchase orders that are related to work orders.</span></span> <span data-ttu-id="8a82f-115">Kun valitset työtilaustehtävän tällä sivulla, voit käyttää **Näytä**-ryhmän painikkeita toimintoruudun **Työtilauksen osto** -välilehdessä suorittaaksesi erilaisia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="8a82f-115">When you select a work order job on this page, you can use the buttons in the **Show** group on the **Work order purchase** tab of the Action Pane to perform various actions:</span></span>

- <span data-ttu-id="8a82f-116">Avaa liittyvä ostotilaus valitsemalla **Ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-116">To open the related purchase order, select **Purchase order**.</span></span> 
- <span data-ttu-id="8a82f-117">Avaa liittyvä työtilaus valitsemalla **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-117">To open the related work order, select **Work order**.</span></span>
- <span data-ttu-id="8a82f-118">Saat yleiskatsauksen siitä, miten valitulla rivillä olevaa nimikettä käytetään resurssienhallinnassa suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-118">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="8a82f-119">Lisätietoja tästä yleiskatsauksesta esitetään kohdassa [Nimike, missä käytetty](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="8a82f-119">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>

<span data-ttu-id="8a82f-120">Seuraavassa kuvassa on esimerkki **Työtilauksen osto** -luettelosivusta.</span><span class="sxs-lookup"><span data-stu-id="8a82f-120">The illustration below shows an example of the **Work order purchase** list page.</span></span>

![Kuva 2](media/09-work-orders.png)


<span data-ttu-id="8a82f-122">Sekä luettelosivulla **Työtilauksen osto** että luettelosivulla **Työtilauksen ostoehdotus** kunkin rivin oikealla puolella näkyy symboli, joka liittyy toimituspäivämäärän seurantaan.</span><span class="sxs-lookup"><span data-stu-id="8a82f-122">On both the **Work order purchase** list page and the **Work order purchase requisition** list page, a symbol that is related to delivery date control appears on the right side of each line.</span></span> <span data-ttu-id="8a82f-123">Jos symboli on huutomerkki punaisessa ympyrässä, siihen liittyvän ostotilauksen tai ostoehdotuksen toimitus voi viivästyä.</span><span class="sxs-lookup"><span data-stu-id="8a82f-123">If the symbol is an exclamation point in a red circle, delivery of the related purchase order or purchase requisition might be delayed.</span></span>

<span data-ttu-id="8a82f-124">Ostotilauksen osalta ostotilaukseen liittyvää päivämäärää käytetään mahdollisen viivästyksen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="8a82f-124">For a purchase order, the date that is related to the purchase order line is used to calculate a possible delay.</span></span> <span data-ttu-id="8a82f-125">Voit tarkastella tätä päivämäärää valitsemalla ostotilausrivi **Ostotilaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8a82f-125">To view this date, on the **Purchase order** page, select the purchase order line.</span></span> <span data-ttu-id="8a82f-126">Päivämäärä näkyy **Rivitiedot**-pikavälilehden **Asetukset**-välilehden **Vahvistettu toimituspäivämäärä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8a82f-126">The date is shown in the **Confirmed delivery date** field on the **Setup** tab of the **Line details** FastTab.</span></span> <span data-ttu-id="8a82f-127">Jos **Vahvistettu toimituspäivämäärä**-kenttää ei ole määritetty, laskemiseen käytetään **Ostotilauksen otsikko** -pikavälilehden **Toimituspäivämäärä**-kentän päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="8a82f-127">If the **Confirmed delivery date** field isn't set, the date in the **Delivery date** field on the **Purchase order header** FastTab is used for the calculation.</span></span> <span data-ttu-id="8a82f-128">Yhtä näistä päivistä verrataan työtilauksen tai työtilauksen työn käytettävissä olevaan päivään seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="8a82f-128">One of those dates is compared to the available date on the work order or work order job, in the following order:</span></span>

1. <span data-ttu-id="8a82f-129">Työtilauksen todellinen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="8a82f-129">Actual start date on the work order</span></span>  

2. <span data-ttu-id="8a82f-130">Liittyvän työtilauksen työn ajoitettu alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="8a82f-130">Scheduled start date on the related work order job</span></span> 

3. <span data-ttu-id="8a82f-131">Työtilauksen ajoitettu alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="8a82f-131">Scheduled start date on the work order</span></span> 

4. <span data-ttu-id="8a82f-132">Työtilauksen odotettu alkamispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="8a82f-132">Expected start date on the work order</span></span> 

<span data-ttu-id="8a82f-133">Kaikissa ostoehdotuksessa mahdollisen viivästyksen laskemiseen käytetään **Ostoehdotukset**-sivun **Ostoehdotuksen otsikko** -pikavälilehden **Pyydetty päivämäärä** -kentän päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="8a82f-133">For a purchase requisition, the date in the **Requested date** field on the **Purchase requisition header** FastTab of the **Purchase requisitions** page is used to calculate a possible delay.</span></span> <span data-ttu-id="8a82f-134">Tätä päivää verrataan työtilauksen tai työtilaustehtävän käytettävissä olevaan päivään samassa järjestyksessä kuin ostotilauksen osalta.</span><span class="sxs-lookup"><span data-stu-id="8a82f-134">The date in that field is compared to the available date on the work order or work order job, in the same order that is used for a purchase order.</span></span>


## <a name="create-a-purchase-order-from-a-work-order"></a><span data-ttu-id="8a82f-135">Ostotilauksen luominen työtilauksesta</span><span class="sxs-lookup"><span data-stu-id="8a82f-135">Create a purchase order from a work order</span></span>

<span data-ttu-id="8a82f-136">**Kaikki työtilaukset** -luettelosivulla voit valita työtilaustehtävän ja sitten luoda siihen liittyvän ostotilauksen tai ostoehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="8a82f-136">On the **All work orders** list page, you can select a work order job, and then create a related purchase order or a related purchase requisition.</span></span> <span data-ttu-id="8a82f-137">Näin autat varmistamaan, että ostotilauksen tai ostoehdotuksen ja työtilauksen välillä on projektisuhteita.</span><span class="sxs-lookup"><span data-stu-id="8a82f-137">In this way, you help guarantee that project relations exist between the purchase order or purchase requisition and the work order.</span></span>

1. <span data-ttu-id="8a82f-138">Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-138">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8a82f-139">Valitse työtilaus, jolle tehdään ostotilaus, ja sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-139">Select the work order to create a purchase order for, and then select **Edit**.</span></span>

3. <span data-ttu-id="8a82f-140">Valitse **Työtilauksen ylläpitotyöt** -pikavälilehdessä työtilaustehtävä, jolle haluat luoda ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="8a82f-140">On the **Work order maintenance jobs** FastTab, select the work order job to create the purchase order for.</span></span>

4. <span data-ttu-id="8a82f-141">Valitse **Nimiketehtävät** > **Ostotilaus työtilaustehtävästä**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-141">Select **Item tasks** > **Purchase order from work order job**.</span></span>

5. <span data-ttu-id="8a82f-142">Valitse **Projektin ostotilaukset** -luettelosivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-142">On the **Project purchase orders** list page, click **New**.</span></span>

6. <span data-ttu-id="8a82f-143">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="8a82f-143">Create the purchase order.</span></span>

>[!NOTE]
><span data-ttu-id="8a82f-144">Samalla tavalla voit luoda myös liittyvän ostoehdotuksen.</span><span class="sxs-lookup"><span data-stu-id="8a82f-144">To create a related purchase requisition, follow the same steps.</span></span> <span data-ttu-id="8a82f-145">Valitse vaiheessa 4 kuitenkin **Nimiketehtävät** > **Ostoehdotus työtilaustehtävästä**.</span><span class="sxs-lookup"><span data-stu-id="8a82f-145">However, select **Item tasks** > **Purchase requisition from work order job** in step 4.</span></span>


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a><span data-ttu-id="8a82f-146">Työtilauksen ja ostotilauksen tai ostoehdotuksen välinen projektisuhde</span><span class="sxs-lookup"><span data-stu-id="8a82f-146">Project relation between work order and purchase order or purchase requisition</span></span>

<span data-ttu-id="8a82f-147">Ostotilausrivi tai ostoehdotusrivi liittyy työtilaustyöhön työtilausprojektin ja siihen liittyvän projektitehtävän numeron kautta.</span><span class="sxs-lookup"><span data-stu-id="8a82f-147">A purchase order line or purchase requisition line is related to a work order job via the work order project and the related project activity number.</span></span> <span data-ttu-id="8a82f-148">Kun luot työtilaustyöstä ostotilauksen tai ostoehdotuksen, siihen liittyvä projektitehtävän numero on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="8a82f-148">When you create a purchase order or purchase requisition from a work order job, the related project activity number is mandatory.</span></span> <span data-ttu-id="8a82f-149">Projektitehtävän numero lisätään automaattisesti ostotilaukseen tai ostoehdotukseen, jos siihen liittyvä työtilaus sisältää työtilaustehtäviä, jotka kaikki käyttävät samaa ylläpitotyön tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="8a82f-149">If all the work order jobs in the related work order have the same maintenance job type, the project activity number is automatically entered on the purchase order or purchase requisition.</span></span> <span data-ttu-id="8a82f-150">Jos työtilaustehtävillä on erilaisia ylläpitotehtävien tyyppejä, projektitehtävän numero on lisättävä ostotilaukseen tai ostoehdotukseen manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="8a82f-150">If the work order jobs have different maintenance job types, you must manually enter the project activity number on the purchase order or purchase requisition.</span></span>

<span data-ttu-id="8a82f-151">Voit tarkastella ostotilausriviin liittyvää tehtävänumeroa tai syöttää sen valitsemalla **Työtilauksen osto** -luettelosivulla ostotilauksen tietueen ja sitten **Ostotilaus**-sarakkeessa ostotilauksen linkin.</span><span class="sxs-lookup"><span data-stu-id="8a82f-151">To view or enter the activity number that is related to a purchase order line, on the **Work order purchase** list page, select the purchase order record, and then, in the **Purchase order** column, select the link for the purchase order.</span></span> <span data-ttu-id="8a82f-152">**Tehtävänumero**-kenttä löytyy **Rivitiedot**-pikavälilehden **Projekti**-välilehdeltä.</span><span class="sxs-lookup"><span data-stu-id="8a82f-152">You can find the **Activity number** field on the **Project** tab of the **Line details** FastTab.</span></span>

<span data-ttu-id="8a82f-153">Alla olevassa kuvassa näkyy esimerkki **Ostotilaus**-sivusta, jossa **Tehtävänumero** on korostettuna.</span><span class="sxs-lookup"><span data-stu-id="8a82f-153">The illustration below shows an example of the **Purchase order** page, with focus on the **Activity number**.</span></span>

![Kuva 3](media/10-work-orders.png)

<span data-ttu-id="8a82f-155">Samoin voit tarkastella työtilauksen ostoehdotusriviin liittyvää tehtävänumeroa tai syöttää sen valitsemalla **Työtilauksen ostoehdotus** -luettelosivulla ostoehdotuksen tietueen ja sitten **Ostoehdotus**-sarakkeessa ostoehdotuksen linkin.</span><span class="sxs-lookup"><span data-stu-id="8a82f-155">Likewise, to view or enter the activity number that is related to a work order purchase requisition line, on the **Work order purchase requisition** list page, select the purchase requisition record, and then, in the **Purchase requisition** column, select the link for the purchase requisition.</span></span> <span data-ttu-id="8a82f-156">**Tehtävänumero**-kenttä löytyy **Rivitiedot**-pikavälilehden **Projekti**-välilehdeltä.</span><span class="sxs-lookup"><span data-stu-id="8a82f-156">You can find the **Activity number** field on the **Project** tab of the **Line details** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]