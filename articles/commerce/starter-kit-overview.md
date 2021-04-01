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
ms.openlocfilehash: fcb0c2317315308de51d8247d23a930f10c3de6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234290"
---
# <a name="module-library-overview"></a><span data-ttu-id="e08bc-103">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e08bc-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e08bc-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen moduulikirjastosta.</span><span class="sxs-lookup"><span data-stu-id="e08bc-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="e08bc-105">Dynamics 365 Commercen moduulikirjasto on moduulikokoelma, jota voi käyttää sähköisen kaupankäynnin sivuston luomisessa.</span><span class="sxs-lookup"><span data-stu-id="e08bc-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="e08bc-106">Moduuleilla on sekä käyttöliittymänäkökulmat että toiminnalliset näkökulmat.</span><span class="sxs-lookup"><span data-stu-id="e08bc-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="e08bc-107">Moduulikirjaston moduuleihin voi kohdistaa teemoja ja muuttaa niiden ulkoasua.</span><span class="sxs-lookup"><span data-stu-id="e08bc-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="e08bc-108">Teemat käyttävät CSS-tyylisivuja (CSS).</span><span class="sxs-lookup"><span data-stu-id="e08bc-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="e08bc-109">Kuvitteellisen verkkokauppasivuston, jonka nimi on Fabrikam, teema on mukana moduulikirjaston osana ja sitä voidaan käyttää viitteenä.</span><span class="sxs-lookup"><span data-stu-id="e08bc-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="e08bc-110">Moduulikirjaston moduulit</span><span class="sxs-lookup"><span data-stu-id="e08bc-110">Module library modules</span></span>

<span data-ttu-id="e08bc-111">Seuraavat moduulit ovat mukana moduulikirjastossa:</span><span class="sxs-lookup"><span data-stu-id="e08bc-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="e08bc-112">**Säilömoduuli** – Säilömoduuli on yksinkertainen moduuli, joka toimii isäntänä muille moduuleille.</span><span class="sxs-lookup"><span data-stu-id="e08bc-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="e08bc-113">Se ohjaa sen sisällään olevien moduulien asettelua.</span><span class="sxs-lookup"><span data-stu-id="e08bc-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="e08bc-114">**Markkinointimoduulit** – Markkinointimoduulit sisältävät sisältölohkon, tekstilohkon, videotoistimen ja karusellimoduulit.</span><span class="sxs-lookup"><span data-stu-id="e08bc-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="e08bc-115">Kaikkia näitä moduuleja voidaan käyttää sisällön esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="e08bc-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="e08bc-116">Ne voidaan asettaa mille tahansa sivulle. Niitä ohjaavat sisällönhallintajärjestelmän (CMS) tiedot.</span><span class="sxs-lookup"><span data-stu-id="e08bc-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="e08bc-117">**Ylä- ja alatunnistemoduulit** Ylä- ja alatunnistemoduulit näkyvät kaikkien sivuston sivujen ylä- ja alatunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="e08bc-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="e08bc-118">Nämä moduulit voidaan määrittää tarpeen mukaan ominaisuuksien avulla.</span><span class="sxs-lookup"><span data-stu-id="e08bc-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="e08bc-119">**Hakumoduulit** – Tuotteet voidaan löytää käyttämällä ylätunnisteen hakumoduulia.</span><span class="sxs-lookup"><span data-stu-id="e08bc-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="e08bc-120">Hakutulokset näkyvät hakutulossivulla.</span><span class="sxs-lookup"><span data-stu-id="e08bc-120">Search results appear on the search results page.</span></span> <span data-ttu-id="e08bc-121">Tuotteita voi etsiä myös luokkasivuilta. Ne ovat kullekin kanavan siirtymishierarkiassa tuetuille luokalle varattuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="e08bc-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="e08bc-122">Lisäksi muokkaajamoduuleja voi käyttää hakutulosten ja luokkasivujen lisäsuodatuksessa.</span><span class="sxs-lookup"><span data-stu-id="e08bc-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="e08bc-123">**Tuotetietosivumoduulit** – Tuotetietosivut käyttävät useita moduuleja tuotetietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="e08bc-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="e08bc-124">Ostoruutumoduulin avulla asiakkaat voivat tarkastella tuotteita ja lisätä niitä ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="e08bc-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="e08bc-125">Muut moduulit, kuten teknisten tietojen moduuli, näyttävät tuotetietoja.</span><span class="sxs-lookup"><span data-stu-id="e08bc-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="e08bc-126">Luokitusten ja arvostelujen moduulin avulla voidaan tarkastella arvosteluja ja syöttää niitä.</span><span class="sxs-lookup"><span data-stu-id="e08bc-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="e08bc-127">**Osta verkosta, nouda myymälästä -moduuli** – Osta verkosta, nouda myymälästä -moduuli on integroitu Bing Maps -sovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e08bc-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="e08bc-128">Sitä voi käyttää lähellä olevien myymälöiden etsimisessä. Asiakkaat voivat noutaa niistä ostamiaan tuotteita.</span><span class="sxs-lookup"><span data-stu-id="e08bc-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="e08bc-129">**Ostomoduulit** – Ostomoduulit sisältävät ostoskorimoduulin, jota voi käyttää nimikkeiden lisäämisessä ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="e08bc-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="e08bc-130">Kassamoduuli kerää toimitusosoitteen, toimitusvaihtoehdot ja lahjakortin, kanta-asiakasohjelman ja luottokortin tiedot tilauksen käsittelemistä varten.</span><span class="sxs-lookup"><span data-stu-id="e08bc-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="e08bc-131">Kun tilaus on tehty, vahvistustiedot voidaan näyttää tilauksen vahvistuksen moduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="e08bc-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="e08bc-132">**Tilinhallintamoduulit** – Sisäänkirjautumismoduulin avulla asiakkaat voivat kirjautua sisään olemassa olevalle tilille ja rekisteröitymismoduulin avulla he voivat luoda uuden tilin.</span><span class="sxs-lookup"><span data-stu-id="e08bc-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="e08bc-133">Kun tili on luotu, viimeaikaisia tilauksia voi tarkastella tilaushistoriamoduulin avulla. Tilauksen tietoja voi tarkastella tilaustietojen moduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="e08bc-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="e08bc-134">**Suositusten moduuli** – Suositukset näytetään tuotteensijoittelumoduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="e08bc-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="e08bc-135">Tämä moduuli tukee algoritmiluetteloita ja toimituksellisia luetteloita, jotka voidaan esitellä millä tahansa sivulla.</span><span class="sxs-lookup"><span data-stu-id="e08bc-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e08bc-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e08bc-136">Additional resources</span></span>

[<span data-ttu-id="e08bc-137">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e08bc-138">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e08bc-139">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e08bc-140">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e08bc-141">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e08bc-142">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e08bc-143">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e08bc-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]