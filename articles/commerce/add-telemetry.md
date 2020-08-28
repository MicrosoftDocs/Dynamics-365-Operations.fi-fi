---
title: Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi
description: Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686811"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="22a0d-103">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="22a0d-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22a0d-104">Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.</span><span class="sxs-lookup"><span data-stu-id="22a0d-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="22a0d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="22a0d-105">Overview</span></span>

<span data-ttu-id="22a0d-106">Web Analytics on tärkeä työkalu, kun halutaan ymmärtää, miten asiakkaat käyttävät sivustoa ja miten he tekevät päätöksiä. Tämä mahdollistaa muuntokokemuksen optimoinnin ja muunnon maksimoinnin.</span><span class="sxs-lookup"><span data-stu-id="22a0d-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="22a0d-107">Käytettävissä on useita Web Analytics -paketteja, joiden avulla tavoitteet voidaan saavuttaa. Paketteja ovat esimerkiksi Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="22a0d-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="22a0d-108">Useimmat Web Analytics -paketit edellyttävät, että lisäät asiakaspuolen komentosarjakoodin HTML:n **\<head\>**-elementtiin kaikille sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="22a0d-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="22a0d-109">Tämän ohjeaiheen ohjeet koskevat myös muita mukautettuja asiakaspuolen toimintoja, joita Microsoft Dynamics 365 Commerce ei tarjoa suoraan.</span><span class="sxs-lookup"><span data-stu-id="22a0d-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="22a0d-110">Uudelleenkäytettävän sivun luominen komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="22a0d-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="22a0d-111">Sivun osan avulla voit käyttää uudelleen sisäistä tai ulkoista komentosarjakoodia kaikilla sivuston sivuilla riippumatta siitä, mitä mallia ne käyttävät.</span><span class="sxs-lookup"><span data-stu-id="22a0d-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="22a0d-112">Uudelleenkäytettävän sivun luominen sisäistä komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="22a0d-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="22a0d-113">Voit luoda uudelleenkäytettävän sivun osan sisäistä komentosarjakoodia varten sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="22a0d-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="22a0d-114">Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="22a0d-115">Valitse **Uusi sivun osa** -valintaikkunassa **Sisäinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="22a0d-116">Kirjoita **Sivun osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="22a0d-117">Valitse luomasi sivun osan **Oletusarvoinen sisäinen komentosarja** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="22a0d-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="22a0d-118">Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi.</span><span class="sxs-lookup"><span data-stu-id="22a0d-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="22a0d-119">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="22a0d-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="22a0d-120">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="22a0d-121">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="22a0d-122">Uudelleenkäytettävän sivun luominen ulkoista komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="22a0d-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="22a0d-123">Voit luoda uudelleenkäytettävän sivun osan ulkoista komentosarjakoodia varten sivustonmuodostimessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="22a0d-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="22a0d-124">Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="22a0d-125">Valitse **Uusi sivun osa** -valintaikkunassa **Ulkoinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="22a0d-126">Kirjoita **Sivun osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="22a0d-127">Valitse luomasi sivun osan **Oletusarvoinen ulkoinen komentosarja** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="22a0d-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="22a0d-128">Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun.</span><span class="sxs-lookup"><span data-stu-id="22a0d-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="22a0d-129">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="22a0d-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="22a0d-130">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="22a0d-131">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="22a0d-132">Komentosarjakoodia sisältävän sivun osan lisääminen malliin</span><span class="sxs-lookup"><span data-stu-id="22a0d-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="22a0d-133">Voit lisätä sivun osan, joka sisältää komentosarjan koodin malliin sivustonmuodostimessa noudattamalla näitä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="22a0d-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="22a0d-134">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="22a0d-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="22a0d-135">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML Head** -paikka.</span><span class="sxs-lookup"><span data-stu-id="22a0d-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="22a0d-136">Valitse kolmen pisteen painike (**...**) **HTML Head** -paikassa ja valitse sitten **Lisää sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="22a0d-137">Valitse komentosarjakoodille luomasi osa.</span><span class="sxs-lookup"><span data-stu-id="22a0d-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="22a0d-138">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="22a0d-139">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="22a0d-140">Ulkoisen komentosarjan tai sisäisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="22a0d-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="22a0d-141">Jos haluat lisätä sisäisen tai ulkoisen komentosarjan suoraan yhden mallin hallitsemille sivuille, sinun ei tarvitse ensin luoda sivun osaa.</span><span class="sxs-lookup"><span data-stu-id="22a0d-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="22a0d-142">Sisäisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="22a0d-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="22a0d-143">Voit lisätä sisäisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="22a0d-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="22a0d-144">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="22a0d-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="22a0d-145">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML Head** -paikka.</span><span class="sxs-lookup"><span data-stu-id="22a0d-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="22a0d-146">Valitse kolmen pisteen painike (**...**) **HTML Head** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="22a0d-147">Valitse **Lisää moduuli** -valintaikkunassa **Sisäinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="22a0d-148">Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi.</span><span class="sxs-lookup"><span data-stu-id="22a0d-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="22a0d-149">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="22a0d-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="22a0d-150">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="22a0d-151">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="22a0d-152">Ulkoisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="22a0d-152">Add an external script directly to a template</span></span>

<span data-ttu-id="22a0d-153">Voit lisätä ulkoisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="22a0d-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="22a0d-154">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="22a0d-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="22a0d-155">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML Head** -paikka.</span><span class="sxs-lookup"><span data-stu-id="22a0d-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="22a0d-156">Valitse kolmen pisteen painike (**...**) **HTML Head** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="22a0d-157">Valitse **Lisää moduuli** -valintaikkunassa **Ulkoinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="22a0d-158">Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun.</span><span class="sxs-lookup"><span data-stu-id="22a0d-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="22a0d-159">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="22a0d-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="22a0d-160">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="22a0d-161">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="22a0d-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22a0d-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="22a0d-162">Additional resources</span></span>

[<span data-ttu-id="22a0d-163">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="22a0d-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="22a0d-164">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="22a0d-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="22a0d-165">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="22a0d-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="22a0d-166">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="22a0d-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="22a0d-167">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="22a0d-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="22a0d-168">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="22a0d-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="22a0d-169">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="22a0d-169">Add languages to your site</span></span>](add-languages-to-site.md)
