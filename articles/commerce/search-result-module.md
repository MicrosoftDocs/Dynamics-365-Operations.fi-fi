---
title: Hakutulosmoduuli
description: Tässä ohjeaiheessa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3409e9e99329def55b173eb78cf03db4a6764c92
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794112"
---
# <a name="search-results-module"></a><span data-ttu-id="1c586-103">Hakutulosmoduuli</span><span class="sxs-lookup"><span data-stu-id="1c586-103">Search results module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c586-104">Tässä ohjeaiheessa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="1c586-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1c586-105">Hakutulosmoduuli palauttaa tuotehaun tulokset ja luettelon tuotteisiin käytettävistä tarkennuksista.</span><span class="sxs-lookup"><span data-stu-id="1c586-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="1c586-106">Dynamics 365 Commerce -sivustojen hakutulosmoduulien avulla voit muodostaa sivuja seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="1c586-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="1c586-107">Käyttäjähaun käynnistämät hakutulokset</span><span class="sxs-lookup"><span data-stu-id="1c586-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="1c586-108">Hakutulokset, jotka näyttävät tietyn tuotejoukon, kuten "Ota samankaltaisia tuotteita"</span><span class="sxs-lookup"><span data-stu-id="1c586-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="1c586-109">Luettelo tuotteista, jotka kuuluvat luokkaan</span><span class="sxs-lookup"><span data-stu-id="1c586-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="1c586-110">Lisätietoja luokka- ja hakutulossivuista on ohjeessa [Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1c586-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="1c586-111">Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston luokan hakutulossivusta.</span><span class="sxs-lookup"><span data-stu-id="1c586-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Esimerkki hakutulossivusta Fabrikam-sivustolla](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="1c586-113">Hakutulosmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1c586-113">Search results module properties</span></span>

<span data-ttu-id="1c586-114">Seuraavassa taulukossa luetellaan hakutulosmoduulien ominaisuudet sekä niiden arvot ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="1c586-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="1c586-115">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="1c586-115">Property</span></span> | <span data-ttu-id="1c586-116">Arvot</span><span class="sxs-lookup"><span data-stu-id="1c586-116">Values</span></span> | <span data-ttu-id="1c586-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1c586-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="1c586-118">Tuotteita sivulla</span><span class="sxs-lookup"><span data-stu-id="1c586-118">Items per page</span></span> | <span data-ttu-id="1c586-119">Kokonaisluku</span><span class="sxs-lookup"><span data-stu-id="1c586-119">Integer</span></span> | <span data-ttu-id="1c586-120">Kullakin sivulla näkyvien nimikkeiden määrä.</span><span class="sxs-lookup"><span data-stu-id="1c586-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="1c586-121">Salli varmuuskopiointi PDP-kohteessa</span><span class="sxs-lookup"><span data-stu-id="1c586-121">Allow back on PDP</span></span> | <span data-ttu-id="1c586-122">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1c586-122">**True** or **False**</span></span> | <span data-ttu-id="1c586-123">Jos tämän ominaisuuden arvoksi määritetään **Tosi**, kun käyttäjä valitsee tuotteen hakutulossivulta, avautuvan tuotetietosivun (PDP) siirtymispolku näyttää Takaisin tuloksiin -linkin.</span><span class="sxs-lookup"><span data-stu-id="1c586-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="1c586-124">Laajenna tarkennukset</span><span class="sxs-lookup"><span data-stu-id="1c586-124">Expand Refiners</span></span> | <span data-ttu-id="1c586-125">**Kaikki**, **1**, **2**, **3** tai **4**</span><span class="sxs-lookup"><span data-stu-id="1c586-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="1c586-126">Tärkeimpien tarkentajien määrä, jotka tulisi laajentaa, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="1c586-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="1c586-127">Jos ominaisuuden arvoksi määritetään esimerkiksi **3**, sivun ensimmäiset kolme tarkentajaa laajennetaan.</span><span class="sxs-lookup"><span data-stu-id="1c586-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="1c586-128">Piilota luokkahierarkian näyttö</span><span class="sxs-lookup"><span data-stu-id="1c586-128">Hide category hierarchy display</span></span> | <span data-ttu-id="1c586-129">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1c586-129">**True** or **False**</span></span> | <span data-ttu-id="1c586-130">Jos ominaisuuden arvoksi määritetään **Tosi**, sivulla näkyvä luokkahierarkia piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="1c586-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="1c586-131">Tämän ominaisuuden arvoksi tulee määrittää **Tosi**, jos luokkahierarkian näyttämiseen käytetään [siirtymispolkumoduulia](add-breadcrumb.md).</span><span class="sxs-lookup"><span data-stu-id="1c586-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="1c586-132">Sisällytä tuotemääritteet hakutuloksiin</span><span class="sxs-lookup"><span data-stu-id="1c586-132">Include product attributes in search results</span></span> | <span data-ttu-id="1c586-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1c586-133">**True** or **False**</span></span> | <span data-ttu-id="1c586-134">Jos ominaisuuden arvoksi määritetään **Tosi**, tuotteiden määritteet palautetaan hakutuloksissa.</span><span class="sxs-lookup"><span data-stu-id="1c586-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="1c586-135">Vaikka nämä määritteet voidaankin näyttää Commerce-sivustossa, laajennus on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="1c586-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="1c586-136">Näytä liitoksen hinnat</span><span class="sxs-lookup"><span data-stu-id="1c586-136">Show affiliation prices</span></span> | <span data-ttu-id="1c586-137">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1c586-137">**True** or **False**</span></span> | <span data-ttu-id="1c586-138">Jos tämän ominaisuuden arvoksi määritetään **Tosi**, tuotteiden liittyvät hinnat näkyvät tuloksissa, kun kirjautunut käyttäjä selaa sivua.</span><span class="sxs-lookup"><span data-stu-id="1c586-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="1c586-139">Dynamics 365 Commerce -julkaisussa 10.0.16 ja sitä myöhemmissä versioissa **Näytä liittyvät hinnat** -konfiguraatiota voidaan käyttää liittyvien hintojen näyttämiseen sivulla.</span><span class="sxs-lookup"><span data-stu-id="1c586-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="1c586-140">Tuetut moduulit</span><span class="sxs-lookup"><span data-stu-id="1c586-140">Supported modules</span></span>

