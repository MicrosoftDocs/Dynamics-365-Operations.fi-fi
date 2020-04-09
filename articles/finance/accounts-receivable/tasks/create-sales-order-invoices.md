---
title: Luo myyntitilauksen laskut
description: Tässä tehtävän ohjauksessa kuvataan myyntitilauksen laskuttaminen sekä laskujen yhdistäminen ja eräkäsittely.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c504ef36f61613c7aa7db5a1e5ddba6e69cd7285
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140263"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="3212e-103">Luo myyntitilauksen laskut</span><span class="sxs-lookup"><span data-stu-id="3212e-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3212e-104">Tässä tehtävän ohjauksessa kuvataan myyntitilauksen laskuttaminen sekä laskujen yhdistäminen ja eräkäsittely.</span><span class="sxs-lookup"><span data-stu-id="3212e-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="3212e-105">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="3212e-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="3212e-106">Laskun luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="3212e-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="3212e-107">Valitse **Siirtymisruutu > Moduulit > Myyntireskontra > Tilaukset > Myyntitilaukset, jotka on lähetetty mutta joita ei ole laskutettu.**</span><span class="sxs-lookup"><span data-stu-id="3212e-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="3212e-108">Valitse myyntitilaus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="3212e-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="3212e-109">Valitse **toimintoruudussa** **Lasku > Luo > Lasku**.</span><span class="sxs-lookup"><span data-stu-id="3212e-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="3212e-110">Ota huomioon, että tälle myyntitilaukselle on liitetty useita pakkausluetteloita.</span><span class="sxs-lookup"><span data-stu-id="3212e-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="3212e-111">Näkyvissä on vain sana <multiple> pakkausluetteloiden numeroiden sijaan.</span><span class="sxs-lookup"><span data-stu-id="3212e-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="3212e-112">Laajenna **Parametrit**-osa.</span><span class="sxs-lookup"><span data-stu-id="3212e-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="3212e-113">Kirjauksen arvoksi on annettava Kyllä, jotta lasku kirjataan.</span><span class="sxs-lookup"><span data-stu-id="3212e-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="3212e-114">Voit myös ottaa kirjauksen pois päältä ja vain tulostaa laskun.</span><span class="sxs-lookup"><span data-stu-id="3212e-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="3212e-115">Saat kuitenkin saman tuloksen, kun luot proformalaskun laskun sijaan.</span><span class="sxs-lookup"><span data-stu-id="3212e-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="3212e-116">Tätä vaihtoehtoa käytetään komentojonotöissä.</span><span class="sxs-lookup"><span data-stu-id="3212e-116">This option is used for batch jobs.</span></span> <span data-ttu-id="3212e-117">Kysely suoritetaan, kun komentojonotyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="3212e-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="3212e-118">Valitse **Tulosta**-kentässä Jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3212e-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="3212e-119">Valitse **Tulosta lasku** -kohdassa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3212e-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="3212e-120">Tulostuksenhallinnan avulla voit tulostaa laskusta useita kopioita ja myös lähettää laskun sähköpostitse PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="3212e-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="3212e-121">Valitse **Tulosta kulut** -kentässä Tee yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="3212e-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="3212e-122">Valitse **Tarkista luottoraja** -kentässä Saldo.</span><span class="sxs-lookup"><span data-stu-id="3212e-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="3212e-123">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="3212e-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="3212e-124">Tilausten yhdistäminen yhdeksi laskuksi</span><span class="sxs-lookup"><span data-stu-id="3212e-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="3212e-125">Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="3212e-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="3212e-126">Etsi asiakas, jolla on useita avoimia laskuja.</span><span class="sxs-lookup"><span data-stu-id="3212e-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="3212e-127">Valitse useita saman asiakkaan avoimia myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="3212e-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="3212e-128">Valitse **toimintoruudussa** **Lasku > Luo > Lasku**.</span><span class="sxs-lookup"><span data-stu-id="3212e-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="3212e-129">Laajenna **Parametrit**-osa.</span><span class="sxs-lookup"><span data-stu-id="3212e-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="3212e-130">Valitse **Määrä**-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="3212e-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="3212e-131">Ota huomioon, että yhteenveto-osassa näkyy kaksi laskua.</span><span class="sxs-lookup"><span data-stu-id="3212e-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="3212e-132">Yhdistetään laskut yhdeksi laskuksi.</span><span class="sxs-lookup"><span data-stu-id="3212e-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="3212e-133">Valitse **Yhteenvedon päivitys** -kentässä Laskutustili.</span><span class="sxs-lookup"><span data-stu-id="3212e-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="3212e-134">Valitse **Järjestä**, kun haluat yhdistää myyntitilaukset yhdeksi laskuksi.</span><span class="sxs-lookup"><span data-stu-id="3212e-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="3212e-135">Kaksi myyntitilausta on nyt yhdistetty yhdeksi laskuksi.</span><span class="sxs-lookup"><span data-stu-id="3212e-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="3212e-136">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="3212e-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="3212e-137">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3212e-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="3212e-138">Laskujen kirjaaminen eränä</span><span class="sxs-lookup"><span data-stu-id="3212e-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="3212e-139">Valitse **Siirtymisruutu > Moduulit > Myyntireskontra > Laskut > Erälaskutus > Lasku**.</span><span class="sxs-lookup"><span data-stu-id="3212e-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="3212e-140">Klikkaa **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="3212e-140">Click **Select**.</span></span>
3. <span data-ttu-id="3212e-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3212e-141">Click **OK**.</span></span>
4. <span data-ttu-id="3212e-142">Valitse **Erä**.</span><span class="sxs-lookup"><span data-stu-id="3212e-142">Click **Batch**.</span></span>
5. <span data-ttu-id="3212e-143">Valitse **eräkäsittelyn** arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3212e-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="3212e-144">Valitse **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="3212e-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="3212e-145">Valitse **Päivät**,</span><span class="sxs-lookup"><span data-stu-id="3212e-145">Select **Days**.</span></span>
8. <span data-ttu-id="3212e-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3212e-146">Click **OK**.</span></span>
9. <span data-ttu-id="3212e-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3212e-147">Click **OK**.</span></span>
10. <span data-ttu-id="3212e-148">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="3212e-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="3212e-149">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3212e-149">Click **Yes**.</span></span>

