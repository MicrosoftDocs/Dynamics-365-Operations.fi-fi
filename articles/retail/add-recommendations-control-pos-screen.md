---
title: "Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle"
description: "Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 26b03b6712c97b12e1221598de308813c7986179
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="09bfa-103">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle</span><span class="sxs-lookup"><span data-stu-id="09bfa-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="09bfa-104">Tuotesuosituspalvelun nykyinen versio ollaan poistamassa, sillä toiminto suunnitellaan uudelleen käyttämällä parempaa algoritmia ja uudempia vähittäismyyntiin soveltuvia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="09bfa-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="09bfa-105">Lisätietoja on kohdassa [Poistetut tai vanhentuneet ominaisuudet](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="09bfa-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="09bfa-106">Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="09bfa-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="09bfa-107">Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Microsoft Dynamics 365 for Retailia.</span><span class="sxs-lookup"><span data-stu-id="09bfa-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="09bfa-108">*Suositukset* ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="09bfa-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="09bfa-109">Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="09bfa-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="09bfa-110">Avaa asettelun suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="09bfa-110">Open Layout designer</span></span>
1.  <span data-ttu-id="09bfa-111">Siirry kohtaan **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="09bfa-112">Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="09bfa-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="09bfa-113">Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla "F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="09bfa-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="09bfa-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="09bfa-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="09bfa-115">Valitse esimerkiksi "Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="09bfa-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="09bfa-116">Valitse **Asettelun suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="09bfa-117">Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="09bfa-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="09bfa-118">Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="09bfa-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="09bfa-119">Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva.</span><span class="sxs-lookup"><span data-stu-id="09bfa-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="09bfa-120">Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.</span><span class="sxs-lookup"><span data-stu-id="09bfa-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="09bfa-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Valitse näyttöasetus</span><span class="sxs-lookup"><span data-stu-id="09bfa-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="09bfa-122">Käytettävissä on kaksi asetusta.</span><span class="sxs-lookup"><span data-stu-id="09bfa-122">There are two configurations options available.</span></span> <span data-ttu-id="09bfa-123">Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="09bfa-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="09bfa-124">Asetukset ovat:</span><span class="sxs-lookup"><span data-stu-id="09bfa-124">The two options are:</span></span>
-   <span data-ttu-id="09bfa-125">Suositukset ovat aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="09bfa-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="09bfa-126">A **Suositukset**-välilehti näkyy oikealla puolella näytön ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="09bfa-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="09bfa-127">Saat suositukset aina näkyville:</span><span class="sxs-lookup"><span data-stu-id="09bfa-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="09bfa-128">Pienennä tapahtumarivien tiedot -alueen korkeutta niin, että se on samalla korkeudella kuin asiakaspaneeli vasemmalla puolellaan. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="09bfa-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="09bfa-129">Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä.</span><span class="sxs-lookup"><span data-stu-id="09bfa-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="09bfa-130">Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="09bfa-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="09bfa-131">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="09bfa-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="09bfa-132">Siirry Dynamics 365 for Retailissa kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="09bfa-133">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="09bfa-134">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="09bfa-135">Lisää Suositukset-välilehti painikeruudukkoon näytön oikealla puolella seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="09bfa-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="09bfa-136">Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.</span><span class="sxs-lookup"><span data-stu-id="09bfa-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="09bfa-137">Valitse **Mukauta**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="09bfa-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="09bfa-138">Valitse **Uusi välilehti**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="09bfa-139">Etsi juuri lisäämäsi uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="09bfa-139">Find the new tab that you just added.</span></span> <span data-ttu-id="09bfa-140">Saatat joutua vierittämään näyttöä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="09bfa-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="09bfa-141">Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="09bfa-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="09bfa-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="09bfa-143">Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi 'Suositellut tuotteet'.</span><span class="sxs-lookup"><span data-stu-id="09bfa-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="09bfa-144">Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.</span><span class="sxs-lookup"><span data-stu-id="09bfa-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="09bfa-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-145">Click **OK**.</span></span> <span data-ttu-id="09bfa-146">Painikeruudukkoon tulee uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="09bfa-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="09bfa-147">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="09bfa-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="09bfa-148">Siirry Dynamics 365 for Retailissa kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="09bfa-149">Valitse luettelossa **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="09bfa-150">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="09bfa-150">Click **Run now**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="09bfa-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="09bfa-151">Additional resources</span></span>
--------

[<span data-ttu-id="09bfa-152">Mukautettujen tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="09bfa-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




