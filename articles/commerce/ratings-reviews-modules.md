---
title: Luokitusten ja arvosteluiden moduulit
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Commercen tuotetietojen sivuilla käytettäviä luokitus- ja arviointimoduuleja.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: ee2a2a781537b592fb5f80ce424a7331c4e21d41
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071857"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="e5e23-103">Luokitusten ja arvosteluiden moduulit</span><span class="sxs-lookup"><span data-stu-id="e5e23-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5e23-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Commercen tuotetietojen sivuilla (PDP) käytettäviä luokitus- ja arviointimoduuleja.</span><span class="sxs-lookup"><span data-stu-id="e5e23-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e5e23-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e5e23-105">Overview</span></span>

<span data-ttu-id="e5e23-106">Sähköisen kaupankäynnin sivustojen luokitukset ja arvostelut auttavat asiakkaita saamaan tietoja tuotteista ennen ostopäätöksen tekemistä. Niiden avulla voi myös kerätä asiakkaiden tuotteita koskevaa palautetta.</span><span class="sxs-lookup"><span data-stu-id="e5e23-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="e5e23-107">Luokitukset näkyvät tuoteluettelo-, luokkaluettelo- ja hakutulossivuilla sekä muilla sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="e5e23-108">Luokitusten histogrammit ja tuotearvostelut näytetään PDP-sivuilla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="e5e23-109">l**Kirjoita arvostelu** -painikkeen avulla asiakkaat voivat lähettää tuotetta koskevia luokituksia ja arvosteluja.</span><span class="sxs-lookup"><span data-stu-id="e5e23-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="e5e23-110">Näitä PDP-toimintoja hallitsevat luokitus- ja tarkistusmoduulit.</span><span class="sxs-lookup"><span data-stu-id="e5e23-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="e5e23-111">Luokitusten ja arvosteluiden moduulit PDP-sivuilla</span><span class="sxs-lookup"><span data-stu-id="e5e23-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="e5e23-112">Kolme moduulia näyttävät luokitukset ja arvostelut PDP-sivujen yhteenvedoissa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e5e23-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="e5e23-113">Kirjoita arvostelu -moduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-113">Write review module</span></span>
- <span data-ttu-id="e5e23-114">Tuotearvosteluluettelomoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-114">Product reviews list module</span></span>
- <span data-ttu-id="e5e23-115">Luokitusten histogrammin moduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-115">Ratings histogram module</span></span>
 
