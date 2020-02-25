---
title: Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus
description: Tässä ohjeaiheessa on luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 17746d2923ab84311253c47647c0020807bdb75c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002493"
---
# <a name="overview-of-default-category-landing-page-and-search-results-page"></a><span data-ttu-id="d075f-103">Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d075f-103">Overview of default category landing page and search results page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d075f-104">Tässä ohjeaiheessa on luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus Microsoft Dynamics 365 Commercen sähköisessä kaupankäynnissä.</span><span class="sxs-lookup"><span data-stu-id="d075f-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="d075f-105">Luokan oletussaapumissivu</span><span class="sxs-lookup"><span data-stu-id="d075f-105">Default category landing page</span></span>

<span data-ttu-id="d075f-106">Luokan oletussaapumissivu on sivu, jolle sivustojen käyttäjät yleensä siirretään, kun he valitsevat siirtymishierarkiassa luokan.</span><span class="sxs-lookup"><span data-stu-id="d075f-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="d075f-107">Luokka-sivulla voit selata ja myös lajitella ja tarkentaa luokiteltuja tuotteita.</span><span class="sxs-lookup"><span data-stu-id="d075f-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Luokan oletussaapumissivu](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="d075f-109">Sivun yläosassa on ylätunniste, jossa näkyvät kaikki tuoteluokat ja muut sivut, jotka myynninedistämispäällikkö on luokitellut.</span><span class="sxs-lookup"><span data-stu-id="d075f-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="d075f-110">Määritys tehdään kanavan siirtymishierarkian määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="d075f-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="d075f-111">Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin ostajaa mahdollisesti kiinnostaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="d075f-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="d075f-112">Seuraavat komponentit ovat olennaisia luokassa:</span><span class="sxs-lookup"><span data-stu-id="d075f-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="d075f-113">**Tuotesijoitteluruudut** näyttävät tuotteet, jotka myynninedistämispäällikkö on määrittänyt luokkaan siirtymishierarkian määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="d075f-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="d075f-114">**Tarkennusten ja valinnan yhteenveto** ovat suodattimia määriä varten. Niiden avulla voi myös tarkentaa nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="d075f-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="d075f-115">Myynninedistämispäällikkö määrittää ne osana kanavaluokkiin ja tuotemääritteisiin liittyvien metatietojen määritystä.</span><span class="sxs-lookup"><span data-stu-id="d075f-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="d075f-116">**Lajitteluasetusten** avulla sivuston vierailijat voivat lajitella tuotteet.</span><span class="sxs-lookup"><span data-stu-id="d075f-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="d075f-117">Oletusarvoisesti käytettävissä ovat seuraavat lajitteluvaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="d075f-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="d075f-118">Hinta – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="d075f-118">Price – low to high</span></span>
    - <span data-ttu-id="d075f-119">Hinta – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="d075f-119">Price – high to low</span></span>
    - <span data-ttu-id="d075f-120">Tuotteen nimi – \[A-Ö\]</span><span class="sxs-lookup"><span data-stu-id="d075f-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="d075f-121">Tuotteen nimi – \[Ö-A\]</span><span class="sxs-lookup"><span data-stu-id="d075f-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="d075f-122">Luokitukset – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="d075f-122">Ratings – low to high</span></span>
    - <span data-ttu-id="d075f-123">Luokitukset – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="d075f-123">Ratings – high to low</span></span>

- <span data-ttu-id="d075f-124">**Sivutuksen** avulla sivuston vierailijat voivat siirtyä yhdeltä luokitellun tuotteen sivulta toiselle.</span><span class="sxs-lookup"><span data-stu-id="d075f-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="d075f-125">**Kokonaismäärä** määrittää luokkaan määritettyjen tuotteiden kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="d075f-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="d075f-126">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="d075f-126">Enrich a category landing page</span></span>

<span data-ttu-id="d075f-127">Jos haluat, että luokan saapumissivun tietyllä luokalla on paljon räätälöityä kokemusta, voit täydentää kyseisen luokan saapumissivua.</span><span class="sxs-lookup"><span data-stu-id="d075f-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="d075f-128">Voit esimerkiksi lisätä markkinointivideon ja joitakin luokan tarinoita, joiden avulla saat ostajan huomion.</span><span class="sxs-lookup"><span data-stu-id="d075f-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="d075f-129">Lisätietoja on kohdassa [Luokan saapumissivun täydentäminen](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="d075f-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="d075f-131">Automaattisten ehdotusten ja hakutulosten sivut</span><span class="sxs-lookup"><span data-stu-id="d075f-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="d075f-132">Sivuston käyttäjät voivat selata sivustoa siirtymishierarkian luokan avulla tai syöttämällä hakutermin hakukenttään.</span><span class="sxs-lookup"><span data-stu-id="d075f-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="d075f-133">Heti, kun käyttäjät alkavat kirjoittaa tekstiä hakukenttään, he näkevät automaattisen ehdotustoiminnon, joka ehdottaa hakutermejä.</span><span class="sxs-lookup"><span data-stu-id="d075f-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="d075f-134">Seuraavassa on joitakin ehdotuksia, jotka saattavat tulla näkyviin:</span><span class="sxs-lookup"><span data-stu-id="d075f-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="d075f-135">**Avainsanoja** käytetään etsittäessä nimikkeitä kaikista kanavan tuotteista.</span><span class="sxs-lookup"><span data-stu-id="d075f-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="d075f-136">**Tuotteet** sisältävät suorat linkit tuotetietosivulle.</span><span class="sxs-lookup"><span data-stu-id="d075f-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="d075f-137">**Luokkahakualueen ehdotukset** tuovat näyttöön eri luokkia. Niiden avulla käyttäjät voivat hakea tietyn luokan avainsanoja.</span><span class="sxs-lookup"><span data-stu-id="d075f-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Mukaansatempaava automaattinen ehdotustoiminto](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="d075f-139">Kun käyttäjät valitsevat jonkin avainsanan tai luokkahakualueen ehdotukset tai kun hakutermillä ei saada ehdotuksia, käyttäjät siirretään hakutulossivulle.</span><span class="sxs-lookup"><span data-stu-id="d075f-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="d075f-140">Käyttäjät voivat tämän jälkeen selata, lajitella ja tarkentaa hakutulosluetteloa löytääksesi haluamasi nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="d075f-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Aloitussivu](./media/SearchLanding.png)

<span data-ttu-id="d075f-142">Seuraavat osat ovat olennaisia hakutulossivulla:</span><span class="sxs-lookup"><span data-stu-id="d075f-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="d075f-143">**Tuotesijoitteluruudut** näyttävät käyttäjän haun tuotteet.</span><span class="sxs-lookup"><span data-stu-id="d075f-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="d075f-144">Oletusarvoisesti nämä ruudut lajitellaan pilvipohjaisen hakurelevanssin pisteiden mukaan käyttäjähaussa.</span><span class="sxs-lookup"><span data-stu-id="d075f-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="d075f-145">**Tarkennusten ja valinnan yhteenveto** ovat suodattimia määriä varten. Niiden avulla voi myös tarkentaa nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="d075f-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="d075f-146">Myynninedistämispäällikkö määrittää ne osana kanavaluokkien ja tuotemääritteiden metatietojen määritystä.</span><span class="sxs-lookup"><span data-stu-id="d075f-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="d075f-147">**Lajitteluasetusten** avulla sivuston vierailijat voivat lajitella tuotteet.</span><span class="sxs-lookup"><span data-stu-id="d075f-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="d075f-148">Oletusarvoisesti käytettävissä ovat seuraavat lajitteluvaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="d075f-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="d075f-149">Hinta – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="d075f-149">Price – low to high</span></span>
    - <span data-ttu-id="d075f-150">Hinta – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="d075f-150">Price – high to low</span></span>
    - <span data-ttu-id="d075f-151">Tuotteen nimi – \[A-Ö\]</span><span class="sxs-lookup"><span data-stu-id="d075f-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="d075f-152">Tuotteen nimi – \[Ö-A\]</span><span class="sxs-lookup"><span data-stu-id="d075f-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="d075f-153">Luokitukset – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="d075f-153">Ratings – low to high</span></span>
    - <span data-ttu-id="d075f-154">Luokitukset – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="d075f-154">Ratings – high to low</span></span>
    - <span data-ttu-id="d075f-155">Oletus</span><span class="sxs-lookup"><span data-stu-id="d075f-155">Default</span></span>

- <span data-ttu-id="d075f-156">**Sivutuksen** avulla sivuston vierailijat voivat siirtyä yhdeltä luokitellun tuotteen sivulta toiselle.</span><span class="sxs-lookup"><span data-stu-id="d075f-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="d075f-157">**Kokonaismäärä** määrittää luokkaan määritettyjen ja hakuehtoja vastaavien tuotteiden kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="d075f-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d075f-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d075f-158">Additional resources</span></span>

[<span data-ttu-id="d075f-159">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d075f-159">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="d075f-160">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d075f-160">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="d075f-161">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d075f-161">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="d075f-162">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d075f-162">Overview of account management pages</span></span>](quick-tour-account-management.md)

