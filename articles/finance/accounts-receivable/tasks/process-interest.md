---
title: Koron käsittely
description: Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442790"
---
# <a name="process-interest"></a><span data-ttu-id="b9f03-103">Koron käsittely</span><span class="sxs-lookup"><span data-stu-id="b9f03-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9f03-104">Tässä menettelyssä kerrotaan, miten korkolaskuja luodaan, tulostetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="b9f03-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="b9f03-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="b9f03-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="b9f03-106">Määritä kirjausprofiilin korko.</span><span class="sxs-lookup"><span data-stu-id="b9f03-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="b9f03-107">Siirry kohtaan **Siirtymisruutu** **> Moduulit > Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="b9f03-108">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-108">Click **Edit**.</span></span>
3. <span data-ttu-id="b9f03-109">Valitse korkokoodi **Asetukset**-pikavälilehden **Korkokoodi**-kentästä avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b9f03-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="b9f03-110">Jos et halua laskea korkoa tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b9f03-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="b9f03-111">**Taulurajoitus**-pikavälilehden avulla voit muuttaa tapaa, jolla korko käsitellään.</span><span class="sxs-lookup"><span data-stu-id="b9f03-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="b9f03-112">Jos kentän arvoksi on määritetty Kyllä, tälle kirjausprofiilille lasketaan korko.</span><span class="sxs-lookup"><span data-stu-id="b9f03-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="b9f03-113">Laske korko</span><span class="sxs-lookup"><span data-stu-id="b9f03-113">Calculate interest</span></span>
1. <span data-ttu-id="b9f03-114">Siirry kohtaan **Siirtymisruutu** **> Moduulit > Luotonvalvonta > Korko > Luo korkolaskut**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="b9f03-115">Valitse tapahtumalajit, joille korko lasketaan.</span><span class="sxs-lookup"><span data-stu-id="b9f03-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="b9f03-116">Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="b9f03-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="b9f03-117">Jos valitset **Korko**-kentän arvoksi Kyllä, korolle lasketaan korkoa.</span><span class="sxs-lookup"><span data-stu-id="b9f03-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="b9f03-118">Tutustu koronkoron laskentaa koskeviin lakeihin, ennen kuin otat nämä tapahtumat käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b9f03-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="b9f03-119">Anna **Päivämäärästä**-kenttään päivämäärä, josta lähtien korko lasketaan.</span><span class="sxs-lookup"><span data-stu-id="b9f03-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="b9f03-120">Jos **Päivämäärästä**-kenttään ei ole määritetty arvoa, kaikki kirjaamattomat korkolaskut peruutetaan ja korko lasketaan uudelleen tapahtuman päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="b9f03-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="b9f03-121">Anna **Päivämäärään**-kenttään päivämäärä, johon asti korko lasketaan.</span><span class="sxs-lookup"><span data-stu-id="b9f03-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="b9f03-122">**Käytettävä kirjausprofiili** -kentästä on valittava vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b9f03-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="b9f03-123">Kirjausprofiilivaihtoehtoja on kolme:</span><span class="sxs-lookup"><span data-stu-id="b9f03-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="b9f03-124">Tili – Käytä kunkin korkolaskun asiakastilille määritettyä kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="b9f03-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="b9f03-125">Valitse – Käytä Kirjausprofiili-kentässä valittavaa kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="b9f03-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="b9f03-126">Tapahtuma – Käytä yksilöllistä kirjausprofiilia tapahtumista, joissa korko lasketaan jokaiselle korkolaskulle.</span><span class="sxs-lookup"><span data-stu-id="b9f03-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="b9f03-127">Ne tapahtumat, joihin ei ole määritetty kirjausprofiilia, käyttävät kirjausprofiilia, joka on määritetty Myyntireskontran parametrit -lomakkeen Kirjanpito ja arvonlisävero -alueella.</span><span class="sxs-lookup"><span data-stu-id="b9f03-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="b9f03-128">Laajenna **Sisällytettävät tietueet** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="b9f03-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="b9f03-129">Valitse **Suodatin**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-129">Click **Filter**.</span></span>
9. <span data-ttu-id="b9f03-130">Anna **Ehdot**-kentässä asiakkaan tunnus.</span><span class="sxs-lookup"><span data-stu-id="b9f03-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="b9f03-131">Syötä arvoksi esimerkiksi US-001.</span><span class="sxs-lookup"><span data-stu-id="b9f03-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="b9f03-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-132">Click **OK**.</span></span>
7. <span data-ttu-id="b9f03-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="b9f03-134">Tulosta korkolaskut</span><span class="sxs-lookup"><span data-stu-id="b9f03-134">Print interest notes</span></span>
1. <span data-ttu-id="b9f03-135">Siirry kohtaan **Siirtymisruutu** **> Moduulit > Luotonvalvonta > Korko > Tarkastele ja käsittele korkolaskuja**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="b9f03-136">Valitse **Tila**-kentässä Luotu.</span><span class="sxs-lookup"><span data-stu-id="b9f03-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="b9f03-137">Valitse **Tulostettu**-kentässä Ei tulostettu.</span><span class="sxs-lookup"><span data-stu-id="b9f03-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="b9f03-138">Valitse **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-138">Click **Print**.</span></span>
5. <span data-ttu-id="b9f03-139">Laajenna **Sisällytettävät tietueet** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="b9f03-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="b9f03-140">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-140">Click **OK**.</span></span>
7. <span data-ttu-id="b9f03-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b9f03-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="b9f03-142">Korkolaskun kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="b9f03-142">Post the interest note</span></span>
1. <span data-ttu-id="b9f03-143">Valitse korkolasku, joka on valmis kirjattavaksi (tila on Luotu).</span><span class="sxs-lookup"><span data-stu-id="b9f03-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="b9f03-144">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-144">Click **Post**.</span></span>
3. <span data-ttu-id="b9f03-145">Syötä korkolaskun kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b9f03-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="b9f03-146">Valitse Kyllä, kun haluat luoda kullekin korkolaskulle kirjanpitotapahtuman.</span><span class="sxs-lookup"><span data-stu-id="b9f03-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="b9f03-147">Jos et valitse Kyllä-arvoa, kaikkien asiakkaan korkolaskujen korot lasketaan yhteen ja kirjataan kirjanpitoon yhtenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="b9f03-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="b9f03-148">Laajenna **Sisällytettävät tietueet** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="b9f03-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="b9f03-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f03-149">Click **OK**.</span></span>
6. <span data-ttu-id="b9f03-150">Valitse **Tila**-kentässä Kirjattu.</span><span class="sxs-lookup"><span data-stu-id="b9f03-150">In the **Status** field, select 'Posted'.</span></span>

