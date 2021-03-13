---
title: Luokan saapumissivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 96fbd7c2ddfcd43e38e9572a60873d5f5930c94c
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097226"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="369b9-103">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="369b9-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="369b9-104">Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="369b9-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="369b9-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="369b9-105">Overview</span></span>

<span data-ttu-id="369b9-106">Commerce tarjoaa oletusluokan saapumissivun, jota käytetään, kun luokkatiedot näytetään.</span><span class="sxs-lookup"><span data-stu-id="369b9-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="369b9-107">Oletusluokkasivulla on pakollisia elementtejä, kuten tarkentimia, luokiteltua tuotesijoittelua, lajitteluvaihtoehtoja, valinnan yhteenveto ja sivutuksen ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="369b9-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="369b9-108">Oletusluokkasivun sijaan voidaan käyttää luokan täydennettyä saapumissivua. Siinä on enemmän sisältöä ja erityisiä elementtejä.</span><span class="sxs-lookup"><span data-stu-id="369b9-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="369b9-109">Tyypilliseen täydennykseen voi kuulua luokkakohtaisen markkinointisisällön lisääminen luokkasivulle.</span><span class="sxs-lookup"><span data-stu-id="369b9-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="369b9-110">Tämä sisältö voi sisältää eri luokkien tuotesijoittelua ristiinmyyntitarkoituksia, toimituksellisia luetteloita, kuvia, videoita ja muuta tekstiä varten.</span><span class="sxs-lookup"><span data-stu-id="369b9-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="369b9-111">Voit muokata oletusluokkasivua tai määrittää tietylle luokalle toisen luokkasivun.</span><span class="sxs-lookup"><span data-stu-id="369b9-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

<span data-ttu-id="369b9-113">Kaupan luontityökalun **Tuoteet**-sivulla on luokkaluettelo kanavista, jotka on määritetty sivustoon.</span><span class="sxs-lookup"><span data-stu-id="369b9-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="369b9-114">Jos luokkasivulle on valittu **Täydennetty**-tila, luokkasivua on täydennetty.</span><span class="sxs-lookup"><span data-stu-id="369b9-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="369b9-115">Muussa tapauksessa luokassa käytetään oletusluokkasivua ja -sisältöä.</span><span class="sxs-lookup"><span data-stu-id="369b9-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="369b9-116">Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä luokkasivuja luokassa valitsemalla luokan nimen.</span><span class="sxs-lookup"><span data-stu-id="369b9-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="369b9-117">Voit täydentää luokkasivua seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="369b9-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="369b9-118">Valitse **Tuotteet**-sivulla sen luokan nimi, jota haluat täydentää luokkasivulla.</span><span class="sxs-lookup"><span data-stu-id="369b9-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="369b9-119">Valitun luokan oletusluokkasivu avautuu sivueditoriin.</span><span class="sxs-lookup"><span data-stu-id="369b9-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="369b9-120">Valitse **Täydennä luokkasivua**.</span><span class="sxs-lookup"><span data-stu-id="369b9-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="369b9-121">Valitse täydennetyn luokkasivun malli.</span><span class="sxs-lookup"><span data-stu-id="369b9-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="369b9-122">Jos teet vain vähäisiä muutoksia, voit valita oletusluokkasivun.</span><span class="sxs-lookup"><span data-stu-id="369b9-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="369b9-123">Vaihtoehtoisesti voit valita tietyn luokkasivunmallin.</span><span class="sxs-lookup"><span data-stu-id="369b9-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="369b9-124">Kun valitset mallin, sivueditori avataan ja valitun mallin avulla luodaan uusi luokkasivu valitulle luokalle.</span><span class="sxs-lookup"><span data-stu-id="369b9-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="369b9-125">Sivu kuitataan ulos sinulle. Nyt voit tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="369b9-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="369b9-126">Moduulit, joissa käytetään luokan määritystietoja, käyttävät valitun luokan tietoja.</span><span class="sxs-lookup"><span data-stu-id="369b9-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="369b9-127">Valitsemasi mallin asetukset määrittävät muutokset, jotka voit tehdä.</span><span class="sxs-lookup"><span data-stu-id="369b9-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="369b9-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="369b9-128">Additional resources</span></span>

[<span data-ttu-id="369b9-129">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="369b9-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="369b9-130">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="369b9-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="369b9-131">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="369b9-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="369b9-132">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="369b9-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="369b9-133">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="369b9-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="369b9-134">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="369b9-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="369b9-135">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="369b9-135">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="369b9-136">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="369b9-136">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
