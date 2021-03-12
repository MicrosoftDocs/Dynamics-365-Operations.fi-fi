---
title: Ylätunnistemoduuli
description: Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1373397c4499ed65835bcc71c6fc628ff356e4e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991512"
---
# <a name="header-module"></a><span data-ttu-id="674f0-103">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="674f0-104">Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="674f0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="674f0-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="674f0-105">Overview</span></span>

<span data-ttu-id="674f0-106">Dynamics 365 Commercen sivun otsikko on määritetty sivun osaksi, joka sisältää otsikon, kampanjabannerin ja evästeiden hyväksyntämoduulit.</span><span class="sxs-lookup"><span data-stu-id="674f0-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="674f0-107">Ylätunnistemoduuli sisältää sivuston logon, linkit siirtymishierarkiaan, linkit muille sivuston sivuille, ostoskorim kuvakkeen moduulin, toivelistasymbolin, kirjautumisvaihtoehdot ja hakupalkin.</span><span class="sxs-lookup"><span data-stu-id="674f0-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="674f0-108">Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten).</span><span class="sxs-lookup"><span data-stu-id="674f0-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="674f0-109">Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).</span><span class="sxs-lookup"><span data-stu-id="674f0-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="674f0-110">Seuraavassa kuvassa on esimerkki otsikkomoduulista kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="674f0-110">The following image shows an example of a header module on a home page.</span></span>

