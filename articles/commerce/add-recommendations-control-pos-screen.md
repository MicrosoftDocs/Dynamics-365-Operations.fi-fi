---
title: Suositusten lisääminen tapahtumanäyttöön
description: Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Commercein näytön asettelun suunnittelutoimintoa.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af2450b27106325a86f6db68f9791637694cda63
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665077"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="e5199-103">Suositusten lisääminen tapahtumanäyttöön</span><span class="sxs-lookup"><span data-stu-id="e5199-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e5199-104">Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Commercein näytön asettelun suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="e5199-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="e5199-105">Lisätietoja tuotesuositusominaisuuksista on [POS-dokumentaation tuotesuosituksissa](product.md).</span><span class="sxs-lookup"><span data-stu-id="e5199-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="e5199-106">Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Commercea.</span><span class="sxs-lookup"><span data-stu-id="e5199-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="e5199-107">Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="e5199-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="e5199-108">Avaa asettelun suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="e5199-108">Open Layout designer</span></span>

1. <span data-ttu-id="e5199-109">Siirry kohtaan **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="e5199-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="e5199-110">Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="e5199-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="e5199-111">Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e5199-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="e5199-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e5199-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="e5199-113">Valitse esimerkiksi **Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e5199-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="e5199-114">Valitse **Asettelun suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="e5199-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="e5199-115">Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e5199-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="e5199-116">Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5199-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="e5199-117">Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva.</span><span class="sxs-lookup"><span data-stu-id="e5199-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="e5199-118">Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.</span><span class="sxs-lookup"><span data-stu-id="e5199-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="e5199-119">[![Asettelun suunnittelutoiminto](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="e5199-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="e5199-120">Näyttöasetuksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="e5199-120">Choose a display option</span></span>

<span data-ttu-id="e5199-121">Käytettävissä on kaksi asetusta.</span><span class="sxs-lookup"><span data-stu-id="e5199-121">There are two configurations options available.</span></span> <span data-ttu-id="e5199-122">Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="e5199-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="e5199-123">Asetukset ovat:</span><span class="sxs-lookup"><span data-stu-id="e5199-123">The two options are:</span></span>

- <span data-ttu-id="e5199-124">Suositukset ovat aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="e5199-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="e5199-125">**Suositukset**-välilehti näkyy ruudukossa näytön oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="e5199-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="e5199-126">Suositusten tuominen aina näkyviin</span><span class="sxs-lookup"><span data-stu-id="e5199-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="e5199-127">Pienennä tapahtumarivien erittelyalueen korkeutta niin, että se on samalla korkeudella kuin vasemmalla puolella oleva asiakaspaneeli.</span><span class="sxs-lookup"><span data-stu-id="e5199-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="e5199-128">[![Tapahtumarivien erittelyalueen korkeutta vähennetty](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="e5199-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="e5199-129">Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä.</span><span class="sxs-lookup"><span data-stu-id="e5199-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="e5199-130">Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan.</span><span class="sxs-lookup"><span data-stu-id="e5199-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="e5199-131">[![Suositusten ohjaus lisätty asetteluun](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="e5199-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="e5199-132">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="e5199-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="e5199-133">Valitse Commercessa **Retail ja Commerce** &gt; **Retail ja Commerce IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="e5199-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="e5199-134">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="e5199-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="e5199-135">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="e5199-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="e5199-136">Suositukset-välilehden lisääminen painikeruudukkoon näytön oikealla puolella</span><span class="sxs-lookup"><span data-stu-id="e5199-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="e5199-137">Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.</span><span class="sxs-lookup"><span data-stu-id="e5199-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="e5199-138">Valitse **Mukauta**.</span><span class="sxs-lookup"><span data-stu-id="e5199-138">Click **Customize**.</span></span>

    <span data-ttu-id="e5199-139">[![Mukautus - Välilehden ohjausvalintaikkuna](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="e5199-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="e5199-140">Valitse **Uusi välilehti**.</span><span class="sxs-lookup"><span data-stu-id="e5199-140">Click **New tab**.</span></span>
4. <span data-ttu-id="e5199-141">Etsi juuri lisäämäsi uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="e5199-141">Find the new tab that you just added.</span></span> <span data-ttu-id="e5199-142">Näyttöä on ehkä vieritettävä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="e5199-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="e5199-143">Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="e5199-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="e5199-144">[![Suositeltujen tuotteiden valinta Sisältö-valikossa](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="e5199-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="e5199-145">Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi Suositellut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="e5199-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="e5199-146">Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.</span><span class="sxs-lookup"><span data-stu-id="e5199-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="e5199-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5199-147">Click **OK**.</span></span> <span data-ttu-id="e5199-148">Painikeruudukkoon tulee uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="e5199-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="e5199-149">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="e5199-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="e5199-150">Valitse Commercessa **Retail ja Commerce** &gt; **Retail ja Commerce IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="e5199-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="e5199-151">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="e5199-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="e5199-152">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="e5199-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5199-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e5199-153">Additional resources</span></span>

[<span data-ttu-id="e5199-154">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e5199-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e5199-155">Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="e5199-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e5199-156">Tuotesuositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e5199-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e5199-157">Kohdennettujen suositusten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e5199-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e5199-158">Kohdennetuista tuotesuosituksista kieltäytyminen</span><span class="sxs-lookup"><span data-stu-id="e5199-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e5199-159">"Osta samankaltaisia tyylejä" -suositusten käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="e5199-159">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="e5199-160">Tuotesuositusten lisääminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="e5199-160">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e5199-161">AI-ML-suositusten tulosten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e5199-161">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e5199-162">Kuratoitujen suositusten manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="e5199-162">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e5199-163">Suositusten luominen esittelytietojen avulla</span><span class="sxs-lookup"><span data-stu-id="e5199-163">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e5199-164">Tuotesuositukset – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="e5199-164">Product recommendations FAQ</span></span>](faq-recommendations.md)
