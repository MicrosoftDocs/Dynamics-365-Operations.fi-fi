---
title: Sivun tallentaminen, esikatseleminen ja julkaiseminen
description: Tässä ohjeaiheessa kerrotaan, miten sivu tallennetaan, miten sitä esikatsellaan ja miten se julkaistaan Microsoft Dynamics 365 Commerce -sovelluksessa.
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
ms.openlocfilehash: db4866b22060b764fdde3e4a44e99e969133c0a0
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961607"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="48e7e-103">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48e7e-104">Tässä ohjeaiheessa kerrotaan, miten sivu tallennetaan, miten sitä esikatsellaan ja miten se julkaistaan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="48e7e-105">Sivun tallentaminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-105">Save a page</span></span>

<span data-ttu-id="48e7e-106">Jos haluat tallentaa sivun, se on kuitattava ulos käyttäjälle ja avattava sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="48e7e-107">Kuittaa tiedosto ulos valitsemalla komentopalkissa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-107">To check out a page, select **Edit** on the command bar.</span></span> <span data-ttu-id="48e7e-108">Kun olet muokannut sivua, sinun tulee tallentaa se välittömästi, että tekemäsi muutokset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="48e7e-108">After you've finished editing a page, you should immediately save it to ensure that your changes are stored.</span></span>

<span data-ttu-id="48e7e-109">Kun tallennat sivun, muutokset näkyvät vain sinulle.</span><span class="sxs-lookup"><span data-stu-id="48e7e-109">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="48e7e-110">Tallennustoiminto on tarkoitettu ensisijaisesti muutosten tallentamista varten silloin, kun sivu ei ole vielä valmis kuitattavaksi sisään.</span><span class="sxs-lookup"><span data-stu-id="48e7e-110">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="48e7e-111">Kun sivun muokkaaminen on tehty, se kannattaa kirjata sisään. Tällöin muutokset näkyvät myös muille.</span><span class="sxs-lookup"><span data-stu-id="48e7e-111">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="48e7e-112">Tässä vaiheessa myös muut käyttäjät voivat kirjata sivun ulos, jos heidän on muokattava sitä.</span><span class="sxs-lookup"><span data-stu-id="48e7e-112">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="48e7e-113">Sivun esikatseleminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-113">Preview a page</span></span>

<span data-ttu-id="48e7e-114">Muokkaustyökalussa on seuraavat kaksi esikatselutoimintoa: visuaalinen sivustonmuodostin, joka on WYSIWYG-esikatseluruutu sivueditorissa, ja erillinen esikatseluikkuna.</span><span class="sxs-lookup"><span data-stu-id="48e7e-114">The authoring tool offers two kinds of preview features: visual page builder, which is a "what you see is what you get" (WYSIWYG) preview pane in the page editor, and a separate preview window.</span></span>

<span data-ttu-id="48e7e-115">Kun käytät sivueditoria, keskiruudussa näkyy WYSIWYG-esikatselu.</span><span class="sxs-lookup"><span data-stu-id="48e7e-115">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="48e7e-116">Tämä esikatselu päivitetään automaattisesti aina sivun tallentamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="48e7e-116">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="48e7e-117">Voit päivittää sen myös manuaalisesti valitsemalla komentopalkissa **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-117">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="48e7e-118">Esikatselu hahmontaa sivun samanlaiseksi kuin käyttäjän näkymä. Sen päällä näkyvät kuitenkin muokkausavustajat.</span><span class="sxs-lookup"><span data-stu-id="48e7e-118">The preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="48e7e-119">Kun sivun muokkaaminen on tehty, haluat ehkä esikatsella sen ja nähdä, millaiselta se näyttää asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="48e7e-119">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="48e7e-120">Voit esikatsella sivua valitsemalla komentopalkissa **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-120">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="48e7e-121">Esikatselu näkyy erillisessä selainikkunassa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-121">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="48e7e-122">Esikatseluikkunan sivu hahmonnetaan sellaiseksi, jona käyttäjä näkee sen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-122">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="48e7e-123">Voit muuttaa ikkunan kokoa ja varmistaa, että responsiiviset moduulit on hahmonnettu oikein kaikissa näkymäporteissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-123">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="48e7e-124">Julkaisemattoman sisällön esikatselu edellyttää todennuksen ja oikeat oikeudet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-124">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="48e7e-125">Jos siis jaat esikatselun URL-osoitteen jollekin henkilölle, tällä tulee olla oikeat oikeudet sisällön käyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="48e7e-125">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="48e7e-126">Sivun julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-126">Publish a page</span></span>

