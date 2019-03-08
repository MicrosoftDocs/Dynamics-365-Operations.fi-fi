---
title: Luo myyntitilauksen laskut
description: Tässä tehtävän ohjauksessa kuvataan myyntitilauksen laskuttaminen sekä laskujen yhdistäminen ja eräkäsittely.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "353307"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="e733b-103">Luo myyntitilauksen laskut</span><span class="sxs-lookup"><span data-stu-id="e733b-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e733b-104">Tässä tehtävän ohjauksessa kuvataan myyntitilauksen laskuttaminen sekä laskujen yhdistäminen ja eräkäsittely.</span><span class="sxs-lookup"><span data-stu-id="e733b-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="e733b-105">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="e733b-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="e733b-106">Laskun luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="e733b-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="e733b-107">Valitse Myyntireskontra > Tilaukset > Myyntitilaukset, jotka on lähetetty mutta joita ei ole laskutettu.</span><span class="sxs-lookup"><span data-stu-id="e733b-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="e733b-108">Valitse myyntitilaus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e733b-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="e733b-109">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="e733b-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e733b-110">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="e733b-110">Click Invoice.</span></span>
    * <span data-ttu-id="e733b-111">Ota huomioon, että tälle myyntitilaukselle on liitetty useita pakkausluetteloita.</span><span class="sxs-lookup"><span data-stu-id="e733b-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="e733b-112">Näkyvissä on vain sana <multiple> pakkausluetteloiden numeroiden sijaan.</span><span class="sxs-lookup"><span data-stu-id="e733b-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="e733b-113">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="e733b-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="e733b-114">Kirjauksen arvoksi on annettava Kyllä, jotta lasku kirjataan.</span><span class="sxs-lookup"><span data-stu-id="e733b-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="e733b-115">Voit myös ottaa kirjauksen pois päältä ja vain tulostaa laskun.</span><span class="sxs-lookup"><span data-stu-id="e733b-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="e733b-116">Saat kuitenkin saman tuloksen, kun luot proformalaskun laskun sijaan.</span><span class="sxs-lookup"><span data-stu-id="e733b-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="e733b-117">Tätä vaihtoehtoa käytetään komentojonotöissä.</span><span class="sxs-lookup"><span data-stu-id="e733b-117">This option is used for batch jobs.</span></span> <span data-ttu-id="e733b-118">Kysely suoritetaan, kun komentojonotyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="e733b-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="e733b-119">Valitse Tulosta-kentässä Jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e733b-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="e733b-120">Valitse Tulosta lasku -kohdassa Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e733b-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="e733b-121">Tulostuksenhallinnan avulla voit tulostaa laskusta useita kopioita ja myös lähettää laskun sähköpostitse PDF-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="e733b-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="e733b-122">Valitse Tulosta kulut -kentässä Tee yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="e733b-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="e733b-123">Valitse Tarkista luottoraja -kentässä Saldo.</span><span class="sxs-lookup"><span data-stu-id="e733b-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="e733b-124">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="e733b-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="e733b-125">Tilausten yhdistäminen yhdeksi laskuksi</span><span class="sxs-lookup"><span data-stu-id="e733b-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="e733b-126">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="e733b-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e733b-127">Etsi asiakas, jolla on useita avoimia laskuja.</span><span class="sxs-lookup"><span data-stu-id="e733b-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="e733b-128">Valitse avoin myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e733b-128">Select an open sales order.</span></span>
4. <span data-ttu-id="e733b-129">Valitse samalta asiakkaalta toinen avoin myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e733b-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="e733b-130">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="e733b-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="e733b-131">Valitse lasku.</span><span class="sxs-lookup"><span data-stu-id="e733b-131">Click Invoice.</span></span>
7. <span data-ttu-id="e733b-132">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="e733b-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="e733b-133">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="e733b-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="e733b-134">Ota huomioon, että yhteenveto-osassa näkyy kaksi laskua.</span><span class="sxs-lookup"><span data-stu-id="e733b-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="e733b-135">Yhdistetään laskut yhdeksi laskuksi.</span><span class="sxs-lookup"><span data-stu-id="e733b-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="e733b-136">Valitse Yhteenvedon päivitys -kentässä Laskutustili.</span><span class="sxs-lookup"><span data-stu-id="e733b-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="e733b-137">Valitse Järjestä, kun haluat yhdistää myyntitilaukset yhdeksi laskuksi.</span><span class="sxs-lookup"><span data-stu-id="e733b-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="e733b-138">Kaksi myyntitilausta on nyt yhdistetty yhdeksi laskuksi.</span><span class="sxs-lookup"><span data-stu-id="e733b-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="e733b-139">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="e733b-139">Click Cancel.</span></span>
12. <span data-ttu-id="e733b-140">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e733b-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="e733b-141">Laskujen kirjaaminen eränä</span><span class="sxs-lookup"><span data-stu-id="e733b-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="e733b-142">Valitse Myyntireskontra > Laskut > Erän laskutus > Lasku.</span><span class="sxs-lookup"><span data-stu-id="e733b-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="e733b-143">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="e733b-143">Click Select.</span></span>
3. <span data-ttu-id="e733b-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e733b-144">Click OK.</span></span>
4. <span data-ttu-id="e733b-145">Valitse erä.</span><span class="sxs-lookup"><span data-stu-id="e733b-145">Click Batch.</span></span>
5. <span data-ttu-id="e733b-146">Valitse Kyllä, jos haluat ottaa eräkäsittelyn käyttöön</span><span class="sxs-lookup"><span data-stu-id="e733b-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="e733b-147">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="e733b-147">Click Recurrence.</span></span>
7. <span data-ttu-id="e733b-148">Valitse Päivät</span><span class="sxs-lookup"><span data-stu-id="e733b-148">Select Days</span></span>
8. <span data-ttu-id="e733b-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e733b-149">Click OK.</span></span>
9. <span data-ttu-id="e733b-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e733b-150">Click OK.</span></span>
10. <span data-ttu-id="e733b-151">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="e733b-151">Click Cancel.</span></span>
11. <span data-ttu-id="e733b-152">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e733b-152">Click Yes.</span></span>

