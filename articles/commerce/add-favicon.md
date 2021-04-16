---
title: Favicon-kuvakkeen lisääminen
description: Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.
author: bicyclingfool
ms.date: 08/31/2020
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
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797716"
---
# <a name="add-a-favicon"></a><span data-ttu-id="0c3be-103">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="0c3be-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c3be-104">Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.</span><span class="sxs-lookup"><span data-stu-id="0c3be-104">This topic explains how to add a favicon to your site.</span></span>

<span data-ttu-id="0c3be-105">Favicon on pieni grafiikkatiedosto, joka näkyy selaimen välilehdessä, osoitepalkissa, selaushistoriassa sekä muissa paikoissa, kuten kirjanmerkeissä tai suosikeissa.</span><span class="sxs-lookup"><span data-stu-id="0c3be-105">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="0c3be-106">Suosittelemme, että lisäät favicon-kuvakkeen sivustoon, koska se edustaa ja vahvistaa omaa tuotemerkkiä ja auttaa sivuston erottumisessa muista sivustoista, joilla asiakkaat käyvät.</span><span class="sxs-lookup"><span data-stu-id="0c3be-106">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="0c3be-107">Voit lisätä useita eri kokoisia favicon-kuvakkeita ja erilaisia favicon-tiedostoja sivustoon. Tässä ohjeaiheessa kerrotaan, miten voit lisätä yhden favicon-kohteen.</span><span class="sxs-lookup"><span data-stu-id="0c3be-107">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="0c3be-108">Samaa prosessia ja sijaintia käytetään useiden favicon-kohteiden lisäämisessä.</span><span class="sxs-lookup"><span data-stu-id="0c3be-108">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="0c3be-109">Lataa favicon sivuston resurssikokoelmaan</span><span class="sxs-lookup"><span data-stu-id="0c3be-109">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="0c3be-110">Lataa favicon sivuston resurssikokoelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0c3be-110">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="0c3be-111">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-111">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="0c3be-112">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-112">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="0c3be-113">Siirry Resurssienhallinnan ikkunassa ladattavan favicon-kuvaketiedoston kohdalle, valitse se ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-113">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="0c3be-114">Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="0c3be-114">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="0c3be-115">Jos haluat julkaista kuvan heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0c3be-115">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0c3be-116">Jos et valitse **Julkaise mediakohteet lataamisen jälkeen** -valintaruutua, palaa **Mediakohteet**-sivulle ja julkaise favicon myöhemmin manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="0c3be-116">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="0c3be-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-117">Select **OK**.</span></span>
1. <span data-ttu-id="0c3be-118">Kopioi oikealla olevaan ominaisuusruutuun favicon-tiedoston julkinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="0c3be-118">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="0c3be-119">Tätä URL-osoitetta käytetään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="0c3be-119">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="0c3be-120">Luo favicon-tiedostollesi HTML-koodia</span><span class="sxs-lookup"><span data-stu-id="0c3be-120">Create the HTML for your favicon</span></span>

<span data-ttu-id="0c3be-121">Jos haluat luoda favicon-tiedostolle HTML-koodia, käytä seuraavaa HTML-merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="0c3be-121">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="0c3be-122">Korvaa **href**-määritteessä **Public\_URL\_for\_your\_favicon** aiemmin kopioimallasi julkisella URL-osoitteella.</span><span class="sxs-lookup"><span data-stu-id="0c3be-122">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="0c3be-123">Luo osa, joka sisältää metatunnisteen omalle faviconillesi</span><span class="sxs-lookup"><span data-stu-id="0c3be-123">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="0c3be-124">Seuraa näitä ohjeita luodaksesi osan, joka sisältää metatunnisteen omalle faviconillesi.</span><span class="sxs-lookup"><span data-stu-id="0c3be-124">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="0c3be-125">Siirry kohtaan **Osat** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-125">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="0c3be-126">Valitse **Uusi osa** -valintaikkunan **Metatunnisteet** moduulina, johon osa perustuu.</span><span class="sxs-lookup"><span data-stu-id="0c3be-126">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="0c3be-127">Kirjoita osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-127">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0c3be-128">Valitse fragmentti hierarkiapuussa **Oletusmetatunnisteet**-alikohde.</span><span class="sxs-lookup"><span data-stu-id="0c3be-128">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="0c3be-129">Valitse oikeanpuoleisessa ruudussa **Metatunnisteet**-kohdasta **Lisää** ja kirjoita sitten aiemmin luomasi favicon-HTML-merkkijono.</span><span class="sxs-lookup"><span data-stu-id="0c3be-129">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="0c3be-130">Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi osan.</span><span class="sxs-lookup"><span data-stu-id="0c3be-130">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="0c3be-131">Lisää metatunnisteen osa sivujesi HTML-pääosaan</span><span class="sxs-lookup"><span data-stu-id="0c3be-131">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="0c3be-132">Seuraa näitä ohjeita lisätäksesi metatunnisteen osa sivujesi HTML-**pää**-osaan.</span><span class="sxs-lookup"><span data-stu-id="0c3be-132">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="0c3be-133">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä faviconisi ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-133">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="0c3be-134">Valitse mallihierarkiapuussa **HTML-pääsäilön** oikealla puolella oleva ellipsi- ( **...**)-painike ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-134">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="0c3be-135">Valitse **Uusi osa** -valintaikkunassa metatunnistesivukatkelma, jonka loit aiemmin ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3be-135">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="0c3be-136">Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.</span><span class="sxs-lookup"><span data-stu-id="0c3be-136">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="0c3be-137">Jos sivustossa käytetään useampaa kuin yhtä mallia, sinun on lisättävä metatunnisteen osa kaikkiin.</span><span class="sxs-lookup"><span data-stu-id="0c3be-137">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="0c3be-138">Kun esikatselet sivuja, jotka perustuvat malliin, johon lisäsit metatunnisteen osan, sinun pitäisi nyt nähdä favicon selaimen välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="0c3be-138">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c3be-139">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0c3be-139">Additional resources</span></span>

[<span data-ttu-id="0c3be-140">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="0c3be-140">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0c3be-141">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="0c3be-141">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0c3be-142">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="0c3be-142">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0c3be-143">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="0c3be-143">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0c3be-144">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="0c3be-144">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0c3be-145">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="0c3be-145">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0c3be-146">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="0c3be-146">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
