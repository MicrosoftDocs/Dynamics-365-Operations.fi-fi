---
title: Moduulikirjaston yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen moduulikirjastosta.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4b3440c046ff055c8afa012c80c56aba741fef27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985558"
---
# <a name="module-library-overview"></a><span data-ttu-id="e96d9-103">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e96d9-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e96d9-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen moduulikirjastosta.</span><span class="sxs-lookup"><span data-stu-id="e96d9-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

## <a name="overview"></a><span data-ttu-id="e96d9-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e96d9-105">Overview</span></span>

<span data-ttu-id="e96d9-106">Dynamics 365 Commercen moduulikirjasto on moduulikokoelma, jota voi käyttää sähköisen kaupankäynnin sivuston luomisessa.</span><span class="sxs-lookup"><span data-stu-id="e96d9-106">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="e96d9-107">Moduuleilla on sekä käyttöliittymänäkökulmat että toiminnalliset näkökulmat.</span><span class="sxs-lookup"><span data-stu-id="e96d9-107">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="e96d9-108">Moduulikirjaston moduuleihin voi kohdistaa teemoja ja muuttaa niiden ulkoasua.</span><span class="sxs-lookup"><span data-stu-id="e96d9-108">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="e96d9-109">Teemat käyttävät CSS-tyylisivuja (CSS).</span><span class="sxs-lookup"><span data-stu-id="e96d9-109">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="e96d9-110">Kuvitteellisen verkkokauppasivuston, jonka nimi on Fabrikam, teema on mukana moduulikirjaston osana ja sitä voidaan käyttää viitteenä.</span><span class="sxs-lookup"><span data-stu-id="e96d9-110">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="e96d9-111">Moduulikirjaston moduulit</span><span class="sxs-lookup"><span data-stu-id="e96d9-111">Module library modules</span></span>

<span data-ttu-id="e96d9-112">Seuraavat moduulit ovat mukana moduulikirjastossa:</span><span class="sxs-lookup"><span data-stu-id="e96d9-112">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="e96d9-113">**Säilömoduuli** – Säilömoduuli on yksinkertainen moduuli, joka toimii isäntänä muille moduuleille.</span><span class="sxs-lookup"><span data-stu-id="e96d9-113">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="e96d9-114">Se ohjaa sen sisällään olevien moduulien asettelua.</span><span class="sxs-lookup"><span data-stu-id="e96d9-114">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="e96d9-115">**Markkinointimoduulit** – Markkinointimoduulit sisältävät sisältölohkon, tekstilohkon, videotoistimen ja karusellimoduulit.</span><span class="sxs-lookup"><span data-stu-id="e96d9-115">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="e96d9-116">Kaikkia näitä moduuleja voidaan käyttää sisällön esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="e96d9-116">All these modules can be used to showcase content.</span></span> <span data-ttu-id="e96d9-117">Ne voidaan asettaa mille tahansa sivulle. Niitä ohjaavat sisällönhallintajärjestelmän (CMS) tiedot.</span><span class="sxs-lookup"><span data-stu-id="e96d9-117">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="e96d9-118">**Ylä- ja alatunnistemoduulit** Ylä- ja alatunnistemoduulit näkyvät kaikkien sivuston sivujen ylä- ja alatunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="e96d9-118">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="e96d9-119">Nämä moduulit voidaan määrittää tarpeen mukaan ominaisuuksien avulla.</span><span class="sxs-lookup"><span data-stu-id="e96d9-119">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="e96d9-120">**Hakumoduulit** – Tuotteet voidaan löytää käyttämällä ylätunnisteen hakumoduulia.</span><span class="sxs-lookup"><span data-stu-id="e96d9-120">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="e96d9-121">Hakutulokset näkyvät hakutulossivulla.</span><span class="sxs-lookup"><span data-stu-id="e96d9-121">Search results appear on the search results page.</span></span> <span data-ttu-id="e96d9-122">Tuotteita voi etsiä myös luokkasivuilta. Ne ovat kullekin kanavan siirtymishierarkiassa tuetuille luokalle varattuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="e96d9-122">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="e96d9-123">Lisäksi muokkaajamoduuleja voi käyttää hakutulosten ja luokkasivujen lisäsuodatuksessa.</span><span class="sxs-lookup"><span data-stu-id="e96d9-123">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="e96d9-124">**Tuotetietosivumoduulit** – Tuotetietosivut käyttävät useita moduuleja tuotetietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="e96d9-124">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="e96d9-125">Ostoruutumoduulin avulla asiakkaat voivat tarkastella tuotteita ja lisätä niitä ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="e96d9-125">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="e96d9-126">Muut moduulit, kuten teknisten tietojen moduuli, näyttävät tuotetietoja.</span><span class="sxs-lookup"><span data-stu-id="e96d9-126">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="e96d9-127">Luokitusten ja arvostelujen moduulin avulla voidaan tarkastella arvosteluja ja syöttää niitä.</span><span class="sxs-lookup"><span data-stu-id="e96d9-127">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="e96d9-128">**Osta verkosta, nouda myymälästä -moduuli** – Osta verkosta, nouda myymälästä -moduuli on integroitu Bing Maps -sovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e96d9-128">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="e96d9-129">Sitä voi käyttää lähellä olevien myymälöiden etsimisessä. Asiakkaat voivat noutaa niistä ostamiaan tuotteita.</span><span class="sxs-lookup"><span data-stu-id="e96d9-129">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="e96d9-130">**Ostomoduulit** – Ostomoduulit sisältävät ostoskorimoduulin, jota voi käyttää nimikkeiden lisäämisessä ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="e96d9-130">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="e96d9-131">Kassamoduuli kerää toimitusosoitteen, toimitusvaihtoehdot ja lahjakortin, kanta-asiakasohjelman ja luottokortin tiedot tilauksen käsittelemistä varten.</span><span class="sxs-lookup"><span data-stu-id="e96d9-131">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="e96d9-132">Kun tilaus on tehty, vahvistustiedot voidaan näyttää tilauksen vahvistuksen moduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="e96d9-132">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="e96d9-133">**Tilinhallintamoduulit** – Sisäänkirjautumismoduulin avulla asiakkaat voivat kirjautua sisään olemassa olevalle tilille ja rekisteröitymismoduulin avulla he voivat luoda uuden tilin.</span><span class="sxs-lookup"><span data-stu-id="e96d9-133">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="e96d9-134">Kun tili on luotu, viimeaikaisia tilauksia voi tarkastella tilaushistoriamoduulin avulla. Tilauksen tietoja voi tarkastella tilaustietojen moduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="e96d9-134">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="e96d9-135">**Suositusten moduuli** – Suositukset näytetään tuotteensijoittelumoduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="e96d9-135">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="e96d9-136">Tämä moduuli tukee algoritmiluetteloita ja toimituksellisia luetteloita, jotka voidaan esitellä millä tahansa sivulla.</span><span class="sxs-lookup"><span data-stu-id="e96d9-136">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e96d9-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e96d9-137">Additional resources</span></span>

[<span data-ttu-id="e96d9-138">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-138">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e96d9-139">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e96d9-140">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-140">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e96d9-141">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e96d9-142">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-142">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e96d9-143">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-143">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e96d9-144">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e96d9-144">Footer module</span></span>](author-footer-module.md)
