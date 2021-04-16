---
title: Staattisten tiedostojen lataaminen ja käyttäminen
description: Tässä aiheessa kuvataan, miten voit ladata staattisen tiedoston Microsoft Dynamics 365 Commerce -sivuston muodostimeen ja miten voit luoda mukautetun URL-osoitteen ja tiedostonimen, joita voidaan käyttää tiedoston pyytämisessä.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d5f092042b3dda65b041ab2f25f7319dd8e158d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801382"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="eab0b-103">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="eab0b-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eab0b-104">Tässä aiheessa kuvataan, miten voit ladata staattisen tiedoston Microsoft Dynamics 365 Commerce -sivuston muodostimeen ja miten voit luoda mukautetun URL-osoitteen ja tiedostonimen, joita voidaan käyttää tiedoston pyytämisessä.</span><span class="sxs-lookup"><span data-stu-id="eab0b-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="eab0b-105">Jotkin kolmannen osapuolen liittimet edellyttävät, että tiedostoa isännöidään ja tarjoillaan verkkokauppasivustosta.</span><span class="sxs-lookup"><span data-stu-id="eab0b-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="eab0b-106">Nämä liittimet odottavat, että tiedosto palautetaan pyynnöillä tiettyyn takaisinkutsun URL-polkuun ja tiedostonimeen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="eab0b-107">Tämän vuoksi tässä ohjeaiheessa kerrotaan, kuinka voit ladata ja käyttää staattista tiedostoa, jonka URL-osoite ja tiedostonimi ovat käyttäjän määritettävissä Dynamics 365 Commerce -verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="eab0b-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="eab0b-108">Staattisen tiedoston palauttavan sivuston URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="eab0b-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="eab0b-109">Jos haluat luoda sivuston URL-osoitteen, joka palauttaa staattisen tiedoston Commerce-sivuston muodostimessa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="eab0b-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="eab0b-110">Siirry sivustosi mediakirjastoon ja lataa palvelimeen tiedosto, jonka haluat saataville URL-osoitteesta, jonka määrität.</span><span class="sxs-lookup"><span data-stu-id="eab0b-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="eab0b-111">Jos olet jo ladannut tiedoston, voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="eab0b-112">Siirry sivuston **URL-osoitteet** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="eab0b-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="eab0b-113">Valitse **Uusi \> Uusi URL-soite**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="eab0b-114">Valitse **Uusi URL-osoite** -valintaikkunassa **Mediakirjaston resurssi**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="eab0b-115">Kirjoita URL-polku **URL-polku** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="eab0b-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="eab0b-116">Lisää tiedoston nimi polkuun.</span><span class="sxs-lookup"><span data-stu-id="eab0b-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="eab0b-117">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-117">Select **Next**.</span></span> <span data-ttu-id="eab0b-118">Mediakirjasto avataan ja siinä näkyvät kaikki lataamasi **tiedostotyypin** mediaresurssit.</span><span class="sxs-lookup"><span data-stu-id="eab0b-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="eab0b-119">Valitse tiedosto, joka on tarkoitettu vaiheessa 5 määritettyyn URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="eab0b-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-120">Select **Save**.</span></span>

<span data-ttu-id="eab0b-121">Tässä vaiheessa luomasi URL-osoite on luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="eab0b-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="eab0b-122">Tiedostoa, johon URL-osoite osoittaa, ei palauteta, ennen kuin julkaiset URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="eab0b-123">Ennen kuin julkaiset URL-osoitteen, voit vahvistaa, että se palauttaa oikeat tiedot.</span><span class="sxs-lookup"><span data-stu-id="eab0b-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="eab0b-124">URL-osoitteen tarkistaminen ja julkaisu</span><span class="sxs-lookup"><span data-stu-id="eab0b-124">Validate and publish a URL</span></span>

<span data-ttu-id="eab0b-125">Voit vahvistaa URL-osoitteen ennen sen julkaisua tekemällä seuraavat toimet.</span><span class="sxs-lookup"><span data-stu-id="eab0b-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="eab0b-126">Siirry sivuston kohtaan **URL-osoitteet** ja valitse esikatseltava URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="eab0b-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="eab0b-127">Valitse oikealla olevan Ominaisuudet-ruudun **Muokkaa**-painikkeen alapuolelta oikea URL-linkki.</span><span class="sxs-lookup"><span data-stu-id="eab0b-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="eab0b-128">Uusi selainikkuna avautuu ja näyttöön tulee virhe 404.</span><span class="sxs-lookup"><span data-stu-id="eab0b-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="eab0b-129">Liitä kyselymerkkijono **?preview=inprogress** URL-osoitteeseen (esimerkiksi `https://yoursite.com/callback.html?preview=inprogress`) ja lataa sivu uudelleen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="eab0b-130">Mediakirjastoon lataamasi tiedosto palautetaan vastauksessa.</span><span class="sxs-lookup"><span data-stu-id="eab0b-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="eab0b-131">Kun olet vahvistanut URL-osoitteen, voit julkaista sen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="eab0b-132">Siirry sivuston kohtaan **URL-osoitteet** ja valitse URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="eab0b-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="eab0b-133">Valitse komentopalkissa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="eab0b-134">Päivitä tiedosto, johon URL-osoite osoittaa</span><span class="sxs-lookup"><span data-stu-id="eab0b-134">Update the file that a URL points to</span></span>

