---
title: Sivuston selauksen mukauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten luodaan mukautettu online-siirtymishierarkia, jonka avulla tuotteita voidaan järjestellä Microsoft Dynamics 365 Commerce -sivuston selaamista varten.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799346"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="6f445-103">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="6f445-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f445-104">Tässä ohjeaiheessa kerrotaan, miten luodaan mukautettu online-siirtymishierarkia, jonka avulla tuotteita voidaan järjestellä Microsoft Dynamics 365 Commerce -sivuston selaamista varten.</span><span class="sxs-lookup"><span data-stu-id="6f445-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="6f445-105">Verkkomyymälöissä asiakkaat yleensä voivat etsiä ja selata tuotteita siirtymällä tuoteluokissa.</span><span class="sxs-lookup"><span data-stu-id="6f445-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="6f445-106">Tätä ominaisuutta käytetään yleensä sivun yläosassa olevien välilehtien tai vasemmalla olevan siirtymispalkin avulla.</span><span class="sxs-lookup"><span data-stu-id="6f445-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="6f445-107">Dynamics 365 Commerce -sovelluksessa voit luoda luokan siirtymisen ja eri luokkien tuotteiden hierarkiarakenteen ja hallita sitä.</span><span class="sxs-lookup"><span data-stu-id="6f445-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="6f445-108">Luo kanavan siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="6f445-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="6f445-109">Voit luoda kanavan siirtymishierarkian seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6f445-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="6f445-110">Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Luokka- ja tuotehallinta**.</span><span class="sxs-lookup"><span data-stu-id="6f445-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="6f445-111">Valitse **Luokan hierarkiat** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6f445-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="6f445-112">Anna hierarkialle nimi.</span><span class="sxs-lookup"><span data-stu-id="6f445-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f445-113">Luotu ylin luokka on luokan juurisolmu.</span><span class="sxs-lookup"><span data-stu-id="6f445-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="6f445-114">Se ei näy sivustossa.</span><span class="sxs-lookup"><span data-stu-id="6f445-114">It won't be shown on your site.</span></span> <span data-ttu-id="6f445-115">Jos haluat luoda luokkahierarkian, jossa yksi ylätason solmu näkyy sivustossa, luo luokka ja nimeä se juuriluokan alitasoksi.</span><span class="sxs-lookup"><span data-stu-id="6f445-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="6f445-116">Valitse **Uusi luokka solmu** ja anna luokan nimi.</span><span class="sxs-lookup"><span data-stu-id="6f445-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="6f445-117">Jatka rinnakkais- ja alitasojen luomista halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6f445-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="6f445-118">Voit nyt määrittää tuotteita kuhunkin ylätason luokkaan luotuun luokkaan.</span><span class="sxs-lookup"><span data-stu-id="6f445-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="6f445-119">Luokkien järjestyksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="6f445-119">Customize the order of categories</span></span>

<span data-ttu-id="6f445-120">Oletusarvoisesti määrittämäsi luokat näkyvät sivustossa aakkosjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="6f445-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="6f445-121">Voit kuitenkin mukauttaa luokkien näyttöjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="6f445-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="6f445-122">Määritä luokkahierarkiatyyppi</span><span class="sxs-lookup"><span data-stu-id="6f445-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="6f445-123">Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Luokka- ja tuotehallinta**.</span><span class="sxs-lookup"><span data-stu-id="6f445-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="6f445-124">Valitse **Luokkahierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="6f445-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="6f445-125">Valitse toimintoruudun **Luokkahierakia**-välilehden **Määritys**-ryhmässä **Liitä hierarkiatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="6f445-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="6f445-126">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6f445-126">Select **New**.</span></span>
1. <span data-ttu-id="6f445-127">Valitse **Luokkahierarkian tyyppi** -kentässä **Kanavan siirtymishierarkia**.</span><span class="sxs-lookup"><span data-stu-id="6f445-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="6f445-128">Valitse **Luokkahierarkia**-kentässä aiemmin valittu kanavan siirtymishierarkia.</span><span class="sxs-lookup"><span data-stu-id="6f445-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="6f445-129">Uusien tai päivitettyjen siirtymishierarkioiden julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="6f445-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="6f445-130">Voit määrittää siirtymishierarkian käyttöön verkkomyymälässä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6f445-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="6f445-131">Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.</span><span class="sxs-lookup"><span data-stu-id="6f445-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="6f445-132">Valitse vasemmanpuoleisesta puusta verkkomyymälä.</span><span class="sxs-lookup"><span data-stu-id="6f445-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="6f445-133">Valitse **Julkaise kanavan päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="6f445-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="6f445-134">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="6f445-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="6f445-135">Etsi luettelosta **Työ 1040** ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6f445-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="6f445-136">Valitse **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="6f445-136">Select **Run now**.</span></span>
1. <span data-ttu-id="6f445-137">Toista vaiheet 5 ja 6 töille 1070 ja 1150.</span><span class="sxs-lookup"><span data-stu-id="6f445-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="6f445-138">Luokkien näyttäminen sivustossa</span><span class="sxs-lookup"><span data-stu-id="6f445-138">Show categories on your site</span></span>

