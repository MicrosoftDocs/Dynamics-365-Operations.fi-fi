---
title: Aiemmin luodun sivuston sivun muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803726"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="2f855-103">Aiemmin luodun sivuston sivun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2f855-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f855-104">Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2f855-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2f855-105">Sivun muokkauksen ensimmäinen vaihe on sivun avaaminen sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="2f855-106">Siirry sivustoon, joka sisältää sivun. Etsi haluamasi sivu sivuluettelosta.</span><span class="sxs-lookup"><span data-stu-id="2f855-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="2f855-107">Jos et löydä sivua, voit käyttää muokkaustyökalun monipuolisia hakutoimintoja.</span><span class="sxs-lookup"><span data-stu-id="2f855-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="2f855-108">Kirjoita sivun tarkka nimi tai sen ensimmäiset kirjaimet ja sen jälkeen tähti (\*).</span><span class="sxs-lookup"><span data-stu-id="2f855-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="2f855-109">Näkyviin tulee suodatettu luettelo sivuista.</span><span class="sxs-lookup"><span data-stu-id="2f855-109">A filtered list of pages appears.</span></span> <span data-ttu-id="2f855-110">Tämän luettelon avulla voit etsiä haluamasi sivun.</span><span class="sxs-lookup"><span data-stu-id="2f855-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="2f855-111">Kun olet löytänyt oikean sivun, avaa sivu sivueditorissa valitsemalla sivun nimi.</span><span class="sxs-lookup"><span data-stu-id="2f855-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="2f855-112">Jos sivusi näkyy sivun tarkistusohjelmassa, voit valita **Muokkaa** ja tarkistaa sivun ennen kuin avaat sen sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="2f855-113">Näin voit kuitata ulos useita sivuja samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="2f855-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="2f855-114">Kun sivu on avattu sivueditorissa, sinun on varmistettava, että se on kuitattu ulos sinulle.</span><span class="sxs-lookup"><span data-stu-id="2f855-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="2f855-115">Muokkaustyökalun komentopalkki on dynaaminen sekä tilanne- ja tilakohtainen.</span><span class="sxs-lookup"><span data-stu-id="2f855-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="2f855-116">Tämän vuoksi siinä näkyvät vain toiminnot, jotka voidaan määrittää sivulla tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="2f855-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="2f855-117">Jos sivua ei esimerkiksi ole kuitattu ulos sinulle, **Tallenna**- ja **Lopeta muokkaus** -painikkeet eivät näy komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="2f855-118">Sivun tila näkyy myös ikkunan oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="2f855-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="2f855-119">Jos sivua ei ole vielä kuitattu ulos sinulle, valitse **Muokkaa** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="2f855-120">Komentopalkki muuttuu sivun uuden tilan mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="2f855-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="2f855-121">Saat myös ilmoituksen, jossa kerrotaan, että sivu on kuitattu ulos sinulle.</span><span class="sxs-lookup"><span data-stu-id="2f855-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="2f855-122">Seuraava vaihe on todellisten muutosten tekeminen.</span><span class="sxs-lookup"><span data-stu-id="2f855-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="2f855-123">Sivun vasemmalla puolella olevaa jäsennyspuuta käytetään usein muutettavan moduulin etsimisessä ja valitsemisessa. Tämän jälkeen muutokset tehdään oikealla olevassa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="2f855-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="2f855-124">Muutos voi kuitenkin joskus vaatia mallien tai osien lisäämisen tai poistamisen.</span><span class="sxs-lookup"><span data-stu-id="2f855-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="2f855-125">Voit lisätä osan tai moduulin sivun jäsennyspuun avulla. Etsi paikka, johon moduuli tai osa lisätään, ja valitse sitten kyseisen paikan kolmen pisteen painike (**...**).</span><span class="sxs-lookup"><span data-stu-id="2f855-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="2f855-126">Näyttöön tulee valikko, joka sisältää moduulin tai osan lisäämisessä käytettävät komennot.</span><span class="sxs-lookup"><span data-stu-id="2f855-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="2f855-127">Voit poistaa moduulin tai osan etsimällä sen sivun jäsennyspuusta ja valitsemalla sen. Valitse kolmen pisteen painike ja valitse sitten moduulin tai osan poistamisen komento.</span><span class="sxs-lookup"><span data-stu-id="2f855-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="2f855-128">Voit myös tarkastella minkä tahansa sellaisen moduulin ominaisuuksia, joka näkyy visuaalisessa sivunmuodostimen esikatselussa, ja muokata niitä. Tällöin voit valita moduulin suoraan.</span><span class="sxs-lookup"><span data-stu-id="2f855-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="2f855-129">Kun muutokset on tehty ja niiden vaikutusta esikatseltu, kuittaa sivu sisään valitsemalla **Lopeta muokkaus** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="2f855-130">Voit julkaista tekemäsi muutokset heti valitsemalla **Julkaise** komentopalkissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="2f855-131">Sivun viimeisin sisäänkuitattu versio, jota muokkasit, on julkaistu. Se on sivustoa tarkastelevien ulkoisten käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="2f855-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="2f855-132">Esimerkki: Aloitussivun videon muuttaminen</span><span class="sxs-lookup"><span data-stu-id="2f855-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="2f855-133">Seuraavassa esimerkissä näytetään, miten aloitussivua muokataan muuttamalla videota, joka näkyy videotoistinmoduulissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="2f855-134">Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).</span><span class="sxs-lookup"><span data-stu-id="2f855-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2f855-135">Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="2f855-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="2f855-136">Etsi ja valitse aloitussivu, joka avataan sivueditorissa.</span><span class="sxs-lookup"><span data-stu-id="2f855-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2f855-137">Valitse komentopalkissa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2f855-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="2f855-138">Valitse sivun jäsennyksessä **pääpaikka**.</span><span class="sxs-lookup"><span data-stu-id="2f855-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="2f855-139">Laajenna kaikki nestesäilömoduulit **pääpaikassa**.</span><span class="sxs-lookup"><span data-stu-id="2f855-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="2f855-140">Etsi ja valitse videotoistinmoduuli.</span><span class="sxs-lookup"><span data-stu-id="2f855-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="2f855-141">Valitse oikealla olevassa ominaisuusruudussa **Video**-ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2f855-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="2f855-142">Resurssin valitsin tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="2f855-142">The asset picker appears.</span></span>
1. <span data-ttu-id="2f855-143">Valitse resurssin valitsimessa käytettävissä oleva videoresurssi tai valitse **Lataa uusi resurssi**, jos haluat ladata uuden videoresurssin.</span><span class="sxs-lookup"><span data-stu-id="2f855-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="2f855-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f855-144">Select **OK**.</span></span>
1. <span data-ttu-id="2f855-145">Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="2f855-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2f855-146">Syötä **Kommentit**-kenttään **Videota muutettiin** ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f855-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="2f855-147">Esikatsele päivitettyä sivua valitsemalla **Esikatsele**.</span><span class="sxs-lookup"><span data-stu-id="2f855-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="2f855-148">Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2f855-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2f855-149">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="2f855-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f855-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2f855-150">Additional resources</span></span>

[<span data-ttu-id="2f855-151">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="2f855-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2f855-152">Sivun asettelujen valitseminen</span><span class="sxs-lookup"><span data-stu-id="2f855-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2f855-153">SEO-metatietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="2f855-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2f855-154">Sivun tallentaminen, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="2f855-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2f855-155">Tuotesivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="2f855-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2f855-156">Luokan saapumissivun täydentäminen</span><span class="sxs-lookup"><span data-stu-id="2f855-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="2f855-157">Sivun sisällön helppokäyttöisyyden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="2f855-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="2f855-158">Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella</span><span class="sxs-lookup"><span data-stu-id="2f855-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
