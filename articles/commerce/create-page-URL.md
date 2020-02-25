---
title: Sivun URL-osoitteen luominen
description: Tässä ohjeaiheessa kerrotaan sivuston URL-osoitteiden luomisen peruskäsitteistä ja proseduureista.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 588cbedb077fab0663d3d62fc4a8b8ed915635b3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001918"
---
# <a name="create-a-page-url"></a><span data-ttu-id="419fe-103">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="419fe-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="419fe-104">Tässä ohjeaiheessa kerrotaan sivuston URL-osoitteiden luomisen peruskäsitteistä ja proseduureista.</span><span class="sxs-lookup"><span data-stu-id="419fe-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="419fe-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="419fe-105">Overview</span></span>

<span data-ttu-id="419fe-106">Täydellinen tai absoluuttinen URL-osoite, joka osoittaa sivuston tietyt osat sisältävälle sivulle.</span><span class="sxs-lookup"><span data-stu-id="419fe-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="419fe-107">Esimerkiksi URL-osoitteessa `https://www.contoso.com/en-us/contactus` on seuraavat osat:</span><span class="sxs-lookup"><span data-stu-id="419fe-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="419fe-108">`https://www.contoso.com` – HTTP-protokolla ja sivuston toimialue.</span><span class="sxs-lookup"><span data-stu-id="419fe-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="419fe-109">`/en-us` – Sivuston kielipolku.</span><span class="sxs-lookup"><span data-stu-id="419fe-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="419fe-110">`/contactus` – **Ota yhteyttä** -sivun relatiivinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="419fe-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="419fe-111">Suhteellinen URL-osoite tunnetaan myös nimellä URL-osoitteen *kuvaava osa*.</span><span class="sxs-lookup"><span data-stu-id="419fe-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="419fe-112">Voit määrittää sivuston toimialueen ja valinnaisen kielipolun sivuston määrittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="419fe-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="419fe-113">Voit lisätä sivustoon toimialueita ja kielipolkuja sivuston asetusten verkkokauppasivun avulla.</span><span class="sxs-lookup"><span data-stu-id="419fe-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="419fe-114">Sivun URL-osoitteen kuvaava osa on olemassa yksittäisenä entiteettinä sivuston muokkausympäristössä.</span><span class="sxs-lookup"><span data-stu-id="419fe-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="419fe-115">Sivun URL-osoite koostuu kahdesta osasta: nimi, joka edustaa URL-osoitteen kuvaavaa osaa ja sivun osoittimesta omassa sivustossa tai ulkoisessa sivustossa.</span><span class="sxs-lookup"><span data-stu-id="419fe-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="419fe-116">Sivun URL-osoite voidaan määrittää myös niin, että se välittää käyttäjän toiselle sivulle omassa sivustossa tai ulkoisessa sivustossa.</span><span class="sxs-lookup"><span data-stu-id="419fe-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="419fe-117">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="419fe-117">Create a page URL</span></span>

<span data-ttu-id="419fe-118">Sivun URL-osoitteita voi luoda kahdella seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="419fe-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="419fe-119">Automaattisesti sivun luomisen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="419fe-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="419fe-120">Manuaalisesti **URL-osoitteet**-sivulla</span><span class="sxs-lookup"><span data-stu-id="419fe-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="419fe-121">Sivun URL-osoitteen luominen sivun luomisen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="419fe-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="419fe-122">Jos annat nimen **URL-osoite**-kenttään uuden sivun luomisen yhteydessä, sivulle osoittava sivun URL-osoite luodaan automaattisesti **URL-osoitteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="419fe-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="419fe-123">Kun URL-osoite ja sivu, johon se osoittaa, on julkaistu, sivuston käyttäjät (asiakkaat) voivat käyttää URL-osoitteeseen liitettyä sivua.</span><span class="sxs-lookup"><span data-stu-id="419fe-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="419fe-124">Jos julkaiset URL-osoitteen ilman sen sivun julkaisemista, johon osoite osoittaa, sivuston käyttäjille näytetään 404-virhe, kun he yrittävät käyttää sivua.</span><span class="sxs-lookup"><span data-stu-id="419fe-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="419fe-125">Jos julkaiset sivun ilman sen URL-osoitteen julkaisemista, johon sivu osoittaa, sivua ei voi käyttää URL-osoitteen avulla.</span><span class="sxs-lookup"><span data-stu-id="419fe-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="419fe-126">Sivun URL-osoitteen manuaalinen luominen</span><span class="sxs-lookup"><span data-stu-id="419fe-126">Manually create a page URL</span></span>

