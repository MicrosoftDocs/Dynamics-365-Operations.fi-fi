---
title: Puhelukeskuksen toiminnot
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Retailin puhelinkeskuksen myyntitoimintojen yleiskatsaus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00d24e9933d087f150ec5270da94ad911423824d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="0570b-103">Puhelukeskuksen toiminnot</span><span class="sxs-lookup"><span data-stu-id="0570b-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="0570b-104">Tässä artikkelissa on Microsoft Dynamics 365 for Retailin puhelinkeskuksen myyntitoimintojen yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="0570b-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="0570b-105">Dynamics 365 for Retail tukee myös puhelinkeskuksia vähittäismyyntikanavana.</span><span class="sxs-lookup"><span data-stu-id="0570b-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="0570b-106">Työntekijät ottavat puhelinkeskuksessa vastaan asiakkaiden tilauksia puhelimitse ja luovat myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="0570b-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="0570b-107">Puhelinkeskuksen toimintoihin sisältyy toimintoja, joiden tarkoituksena on helpottaa puhelimessa tilaamista ja asiakaspalvelua tilausprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="0570b-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="0570b-108">Esimerkiksi puhelukeskuksen työntekijät voivat syöttää maksutiedot suoraan myyntitilauksesta ja tarkastella yksityiskohtaista yhteenvetoa kuluista ja maksuista ennen tilauksen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="0570b-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="0570b-109">Työntekijöillä on myös mahdollisuus hallita hinnoittelua ja käyttää eri tietoja asiakkaista, tuotteista ja hinnoista **Myyntitilaus**-sivun kautta.</span><span class="sxs-lookup"><span data-stu-id="0570b-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="0570b-110">Puhelukeskukset voivat myös laajennetusti seurata asiakkaan historiatietoja ja tilauksen tilaa.</span><span class="sxs-lookup"><span data-stu-id="0570b-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="0570b-111">Jokaisella puhelinkeskuksella voi olla omat käyttäjät, maksutavat, hintaryhmät, taloushallinnon dimensiot ja toimitustavat.</span><span class="sxs-lookup"><span data-stu-id="0570b-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="0570b-112">Voit määrittää nämä asetukset puhelinkeskusta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="0570b-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="0570b-113">Voit lisäksi ottaa käyttöön tai poistaa käytöstä seuraavat, vain puhelinpalvelukeskuksille ominaiset toimintoryhmät **Puhelukeskus**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="0570b-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="0570b-114">**Tilauksen viimeistely** – Tämä ryhmä sisältää ominaisuuksia, jotka liittyvät maksuihin ja tilausten viimeistelyyn **Myyntitilaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0570b-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="0570b-115">**Ohjattu myynti** – Tämä ryhmä sisältää ominaisuuksia, jotka liittyvät lähdekoodeihin, komentosarjoihin ja luettelopyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="0570b-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="0570b-116">Kun olet ottanut nämä toiminnot käyttöön puhelukeskuksen asetuksissa, ne ovat **Myyntitilaus**-sivulla puhelukeskukseen liittyvien käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="0570b-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="0570b-117">Useimmat näistä ominaisuuksista vaativat lisäasetuksia ennen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="0570b-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="0570b-118">Ennen kuin käyttäjät voivat luoda puhelukeskustilauksia, sinun on lisättävä nämä käyttäjät puhelukeskuksen käyttäjiksi.</span><span class="sxs-lookup"><span data-stu-id="0570b-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="0570b-119">Tällä toimella otetaan käyttöön puhelukeskuskanavakohtainen konfiguraatio ja toiminnot.</span><span class="sxs-lookup"><span data-stu-id="0570b-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="0570b-120">Alla on joitain esimerkkejä saataville tulevista toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="0570b-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="0570b-121">Ohjattu myynti tarjoaa konfiguraatiovaihtoehtoja puhelinmyynnin käsikirjoituksista ja tuotekuvista, jotka auttavat ja ohjaavat myyntiassistentteja, kun he ottavat vastaan tilauksia.</span><span class="sxs-lookup"><span data-stu-id="0570b-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="0570b-122">Tilauksia ei voida viimeistellä ennen kuin myyntiassistentit ovat ottaneet vastaan ainakin yhden maksutavan.</span><span class="sxs-lookup"><span data-stu-id="0570b-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="0570b-123">Lisämyyntiä ja liittyvien tuotteiden myyntiä koskevia sääntöjä voidaan konfiguroida kehottamaan myyntiassistentteja edistämään määrättyjä tuotteita asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="0570b-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="0570b-124">Myyntiassistentit voivat kirjata sen luettelon lähdekoodin, josta asiakas on tekemässä tilausta.</span><span class="sxs-lookup"><span data-stu-id="0570b-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="0570b-125">Myyntiassistentit voivat lisätä jälleenmyyjän kuponkeja tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="0570b-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="0570b-126">Myyntiassistentit voivat myydä jatkuvuusohjelmia.</span><span class="sxs-lookup"><span data-stu-id="0570b-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="0570b-127">Tilauksia voidaan asettaa pitoon manuaalisesti tai automaattisesti osoittamaan, että tarvitaan lisätutkimuksia ennen kuin tilaus voidaan käsitellä.</span><span class="sxs-lookup"><span data-stu-id="0570b-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





