---
title: Määrää ei voi vähentää, kun myyntitilaus peruutetaan
description: Määrää ei voi vähentää, kun myyntitilaus peruutetaan.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230833"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="cffb5-103">Määrää ei voi vähentää, kun myyntitilaus peruutetaan</span><span class="sxs-lookup"><span data-stu-id="cffb5-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="cffb5-104">Virhekoodi: SYS138831</span><span class="sxs-lookup"><span data-stu-id="cffb5-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="cffb5-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="cffb5-105">Symptoms</span></span>

<span data-ttu-id="cffb5-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="cffb5-106">The system shows the following error message:</span></span>

> <span data-ttu-id="cffb5-107">Määrää ei voi vähentää.</span><span class="sxs-lookup"><span data-stu-id="cffb5-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="cffb5-108">Tilauksen varastotapahtumien määrä on liian pieni, koska määrään tai sen osaan viitataan toimitustilauksessa tai tuotantotilauksessa tai se on merkitty muihin tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="cffb5-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="cffb5-109">Syy</span><span class="sxs-lookup"><span data-stu-id="cffb5-109">Cause</span></span>

<span data-ttu-id="cffb5-110">Jos myyntitilaukseen liittyy työtä, et voi peruuttaa myyntitilausta, ennen kuin työ peruutetaan ja palautetaan.</span><span class="sxs-lookup"><span data-stu-id="cffb5-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="cffb5-111">Tämä vaatimus on pätee, vaikka myyntitilaukseen liittyvä työ olisi suljettu.</span><span class="sxs-lookup"><span data-stu-id="cffb5-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="cffb5-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="cffb5-112">Resolution</span></span>

<span data-ttu-id="cffb5-113">Voit korjata ongelman tekemällä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="cffb5-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="cffb5-114">Peruuta avoimet työt.</span><span class="sxs-lookup"><span data-stu-id="cffb5-114">Cancel open work.</span></span>
1. <span data-ttu-id="cffb5-115">Poista kuorma.</span><span class="sxs-lookup"><span data-stu-id="cffb5-115">Delete the load.</span></span>
1. <span data-ttu-id="cffb5-116">Vähennä kerättyä määrää.</span><span class="sxs-lookup"><span data-stu-id="cffb5-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="cffb5-117">Peruuta avoimet työt</span><span class="sxs-lookup"><span data-stu-id="cffb5-117">Cancel open work</span></span>

<span data-ttu-id="cffb5-118">Voit peruuttaa avoimet työt seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="cffb5-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="cffb5-119">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="cffb5-120">Määritä **Työtunnus**-kentässä peruutettavan työn tunnus ja jonka **Työn tila** -arvona on *Avoinna*, *Käsittelyssä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.</span><span class="sxs-lookup"><span data-stu-id="cffb5-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="cffb5-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-121">Select **OK**.</span></span>
1. <span data-ttu-id="cffb5-122">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="cffb5-123">Poista kuorma</span><span class="sxs-lookup"><span data-stu-id="cffb5-123">Delete the load</span></span>

<span data-ttu-id="cffb5-124">Voit poistaa kuorman seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="cffb5-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="cffb5-125">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="cffb5-126">Avaa asianmukainen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="cffb5-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="cffb5-127">Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Työn tiedot**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="cffb5-128">Valitse **Työ**-sivun toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="cffb5-129">Vahvista, että **Työn tila** -kentän arvoksi on määritetty *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="cffb5-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="cffb5-130">Sulje **Työ**-sivu.</span><span class="sxs-lookup"><span data-stu-id="cffb5-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="cffb5-131">Valitse myyntitilauksen tietosivun **Myyntitilausrivit**-pikavälilehdestä **Varasto \> Kuorman tiedot**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="cffb5-132">Valitse toimintoruudussa **Poista**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="cffb5-133">Vahvista, että haluat poistaa kuorman valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="cffb5-134">Sulje **Kuorma**-sivu.</span><span class="sxs-lookup"><span data-stu-id="cffb5-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="cffb5-135">Vähennä kerättyä määrää</span><span class="sxs-lookup"><span data-stu-id="cffb5-135">Reduce the picked quantity</span></span>

<span data-ttu-id="cffb5-136">Kun kaikki työt on peruutettu, pienennä keräysmäärää noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="cffb5-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="cffb5-137">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="cffb5-138">Avaa asianmukainen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="cffb5-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="cffb5-139">Valitse **Myyntitilausrivit**-pikavälilehdessä **Päivitä rivi \> Kerää** työkaluriviltä.</span><span class="sxs-lookup"><span data-stu-id="cffb5-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="cffb5-140">Valitse **Kerää**-sivun **Tapahtumat**-osasta rivi, jonka **Varasto-ottotila**-kentän arvoksi on määritetty *Kerätty*.</span><span class="sxs-lookup"><span data-stu-id="cffb5-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="cffb5-141">Valitse **Tapahtumat**-osassa **Lisää keräilyrivi** työkaluriviltä.</span><span class="sxs-lookup"><span data-stu-id="cffb5-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="cffb5-142">Valitse **Keräilyrivit**-osassa **Vahvista kaikkien keräily** työkaluriviltä.</span><span class="sxs-lookup"><span data-stu-id="cffb5-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="cffb5-143">Sulje **Kerää**-sivu.</span><span class="sxs-lookup"><span data-stu-id="cffb5-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="cffb5-144">Valitse myyntitilauksen tietosivun toimintoruudun **Myyntitilaus**-välilehden **Ylläpidä**-ryhmässä **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="cffb5-145">Vahvista, että haluat peruuttaa myyntitilauksen valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="cffb5-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
