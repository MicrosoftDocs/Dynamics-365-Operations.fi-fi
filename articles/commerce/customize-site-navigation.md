---
title: Sivuston selauksen mukauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan mukautettu online-siirtymishierarkia, jonka avulla tuotteita voidaan järjestellä Microsoft Dynamics 365 Commerce -sivuston selaamista varten.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2235510c7ef386d66fe3b137f8e791d14706379
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001826"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="f202f-103">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="f202f-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f202f-104">Tässä ohjeaiheessa kerrotaan, miten luodaan mukautettu online-siirtymishierarkia, jonka avulla tuotteita voidaan järjestellä Microsoft Dynamics 365 Commerce -sivuston selaamista varten.</span><span class="sxs-lookup"><span data-stu-id="f202f-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="f202f-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f202f-105">Overview</span></span>

<span data-ttu-id="f202f-106">Verkkomyymälöissä asiakkaat yleensä voivat etsiä ja selata tuotteita siirtymällä tuoteluokissa.</span><span class="sxs-lookup"><span data-stu-id="f202f-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="f202f-107">Tätä ominaisuutta käytetään yleensä sivun yläosassa olevien välilehtien tai vasemmalla olevan siirtymispalkin avulla.</span><span class="sxs-lookup"><span data-stu-id="f202f-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="f202f-108">Dynamics 365 Commerce -sovelluksessa voit luoda luokan siirtymisen ja eri luokkien tuotteiden hierarkiarakenteen ja hallita sitä.</span><span class="sxs-lookup"><span data-stu-id="f202f-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="f202f-109">Luo kanavan siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="f202f-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="f202f-110">Voit luoda kanavan siirtymishierarkian seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f202f-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f202f-111">Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Luokka- ja tuotehallinta**.</span><span class="sxs-lookup"><span data-stu-id="f202f-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="f202f-112">Valitse **Luokan hierarkiat** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f202f-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="f202f-113">Anna hierarkialle nimi.</span><span class="sxs-lookup"><span data-stu-id="f202f-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f202f-114">Luotu ylin luokka on luokan juurisolmu.</span><span class="sxs-lookup"><span data-stu-id="f202f-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="f202f-115">Se ei näy sivustossa.</span><span class="sxs-lookup"><span data-stu-id="f202f-115">It won't be shown on your site.</span></span> <span data-ttu-id="f202f-116">Jos haluat luoda luokkahierarkian, jossa yksi ylätason solmu näkyy sivustossa, luo luokka ja nimeä se juuriluokan alitasoksi.</span><span class="sxs-lookup"><span data-stu-id="f202f-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="f202f-117">Valitse **Uusi luokka solmu** ja anna luokan nimi.</span><span class="sxs-lookup"><span data-stu-id="f202f-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="f202f-118">Jatka rinnakkais- ja alitasojen luomista halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="f202f-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="f202f-119">Voit nyt määrittää tuotteita kuhunkin ylätason luokkaan luotuun luokkaan.</span><span class="sxs-lookup"><span data-stu-id="f202f-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="f202f-120">Luokkien järjestyksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="f202f-120">Customize the order of categories</span></span>

