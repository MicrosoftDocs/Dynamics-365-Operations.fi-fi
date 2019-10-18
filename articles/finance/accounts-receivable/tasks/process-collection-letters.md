---
title: Käsittele maksukehotuksia
description: Tässä aiheessa käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177575"
---
# <a name="process-collection-letters"></a><span data-ttu-id="048c7-103">Käsittele maksukehotuksia</span><span class="sxs-lookup"><span data-stu-id="048c7-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="048c7-104">Tässä aiheessa käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="048c7-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="048c7-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="048c7-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="048c7-106">Määritä maksukehotusjärjestys kirjausprofiilissa</span><span class="sxs-lookup"><span data-stu-id="048c7-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="048c7-107">Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="048c7-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="048c7-108">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="048c7-108">Click **Edit**.</span></span>
3. <span data-ttu-id="048c7-109">Valitse maksukehotussarja avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="048c7-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="048c7-110">Jos et halua luoda maksukehotuksia tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="048c7-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="048c7-111">Laajenna **Taulurajoitus**-välilehti ja muuta tapaa, jolla maksukehotuksia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="048c7-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="048c7-112">Jos kentän arvoksi on määritetty **Kyllä**, tälle kirjausprofiilille luodaan maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="048c7-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="048c7-113">Luo maksukehotukset</span><span class="sxs-lookup"><span data-stu-id="048c7-113">Create collection letters</span></span>
1. <span data-ttu-id="048c7-114">Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Maksukehotus > Luo maksukehotukset**.</span><span class="sxs-lookup"><span data-stu-id="048c7-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="048c7-115">Valitse tapahtumatyypit, joissa käytetään maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="048c7-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="048c7-116">Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="048c7-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="048c7-117">Valitse asetus **Maksukehotus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="048c7-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="048c7-118">Lisää **Maksukehotuksen päivämäärä** -kenttään maksukehotuksen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="048c7-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="048c7-119">Valitse kirjausprofiili, jos muutit **Käytettävä kirjausprofiili** -asetukseksi **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="048c7-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="048c7-120">Käytettävissä ovat seuraavat kaksi kirjausprofiilivaihtoehtoa:</span><span class="sxs-lookup"><span data-stu-id="048c7-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="048c7-121">**Tili** – Käytä kunkin korkolaskun asiakastilille määritettyä kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="048c7-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="048c7-122">**Valitse** – Käytä **Kirjausprofiili**-kentässä valittavaa kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="048c7-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="048c7-123">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="048c7-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="048c7-124">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="048c7-124">Select **Filter**.</span></span>
8. <span data-ttu-id="048c7-125">Anna **Ehdot**-kentässä asiakkaan tunnus.</span><span class="sxs-lookup"><span data-stu-id="048c7-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="048c7-126">Syötä arvoksi esimerkiksi US-001.</span><span class="sxs-lookup"><span data-stu-id="048c7-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="048c7-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="048c7-127">Select **OK**.</span></span>
10. <span data-ttu-id="048c7-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="048c7-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="048c7-129">Tulostaa maksukehotukset</span><span class="sxs-lookup"><span data-stu-id="048c7-129">Print collection letters</span></span>
1. <span data-ttu-id="048c7-130">Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia**.</span><span class="sxs-lookup"><span data-stu-id="048c7-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="048c7-131">Valitse **Tila**-kentässä **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="048c7-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="048c7-132">Valitse **Tulostettu**-kentässä **Ei tulostettu**.</span><span class="sxs-lookup"><span data-stu-id="048c7-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="048c7-133">Valitse **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="048c7-133">Select **Print**.</span></span>
5. <span data-ttu-id="048c7-134">Valitse **Maksukehotus**.</span><span class="sxs-lookup"><span data-stu-id="048c7-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="048c7-135">Kirjoita **Parametrit** -osaan kirjausten katkaisupäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="048c7-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="048c7-136">Laajenna **Sisällytettävät tietueet** -osa ja kirjoita maksukehotushuomautuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="048c7-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="048c7-137">Tulosta maksukehotus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="048c7-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="048c7-138">Kirjaa maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="048c7-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="048c7-139">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="048c7-139">Select **Post**.</span></span>
    1. <span data-ttu-id="048c7-140">Anna maksukehotuksen kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="048c7-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="048c7-141">Laajenna **Sisällytettävät tietueet** -osa.</span><span class="sxs-lookup"><span data-stu-id="048c7-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="048c7-142">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="048c7-142">Select **OK**.</span></span>
    1. <span data-ttu-id="048c7-143">Valitse **Tila**-kentässä **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="048c7-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="048c7-144">Valitse asetus **Tulostettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="048c7-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="048c7-145">Maksukehotusten hallinta asiakastasolla</span><span class="sxs-lookup"><span data-stu-id="048c7-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="048c7-146">Voit määrittää maksukehotukset myös asiakastasolla, jolloin kunkin tapahtuman maksukehotuskoodia seurataan. Maksukehotuksen käsittely perustuu kuitenkin yhteen asiakkaalle tallennettuun maksukehotetasoon.</span><span class="sxs-lookup"><span data-stu-id="048c7-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="048c7-147">Yksi maksukehotus sisältää kaikki kyseisen asiakkaan erääntyneet tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="048c7-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="048c7-148">Koska eräpäivän jälkeistä maksuaikaa seurataan nyt asiakastasolla, seuraavaa maksukehotusta ei lähetetä, ennen kuin tietty määrä päiviä sarjan seuraavan maksukehotuksen eräpäivän jälkeistä maksuaika on kulunut, vaikka tapahtumat erääntyvät sen jälkeen, kun viimeisin maksukehotus on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="048c7-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="048c7-149">Tämä asetus vähentää kullekin asiakkaalle lähetettävien maksukehotusten määrää.</span><span class="sxs-lookup"><span data-stu-id="048c7-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="048c7-150">Asiakkaan määrittäminen maksukehotusten hallintaan asiakastasolla</span><span class="sxs-lookup"><span data-stu-id="048c7-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="048c7-151">Valitse ensin **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Myyntireskontran parametrit** ja sitten **Perintä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="048c7-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="048c7-152">Muuta **Luo maksukehotus per** -arvoksi **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="048c7-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="048c7-153">Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia**.</span><span class="sxs-lookup"><span data-stu-id="048c7-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="048c7-154">Asiakkaan kaikille erääntyneille tapahtumille luodaan vain yksi maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="048c7-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="048c7-155">Maksujen ja hyvityslaskujen ohittaminen maksukehotuksen koodia laskettaessa</span><span class="sxs-lookup"><span data-stu-id="048c7-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="048c7-156">Jos sisällytät maksukehotuksiin sisältyviin tapahtumiin maksuja ja hyvityslaskuja, sinulla voi olla maksukehotuksen käynnistäviä maksuja tai hyvityslaskuja.</span><span class="sxs-lookup"><span data-stu-id="048c7-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="048c7-157">Voit hallita, miten maksut ja hyvityslaskut hallitsevat maksukehotuskoodia vaihtamalla **Älä huomioi maksuja tai hyvityslaskuja maksukehotuksen koodin laskemisessa** -parametrin arvon.</span><span class="sxs-lookup"><span data-stu-id="048c7-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="048c7-158">Ohita maksut ja hyvityslaskut maksukehotuksen koodia laskettaessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="048c7-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="048c7-159">Valitse ensin **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Myyntireskontran parametrit** ja sitten **Perintä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="048c7-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="048c7-160">Vaihda **Älä huomioi maksuja tai hyvityslaskuja maksukehotuksen koodin laskemisessa** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="048c7-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>