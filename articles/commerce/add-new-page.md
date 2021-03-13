---
title: Uuden sivuston sivun lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten uusi sivu lisätään Microsoft Dynamics 365 Commerce -sovelluksessa.
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
ms.openlocfilehash: 54e690b0dde048b17ce074fcc30cf20a9ff7a4ca
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097126"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="f2ee3-103">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f2ee3-104">Tässä ohjeaiheessa kerrotaan, miten uusi sivu lisätään Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2ee3-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f2ee3-105">Overview</span></span>

<span data-ttu-id="f2ee3-106">Kun olet luonut sivustoon malleja ja osia, seuraava vaihe on luoda sivuja, jotka käyttävät malleja ja osia.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="f2ee3-107">Valitse ensin malli tai asettelu, sivun nimi ja sivun URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="f2ee3-108">Malli tai asettelu</span><span class="sxs-lookup"><span data-stu-id="f2ee3-108">Template or layout</span></span>

<span data-ttu-id="f2ee3-109">Voit käyttää uudella sivulla mallia tai asettelua.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="f2ee3-110">Lisätietoja on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="f2ee3-111">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="f2ee3-111">Page name</span></span>

<span data-ttu-id="f2ee3-112">Sivun nimen on oltava yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-112">The page name must be unique to your page.</span></span> <span data-ttu-id="f2ee3-113">Sen on oltava kuvaava, jotta voit löytää sen helposti ja muut tietävät, mitä varten sivu on tarkoitettu.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="f2ee3-114">Valitse sivun nimi huolellisesti, koska sitä ei voi muuttaa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="f2ee3-115">Sivun URL</span><span class="sxs-lookup"><span data-stu-id="f2ee3-115">Page URL</span></span>

<span data-ttu-id="f2ee3-116">Voit määrittää uuden sivun URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="f2ee3-117">Kun luot sivun, voit kirjoittaa merkkijonon, jota käytetään täydellisen URL-osoitteen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="f2ee3-118">Tämä merkkijono on suhteellinen URL-osoite tai URL-osoitteen kuvaava osa.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="f2ee3-119">Koko URL-osoite muodostetaan URL-osoitteen kuvaavan osan perusteella. Uusi sivu liitetään siihen.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="f2ee3-120">Voit muuttaa URL-osoitteen kuvaavaa osaa myöhemmin ennen sivun julkaisemista.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="f2ee3-121">Lisätietoja on kohdassa [Sivun URL-osoitteen luominen](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f2ee3-122">Dynamics 365 Commerce irrottaa URL-osoitteet ja sisällön.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="f2ee3-123">Toisin sanoen voidaan luoda situ, jota ei ole liitetty URL-osoitteeseen. Samoin voidaan luoda URL-osoite, jota ei ole liitetty sivuun.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="f2ee3-124">Tämän vuoksi sisällön vaihtamisen voi tehdä URL-osoitteelle, eikä siitä seuraa käyttökatkoksia. Uudelleenohjauksia on myös helppo hallita.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="f2ee3-125">Uuden sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-125">Add a new page</span></span>

<span data-ttu-id="f2ee3-126">Voit lisätä sivustoon uuden sivuston sivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="f2ee3-127">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f2ee3-128">Valitse **Uusi sivu**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-128">Select **New Page**.</span></span>
1. <span data-ttu-id="f2ee3-129">Valitse **Uusi sivu** -valintaikkunassa malli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="f2ee3-130">Anna **Sivun nimi** -kenttään sivun nimi (esimerkiksi **Oma uusi sivu**).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="f2ee3-131">Anna **URL-osoite**-kenttään merkkijono (URL-osoitteen kuvaava osa) ja tee URL-osoite valmiiksi (esimerkiksi **omauusisivu**).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="f2ee3-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-132">Select **OK**.</span></span> <span data-ttu-id="f2ee3-133">Sivueditori avautuu.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-133">The page editor appears.</span></span> <span data-ttu-id="f2ee3-134">Huomaa, että ylä- ja alatunniste lisätään sivulle automaattisesti valitsemasi mallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="f2ee3-135">Valitse sivun jäsennyksessä **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2ee3-136">Valitse **Säilö** ja valitse sitten **OK**</span><span class="sxs-lookup"><span data-stu-id="f2ee3-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="f2ee3-137">Valitse **Nestesäilö**. Valitse kolmen pisteen painike ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2ee3-138">Valitse **Sisällöntäyteinen lohko** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2ee3-139">Valitse **Sisällöntäyteinen lohko**. Valitse kolmen pisteen painike ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2ee3-140">Valitse **Sisällöntäyteinen lohkonimike** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2ee3-141">Valitse oikeanpuoleisessa ominaisuusruudussa **Kappale** ja kirjoita kenttään **Oma tekstiteksti**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="f2ee3-142">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="f2ee3-143">Syötä **Kommentit**-kenttään **Lisätty uusi sivu** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2ee3-144">Esikatsele sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="f2ee3-145">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="f2ee3-146">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-146">Select **Publish**.</span></span>
1. <span data-ttu-id="f2ee3-147">Valitse siirtymispolussa (navigointilinkit) **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="f2ee3-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f2ee3-148">Valitse vasemmanpuoleisessa siirtymisruudussa **URL-osoitteet**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="f2ee3-149">Etsi ja valitse oma URL-osoite (**omauusisivu**) luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="f2ee3-150">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f2ee3-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2ee3-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f2ee3-151">Additional resources</span></span>

[<span data-ttu-id="f2ee3-152">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="f2ee3-153">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="f2ee3-154">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="f2ee3-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="f2ee3-155">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="f2ee3-156">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="f2ee3-157">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="f2ee3-158">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="f2ee3-158">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="f2ee3-159">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="f2ee3-159">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
