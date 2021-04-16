---
title: Tuotetietosivujen yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792216"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="89d34-103">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="89d34-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89d34-104">Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="89d34-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="89d34-105">PDP-sivulla on tuotteen eritellyt tiedot. Sen avulla asiakkaat voivat valita tuotevaihtoehtoja, kuten koon, tyylin ja värin.</span><span class="sxs-lookup"><span data-stu-id="89d34-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="89d34-106">PDP-sivulla on oltava kaikki tuotteen tiedot, joita asiakas tarvitsee ostopäätöksen tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="89d34-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="89d34-107">Seuraavassa kuvassa on esimerkki PDP-sivusta.</span><span class="sxs-lookup"><span data-stu-id="89d34-107">The following illustration shows an example of a PDP.</span></span>

![Esimerkki tuotetietosivusta](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="89d34-109">Ylä- ja alatunnistemoduulit</span><span class="sxs-lookup"><span data-stu-id="89d34-109">Header and footer modules</span></span>

<span data-ttu-id="89d34-110">PDP-sivun yläosassa on ylätunniste, joka sisältää kaikki tuoteluokat ja muut sivut, joita jälleenmyyjä haluaa asiakkaiden selaavan.</span><span class="sxs-lookup"><span data-stu-id="89d34-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="89d34-111">Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin asiakasta mahdollisesti kiinnostaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="89d34-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="89d34-112">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="89d34-112">Buy box module</span></span>

<span data-ttu-id="89d34-113">PDP:N tärkein moduuli on ostolaatikkomoduuli, joka näkyy ensimmäisenä nimikkeenä sivun pääosassa.</span><span class="sxs-lookup"><span data-stu-id="89d34-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="89d34-114">Ostolaatikkomoduuli näyttää tärkeitä tuotetietoja, kuten tuotteen nimen, tuotteen kuvauksen, tuotteen hinnan, tuotekuvat ja tuoteluokitukset.</span><span class="sxs-lookup"><span data-stu-id="89d34-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="89d34-115">Ostoruutumoduulin avulla asiakas voi valita tuotevaihtoehtoja (esimerkiksi koon, tyylin ja värin) ja lisätä tuotteen ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="89d34-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="89d34-116">Sen avulla asiakas voi myös ostaa tuotteen verkosta ja noutaa sen myymälästä.</span><span class="sxs-lookup"><span data-stu-id="89d34-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="89d34-117">Osta verkosta ja nouda myymälästä -moduulissa käytetään Bing Maps -ohjelmointirajapintojen integrointia. Sen avulla etsitään lähellä olevat myymälät tai asiakkaan määrittämässä sijainnissa olevat myymälät.</span><span class="sxs-lookup"><span data-stu-id="89d34-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="89d34-118">Ostoruutumoduuli vaatiin tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="89d34-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="89d34-119">Tämä tunnus johdetaan sivun kontekstista.</span><span class="sxs-lookup"><span data-stu-id="89d34-119">This ID is derived from the page context.</span></span> <span data-ttu-id="89d34-120">Jos ostoruutumoduuli lisätään sivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, se ei hahmonna tietoja oikein.</span><span class="sxs-lookup"><span data-stu-id="89d34-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="89d34-121">Tuotemääritysten moduuli</span><span class="sxs-lookup"><span data-stu-id="89d34-121">Product specifications module</span></span>

<span data-ttu-id="89d34-122">Tuotemääritysten moduulia voi käyttää tuotteen lisätietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="89d34-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="89d34-123">Nämä tiedot haetaan Commerce-sovelluksen tuotemääritteistä.</span><span class="sxs-lookup"><span data-stu-id="89d34-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="89d34-124">Tuotemääritysten moduulissa näytetään kaikki määritteet, joiden **käytettävissä**-ominaisuuden arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="89d34-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="89d34-125">Tuotemääritysten hakeminen vaatii tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="89d34-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="89d34-126">Suositusten moduuli</span><span class="sxs-lookup"><span data-stu-id="89d34-126">Recommendations module</span></span>

<span data-ttu-id="89d34-127">Suositusten moduuli on tärkeä moduuli PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="89d34-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="89d34-128">Kun asiakkaat selaavat tuotteita, heille kannattaa esittää useita tuotevaihtoehtoja. Näin he voivat löytää oikean tuotteen ja ostaa sen.</span><span class="sxs-lookup"><span data-stu-id="89d34-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="89d34-129">Suositusten avulla asiakkaat löytävät helposti liittyvän sisällön ja jatkavat ostosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="89d34-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="89d34-130">Käytettävissä on erityyppisiä suositusluetteloita:</span><span class="sxs-lookup"><span data-stu-id="89d34-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="89d34-131">**Ihmiset pitävät myös** -luettelo perustuu koneoppimiseen.</span><span class="sxs-lookup"><span data-stu-id="89d34-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="89d34-132">Se käyttää muiden asiakkaiden tapahtumahistoriaa suositusten antamiseen.</span><span class="sxs-lookup"><span data-stu-id="89d34-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="89d34-133">Tämä luettelo on luotu suositusten palvelun avulla. Se muistuttaa Asiakkaat, jotka ostivat tämän, ostivat myös... -luetteloa.</span><span class="sxs-lookup"><span data-stu-id="89d34-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="89d34-134">Tämän luettelon luomiseen tarvitaan tuotteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="89d34-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="89d34-135">Commercen tuotteelle voidaan määrittää **Liittyvät**-luettelo.</span><span class="sxs-lookup"><span data-stu-id="89d34-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="89d34-136">Esimerkiksi ruskealle nahkaiselle matkustusta varten tehdylle käsilaukulle voidaan määrittää Liittyvät-luettelo, joka sisältää nahkaisia tai matkustusta varten suunniteltuja käsilaukkuja.</span><span class="sxs-lookup"><span data-stu-id="89d34-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="89d34-137">Commercessa voidaan määrittää myös muun tyyppisiä Liittyvät-luetteloita, kuten **Lisävarusteet** ja **Lisää samanlaisia**.</span><span class="sxs-lookup"><span data-stu-id="89d34-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="89d34-138">Tämän luettelon luomiseen tarvitaan tuotteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="89d34-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="89d34-139">Jos tämä lisätään aloitussivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, luettelo on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="89d34-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="89d34-140">PDP-sivuilla voi käyttää algoritmien avulla luotuja suositusluetteloita, kuten **Suositut**, **Myydyimmät** ja **Uudet**.</span><span class="sxs-lookup"><span data-stu-id="89d34-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="89d34-141">Vaikka nämä luettelot eivät välttämättä liity suoraan PDP-sivulla olevaan tuotteeseen, asiakkaat voivat etsiä niiden avulla heitä mahdollisesti kiinnostavia tuotteita.</span><span class="sxs-lookup"><span data-stu-id="89d34-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="89d34-142">Tämäntyyppiset luettelot eivät edellytä tuotteen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="89d34-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="89d34-143">Nämä ovat yleisiä luetteloita, joita luodaan ostokäyttäytymisen mukaan sivustossa.</span><span class="sxs-lookup"><span data-stu-id="89d34-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="89d34-144">Toimitukselliset luettelot ovat manuaalisesti kuratoituja luetteloita.</span><span class="sxs-lookup"><span data-stu-id="89d34-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="89d34-145">Jälleenmyyjä voi esimerkiksi päättää manuaalisesti luetteloiden sisältämät tuotteet.</span><span class="sxs-lookup"><span data-stu-id="89d34-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="89d34-146">Luokitusten ja arvosteluiden moduulit</span><span class="sxs-lookup"><span data-stu-id="89d34-146">Ratings and reviews modules</span></span>

<span data-ttu-id="89d34-147">Kolmea moduulia voidaan käyttää näyttämään ja lisäämään arvosteluja:</span><span class="sxs-lookup"><span data-stu-id="89d34-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="89d34-148">**Arvostelut** – Tämä moduuli näyttää muiden asiakkaiden antamat luokitukset ja arvostelut.</span><span class="sxs-lookup"><span data-stu-id="89d34-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="89d34-149">Asiakkaat voivat lajitella ja suodattaa arvosteluja.</span><span class="sxs-lookup"><span data-stu-id="89d34-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="89d34-150">Tämä moduuli myös sallii asiakkaiden antaa hyviä tai huonoja arvosteluja, ja raportoida asioista.</span><span class="sxs-lookup"><span data-stu-id="89d34-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="89d34-151">**Kirjoita arvostelu** -Tämä moduuli sallii asiakkaiden kirjoittaa omia arvosteluja tuotteesta.</span><span class="sxs-lookup"><span data-stu-id="89d34-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="89d34-152">**Luokitukset histogrammi** – Tämä moduuli sisältää histogrammin, joka ilmaisee tuotteen luokituskehityksen.</span><span class="sxs-lookup"><span data-stu-id="89d34-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="89d34-153">Lisätietoja on kohdassa [Luokitusten ja arvostelujen yleiskuvaus](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="89d34-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="89d34-154">Markkinointimoduulit</span><span class="sxs-lookup"><span data-stu-id="89d34-154">Marketing modules</span></span>

<span data-ttu-id="89d34-155">Jos markkinointisisältö koskee vain tiettyä tuotetta, mikä tahansa markkinointimoduuli voidaan lisätä PDP-sivulle.</span><span class="sxs-lookup"><span data-stu-id="89d34-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="89d34-156">Voit lisätä markkinointimoduuleja PDP-sivulla täydentämällä sivua.</span><span class="sxs-lookup"><span data-stu-id="89d34-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="89d34-157">Lisätietoja on kohdassa [Tuotesivun täydentäminen](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="89d34-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89d34-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="89d34-158">Additional resources</span></span>

[<span data-ttu-id="89d34-159">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="89d34-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="89d34-160">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="89d34-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="89d34-161">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="89d34-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="89d34-162">Tuotetietosivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="89d34-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
