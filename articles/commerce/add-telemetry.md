---
title: Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi
description: Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411914"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="03597-103">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="03597-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03597-104">Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.</span><span class="sxs-lookup"><span data-stu-id="03597-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="03597-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="03597-105">Overview</span></span>

<span data-ttu-id="03597-106">Web Analytics on tärkeä työkalu, kun halutaan ymmärtää, miten asiakkaat käyttävät sivustoa ja miten he tekevät päätöksiä. Tämä mahdollistaa muuntokokemuksen optimoinnin ja muunnon maksimoinnin.</span><span class="sxs-lookup"><span data-stu-id="03597-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="03597-107">Käytettävissä on useita Web Analytics -paketteja, joiden avulla tavoitteet voidaan saavuttaa. Paketteja ovat esimerkiksi Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="03597-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="03597-108">Useimmat Web Analytics -paketit edellyttävät, että lisäät asiakaspuolen komentosarjakoodin HTML:n **\<head\>**-elementtiin kaikille sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="03597-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="03597-109">Tämän ohjeaiheen ohjeet koskevat myös muita mukautettuja asiakaspuolen toimintoja, joita Microsoft Dynamics 365 Commerce ei tarjoa suoraan.</span><span class="sxs-lookup"><span data-stu-id="03597-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="03597-110">Uudelleenkäytettävän osan luominen komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="03597-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="03597-111">Osan avulla voit käyttää uudelleen sisäistä tai ulkoista komentosarjakoodia kaikilla sivuston sivuilla käytettävästä mallista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="03597-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="03597-112">Uudelleenkäytettävän osan luominen sisäistä komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="03597-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="03597-113">Voit luoda uudelleenkäytettävän osan sisäistä komentosarjakoodia varten sivuston luontiohjelmassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="03597-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="03597-114">Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="03597-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="03597-115">Valitse **Uusi osa** -valintaikkunassa **Sisäinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="03597-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="03597-116">Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="03597-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="03597-117">Valitse luomasi osan **Oletusarvoinen sisäinen komentosarja** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="03597-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="03597-118">Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi.</span><span class="sxs-lookup"><span data-stu-id="03597-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="03597-119">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="03597-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="03597-120">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="03597-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="03597-121">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="03597-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="03597-122">Uudelleenkäytettävän osan luominen ulkoista komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="03597-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="03597-123">Voit luoda uudelleenkäytettävän osan ulkoista komentosarjakoodia varten sivuston luontiohjelmassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="03597-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="03597-124">Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="03597-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="03597-125">Valitse **Uusi osa** -valintaikkunassa **Ulkoinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="03597-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="03597-126">Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="03597-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="03597-127">Valitse luomasi osan **Oletusarvoinen ulkoinen komentosarja** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="03597-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="03597-128">Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun.</span><span class="sxs-lookup"><span data-stu-id="03597-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="03597-129">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="03597-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="03597-130">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="03597-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="03597-131">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="03597-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="03597-132">Jos sisällön suojauskäytäntö (CSP) on otettu sivustossa käyttöön, varmista, että ulkoiset URL-osoitteet on lisätty **script-src**-CSP-direktiiviin Commercen sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="03597-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="03597-133">Lisätietoja on kohdassa [Sisällön suojauskäytännön hallinta](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="03597-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="03597-134">Komentosarjakoodia sisältävän osan lisääminen malliin</span><span class="sxs-lookup"><span data-stu-id="03597-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="03597-135">Voit lisätä osan, joka sisältää komentosarjan koodin malliin sivuston luontiohjelmassa noudattamalla näitä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="03597-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="03597-136">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="03597-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="03597-137">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="03597-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="03597-138">Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="03597-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="03597-139">Valitse komentosarjakoodille luomasi osa.</span><span class="sxs-lookup"><span data-stu-id="03597-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="03597-140">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="03597-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="03597-141">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="03597-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="03597-142">Ulkoisen komentosarjan tai sisäisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="03597-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="03597-143">Jos haluat lisätä sisäisen tai ulkoisen komentosarjan suoraan yhden mallin hallitsemille sivuille, sinun ei tarvitse ensin luoda osaa.</span><span class="sxs-lookup"><span data-stu-id="03597-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="03597-144">Sisäisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="03597-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="03597-145">Voit lisätä sisäisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="03597-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="03597-146">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="03597-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="03597-147">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="03597-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="03597-148">Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="03597-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="03597-149">Valitse **Lisää moduuli** -valintaikkunassa **Sisäinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="03597-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="03597-150">Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi.</span><span class="sxs-lookup"><span data-stu-id="03597-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="03597-151">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="03597-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="03597-152">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="03597-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="03597-153">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="03597-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="03597-154">Ulkoisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="03597-154">Add an external script directly to a template</span></span>

<span data-ttu-id="03597-155">Voit lisätä ulkoisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="03597-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="03597-156">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="03597-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="03597-157">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="03597-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="03597-158">Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="03597-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="03597-159">Valitse **Lisää moduuli** -valintaikkunassa **Ulkoinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="03597-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="03597-160">Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun.</span><span class="sxs-lookup"><span data-stu-id="03597-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="03597-161">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="03597-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="03597-162">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="03597-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="03597-163">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="03597-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03597-164">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="03597-164">Additional resources</span></span>

[<span data-ttu-id="03597-165">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="03597-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="03597-166">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="03597-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="03597-167">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="03597-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="03597-168">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="03597-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="03597-169">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="03597-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="03597-170">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="03597-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="03597-171">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="03597-171">Add languages to your site</span></span>](add-languages-to-site.md)
