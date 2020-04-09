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
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140781"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="4277c-103">Online-myynti- ja maksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="4277c-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4277c-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="4277c-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="4277c-105">Online-myynnin ja maksujen kirjaaminen on kaksivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="4277c-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="4277c-106">Online-kaupan tapahtumatietojen vetäminen pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="4277c-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="4277c-107">Synkronoidaan tilauksia, jotta myyntitilaukset luodaan pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="4277c-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="4277c-108">Online-myynnin tapahtumatietojen vetäminen onnistuu joko suorittamalla P-työ manuaalisesti tai luomalla toistuva erätyö.</span><span class="sxs-lookup"><span data-stu-id="4277c-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="4277c-109">P-työn manuaalinen suoritus</span><span class="sxs-lookup"><span data-stu-id="4277c-109">Manually running the P-job</span></span>

1. <span data-ttu-id="4277c-110">Valitse Kaikki työtilat > Retail ja Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="4277c-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4277c-111">Valitse Jakeluaikataulu.</span><span class="sxs-lookup"><span data-stu-id="4277c-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4277c-112">Valitse P-0001.</span><span class="sxs-lookup"><span data-stu-id="4277c-112">Select P-0001.</span></span>
4. <span data-ttu-id="4277c-113">Säädä kanavan tietokantaryhmiä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4277c-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="4277c-114">Valitse Suorita nyt.</span><span class="sxs-lookup"><span data-stu-id="4277c-114">Click Run now.</span></span>
6. <span data-ttu-id="4277c-115">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4277c-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="4277c-116">Toistuvan P-työn ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="4277c-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="4277c-117">Valitse Kaikki työtilat > Retail ja Commerce IT.</span><span class="sxs-lookup"><span data-stu-id="4277c-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4277c-118">Valitse Jakeluaikataulu.</span><span class="sxs-lookup"><span data-stu-id="4277c-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4277c-119">Valitse P-0001.</span><span class="sxs-lookup"><span data-stu-id="4277c-119">Select P-0001.</span></span>
4. <span data-ttu-id="4277c-120">Valitse Luo erätyö.</span><span class="sxs-lookup"><span data-stu-id="4277c-120">Click Create batch job.</span></span>
5. <span data-ttu-id="4277c-121">valitse Suorita taustalla.</span><span class="sxs-lookup"><span data-stu-id="4277c-121">Click Run in the background.</span></span>
5. <span data-ttu-id="4277c-122">Ota käyttöön Eräkäsittely.</span><span class="sxs-lookup"><span data-stu-id="4277c-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="4277c-123">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="4277c-123">Click Recurrence..</span></span>
7. <span data-ttu-id="4277c-124">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="4277c-124">Select the No end date option.</span></span>
8. <span data-ttu-id="4277c-125">Syötä Määrä-kenttään ajojen aikaväli minuutteina.</span><span class="sxs-lookup"><span data-stu-id="4277c-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4277c-126">Yleensä tämä olisi 5-10.</span><span class="sxs-lookup"><span data-stu-id="4277c-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="4277c-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4277c-127">Click OK.</span></span>
10. <span data-ttu-id="4277c-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4277c-128">Click OK.</span></span>

<span data-ttu-id="4277c-129">Tilaukset voidaan synkronoida joko manuaalisesti suorittamalla Synkronoi tilaukset -työ tai luomalla toistuva erätyö.</span><span class="sxs-lookup"><span data-stu-id="4277c-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="4277c-130">Tilauksen synkronoinnin suorittaminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="4277c-130">Manually running order synchronization</span></span> 

<span data-ttu-id="4277c-131">Suorittamalla seuraavat vaiheet voit suorittaa "Synkronoi tilaukset" -työn manuaalisesti kerran.</span><span class="sxs-lookup"><span data-stu-id="4277c-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="4277c-132">Siirry kohtaan Kaikki työtilat > Myymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="4277c-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4277c-133">Valitse Synkronoi tilaukset.</span><span class="sxs-lookup"><span data-stu-id="4277c-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4277c-134">Valitse Organisaatiohierarkia-kentässä Myymälät alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="4277c-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4277c-135">Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="4277c-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4277c-136">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="4277c-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4277c-137">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4277c-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4277c-138">Ota pois käytöstä Eräkäsittely.</span><span class="sxs-lookup"><span data-stu-id="4277c-138">Disable Batch processing</span></span>
6. <span data-ttu-id="4277c-139">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="4277c-139">Click Recurrence.</span></span>
7. <span data-ttu-id="4277c-140">Valitse Päättyy jälkeen -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4277c-140">Select End After option</span></span>
8. <span data-ttu-id="4277c-141">Kirjoita Päättyy jälkeen -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="4277c-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="4277c-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4277c-142">Click OK.</span></span>
10. <span data-ttu-id="4277c-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4277c-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="4277c-144">Toistuvien tilausten synkronointien ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="4277c-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="4277c-145">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="4277c-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="4277c-146">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="4277c-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4277c-147">Siirry kohtaan Kaikki työtilat > Myymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="4277c-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4277c-148">Valitse Synkronoi tilaukset.</span><span class="sxs-lookup"><span data-stu-id="4277c-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4277c-149">Valitse Organisaatiohierarkia-kentässä Myymälät alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="4277c-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4277c-150">Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="4277c-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4277c-151">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="4277c-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4277c-152">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4277c-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4277c-153">Ota käyttöön Eräkäsittely</span><span class="sxs-lookup"><span data-stu-id="4277c-153">Enable Batch processing</span></span>
6. <span data-ttu-id="4277c-154">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="4277c-154">Click Recurrence.</span></span>
7. <span data-ttu-id="4277c-155">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="4277c-155">Select the No end date option.</span></span>
8. <span data-ttu-id="4277c-156">Syötä Määrä-kenttään ajojen aikaväli minuutteina.</span><span class="sxs-lookup"><span data-stu-id="4277c-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4277c-157">Yleensä tämä olisi 2-20</span><span class="sxs-lookup"><span data-stu-id="4277c-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="4277c-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4277c-158">Click OK.</span></span>
10. <span data-ttu-id="4277c-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4277c-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="4277c-160">Prosessiin liittyvät tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="4277c-160">Data entities involved in the process</span></span>

- <span data-ttu-id="4277c-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="4277c-161">RetailTransactionTable</span></span>
- <span data-ttu-id="4277c-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="4277c-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="4277c-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="4277c-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="4277c-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="4277c-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="4277c-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="4277c-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="4277c-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="4277c-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="4277c-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="4277c-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="4277c-171">RetailTransactionAttributeTrans</span></span>
