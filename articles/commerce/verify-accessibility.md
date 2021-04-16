---
title: Sivun sisällön helppokäyttöisyyden tarkistaminen
description: Tässä ohjeaiheessa kerrotaan, miten voit varmistaa sivun sisällön helppokäyttöisyyden Microsoft Dynamics 365 Commercella.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791628"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="0c9f0-103">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c9f0-104">Tässä ohjeaiheessa kerrotaan, miten voit varmistaa sivun sisällön helppokäyttöisyyden Microsoft Dynamics 365 Commercella.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0c9f0-105">Kun olet lopettanut sivun muuttamisen, varmista, että sisältö on kaikkien Web-sivustojen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="0c9f0-106">Commercen luontityökalujen avulla voit helposti tarkistaa sivun sisällön helppokäyttöisyyden käyttämällä integroitua [Microsoft Accessibility Insights](https://accessibilityinsights.io/) -palvelua.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="0c9f0-107">Tämä palvelu varmistaa sivusi sisällön uusimpien [World Wide Web Consortium (W3C) -helppokäyttöisyysohjeiden](https://www.w3.org/standards/webdesign/accessibility) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="0c9f0-108">[Microsoft Accessibility Insights](https://accessibilityinsights.io/) -integroinnin on oltava käytössä vuokraajassa tai sivustotasolla, ennen kuin sitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="0c9f0-109">Microsoftin helppokäyttöisyystietojen ottaminen käyttöön kaikissa vuokraajan sivustoissa</span><span class="sxs-lookup"><span data-stu-id="0c9f0-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="0c9f0-110">Voit ottaa [Microsoft helppokäyttöisyystietojen](https://accessibilityinsights.io/) -integroinnin käyttöön kaikissa vuokraajasi Commerce-sivustoissa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="0c9f0-111">Jotta voit käyttää vuokraajan asetuksia, sinun on oltava kirjautuneena sisään Commercen järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="0c9f0-112">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="0c9f0-113">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="0c9f0-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="0c9f0-114">Valitse **Vuokraajan asetukset** -kohdasta **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="0c9f0-115">Määritä **Helppokäyttötoiminnon tarkistus** -asetukseksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="0c9f0-116">Microsoftin helppokäyttötoimintotietojen ottaminen käyttöön yksittäisessä sivustossa</span><span class="sxs-lookup"><span data-stu-id="0c9f0-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="0c9f0-117">Voit ottaa [Microsoft helppokäyttöisyystietojen](https://accessibilityinsights.io/) -integroinnin käyttöön yhdessä Commerce-sivustossa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="0c9f0-118">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="0c9f0-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0c9f0-119">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="0c9f0-120">Valitse **Sivuston asetukset** -kohdasta **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="0c9f0-121">Määritä **Helppokäyttötoiminnon tarkistus** -asetukseksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="0c9f0-122">Kotisivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="0c9f0-123">Jos haluat käyttää integroitua [Microsoft helppokäyttöisyystiedot](https://accessibilityinsights.io/) -palvelua kotisivusi sisällön skannaukseen ja vahvistamiseen kaupankäynnin aikana, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0c9f0-124">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="0c9f0-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0c9f0-125">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="0c9f0-126">Etsi ja valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0c9f0-127">Valitse komentopalkissa **Tarkista helppokäyttöisyys**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="0c9f0-128">**Tarkista helppokäyttöisyys** -sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="0c9f0-129">Kun tarkistus on valmis, tarkista raportin sisältö.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="0c9f0-130">Jos jokin tarkistus epäonnistui, valitse jokainen epäonnistunut tarkistuskohde laajentaaksesi sitä, jotta voit nähdä lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="0c9f0-131">Jos haluat sulkea raportin sen jälkeen, kun olet tarkistanut sen, vieritä **Tarkista Helppokäyttötoiminnot** -sivun alareunaan ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c9f0-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0c9f0-132">Additional resources</span></span>

[<span data-ttu-id="0c9f0-133">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0c9f0-134">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0c9f0-135">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0c9f0-136">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="0c9f0-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0c9f0-137">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0c9f0-138">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0c9f0-139">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="0c9f0-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0c9f0-140">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="0c9f0-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