<span data-ttu-id="eab0b-135">Kun URL-osoite on julkaistu, voit päivittää sen niin, että se osoittaa toiseen tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="eab0b-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="eab0b-136">Vaihtoehtoisesti voit päivittää URL-osoitteen niin, että se osoittaa eri tyyppiseen resurssii, kuten seuraavassa osassa on kuvattu.</span><span class="sxs-lookup"><span data-stu-id="eab0b-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="eab0b-137">Voit esimerkiksi osoittaa URL-osoitteen sisäiselle sivulle tai uudelleenohjaukseen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="eab0b-138">Jos haluat päivittää tiedoston, johon URL-osoite viittaa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="eab0b-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="eab0b-139">Siirry sivuston kohtaan **URL-osoitteet** ja valitse päivitettävä URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="eab0b-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="eab0b-140">Valitse oikeanpuoleisessa ominaisuusruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="eab0b-141">Valitse **URL-osoitteen määritys** -kohdasta **Vaihe 2** -ruutu ja valitse sitten uusi tiedosto mediakirjastosta.</span><span class="sxs-lookup"><span data-stu-id="eab0b-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="eab0b-142">Valitse **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="eab0b-143">Päivitä resurssityyppi, johon URL-osoite osoittaa</span><span class="sxs-lookup"><span data-stu-id="eab0b-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="eab0b-144">Voit myös päivittää URL-osoitteen niin, että se osoittaa erityyppiseen resurssiin, kuten sisäiselle sivulle tai uudelleenohjaukseen.</span><span class="sxs-lookup"><span data-stu-id="eab0b-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="eab0b-145">Jos haluat päivittää resurssityypin, johon URL-osoite viittaa, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="eab0b-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="eab0b-146">Siirry sivuston kohtaan **URL-osoitteet** ja valitse päivitettävä URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="eab0b-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="eab0b-147">Valitse oikeanpuoleisessa ominaisuusruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="eab0b-148">Valitse **URL-osoitteen määritys** -kohdan **Vaihe 1** -kohdassa toinen resurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="eab0b-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="eab0b-149">Valitse **Vaihe 2** -ruutu ja valitse sitten uusi resurssi.</span><span class="sxs-lookup"><span data-stu-id="eab0b-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="eab0b-150">Valitse **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="eab0b-151">URL-polun muuttaminen</span><span class="sxs-lookup"><span data-stu-id="eab0b-151">Change the URL path</span></span>

<span data-ttu-id="eab0b-152">Kun URL-osoite on luotu, sen polkua ei voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="eab0b-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="eab0b-153">Jos sinun on muutettava URL-polkua, joka tarjoaa tiedoston tai jonkin muun resurssin, luo uusi URL-osoite, yhdistä se olemassa olevaan tiedostoon tai muuhun resurssiin ja sitten peruuta vanhan URL-osoitteen julkaisu ja poista osoite.</span><span class="sxs-lookup"><span data-stu-id="eab0b-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="eab0b-154">Voit muuttaa URL-polkua seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="eab0b-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="eab0b-155">Jos haluat luoda uuden URL-osoitteen ja yhdistää sen aiemmin luotuun tiedostoon tai muuhun resurssiin, noudata aiemmin tässä ohjeaiheessa olevan osan [Staattisen tiedoston palauttavan sivuston URL-osoitteen luominen](#create-a-site-url-that-returns-a-static-file) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="eab0b-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="eab0b-156">Valitse uusi URL-osoite ja valitse komentopalkissa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="eab0b-157">Uusi URL-osoite julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="eab0b-157">The new URL is published.</span></span>
1. <span data-ttu-id="eab0b-158">Voit peruuttaa vanhan URL-osoitteen julkaisemisen valitsemalla osoitteen ja valitsemalla sitten komentopalkissa **Peruuta julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="eab0b-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="eab0b-159">Voit nyt poistaa vanhan URL-osoitteen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="eab0b-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eab0b-160">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="eab0b-160">Additional resources</span></span>

[<span data-ttu-id="eab0b-161">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="eab0b-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="eab0b-162">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="eab0b-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="eab0b-163">Videoiden lataaminen</span><span class="sxs-lookup"><span data-stu-id="eab0b-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="eab0b-164">Muiden tiedostojen kuin kuvien ja videoiden lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="eab0b-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="eab0b-165">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="eab0b-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="eab0b-166">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="eab0b-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]