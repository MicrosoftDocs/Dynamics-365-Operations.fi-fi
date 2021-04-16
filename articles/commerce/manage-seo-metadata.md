---
title: SEO-metatietojen hallinta
description: Tässä ohjeaiheessa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.
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
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794208"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="7edfd-103">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="7edfd-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7edfd-104">Tässä ohjeaiheessa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="7edfd-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7edfd-105">Sivuston hakukoneoptimoinnin metatietoja voi hallita sivustokarttojen ja sivun metatietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="7edfd-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="7edfd-106">Sivustokartat</span><span class="sxs-lookup"><span data-stu-id="7edfd-106">Site maps</span></span>

<span data-ttu-id="7edfd-107">Sivustokartta on sivuston sivujen koneluettava luettelo, joka on XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="7edfd-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="7edfd-108">Se on tarkoitettu hakuohjelmien käyttöön. Näin ne voivat tarjota parempia hakutuloksia sivustosta.</span><span class="sxs-lookup"><span data-stu-id="7edfd-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="7edfd-109">Hakuohjelmat voivat käyttää sivustokarttoja manuaalisesti tai ne voidaan julkaista robots.txt-tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="7edfd-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="7edfd-110">Dynamics 365 Commerce tukee sivustokarttojen automaattista luontia.</span><span class="sxs-lookup"><span data-stu-id="7edfd-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="7edfd-111">Sivustokartat päivittyvät automaattisesti, kun sivut julkaistaan tai niiden julkaiseminen perutaan.</span><span class="sxs-lookup"><span data-stu-id="7edfd-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="7edfd-112">Sivustokartan luonnin ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="7edfd-112">Turn on site map generation</span></span>

1. <span data-ttu-id="7edfd-113">Kirjaudu sisään muokkaustyökaluun.</span><span class="sxs-lookup"><span data-stu-id="7edfd-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="7edfd-114">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="7edfd-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7edfd-115">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivuston hallinta**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="7edfd-116">Varmista, että **Sivustokartta käytössä** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="7edfd-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="7edfd-117">Sivun metatiedot</span><span class="sxs-lookup"><span data-stu-id="7edfd-117">Page metadata</span></span>

<span data-ttu-id="7edfd-118">Dynamics 365 Commercen avulla voit hallita yksittäisten sivujen hakukoneoptimoinnin metatietoja.</span><span class="sxs-lookup"><span data-stu-id="7edfd-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="7edfd-119">Voit tarkastella ja muokata näitä tietoja sivusäilön **Hakukoneoptimoinnin ominaisuudet** -osassa.</span><span class="sxs-lookup"><span data-stu-id="7edfd-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="7edfd-120">Seuraavia hakukoneoptimoinnin metatietojen ominaisuuksia tuetaan:</span><span class="sxs-lookup"><span data-stu-id="7edfd-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="7edfd-121">Titteli</span><span class="sxs-lookup"><span data-stu-id="7edfd-121">Title</span></span>
- <span data-ttu-id="7edfd-122">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7edfd-122">Description</span></span>
- <span data-ttu-id="7edfd-123">Hakukoneoptimoinnin avainsanat</span><span class="sxs-lookup"><span data-stu-id="7edfd-123">SEO keywords</span></span>
- <span data-ttu-id="7edfd-124">Aria-otsikot</span><span class="sxs-lookup"><span data-stu-id="7edfd-124">Aria labels</span></span>
- <span data-ttu-id="7edfd-125">noindex</span><span class="sxs-lookup"><span data-stu-id="7edfd-125">noindex</span></span>
- <span data-ttu-id="7edfd-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="7edfd-126">nofollow</span></span>
- <span data-ttu-id="7edfd-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="7edfd-127">noarchive</span></span>
- <span data-ttu-id="7edfd-128">nocache</span><span class="sxs-lookup"><span data-stu-id="7edfd-128">nocache</span></span>
- <span data-ttu-id="7edfd-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="7edfd-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="7edfd-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="7edfd-130">nosnippet</span></span>
- <span data-ttu-id="7edfd-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="7edfd-131">noImageIndex</span></span>
- <span data-ttu-id="7edfd-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="7edfd-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="7edfd-133">Sivun metatietojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-133">Modify page metadata</span></span>

<span data-ttu-id="7edfd-134">Voit muokata sivun metatietoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7edfd-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="7edfd-135">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="7edfd-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7edfd-136">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="7edfd-137">Valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="7edfd-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="7edfd-138">Valitse komentopalkissa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="7edfd-139">Laajenna oikeanpuoleisessa ominaisuusruudussa **Oletusmetatunnukset**-kohta.</span><span class="sxs-lookup"><span data-stu-id="7edfd-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="7edfd-140">Jos haluat lisätä uuden metatunnuksen, valitse **Lisää** ja kirjoita sitten tunnus kenttään.</span><span class="sxs-lookup"><span data-stu-id="7edfd-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="7edfd-141">Jos haluat poistaa olemassa olevan metatunnuksen, valitse sen oikealla puolella oleva roskakorisymboli.</span><span class="sxs-lookup"><span data-stu-id="7edfd-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="7edfd-142">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7edfd-143">Syötä **Kommentit**-kenttään **Päivitetyt metatunnukset** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="7edfd-144">Esikatsele sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="7edfd-145">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7edfd-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="7edfd-146">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="7edfd-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7edfd-147">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7edfd-147">Additional resources</span></span>

[<span data-ttu-id="7edfd-148">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="7edfd-149">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="7edfd-150">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="7edfd-151">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="7edfd-152">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="7edfd-153">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="7edfd-154">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="7edfd-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="7edfd-155">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="7edfd-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
