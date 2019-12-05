---
title: Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle
description: Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811213"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="e1d78-103">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle</span><span class="sxs-lookup"><span data-stu-id="e1d78-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e1d78-104">Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Retailin näytön asettelun suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="e1d78-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="e1d78-105">Lisätietoja tuotesuositusominaisuuksista on [POS-dokumentaation tuotesuosituksissa](product.md).</span><span class="sxs-lookup"><span data-stu-id="e1d78-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="e1d78-106">Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Microsoft Dynamics 365 Retailia.</span><span class="sxs-lookup"><span data-stu-id="e1d78-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="e1d78-107">Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="e1d78-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="e1d78-108">Avaa asettelun suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="e1d78-108">Open Layout designer</span></span>

1. <span data-ttu-id="e1d78-109">Siirry kohtaan **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="e1d78-110">Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="e1d78-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="e1d78-111">Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="e1d78-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e1d78-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="e1d78-113">Valitse esimerkiksi **Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="e1d78-114">Valitse **Asettelun suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="e1d78-115">Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e1d78-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="e1d78-116">Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e1d78-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="e1d78-117">Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva.</span><span class="sxs-lookup"><span data-stu-id="e1d78-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="e1d78-118">Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.</span><span class="sxs-lookup"><span data-stu-id="e1d78-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="e1d78-119">[![Asettelun suunnittelutoiminto](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="e1d78-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="e1d78-120">Näyttöasetuksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="e1d78-120">Choose a display option</span></span>

<span data-ttu-id="e1d78-121">Käytettävissä on kaksi asetusta.</span><span class="sxs-lookup"><span data-stu-id="e1d78-121">There are two configurations options available.</span></span> <span data-ttu-id="e1d78-122">Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="e1d78-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="e1d78-123">Asetukset ovat:</span><span class="sxs-lookup"><span data-stu-id="e1d78-123">The two options are:</span></span>

- <span data-ttu-id="e1d78-124">Suositukset ovat aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="e1d78-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="e1d78-125">**Suositukset**-välilehti näkyy ruudukossa näytön oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="e1d78-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="e1d78-126">Suositusten tuominen aina näkyviin</span><span class="sxs-lookup"><span data-stu-id="e1d78-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="e1d78-127">Pienennä tapahtumarivien erittelyalueen korkeutta niin, että se on samalla korkeudella kuin vasemmalla puolella oleva asiakaspaneeli.</span><span class="sxs-lookup"><span data-stu-id="e1d78-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="e1d78-128">[![Tapahtumarivien erittelyalueen korkeutta vähennetty](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="e1d78-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="e1d78-129">Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä.</span><span class="sxs-lookup"><span data-stu-id="e1d78-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="e1d78-130">Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan.</span><span class="sxs-lookup"><span data-stu-id="e1d78-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="e1d78-131">[![Suositusten ohjaus lisätty asetteluun](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="e1d78-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="e1d78-132">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="e1d78-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="e1d78-133">Valitse Dynamics 365 for Retailissa **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="e1d78-134">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="e1d78-135">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="e1d78-136">Suositukset-välilehden lisääminen painikeruudukkoon näytön oikealla puolella</span><span class="sxs-lookup"><span data-stu-id="e1d78-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="e1d78-137">Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.</span><span class="sxs-lookup"><span data-stu-id="e1d78-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="e1d78-138">Valitse **Mukauta**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-138">Click **Customize**.</span></span>

    <span data-ttu-id="e1d78-139">[![Mukautus - Välilehden ohjausvalintaikkuna](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="e1d78-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="e1d78-140">Valitse **Uusi välilehti**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-140">Click **New tab**.</span></span>
4. <span data-ttu-id="e1d78-141">Etsi juuri lisäämäsi uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="e1d78-141">Find the new tab that you just added.</span></span> <span data-ttu-id="e1d78-142">Näyttöä on ehkä vieritettävä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="e1d78-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="e1d78-143">Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="e1d78-144">[![Suositeltujen tuotteiden valinta Sisältö-valikossa](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="e1d78-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="e1d78-145">Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi Suositellut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="e1d78-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="e1d78-146">Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.</span><span class="sxs-lookup"><span data-stu-id="e1d78-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="e1d78-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-147">Click **OK**.</span></span> <span data-ttu-id="e1d78-148">Painikeruudukkoon tulee uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="e1d78-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="e1d78-149">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="e1d78-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="e1d78-150">Valitse Dynamics 365 for Retailissa **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="e1d78-151">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="e1d78-152">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="e1d78-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1d78-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e1d78-153">Additional resources</span></span>

[<span data-ttu-id="e1d78-154">Tuotesuositukset myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="e1d78-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e1d78-155">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e1d78-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