<span data-ttu-id="48e7e-127">Kun sivu on valmis, seuraava vaihe on julkaista se. Tämän jälkeen ulkoiset käyttäjät voivat tarkastella sisältöä.</span><span class="sxs-lookup"><span data-stu-id="48e7e-127">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="48e7e-128">Ennen kuin voit julkaista sivun, sinun on tarkistettava se valitsemalla komentopalkissa **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-128">Before you can publish a page, you must check it in by selecting **Finish editing** on the command bar.</span></span>

<span data-ttu-id="48e7e-129">Voit julkaista sivun ja peruuttaa sen julkaisun sivun tarkistusohjelmassa tai sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-129">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="48e7e-130">Sivun tarkistusohjelmassa on sivuluettelo. Se mahdollistaa joukkotoiminnot.</span><span class="sxs-lookup"><span data-stu-id="48e7e-130">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="48e7e-131">Sivueditoria voi käyttää vain yhden sellaisen sivun julkaisemisessa tai sivun julkaisun peruuttamisessa, joka on auki editorissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-131">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="48e7e-132">Jos haluat julkaista yhden tai useita sivuja sivun tarkistusohjelmassa, valitse sivut, varmista, että ne on kirjattu sisään ja valitse sitten **Julkaise** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-132">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="48e7e-133">Sivut julkaistaan. Saat ilmoituksen muokkaustyökalun toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="48e7e-133">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="48e7e-134">Jos haluat julkaista yhden sivun sivueditorissa, tee samat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="48e7e-134">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="48e7e-135">Kun sivu on avoinna sivueditorissa, varmista, että se on kuitattu sisään, ja valitse sitten **Julkaise** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-135">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="48e7e-136">Sivu julkaistaan. Saat ilmoituksen muokkaustyökalun toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="48e7e-136">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="48e7e-137">Kun julkaiset sivun, vain sivun sisältö julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="48e7e-137">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="48e7e-138">Käyttäjät voivat siirtyä sivulle ja tarkastella sitä vasta sen jälkeen, kun siihen on liitetty URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="48e7e-138">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="48e7e-139">URL-osoite on julkaistava erikseen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-139">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48e7e-140">Ennen kuin voit julkaista sivun, kaikkien kuvien ja osien, joihin sivu viittaa, on jo oltava julkaistu.</span><span class="sxs-lookup"><span data-stu-id="48e7e-140">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="48e7e-141">Aloitussivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-141">Save, preview, and publish a home page</span></span>

<span data-ttu-id="48e7e-142">Voit tallentaa, esikatsella ja julkaista aloitussivun noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="48e7e-142">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="48e7e-143">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="48e7e-143">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="48e7e-144">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-144">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="48e7e-145">Etsi ja valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="48e7e-145">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="48e7e-146">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-146">Select **Edit**.</span></span>
1. <span data-ttu-id="48e7e-147">Muokkaa sivua tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="48e7e-147">Modify the page as you require.</span></span>
1. <span data-ttu-id="48e7e-148">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-148">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="48e7e-149">Kirjoita **Kommentit**-kenttään tekemäsi muutosten huomautukset ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-149">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="48e7e-150">Esikatsele sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-150">Select **Preview** to preview your page.</span></span> <span data-ttu-id="48e7e-151">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="48e7e-151">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="48e7e-152">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-152">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="48e7e-153">URL-osoitteen julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-153">Publish a URL</span></span>

<span data-ttu-id="48e7e-154">Julkaise URL-osoite seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="48e7e-154">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="48e7e-155">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="48e7e-155">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="48e7e-156">Valitse vasemmanpuoleisessa siirtymisruudussa **URL-osoitteet**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-156">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="48e7e-157">Etsi ja valitse julkaistava URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="48e7e-157">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="48e7e-158">Valitse komentopalkissa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-158">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48e7e-159">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="48e7e-159">Additional resources</span></span>

[<span data-ttu-id="48e7e-160">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-160">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="48e7e-161">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-161">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="48e7e-162">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-162">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="48e7e-163">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="48e7e-163">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="48e7e-164">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-164">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="48e7e-165">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-165">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="48e7e-166">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="48e7e-166">Verify page content accessibility</span></span>](verify-accessibility.md)
