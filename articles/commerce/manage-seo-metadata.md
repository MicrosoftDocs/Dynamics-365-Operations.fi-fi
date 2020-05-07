---
title: SEO-metatietojen hallinta
description: Tässä ohjeaiheessa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 74229628e48ffb8ac974acd868e325eeca77d91e
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270047"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="3b457-103">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="3b457-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3b457-104">Tässä ohjeaiheessa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3b457-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3b457-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="3b457-105">Overview</span></span>

<span data-ttu-id="3b457-106">Sivuston hakukoneoptimoinnin metatietoja voi hallita sivustokarttojen ja sivun metatietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="3b457-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="3b457-107">Sivustokartat</span><span class="sxs-lookup"><span data-stu-id="3b457-107">Site maps</span></span>

<span data-ttu-id="3b457-108">Sivustokartta on sivuston sivujen koneluettava luettelo, joka on XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="3b457-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="3b457-109">Se on tarkoitettu hakuohjelmien käyttöön. Näin ne voivat tarjota parempia hakutuloksia sivustosta.</span><span class="sxs-lookup"><span data-stu-id="3b457-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="3b457-110">Hakuohjelmat voivat käyttää sivustokarttoja manuaalisesti tai ne voidaan julkaista robots.txt-tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="3b457-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="3b457-111">Dynamics 365 Commerce tukee sivustokarttojen automaattista luontia.</span><span class="sxs-lookup"><span data-stu-id="3b457-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="3b457-112">Sivustokartat päivittyvät automaattisesti, kun sivut julkaistaan tai niiden julkaiseminen perutaan.</span><span class="sxs-lookup"><span data-stu-id="3b457-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="3b457-113">Sivustokartan luonnin ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="3b457-113">Turn on site map generation</span></span>

1. <span data-ttu-id="3b457-114">Kirjaudu sisään muokkaustyökaluun.</span><span class="sxs-lookup"><span data-stu-id="3b457-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="3b457-115">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="3b457-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3b457-116">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivuston hallinta**.</span><span class="sxs-lookup"><span data-stu-id="3b457-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="3b457-117">Varmista, että **Sivustokartta käytössä** -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="3b457-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="3b457-118">Sivun metatiedot</span><span class="sxs-lookup"><span data-stu-id="3b457-118">Page metadata</span></span>

<span data-ttu-id="3b457-119">Dynamics 365 Commercen avulla voit hallita yksittäisten sivujen hakukoneoptimoinnin metatietoja.</span><span class="sxs-lookup"><span data-stu-id="3b457-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="3b457-120">Voit tarkastella ja muokata näitä tietoja sivusäilön **Hakukoneoptimoinnin ominaisuudet** -osassa.</span><span class="sxs-lookup"><span data-stu-id="3b457-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="3b457-121">Seuraavia hakukoneoptimoinnin metatietojen ominaisuuksia tuetaan:</span><span class="sxs-lookup"><span data-stu-id="3b457-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="3b457-122">Titteli</span><span class="sxs-lookup"><span data-stu-id="3b457-122">Title</span></span>
- <span data-ttu-id="3b457-123">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3b457-123">Description</span></span>
- <span data-ttu-id="3b457-124">Hakukoneoptimoinnin avainsanat</span><span class="sxs-lookup"><span data-stu-id="3b457-124">SEO keywords</span></span>
- <span data-ttu-id="3b457-125">Aria-otsikot</span><span class="sxs-lookup"><span data-stu-id="3b457-125">Aria labels</span></span>
- <span data-ttu-id="3b457-126">noindex</span><span class="sxs-lookup"><span data-stu-id="3b457-126">noindex</span></span>
- <span data-ttu-id="3b457-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="3b457-127">nofollow</span></span>
- <span data-ttu-id="3b457-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="3b457-128">noarchive</span></span>
- <span data-ttu-id="3b457-129">nocache</span><span class="sxs-lookup"><span data-stu-id="3b457-129">nocache</span></span>
- <span data-ttu-id="3b457-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="3b457-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="3b457-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="3b457-131">nosnippet</span></span>
- <span data-ttu-id="3b457-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="3b457-132">noImageIndex</span></span>
- <span data-ttu-id="3b457-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="3b457-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="3b457-134">Sivun metatietojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="3b457-134">Modify page metadata</span></span>

<span data-ttu-id="3b457-135">Voit muokata sivun metatietoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3b457-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="3b457-136">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="3b457-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3b457-137">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="3b457-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="3b457-138">Valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="3b457-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="3b457-139">Valitse komentopalkissa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3b457-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="3b457-140">Laajenna oikeanpuoleisessa ominaisuusruudussa **Oletusmetatunnukset**-kohta.</span><span class="sxs-lookup"><span data-stu-id="3b457-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="3b457-141">Jos haluat lisätä uuden metatunnuksen, valitse **Lisää**ja kirjoita sitten tunnus kenttään.</span><span class="sxs-lookup"><span data-stu-id="3b457-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="3b457-142">Jos haluat poistaa olemassa olevan metatunnuksen, valitse sen oikealla puolella oleva roskakorisymboli.</span><span class="sxs-lookup"><span data-stu-id="3b457-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="3b457-143">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="3b457-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3b457-144">Syötä **Kommentit**-kenttään **Päivitetyt metatunnukset** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b457-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b457-145">Esikatsele sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="3b457-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="3b457-146">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3b457-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="3b457-147">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="3b457-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b457-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3b457-148">Additional resources</span></span>

[<span data-ttu-id="3b457-149">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="3b457-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="3b457-150">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="3b457-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3b457-151">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="3b457-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="3b457-152">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="3b457-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="3b457-153">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="3b457-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="3b457-154">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="3b457-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="3b457-155">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="3b457-155">Verify page content accessibility</span></span>](verify-accessibility.md)
