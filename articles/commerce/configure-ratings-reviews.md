---
title: Määritä luokitukset ja arvostelut
description: Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002194"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="0ca3d-103">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="0ca3d-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0ca3d-104">Tässä ohjeaiheessa kerrotaan, miten sähköisen kaupankäynnin sivusto määritetään niin, että se näyttää asiakasluokituksia ja -arvostelut Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0ca3d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0ca3d-105">Overview</span></span>

<span data-ttu-id="0ca3d-106">Sähköisen kaupankäynnin sivustojen luokitukset ja arvostelut auttavat asiakkaita saamaan tietoja tuotteista ennen ostopäätöksen tekemistä. NIiden avulla saadaan selville, mitä muut asiakkaat ajattelevat kyseisistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="0ca3d-107">Sähköisen kaupankäynnin sivustoissa luokitukset ja arvostelut ovat myös keino, jolla kerätään asiakaspalautetta tuotteista.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="0ca3d-108">Luokitukset näkyvät tuoteluettelo-, luokkaluettelo- ja hakutulossivuilla sekä muilla sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="0ca3d-109">Luokitusten histogrammit ja tuotearvostelut näytetään tuotetietosivuilla (PDP:t).</span><span class="sxs-lookup"><span data-stu-id="0ca3d-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="0ca3d-110">l**Kirjoita arvostelu** -painikkeen avulla asiakkaat voivat lähettää tuotetta koskevia luokituksia ja arvosteluja.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="0ca3d-111">Luokitusten ja arvosteluiden moduulit PDP-sivuilla</span><span class="sxs-lookup"><span data-stu-id="0ca3d-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="0ca3d-112">Kolme moduulia näyttävät luokitukset ja arvostelut PDP-sivujen yhteenvedoissa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0ca3d-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="0ca3d-113">Kirjoita arvostelu -moduuli</span><span class="sxs-lookup"><span data-stu-id="0ca3d-113">Write review module</span></span>
- <span data-ttu-id="0ca3d-114">Tuotearvosteluluettelomoduuli</span><span class="sxs-lookup"><span data-stu-id="0ca3d-114">Product reviews list module</span></span>
- <span data-ttu-id="0ca3d-115">Luokitusten histogrammin moduuli</span><span class="sxs-lookup"><span data-stu-id="0ca3d-115">Ratings histogram module</span></span>
 
