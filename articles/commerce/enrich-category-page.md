---
title: Luokan saapumissivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799008"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="81029-103">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="81029-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81029-104">Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="81029-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="81029-105">Commerce tarjoaa oletusluokan saapumissivun, jota käytetään, kun luokkatiedot näytetään.</span><span class="sxs-lookup"><span data-stu-id="81029-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="81029-106">Oletusluokkasivulla on pakollisia elementtejä, kuten tarkentimia, luokiteltua tuotesijoittelua, lajitteluvaihtoehtoja, valinnan yhteenveto ja sivutuksen ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="81029-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="81029-107">Oletusluokkasivun sijaan voidaan käyttää luokan täydennettyä saapumissivua. Siinä on enemmän sisältöä ja erityisiä elementtejä.</span><span class="sxs-lookup"><span data-stu-id="81029-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="81029-108">Tyypilliseen täydennykseen voi kuulua luokkakohtaisen markkinointisisällön lisääminen luokkasivulle.</span><span class="sxs-lookup"><span data-stu-id="81029-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="81029-109">Tämä sisältö voi sisältää eri luokkien tuotesijoittelua ristiinmyyntitarkoituksia, toimituksellisia luetteloita, kuvia, videoita ja muuta tekstiä varten.</span><span class="sxs-lookup"><span data-stu-id="81029-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="81029-110">Voit muokata oletusluokkasivua tai määrittää tietylle luokalle toisen luokkasivun.</span><span class="sxs-lookup"><span data-stu-id="81029-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

<span data-ttu-id="81029-112">Kaupan luontityökalun **Tuoteet**-sivulla on luokkaluettelo kanavista, jotka on määritetty sivustoon.</span><span class="sxs-lookup"><span data-stu-id="81029-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="81029-113">Jos luokkasivulle on valittu **Täydennetty**-tila, luokkasivua on täydennetty.</span><span class="sxs-lookup"><span data-stu-id="81029-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="81029-114">Muussa tapauksessa luokassa käytetään oletusluokkasivua ja -sisältöä.</span><span class="sxs-lookup"><span data-stu-id="81029-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="81029-115">Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä luokkasivuja luokassa valitsemalla luokan nimen.</span><span class="sxs-lookup"><span data-stu-id="81029-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="81029-116">Voit täydentää luokkasivua seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="81029-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="81029-117">Valitse **Tuotteet**-sivulla sen luokan nimi, jota haluat täydentää luokkasivulla.</span><span class="sxs-lookup"><span data-stu-id="81029-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="81029-118">Valitun luokan oletusluokkasivu avautuu sivueditoriin.</span><span class="sxs-lookup"><span data-stu-id="81029-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="81029-119">Valitse **Täydennä luokkasivua**.</span><span class="sxs-lookup"><span data-stu-id="81029-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="81029-120">Valitse täydennetyn luokkasivun malli.</span><span class="sxs-lookup"><span data-stu-id="81029-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="81029-121">Jos teet vain vähäisiä muutoksia, voit valita oletusluokkasivun.</span><span class="sxs-lookup"><span data-stu-id="81029-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="81029-122">Vaihtoehtoisesti voit valita tietyn luokkasivunmallin.</span><span class="sxs-lookup"><span data-stu-id="81029-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="81029-123">Kun valitset mallin, sivueditori avataan ja valitun mallin avulla luodaan uusi luokkasivu valitulle luokalle.</span><span class="sxs-lookup"><span data-stu-id="81029-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="81029-124">Sivu kuitataan ulos sinulle. Nyt voit tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="81029-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="81029-125">Moduulit, joissa käytetään luokan määritystietoja, käyttävät valitun luokan tietoja.</span><span class="sxs-lookup"><span data-stu-id="81029-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="81029-126">Valitsemasi mallin asetukset määrittävät muutokset, jotka voit tehdä.</span><span class="sxs-lookup"><span data-stu-id="81029-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81029-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="81029-127">Additional resources</span></span>

[<span data-ttu-id="81029-128">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="81029-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="81029-129">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="81029-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="81029-130">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="81029-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="81029-131">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="81029-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="81029-132">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="81029-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="81029-133">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="81029-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="81029-134">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="81029-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="81029-135">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="81029-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
