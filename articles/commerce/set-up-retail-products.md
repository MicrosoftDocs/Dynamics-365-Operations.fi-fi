---
title: Vähittäismyyntituotteiden määrittäminen
description: Tässä artikkelissa käsitellään tuotteiden määrittämistä Dynamics 365 Commerceissa.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b2c5a8976973203a943a2cec7658a2998c54f279
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057229"
---
# <a name="set-up-retail-products"></a><span data-ttu-id="867cd-103">Vähittäismyyntituotteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="867cd-103">Set up retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="867cd-104">Tässä artikkelissa käsitellään tuotteiden määrittämistä Dynamics 365 Commerceissa.</span><span class="sxs-lookup"><span data-stu-id="867cd-104">This article describes how to set up products in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="867cd-105">Sinun on luotava ja määritettävä tuotteet uudelleen myytäviksi Commerce-sovelluksessa, ennen kuin tuotteita voi tarjota myytäväksi.</span><span class="sxs-lookup"><span data-stu-id="867cd-105">Before you can offer products for resale in your commerce channels, you must create and configure the products.</span></span> <span data-ttu-id="867cd-106">Commerce luo organisaationlaajuiset tuotteet päätuotteessa.</span><span class="sxs-lookup"><span data-stu-id="867cd-106">Commerce creates organization-wide products in the product master.</span></span> <span data-ttu-id="867cd-107">Voit luoda tuotteita, määrittää tuotteiden ominaisuuksia ja määritteitä sekä määrittää tuotteet kauppaluokkahierarkioihin.</span><span class="sxs-lookup"><span data-stu-id="867cd-107">You can create the products, define the product properties and attributes, and assign the products to commerce category hierarchies.</span></span> <span data-ttu-id="867cd-108">Jotta tuotteet olisivat käytettävissä kanavissa ja jotta ne voitaisiin lisätä aktiiviseen valikoimaan, tuotteet on vapautettava yrityksiin, jossa ne ovat saatavilla.</span><span class="sxs-lookup"><span data-stu-id="867cd-108">To make the products available to your channels and add them to an active assortment, you must release the products to the legal entities where they are available.</span></span> <span data-ttu-id="867cd-109">Voit määrittää tuotteet, joita myydään kanavissa, toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="867cd-109">To set up the products that you sell by using channels, complete the following tasks.</span></span>

