---
title: Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi
description: Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797428"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="b3785-103">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="b3785-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3785-104">Tässä ohjeaiheessa kerrotaan, miten asiakaspuolen komentosarjakoodi lisätään sivustosivuille tukemaan asiakaspuolen telemetriatietojen keräämistä.</span><span class="sxs-lookup"><span data-stu-id="b3785-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="b3785-105">Web Analytics on tärkeä työkalu, kun halutaan ymmärtää, miten asiakkaat käyttävät sivustoa ja miten he tekevät päätöksiä. Tämä mahdollistaa muuntokokemuksen optimoinnin ja muunnon maksimoinnin.</span><span class="sxs-lookup"><span data-stu-id="b3785-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="b3785-106">Käytettävissä on useita Web Analytics -paketteja, joiden avulla tavoitteet voidaan saavuttaa. Paketteja ovat esimerkiksi Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="b3785-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="b3785-107">Useimmat Web Analytics -paketit edellyttävät, että lisäät asiakaspuolen komentosarjakoodin HTML:n **\<head\>**-elementtiin kaikille sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="b3785-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="b3785-108">Tämän ohjeaiheen ohjeet koskevat myös muita mukautettuja asiakaspuolen toimintoja, joita Microsoft Dynamics 365 Commerce ei tarjoa suoraan.</span><span class="sxs-lookup"><span data-stu-id="b3785-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="b3785-109">Uudelleenkäytettävän osan luominen komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="b3785-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="b3785-110">Osan avulla voit käyttää uudelleen sisäistä tai ulkoista komentosarjakoodia kaikilla sivuston sivuilla käytettävästä mallista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="b3785-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="b3785-111">Uudelleenkäytettävän osan luominen sisäistä komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="b3785-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="b3785-112">Voit luoda uudelleenkäytettävän osan sisäistä komentosarjakoodia varten sivuston luontiohjelmassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b3785-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b3785-113">Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b3785-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="b3785-114">Valitse **Uusi osa** -valintaikkunassa **Sisäinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="b3785-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="b3785-115">Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3785-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b3785-116">Valitse luomasi osan **Oletusarvoinen sisäinen komentosarja** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="b3785-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="b3785-117">Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi.</span><span class="sxs-lookup"><span data-stu-id="b3785-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="b3785-118">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b3785-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b3785-119">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="b3785-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b3785-120">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b3785-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="b3785-121">Uudelleenkäytettävän osan luominen ulkoista komentosarjakoodia varten</span><span class="sxs-lookup"><span data-stu-id="b3785-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="b3785-122">Voit luoda uudelleenkäytettävän osan ulkoista komentosarjakoodia varten sivuston luontiohjelmassa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b3785-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b3785-123">Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b3785-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="b3785-124">Valitse **Uusi osa** -valintaikkunassa **Ulkoinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="b3785-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="b3785-125">Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3785-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b3785-126">Valitse luomasi osan **Oletusarvoinen ulkoinen komentosarja** -moduuli.</span><span class="sxs-lookup"><span data-stu-id="b3785-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="b3785-127">Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun.</span><span class="sxs-lookup"><span data-stu-id="b3785-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="b3785-128">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b3785-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b3785-129">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="b3785-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b3785-130">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b3785-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="b3785-131">Jos sisällön suojauskäytäntö (CSP) on otettu sivustossa käyttöön, varmista, että ulkoiset URL-osoitteet on lisätty **script-src**-CSP-direktiiviin Commercen sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="b3785-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="b3785-132">Lisätietoja on kohdassa [Sisällön suojauskäytännön hallinta](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="b3785-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="b3785-133">Komentosarjakoodia sisältävän osan lisääminen malliin</span><span class="sxs-lookup"><span data-stu-id="b3785-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="b3785-134">Voit lisätä osan, joka sisältää komentosarjan koodin malliin sivuston luontiohjelmassa noudattamalla näitä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="b3785-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b3785-135">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="b3785-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b3785-136">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="b3785-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b3785-137">Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="b3785-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="b3785-138">Valitse komentosarjakoodille luomasi osa.</span><span class="sxs-lookup"><span data-stu-id="b3785-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="b3785-139">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="b3785-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b3785-140">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b3785-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="b3785-141">Ulkoisen komentosarjan tai sisäisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="b3785-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="b3785-142">Jos haluat lisätä sisäisen tai ulkoisen komentosarjan suoraan yhden mallin hallitsemille sivuille, sinun ei tarvitse ensin luoda osaa.</span><span class="sxs-lookup"><span data-stu-id="b3785-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="b3785-143">Sisäisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="b3785-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="b3785-144">Voit lisätä sisäisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b3785-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b3785-145">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="b3785-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b3785-146">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="b3785-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b3785-147">Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="b3785-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b3785-148">Valitse **Lisää moduuli** -valintaikkunassa **Sisäinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="b3785-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="b3785-149">Kirjoita oikealla olevan ominaisuusruudun **Sisäinen komentosarja** -kohtaan asiakaspuolen komentosarjasi.</span><span class="sxs-lookup"><span data-stu-id="b3785-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="b3785-150">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b3785-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b3785-151">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="b3785-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b3785-152">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b3785-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="b3785-153">Ulkoisen komentosarjan lisääminen suoraan malliin</span><span class="sxs-lookup"><span data-stu-id="b3785-153">Add an external script directly to a template</span></span>

<span data-ttu-id="b3785-154">Voit lisätä ulkoisen komentosarjan suoraan sivustonmuodostimen malliin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b3785-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b3785-155">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä komentosarjakoodin.</span><span class="sxs-lookup"><span data-stu-id="b3785-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b3785-156">Laajenna vasemmanpuoleisessa ruudussa mallihierarkia, jolloin **HTML:n pääpaikka** tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="b3785-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b3785-157">Valitse kolmen pisteen painike (**...**) **HTML:n pääpaikassa** ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="b3785-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b3785-158">Valitse **Lisää moduuli** -valintaikkunassa **Ulkoinen komentosarja**.</span><span class="sxs-lookup"><span data-stu-id="b3785-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="b3785-159">Lisää ulkoisen komentosarjalähteen ulkoinen tai suhteellinen URL-osoite **Komentosarjan lähde** -kohdan oikealla puolella olevaan ominaisuusruutuun.</span><span class="sxs-lookup"><span data-stu-id="b3785-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="b3785-160">Määritä sitten muut asetukset tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b3785-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b3785-161">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="b3785-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b3785-162">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b3785-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3785-163">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b3785-163">Additional resources</span></span>

[<span data-ttu-id="b3785-164">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="b3785-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b3785-165">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="b3785-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b3785-166">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="b3785-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b3785-167">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b3785-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b3785-168">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="b3785-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b3785-169">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b3785-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b3785-170">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="b3785-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
