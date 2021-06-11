---
title: Tuotedimensioiden näyttöasetusten kohdistaminen
description: Tässä ohjeaiheessa kerrotaan tuotedimensioiden näyttöasetuksista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117221"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="b843b-103">Tuotedimensioiden näyttöasetusten kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="b843b-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b843b-104">Tässä ohjeaiheessa kerrotaan tuotedimensioiden näyttöasetuksista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="b843b-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b843b-105">Dynamics 365 Commerce tukee koko-, tyyli- ja väridimensioita, jotta tuotemuuttujat erotetaan toisistaan.</span><span class="sxs-lookup"><span data-stu-id="b843b-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="b843b-106">Dimensiot näytetään yleensä tekstiarvoina, kuten "pieni", "keskikokoinen" ja "suuri" kokoja varten, ja väreistä "musta" ja "ruskea".</span><span class="sxs-lookup"><span data-stu-id="b843b-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="b843b-107">Jos tuote tukee useita muunnelmia, tuotemuuttujan selaaminen voi olla vaikeaa, koska kunkin muuttujan kuvan tarkasteleminen edellyttää useita valintoja.</span><span class="sxs-lookup"><span data-stu-id="b843b-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="b843b-108">Commercen versio 10.0.20 voi helpottaa tuotemuuttujan selaamista, koska se käyttää kuvia ja heksadesimaalikoodeja (hex) dimensioiden näyttämiseen väriruutuina.</span><span class="sxs-lookup"><span data-stu-id="b843b-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="b843b-109">Commercen sivustotyökalussa dimensioasetukset määritetään kohdassa **Sivuston asetukset \> Laajennukset \> Dimensioasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b843b-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="b843b-110">Seuraavassa kuvassa on esimerkki sivustonmuodostuksen dimensioasetuksista.</span><span class="sxs-lookup"><span data-stu-id="b843b-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Esimerkki Commercen sivustonmuodostustyökalun sivustoasetuksista](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="b843b-112">Käytettävissä on kaksi dimensioasetusta:</span><span class="sxs-lookup"><span data-stu-id="b843b-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="b843b-113">**Dimensiot, jotka näytetään kuvana** – Määritä, mitkä dimensiot näkyvät väriruutuina sähköisen kaupankäynnin verkkosivuilla, kuten tuotetietosivuilla (PDF-sivut) ja hakutulosluettelosivuilla.</span><span class="sxs-lookup"><span data-stu-id="b843b-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="b843b-114">Mikä tahansa väri-, koko- ja tyylidimensioiden yhdistelmä voidaan näyttää väriruutuna.</span><span class="sxs-lookup"><span data-stu-id="b843b-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="b843b-115">Jos dimensio on valittu näytettäväksi väriruutuna silloin, Commerce-moduulin muodostaminen näyttää käytettävissä olevan hex-koodimallin väriruutukonfiguraation.</span><span class="sxs-lookup"><span data-stu-id="b843b-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="b843b-116">Jos hex-koodia ei ole määritetty, järjestelmälogiikka etsii kuvan URL-osoitteen väriruudun konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="b843b-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="b843b-117">Jos hex-koodia eikä kuvan URL-osoitetta ei ole määritetty, teksti tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="b843b-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="b843b-118">Seuraavassa kuvassa on esimerkki, jossa sähköisen kauppasivuston PDP sisältää väri- ja kokoväriruudut.</span><span class="sxs-lookup"><span data-stu-id="b843b-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="b843b-119">Tässä esimerkissä väridimensiolle on konfiguroitu heksadesimaalikoodi.</span><span class="sxs-lookup"><span data-stu-id="b843b-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="b843b-120">Näin ollen väriruudut näytetään väreinä.</span><span class="sxs-lookup"><span data-stu-id="b843b-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="b843b-121">Kokodimensiolle ei kuitenkaan ole määritetty heksadesimaalikoodia eikä kuvan URL-osoitetta.</span><span class="sxs-lookup"><span data-stu-id="b843b-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="b843b-122">Näin ollen näkyvissä on teksti.</span><span class="sxs-lookup"><span data-stu-id="b843b-122">Therefore, text is shown.</span></span>

    ![Esimerkki sähköisen kaupan tuotetietosivulla väriruutuina näkyvistä väridimensioista](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="b843b-124">**Tuotekortissa näytettävät dimensiot** – Määritä, mitkä dimensiot näkyvät luetteloissa ja luettelosivuilla näkyvissä tuotekorteissa.</span><span class="sxs-lookup"><span data-stu-id="b843b-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="b843b-125">Ennen kuin dimensio voidaan näyttää tuotekortissa, tämän asetuksen on oltava käytössä dimensiolle.</span><span class="sxs-lookup"><span data-stu-id="b843b-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="b843b-126">Myös **Kuvana näytettävät dimensiot** -asetus tulisi ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b843b-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="b843b-127">Tuotekorttien väriruudun valinta on optimoitu väridimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="b843b-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="b843b-128">Muiden dimensioiden osalta saattaa olla tarpeen käyttää näkymän alanumeroa, jotta valintaa voidaan mukauttaa.</span><span class="sxs-lookup"><span data-stu-id="b843b-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="b843b-129">Seuraavassa kuvassa on esimerkki, jossa sähköisen kauppasivuston luettelosivu sisältää tuotekortteja, joilla on väriruudut.</span><span class="sxs-lookup"><span data-stu-id="b843b-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Esimerkki sähköisen kaupan luettelosivulla väriruutuina näkyvistä väridimensioista](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="b843b-131">Lisätietoja tuotedimensioiden konfiguroinnista niin, että ne näkyvät verkkosivuilla väriruutuina, on kohdassa [Tuotedimension arvojen konfiguroiminen näkymään väriruutuina](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="b843b-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b843b-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b843b-132">Additional resources</span></span>

[<span data-ttu-id="b843b-133">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b843b-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b843b-134">Hakutulosmoduuli</span><span class="sxs-lookup"><span data-stu-id="b843b-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="b843b-135">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="b843b-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b843b-136">Tuotedimensioarvojen konfiguroiminen näkymään väriruutuina</span><span class="sxs-lookup"><span data-stu-id="b843b-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]