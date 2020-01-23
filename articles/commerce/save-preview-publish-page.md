---
title: Sivun tallentaminen, esikatseleminen ja julkaiseminen
description: Tässä ohjeaiheessa kerrotaan, miten sivu tallennetaan, miten sitä esikatsellaan ja miten se julkaistaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 3fff8299ecc6833890b14fa421501236830b2c61
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945671"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="e93fb-103">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e93fb-104">Tässä ohjeaiheessa kerrotaan, miten sivu tallennetaan, miten sitä esikatsellaan ja miten se julkaistaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="e93fb-105">Sivun tallentaminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-105">Save a page</span></span>

<span data-ttu-id="e93fb-106">Jos haluat tallentaa sivun, se on kuitattava ulos käyttäjälle ja avattava sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="e93fb-107">Tallenna sivu heti muokkaamisen jälkeen, jotta voit varmistaa, että tekemäsi muutokset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="e93fb-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="e93fb-108">Kun tallennat sivun, muutokset näkyvät vain sinulle.</span><span class="sxs-lookup"><span data-stu-id="e93fb-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="e93fb-109">Tallennustoiminto on tarkoitettu ensisijaisesti muutosten tallentamista varten silloin, kun sivu ei ole vielä valmis kuitattavaksi sisään.</span><span class="sxs-lookup"><span data-stu-id="e93fb-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="e93fb-110">Kun sivun muokkaaminen on tehty, se kannattaa kirjata sisään. Tällöin muutokset näkyvät myös muille.</span><span class="sxs-lookup"><span data-stu-id="e93fb-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="e93fb-111">Tässä vaiheessa myös muut käyttäjät voivat kirjata sivun ulos, jos heidän on muokattava sitä.</span><span class="sxs-lookup"><span data-stu-id="e93fb-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="e93fb-112">Sivun esikatseleminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-112">Preview a page</span></span>

<span data-ttu-id="e93fb-113">Muokkaustyökalussa on seuraavat kaksi erilaista esikatselutoimintoa: WYSIWYG (what you see is what you get) -esikatseluruutu sivueditorissa ja erillinen esikatseluikkuna.</span><span class="sxs-lookup"><span data-stu-id="e93fb-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="e93fb-114">Kun käytät sivueditoria, keskiruudussa näkyy WYSIWYG-esikatselu.</span><span class="sxs-lookup"><span data-stu-id="e93fb-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="e93fb-115">Tämä esikatselu päivitetään automaattisesti aina sivun tallentamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e93fb-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="e93fb-116">Voit päivittää sen myös manuaalisesti valitsemalla komentopalkissa **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="e93fb-117">WYSIWYG-esikatselu hahmontaa sivun samanlaiseksi kuin käyttäjän näkymä. Sen päällä näkyvät kuitenkin muokkausavustajat.</span><span class="sxs-lookup"><span data-stu-id="e93fb-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="e93fb-118">Kun sivun muokkaaminen on tehty, haluat ehkä esikatsella sen ja nähdä, millaiselta se näyttää asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="e93fb-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="e93fb-119">Voit esikatsella sivua valitsemalla komentopalkissa **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="e93fb-120">Esikatselu näkyy erillisessä selainikkunassa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="e93fb-121">Esikatseluikkunan sivu hahmonnetaan sellaiseksi, jona käyttäjä näkee sen.</span><span class="sxs-lookup"><span data-stu-id="e93fb-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="e93fb-122">Voit muuttaa ikkunan kokoa ja varmistaa, että responsiiviset moduulit on hahmonnettu oikein kaikissa näkymäporteissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="e93fb-123">Julkaisemattoman sisällön esikatselu edellyttää todennuksen ja oikeat oikeudet.</span><span class="sxs-lookup"><span data-stu-id="e93fb-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="e93fb-124">Jos siis jaat esikatselun URL-osoitteen jollekin henkilölle, tällä tulee olla oikeat oikeudet sisällön käyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e93fb-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="e93fb-125">Sivun julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-125">Publish a page</span></span>

