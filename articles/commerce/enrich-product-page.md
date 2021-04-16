---
title: Tuotesivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799038"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="e4be4-103">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4be4-104">Tässä ohjeaiheessa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e4be4-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e4be4-105">Oletusarvon mukaan sivustossa käytetään yleistä sivua tuotetietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="e4be4-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="e4be4-106">Tämä sivu sisältää perustiedot tuotteesta ja sen myynnissä vaadittavista ohjausobjekteista.</span><span class="sxs-lookup"><span data-stu-id="e4be4-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="e4be4-107">Voit kuitenkin täydentää Commerce Scale Unitin tietoja tiettyä tuotetta koskevilla kuvilla tai tekstillä.</span><span class="sxs-lookup"><span data-stu-id="e4be4-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="e4be4-108">Tätä prosessia kutsutaan tuotesivun täydentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e4be4-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="e4be4-109">Usein tuotteita varten halutaan käyttää erityistä lisäsisältöä.</span><span class="sxs-lookup"><span data-stu-id="e4be4-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="e4be4-110">Kun siirryt **Retail ja Commerce**-kohtaan muokkaustyökalussa, näkyviin tulee tuoteluettelo kanavasta, joka on liitetty sivustoon.</span><span class="sxs-lookup"><span data-stu-id="e4be4-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="e4be4-111">Tässä luettelossa **Täydennetty**-sarake ilmaisee, onko tuotteen tuotesivua täydennetty.</span><span class="sxs-lookup"><span data-stu-id="e4be4-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="e4be4-112">Jos sarakkeessa on valintamerkki, tuotteella on täydennetty tuotesivu.</span><span class="sxs-lookup"><span data-stu-id="e4be4-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="e4be4-113">Jos valintamerkkiä ei ole, tuotteella käytetään oletustuotesivua ja -sisältöä.</span><span class="sxs-lookup"><span data-stu-id="e4be4-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="e4be4-114">Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä tuotesivuja valitsemalla tuotteen nimen luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e4be4-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="e4be4-115">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-115">Enrich a product page</span></span>

<span data-ttu-id="e4be4-116">Voit täydentää tuotesivua noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e4be4-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="e4be4-117">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="e4be4-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e4be4-118">Valitse vasemmanpuoleisessa siirtymisruudussa **Tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="e4be4-119">Valitse mikä tahansa tuote, jolla ei ole täydennettyä tuotesivua.</span><span class="sxs-lookup"><span data-stu-id="e4be4-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="e4be4-120">Valitse toimintoruudussa **Täydennä tuotesivua**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="e4be4-121">Valitse **PDP-malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4be4-122">Laajenna sivun vasemmanpuoleisen jäsennyspuun **pääpaikka**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="e4be4-123">Valitse kolmen pisteen painike (**...**) **pääpaikalle** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e4be4-124">Valitse **Säilö 2** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4be4-125">Valitse paikan kolmen pisteen painike **säilölle 2** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e4be4-126">Valitse **Ominaisuus** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4be4-127">Syötä oikealla olevassa ominaisuusruudussa **RTF**-kenttään tuotteen päivitetty kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e4be4-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="e4be4-128">Syötä **Otsikko**-kenttään otsikkoteksti ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="e4be4-129">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e4be4-130">Syötä **Kommentit**-kenttään **Täydennä tuotetta** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4be4-131">Esikatsele täydennettyä tuotesivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="e4be4-132">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e4be4-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e4be4-133">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e4be4-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4be4-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e4be4-134">Additional resources</span></span>

[<span data-ttu-id="e4be4-135">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e4be4-136">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e4be4-137">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e4be4-138">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="e4be4-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e4be4-139">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e4be4-140">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e4be4-141">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e4be4-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="e4be4-142">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="e4be4-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
