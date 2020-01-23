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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885475"
---
# <a name="header-module"></a><span data-ttu-id="ef9e8-103">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ef9e8-104">Tässä ohjeaiheessa on tietoja ylätunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ef9e8-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ef9e8-105">Overview</span></span>

<span data-ttu-id="ef9e8-106">Ylätunnistemoduuli on erityinen säilö, jota käytetään kaikkien sivun ylätunnisteessa näkyvien moduulien isännöinnissä.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="ef9e8-107">Se voi sisältää esimerkiksi sivuston logon, siirtymishierarkian linkit, sivuston muiden sivujen linkit ja hakupalkin..</span><span class="sxs-lookup"><span data-stu-id="ef9e8-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="ef9e8-108">Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten).</span><span class="sxs-lookup"><span data-stu-id="ef9e8-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="ef9e8-109">Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).</span><span class="sxs-lookup"><span data-stu-id="ef9e8-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="ef9e8-110">Ylätunnisteen ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="ef9e8-110">Properties of a header</span></span>

<span data-ttu-id="ef9e8-111">Ylätunnistemoduuli tukee yleisten säilöen tapaan **ylätunniste**- ja **leveys**-ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="ef9e8-112">Ylätunnistemoduulissa on useita paikkoja.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-112">A header module has multiple slots.</span></span> <span data-ttu-id="ef9e8-113">Paikkoja on esimerkiksi tietosanomassa, siirtymisvalikossa, logossa, hakupalkissa, ostoskorikuvakkeessa, toivomuslistakuvakkeessa ja tilin tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="ef9e8-114">Jokainen paikka tukee tiettyä moduulijoukkoa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="ef9e8-115">Ylätunnistemoduulin käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="ef9e8-115">Modules that are available in a header module</span></span>

<span data-ttu-id="ef9e8-116">Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:</span><span class="sxs-lookup"><span data-stu-id="ef9e8-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="ef9e8-117">**Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="ef9e8-118">Kanavan siirtymishierarkia voidaan määrittää Dynamics 365 Retail -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="ef9e8-119">Määritetyt nimikkeet näkyvät tämän jälkeen ylätunnisteen siirtymistoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="ef9e8-120">Lisäksi voidaan määrittää staattisia siirtymislinkkejä ja suhteellisia linkkejä muille sähköisen kaupankäynnin sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="ef9e8-121">Ylätunniste voidaan tasata vasemmalle, oikealle tai keskelle.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="ef9e8-122">**Ostoskorikuvake** – Ostoskorikuvake on erityinen kuvake ostoskoria varten.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="ef9e8-123">Se näkyy ylätunnisteessa ja osoittaa ostoskorin nimikkeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="ef9e8-124">Ostoskorisivun linkin yhteydessä on oltava ostoskorikuvake, jonka avulla asiakkaat ohjataan uudelleen ostoskorisivulle kuvakkeen valitsemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="ef9e8-125">**Toivomuslistakuvake** – Toivomuslistakuvake näkyy ylätunnisteessa. Se osoittaa asiakkaan toivomuslistaan lisättyjen nimikkeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="ef9e8-126">Toivomuslistasivun linkin yhteydessä on oltava tämä kuvake. Sen avulla asiakkaat ohjataan uudelleen toivomuslistasivulle kuvakkeen valitsemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="ef9e8-127">**Sisäänkirjausmoduuli** – Sisäänkirjautumismoduuli näkyy ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="ef9e8-128">Sen avulla asiakkaat voivat kirjautua sisään tilille tai rekisteröityä tilille.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="ef9e8-129">Jos asiakas on jo kirjautunut sisään, moduuli voidaan määrittää näyttämään linkit tilisivulle, tilaushistoriasivulle tai toiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="ef9e8-130">**Logomoduuli** – Tämä moduuli näyttää logon, joka edustaa jälleenmyyjää ja tuotemerkkiä.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="ef9e8-131">Se on kuva, jossa on linkki.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-131">It's an image that has a link.</span></span> <span data-ttu-id="ef9e8-132">Linkki määritetään yleensä niin, että se ohjaa uudelleen aloitussivulle. Tämän vuoksi asiakkaat voivat nopeasti palata aloitussivulle miltä tahansa sivuston sivulta.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="ef9e8-133">**Hälytys** – Hälytys näkyy ylätunnisteessa. Sitä käytetään sivuston kaikkia sivuja koskevan sisäisen sanoman näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="ef9e8-134">Hälytys voi esimerkiksi näyttää Vuosittainen alennus päättyy 2 päivän kuluttua -sanoman.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="ef9e8-135">**Hakupalkki** – Hakupalkin avulla käyttäjät voivat syöttää hakusanoja ja etsiä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="ef9e8-136">Moduulissa on määritettävä hakutulossivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="ef9e8-137">Kyselymerkkijonon parametri voidaan määrittää (oletusarvo on **q**).</span><span class="sxs-lookup"><span data-stu-id="ef9e8-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="ef9e8-138">Hakupalkissa on automaattisen ehdotuksen paikka, johon automaattisen ehdotuksen moduuli lisätään.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="ef9e8-139">**Automaattinen ehdotus** – Automaattisesti ehdotetut tulokset näytetään automaattisen ehdotuksen moduulissa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="ef9e8-140">Nämä tulokset voivat olla avainsanoja, tuotteita tai luokkia, joista hakusana löytyy.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="ef9e8-141">Ylätunnistemoduulin luominen</span><span class="sxs-lookup"><span data-stu-id="ef9e8-141">Create a header module</span></span>

<span data-ttu-id="ef9e8-142">Voit luoda ylätunnistemoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="ef9e8-143">Luo sivun osa, jossa ylätunnistemoduuli on.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="ef9e8-144">Lisää moduulit ylätunnistemoduulin paikkoihin.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="ef9e8-145">Päivitä kunkin moduulin asetukset.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="ef9e8-146">Tallenna sivun osa.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="ef9e8-147">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="ef9e8-148">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="ef9e8-149">Lisää oletussivun ylätunnisteen pääpaikkaan sivun osa, joka sisältää ylätunnistemoduulin.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="ef9e8-150">Tallenna malli.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-150">Save the template.</span></span> 
1. <span data-ttu-id="ef9e8-151">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="ef9e8-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef9e8-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ef9e8-152">Additional resources</span></span>

[<span data-ttu-id="ef9e8-153">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ef9e8-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ef9e8-154">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ef9e8-155">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ef9e8-156">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ef9e8-157">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ef9e8-158">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ef9e8-159">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ef9e8-160">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ef9e8-160">Footer module</span></span>](author-footer-module.md)
