---
title: Luokan saapumissivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab152dff0925f9c816419083577b5272ac813be
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945777"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="0424a-103">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="0424a-103">Enrich a category landing page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0424a-104">Tässä ohjeaiheessa kerrotaan luokkasivujen täydentämisestä Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0424a-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0424a-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0424a-105">Overview</span></span>

<span data-ttu-id="0424a-106">Commerce tarjoaa oletusluokan saapumissivun, jota käytetään, kun luokkatiedot näytetään.</span><span class="sxs-lookup"><span data-stu-id="0424a-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="0424a-107">Oletusluokkasivulla on pakollisia elementtejä, kuten tarkentimia, luokiteltua tuotesijoittelua, lajitteluvaihtoehtoja, valinnan yhteenveto ja sivutuksen ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="0424a-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="0424a-108">Oletusluokkasivun sijaan voidaan käyttää luokan täydennettyä saapumissivua. Siinä on enemmän sisältöä ja erityisiä elementtejä.</span><span class="sxs-lookup"><span data-stu-id="0424a-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="0424a-109">Tyypilliseen täydennykseen voi kuulua luokkakohtaisen markkinointisisällön lisääminen luokkasivulle.</span><span class="sxs-lookup"><span data-stu-id="0424a-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="0424a-110">Tämä sisältö voi sisältää eri luokkien tuotesijoittelua ristiinmyyntitarkoituksia, toimituksellisia luetteloita, kuvia, videoita ja muuta tekstiä varten.</span><span class="sxs-lookup"><span data-stu-id="0424a-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="0424a-111">Voit muokata oletusluokkasivua tai määrittää tietylle luokalle toisen luokkasivun.</span><span class="sxs-lookup"><span data-stu-id="0424a-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Täydennetty luokan saapumissivu](./media/CategoryLandingPages.png)

<span data-ttu-id="0424a-113">Muokkaustyökalun **Tuote**-sivulla on luokkaluettelo kanavista, jotka on määritetty sivustoon.</span><span class="sxs-lookup"><span data-stu-id="0424a-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="0424a-114">Jos luokkasivulle on valittu **Täydennetty**-tila, luokkasivua on täydennetty.</span><span class="sxs-lookup"><span data-stu-id="0424a-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="0424a-115">Muussa tapauksessa luokassa käytetään oletusluokkasivua ja -sisältöä.</span><span class="sxs-lookup"><span data-stu-id="0424a-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="0424a-116">Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä luokkasivuja luokassa valitsemalla luokan nimen.</span><span class="sxs-lookup"><span data-stu-id="0424a-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="0424a-117">Voit täydentää luokkasivua seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0424a-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="0424a-118">Valitse **Tuotteet**-sivulla sen luokan nimi, jonka luokkasivun haluat täydentää.</span><span class="sxs-lookup"><span data-stu-id="0424a-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="0424a-119">Valitun luokan oletusluokkasivu avautuu sivueditoriin.</span><span class="sxs-lookup"><span data-stu-id="0424a-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="0424a-120">Valitse **Täydennä luokkasivua**.</span><span class="sxs-lookup"><span data-stu-id="0424a-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="0424a-121">Valitse täydennetyn luokkasivun malli.</span><span class="sxs-lookup"><span data-stu-id="0424a-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="0424a-122">Jos teet vain vähäisiä muutoksia, voit valita oletusluokkasivun.</span><span class="sxs-lookup"><span data-stu-id="0424a-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="0424a-123">Vaihtoehtoisesti voit valita tietyn luokkasivunmallin.</span><span class="sxs-lookup"><span data-stu-id="0424a-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="0424a-124">Kun valitset mallin, sivueditori avataan ja valitun mallin avulla luodaan uusi luokkasivu valitulle luokalle.</span><span class="sxs-lookup"><span data-stu-id="0424a-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="0424a-125">Sivu kuitataan ulos sinulle. Nyt voit tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="0424a-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="0424a-126">Moduulit, joissa käytetään luokan määritystietoja, käyttävät valitun luokan tietoja.</span><span class="sxs-lookup"><span data-stu-id="0424a-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="0424a-127">Valitsemasi mallin asetukset määrittävät muutokset, jotka voit tehdä.</span><span class="sxs-lookup"><span data-stu-id="0424a-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0424a-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0424a-128">Additional resources</span></span>

[<span data-ttu-id="0424a-129">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="0424a-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0424a-130">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="0424a-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0424a-131">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="0424a-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0424a-132">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="0424a-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0424a-133">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="0424a-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0424a-134">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="0424a-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0424a-135">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="0424a-135">Verify page content accessibility</span></span>](verify-accessibility.md)
