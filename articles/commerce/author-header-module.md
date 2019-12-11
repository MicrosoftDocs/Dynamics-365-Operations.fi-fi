---
title: Ylätunnistemoduuli
description: Tässä ohjeaiheessa on tietoja ylätunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697272"
---
# <a name="header-module"></a><span data-ttu-id="8f37b-103">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-103">Header module</span></span>

<span data-ttu-id="8f37b-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="8f37b-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="8f37b-105">Tässä ohjeaiheessa on tietoja ylätunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="8f37b-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8f37b-106">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8f37b-106">Overview</span></span>

<span data-ttu-id="8f37b-107">Ylätunnistemoduuli on erityinen säilö, jota käytetään kaikkien sivun ylätunnisteessa näkyvien moduulien isännöinnissä.</span><span class="sxs-lookup"><span data-stu-id="8f37b-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="8f37b-108">Se voi sisältää esimerkiksi sivuston logon, siirtymishierarkian linkit, sivuston muiden sivujen linkit ja hakupalkin..</span><span class="sxs-lookup"><span data-stu-id="8f37b-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="8f37b-109">Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten).</span><span class="sxs-lookup"><span data-stu-id="8f37b-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="8f37b-110">Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).</span><span class="sxs-lookup"><span data-stu-id="8f37b-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="8f37b-111">Ylätunnisteen ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8f37b-111">Properties of a header</span></span>

<span data-ttu-id="8f37b-112">Ylätunnistemoduuli tukee yleisten säilöen tapaan **ylätunniste**- ja **leveys**-ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="8f37b-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="8f37b-113">Ylätunnistemoduulissa on useita paikkoja.</span><span class="sxs-lookup"><span data-stu-id="8f37b-113">A header module has multiple slots.</span></span> <span data-ttu-id="8f37b-114">Paikkoja on esimerkiksi tietosanomassa, siirtymisvalikossa, logossa, hakupalkissa, ostoskorikuvakkeessa, toivomuslistakuvakkeessa ja tilin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="8f37b-115">Jokainen paikka tukee tiettyä moduulijoukkoa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="8f37b-116">Ylätunnistemoduulin käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="8f37b-116">Modules that are available in a header module</span></span>

