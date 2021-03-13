---
title: Tuotesivun täydentäminen
description: Tässä ohjeaiheessa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097335"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="38cdb-103">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="38cdb-104">Tässä ohjeaiheessa kerrotaan, miten tuotesivua täydennetään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="38cdb-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="38cdb-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="38cdb-105">Overview</span></span>

<span data-ttu-id="38cdb-106">Oletusarvon mukaan sivustossa käytetään yleistä sivua tuotetietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="38cdb-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="38cdb-107">Tämä sivu sisältää perustiedot tuotteesta ja sen myynnissä vaadittavista ohjausobjekteista.</span><span class="sxs-lookup"><span data-stu-id="38cdb-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="38cdb-108">Voit kuitenkin täydentää Commerce Scale Unitin tietoja tiettyä tuotetta koskevilla kuvilla tai tekstillä.</span><span class="sxs-lookup"><span data-stu-id="38cdb-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="38cdb-109">Tätä prosessia kutsutaan tuotesivun täydentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="38cdb-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="38cdb-110">Usein tuotteita varten halutaan käyttää erityistä lisäsisältöä.</span><span class="sxs-lookup"><span data-stu-id="38cdb-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="38cdb-111">Kun siirryt **Retail ja Commerce**-kohtaan muokkaustyökalussa, näkyviin tulee tuoteluettelo kanavasta, joka on liitetty sivustoon.</span><span class="sxs-lookup"><span data-stu-id="38cdb-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="38cdb-112">Tässä luettelossa **Täydennetty**-sarake ilmaisee, onko tuotteen tuotesivua täydennetty.</span><span class="sxs-lookup"><span data-stu-id="38cdb-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="38cdb-113">Jos sarakkeessa on valintamerkki, tuotteella on täydennetty tuotesivu.</span><span class="sxs-lookup"><span data-stu-id="38cdb-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="38cdb-114">Jos valintamerkkiä ei ole, tuotteella käytetään oletustuotesivua ja -sisältöä.</span><span class="sxs-lookup"><span data-stu-id="38cdb-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="38cdb-115">Voit esikatsella sekä täydennettyjä että muita kuin täydennettyjä tuotesivuja valitsemalla tuotteen nimen luettelosta.</span><span class="sxs-lookup"><span data-stu-id="38cdb-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="38cdb-116">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-116">Enrich a product page</span></span>

<span data-ttu-id="38cdb-117">Voit täydentää tuotesivua noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="38cdb-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="38cdb-118">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="38cdb-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="38cdb-119">Valitse vasemmanpuoleisessa siirtymisruudussa **Tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="38cdb-120">Valitse mikä tahansa tuote, jolla ei ole täydennettyä tuotesivua.</span><span class="sxs-lookup"><span data-stu-id="38cdb-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="38cdb-121">Valitse toimintoruudussa **Täydennä tuotesivua**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="38cdb-122">Valitse **PDP-malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="38cdb-123">Laajenna sivun vasemmanpuoleisen jäsennyspuun **pääpaikka**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="38cdb-124">Valitse kolmen pisteen painike (**...**) **pääpaikalle** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="38cdb-125">Valitse **Säilö 2** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="38cdb-126">Valitse paikan kolmen pisteen painike **säilölle 2** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="38cdb-127">Valitse **Ominaisuus** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="38cdb-128">Syötä oikealla olevassa ominaisuusruudussa **RTF**-kenttään tuotteen päivitetty kuvaus.</span><span class="sxs-lookup"><span data-stu-id="38cdb-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="38cdb-129">Syötä **Otsikko**-kenttään otsikkoteksti ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="38cdb-130">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="38cdb-131">Syötä **Kommentit**-kenttään **Täydennä tuotetta** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="38cdb-132">Esikatsele täydennettyä tuotesivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="38cdb-133">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="38cdb-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="38cdb-134">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="38cdb-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38cdb-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="38cdb-135">Additional resources</span></span>

[<span data-ttu-id="38cdb-136">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="38cdb-137">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="38cdb-138">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="38cdb-139">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="38cdb-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="38cdb-140">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="38cdb-141">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="38cdb-142">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="38cdb-142">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="38cdb-143">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="38cdb-143">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