1. <span data-ttu-id="867cd-110">**Määritä tuotehierarkia.**</span><span class="sxs-lookup"><span data-stu-id="867cd-110">**Define a product hierarchy.**</span></span> <span data-ttu-id="867cd-111">Käyttämällä Commercen luokkahierarkiaominaisuuksia voit määrittää luokkahierarkiat, joiden avulla voit ryhmitellä ja luokitella kanaviin jaeltavat tuotteet.</span><span class="sxs-lookup"><span data-stu-id="867cd-111">By using the category hierarchy features in Commerce, you can define category hierarchies to group and categorize the products that you distribute to your channels.</span></span> <span data-ttu-id="867cd-112">Käyttäjän määrittämät ja järjestelmän määritteet voidaan määritellä luokkatasolla.</span><span class="sxs-lookup"><span data-stu-id="867cd-112">User-defined and system attributes can be defined at the category level.</span></span> <span data-ttu-id="867cd-113">Tämän jälkeen kaikki kyseiseen luokkaan määritetyt tuotteet perivät nämä määritteet.</span><span class="sxs-lookup"><span data-stu-id="867cd-113">Then, all products that are assigned to the category inherit those attributes.</span></span> <span data-ttu-id="867cd-114">Luokkahierarkioita voidaan määritellä useita, ja kukin tuote voidaan määrittää useaan hierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="867cd-114">Multiple category hierarchies can be defined, and each product can be assigned to multiple hierarchies.</span></span> <span data-ttu-id="867cd-115">Yhden hierarkian sisällä kukin tuote voidaan kuitenkin määrittää vain yhteen luokkaan.</span><span class="sxs-lookup"><span data-stu-id="867cd-115">However, in a single hierarchy, each product can be assigned to only one category.</span></span>
2. <span data-ttu-id="867cd-116">**Lisää tuotteita ja tuotevariantteja päätuotteeseen.**</span><span class="sxs-lookup"><span data-stu-id="867cd-116">**Add products and product variants to the product master.**</span></span> <span data-ttu-id="867cd-117">Tuotteet, jotka lisätään päätuotteeseen, edustavat yleistä tuoteluetteloa.</span><span class="sxs-lookup"><span data-stu-id="867cd-117">Products that are added to the product master represent a global list of products.</span></span> <span data-ttu-id="867cd-118">Voit lisätä tuotteita manuaalisesti yhden kerrallaan tai tuoda tuotetietoja toimittajilta.</span><span class="sxs-lookup"><span data-stu-id="867cd-118">You can add products manually, one at a time, or you can import product data from your vendors.</span></span>
3. <span data-ttu-id="867cd-119">**Vapauta tuotteet yrityksille.**</span><span class="sxs-lookup"><span data-stu-id="867cd-119">**Release the products to legal entities.**</span></span> <span data-ttu-id="867cd-120">Vain tuotteet, jotka on vapautettu yrityksille, voidaan tuoda kanavien saataville.</span><span class="sxs-lookup"><span data-stu-id="867cd-120">Only products that have been released to legal entities can be made available to your channels.</span></span> <span data-ttu-id="867cd-121">Kun määrität jotakin tuotetta ensimmäisen kerran, voit määrittää sen organisaationlaajuiselle tasolle.</span><span class="sxs-lookup"><span data-stu-id="867cd-121">When you first define a product, you define it on an organization-wide level.</span></span> <span data-ttu-id="867cd-122">Tämän jälkeen voit valita yhden tai useamman yrityksen, jolle tuote vapautetaan.</span><span class="sxs-lookup"><span data-stu-id="867cd-122">You can then select one or more legal entities to release the product to.</span></span> <span data-ttu-id="867cd-123">Tuote on tämän jälkeen usean kanavan käytettävissä organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="867cd-123">The product then becomes available to multiple channels across your organization.</span></span> <span data-ttu-id="867cd-124">Näillä toiminnoilla voit luoda yhden tuotteen kerrallaan, lisätä ja päivittää tuotemääritteitä ja -ominaisuuksia samassa paikassa ja jaella tuotteen organisaatiossa niille kanaville, joissa se on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="867cd-124">You can use this functionality to create a product one time, add and update product attributes and properties in one place, and then distribute the product across your organization, to the channels where it's available.</span></span>
4. <span data-ttu-id="867cd-125">**Lisää tuotteet valikoimiin.**</span><span class="sxs-lookup"><span data-stu-id="867cd-125">**Add products to assortments.**</span></span> <span data-ttu-id="867cd-126">Valikoiman edustaa kanavissa tarjottavien tuotteiden kokoelmaa.</span><span class="sxs-lookup"><span data-stu-id="867cd-126">An assortment represents a collection of products that you offer in your channels.</span></span> <span data-ttu-id="867cd-127">Voit määrittää yhden tai useamman valikoiman ja määrittää kunkin tuotteen yhteen tai useampaan valikoimaan.</span><span class="sxs-lookup"><span data-stu-id="867cd-127">You can define one or more assortments, and each product can be assigned to one or more assortments.</span></span> <span data-ttu-id="867cd-128">Jos haluat määrittää tuotteita kanaville, määritä valikoimat kyseisille kanaville.</span><span class="sxs-lookup"><span data-stu-id="867cd-128">To assign products to channels, you assign the assortments to those channels.</span></span> <span data-ttu-id="867cd-129">Luodessasi valikoimaa voit lisätä tuotteita, joita ei ole vielä vapautettu yritykselle.</span><span class="sxs-lookup"><span data-stu-id="867cd-129">When you create an assortment, you can add products that haven't yet been released to a legal entity.</span></span> <span data-ttu-id="867cd-130">Tuotteet on kuitenkin julkaistava jollekin yritykselle, ennen kuin ne voidaan tuoda kanavien käyttöön.</span><span class="sxs-lookup"><span data-stu-id="867cd-130">However, you must release the products to a legal entity before those products can be made available to the channels.</span></span>
5. <span data-ttu-id="867cd-131">**Lisää tuotteet siirtymishierarkioihin.**</span><span class="sxs-lookup"><span data-stu-id="867cd-131">**Add products to navigation hierarchies.**</span></span> <span data-ttu-id="867cd-132">Ennen kuin tuotteita voidaan selata verkossa tai myyntipisteessä, ne on luokiteltava johonkin Commercen siirtymishierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="867cd-132">Before products can be browsed online or in point of sale (POS), they must be categorized in a Commerce navigation hierarchy.</span></span>
6. <span data-ttu-id="867cd-133">**Lisää tuotteet luetteloon.**</span><span class="sxs-lookup"><span data-stu-id="867cd-133">**Add products to catalogs.**</span></span> <span data-ttu-id="867cd-134">Tämä vaihe on myyntipisteiden osalta valinnainen, mutta verkkokaupat edellyttävät, että tuotteet sisältyvät vähintään yhteen luetteloon.</span><span class="sxs-lookup"><span data-stu-id="867cd-134">Although this step is optional for POS, online stores require that products be included in at least one catalog.</span></span>