<span data-ttu-id="8f37b-117">Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:</span><span class="sxs-lookup"><span data-stu-id="8f37b-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="8f37b-118">**Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä.</span><span class="sxs-lookup"><span data-stu-id="8f37b-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="8f37b-119">Kanavan siirtymishierarkia voidaan määrittää Dynamics 365 Retail -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="8f37b-120">Määritetyt nimikkeet näkyvät tämän jälkeen ylätunnisteen siirtymistoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="8f37b-121">Lisäksi voidaan määrittää staattisia siirtymislinkkejä ja suhteellisia linkkejä muille sähköisen kaupankäynnin sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="8f37b-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="8f37b-122">Ylätunniste voidaan tasata vasemmalle, oikealle tai keskelle.</span><span class="sxs-lookup"><span data-stu-id="8f37b-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="8f37b-123">**Ostoskorikuvake** – Ostoskorikuvake on erityinen kuvake ostoskoria varten.</span><span class="sxs-lookup"><span data-stu-id="8f37b-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="8f37b-124">Se näkyy ylätunnisteessa ja osoittaa ostoskorin nimikkeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="8f37b-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="8f37b-125">Ostoskorisivun linkin yhteydessä on oltava ostoskorikuvake, jonka avulla asiakkaat ohjataan uudelleen ostoskorisivulle kuvakkeen valitsemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8f37b-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="8f37b-126">**Toivomuslistakuvake** – Toivomuslistakuvake näkyy ylätunnisteessa. Se osoittaa asiakkaan toivomuslistaan lisättyjen nimikkeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="8f37b-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="8f37b-127">Toivomuslistasivun linkin yhteydessä on oltava tämä kuvake. Sen avulla asiakkaat ohjataan uudelleen toivomuslistasivulle kuvakkeen valitsemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8f37b-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="8f37b-128">**Sisäänkirjausmoduuli** – Sisäänkirjautumismoduuli näkyy ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="8f37b-129">Sen avulla asiakkaat voivat kirjautua sisään tilille tai rekisteröityä tilille.</span><span class="sxs-lookup"><span data-stu-id="8f37b-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="8f37b-130">Jos asiakas on jo kirjautunut sisään, moduuli voidaan määrittää näyttämään linkit tilisivulle, tilaushistoriasivulle tai toiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="8f37b-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="8f37b-131">**Logomoduuli** – Tämä moduuli näyttää logon, joka edustaa jälleenmyyjää ja tuotemerkkiä.</span><span class="sxs-lookup"><span data-stu-id="8f37b-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="8f37b-132">Se on kuva, jossa on linkki.</span><span class="sxs-lookup"><span data-stu-id="8f37b-132">It's an image that has a link.</span></span> <span data-ttu-id="8f37b-133">Linkki määritetään yleensä niin, että se ohjaa uudelleen aloitussivulle. Tämän vuoksi asiakkaat voivat nopeasti palata aloitussivulle miltä tahansa sivuston sivulta.</span><span class="sxs-lookup"><span data-stu-id="8f37b-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="8f37b-134">**Hälytys** – Hälytys näkyy ylätunnisteessa. Sitä käytetään sivuston kaikkia sivuja koskevan sisäisen sanoman näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="8f37b-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="8f37b-135">Hälytys voi esimerkiksi näyttää Vuosittainen alennus päättyy 2 päivän kuluttua -sanoman.</span><span class="sxs-lookup"><span data-stu-id="8f37b-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="8f37b-136">**Hakupalkki** – Hakupalkin avulla käyttäjät voivat syöttää hakusanoja ja etsiä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="8f37b-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="8f37b-137">Moduulissa on määritettävä hakutulossivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="8f37b-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="8f37b-138">Kyselymerkkijonon parametri voidaan määrittää (oletusarvo on **q**).</span><span class="sxs-lookup"><span data-stu-id="8f37b-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="8f37b-139">Hakupalkissa on automaattisen ehdotuksen paikka, johon automaattisen ehdotuksen moduuli lisätään.</span><span class="sxs-lookup"><span data-stu-id="8f37b-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="8f37b-140">**Automaattinen ehdotus** – Automaattisesti ehdotetut tulokset näytetään automaattisen ehdotuksen moduulissa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="8f37b-141">Nämä tulokset voivat olla avainsanoja, tuotteita tai luokkia, joista hakusana löytyy.</span><span class="sxs-lookup"><span data-stu-id="8f37b-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="8f37b-142">Ylätunnistemoduulin luominen</span><span class="sxs-lookup"><span data-stu-id="8f37b-142">Create a header module</span></span>

<span data-ttu-id="8f37b-143">Voit luoda ylätunnistemoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8f37b-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="8f37b-144">Luo sivun osa, jossa ylätunnistemoduuli on.</span><span class="sxs-lookup"><span data-stu-id="8f37b-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="8f37b-145">Lisää moduulit ylätunnistemoduulin paikkoihin.</span><span class="sxs-lookup"><span data-stu-id="8f37b-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="8f37b-146">Päivitä kunkin moduulin asetukset.</span><span class="sxs-lookup"><span data-stu-id="8f37b-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="8f37b-147">Tallenna sivun osa.</span><span class="sxs-lookup"><span data-stu-id="8f37b-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="8f37b-148">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="8f37b-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="8f37b-149">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="8f37b-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="8f37b-150">Lisää oletussivun ylätunnisteen pääpaikkaan sivun osa, joka sisältää ylätunnistemoduulin.</span><span class="sxs-lookup"><span data-stu-id="8f37b-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="8f37b-151">Tallenna malli.</span><span class="sxs-lookup"><span data-stu-id="8f37b-151">Save the template.</span></span> 
1. <span data-ttu-id="8f37b-152">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="8f37b-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f37b-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8f37b-153">Additional resources</span></span>

[<span data-ttu-id="8f37b-154">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8f37b-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8f37b-155">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8f37b-156">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8f37b-157">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8f37b-158">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8f37b-159">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8f37b-160">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8f37b-161">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8f37b-161">Footer module</span></span>](author-footer-module.md)
