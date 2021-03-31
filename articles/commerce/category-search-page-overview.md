---
title: Luokan oletussaapumissivun ja oletushakutulossivun yleiskatsaus
description: Tässä ohjeaiheessa on luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus Dynamics 365 Commerce -sovelluksessa.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7a40df479bffdc6fdee8f0a7f64fde980cbbdbab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215718"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="64212-103">Luokan oletussaapumissivun ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64212-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64212-104">Tässä ohjeaiheessa on luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus Microsoft Dynamics 365 Commercen sähköisessä kaupankäynnissä.</span><span class="sxs-lookup"><span data-stu-id="64212-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="64212-105">Luokan oletussaapumissivu</span><span class="sxs-lookup"><span data-stu-id="64212-105">Default category landing page</span></span>

<span data-ttu-id="64212-106">Luokan oletussaapumissivu on sivu, jolle sivustojen käyttäjät yleensä siirretään, kun he valitsevat siirtymishierarkiassa luokan.</span><span class="sxs-lookup"><span data-stu-id="64212-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="64212-107">Luokka-sivulla voit selata ja myös lajitella ja tarkentaa luokiteltuja tuotteita.</span><span class="sxs-lookup"><span data-stu-id="64212-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Luokan oletussaapumissivu](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="64212-109">Sivun yläosassa on ylätunniste, jossa näkyvät kaikki tuoteluokat ja muut sivut, jotka myynninedistämispäällikkö on luokitellut.</span><span class="sxs-lookup"><span data-stu-id="64212-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="64212-110">Määritys tehdään kanavan siirtymishierarkian määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="64212-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="64212-111">Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin ostajaa mahdollisesti kiinnostaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="64212-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="64212-112">Seuraavat komponentit ovat olennaisia luokassa:</span><span class="sxs-lookup"><span data-stu-id="64212-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="64212-113">**Tuotesijoitteluruudut** näyttävät tuotteet, jotka myynninedistämispäällikkö on määrittänyt luokkaan siirtymishierarkian määrityksen osana.</span><span class="sxs-lookup"><span data-stu-id="64212-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="64212-114">**Tarkennusten ja valinnan yhteenveto** ovat suodattimia määriä varten. Niiden avulla voi myös tarkentaa nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="64212-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="64212-115">Myynninedistämispäällikkö määrittää ne osana kanavaluokkiin ja tuotemääritteisiin liittyvien metatietojen määritystä.</span><span class="sxs-lookup"><span data-stu-id="64212-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="64212-116">**Lajitteluasetusten** avulla sivuston vierailijat voivat lajitella tuotteet.</span><span class="sxs-lookup"><span data-stu-id="64212-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="64212-117">Oletusarvoisesti käytettävissä ovat seuraavat lajitteluvaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="64212-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="64212-118">Hinta – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="64212-118">Price – low to high</span></span>
    - <span data-ttu-id="64212-119">Hinta – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="64212-119">Price – high to low</span></span>
    - <span data-ttu-id="64212-120">Tuotteen nimi – \[A-Ö\]</span><span class="sxs-lookup"><span data-stu-id="64212-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="64212-121">Tuotteen nimi – \[Ö-A\]</span><span class="sxs-lookup"><span data-stu-id="64212-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="64212-122">Luokitukset – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="64212-122">Ratings – low to high</span></span>
    - <span data-ttu-id="64212-123">Luokitukset – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="64212-123">Ratings – high to low</span></span>

- <span data-ttu-id="64212-124">**Sivutuksen** avulla sivuston vierailijat voivat siirtyä yhdeltä luokitellun tuotteen sivulta toiselle.</span><span class="sxs-lookup"><span data-stu-id="64212-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="64212-125">**Kokonaismäärä** määrittää luokkaan määritettyjen tuotteiden kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="64212-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="64212-126">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="64212-126">Enrich a category landing page</span></span>

<span data-ttu-id="64212-127">Jos haluat, että luokan saapumissivun tietyllä luokalla on paljon räätälöityä kokemusta, voit täydentää kyseisen luokan saapumissivua.</span><span class="sxs-lookup"><span data-stu-id="64212-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="64212-128">Voit esimerkiksi lisätä markkinointivideon ja joitakin luokan tarinoita, joiden avulla saat ostajan huomion.</span><span class="sxs-lookup"><span data-stu-id="64212-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="64212-129">Lisätietoja on kohdassa [Luokan saapumissivun täydentäminen](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="64212-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="64212-131">Automaattisten ehdotusten ja hakutulosten sivut</span><span class="sxs-lookup"><span data-stu-id="64212-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="64212-132">Sivuston käyttäjät voivat selata sivustoa siirtymishierarkian luokan avulla tai syöttämällä hakutermin hakukenttään.</span><span class="sxs-lookup"><span data-stu-id="64212-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="64212-133">Heti, kun käyttäjät alkavat kirjoittaa tekstiä hakukenttään, he näkevät automaattisen ehdotustoiminnon, joka ehdottaa hakutermejä.</span><span class="sxs-lookup"><span data-stu-id="64212-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="64212-134">Seuraavassa on joitakin ehdotuksia, jotka saattavat tulla näkyviin:</span><span class="sxs-lookup"><span data-stu-id="64212-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="64212-135">**Avainsanoja** käytetään etsittäessä nimikkeitä kaikista kanavan tuotteista.</span><span class="sxs-lookup"><span data-stu-id="64212-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="64212-136">**Tuotteet** sisältävät suorat linkit tuotetietosivulle.</span><span class="sxs-lookup"><span data-stu-id="64212-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="64212-137">**Luokkahakualueen ehdotukset** tuovat näyttöön eri luokkia. Niiden avulla käyttäjät voivat hakea tietyn luokan avainsanoja.</span><span class="sxs-lookup"><span data-stu-id="64212-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Mukaansatempaava automaattinen ehdotustoiminto](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="64212-139">Kun käyttäjät valitsevat jonkin avainsanan tai luokkahakualueen ehdotukset tai kun hakutermillä ei saada ehdotuksia, käyttäjät siirretään hakutulossivulle.</span><span class="sxs-lookup"><span data-stu-id="64212-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="64212-140">Käyttäjät voivat tämän jälkeen selata, lajitella ja tarkentaa hakutulosluetteloa löytääksesi haluamasi nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="64212-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Aloitussivu](./media/SearchLanding.png)

<span data-ttu-id="64212-142">Seuraavat osat ovat olennaisia hakutulossivulla:</span><span class="sxs-lookup"><span data-stu-id="64212-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="64212-143">**Tuotesijoitteluruudut** näyttävät käyttäjän haun tuotteet.</span><span class="sxs-lookup"><span data-stu-id="64212-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="64212-144">Oletusarvoisesti nämä ruudut lajitellaan pilvipohjaisen hakurelevanssin pisteiden mukaan käyttäjähaussa.</span><span class="sxs-lookup"><span data-stu-id="64212-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="64212-145">**Tarkennusten ja valinnan yhteenveto** ovat suodattimia määriä varten. Niiden avulla voi myös tarkentaa nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="64212-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="64212-146">Myynninedistämispäällikkö määrittää ne osana kanavaluokkien ja tuotemääritteiden metatietojen määritystä.</span><span class="sxs-lookup"><span data-stu-id="64212-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="64212-147">**Lajitteluasetusten** avulla sivuston vierailijat voivat lajitella tuotteet.</span><span class="sxs-lookup"><span data-stu-id="64212-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="64212-148">Oletusarvoisesti käytettävissä ovat seuraavat lajitteluvaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="64212-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="64212-149">Hinta – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="64212-149">Price – low to high</span></span>
    - <span data-ttu-id="64212-150">Hinta – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="64212-150">Price – high to low</span></span>
    - <span data-ttu-id="64212-151">Tuotteen nimi – \[A-Ö\]</span><span class="sxs-lookup"><span data-stu-id="64212-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="64212-152">Tuotteen nimi – \[Ö-A\]</span><span class="sxs-lookup"><span data-stu-id="64212-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="64212-153">Luokitukset – matalasta korkeaan</span><span class="sxs-lookup"><span data-stu-id="64212-153">Ratings – low to high</span></span>
    - <span data-ttu-id="64212-154">Luokitukset – korkeasta matalaan</span><span class="sxs-lookup"><span data-stu-id="64212-154">Ratings – high to low</span></span>
    - <span data-ttu-id="64212-155">Oletus</span><span class="sxs-lookup"><span data-stu-id="64212-155">Default</span></span>

- <span data-ttu-id="64212-156">**Sivutuksen** avulla sivuston vierailijat voivat siirtyä yhdeltä luokitellun tuotteen sivulta toiselle.</span><span class="sxs-lookup"><span data-stu-id="64212-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="64212-157">**Kokonaismäärä** määrittää luokkaan määritettyjen ja hakuehtoja vastaavien tuotteiden kokonaismäärän.</span><span class="sxs-lookup"><span data-stu-id="64212-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="64212-158">Nämä pilvipohjaiset hakutoiminnot ovat saatavilla versiosta 10.0.8 alkaen.</span><span class="sxs-lookup"><span data-stu-id="64212-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="64212-159">Varmista, että valikossa **Kaupan parametrit > Määrityksen parametrit** on merkintä ProductSearch.UseAzureSearch set to 'true'.</span><span class="sxs-lookup"><span data-stu-id="64212-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="64212-160">![Määrityksen parametrit pilvipohjaiselle haulle](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="64212-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64212-161">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="64212-161">Additional resources</span></span>

[<span data-ttu-id="64212-162">Pilvipohjaisen haun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64212-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="64212-163">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64212-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="64212-164">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64212-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="64212-165">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64212-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="64212-166">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="64212-166">Account management pages overview</span></span>](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]