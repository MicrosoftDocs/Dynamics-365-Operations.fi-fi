---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261418"
---
# <a name="cart-module"></a><span data-ttu-id="8fbae-103">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8fbae-104">Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="8fbae-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8fbae-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="8fbae-105">Overview</span></span>

<span data-ttu-id="8fbae-106">Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle.</span><span class="sxs-lookup"><span data-stu-id="8fbae-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="8fbae-107">Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="8fbae-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="8fbae-108">Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana.</span><span class="sxs-lookup"><span data-stu-id="8fbae-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="8fbae-109">Se tukee myös **Jatka ostoksia** -linkkejä.</span><span class="sxs-lookup"><span data-stu-id="8fbae-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="8fbae-110">Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.</span><span class="sxs-lookup"><span data-stu-id="8fbae-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="8fbae-111">Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste.</span><span class="sxs-lookup"><span data-stu-id="8fbae-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="8fbae-112">Ostoskorimoduulin ominaisuudet ja paikat</span><span class="sxs-lookup"><span data-stu-id="8fbae-112">Cart module properties and slots</span></span>

<span data-ttu-id="8fbae-113">Ostoskorimoduulissa on **Otsikko**-ominaisuus, jonka arvoiksi voidaan määrittää esimerkiksi **Ostoskassi** ja **Ostoskorin nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="8fbae-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="8fbae-114">Moduulit, joita voidaan käyttää ostoskorimoduulissa</span><span class="sxs-lookup"><span data-stu-id="8fbae-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="8fbae-115">**Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="8fbae-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="8fbae-116">Sisällönhallintajärjestelmä (CMS) ohjaa viestintää.</span><span class="sxs-lookup"><span data-stu-id="8fbae-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="8fbae-117">Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="8fbae-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="8fbae-118">**Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="8fbae-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="8fbae-119">Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin.</span><span class="sxs-lookup"><span data-stu-id="8fbae-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="8fbae-120">Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="8fbae-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="8fbae-121">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8fbae-121">Module properties</span></span>

<span data-ttu-id="8fbae-122">Ostoskorimoduulissa on seuraavat asetukset, jotka voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:</span><span class="sxs-lookup"><span data-stu-id="8fbae-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="8fbae-123">**Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="8fbae-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="8fbae-124">Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.</span><span class="sxs-lookup"><span data-stu-id="8fbae-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="8fbae-125">**Varaston tarkistus** – Kun arvoksi on asetettu **Tosi**, nimike lisätään ostoskoriin vasta, kun ostoruutumoduuli varmistaa, että nimikettä on varastossa.</span><span class="sxs-lookup"><span data-stu-id="8fbae-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="8fbae-126">Tämä varaston tarkistus tehdään skenaarioissa, joissa nimike toimitetaan, että skenaarioissa, joissa se noudetaan myymälästä.</span><span class="sxs-lookup"><span data-stu-id="8fbae-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="8fbae-127">Jos arvoksi on määritetty **Epätosi**, varaston tarkistus tehdään vasta, kun nimike on lisätty ostoskoriin ja tilaus on tehty.</span><span class="sxs-lookup"><span data-stu-id="8fbae-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="8fbae-128">Lisätietoja varastoasetusten määrittämisestä taustaohjelmassa on kohdassa [Varaston käytettävyyden laskeminen vähittäismyyntikanaville](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="8fbae-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="8fbae-129">**Varaston puskuri** – Tällä ominaisuudella määritetään varaston puskurimäärä.</span><span class="sxs-lookup"><span data-stu-id="8fbae-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="8fbae-130">Varastoa ylläpidetään reaaliaikaisesti. Jos useat asiakkaat tekevät tilauksia, todellisen varastomäärän ylläpitäminen voi olla vaikeaa.</span><span class="sxs-lookup"><span data-stu-id="8fbae-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="8fbae-131">Kun varaston tarkistus tehdään ja varasto on pienempi kuin puskurisumma, tuotetta käsitellään kuin se olisi loppunut varastosta.</span><span class="sxs-lookup"><span data-stu-id="8fbae-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="8fbae-132">Kun myynti tapahtuu nopeasti useiden kanavien kautta eikä varastomäärä ole täysin synkronoitu, on pienempi riski siitä, että nimikettä ei ole varastossa myynnin hetkellä.</span><span class="sxs-lookup"><span data-stu-id="8fbae-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="8fbae-133">**Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti.</span><span class="sxs-lookup"><span data-stu-id="8fbae-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="8fbae-134">Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.</span><span class="sxs-lookup"><span data-stu-id="8fbae-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="8fbae-135">Commerce Scale Unit -käyttö</span><span class="sxs-lookup"><span data-stu-id="8fbae-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="8fbae-136">Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="8fbae-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="8fbae-137">Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.</span><span class="sxs-lookup"><span data-stu-id="8fbae-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="8fbae-138">Ostoskorimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="8fbae-138">Add a cart module to a page</span></span>

<span data-ttu-id="8fbae-139">Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8fbae-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8fbae-140">Luo osa nimeltä **Ostoskoriosa** ja lisää uuteen osaan ostoskorimoduuli.</span><span class="sxs-lookup"><span data-stu-id="8fbae-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="8fbae-141">Lisää otsikko ostoskorimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="8fbae-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="8fbae-142">Lisää myymälän valitsinmoduuli ostoskorimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="8fbae-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="8fbae-143">Tallenna osa, lopeta sen muokkaus ja sitten julkaise osa.</span><span class="sxs-lookup"><span data-stu-id="8fbae-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="8fbae-144">Luo malli nimeltä **Ostoskorimalli** ja lisää juuri luotu ostoskoriosa.</span><span class="sxs-lookup"><span data-stu-id="8fbae-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="8fbae-145">Tallenna malli, lopeta sen muokkaus ja sitten julkaise malli.</span><span class="sxs-lookup"><span data-stu-id="8fbae-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="8fbae-146">Luo sivu, joka käyttää uutta mallia.</span><span class="sxs-lookup"><span data-stu-id="8fbae-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="8fbae-147">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="8fbae-147">Save and preview the page.</span></span>
1. <span data-ttu-id="8fbae-148">Lopeta sivun muokkaus ja sitten julkaise sivu.</span><span class="sxs-lookup"><span data-stu-id="8fbae-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8fbae-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8fbae-149">Additional resources</span></span>

[<span data-ttu-id="8fbae-150">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8fbae-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8fbae-151">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8fbae-152">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8fbae-153">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8fbae-154">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8fbae-155">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8fbae-156">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8fbae-157">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8fbae-158">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8fbae-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="8fbae-159">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="8fbae-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
