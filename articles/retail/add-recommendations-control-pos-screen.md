---
title: Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle
description: Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606846"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="9c36f-103">Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle</span><span class="sxs-lookup"><span data-stu-id="9c36f-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9c36f-104">Tuotesuosituspalvelun nykyinen versio ollaan poistamassa, sillä toiminto suunnitellaan uudelleen käyttämällä parempaa algoritmia ja uudempia vähittäismyyntiin soveltuvia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="9c36f-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="9c36f-105">Lisätietoja on kohdassa [Poistetut tai vanhentuneet ominaisuudet](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="9c36f-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="9c36f-106">Tässä ohjeaiheessa kuvataan suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumanäytölle käyttämällä Microsoft Dynamics 365 for Retailin näytön asettelun suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="9c36f-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="9c36f-107">Voit näyttää tuotesuosituksia myyntipisteen laitteessa, kun käytät Microsoft Dynamics 365 for Retailia.</span><span class="sxs-lookup"><span data-stu-id="9c36f-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="9c36f-108">*Suositukset* ovat nimikkeitä, joista asiakas on mahdollisesti kiinnostunut ostohistorian, toiveluettelon ja muiden asiakkaiden verkosta tai kivijalkakaupasta ostamien tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="9c36f-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="9c36f-109">Voit näyttää tuotteen suosituksi lisäämällä ohjausobjektin tapahtumanäytölle näytön asettelun suunnittelutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="9c36f-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="9c36f-110">Avaa asettelun suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="9c36f-110">Open Layout designer</span></span>

1. <span data-ttu-id="9c36f-111">Siirry kohtaan **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="9c36f-112">Pikasuodattimen avulla voit etsiä näyttöä, johon haluat lisätä ohjausobjektin.</span><span class="sxs-lookup"><span data-stu-id="9c36f-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="9c36f-113">Voit esimerkiksi suodattaa **Näyttöasettelun tunnus** -kentässä arvolla **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-113">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="9c36f-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c36f-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="9c36f-115">Valitse esimerkiksi **Nimi: F2CP16:9M Näyttöasettelun tunnus: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-115">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="9c36f-116">Valitse **Asettelun suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="9c36f-117">Noudata kehotteita asettelun suunnittelutoiminnon käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="9c36f-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="9c36f-118">Tunnistetietoja kysyttäessä anna samat tunnistetiedot, jotka olivat käytössä, kun asettelun suunnittelutoiminto käynnistettiin **Näytön asettelut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="9c36f-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="9c36f-119">Kun kirjaudut, tulee sivu, joka on samanlainen kuin alla oleva.</span><span class="sxs-lookup"><span data-stu-id="9c36f-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="9c36f-120">Asettelu on erilainen riippuen oman myymälän tekemistä mukautuksista.</span><span class="sxs-lookup"><span data-stu-id="9c36f-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="9c36f-121">[![Asettelun suunnittelutoiminto](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="9c36f-121">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="9c36f-122">Näyttöasetuksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="9c36f-122">Choose a display option</span></span>

<span data-ttu-id="9c36f-123">Käytettävissä on kaksi asetusta.</span><span class="sxs-lookup"><span data-stu-id="9c36f-123">There are two configurations options available.</span></span> <span data-ttu-id="9c36f-124">Valitse vaihtoehto, joka sopii parhaiten myymälällesi ja noudata ohjeita loppuun viimeistelläksesi ohjausobjektin määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="9c36f-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="9c36f-125">Asetukset ovat:</span><span class="sxs-lookup"><span data-stu-id="9c36f-125">The two options are:</span></span>

- <span data-ttu-id="9c36f-126">Suositukset ovat aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="9c36f-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="9c36f-127">A **Suositukset**-välilehti näkyy oikealla puolella näytön ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="9c36f-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="9c36f-128">Suositusten tuominen aina näkyviin</span><span class="sxs-lookup"><span data-stu-id="9c36f-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="9c36f-129">Pienennä tapahtumarivien tiedot -alueen korkeutta niin, että se on samalla korkeudella kuin asiakaspaneeli vasemmalla puolellaan.</span><span class="sxs-lookup"><span data-stu-id="9c36f-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="9c36f-130">[![Tapahtumarivien erittelyalueen korkeutta vähennetty](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="9c36f-130">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="9c36f-131">Vasemmanpuoleisesta valikosta vedä ja pudota suosituksien ohjausobjekti Tapahtumarivin tiedot -alueen ja painikeruudukon väliin näytön alareunassa keskellä.</span><span class="sxs-lookup"><span data-stu-id="9c36f-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="9c36f-132">Muuta ohjausobjektin kokoa, jotta se mahtuu kyseiseen tilaan.</span><span class="sxs-lookup"><span data-stu-id="9c36f-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="9c36f-133">[![Suositusten ohjaus lisätty asetteluun](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="9c36f-133">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="9c36f-134">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="9c36f-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="9c36f-135">Valitse Dynamics 365 for Retailissa **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="9c36f-136">Valitse luettelossa  **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="9c36f-137">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="9c36f-138">Suositukset-välilehden lisääminen painikeruudukkoon näytön oikealla puolella</span><span class="sxs-lookup"><span data-stu-id="9c36f-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="9c36f-139">Napsauta hiiren kakkospainikkeella tyhjää tilaa sivun oikeassa reunassa painikeruudukon viimeisen välilehden alapuolella.</span><span class="sxs-lookup"><span data-stu-id="9c36f-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="9c36f-140">Valitse **Mukauta**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-140">Click **Customize**.</span></span>

    <span data-ttu-id="9c36f-141">[![Mukautus - Välilehden ohjausvalintaikkuna](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="9c36f-141">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="9c36f-142">Valitse **Uusi välilehti**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-142">Click **New tab**.</span></span>
4. <span data-ttu-id="9c36f-143">Etsi juuri lisäämäsi uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="9c36f-143">Find the new tab that you just added.</span></span> <span data-ttu-id="9c36f-144">Näyttöä on ehkä vieritettävä alaspäin.</span><span class="sxs-lookup"><span data-stu-id="9c36f-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="9c36f-145">Valitse avattavassa **Sisältö**-valikossa **Suositellut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="9c36f-146">[![Suositeltujen tuotteiden valinta Sisältö-valikossa](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="9c36f-146">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="9c36f-147">Kirjoita **Otsikko**-kenttään suositusten välilehden nimi. Kirjoita esimerkiksi Suositellut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="9c36f-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="9c36f-148">Valitse **Kuva**-kentässä välilehdessä näytettävä kuva.</span><span class="sxs-lookup"><span data-stu-id="9c36f-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="9c36f-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-149">Click **OK**.</span></span> <span data-ttu-id="9c36f-150">Painikeruudukkoon tulee uusi välilehti.</span><span class="sxs-lookup"><span data-stu-id="9c36f-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="9c36f-151">Valitse **X**, jotta tallennat ja poistut asettelun suunnittelutoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="9c36f-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="9c36f-152">Valitse Dynamics 365 for Retailissa **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulut**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="9c36f-153">Valitse luettelossa  **1090, kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="9c36f-154">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="9c36f-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c36f-155">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9c36f-155">Additional resources</span></span>

[<span data-ttu-id="9c36f-156">Mukautettujen tuotesuositusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9c36f-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
