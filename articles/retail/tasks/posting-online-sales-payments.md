---
title: Online-myynti- ja maksujen kirjaaminen
description: Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864150"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="551c2-103">Online-myynti- ja maksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="551c2-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="551c2-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="551c2-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="551c2-105">Online-myynnin ja maksujen kirjaaminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="551c2-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="551c2-106">Online-vähittäiskaupan tapahtumatietojen vetäminen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="551c2-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="551c2-107">Synkronoidaan tilauksia, jotta myyntitilaukset luodaan pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="551c2-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="551c2-108">Online-vähittäismyynnin tapahtumatietojen vetäminen onnistuu joko suorittamalla P-työ manuaalisesti tai luomalla toistuva erätyö.</span><span class="sxs-lookup"><span data-stu-id="551c2-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="551c2-109">P-työn manuaalinen suoritus</span><span class="sxs-lookup"><span data-stu-id="551c2-109">Manually running the P-job</span></span>

1. <span data-ttu-id="551c2-110">Siirry kohtaan Kaikki työtilat > Vähittäismyynnin IT.</span><span class="sxs-lookup"><span data-stu-id="551c2-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="551c2-111">Valitse Jakeluaikataulu.</span><span class="sxs-lookup"><span data-stu-id="551c2-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="551c2-112">Valitse P-0001.</span><span class="sxs-lookup"><span data-stu-id="551c2-112">Select P-0001.</span></span>
4. <span data-ttu-id="551c2-113">Säädä kanavan tietokantaryhmiä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="551c2-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="551c2-114">Valitse Suorita nyt.</span><span class="sxs-lookup"><span data-stu-id="551c2-114">Click Run now.</span></span>
6. <span data-ttu-id="551c2-115">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="551c2-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="551c2-116">Toistuvan P-työn ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="551c2-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="551c2-117">Siirry kohtaan Kaikki työtilat > Vähittäismyynnin IT.</span><span class="sxs-lookup"><span data-stu-id="551c2-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="551c2-118">Valitse Jakeluaikataulu.</span><span class="sxs-lookup"><span data-stu-id="551c2-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="551c2-119">Valitse P-0001.</span><span class="sxs-lookup"><span data-stu-id="551c2-119">Select P-0001.</span></span>
4. <span data-ttu-id="551c2-120">Valitse Luo erätyö.</span><span class="sxs-lookup"><span data-stu-id="551c2-120">Click Create batch job.</span></span>
5. <span data-ttu-id="551c2-121">valitse Suorita taustalla.</span><span class="sxs-lookup"><span data-stu-id="551c2-121">Click Run in the background.</span></span>
5. <span data-ttu-id="551c2-122">Ota käyttöön Eräkäsittely.</span><span class="sxs-lookup"><span data-stu-id="551c2-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="551c2-123">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="551c2-123">Click Recurrence..</span></span>
7. <span data-ttu-id="551c2-124">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="551c2-124">Select the No end date option.</span></span>
8. <span data-ttu-id="551c2-125">Syötä Määrä-kenttään ajojen aikaväli minuutteina.</span><span class="sxs-lookup"><span data-stu-id="551c2-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="551c2-126">Yleensä tämä olisi 5-10.</span><span class="sxs-lookup"><span data-stu-id="551c2-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="551c2-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="551c2-127">Click OK.</span></span>
10. <span data-ttu-id="551c2-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="551c2-128">Click OK.</span></span>

<span data-ttu-id="551c2-129">Tilaukset voidaan synkronoida joko manuaalisesti suorittamalla Synkronoi tilaukset -työ tai luomalla toistuva erätyö.</span><span class="sxs-lookup"><span data-stu-id="551c2-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="551c2-130">Tilauksen synkronoinnin suorittaminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="551c2-130">Manually running order synchronization</span></span> 

<span data-ttu-id="551c2-131">Suorittamalla seuraavat vaiheet voit suorittaa "Synkronoi tilaukset" -työn manuaalisesti kerran.</span><span class="sxs-lookup"><span data-stu-id="551c2-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="551c2-132">Siirry kohtaan Kaikki työtilat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="551c2-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="551c2-133">Valitse Synkronoi tilaukset.</span><span class="sxs-lookup"><span data-stu-id="551c2-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="551c2-134">Valitse Organisaatiohierarkia-kentässä Vähittäismyymälät alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="551c2-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="551c2-135">Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="551c2-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="551c2-136">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="551c2-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="551c2-137">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="551c2-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="551c2-138">Ota pois käytöstä Eräkäsittely.</span><span class="sxs-lookup"><span data-stu-id="551c2-138">Disable Batch processing</span></span>
6. <span data-ttu-id="551c2-139">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="551c2-139">Click Recurrence.</span></span>
7. <span data-ttu-id="551c2-140">Valitse Päättyy jälkeen -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="551c2-140">Select End After option</span></span>
8. <span data-ttu-id="551c2-141">Kirjoita Päättyy jälkeen -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="551c2-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="551c2-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="551c2-142">Click OK.</span></span>
10. <span data-ttu-id="551c2-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="551c2-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="551c2-144">Toistuvien tilausten synkronointien ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="551c2-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="551c2-145">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="551c2-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="551c2-146">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="551c2-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="551c2-147">Siirry kohtaan Kaikki työtilat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="551c2-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="551c2-148">Valitse Synkronoi tilaukset.</span><span class="sxs-lookup"><span data-stu-id="551c2-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="551c2-149">Valitse Organisaatiohierarkia-kentässä Vähittäismyymälät alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="551c2-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="551c2-150">Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="551c2-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="551c2-151">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="551c2-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="551c2-152">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="551c2-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="551c2-153">Ota käyttöön Eräkäsittely</span><span class="sxs-lookup"><span data-stu-id="551c2-153">Enable Batch processing</span></span>
6. <span data-ttu-id="551c2-154">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="551c2-154">Click Recurrence.</span></span>
7. <span data-ttu-id="551c2-155">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="551c2-155">Select the No end date option.</span></span>
8. <span data-ttu-id="551c2-156">Syötä Määrä-kenttään ajojen aikaväli minuutteina.</span><span class="sxs-lookup"><span data-stu-id="551c2-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="551c2-157">Yleensä tämä olisi 2-20</span><span class="sxs-lookup"><span data-stu-id="551c2-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="551c2-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="551c2-158">Click OK.</span></span>
10. <span data-ttu-id="551c2-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="551c2-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="551c2-160">Prosessiin liittyvät tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="551c2-160">Data entities involved in the process</span></span>

- <span data-ttu-id="551c2-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="551c2-161">RetailTransactionTable</span></span>
- <span data-ttu-id="551c2-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="551c2-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="551c2-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="551c2-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="551c2-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="551c2-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="551c2-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="551c2-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="551c2-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="551c2-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="551c2-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="551c2-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="551c2-171">RetailTransactionAttributeTrans</span></span>
