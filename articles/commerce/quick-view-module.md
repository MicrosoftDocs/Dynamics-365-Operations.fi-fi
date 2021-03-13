---
title: Pikanäkymämoduuli
description: Tässä ohjeaiheessa on tietoja pikanäkymämoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097049"
---
# <a name="quick-view-module"></a><span data-ttu-id="50da4-103">Pikanäkymämoduuli</span><span class="sxs-lookup"><span data-stu-id="50da4-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="50da4-104">Tässä ohjeaiheessa on tietoja pikanäkymämoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="50da4-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="50da4-105">Pikanäkymämoduulin avulla käyttäjät voivat tarkastella nopeasti tuotetietoja, kun he selaavat tuotteita luettelosivulla, ja lisätä tuotteen tai tuotteita luettelosivulta ostoskoriin, tarvitsematta siirtyä tuotetietosivulle (PDP).</span><span class="sxs-lookup"><span data-stu-id="50da4-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="50da4-106">Pikanäkymämoduuli sisältää yhteenvedon tuotetietoista, joita käyttäjät tarvitsevat Lisää ostoskoriin -päätöksen tekemistä varten.</span><span class="sxs-lookup"><span data-stu-id="50da4-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="50da4-107">Lisäksi siinä on linkki tuotetietosivulle, jotta käyttäjät voivat tarkastella lisätuotetietoja ja ostovaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="50da4-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="50da4-108">[Tuotekokoelma](product-collection-module-overview.md)- ja [Hakutulokset](search-result-module.md)-moduulit tukevat pikanäkymämoduulia.</span><span class="sxs-lookup"><span data-stu-id="50da4-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50da4-109">Pikanäkymämoduuli on käytettävissä Commerce 10.0.17 -versiosta eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="50da4-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="50da4-110">Seuraavassa kuvassa on esimerkki pikanäkymämoduulista tuoteluettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="50da4-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Esimerkki pikanäkymämoduulista tuoteluettelosivulla](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="50da4-112">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="50da4-112">Module properties</span></span>

<span data-ttu-id="50da4-113">Pikanäkymämoduuli tukee joitakin samoja toimintoja kuin ostoruutumoduuli.</span><span class="sxs-lookup"><span data-stu-id="50da4-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="50da4-114">Siksi pikanäkymämoduulin ominaisuudet muistuttavat ostoruutumoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="50da4-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="50da4-115">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="50da4-115">Property</span></span> | <span data-ttu-id="50da4-116">Arvot</span><span class="sxs-lookup"><span data-stu-id="50da4-116">Values</span></span> | <span data-ttu-id="50da4-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="50da4-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="50da4-118">Otsikon tunniste</span><span class="sxs-lookup"><span data-stu-id="50da4-118">Heading tag</span></span> | <span data-ttu-id="50da4-119">**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**</span><span class="sxs-lookup"><span data-stu-id="50da4-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="50da4-120">Tämä ominaisuus määrittää tuoteotsikon otsikon tunnisteen.</span><span class="sxs-lookup"><span data-stu-id="50da4-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="50da4-121">Jos pikanäkymämoduuli on sivun yläosassa, helppokäyttöisyysstandardit täyttyvät, kun tämän ominaisuuden arvona on **H1**.</span><span class="sxs-lookup"><span data-stu-id="50da4-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="50da4-122">Salli mukautettu hinta</span><span class="sxs-lookup"><span data-stu-id="50da4-122">Allow custom price</span></span> | <span data-ttu-id="50da4-123">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="50da4-123">**True** or **False**</span></span> | <span data-ttu-id="50da4-124">Jos ominaisuuden arvoksi määritetään **Tosi**, käyttäjä voi määrittää mukautetun hinnan.</span><span class="sxs-lookup"><span data-stu-id="50da4-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="50da4-125">Vähimmäishinta</span><span class="sxs-lookup"><span data-stu-id="50da4-125">Minimum price</span></span> | <span data-ttu-id="50da4-126">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="50da4-126">Integer</span></span> | <span data-ttu-id="50da4-127">Tämä ominaisuus on käytettävissä vain, jos **Salli mukautettu hinta** -ominaisuuden arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="50da4-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="50da4-128">Se määrittää vähimmäishinnan, jonka käyttäjä voi syöttää (esimerkiksi 1 $).</span><span class="sxs-lookup"><span data-stu-id="50da4-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="50da4-129">Enimmäishinta</span><span class="sxs-lookup"><span data-stu-id="50da4-129">Maximum price</span></span> | <span data-ttu-id="50da4-130">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="50da4-130">Integer</span></span> | <span data-ttu-id="50da4-131">Tämä ominaisuus on käytettävissä vain, jos **Salli mukautettu hinta** -ominaisuuden arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="50da4-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="50da4-132">Se määrittää enimmäishinnan, jonka käyttäjä voi syöttää (esimerkiksi 1 000 $).</span><span class="sxs-lookup"><span data-stu-id="50da4-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="50da4-133">Commercen sivustonmuodostimen asetukset</span><span class="sxs-lookup"><span data-stu-id="50da4-133">Commerce site builder settings</span></span>

<span data-ttu-id="50da4-134">Kuten ostoruutumoduuli, pikanäkymämoduuli noudattaa asetuksia kohdassa **Sivuston asetukset \> Laajennukset \> Lisää tuote ostoskoriin**.</span><span class="sxs-lookup"><span data-stu-id="50da4-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="50da4-135">**Siirry ostoskorisivulle** -asetus kuitenkin ohitetaan, koska se on ristiriidassa pikanäkymämoduulin tarkoituksen kanssa. Näin käyttäjät voivat selata useita tuotteita luettelosivulla ja lisätä niitä kärryynsä siirtymättä pois luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="50da4-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="50da4-136">Pikanäkymämoduulin lisääminen kokoelmamoduuliin</span><span class="sxs-lookup"><span data-stu-id="50da4-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="50da4-137">Pikanäkymämoduuli voidaan lisätä Tuotekokoelma- ja Hakutulokset-moduuleihin.</span><span class="sxs-lookup"><span data-stu-id="50da4-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="50da4-138">Voit lisätä pikanäkymämoduulin tuotekokoelmamoduuliin Commercen sivustonmuodostimessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="50da4-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="50da4-139">Siirry kohtaan **Sivut** ja valitse Fabrikam-sivuston aloitussivu.</span><span class="sxs-lookup"><span data-stu-id="50da4-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="50da4-140">Siirry mihin tahansa kotisivun **Tuotekokoelma**-moduuliin, valitse kolmepistettä (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="50da4-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="50da4-141">Valitse **Lisää moduuli** -valintaikkunassa **Pikanäkymä**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="50da4-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="50da4-142">Valitse **Pikanäkymä**-moduulin ominaisuusruudusta **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="50da4-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="50da4-143">Määritä **Otsikko**-valintaikkunassa **Otsikkotaso**-kentän arvoksi **H2** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="50da4-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="50da4-144">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="50da4-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50da4-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="50da4-145">Additional resources</span></span>

[<span data-ttu-id="50da4-146">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="50da4-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="50da4-147">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="50da4-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="50da4-148">Tuotekokoelmamoduuli</span><span class="sxs-lookup"><span data-stu-id="50da4-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="50da4-149">Hakutulosmoduuli</span><span class="sxs-lookup"><span data-stu-id="50da4-149">Search results module</span></span>](search-result-module.md)