<span data-ttu-id="419fe-127">Kun luotu uusia sivuja, sinun ei tarvitse määrittää tiettyä sivun URL-osoitetta.</span><span class="sxs-lookup"><span data-stu-id="419fe-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="419fe-128">Jos jätät URL-osoite-kentän tyhjäksi, sivu luodaan ilman linkkejä.</span><span class="sxs-lookup"><span data-stu-id="419fe-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="419fe-129">Tällöin asiakkaat eivät voi käyttää sivua vaikka se olisi julkaistu.</span><span class="sxs-lookup"><span data-stu-id="419fe-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="419fe-130">Jotta sivu olisi käytettävissä, sinun on luotava URL-osoite manuaalisesti ja linkitettävä se sivulle.</span><span class="sxs-lookup"><span data-stu-id="419fe-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="419fe-131">Voit luoda sivun URL-osoitteen manuaalisesti seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="419fe-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="419fe-132">Valitse **URL-osoitteet**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="419fe-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="419fe-133">Valitse sivuston sivu, joka liitetään URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="419fe-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="419fe-134">Kirjoita URL-osoitteen kuvaava osa ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="419fe-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="419fe-135">Tässä vaiheessa URL-osoite on luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="419fe-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="419fe-136">Se on julkaistava, ennen kuin sivuston käyttäjät voivat käyttää liittyvää sivua.</span><span class="sxs-lookup"><span data-stu-id="419fe-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="419fe-137">Sivun URL-osoitteen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="419fe-137">Update a page URL</span></span>

<span data-ttu-id="419fe-138">Voit päivittää sivun URL-osoitteen kohdesivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="419fe-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="419fe-139">Valitse **URL-osoitteet**-sivulla päivitettävä URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="419fe-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="419fe-140">Valitse oikeanpuoleisessa ominaisuusruudussa kohdesivun kentän vieressä oleva kolmen pisteen painike (**...**).</span><span class="sxs-lookup"><span data-stu-id="419fe-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="419fe-141">Valitse valintaikkunassa toinen sivu ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="419fe-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="419fe-142">Tallenna ja julkaise URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="419fe-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="419fe-143">Sivun URL-osoitteen uudelleenohjaus</span><span class="sxs-lookup"><span data-stu-id="419fe-143">Redirect a page URL</span></span>

<span data-ttu-id="419fe-144">Joskus asiakkaat on hyvä ohjata eri sivulle kuin sille, jonka URL-osoitteen he valitsevat.</span><span class="sxs-lookup"><span data-stu-id="419fe-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="419fe-145">Tällöin paras ja helpoin tapa on usein muuttaa sivua, johon sivun URL-osoite osoittaa.</span><span class="sxs-lookup"><span data-stu-id="419fe-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="419fe-146">Voit kuitenkin perustellusti käyttää HTTP 301- tai 3023-uudelleenohjauksia ja ohjata URL-osoitteen pyynnöt toiseen URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="419fe-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="419fe-147">Voit ohjata URL-osoitteen toiseen URL-osoitteeseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="419fe-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="419fe-148">Valitse **URL-osoitteet**-sivulla päivitettävä URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="419fe-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="419fe-149">Valitse oikealla olevassa ominaisuusruudussa **Ohjaa uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="419fe-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="419fe-150">Valitse uudelleenohjauksen kohde seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="419fe-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="419fe-151">Jos haluat osoittaa sivuston toiseen sivuun, valitse **Sisäinen URL-osoite**. Valitse kolmen pisteen painike (**...**) ja valitse sitten uudelleenohjattava URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="419fe-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="419fe-152">Voit osoittaa ulkoisen sivuston sivuun valitsemalla **Ulkoinen URL-osoite** ja syöttämällä kyseisen sivun täydellisen URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="419fe-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="419fe-153">Varmista, että sisällytät protokollan.</span><span class="sxs-lookup"><span data-stu-id="419fe-153">Be sure to include the protocol.</span></span> <span data-ttu-id="419fe-154">Syötä arvoksi esimerkiksi `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="419fe-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="419fe-155">Jos URL-osoite ohjaa jo uudelleen sisäiseen URL-osoitteeseen, valitse **Tyhjennä valinta**, ennen kuin syötät ulkoisen URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="419fe-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="419fe-156">Valitse uudelleenohjauksen tyyppi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="419fe-156">Select a redirect type:</span></span>

    - <span data-ttu-id="419fe-157">**Pysyvä uudelleenohjaus (301)** – Valitse tämä vaihtoehto, kun tiedät, että sisältösi liikkuu pysyvästi eikä palaa aiempaan URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="419fe-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="419fe-158">Hakukoneet määrittävät uudelleenohjauksen URL-osoitteen hakukoneoptimoinnin arvon URL-osoitteelle. joka uudelleenohjataan. Se myös päivittää uuden URL-osoitteen niiden tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="419fe-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="419fe-159">**Väliaikainen uudelleenohjaus (302)** – Valitse tämä vaihtoehto, jos haluat uudelleenohjata liikenteen päivittämättä hakukoneita.</span><span class="sxs-lookup"><span data-stu-id="419fe-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="419fe-160">Tätä menetelmää käytetään yleensä, jos sisältö palaa pian edelliseen URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="419fe-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="419fe-161">Kun olet valmis toteuttamaan uudelleenohjauksen, tallenna ja julkaise URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="419fe-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="419fe-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="419fe-162">Additional resources</span></span>

[<span data-ttu-id="419fe-163">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="419fe-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="419fe-164">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="419fe-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="419fe-165">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="419fe-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="419fe-166">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="419fe-166">Add languages to your site</span></span>](add-languages-to-site.md)
