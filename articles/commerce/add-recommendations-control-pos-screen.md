---
title: Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle
description: Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Commercein näytön asettelun suunnittelutoimintoa.
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
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022343"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="4841f-103">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle</span><span class="sxs-lookup"><span data-stu-id="4841f-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="4841f-104">Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 Commercein näytön asettelun suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="4841f-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="4841f-105">Lisätietoja tuotesuositusominaisuuksista on [POS-dokumentaation tuotesuosituksissa](product.md).</span><span class="sxs-lookup"><span data-stu-id="4841f-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="4841f-106">Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Commercea.</span><span class="sxs-lookup"><span data-stu-id="4841f-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="4841f-107">Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="4841f-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="4841f-108">Avaa asettelun suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="4841f-108">Open Layout designer</span></span>

1. <span data-ttu-id="4841f-109">Siirry kohtaan **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="4841f-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="4841f-110">Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="4841f-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="4841f-111">Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="4841f-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="4841f-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4841f-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="4841f-113">Valitse esimerkiksi **Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="4841f-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="4841f-114">Valitse **Asettelun suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="4841f-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="4841f-115">Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="4841f-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="4841f-116">Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4841f-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="4841f-117">Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva.</span><span class="sxs-lookup"><span data-stu-id="4841f-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="4841f-118">Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.</span><span class="sxs-lookup"><span data-stu-id="4841f-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="4841f-119">[![Asettelun suunnittelutoiminto](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="4841f-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="4841f-120">Näyttöasetuksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="4841f-120">Choose a display option</span></span>

<span data-ttu-id="4841f-121">Käytettävissä on kaksi asetusta.</span><span class="sxs-lookup"><span data-stu-id="4841f-121">There are two configurations options available.</span></span> <span data-ttu-id="4841f-122">Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="4841f-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="4841f-123">Asetukset ovat:</span><span class="sxs-lookup"><span data-stu-id="4841f-123">The two options are:</span></span>

- <span data-ttu-id="4841f-124">Suositukset ovat aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="4841f-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="4841f-125">**Suositukset**-välilehti näkyy ruudukossa näytön oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="4841f-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="4841f-126">Suositusten tuominen aina näkyviin</span><span class="sxs-lookup"><span data-stu-id="4841f-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="4841f-127">Pienennä tapahtumarivien erittelyalueen korkeutta niin, että se on samalla korkeudella kuin vasemmalla puolella oleva asiakaspaneeli.</span><span class="sxs-lookup"><span data-stu-id="4841f-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="4841f-128">[![Tapahtumarivien erittelyalueen korkeutta vähennetty](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="4841f-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="4841f-129">Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä.</span><span class="sxs-lookup"><span data-stu-id="4841f-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="4841f-130">Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan.</span><span class="sxs-lookup"><span data-stu-id="4841f-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="4841f-131">[![Suositusten ohjaus lisätty asetteluun](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="4841f-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="4841f-132">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="4841f-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="4841f-133">Valitse Commercessa **Retail ja Commerce** &gt; **Retail ja Commerce IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="4841f-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="4841f-134">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="4841f-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="4841f-135">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="4841f-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="4841f-136">Suositukset-välilehden lisääminen painikeruudukkoon näytön oikealla puolella</span><span class="sxs-lookup"><span data-stu-id="4841f-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="4841f-137">Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.</span><span class="sxs-lookup"><span data-stu-id="4841f-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="4841f-138">Valitse **Mukauta**.</span><span class="sxs-lookup"><span data-stu-id="4841f-138">Click **Customize**.</span></span>

    <span data-ttu-id="4841f-139">[![Mukautus - Välilehden ohjausvalintaikkuna](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="4841f-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="4841f-140">Valitse **Uusi välilehti**.</span><span class="sxs-lookup"><span data-stu-id="4841f-140">Click **New tab**.</span></span>
4. <span data-ttu-id="4841f-141">Etsi juuri lisäämäsi uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="4841f-141">Find the new tab that you just added.</span></span> <span data-ttu-id="4841f-142">Näyttöä on ehkä vieritettävä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="4841f-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="4841f-143">Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="4841f-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="4841f-144">[![Suositeltujen tuotteiden valinta Sisältö-valikossa](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="4841f-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="4841f-145">Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi Suositellut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="4841f-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="4841f-146">Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.</span><span class="sxs-lookup"><span data-stu-id="4841f-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="4841f-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4841f-147">Click **OK**.</span></span> <span data-ttu-id="4841f-148">Painikeruudukkoon tulee uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="4841f-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="4841f-149">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="4841f-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="4841f-150">Valitse Commercessa **Retail ja Commerce** &gt; **Retail ja Commerce IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="4841f-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="4841f-151">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="4841f-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="4841f-152">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="4841f-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4841f-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4841f-153">Additional resources</span></span>

[<span data-ttu-id="4841f-154">Tuotesuositukset myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4841f-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4841f-155">Tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4841f-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)