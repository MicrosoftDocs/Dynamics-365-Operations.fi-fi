---
title: Tuotetietosivujen yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b0f50b4e7b78f4a5b9fe674a101476879923e10d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979825"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="a54cc-103">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a54cc-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a54cc-104">Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="a54cc-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a54cc-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a54cc-105">Overview</span></span>

<span data-ttu-id="a54cc-106">PDP-sivulla on tuotteen eritellyt tiedot. Sen avulla asiakkaat voivat valita tuotevaihtoehtoja, kuten koon, tyylin ja värin.</span><span class="sxs-lookup"><span data-stu-id="a54cc-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="a54cc-107">PDP-sivulla on oltava kaikki tuotteen tiedot, joita asiakas tarvitsee ostopäätöksen tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="a54cc-108">Seuraavassa kuvassa on esimerkki PDP-sivusta.</span><span class="sxs-lookup"><span data-stu-id="a54cc-108">The following illustration shows an example of a PDP.</span></span>

![Esimerkki tuotetietosivusta](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="a54cc-110">Ylä- ja alatunnistemoduulit</span><span class="sxs-lookup"><span data-stu-id="a54cc-110">Header and footer modules</span></span>

<span data-ttu-id="a54cc-111">PDP-sivun yläosassa on ylätunniste, joka sisältää kaikki tuoteluokat ja muut sivut, joita jälleenmyyjä haluaa asiakkaiden selaavan.</span><span class="sxs-lookup"><span data-stu-id="a54cc-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="a54cc-112">Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin asiakasta mahdollisesti kiinnostaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="a54cc-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="a54cc-113">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="a54cc-113">Buy box module</span></span>

<span data-ttu-id="a54cc-114">PDP:N tärkein moduuli on ostolaatikkomoduuli, joka näkyy ensimmäisenä nimikkeenä sivun pääosassa.</span><span class="sxs-lookup"><span data-stu-id="a54cc-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="a54cc-115">Ostolaatikkomoduuli näyttää tärkeitä tuotetietoja, kuten tuotteen nimen, tuotteen kuvauksen, tuotteen hinnan, tuotekuvat ja tuoteluokitukset.</span><span class="sxs-lookup"><span data-stu-id="a54cc-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="a54cc-116">Ostoruutumoduulin avulla asiakas voi valita tuotevaihtoehtoja (esimerkiksi koon, tyylin ja värin) ja lisätä tuotteen ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="a54cc-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="a54cc-117">Sen avulla asiakas voi myös ostaa tuotteen verkosta ja noutaa sen myymälästä.</span><span class="sxs-lookup"><span data-stu-id="a54cc-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="a54cc-118">Osta verkosta ja nouda myymälästä -moduulissa käytetään Bing Maps -ohjelmointirajapintojen integrointia. Sen avulla etsitään lähellä olevat myymälät tai asiakkaan määrittämässä sijainnissa olevat myymälät.</span><span class="sxs-lookup"><span data-stu-id="a54cc-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="a54cc-119">Ostoruutumoduuli vaatiin tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="a54cc-120">Tämä tunnus johdetaan sivun kontekstista.</span><span class="sxs-lookup"><span data-stu-id="a54cc-120">This ID is derived from the page context.</span></span> <span data-ttu-id="a54cc-121">Jos ostoruutumoduuli lisätään sivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, se ei hahmonna tietoja oikein.</span><span class="sxs-lookup"><span data-stu-id="a54cc-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="a54cc-122">Tuotemääritysten moduuli</span><span class="sxs-lookup"><span data-stu-id="a54cc-122">Product specifications module</span></span>

<span data-ttu-id="a54cc-123">Tuotemääritysten moduulia voi käyttää tuotteen lisätietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="a54cc-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="a54cc-124">Nämä tiedot haetaan Commerce-sovelluksen tuotemääritteistä.</span><span class="sxs-lookup"><span data-stu-id="a54cc-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="a54cc-125">Tuotemääritysten moduulissa näytetään kaikki määritteet, joiden **käytettävissä**-ominaisuuden arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="a54cc-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="a54cc-126">Tuotemääritysten hakeminen vaatii tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="a54cc-127">Suositusten moduuli</span><span class="sxs-lookup"><span data-stu-id="a54cc-127">Recommendations module</span></span>

<span data-ttu-id="a54cc-128">Suositusten moduuli on tärkeä moduuli PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a54cc-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="a54cc-129">Kun asiakkaat selaavat tuotteita, heille kannattaa esittää useita tuotevaihtoehtoja. Näin he voivat löytää oikean tuotteen ja ostaa sen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="a54cc-130">Suositusten avulla asiakkaat löytävät helposti liittyvän sisällön ja jatkavat ostosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="a54cc-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="a54cc-131">Käytettävissä on erityyppisiä suositusluetteloita:</span><span class="sxs-lookup"><span data-stu-id="a54cc-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="a54cc-132">**Ihmiset pitävät myös** -luettelo perustuu koneoppimiseen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="a54cc-133">Se käyttää muiden asiakkaiden tapahtumahistoriaa suositusten antamiseen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="a54cc-134">Tämä luettelo on luotu suositusten palvelun avulla. Se muistuttaa Asiakkaat, jotka ostivat tämän, ostivat myös... -luetteloa.</span><span class="sxs-lookup"><span data-stu-id="a54cc-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="a54cc-135">Tämän luettelon luomiseen tarvitaan tuotteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="a54cc-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="a54cc-136">Commercen tuotteelle voidaan määrittää **Liittyvät**-luettelo.</span><span class="sxs-lookup"><span data-stu-id="a54cc-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="a54cc-137">Esimerkiksi ruskealle nahkaiselle matkustusta varten tehdylle käsilaukulle voidaan määrittää Liittyvät-luettelo, joka sisältää nahkaisia tai matkustusta varten suunniteltuja käsilaukkuja.</span><span class="sxs-lookup"><span data-stu-id="a54cc-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="a54cc-138">Commercessa voidaan määrittää myös muun tyyppisiä Liittyvät-luetteloita, kuten **Lisävarusteet** ja **Lisää samanlaisia**.</span><span class="sxs-lookup"><span data-stu-id="a54cc-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="a54cc-139">Tämän luettelon luomiseen tarvitaan tuotteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="a54cc-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="a54cc-140">Jos tämä lisätään aloitussivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, luettelo on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="a54cc-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="a54cc-141">PDP-sivuilla voi käyttää algoritmien avulla luotuja suositusluetteloita, kuten **Suositut**, **Myydyimmät** ja **Uudet**.</span><span class="sxs-lookup"><span data-stu-id="a54cc-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="a54cc-142">Vaikka nämä luettelot eivät välttämättä liity suoraan PDP-sivulla olevaan tuotteeseen, asiakkaat voivat etsiä niiden avulla heitä mahdollisesti kiinnostavia tuotteita.</span><span class="sxs-lookup"><span data-stu-id="a54cc-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="a54cc-143">Tämäntyyppiset luettelot eivät edellytä tuotteen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="a54cc-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="a54cc-144">Nämä ovat yleisiä luetteloita, joita luodaan ostokäyttäytymisen mukaan sivustossa.</span><span class="sxs-lookup"><span data-stu-id="a54cc-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="a54cc-145">Toimitukselliset luettelot ovat manuaalisesti kuratoituja luetteloita.</span><span class="sxs-lookup"><span data-stu-id="a54cc-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="a54cc-146">Jälleenmyyjä voi esimerkiksi päättää manuaalisesti luetteloiden sisältämät tuotteet.</span><span class="sxs-lookup"><span data-stu-id="a54cc-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="a54cc-147">Luokitusten ja arvosteluiden moduulit</span><span class="sxs-lookup"><span data-stu-id="a54cc-147">Ratings and reviews modules</span></span>

<span data-ttu-id="a54cc-148">Kolmea moduulia voidaan käyttää näyttämään ja lisäämään arvosteluja:</span><span class="sxs-lookup"><span data-stu-id="a54cc-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="a54cc-149">**Arvostelut** – Tämä moduuli näyttää muiden asiakkaiden antamat luokitukset ja arvostelut.</span><span class="sxs-lookup"><span data-stu-id="a54cc-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="a54cc-150">Asiakkaat voivat lajitella ja suodattaa arvosteluja.</span><span class="sxs-lookup"><span data-stu-id="a54cc-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="a54cc-151">Tämä moduuli myös sallii asiakkaiden antaa hyviä tai huonoja arvosteluja, ja raportoida asioista.</span><span class="sxs-lookup"><span data-stu-id="a54cc-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="a54cc-152">**Kirjoita arvostelu** -Tämä moduuli sallii asiakkaiden kirjoittaa omia arvosteluja tuotteesta.</span><span class="sxs-lookup"><span data-stu-id="a54cc-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="a54cc-153">**Luokitukset histogrammi** – Tämä moduuli sisältää histogrammin, joka ilmaisee tuotteen luokituskehityksen.</span><span class="sxs-lookup"><span data-stu-id="a54cc-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="a54cc-154">Lisätietoja on kohdassa [Luokitusten ja arvostelujen yleiskuvaus](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a54cc-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="a54cc-155">Markkinointimoduulit</span><span class="sxs-lookup"><span data-stu-id="a54cc-155">Marketing modules</span></span>

<span data-ttu-id="a54cc-156">Jos markkinointisisältö koskee vain tiettyä tuotetta, mikä tahansa markkinointimoduuli voidaan lisätä PDP-sivulle.</span><span class="sxs-lookup"><span data-stu-id="a54cc-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="a54cc-157">Voit lisätä markkinointimoduuleja PDP-sivulla täydentämällä sivua.</span><span class="sxs-lookup"><span data-stu-id="a54cc-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="a54cc-158">Lisätietoja on kohdassa [Tuotesivun täydentäminen](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="a54cc-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a54cc-159">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a54cc-159">Additional resources</span></span>

[<span data-ttu-id="a54cc-160">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a54cc-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="a54cc-161">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a54cc-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="a54cc-162">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a54cc-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="a54cc-163">Tuotetietosivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="a54cc-163">Enrich a product details page</span></span>](enrich-product-page.md)