<span data-ttu-id="f202f-121">Oletusarvoisesti määrittämäsi luokat näkyvät sivustossa aakkosjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="f202f-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="f202f-122">Voit kuitenkin mukauttaa luokkien näyttöjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="f202f-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="f202f-123">Määritä luokkahierarkiatyyppi</span><span class="sxs-lookup"><span data-stu-id="f202f-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="f202f-124">Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Luokka- ja tuotehallinta**.</span><span class="sxs-lookup"><span data-stu-id="f202f-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="f202f-125">Valitse **Luokkahierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="f202f-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="f202f-126">Valitse toimintoruudun **Luokkahierakia**-välilehden **Määritys**-ryhmässä **Liitä hierarkiatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="f202f-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="f202f-127">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f202f-127">Select **New**.</span></span>
1. <span data-ttu-id="f202f-128">Valitse **Luokkahierarkian tyyppi** -kentässä **Kanavan siirtymishierarkia**.</span><span class="sxs-lookup"><span data-stu-id="f202f-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="f202f-129">Valitse **Luokkahierarkia**-kentässä aiemmin valittu kanavan siirtymishierarkia.</span><span class="sxs-lookup"><span data-stu-id="f202f-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="f202f-130">Uusien tai päivitettyjen siirtymishierarkioiden julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="f202f-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="f202f-131">Voit määrittää siirtymishierarkian käyttöön verkkomyymälässä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f202f-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="f202f-132">Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.</span><span class="sxs-lookup"><span data-stu-id="f202f-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="f202f-133">Valitse vasemmanpuoleisesta puusta verkkomyymälä.</span><span class="sxs-lookup"><span data-stu-id="f202f-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="f202f-134">Valitse **Julkaise kanavan päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="f202f-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="f202f-135">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="f202f-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="f202f-136">Etsi luettelosta **Työ 1040** ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f202f-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="f202f-137">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="f202f-137">Select **Run now**.</span></span>
1. <span data-ttu-id="f202f-138">Toista vaiheet 5 ja 6 töille 1070 ja 1150.</span><span class="sxs-lookup"><span data-stu-id="f202f-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="f202f-139">Luokkien näyttäminen sivustossa</span><span class="sxs-lookup"><span data-stu-id="f202f-139">Show categories on your site</span></span>

<span data-ttu-id="f202f-140">Jos haluat näyttää luokkahierarkian verkkomyymälässä, lisää siirtymisvalikkomoduuli sopivaan sijaintiin mallissa tai osassa.</span><span class="sxs-lookup"><span data-stu-id="f202f-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="f202f-141">Tämä siirtymisvalikkomoduuli näyttää nyt siirtymishierarkian, jos olet julkaissut siirtymishierarkian kanavassa, johon sivusto on sidottu.</span><span class="sxs-lookup"><span data-stu-id="f202f-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="f202f-142">Myymälän aloituspakettiin sisältyvän siirtymisvalikkomoduulin avulla käyttäjät voivat siirtyä vain luokissa, joissa ei ole aliluokkia.</span><span class="sxs-lookup"><span data-stu-id="f202f-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="f202f-143">Jos asiakkaiden on voivat siirtyä luokissa, joissa on aliluokkia, mukauta siirtymisvalikkomoduulia.</span><span class="sxs-lookup"><span data-stu-id="f202f-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="f202f-144">Mukautettujen siirtymisvaihtoehtojen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f202f-144">Add custom navigation options</span></span>

<span data-ttu-id="f202f-145">Siirtymisvalikossa voit lisätä siirtymisvaihtoehtoja, jotka eivät ole tuoteluokkahierarkian osa.</span><span class="sxs-lookup"><span data-stu-id="f202f-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="f202f-146">Esimerkiksi tuoteluokkaluettelon loppuun voit lisätä **Ota yhteyttä** -nimikkeen, joka vie sivustolle luodulle yhteydenottosivulle.</span><span class="sxs-lookup"><span data-stu-id="f202f-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="f202f-147">Voit lisätä siirtymisvalikkoon mukautettuja siirtymisvaihtoehtoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f202f-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="f202f-148">Valitse mukautettavassa mallissa tai osassa siirtymisvalikkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="f202f-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="f202f-149">Valitse ominaisuusruudun **Tiedot**-välilehdessä **Lisää nimike**, jos haluat luoda uuden sisällönhallintajärjestelmän (CMS) siirtymisnimikkeen.</span><span class="sxs-lookup"><span data-stu-id="f202f-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="f202f-150">Anna linkin teksti ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f202f-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="f202f-151">Toista vaiheet 2 ja 3 ja lisää mukautettuja siirtymisvaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="f202f-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="f202f-152">Kun olet valmis, tallenna malli tai osa ja kuittaa se sisään.</span><span class="sxs-lookup"><span data-stu-id="f202f-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f202f-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f202f-153">Additional resources</span></span>

[<span data-ttu-id="f202f-154">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f202f-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f202f-155">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="f202f-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f202f-156">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="f202f-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="f202f-157">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f202f-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f202f-158">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f202f-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="f202f-159">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="f202f-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="f202f-160">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="f202f-160">Work with publish groups</span></span>](publish-groups.md)
