--- 
title: "Käsittele maksukehotuksia"
description: "Tässä menettelyssä käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: fe76f2934360580c4015ea13225b9228cc2780b9
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="d2912-103">Käsittele maksukehotuksia</span><span class="sxs-lookup"><span data-stu-id="d2912-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2912-104">Tässä menettelyssä käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d2912-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="d2912-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="d2912-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="d2912-106">Määritä maksukehotusjärjestys kirjausprofiilissa</span><span class="sxs-lookup"><span data-stu-id="d2912-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="d2912-107">Siirry kohtaan Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="d2912-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="d2912-108">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d2912-108">Click Edit.</span></span>
    * <span data-ttu-id="d2912-109">Valitse maksukehotussarja avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="d2912-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="d2912-110">Jos et halua luoda maksukehotuksia tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="d2912-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="d2912-111">Voit muuttaa Taulurajoitus-välilehdessä tapaa, jolla maksukehotuksia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="d2912-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="d2912-112">Jos kentän arvoksi on määritetty Kyllä, tälle kirjausprofiilille luodaan maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="d2912-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="d2912-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d2912-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="d2912-114">Luo maksukehotukset</span><span class="sxs-lookup"><span data-stu-id="d2912-114">Create collection letters</span></span>
1. <span data-ttu-id="d2912-115">Siirry kohtaan Luotonvalvonta > Maksukehotus > Luo maksukehotukset.</span><span class="sxs-lookup"><span data-stu-id="d2912-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="d2912-116">Valitse tapahtumatyypit, joissa käytetään maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="d2912-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="d2912-117">Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="d2912-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="d2912-118">Valitse asetus Maksukehotus-kentästä.</span><span class="sxs-lookup"><span data-stu-id="d2912-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="d2912-119">Anna maksukehotuksen päiväys.</span><span class="sxs-lookup"><span data-stu-id="d2912-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="d2912-120">Kirjausprofiilivaihtoehtoja on kaksi: Tili – käytä jokaisessa korkolaskussa asiakkaan tiliin liitettyä kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="d2912-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="d2912-121">Valitse – Käytä Kirjausprofiili-kentässä valittavaa kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="d2912-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="d2912-122">Valitse kirjausprofiili, jos muutit Käytettävä kirjausprofiili -asetukseksi Valitse.</span><span class="sxs-lookup"><span data-stu-id="d2912-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="d2912-123">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="d2912-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="d2912-124">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="d2912-124">Click Filter.</span></span>
6. <span data-ttu-id="d2912-125">Anna Ehdot-kentässä asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="d2912-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="d2912-126">Syötä arvoksi esimerkiksi US-001.</span><span class="sxs-lookup"><span data-stu-id="d2912-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="d2912-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d2912-127">Click OK.</span></span>
8. <span data-ttu-id="d2912-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d2912-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="d2912-129">Tulostaa maksukehotukset</span><span class="sxs-lookup"><span data-stu-id="d2912-129">Print collection letters</span></span>
1. <span data-ttu-id="d2912-130">Valitse Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="d2912-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="d2912-131">Valitse Tila-kentässä Luotu.</span><span class="sxs-lookup"><span data-stu-id="d2912-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="d2912-132">Valitse Tulostettu-kentässä Ei tulostettu.</span><span class="sxs-lookup"><span data-stu-id="d2912-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="d2912-133">Valitse Tulosta.</span><span class="sxs-lookup"><span data-stu-id="d2912-133">Click Print.</span></span>
5. <span data-ttu-id="d2912-134">Valitse Maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="d2912-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="d2912-135">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="d2912-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d2912-136">Anna kirjausten katkaisupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d2912-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="d2912-137">Tulosta maksukehotus valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="d2912-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="d2912-138">Kirjaa maksukehotus</span><span class="sxs-lookup"><span data-stu-id="d2912-138">Post the collection letter</span></span>
1. <span data-ttu-id="d2912-139">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="d2912-139">Click Post.</span></span>
2. <span data-ttu-id="d2912-140">Anna maksukehotuksen kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d2912-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="d2912-141">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="d2912-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="d2912-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d2912-142">Click OK.</span></span>
5. <span data-ttu-id="d2912-143">Valitse Tila-kentässä Kirjattu.</span><span class="sxs-lookup"><span data-stu-id="d2912-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="d2912-144">Valitse vaihtoehto Tulostettu-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d2912-144">In the Printed field, select an option.</span></span>