<span data-ttu-id="0ca3d-116">Seuraavassa kuvassa näytetään, miltä luokitusten ja arvosteluiden moduulit näyttävät PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Luokitusten ja arvosteluiden moduulit PDP-sivulla](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="0ca3d-118">Lisätietoja PDP-mallien ja -asettelujen optimoimisesta niin, että voit jakaa luokitusten ja arvosteluiden moduulien määritykset useiden PDP-sivujen kanssa sähköisen kaupankäynnin sivustossa, on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0ca3d-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="0ca3d-119">Seuraavassa kuvassa on tietoja siitä, miten **Lisää moduuli** -valintaikkuna esittää luokitusten ja arvosteluiden moduulit Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Lisää moduuli -valintaikkuna](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="0ca3d-121">Kirjoita arvostelu -moduuli</span><span class="sxs-lookup"><span data-stu-id="0ca3d-121">Write review module</span></span>

<span data-ttu-id="0ca3d-122">Kirjoita arvostelu -moduuli sisältää **Kirjoita arvostelu** -painikkeen, jonka avulla käyttäjät voivat kirjautua sisään, määrittää luokituksen ja kirjoittaa tuotetta koskevan arvostelun.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="0ca3d-123">Tämän moduulin avulla käyttäjät voivat myös muokata aiemmin lähettämiään luokituksia ja arvosteluita.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="0ca3d-124">Tämä moduuli näkyy yleensä luokitusten histogrammi -ja tuotearvosteluluettelomoduulien yläpuolella PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="0ca3d-125">Seuraavassa kuvassa on **Kirjoita arvostelu** -valintaikkuna, joka näkyy, kun asiakas valitsee **Kirjoita arvostelu** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="0ca3d-126">Asiakas voi tämän valintaikkunan avulla lähettää luokituksen ja arvostelun.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Kirjoita arvostelu -valintaikkuna](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="0ca3d-128">Seuraavassa taulukossa on Kirjoita arvostelu -moduulin ominaisuus, joka on määritettävä muokkaustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0ca3d-129">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="0ca3d-129">Property name</span></span> | <span data-ttu-id="0ca3d-130">Arvo</span><span class="sxs-lookup"><span data-stu-id="0ca3d-130">Value</span></span>        | <span data-ttu-id="0ca3d-131">Ominaisuuden kuvaus</span><span class="sxs-lookup"><span data-stu-id="0ca3d-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="0ca3d-132">Nimi</span><span class="sxs-lookup"><span data-stu-id="0ca3d-132">Name</span></span>          | <span data-ttu-id="0ca3d-133">Kirjoita arvostelu</span><span class="sxs-lookup"><span data-stu-id="0ca3d-133">Write review</span></span> | <span data-ttu-id="0ca3d-134">Kirjoita arvostelu -moduulin nimi.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="0ca3d-135">Luokitusten histogrammin moduuli</span><span class="sxs-lookup"><span data-stu-id="0ca3d-135">Ratings histogram module</span></span>

<span data-ttu-id="0ca3d-136">Luokitusten histogrammin moduulissa on luokitusten histogrammi.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="0ca3d-137">Tämä moduuli tulee yleensä näkyviin Kirjoita arvostelu -moduulin ja tuotearvosteluluettelomoduulin väliin PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="0ca3d-138">Luokitusten histogrammin moduulia ei tarvitse määrittää.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="0ca3d-139">Moduuli on ainoastaan lisättävä PDP-malliin.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="0ca3d-140">Seuraavissa kuvissa näkyy, miltä PDP-malli näyttää Dynamics 365 Commerce -sovelluksessa, kun luokitusten ja arvostelujen moduulit on määritetty näytettäväksi PDP-sivuilla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP-malli, kun luokitukset ja arvostelut on määritetty näytettäväksi PDP-sivuilla](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="0ca3d-142">Tuotearvosteluluettelomoduuli</span><span class="sxs-lookup"><span data-stu-id="0ca3d-142">Product reviews list module</span></span>

<span data-ttu-id="0ca3d-143">Tuotearvosteluluettelomoduulissa on tuotearvosteluluettelo sekä lajittelu-, suodatus- ja sivutusvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="0ca3d-144">Tämä moduuli tulee yleensä näkyviin luokitusten histogrammin moduulin jälkeen PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="0ca3d-145">Seuraavassa taulukossa on tuotearvosteluluettelomoduulin ominaisuudet, jotka on määritettävä muokkaustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0ca3d-146">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="0ca3d-146">Property name</span></span>              | <span data-ttu-id="0ca3d-147">Arvo</span><span class="sxs-lookup"><span data-stu-id="0ca3d-147">Value</span></span> | <span data-ttu-id="0ca3d-148">Ominaisuuden kuvaus</span><span class="sxs-lookup"><span data-stu-id="0ca3d-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="0ca3d-149">Kullakin sivulla näytettävät arvostelut</span><span class="sxs-lookup"><span data-stu-id="0ca3d-149">Reviews shown on each page</span></span> | <span data-ttu-id="0ca3d-150">10</span><span class="sxs-lookup"><span data-stu-id="0ca3d-150">10</span></span>    | <span data-ttu-id="0ca3d-151">Niiden arvosteluiden määrä, jotka tulee näyttää kerralla PDP-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="0ca3d-152">**Seuraava**- ja **Edellinen**-painikkeet ovat mukana, jotta käyttäjät voivat liikkua arvostelusivuilla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="0ca3d-153">Luokitusten histogrammi – Yhteenvetonäkymä</span><span class="sxs-lookup"><span data-stu-id="0ca3d-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="0ca3d-154">Tuotearvosteluluettelomoduuli sisältää paikan, jossa voit lisätä luokitusten histogrammin moduulin.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="0ca3d-155">Seuraavassa kuvassa näkyy, miten voit lisätä luokitusten histogrammin moduulin tuotearvosteluluettelomoduuliin Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Luokitusten histogrammin moduulin lisääminen tuotearvosteluluettelomoduuliin](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="0ca3d-157">Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="0ca3d-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="0ca3d-158">Luokitusten ja arvostelujen määrityksen arvot, kuten vuokraajan tunnus, arvostelun tekstin pituus ja luokituksen otsikon pituus, määritetään sivustotasolla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="0ca3d-159">Voit määrittää sivuston näyttämään luokitukset ja arvostelut seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="0ca3d-160">Siirry kohtaan **Aloitus \> Sivustot**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0ca3d-161">Valitse sivuston nimi.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="0ca3d-162">Siirry kohtaan **Sivuston hallinta \> Laajennettavuus**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="0ca3d-163">Syötä **Arvostelun tekstin enimmäispituus** -kenttään arvostelun tekstin merkkien enimmäismäärä (esimerkiksi **1 000**).</span><span class="sxs-lookup"><span data-stu-id="0ca3d-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="0ca3d-164">Syötä **Arvostelun otsikon enimmäispituus** -kenttään arvostelun otsikoiden merkkien enimmäismäärä (esimerkiksi **55**).</span><span class="sxs-lookup"><span data-stu-id="0ca3d-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="0ca3d-165">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0ca3d-166">Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Sivuston määrittäminen niin, että se näyttää luokitukset ja arvostelut](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="0ca3d-168">Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan</span><span class="sxs-lookup"><span data-stu-id="0ca3d-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="0ca3d-169">Tuoteluokitus näkyy PDP:n yläosassa olevan tuotteen otsikon alla.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="0ca3d-170">Tuoteluokitus voidaan määrittää niin, että se on linkitetty saman PDP:n **Arvostelut**-osaan.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="0ca3d-171">Voit linkittää tuoteluokituksen PDP:n osan **Arvostelut**-osaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="0ca3d-172">Avaa PDP-malli.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="0ca3d-173">Siirry kohtaan **Ostoruudun säilömoduulin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="0ca3d-174">Valitse **Ostoruutu**-kohdassa **Tuoteluokitukset** ja valitse sitten **Linkitä napsautus täydellisten arviointien moduuliin** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="0ca3d-175">Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Tuoteluokituksen linkittäminen PDP:n Arvostelut-osaan](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="0ca3d-177">Tietosuoja- ja käytäntösivun linkin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0ca3d-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="0ca3d-178">Voit määrittää tietosuoja- ja käytäntösivun linkin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="0ca3d-179">Siirry kohtaan **Aloitus \> Sivustot**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="0ca3d-180">Valitse sivuston nimi.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="0ca3d-181">Siirry kohtaan **Sivuston hallinta \> Laajennettavuus**</span><span class="sxs-lookup"><span data-stu-id="0ca3d-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="0ca3d-182">Valitse **Reitit**-välilehdessä **RNR - tietosuoja ja käytäntö** -kohdassa **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="0ca3d-183">Jos linkki on jo syötetty ja haluat korvata sen, valitse linkki.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="0ca3d-184">Valitse **Lisää linkki** -valintaikkunassa tietosuoja-ja käytäntösivun linkki ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="0ca3d-185">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="0ca3d-186">Seuraava kuva osoittaa, miltä tämä määritys näyttää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Tietosuoja- ja käytäntösivun linkin määrittäminen](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="0ca3d-188">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0ca3d-188">Additional resources</span></span>

[<span data-ttu-id="0ca3d-189">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0ca3d-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0ca3d-190">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="0ca3d-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="0ca3d-191">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="0ca3d-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="0ca3d-192">Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa</span><span class="sxs-lookup"><span data-stu-id="0ca3d-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
