---
title: Aiemmin luodun sivuston sivun muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.
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
ms.openlocfilehash: 50373d3681e269bf6164b2a425bbafebdd93d64f
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945694"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="1d297-103">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="1d297-103">Modify an existing site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1d297-104">Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="1d297-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d297-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1d297-105">Overview</span></span>

<span data-ttu-id="1d297-106">Sivun muokkauksen ensimmäinen vaihe on sivun avaaminen sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="1d297-107">Siirry sivustoon, joka sisältää sivun. Etsi haluamasi sivu sivuluettelosta.</span><span class="sxs-lookup"><span data-stu-id="1d297-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="1d297-108">Jos et löydä sivua, voit käyttää muokkaustyökalun monipuolisia hakutoimintoja.</span><span class="sxs-lookup"><span data-stu-id="1d297-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="1d297-109">Kirjoita sivun tarkka nimi tai sen ensimmäiset kirjaimet ja sen jälkeen tähti (\*).</span><span class="sxs-lookup"><span data-stu-id="1d297-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="1d297-110">Näkyviin tulee suodatettu luettelo sivuista.</span><span class="sxs-lookup"><span data-stu-id="1d297-110">A filtered list of pages appears.</span></span> <span data-ttu-id="1d297-111">Tämän luettelon avulla voit etsiä haluamasi sivun.</span><span class="sxs-lookup"><span data-stu-id="1d297-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="1d297-112">Kun olet löytänyt oikean sivun, avaa sivu sivueditorissa valitsemalla sivun nimi.</span><span class="sxs-lookup"><span data-stu-id="1d297-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="1d297-113">Jos sivusi näkyy sivun tarkistusohjelmassa, voit valita sen ja kuitata sen ulos, ennen kuin avaat sen sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="1d297-114">Näin voit kuitata ulos useita sivuja samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="1d297-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="1d297-115">Kun sivu on avattu sivueditorissa, sinun on varmistettava, että se on kuitattu ulos sinulle.</span><span class="sxs-lookup"><span data-stu-id="1d297-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="1d297-116">Muokkaustyökalun komentopalkki on dynaaminen sekä tilanne- ja tilakohtainen.</span><span class="sxs-lookup"><span data-stu-id="1d297-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="1d297-117">Tämän vuoksi siinä näkyvät vain toiminnot, jotka voidaan määrittää sivulla tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="1d297-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="1d297-118">Jos sivua ei esimerkiksi ole kuitattu ulos sinulle, **Tallenna**- ja **Kuittaa sisään** -painikkeet eivät näy komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="1d297-119">Sivun tila näkyy myös ikkunan oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="1d297-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="1d297-120">Jos sivua ei ole vielä kuitattu ulos sinulle, valitse **Kuittaa ulos** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="1d297-121">Komentopalkki muuttuu sivun uuden tilan mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="1d297-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="1d297-122">Saat myös ilmoituksen, jossa kerrotaan, että sivu on kuitattu ulos sinulle.</span><span class="sxs-lookup"><span data-stu-id="1d297-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="1d297-123">Seuraava vaihe on todellisten muutosten tekeminen.</span><span class="sxs-lookup"><span data-stu-id="1d297-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="1d297-124">Sivun vasemmalla puolella olevaa jäsennyspuuta käytetään usein muutettavan moduulin etsimisessä ja valitsemisessa. Tämän jälkeen muutokset tehdään oikealla olevassa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="1d297-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="1d297-125">Muutos voi kuitenkin joskus vaatia mallien tai osien lisäämisen tai poistamisen.</span><span class="sxs-lookup"><span data-stu-id="1d297-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="1d297-126">Voit lisätä osan tai moduulin sivun jäsennyspuun avulla. Etsi paikka, johon moduuli tai osa lisätään, ja valitse sitten kyseisen paikan kolmen pisteen painike (**...**).</span><span class="sxs-lookup"><span data-stu-id="1d297-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="1d297-127">Näyttöön tulee valikko, joka sisältää moduulin tai osan lisäämisessä käytettävät komennot.</span><span class="sxs-lookup"><span data-stu-id="1d297-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="1d297-128">Voit poistaa moduulin tai osan etsimällä sen sivun jäsennyspuusta ja valitsemalla sen. Valitse kolmen pisteen painike ja valitse sitten moduulin tai osan poistamisen komento.</span><span class="sxs-lookup"><span data-stu-id="1d297-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="1d297-129">Voit myös tarkastella minkä tahansa sellaisen moduulin ominaisuuksia ja muokata niitä, joka näkyy WYSIWYG-esikatselussa. Tällöin voit valita moduulin suoraan.</span><span class="sxs-lookup"><span data-stu-id="1d297-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="1d297-130">Kun muutokset on tehty ja niiden vaikutusta esikatseltu, kuittaa sivu sisään valitsemalla **Kuittaa sisään** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="1d297-131">Voit julkaista tekemäsi muutokset heti valitsemalla **Julkaise** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="1d297-132">Sivun viimeisin sisäänkuitattu versio, jota muokkasit, on julkaistu. Se on sivustoa tarkastelevien ulkoisten käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="1d297-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="1d297-133">Esimerkki: Aloitussivun videon muuttaminen</span><span class="sxs-lookup"><span data-stu-id="1d297-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="1d297-134">Seuraavassa esimerkissä näytetään, miten aloitussivua muokataan muuttamalla videota, joka näkyy videotoistinmoduulissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="1d297-135">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="1d297-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1d297-136">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="1d297-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="1d297-137">Etsi ja valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="1d297-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="1d297-138">Valitse komentopalkissa **Kuittaa ulos**.</span><span class="sxs-lookup"><span data-stu-id="1d297-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="1d297-139">Valitse sivun jäsennyksessä **pääpaikka**.</span><span class="sxs-lookup"><span data-stu-id="1d297-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="1d297-140">Laajenna kaikki nestesäilömoduulit **pääpaikassa**.</span><span class="sxs-lookup"><span data-stu-id="1d297-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="1d297-141">Etsi ja valitse videotoistinmoduuli.</span><span class="sxs-lookup"><span data-stu-id="1d297-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="1d297-142">Valitse oikealla olevassa ominaisuusruudussa **Video**-ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="1d297-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="1d297-143">Resurssin valitsin tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="1d297-143">The asset picker appears.</span></span>
1. <span data-ttu-id="1d297-144">Valitse resurssin valitsimessa käytettävissä oleva videoresurssi tai valitse **Lataa uusi resurssi**, jos haluat ladata uuden videoresurssin.</span><span class="sxs-lookup"><span data-stu-id="1d297-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="1d297-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1d297-145">Select **OK**.</span></span>
1. <span data-ttu-id="1d297-146">Valitse ensin **Tallenna** ja sitten **Kirjaa sisään**.</span><span class="sxs-lookup"><span data-stu-id="1d297-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="1d297-147">Syötä **Kommentit**-kenttään **Videota muutettiin** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1d297-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="1d297-148">Esikatsele päivitettyä sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="1d297-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="1d297-149">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1d297-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="1d297-150">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="1d297-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d297-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1d297-151">Additional resources</span></span>

[<span data-ttu-id="1d297-152">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="1d297-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1d297-153">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="1d297-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1d297-154">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="1d297-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="1d297-155">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="1d297-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1d297-156">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="1d297-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1d297-157">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="1d297-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="1d297-158">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="1d297-158">Verify page content accessibility</span></span>](verify-accessibility.md)
