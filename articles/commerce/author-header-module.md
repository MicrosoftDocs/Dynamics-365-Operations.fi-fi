---
title: Ylätunnistemoduuli
description: Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025654"
---
# <a name="header-module"></a><span data-ttu-id="4eaf5-103">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4eaf5-104">Tässä ohjeaiheessa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4eaf5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4eaf5-105">Overview</span></span>

<span data-ttu-id="4eaf5-106">Dynamics 365 Commercessa sivun ylätunniste koostuu useita moduuleista, kuten ylätunniste-, siirtymisvalikko-, haku-, mainosbanneri- ja evästehyväksyntämoduuleista.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="4eaf5-107">Ylätunnistemoduuli sisältää sivuston logon, linkit siirtymishierarkiaan, linkit muille sivuston sivuille, ostoskorisymbolin, toivelistasymbolin, kirjautumisvaihtoehdot ja hakupalkin.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="4eaf5-108">Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten).</span><span class="sxs-lookup"><span data-stu-id="4eaf5-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="4eaf5-109">Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).</span><span class="sxs-lookup"><span data-stu-id="4eaf5-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="4eaf5-110">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4eaf5-110">Properties of a header module</span></span>

<span data-ttu-id="4eaf5-111">Ylätunnistemoduuli tukee **Logon kuva**-, **Logon linkki**- ja **Oman tilin linkit** -ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="4eaf5-112">**Logon kuva**- ja **Logon linkki** -ominaisuuksilla määritetään sivulla oleva logo.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="4eaf5-113">Lisätietoja on kohdassa [Logon lisääminen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="4eaf5-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="4eaf5-114">**Oman tilin linkit** -ominaisuudella voidaan määrittää ne tilisivut, joiden pikalinkit sivuston omistaja haluaa näyttää ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="4eaf5-115">Ylätunnistemoduulin käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="4eaf5-115">Modules that are available in a header module</span></span>

<span data-ttu-id="4eaf5-116">Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:</span><span class="sxs-lookup"><span data-stu-id="4eaf5-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="4eaf5-117">**Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="4eaf5-118">Kanavan siirtymishierarkia voidaan määrittää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4eaf5-119">Siirtymisvalikossa on **Siirtymisen lähde** -ominaisuus, jolla määritetään Retail Serverin siirtymisvalikon vaihtoehdot ja staattiset valikkovaihtoehdot lähteeksi.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="4eaf5-120">Jos staattiset valikkovaihtoehdot määritetään lähteeksi, sivuston muille sivulle voidaan antaa suhteelliset linkit.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="4eaf5-121">Määritetyt nimikkeet näkyvät tämän jälkeen ylätunnisteen siirtymistoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="4eaf5-122">**Haku** – Hakumoduulin avulla käyttäjät voivat etsiä tuotteita hakusanojen avulla.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="4eaf5-123">Oletushakusivun URL-osoite ja hakukyselyn parametrit on annettava valitsemalla **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="4eaf5-124">Hakumoduulissa on ominaisuuksia, joiden avulla voit estää hakupainikkeen tai -selitteen tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="4eaf5-125">Hakumoduuli tukee myös automaattisia ehdotuksia, kuten tuotteen, avainsanan ja luokan hakutuloksia.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="4eaf5-126">Sivun ylätunnistemoduulin luominen</span><span class="sxs-lookup"><span data-stu-id="4eaf5-126">Create a header module for a page</span></span>

<span data-ttu-id="4eaf5-127">Voit luoda ylätunnistemoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="4eaf5-128">Luo **Ylätunnisteosa**-niminen osa ja lisää siihen säilömoduuli.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="4eaf5-129">Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="4eaf5-130">Lisää mainosbanneri- ja evästehyväksyntämoduulit säilömoduuliin.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="4eaf5-131">Lisää osaan toinen säilömoduuli ja määritä **Leveys**-ominaisuudeksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="4eaf5-132">Lisää ylätunnistemoduuli toiseen säilömoduuliin.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="4eaf5-133">Lisää siirtymisvalikkomoduuli ylätunnistemoduulin **Siirtymisvalikko**-paikkaan.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="4eaf5-134">Määritä siirtymisvalikkomoduulin ominaisuusruudussa siirtymisvalikkomoduulin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="4eaf5-135">Lisää hakumoduuli ylätunnistemoduulin **Haku**-paikkaan.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="4eaf5-136">Määritä hakumoduulin ominaisuusruudussa hakumoduulin ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="4eaf5-137">Tallenna sivuosa, lopeta sen muokkaus ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="4eaf5-138">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="4eaf5-139">Lisää oletussivun **Otsikko**-paikassa ylätunnisteeseen ylätunnistemoduulin sisältävä ylätunniste-sivuosa.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="4eaf5-140">Tallenna malli, lopeta sen muokkaus ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="4eaf5-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4eaf5-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4eaf5-141">Additional resources</span></span>

[<span data-ttu-id="4eaf5-142">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4eaf5-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4eaf5-143">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4eaf5-144">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4eaf5-145">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4eaf5-146">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4eaf5-147">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4eaf5-148">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4eaf5-149">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4eaf5-149">Footer module</span></span>](author-footer-module.md)
