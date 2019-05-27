---
title: Käsittele maksukehotuksia
description: Tässä menettelyssä käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549626"
---
# <a name="process-collection-letters"></a><span data-ttu-id="7f86b-103">Käsittele maksukehotuksia</span><span class="sxs-lookup"><span data-stu-id="7f86b-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f86b-104">Tässä menettelyssä käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="7f86b-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="7f86b-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="7f86b-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="7f86b-106">Määritä maksukehotusjärjestys kirjausprofiilissa</span><span class="sxs-lookup"><span data-stu-id="7f86b-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="7f86b-107">Valitse **Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="7f86b-108">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-108">Click **Edit**.</span></span>
3. <span data-ttu-id="7f86b-109">Valitse maksukehotussarja avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7f86b-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="7f86b-110">Jos et halua luoda maksukehotuksia tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="7f86b-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="7f86b-111">Laajenna Taulurajoitus-välilehti ja muuta tapaa, jolla maksukehotuksia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="7f86b-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="7f86b-112">Jos kentän arvoksi on määritetty **Kyllä**, tälle kirjausprofiilille luodaan maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="7f86b-113">Luo maksukehotukset</span><span class="sxs-lookup"><span data-stu-id="7f86b-113">Create collection letters</span></span>
1. <span data-ttu-id="7f86b-114">Valitse **Luotonvalvonta > Maksukehotus > Luo maksukehotukset**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="7f86b-115">Valitse tapahtumatyypit, joissa käytetään maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="7f86b-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="7f86b-116">Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="7f86b-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="7f86b-117">Valitse asetus **Maksukehotus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7f86b-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="7f86b-118">Anna maksukehotuksen päiväys.</span><span class="sxs-lookup"><span data-stu-id="7f86b-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="7f86b-119">Valitse kirjausprofiili, jos muutit **Käytettävä kirjausprofiili** -asetukseksi **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="7f86b-120">Käytettävissä ovat seuraavat kaksi kirjausprofiilivaihtoehtoa:</span><span class="sxs-lookup"><span data-stu-id="7f86b-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="7f86b-121">**Tili** – Käytä kunkin korkolaskun asiakastilille määritettyä kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="7f86b-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="7f86b-122">**Valitse** – Käytä **Kirjausprofiili**-kentässä valittavaa kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="7f86b-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="7f86b-123">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="7f86b-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="7f86b-124">Valitse **Suodatin**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-124">Click **Filter**.</span></span>
7. <span data-ttu-id="7f86b-125">Anna **Ehdot**-kentässä asiakkaan tunnus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="7f86b-126">Syötä arvoksi esimerkiksi US-001.</span><span class="sxs-lookup"><span data-stu-id="7f86b-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="7f86b-127">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-127">Click **OK**.</span></span>
9. <span data-ttu-id="7f86b-128">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="7f86b-129">Tulostaa maksukehotukset</span><span class="sxs-lookup"><span data-stu-id="7f86b-129">Print collection letters</span></span>
1. <span data-ttu-id="7f86b-130">Valitse **Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="7f86b-131">Valitse **Tila**-kentässä **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="7f86b-132">Valitse **Tulostettu**-kentässä **Ei tulostettu**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="7f86b-133">Valitse **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-133">Click **Print**.</span></span>
5. <span data-ttu-id="7f86b-134">Valitse **Maksukehotus**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="7f86b-135">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="7f86b-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="7f86b-136">Anna kirjausten katkaisupäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7f86b-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="7f86b-137">Tulosta maksukehotus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="7f86b-138">Kirjaa maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="7f86b-139">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-139">Click **Post**.</span></span>
   2. <span data-ttu-id="7f86b-140">Anna maksukehotuksen kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7f86b-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="7f86b-141">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="7f86b-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="7f86b-142">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-142">Click **OK**.</span></span>
   5. <span data-ttu-id="7f86b-143">Valitse **Tila**-kentässä **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="7f86b-144">Valitse asetus **Tulostettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7f86b-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="7f86b-145">Maksukehotusten hallinta asiakastasolla</span><span class="sxs-lookup"><span data-stu-id="7f86b-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="7f86b-146">Voit määrittää maksukehotukset myös asiakastasolla, jolloin kunkin tapahtuman maksukehotuskoodia seurataan. Maksukehotuksen käsittely perustuu kuitenkin yhteen asiakkaalle tallennettuun maksukehotetasoon.</span><span class="sxs-lookup"><span data-stu-id="7f86b-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="7f86b-147">Yksi maksukehotus sisältää kaikki kyseisen asiakkaan erääntyneet tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="7f86b-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="7f86b-148">Koska eräpäivän jälkeistä maksuaikaa seurataan nyt asiakastasolla, seuraavaa maksukehotusta ei lähetetä, ennen kuin tietty määrä päiviä sarjan seuraavan maksukehotuksen eräpäivän jälkeistä maksuaika on kulunut, vaikka tapahtumat erääntyvät sen jälkeen, kun viimeisin maksukehotus on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="7f86b-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="7f86b-149">Tämä asetus vähentää kullekin asiakkaalle lähetettävien maksukehotusten määrää.</span><span class="sxs-lookup"><span data-stu-id="7f86b-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="7f86b-150">Asiakkaan määrittäminen maksukehotusten hallintaan asiakastasolla</span><span class="sxs-lookup"><span data-stu-id="7f86b-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="7f86b-151">Valitse ensin **Luotonvalvonta > Asetukset > Myyntireskontran parametrit** ja sitten **Perintä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7f86b-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="7f86b-152">Muuta **Luo maksukehotus per** -arvoksi **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="7f86b-153">Valitse **Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="7f86b-154">Asiakkaan kaikille erääntyneille tapahtumille luodaan vain yksi maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="7f86b-155">Maksujen ja hyvityslaskujen ohittaminen maksukehotuksen koodia laskettaessa</span><span class="sxs-lookup"><span data-stu-id="7f86b-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="7f86b-156">Jos sisällytät maksukehotuksiin sisältyviin tapahtumiin maksuja ja hyvityslaskuja, sinulla voi olla maksukehotuksen käynnistäviä maksuja tai hyvityslaskuja.</span><span class="sxs-lookup"><span data-stu-id="7f86b-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="7f86b-157">Voit hallita, miten maksut ja hyvityslaskut hallitsevat maksukehotuskoodia vaihtamalla **Älä huomioi maksuja tai hyvityslaskuja maksukehotuksen koodin laskemisessa** -parametrin arvon.</span><span class="sxs-lookup"><span data-stu-id="7f86b-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="7f86b-158">Ohita maksut ja hyvityslaskut maksukehotuksen koodia laskettaessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7f86b-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="7f86b-159">Valitse ensin **Luotonvalvonta > Asetukset > Myyntireskontran parametrit** ja sitten **Perintä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7f86b-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="7f86b-160">Vaihda **Älä huomioi maksuja tai hyvityslaskuja maksukehotuksen koodin laskemisessa** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7f86b-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
