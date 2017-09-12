---
title: "Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle"
description: "Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 7f8522110c0d7d5277b0b3f3c7b21d8605d43f2c
ms.contentlocale: fi-fi
ms.lasthandoff: 06/29/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="aaa77-103">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumasivulle</span><span class="sxs-lookup"><span data-stu-id="aaa77-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="aaa77-104">Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="aaa77-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="aaa77-105">Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Microsoft Dynamics 365 for Retailia.</span><span class="sxs-lookup"><span data-stu-id="aaa77-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="aaa77-106">*Suositukset* ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="aaa77-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="aaa77-107">Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="aaa77-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="aaa77-108">Avaa asettelun suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="aaa77-108">Open Layout designer</span></span>
1.  <span data-ttu-id="aaa77-109">Siirry kohtaan **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="aaa77-110">Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="aaa77-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="aaa77-111">Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla "F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="aaa77-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="aaa77-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="aaa77-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="aaa77-113">Valitse esimerkiksi "Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="aaa77-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="aaa77-114">Valitse **Asettelun suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="aaa77-115">Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="aaa77-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="aaa77-116">Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aaa77-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="aaa77-117">Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva.</span><span class="sxs-lookup"><span data-stu-id="aaa77-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="aaa77-118">Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.</span><span class="sxs-lookup"><span data-stu-id="aaa77-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="aaa77-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Valitse näyttöasetus</span><span class="sxs-lookup"><span data-stu-id="aaa77-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="aaa77-120">Käytettävissä on kaksi asetusta.</span><span class="sxs-lookup"><span data-stu-id="aaa77-120">There are two configurations options available.</span></span> <span data-ttu-id="aaa77-121">Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="aaa77-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="aaa77-122">Asetukset ovat:</span><span class="sxs-lookup"><span data-stu-id="aaa77-122">The two options are:</span></span>
-   <span data-ttu-id="aaa77-123">Suositukset ovat aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="aaa77-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="aaa77-124">A **Suositukset**-välilehti näkyy oikealla puolella näytön ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="aaa77-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="aaa77-125">Saat suositukset aina näkyville:</span><span class="sxs-lookup"><span data-stu-id="aaa77-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="aaa77-126">Pienennä tapahtumarivien tiedot -alueen korkeutta niin, että se on samalla korkeudella kuin asiakaspaneeli vasemmalla puolellaan. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="aaa77-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="aaa77-127">Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä.</span><span class="sxs-lookup"><span data-stu-id="aaa77-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="aaa77-128">Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="aaa77-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="aaa77-129">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="aaa77-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="aaa77-130">Siirry Dynamics 365 for Retailissa kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="aaa77-131">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="aaa77-132">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="aaa77-133">Lisää Suositukset-välilehti painikeruudukkoon näytön oikealla puolella seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aaa77-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="aaa77-134">Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.</span><span class="sxs-lookup"><span data-stu-id="aaa77-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="aaa77-135">Valitse **Mukauta**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="aaa77-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="aaa77-136">Valitse **Uusi välilehti**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="aaa77-137">Etsi juuri lisäämäsi uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="aaa77-137">Find the new tab that you just added.</span></span> <span data-ttu-id="aaa77-138">Saatat joutua vierittämään näyttöä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="aaa77-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="aaa77-139">Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="aaa77-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="aaa77-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="aaa77-141">Kirjoita **Otsikko**-kenttään suositusten välilehden nimi.</span><span class="sxs-lookup"><span data-stu-id="aaa77-141">In the **Label** field, type a name for the recommendations tab.</span></span> <span data-ttu-id="aaa77-142">Kirjoita esimerkiksi 'Suositellut tuotteet'.</span><span class="sxs-lookup"><span data-stu-id="aaa77-142">For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="aaa77-143">Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.</span><span class="sxs-lookup"><span data-stu-id="aaa77-143">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="aaa77-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-144">Click **OK**.</span></span> <span data-ttu-id="aaa77-145">Painikeruudukkoon tulee uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="aaa77-145">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="aaa77-146">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="aaa77-146">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="aaa77-147">Siirry Dynamics 365 for Retailissa kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-147">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="aaa77-148">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-148">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="aaa77-149">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="aaa77-149">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="aaa77-150">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="aaa77-150">See also</span></span>
--------

[<span data-ttu-id="aaa77-151">Mukautettujen tuotesuositusten yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="aaa77-151">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