<span data-ttu-id="1c586-141">Hakutulosmoduuli tukee [pikanäkymämoduulia](quick-view-module.md), jonka avulla käyttäjät voivat tarkastella tuotetietoja ja lisätä nimikkeitä ostoskoriin hakutulossivulta.</span><span class="sxs-lookup"><span data-stu-id="1c586-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="1c586-142">Hakutulosmoduulin lisääminen luokkasivulle</span><span class="sxs-lookup"><span data-stu-id="1c586-142">Add a search results module to a category page</span></span>

<span data-ttu-id="1c586-143">Voit lisätä luokkasivulle hakutulosmoduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1c586-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="1c586-144">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="1c586-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1c586-145">Kirjoita **Uusi malli** -valintaikkunassa nimi **Hakutulokset** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c586-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="1c586-146">Valitse kolme pistettä (...) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="1c586-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1c586-147">Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c586-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1c586-148">Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (...) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="1c586-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1c586-149">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c586-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1c586-150">Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="1c586-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1c586-151">Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c586-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1c586-152">Anna sitten **Navigointipolku**-omiansiuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä**.</span><span class="sxs-lookup"><span data-stu-id="1c586-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="1c586-153">Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="1c586-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1c586-154">Valitse **Lisää moduuli** -valintaikkunassa **Hakutulokset**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c586-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1c586-155">Kirjoita **Hakutulokset**-ominaisuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä** ja määritä sitten muut hakutulosmoduulin pakolliset ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="1c586-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="1c586-156">Kun määrität nämä ominaisuudet malliin, varmistat, että tietyn luokkasivun mukautukset sisältävät nämä asetukset automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1c586-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="1c586-157">Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.</span><span class="sxs-lookup"><span data-stu-id="1c586-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="1c586-158">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="1c586-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="1c586-159">Valitse **Valitse malli** -valintaikkunassa luomasi **Hakutulokset**-malli, kirjoita **sivun nimeksi** **Luokkasivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c586-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="1c586-160">Koska kaikki arvot on määritetty mallissa, sivu on valmis julkaistavaksi.</span><span class="sxs-lookup"><span data-stu-id="1c586-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="1c586-161">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="1c586-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c586-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1c586-162">Additional resources</span></span>

[<span data-ttu-id="1c586-163">Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1c586-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="1c586-164">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1c586-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1c586-165">Pikanäkymämoduuli</span><span class="sxs-lookup"><span data-stu-id="1c586-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
