---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025433"
---
# <a name="cart-module"></a><span data-ttu-id="10651-103">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="10651-104">Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="10651-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10651-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="10651-105">Overview</span></span>

<span data-ttu-id="10651-106">Ostokorimoduulissa näytetään ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle.</span><span class="sxs-lookup"><span data-stu-id="10651-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="10651-107">Se sisältää esimerkiksi kaikki ostoskoriin lisätyt nimikkeet ja tilauksen yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="10651-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="10651-108">Lisäksi asiakas voi käyttää tai poistaa kampanjakoodeja.</span><span class="sxs-lookup"><span data-stu-id="10651-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="10651-109">Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana.</span><span class="sxs-lookup"><span data-stu-id="10651-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="10651-110">Se tukee myös **Jatka ostoksia** -linkkejä.</span><span class="sxs-lookup"><span data-stu-id="10651-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="10651-111">Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.</span><span class="sxs-lookup"><span data-stu-id="10651-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="10651-112">Ostoskorimoduuli hahmontaa tiedot ostoskorin tunnuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="10651-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="10651-113">Ostoskorin tunnus on selaimen eväste, joka on käytettävissä koko sivustossa.</span><span class="sxs-lookup"><span data-stu-id="10651-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="10651-114">Ostoskorimoduulin ominaisuudet ja paikat</span><span class="sxs-lookup"><span data-stu-id="10651-114">Cart module properties and slots</span></span>

<span data-ttu-id="10651-115">Ostoskorimoduulissa on **Otsikko**-ominaisuus, jonka arvoiksi voidaan määrittää esimerkiksi **Ostoskassi** ja **Ostoskorin nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="10651-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="10651-116">Moduulit, joita voidaan käyttää ostoskorimoduulissa</span><span class="sxs-lookup"><span data-stu-id="10651-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="10651-117">**Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="10651-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="10651-118">Sisällönhallintajärjestelmä (CMS) ohjaa viestintää.</span><span class="sxs-lookup"><span data-stu-id="10651-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="10651-119">Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="10651-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="10651-120">**Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="10651-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="10651-121">Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin.</span><span class="sxs-lookup"><span data-stu-id="10651-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="10651-122">Myymälän valitsinmoduuli on integroitu Bing Maps -geokoodauksen ohjelmointirajapintaan, jota käytetään muuntamaan sijainti leveys- ja pituusasteiksi.</span><span class="sxs-lookup"><span data-stu-id="10651-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="10651-123">Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Vähittäismyynnin yhteiset parametrit -sivulla Dynamics 365 Retailissa.</span><span class="sxs-lookup"><span data-stu-id="10651-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="10651-124">Tämä moduuli tukee kahta ominaisuutta: **Hakusäde** ja **Käyttöehdot-linkki**.</span><span class="sxs-lookup"><span data-stu-id="10651-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="10651-125">**Hakusäde**-ominaisuus määrittää myymälän hakusäteen maileina.</span><span class="sxs-lookup"><span data-stu-id="10651-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="10651-126">Jos arvoa ei määritetä, käytössä on oletushakusäde 50 mailia.</span><span class="sxs-lookup"><span data-stu-id="10651-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="10651-127">Jos käytössä on Bings Maps tai jokin ulkoinen palvelu, palveluehtojen linkki voidaan antaa **Käyttöehdot-linkki**-ominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="10651-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="10651-128">Palveluehtojen linkki on pakollinen Bing Maps -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="10651-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="10651-129">Ostoskorimoduulin asetukset</span><span class="sxs-lookup"><span data-stu-id="10651-129">Cart module settings</span></span>

<span data-ttu-id="10651-130">Ostoskorimoduulissa on seuraavat asetukset, jotka voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:</span><span class="sxs-lookup"><span data-stu-id="10651-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="10651-131">**Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="10651-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="10651-132">Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.</span><span class="sxs-lookup"><span data-stu-id="10651-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="10651-133">**Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa.</span><span class="sxs-lookup"><span data-stu-id="10651-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="10651-134">Tämä varaston tarkistus tehdään sekä skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä.</span><span class="sxs-lookup"><span data-stu-id="10651-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="10651-135">Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="10651-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="10651-136">**Varaston puskuri** – Tällä ominaisuudella määritetään varaston puskurimäärä.</span><span class="sxs-lookup"><span data-stu-id="10651-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="10651-137">Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa.</span><span class="sxs-lookup"><span data-stu-id="10651-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="10651-138">Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta.</span><span class="sxs-lookup"><span data-stu-id="10651-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="10651-139">Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärä ole täysin synkronoitu, on pienempi riski siitä, että nimikettä ei ole varastossa myynnin hetkellä.</span><span class="sxs-lookup"><span data-stu-id="10651-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="10651-140">**Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti.</span><span class="sxs-lookup"><span data-stu-id="10651-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="10651-141">Tämä reitti voidaan määrittää sivustotasolla.</span><span class="sxs-lookup"><span data-stu-id="10651-141">This route can be configured at the site level.</span></span> <span data-ttu-id="10651-142">Tämän määrityksen ansiosta vähittäismyyjät voivat siirtää asiakkaan takaisin aloitussivulle tai jollekin muulle sivuston sivulle.</span><span class="sxs-lookup"><span data-stu-id="10651-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="10651-143">Commerce Scale Unit -käyttö</span><span class="sxs-lookup"><span data-stu-id="10651-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="10651-144">Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="10651-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="10651-145">Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.</span><span class="sxs-lookup"><span data-stu-id="10651-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="10651-146">Ostoskorimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="10651-146">Add a cart module to a page</span></span>

<span data-ttu-id="10651-147">Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="10651-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="10651-148">Luo osa nimeltä **Ostoskoriosa** ja lisää siihen ostoskorimoduuli.</span><span class="sxs-lookup"><span data-stu-id="10651-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="10651-149">Lisää otsikko ostoskorimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="10651-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="10651-150">Lisää myymälän valitsinmoduuli ostoskorimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="10651-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="10651-151">Tallenna osa, lopeta sen muokkaus ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="10651-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="10651-152">Luo malli nimeltä **Ostoskorimalli** ja lisää siihen juuri luotu ostoskoriosa.</span><span class="sxs-lookup"><span data-stu-id="10651-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="10651-153">Tallenna malli, lopeta sen muokkaus ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="10651-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="10651-154">Luo sivu, joka käyttää uutta mallia.</span><span class="sxs-lookup"><span data-stu-id="10651-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="10651-155">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="10651-155">Save and preview the page.</span></span>
1. <span data-ttu-id="10651-156">Kun sivun muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="10651-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10651-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="10651-157">Additional resources</span></span>

[<span data-ttu-id="10651-158">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="10651-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="10651-159">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="10651-160">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="10651-161">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="10651-162">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="10651-163">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="10651-164">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="10651-164">Footer module</span></span>](author-footer-module.md)