<span data-ttu-id="e5e23-116">Seuraavassa kuvassa näytetään, miltä luokitusten ja arvosteluiden moduulit näyttävät PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Luokitusten ja arvosteluiden moduulit PDP-sivulla](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="e5e23-118">Lisätietoja PDP-mallien ja -asettelujen optimoimisesta niin, että voit jakaa luokitusten ja arvosteluiden moduulien määritykset useiden PDP-sivujen kanssa sähköisen kaupankäynnin sivustossa, on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e5e23-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="e5e23-119">Seuraavassa kuvassa on tietoja siitä, miten **Lisää moduuli** -valintaikkuna esittää luokitusten ja arvosteluiden moduulit Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e5e23-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="e5e23-120">![Lisää moduuli -valintaikkuna](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="e5e23-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="e5e23-121">Kirjoita arvostelu -moduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-121">Write review module</span></span>

<span data-ttu-id="e5e23-122">Kirjoita arvostelu -moduuli sisältää **Kirjoita arvostelu** -painikkeen, jonka avulla käyttäjät voivat kirjautua sisään, määrittää luokituksen ja kirjoittaa tuotetta koskevan arvostelun.</span><span class="sxs-lookup"><span data-stu-id="e5e23-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="e5e23-123">Tämän moduulin avulla käyttäjät voivat myös muokata aiemmin lähettämiään luokituksia ja arvosteluita.</span><span class="sxs-lookup"><span data-stu-id="e5e23-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="e5e23-124">Tämä moduuli näkyy yleensä luokitusten histogrammi -ja tuotearvosteluluettelomoduulien yläpuolella PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="e5e23-125">Seuraavassa kuvassa on **Kirjoita arvostelu** -valintaikkuna, joka näkyy, kun asiakas valitsee **Kirjoita arvostelu** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="e5e23-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="e5e23-126">Asiakas voi tämän valintaikkunan avulla lähettää luokituksen ja arvostelun.</span><span class="sxs-lookup"><span data-stu-id="e5e23-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="e5e23-127">![Kirjoita arvostelu -valintaikkuna](media/rnr-eCommerce-write-review-module.png) Seuraavassa taulussa ovat kirjoita arvostelu -ominaisuus, joka on määritettävä luontityökalussa.</span><span class="sxs-lookup"><span data-stu-id="e5e23-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="e5e23-128">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="e5e23-128">Property name</span></span> | <span data-ttu-id="e5e23-129">Arvo</span><span class="sxs-lookup"><span data-stu-id="e5e23-129">Value</span></span>        | <span data-ttu-id="e5e23-130">Ominaisuuden kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5e23-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="e5e23-131">Nimi</span><span class="sxs-lookup"><span data-stu-id="e5e23-131">Name</span></span>          | <span data-ttu-id="e5e23-132">Kirjoita arvostelu</span><span class="sxs-lookup"><span data-stu-id="e5e23-132">Write review</span></span> | <span data-ttu-id="e5e23-133">Kirjoita arvostelu -moduulin nimi.</span><span class="sxs-lookup"><span data-stu-id="e5e23-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="e5e23-134">Luokitusten histogrammin moduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-134">Ratings histogram module</span></span>

<span data-ttu-id="e5e23-135">Luokitusten histogrammin moduulissa on luokitusten histogrammi.</span><span class="sxs-lookup"><span data-stu-id="e5e23-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="e5e23-136">Tämä moduuli tulee yleensä näkyviin Kirjoita arvostelu -moduulin ja tuotearvosteluluettelomoduulin väliin PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="e5e23-137">Luokitusten histogrammin moduulia ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="e5e23-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="e5e23-138">Moduuli on ainoastaan lisättävä PDP-malliin.</span><span class="sxs-lookup"><span data-stu-id="e5e23-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="e5e23-139">Seuraavissa kuvissa näkyy, miltä PDP-malli näyttää Dynamics 365 Commerce -sovelluksessa, kun luokitusten ja arvostelujen moduulit on määritetty näytettäväksi PDP-sivuilla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="e5e23-140">![PDP-malli, kun luokitukset ja arvostelut on määritetty näytettäväksi PDP-sivuilla](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="e5e23-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="e5e23-141">Tuotearvosteluluettelomoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-141">Product reviews list module</span></span>

<span data-ttu-id="e5e23-142">Tuotearvosteluluettelomoduulissa on tuotearvosteluluettelo sekä lajittelu-, suodatus- ja sivutusvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="e5e23-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="e5e23-143">Tämä moduuli tulee yleensä näkyviin luokitusten histogrammin moduulin jälkeen PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="e5e23-144">Seuraavassa taulukossa on tuotearvosteluluettelomoduulin ominaisuudet, jotka on määritettävä muokkaustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="e5e23-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="e5e23-145">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="e5e23-145">Property name</span></span>              | <span data-ttu-id="e5e23-146">Arvo</span><span class="sxs-lookup"><span data-stu-id="e5e23-146">Value</span></span> | <span data-ttu-id="e5e23-147">Ominaisuuden kuvaus</span><span class="sxs-lookup"><span data-stu-id="e5e23-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="e5e23-148">Kullakin sivulla näytettävät arvostelut</span><span class="sxs-lookup"><span data-stu-id="e5e23-148">Reviews shown on each page</span></span> | <span data-ttu-id="e5e23-149">10</span><span class="sxs-lookup"><span data-stu-id="e5e23-149">10</span></span>    | <span data-ttu-id="e5e23-150">Niiden arvosteluiden määrä, jotka tulee näyttää kerralla PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="e5e23-151">**Seuraava**- ja **Edellinen**-painikkeet ovat mukana, jotta käyttäjät voivat liikkua arvostelusivuilla.</span><span class="sxs-lookup"><span data-stu-id="e5e23-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="e5e23-152">Luokitusten histogrammi – Yhteenvetonäkymä</span><span class="sxs-lookup"><span data-stu-id="e5e23-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="e5e23-153">Tuotearvosteluluettelomoduuli sisältää paikan, jossa voit lisätä luokitusten histogrammin moduulin.</span><span class="sxs-lookup"><span data-stu-id="e5e23-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="e5e23-154">Seuraavassa kuvassa näkyy, miten voit lisätä luokitusten histogrammin moduulin tuotearvosteluluettelomoduuliin Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e5e23-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Luokitusten histogrammin moduulin lisääminen tuotearvosteluluettelomoduuliin](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="e5e23-156">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e5e23-156">Additional resources</span></span>

[<span data-ttu-id="e5e23-157">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e5e23-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e5e23-158">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e5e23-159">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e5e23-160">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e5e23-161">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e5e23-162">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e5e23-163">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="e5e23-163">Footer module</span></span>](author-footer-module.md)
