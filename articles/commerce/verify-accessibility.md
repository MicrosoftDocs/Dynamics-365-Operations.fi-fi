---
title: Sivun sisällön helppokäyttöisyyden tarkistaminen
description: Tässä ohjeaiheessa kerrotaan, miten voit varmistaa sivun sisällön helppokäyttöisyyden Microsoft Dynamics 365 Commercella.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70604ed16d72e519724aeb2c33bd4a91a8b26c8c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946003"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="b196c-103">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="b196c-103">Verify page content accessibility</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b196c-104">Tässä ohjeaiheessa kerrotaan, miten voit varmistaa sivun sisällön helppokäyttöisyyden Microsoft Dynamics 365 Commercella.</span><span class="sxs-lookup"><span data-stu-id="b196c-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b196c-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b196c-105">Overview</span></span>

<span data-ttu-id="b196c-106">Kun olet lopettanut sivun muuttamisen, varmista, että sisältö on kaikkien Web-sivustojen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b196c-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="b196c-107">Commercen luontityökalujen avulla voit helposti tarkistaa sivun sisällön helppokäyttöisyyden käyttämällä integroitua [Microsoft Accessibility Insights](https://accessibilityinsights.io/) -palvelua.</span><span class="sxs-lookup"><span data-stu-id="b196c-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="b196c-108">Tämä palvelu varmistaa sivusi sisällön uusimpien [World Wide Web Consortium (W3C) -helppokäyttöisyysohjeiden](https://www.w3.org/standards/webdesign/accessibility) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b196c-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="b196c-109">[Microsoft Accessibility Insights](https://accessibilityinsights.io/) -integroinnin on oltava käytössä vuokraajassa tai sivustotasolla, ennen kuin sitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="b196c-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="b196c-110">Microsoftin helppokäyttöisyystietojen ottaminen käyttöön kaikissa vuokraajan sivustoissa</span><span class="sxs-lookup"><span data-stu-id="b196c-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="b196c-111">Voit ottaa [Microsoft helppokäyttöisyystietojen](https://accessibilityinsights.io/) -integroinnin käyttöön kaikissa vuokraajasi Commerce-sivustoissa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b196c-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="b196c-112">Jotta voit käyttää vuokraajan asetuksia, sinun on oltava kirjautuneena sisään Commercen järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="b196c-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="b196c-113">Kirjaudu Commerce-järjestelmään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="b196c-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="b196c-114">Laajenna vasemmanpuoleisessa siirtymisruudussa **vuokraajan asetukset** (hammasratassymbolin vieressä).</span><span class="sxs-lookup"><span data-stu-id="b196c-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="b196c-115">Valitse **Vuokraajan asetukset** -kohdasta **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="b196c-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b196c-116">Määritä **Helppokäyttötoiminnon tarkistus** -asetukseksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="b196c-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="b196c-117">Microsoftin helppokäyttötoimintotietojen ottaminen käyttöön yksittäisessä sivustossa</span><span class="sxs-lookup"><span data-stu-id="b196c-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="b196c-118">Voit ottaa [Microsoft helppokäyttöisyystietojen](https://accessibilityinsights.io/) -integroinnin käyttöön yhdessä Commerce-sivustossa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b196c-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="b196c-119">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="b196c-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b196c-120">Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.</span><span class="sxs-lookup"><span data-stu-id="b196c-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="b196c-121">Valitse **Sivuston asetukset** -kohdasta **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="b196c-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b196c-122">Määritä **Helppokäyttötoiminnon tarkistus** -asetukseksi **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="b196c-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="b196c-123">Kotisivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="b196c-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="b196c-124">Jos haluat käyttää integroitua [Microsoft helppokäyttöisyystiedot](https://accessibilityinsights.io/) -palvelua kotisivusi sisällön skannaukseen ja vahvistamiseen kaupankäynnin aikana, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b196c-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b196c-125">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="b196c-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b196c-126">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="b196c-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="b196c-127">Etsi ja valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="b196c-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="b196c-128">Valitse komentopalkissa **Tarkista helppokäyttöisyys**.</span><span class="sxs-lookup"><span data-stu-id="b196c-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="b196c-129">**Tarkista helppokäyttöisyys** -sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="b196c-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="b196c-130">Kun tarkistus on valmis, tarkista raportin sisältö.</span><span class="sxs-lookup"><span data-stu-id="b196c-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="b196c-131">Jos jokin tarkistus epäonnistui, valitse jokainen epäonnistunut tarkistuskohde laajentaaksesi sitä, jotta voit nähdä lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="b196c-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="b196c-132">Jos haluat sulkea raportin sen jälkeen, kun olet tarkistanut sen, vieritä **Tarkista Helppokäyttötoiminnot** -sivun alareunaan ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b196c-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b196c-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b196c-133">Additional resources</span></span>

[<span data-ttu-id="b196c-134">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b196c-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b196c-135">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="b196c-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b196c-136">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="b196c-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b196c-137">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="b196c-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b196c-138">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="b196c-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b196c-139">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="b196c-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b196c-140">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="b196c-140">Enrich a category landing page</span></span>](enrich-category-page.md)
