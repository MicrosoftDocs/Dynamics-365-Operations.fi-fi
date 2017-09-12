--- 
title: "Koron käsittely"
description: "Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="process-interest"></a><span data-ttu-id="ac131-103">Koron käsittely</span><span class="sxs-lookup"><span data-stu-id="ac131-103">Process interest</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac131-104">Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ac131-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="ac131-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="ac131-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="ac131-106">Määritä kirjausprofiilin korko.</span><span class="sxs-lookup"><span data-stu-id="ac131-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="ac131-107">Siirry kohtaan Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="ac131-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="ac131-108">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="ac131-108">Click Edit.</span></span>
    * <span data-ttu-id="ac131-109">Valitse korkokoodi avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="ac131-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="ac131-110">Jos et halua laskea korkoa tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="ac131-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="ac131-111">Taulurajoitus-välilehden avulla voit muuttaa tapaa, jolla korko käsitellään.</span><span class="sxs-lookup"><span data-stu-id="ac131-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="ac131-112">Jos kentän arvoksi on määritetty Kyllä, tälle kirjausprofiilille lasketaan korko.</span><span class="sxs-lookup"><span data-stu-id="ac131-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="ac131-113">Laske korko</span><span class="sxs-lookup"><span data-stu-id="ac131-113">Calculate interest</span></span>
1. <span data-ttu-id="ac131-114">Siirry kohtaan Luotonvalvonta > Korko > Luo korkolaskut.</span><span class="sxs-lookup"><span data-stu-id="ac131-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="ac131-115">Valitse tapahtumalajit, joille korko lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ac131-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="ac131-116">Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="ac131-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="ac131-117">Jos valitset arvoksi Korko, korolle lasketaan korkoa.</span><span class="sxs-lookup"><span data-stu-id="ac131-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="ac131-118">Tutustu koronkoron laskentaa koskeviin lakeihin, ennen kuin otat nämä tapahtumat käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ac131-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="ac131-119">Korko lasketaan tästä päivästä Päivämäärään-kentän arvoon asti.</span><span class="sxs-lookup"><span data-stu-id="ac131-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="ac131-120">Jos Päivämäärästä-kenttään ei ole määritetty arvoa, kaikki kirjaamattomat korkolaskut peruutetaan ja korko lasketaan uudelleen tapahtuman päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="ac131-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="ac131-121">Syötä korkolaskun päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ac131-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="ac131-122">Kirjausprofiilivaihtoehtoja on kolme: Tili – Käytä jokaisessa korkolaskussa asiakkaan tiliin liitettyä kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="ac131-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="ac131-123">Valitse – Käytä Kirjausprofiili-kentässä valittavaa kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="ac131-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="ac131-124">Tapahtuma – Käytä yksilöllistä kirjausprofiilia tapahtumista, joissa korko lasketaan jokaiselle korkolaskulle.</span><span class="sxs-lookup"><span data-stu-id="ac131-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="ac131-125">Ne tapahtumat, joihin ei ole määritetty kirjausprofiilia, käyttävät kirjausprofiilia, joka on määritetty Myyntireskontran parametrit -lomakkeen Kirjanpito ja arvonlisävero -alueella.</span><span class="sxs-lookup"><span data-stu-id="ac131-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="ac131-126">Valitse kirjausprofiili tässä, jos muutit Käytettävä kirjausprofiili -kohdan arvoksi Valitse.</span><span class="sxs-lookup"><span data-stu-id="ac131-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="ac131-127">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="ac131-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="ac131-128">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="ac131-128">Click Filter.</span></span>
5. <span data-ttu-id="ac131-129">Syötä Ehdot-kenttään asiakkaan tunnus.</span><span class="sxs-lookup"><span data-stu-id="ac131-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="ac131-130">Syötä arvoksi esimerkiksi US-001.</span><span class="sxs-lookup"><span data-stu-id="ac131-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="ac131-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ac131-131">Click OK.</span></span>
7. <span data-ttu-id="ac131-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ac131-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="ac131-133">Tulosta korkolaskut</span><span class="sxs-lookup"><span data-stu-id="ac131-133">Print interest notes</span></span>
1. <span data-ttu-id="ac131-134">Siirry kohtaan Luotonvalvonta > Korko > Tarkastele ja käsittele korkolaskuja.</span><span class="sxs-lookup"><span data-stu-id="ac131-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="ac131-135">Valitse Tila-kentässä Luotu.</span><span class="sxs-lookup"><span data-stu-id="ac131-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="ac131-136">Valitse Tulostettu-kentässä Ei tulostettu.</span><span class="sxs-lookup"><span data-stu-id="ac131-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="ac131-137">Valitse Tulosta.</span><span class="sxs-lookup"><span data-stu-id="ac131-137">Click Print.</span></span>
5. <span data-ttu-id="ac131-138">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="ac131-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="ac131-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ac131-139">Click OK.</span></span>
7. <span data-ttu-id="ac131-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ac131-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="ac131-141">Korkolaskun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="ac131-141">Post the interest note</span></span>
1. <span data-ttu-id="ac131-142">Valitse korkolasku, joka on valmis kirjattavaksi (tila on Luotu).</span><span class="sxs-lookup"><span data-stu-id="ac131-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="ac131-143">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="ac131-143">Click Post.</span></span>
3. <span data-ttu-id="ac131-144">Syötä korkolaskun kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ac131-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="ac131-145">Valitse Kyllä, kun haluat luoda kullekin korkolaskulle kirjanpitotapahtuman.</span><span class="sxs-lookup"><span data-stu-id="ac131-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="ac131-146">Jos et valitse Kyllä-arvoa, kaikkien asiakkaan korkolaskujen korot lasketaan yhteen ja kirjataan kirjanpitoon yhtenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="ac131-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="ac131-147">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="ac131-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="ac131-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ac131-148">Click OK.</span></span>
6. <span data-ttu-id="ac131-149">Valitse Tila-kentässä Kirjattu.</span><span class="sxs-lookup"><span data-stu-id="ac131-149">In the Status field, select 'Posted'.</span></span>


