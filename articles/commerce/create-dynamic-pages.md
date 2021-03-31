---
title: Dynaamisten sähköisen kaupankäynnin sivujen luominen URL-parametrien perusteella
description: Tässä aiheessa kuvataan, kuinka määritetään Microsoft Dynamics 365 Commerce -verkkokauppasivu, joka voi tuottaa URL-parametreihin perustuvaa dynaamista sisältöä.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d6b4756fc81dc99786da251d5d9a575a71ccc49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208012"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="ae7a3-103">Dynaamisten sähköisen kaupankäynnin sivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="ae7a3-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ae7a3-104">Tässä aiheessa kuvataan, kuinka määritetään Microsoft Dynamics 365 Commerce -verkkokauppasivu, joka voi tuottaa URL-parametreihin perustuvaa dynaamista sisältöä.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="ae7a3-105">Sähköisen kaupankäyntisivun voi konfiguroida käyttämään erilaista sisältöä URL-polun segmentin perusteella.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="ae7a3-106">Näin ollen sivu tunnetaan dynaamisena sivuna.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="ae7a3-107">Segmenttiä käytetään sivun sisällön noutamisen parametrina.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="ae7a3-108">Voit luoda esimerkiksi sivun, jonka nimi on **blog\_viewer**, ja se liitetään URL-osoitteeseen `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="ae7a3-109">Tämän sivun avulla voidaan sitten näyttää eri sisältöä URL-polun viimeisen segmentin perusteella.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="ae7a3-110">Esimerkiksi URL-osoitteen `https://fabrikam.com/blog/article-1` viimeinen segmentti on **article-1**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="ae7a3-111">Erilliset dynaamisen sivun ohittavat mukautetut sivut voidaan liittää myös URL-polun segmentteihin.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="ae7a3-112">Voit luoda esimerkiksi sivun, jonka nimi on **blog\_summary**, ja se liitetään URL-osoitteeseen `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="ae7a3-113">Kun tämä URL-osoite on pyydetty, palautetaan **blog\_summary** -sivu, joka liittyy **/about-this-blog** -parametriin, sen sijaan että palautettaisiin **blog\_viewer** -sivu.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="ae7a3-114">Dynaamisen sivusisällön isännöinti-, noutaminen- ja näyttämistoiminnot toteutetaan mukautetulla moduulilla.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="ae7a3-115">Lisätietoja on ohjeaiheessa [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae7a3-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="ae7a3-116">Dynaamisen verkkokauppasivun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="ae7a3-117">Voit määrittää dynaamisen sähköisen kaupankäynnin sivun luomalla dynaamisen sivun, luomalla perus-URL-osoitteen ja määrittämällä reitityksen dynaamiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="ae7a3-118">Dynaamista sisältöä tarjoavan sivun luominen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="ae7a3-119">Voit luoda dynaamista sisältöä tuottavan sivun noudattamalla ohjeita: [Uuden sivuston sivun lisääminen](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="ae7a3-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="ae7a3-120">Luotava sivu edellyttää, että käytössä on moduuli, joka käyttää URL-polun viimeistä segmenttiä ulkoisen tietolähteen sisällön hakemiseen.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="ae7a3-121">Lisätietoja mukautetusta moduulien kehittämisestä on kohdassa [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae7a3-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="ae7a3-122">Luo dynaamisen sivun perus-URL-osoite</span><span class="sxs-lookup"><span data-stu-id="ae7a3-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="ae7a3-123">Luo dynaamiselle sivulle perus-URL-osoite Commercen sivustonmuodostimessa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae7a3-124">Siirry kohtaan **URL-osoitteet** ja valitse **Uusi \> Uusi URL-osoite**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="ae7a3-125">Valitse **Luo uusi URL-osoite** -valintaikkunasta **Sisäinen sivu**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="ae7a3-126">Kirjoita **URL-polku**-kohdassa polku, jota käytetään dynaamisen sivun juuripolkuna (tässä esimerkissä **/blog**).</span><span class="sxs-lookup"><span data-stu-id="ae7a3-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="ae7a3-127">Valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-127">Then select **Next**.</span></span>
1. <span data-ttu-id="ae7a3-128">Valitse **Valitse sivu** -valintaikkunassa sivu, jonka loit aiemmin dynaamiseksi sivuksi ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="ae7a3-129">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="ae7a3-130">Reitityksen konfiguroiminen dynaamiselle sivulle</span><span class="sxs-lookup"><span data-stu-id="ae7a3-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="ae7a3-131">Määritä dynaamiselle sivulle reititys Commercen sivustonmuodostimessa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae7a3-132">Siirry kohtaan **Sivuston asetukset \> Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="ae7a3-133">Valitse kohdassa **Parametrisoidut URL-polut** **Lisää** ja kirjoita sitten URL-osoitteen luomisen yhteydessä syötetty URL-polku (tässä esimerkissä **/blog**).</span><span class="sxs-lookup"><span data-stu-id="ae7a3-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="ae7a3-134">Valitse **Tallenna ja julkaise**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-134">Select **Save and publish**.</span></span>

<span data-ttu-id="ae7a3-135">Kun reititys on konfiguroitu, kaikki parametrisoidun URL-polun pyynnöt palauttavat tähän URL-osoitteeseen liittyvän sivun.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="ae7a3-136">Jos pyynnöt sisältävät lisäsegmentin, siihen liittyvä sivu palautetaan ja sivun sisältö haetaan käyttämällä segmenttiä parametrina.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="ae7a3-137">Esimerkiksi `https://fabrikam.com/blog/article-1` palauttaa esimerkiksi **blog\_summary** -sivun ja sivun sisältö haetaan käyttämällä **/article-1**-parametria.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="ae7a3-138">Parametriswoidun URL-osoitteen ohittaminen mukautetulla sivulla</span><span class="sxs-lookup"><span data-stu-id="ae7a3-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="ae7a3-139">Noudattamalla seuraavia ohjeita voit ohittaa parametrisoidun URL-osoitteen mukautetulla sivulla Commercen sivustonmuodostimen avulla.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae7a3-140">Siirry kohtaan **URL-osoitteet** ja valitse **Uusi \> Uusi URL-osoite**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="ae7a3-141">Valitse **Luo uusi URL-osoite** -valintaikkunasta **Sisäinen sivu**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="ae7a3-142">Kirjoita **URL-polku**-kohdassa polku, joka sisältää ohitettavan segmentin (tässä esimerkissä **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="ae7a3-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="ae7a3-143">Valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-143">Then select **Next**.</span></span>
1. <span data-ttu-id="ae7a3-144">Valitse mukautettu sivu **Valitse sivu** -valintaikkunasta ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="ae7a3-145">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-145">Select **Publish**.</span></span>
1. <span data-ttu-id="ae7a3-146">Jos mukautettua sivua ei ole vielä julkaisuttu, siirry kohtaan **Sivut**, valitse mukautettu sivu ja valitse sitten **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="ae7a3-147">Kun mukautettu sivu on julkaistu, se tarjotaan sen sijaan, että tarjottaisiin dynaaminen sivu, jolla on parametrisoitua sisältöä.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae7a3-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ae7a3-148">Additional resources</span></span>

[<span data-ttu-id="ae7a3-149">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="ae7a3-150">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ae7a3-151">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ae7a3-152">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="ae7a3-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="ae7a3-153">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ae7a3-154">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="ae7a3-155">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="ae7a3-156">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="ae7a3-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="ae7a3-157">Online-kanavan laajennettavuus</span><span class="sxs-lookup"><span data-stu-id="ae7a3-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]