![Esimerkki otsikkomoduulista](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="674f0-112">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="674f0-112">Properties of a header module</span></span>

<span data-ttu-id="674f0-113">Ylätunnistemoduuli tukee **Logon kuva**-, **Logon linkki**- ja **Oman tilin linkit** -ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="674f0-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="674f0-114">**Logon kuva**- ja **Logon linkki** -ominaisuuksilla määritetään sivulla oleva logo.</span><span class="sxs-lookup"><span data-stu-id="674f0-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="674f0-115">Lisätietoja on kohdassa [Logon lisääminen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="674f0-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="674f0-116">**Oman tilin linkit** -ominaisuudella voidaan määrittää ne tilisivut, joiden pikalinkit sivuston omistaja haluaa näyttää ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="674f0-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="674f0-117">Ylätunnistemoduulin käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="674f0-117">Modules that are available within a header module</span></span>

<span data-ttu-id="674f0-118">Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:</span><span class="sxs-lookup"><span data-stu-id="674f0-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="674f0-119">**Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä.</span><span class="sxs-lookup"><span data-stu-id="674f0-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="674f0-120">Lisätietoja on kohdassa [Siirtymisvalikkomoduuli](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="674f0-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="674f0-121">**Haku** – Hakumoduulin avulla käyttäjät voivat etsiä tuotteita hakusanojen avulla.</span><span class="sxs-lookup"><span data-stu-id="674f0-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="674f0-122">Oletushakusivun URL-osoite ja hakukyselyn parametrit on annettava valitsemalla **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="674f0-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="674f0-123">Hakumoduulissa on ominaisuuksia, joiden avulla voit estää hakupainikkeen tai -selitteen tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="674f0-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="674f0-124">Hakumoduuli tukee myös automaattisia ehdotuksia, kuten tuotteen, avainsanan ja luokan hakutuloksia.</span><span class="sxs-lookup"><span data-stu-id="674f0-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="674f0-125">**Ostoskorikuvake** – Ostoskorikuvakemoduuli edustaa ostoskorin symbolia, joka ilmaisee, kuinka monta nimikettä ostoskorissa on tiettynä ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="674f0-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="674f0-126">Lisätietoja on kohdassa [Ostoskorikuvakemoduuli](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="674f0-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="674f0-127">**Toimipaikan valitsin** – Toimipaikan valitsinmoduulissa käyttäjät voivat selata esimääritettyjä toimipaikkoja markkina-alueen, alueiden ja kielialueiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="674f0-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="674f0-128">Lisätietoja on kohdassa [Toimipaikan valitsinmoduuli](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="674f0-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="674f0-129">**Myymälän valitsin** – Myymälän valitsinmoduuli voidaan sisällyttää otsikon myymälän valitsinpaikkaan.</span><span class="sxs-lookup"><span data-stu-id="674f0-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="674f0-130">Sen avulla käyttäjät voivat selata ja etsiä lähellä olevia myymälöitä.</span><span class="sxs-lookup"><span data-stu-id="674f0-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="674f0-131">Käyttäjät voivat määrittää myös ensisijaisen myymälän.</span><span class="sxs-lookup"><span data-stu-id="674f0-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="674f0-132">Kyseinen myymälä näytetään sitten otsikossa.</span><span class="sxs-lookup"><span data-stu-id="674f0-132">That store will then be shown in the header.</span></span> <span data-ttu-id="674f0-133">Jos myymälän valitsinmoduuli sisältyy otsikkomoduuliin, sen **Tila**-ominaisuudeksi on määritettävä **Etsi myymälät**.</span><span class="sxs-lookup"><span data-stu-id="674f0-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="674f0-134">Lisätietoja on kohdassa [Myymälän valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="674f0-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="674f0-135">Otsikkomoduulien kortin kuvakemoduulin tuki on saatavana Dynamics 365 Commercen versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="674f0-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="674f0-136">Otsikkomoduulien toimipaikan valitsinmoduulin tuki on saatavana Dynamics 365 Commercen versiossa 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="674f0-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="674f0-137">Otsikkomoduulien myymälän valitsinmoduulin tuki on saatavana Dynamics 365 Commercen versiossa 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="674f0-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="674f0-138">Sivun otsikko-osan luominen</span><span class="sxs-lookup"><span data-stu-id="674f0-138">Create a header fragment for a page</span></span>

<span data-ttu-id="674f0-139">Voit luoda otsikko-osan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="674f0-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="674f0-140">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="674f0-140">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="674f0-141">Valitse **Uusi osa** -valintaikkunassa **Kontti**-moduuli. Syötä osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="674f0-142">Valitse **Oletussäilö**-paikka ja määritä sitten Ominaisuudet-ruudussa oikealla puolella oleva **Leveys**-ominaisuuden arvoksi **Täytä näyttö**.</span><span class="sxs-lookup"><span data-stu-id="674f0-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="674f0-143">Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="674f0-143">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="674f0-144">Valitse **Lisää moduuli** -valintaikkunassa **Evästeiden hyväksyntä**-, **Otsikko**- ja **Kampanjabanneri**-moduulit ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-144">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="674f0-145">Valitse **Kampanjabanneri**-moduulin ominaisuusruudussa **Lisää sanoma** ja valitse sitten **Sanoma**.</span><span class="sxs-lookup"><span data-stu-id="674f0-145">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="674f0-146">Lisää **Sanoma**-valintaruutuun teksti ja linkit mainossisältöä varten ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="674f0-147">Lisää **evästeiden hyväksyntämoduulin** ominaisuusruudussa teksti ja muokkaa sitä. Linkitä teksti sivuston tietosuojakäytännön sivulle.</span><span class="sxs-lookup"><span data-stu-id="674f0-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="674f0-148">Valitse otsikkomoduulissa **Siirtymisvalikko**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="674f0-148">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="674f0-149">Valitse **Lisää moduuli** -valintaikkunassa **Siirtymisvalikko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="674f0-150">Valitse siirtymisvalikkomoduulin ominaisuusruudun **Siirtymisvalikon lähde** -kohdassa **Retail Server**.</span><span class="sxs-lookup"><span data-stu-id="674f0-150">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="674f0-151">Valitse siirtymisvalikkomoduulin ominaisuusruudun **Staattiset valikon vaihtoehdot** -kohdassa **Lisää valikon vaihtoehto** ja valitse sitten **Valikon vaihtoehto**.</span><span class="sxs-lookup"><span data-stu-id="674f0-151">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="674f0-152">Syötä **Valikon vaihtoehto** -valintaruudun **Valikon vaihtoehdon teksti** -kohtaan Yhteyshenkilö.</span><span class="sxs-lookup"><span data-stu-id="674f0-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="674f0-153">Valitse **Valikon vaihtoehto** -valintaruudun **Valikon vaihtoehdon linkin kohde** -kohdassa **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="674f0-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="674f0-154">Valitse **Lisää linkki** -valintaikkunassa sivuston yhteyshenkilösivun URL-osoite ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="674f0-155">Valitse **Valikon vaihtoehto** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="674f0-156">Valitse otsikkomoduulissa **Haku**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="674f0-156">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="674f0-157">Valitse **Lisää moduuli** -valintaikkunassa **Haku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="674f0-158">Määritä hakumoduulin tarvittavat ominaisuudet ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="674f0-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="674f0-159">Valitse otsikkomoduulissa **Ostoskorikuvake**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="674f0-159">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="674f0-160">Valitse **Lisää moduuli** -valintaikkunassa **Ostoskorikuvake**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="674f0-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="674f0-161">Määritä ostoskorikuvakemoduulin tarvittavat ominaisuudet ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="674f0-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="674f0-162">Jos haluat, että ostoskorikuvake näyttää ostoskorin yhteenvedon (joka tunnetaan myös nimellä pienoiskärry), kun käyttäjä vie osoittimen sen päälle, valitse **Näytä pienoiskärry**.</span><span class="sxs-lookup"><span data-stu-id="674f0-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="674f0-163">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="674f0-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="674f0-164">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="674f0-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="674f0-165">Lisää **Oletussivu**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.</span><span class="sxs-lookup"><span data-stu-id="674f0-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="674f0-166">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="674f0-166">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="674f0-167">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="674f0-167">Additional resources</span></span>

[<span data-ttu-id="674f0-168">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="674f0-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="674f0-169">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="674f0-170">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="674f0-171">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="674f0-172">Siirtymisvalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="674f0-173">Evästeiden hyväksyntä</span><span class="sxs-lookup"><span data-stu-id="674f0-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="674f0-174">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="674f0-175">Toimipaikan valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="674f0-176">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="674f0-176">Store selector module</span></span>](store-selector.md)
