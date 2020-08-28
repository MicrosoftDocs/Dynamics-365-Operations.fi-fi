---
title: Ylätunnistemoduuli
description: Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686619"
---
# <a name="header-module"></a><span data-ttu-id="156d9-103">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="156d9-104">Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="156d9-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="156d9-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="156d9-105">Overview</span></span>

<span data-ttu-id="156d9-106">Dynamics 365 Commercessa sivun ylätunniste koostuu useita moduuleista, kuten ylätunniste-, siirtymisvalikko-, haku-, mainosbanneri- ja evästehyväksyntämoduuleista.</span><span class="sxs-lookup"><span data-stu-id="156d9-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="156d9-107">Ylätunnistemoduuli sisältää sivuston logon, linkit siirtymishierarkiaan, linkit muille sivuston sivuille, ostoskorisymbolin, toivelistasymbolin, kirjautumisvaihtoehdot ja hakupalkin.</span><span class="sxs-lookup"><span data-stu-id="156d9-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="156d9-108">Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten).</span><span class="sxs-lookup"><span data-stu-id="156d9-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="156d9-109">Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).</span><span class="sxs-lookup"><span data-stu-id="156d9-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="156d9-110">Seuraavassa kuvassa on esimerkki otsikkomoduulista kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="156d9-110">The following image shows an example of a header module on a home page.</span></span>

![Esimerkki otsikkomoduulista](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="156d9-112">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="156d9-112">Properties of a header module</span></span>

<span data-ttu-id="156d9-113">Ylätunnistemoduuli tukee **Logon kuva**-, **Logon linkki**- ja **Oman tilin linkit** -ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="156d9-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="156d9-114">**Logon kuva**- ja **Logon linkki** -ominaisuuksilla määritetään sivulla oleva logo.</span><span class="sxs-lookup"><span data-stu-id="156d9-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="156d9-115">Lisätietoja on kohdassa [Logon lisääminen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="156d9-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="156d9-116">**Oman tilin linkit** -ominaisuudella voidaan määrittää ne tilisivut, joiden pikalinkit sivuston omistaja haluaa näyttää ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="156d9-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="156d9-117">Ylätunnistemoduulin käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="156d9-117">Modules that are available in a header module</span></span>

<span data-ttu-id="156d9-118">Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:</span><span class="sxs-lookup"><span data-stu-id="156d9-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="156d9-119">**Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä.</span><span class="sxs-lookup"><span data-stu-id="156d9-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="156d9-120">Kanavan siirtymishierarkia voidaan määrittää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="156d9-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="156d9-121">Siirtymisvalikossa on **Siirtymisen lähde** -ominaisuus, jolla määritetään Retail Serverin siirtymisvalikon vaihtoehdot ja staattiset valikkovaihtoehdot lähteeksi.</span><span class="sxs-lookup"><span data-stu-id="156d9-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="156d9-122">Jos staattiset valikkovaihtoehdot määritetään lähteeksi, sivuston muille sivulle voidaan antaa suhteelliset linkit.</span><span class="sxs-lookup"><span data-stu-id="156d9-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="156d9-123">Määritetyt nimikkeet näkyvät tämän jälkeen ylätunnisteen siirtymistoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="156d9-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="156d9-124">**Haku** – Hakumoduulin avulla käyttäjät voivat etsiä tuotteita hakusanojen avulla.</span><span class="sxs-lookup"><span data-stu-id="156d9-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="156d9-125">Oletushakusivun URL-osoite ja hakukyselyn parametrit on annettava valitsemalla **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="156d9-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="156d9-126">Hakumoduulissa on ominaisuuksia, joiden avulla voit estää hakupainikkeen tai -selitteen tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="156d9-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="156d9-127">Hakumoduuli tukee myös automaattisia ehdotuksia, kuten tuotteen, avainsanan ja luokan hakutuloksia.</span><span class="sxs-lookup"><span data-stu-id="156d9-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="156d9-128">**Ostoskorikuvake** – Ostoskorikuvakemoduuli edustaa ostoskorin symbolia, joka ilmaisee, kuinka monta nimikettä ostoskorissa on tiettynä ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="156d9-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="156d9-129">Lisätietoja on kohdassa [Ostoskorikuvakemoduuli](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="156d9-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="156d9-130">Sivun ylätunnistemoduulin luominen</span><span class="sxs-lookup"><span data-stu-id="156d9-130">Create a header module for a page</span></span>

<span data-ttu-id="156d9-131">Voit luoda ylätunnistemoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="156d9-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="156d9-132">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="156d9-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="156d9-133">Valitse **Uusi sivun osa** -valintaikkunassa **Kontti**-moduuli. Syötä sivun osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-134">Valitse **Oletussäilö**-paikka ja määritä sitten Ominaisuudet-ruudussa oikealla puolella oleva **Leveys**-ominaisuuden arvoksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="156d9-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="156d9-135">Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="156d9-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156d9-136">Valitse **Lisää moduuli** -valintaikkunan **Kampanjabanneri**- ja **Hyväksy evästeet** -moduulit ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-137">Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="156d9-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156d9-138">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-139">Valitse **Säilö**-paikka ja määritä sitten Ominaisuudet-ruudussa oikealla puolella oleva **Leveys**-ominaisuuden arvoksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="156d9-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="156d9-140">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="156d9-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156d9-141">Valitse **Lisää moduuli** -valintaikkunassa **Otsikko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-142">Valitse otsikkomoduulissa **Siirtymisvalikko**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="156d9-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156d9-143">Valitse **Lisää moduuli** -valintaikkunassa **Siirtymisvalikko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-144">Määritä siirtymisvalikkomoduulin tarvittavat ominaisuudet ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="156d9-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="156d9-145">Valitse otsikkomoduulissa **Haku**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="156d9-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156d9-146">Valitse **Lisää moduuli** -valintaikkunassa **Haku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-147">Määritä hakumoduulin tarvittavat ominaisuudet ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="156d9-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="156d9-148">Valitse otsikkomoduulissa **Ostoskorikuvake**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="156d9-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156d9-149">Valitse **Lisää moduuli** -valintaikkunassa **Ostoskorikuvake**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="156d9-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="156d9-150">Määritä ostoskorikuvakemoduulin tarvittavat ominaisuudet ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="156d9-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="156d9-151">Jos haluat, että ostoskorikuvake näyttää ostoskorin yhteenvedon (joka tunnetaan myös nimellä pienoiskärry), kun käyttäjä vie osoittimen sen päälle, valitse **Näytä pienoiskärry**.</span><span class="sxs-lookup"><span data-stu-id="156d9-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="156d9-152">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="156d9-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="156d9-153">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="156d9-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="156d9-154">Lisää **Oletussivu**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.</span><span class="sxs-lookup"><span data-stu-id="156d9-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="156d9-155">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="156d9-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="156d9-156">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="156d9-156">Additional resources</span></span>

[<span data-ttu-id="156d9-157">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="156d9-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="156d9-158">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="156d9-159">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="156d9-160">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="156d9-161">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="156d9-162">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="156d9-163">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="156d9-164">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="156d9-165">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="156d9-165">Footer module</span></span>](author-footer-module.md)