<span data-ttu-id="e93fb-126">Kun sivu on valmis, seuraava vaihe on julkaista se. Tämän jälkeen ulkoiset käyttäjät voivat tarkastella sisältöä.</span><span class="sxs-lookup"><span data-stu-id="e93fb-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="e93fb-127">Ennen kuin voit julkaista sivun, se on kirjattava sisään.</span><span class="sxs-lookup"><span data-stu-id="e93fb-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="e93fb-128">Voit julkaista sivun ja peruuttaa sen julkaisun sivun tarkistusohjelmassa tai sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="e93fb-129">Sivun tarkistusohjelmassa on sivuluettelo. Se mahdollistaa joukkotoiminnot.</span><span class="sxs-lookup"><span data-stu-id="e93fb-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="e93fb-130">Sivueditoria voi käyttää vain yhden sellaisen sivun julkaisemisessa tai sivun julkaisun peruuttamisessa, joka on auki editorissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="e93fb-131">Jos haluat julkaista yhden tai useita sivuja sivun tarkistusohjelmassa, valitse sivut, varmista, että ne on kirjattu sisään ja valitse sitten **Julkaise** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="e93fb-132">Sivut julkaistaan. Saat ilmoituksen muokkaustyökalun toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="e93fb-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="e93fb-133">Jos haluat julkaista yhden sivun sivueditorissa, tee samat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="e93fb-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="e93fb-134">Kun sivu on avoinna sivueditorissa, varmista, että se on kuitattu sisään, ja valitse sitten **Julkaise** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="e93fb-135">Sivu julkaistaan. Saat ilmoituksen muokkaustyökalun toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="e93fb-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="e93fb-136">Kun julkaiset sivun, vain sivun sisältö julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="e93fb-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="e93fb-137">Käyttäjät voivat siirtyä sivulle ja tarkastella sitä vasta sen jälkeen, kun siihen on liitetty URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="e93fb-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="e93fb-138">URL-osoite on julkaistava erikseen.</span><span class="sxs-lookup"><span data-stu-id="e93fb-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e93fb-139">Ennen kuin voit julkaista sivun, kaikkien kuvien ja osien, joihin sivu viittaa, on jo oltava julkaistu.</span><span class="sxs-lookup"><span data-stu-id="e93fb-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="e93fb-140">Aloitussivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="e93fb-141">Voit tallentaa, esikatsella ja julkaista aloitussivun noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e93fb-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="e93fb-142">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="e93fb-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e93fb-143">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="e93fb-144">Etsi ja valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="e93fb-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="e93fb-145">Valitse **Kirjaa ulos**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="e93fb-146">Muokkaa sivua tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e93fb-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="e93fb-147">Valitse ensin **Tallenna** ja sitten **Kirjaa sisään**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="e93fb-148">Kirjoita **Kommentit**-kenttään tekemäsi muutosten huomautukset ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="e93fb-149">Esikatsele sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="e93fb-150">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e93fb-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e93fb-151">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="e93fb-152">URL-osoitteen julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-152">Publish a URL</span></span>

<span data-ttu-id="e93fb-153">Julkaise URL-osoite seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e93fb-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="e93fb-154">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="e93fb-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e93fb-155">Valitse vasemmanpuoleisessa siirtymisruudussa **URL-osoitteet**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="e93fb-156">Etsi ja valitse julkaistava URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="e93fb-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="e93fb-157">Valitse komentopalkissa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e93fb-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e93fb-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e93fb-158">Additional resources</span></span>

[<span data-ttu-id="e93fb-159">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e93fb-160">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e93fb-161">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e93fb-162">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="e93fb-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e93fb-163">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e93fb-164">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-164">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e93fb-165">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e93fb-165">Verify page content accessibility</span></span>](verify-accessibility.md)
