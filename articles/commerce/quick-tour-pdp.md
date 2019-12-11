---
title: Tuotetietosivujen yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697862"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="66195-103">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="66195-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="66195-104">Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="66195-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="66195-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="66195-105">Overview</span></span>

<span data-ttu-id="66195-106">PDP-sivulla on tuotteen eritellyt tiedot. Sen avulla asiakkaat voivat valita tuotevaihtoehtoja, kuten koon, tyylin ja värin.</span><span class="sxs-lookup"><span data-stu-id="66195-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="66195-107">PDP-sivulla on oltava kaikki tuotteen tiedot, joita asiakas tarvitsee ostopäätöksen tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="66195-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="66195-108">Seuraavassa kuvassa on esimerkki PDP-sivusta.</span><span class="sxs-lookup"><span data-stu-id="66195-108">The following illustration shows an example of a PDP.</span></span>

![Esimerkki tuotetietosivusta](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="66195-110">Ylä- ja alatunnistemoduulit</span><span class="sxs-lookup"><span data-stu-id="66195-110">Header and footer modules</span></span>

<span data-ttu-id="66195-111">PDP-sivun yläosassa on ylätunniste, joka sisältää kaikki tuoteluokat ja muut sivut, joita jälleenmyyjä haluaa asiakkaiden selaavan.</span><span class="sxs-lookup"><span data-stu-id="66195-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="66195-112">Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin asiakasta mahdollisesti kiinnostaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="66195-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="66195-113">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="66195-113">Buy box module</span></span>

<span data-ttu-id="66195-114">PDP-sivun tärkein moduuli on ostoruutumoduuli.</span><span class="sxs-lookup"><span data-stu-id="66195-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="66195-115">Siksi se on sivun pääosan ensimmäinen nimike.</span><span class="sxs-lookup"><span data-stu-id="66195-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="66195-116">Ostoruutumoduuli on säilömoduuli. Se isännöi useita moduuleja, jotka sisältävät tuotetta koskevia tärkeitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="66195-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="66195-117">Näitä tietoja ovat esimerkiksi tuotteen nimi, tuotteen kuvat, kuvaus, hinta ja tuoteluokitukset.</span><span class="sxs-lookup"><span data-stu-id="66195-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="66195-118">Ostoruutumoduulin avulla asiakas voi valita tuotevaihtoehtoja (esimerkiksi koon, tyylin ja värin) ja lisätä tuotteen ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="66195-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="66195-119">Sen avulla asiakas voi myös ostaa tuotteen verkosta ja noutaa sen myymälästä.</span><span class="sxs-lookup"><span data-stu-id="66195-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="66195-120">Osta verkosta ja nouda myymälästä -moduulissa käytetään Bing Maps -ohjelmointirajapintojen integrointia. Sen avulla etsitään lähellä olevat myymälät tai asiakkaan määrittämässä sijainnissa olevat myymälät.</span><span class="sxs-lookup"><span data-stu-id="66195-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="66195-121">Ostoruutumoduuli vaatiin tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="66195-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="66195-122">Tämä tunnus johdetaan sivun kontekstista.</span><span class="sxs-lookup"><span data-stu-id="66195-122">This ID is derived from the page context.</span></span> <span data-ttu-id="66195-123">Jos ostoruutumoduuli lisätään sivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, se ei hahmonna tietoja oikein.</span><span class="sxs-lookup"><span data-stu-id="66195-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="66195-124">Tuotemääritysten moduuli</span><span class="sxs-lookup"><span data-stu-id="66195-124">Product specifications module</span></span>

<span data-ttu-id="66195-125">Tuotemääritysten moduulia voi käyttää tuotteen lisätietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="66195-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="66195-126">Nämä tiedot haetaan Dynamics 365 Retail -sovelluksen tuotemääritteistä.</span><span class="sxs-lookup"><span data-stu-id="66195-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="66195-127">Tuotemääritysten moduulissa näytetään kaikki määritteet, joiden **käytettävissä**-ominaisuuden arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="66195-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="66195-128">Tuotemääritysten hakeminen vaatii tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="66195-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="66195-129">Suositusten moduuli</span><span class="sxs-lookup"><span data-stu-id="66195-129">Recommendations module</span></span>

<span data-ttu-id="66195-130">Suositusten moduuli on tärkeä moduuli PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="66195-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="66195-131">Kun asiakkaat selaavat tuotteita, heille kannattaa esittää useita tuotevaihtoehtoja. Näin he voivat löytää oikean tuotteen ja ostaa sen.</span><span class="sxs-lookup"><span data-stu-id="66195-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="66195-132">Suositusten avulla asiakkaat löytävät helposti liittyvän sisällön ja jatkavat ostosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="66195-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="66195-133">Käytettävissä on erityyppisiä suositusluetteloita:</span><span class="sxs-lookup"><span data-stu-id="66195-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="66195-134">**Ihmiset pitävät myös** -luettelo perustuu koneoppimiseen.</span><span class="sxs-lookup"><span data-stu-id="66195-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="66195-135">Se käyttää muiden asiakkaiden tapahtumahistoriaa suositusten antamiseen.</span><span class="sxs-lookup"><span data-stu-id="66195-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="66195-136">Tämä luettelo on luotu suositusten palvelun avulla. Se muistuttaa Asiakkaat, jotka ostivat tämän, ostivat myös... -luetteloa.</span><span class="sxs-lookup"><span data-stu-id="66195-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="66195-137">Tämän luettelon luomiseen tarvitaan tuotteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="66195-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="66195-138">Retailin tuotteelle voidaan määrittää **Liittyvät**-luettelo.</span><span class="sxs-lookup"><span data-stu-id="66195-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="66195-139">Esimerkiksi ruskealle nahkaiselle matkustusta varten tehdylle käsilaukulle voidaan määrittää Liittyvät-luettelo, joka sisältää nahkaisia tai matkustusta varten suunniteltuja käsilaukkuja.</span><span class="sxs-lookup"><span data-stu-id="66195-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="66195-140">Retailissa voidaan määrittää myös muun tyyppisiä Liittyvät-luetteloita, kuten **Lisävarusteet** ja **Lisää samanlaisia**.</span><span class="sxs-lookup"><span data-stu-id="66195-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="66195-141">Tämän luettelon luomiseen tarvitaan tuotteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="66195-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="66195-142">Jos tämä lisätään aloitussivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, luettelo on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="66195-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="66195-143">PDP-sivuilla voi käyttää algoritmien avulla luotuja suositusluetteloita, kuten **Suositut**, **Myydyimmät** ja **Uudet**.</span><span class="sxs-lookup"><span data-stu-id="66195-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="66195-144">Vaikka nämä luettelot eivät välttämättä liity suoraan PDP-sivulla olevaan tuotteeseen, asiakkaat voivat etsiä niiden avulla heitä mahdollisesti kiinnostavia tuotteita.</span><span class="sxs-lookup"><span data-stu-id="66195-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="66195-145">Tämäntyyppiset luettelot eivät edellytä tuotteen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="66195-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="66195-146">Nämä ovat yleisiä luetteloita, joita luodaan ostokäyttäytymisen mukaan sivustossa.</span><span class="sxs-lookup"><span data-stu-id="66195-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="66195-147">Toimitukselliset luettelot ovat manuaalisesti kuratoituja luetteloita.</span><span class="sxs-lookup"><span data-stu-id="66195-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="66195-148">Jälleenmyyjä voi esimerkiksi päättää manuaalisesti luetteloiden sisältämät tuotteet.</span><span class="sxs-lookup"><span data-stu-id="66195-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="66195-149">Luokitusten ja arvosteluiden moduuli</span><span class="sxs-lookup"><span data-stu-id="66195-149">Ratings and reviews module</span></span>

<span data-ttu-id="66195-150">Luokitukset ja arvostelut -moduulissa näkyvät muiden asiakkaiden antamat luokitukset ja arvostelut.</span><span class="sxs-lookup"><span data-stu-id="66195-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="66195-151">Sen avulla asiakas voi myös kirjoittaa tuotteesta oman arvostelun.</span><span class="sxs-lookup"><span data-stu-id="66195-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="66195-152">Lisäksi se sisältää histogrammin, joka ilmaisee tuotteen luokitusten kehityksen.</span><span class="sxs-lookup"><span data-stu-id="66195-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="66195-153">Lisätietoja on kohdassa [Luokitusten ja arvostelujen yleiskuvaus](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="66195-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="66195-154">Markkinointimoduulit</span><span class="sxs-lookup"><span data-stu-id="66195-154">Marketing modules</span></span>

<span data-ttu-id="66195-155">Jos markkinointisisältö koskee vain tiettyä tuotetta, mikä tahansa markkinointimoduuli voidaan lisätä PDP-sivulle.</span><span class="sxs-lookup"><span data-stu-id="66195-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="66195-156">Voit lisätä markkinointimoduuleja PDP-sivulla täydentämällä sivua.</span><span class="sxs-lookup"><span data-stu-id="66195-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="66195-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="66195-157">Additional resources</span></span>

[<span data-ttu-id="66195-158">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="66195-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="66195-159">Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="66195-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="66195-160">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="66195-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="66195-161">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="66195-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