<span data-ttu-id="6f445-139">Jos haluat näyttää luokkahierarkian verkkomyymälässä, lisää siirtymisvalikkomoduuli sopivaan sijaintiin mallissa tai osassa.</span><span class="sxs-lookup"><span data-stu-id="6f445-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="6f445-140">Tämä siirtymisvalikkomoduuli näyttää nyt siirtymishierarkian, jos olet julkaissut siirtymishierarkian kanavassa, johon sivusto on sidottu.</span><span class="sxs-lookup"><span data-stu-id="6f445-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="6f445-141">Myymälän moduulikirjastoon sisältyvän siirtymisvalikkomoduulin avulla käyttäjät voivat siirtyä vain luokissa, joissa ei ole aliluokkia.</span><span class="sxs-lookup"><span data-stu-id="6f445-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="6f445-142">Jos asiakkaiden on voivat siirtyä luokissa, joissa on aliluokkia, mukauta siirtymisvalikkomoduulia.</span><span class="sxs-lookup"><span data-stu-id="6f445-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="6f445-143">Mukautettujen siirtymisvaihtoehtojen lisääminen</span><span class="sxs-lookup"><span data-stu-id="6f445-143">Add custom navigation options</span></span>

<span data-ttu-id="6f445-144">Siirtymisvalikossa voit lisätä siirtymisvaihtoehtoja, jotka eivät ole tuoteluokkahierarkian osa.</span><span class="sxs-lookup"><span data-stu-id="6f445-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="6f445-145">Esimerkiksi tuoteluokkaluettelon loppuun voit lisätä **Ota yhteyttä** -nimikkeen, joka vie sivustolle luodulle yhteydenottosivulle.</span><span class="sxs-lookup"><span data-stu-id="6f445-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="6f445-146">Voit lisätä siirtymisvalikkoon mukautettuja siirtymisvaihtoehtoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6f445-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="6f445-147">Valitse mukautettavassa mallissa tai osassa siirtymisvalikkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="6f445-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="6f445-148">Valitse ominaisuusruudun **Tiedot**-välilehdessä **Lisää nimike**, jos haluat luoda uuden sisällönhallintajärjestelmän (CMS) siirtymisnimikkeen.</span><span class="sxs-lookup"><span data-stu-id="6f445-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="6f445-149">Anna linkin teksti ja URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="6f445-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="6f445-150">Toista vaiheet 2 ja 3 ja lisää mukautettuja siirtymisvaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="6f445-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="6f445-151">Kun olet valmis, tallenna malli tai osa valitsemalla **Tallenna** ja tarkista se sitten valitsemalla **Viimeistele muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="6f445-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f445-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6f445-152">Additional resources</span></span>

[<span data-ttu-id="6f445-153">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6f445-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="6f445-154">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="6f445-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="6f445-155">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="6f445-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="6f445-156">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6f445-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="6f445-157">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="6f445-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="6f445-158">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="6f445-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="6f445-159">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="6f445-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
