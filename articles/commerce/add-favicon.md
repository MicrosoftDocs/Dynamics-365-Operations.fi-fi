---
title: Favicon-kuvakkeen lisääminen
description: Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 262e478d426fd913130b21a3434331c7d27b54b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411905"
---
# <a name="add-a-favicon"></a><span data-ttu-id="379ff-103">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="379ff-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="379ff-104">Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.</span><span class="sxs-lookup"><span data-stu-id="379ff-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="379ff-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="379ff-105">Overview</span></span>

<span data-ttu-id="379ff-106">Favicon on pieni grafiikkatiedosto, joka näkyy selaimen välilehdessä, osoitepalkissa, selaushistoriassa sekä muissa paikoissa, kuten kirjanmerkeissä tai suosikeissa.</span><span class="sxs-lookup"><span data-stu-id="379ff-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="379ff-107">Suosittelemme, että lisäät favicon-kuvakkeen sivustoon, koska se edustaa ja vahvistaa omaa tuotemerkkiä ja auttaa sivuston erottumisessa muista sivustoista, joilla asiakkaat käyvät.</span><span class="sxs-lookup"><span data-stu-id="379ff-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="379ff-108">Voit lisätä useita eri kokoisia favicon-kuvakkeita ja erilaisia favicon-tiedostoja sivustoon. Tässä ohjeaiheessa kerrotaan, miten voit lisätä yhden favicon-kohteen.</span><span class="sxs-lookup"><span data-stu-id="379ff-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="379ff-109">Samaa prosessia ja sijaintia käytetään useiden favicon-kohteiden lisäämisessä.</span><span class="sxs-lookup"><span data-stu-id="379ff-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="379ff-110">Lataa favicon sivuston resurssikokoelmaan</span><span class="sxs-lookup"><span data-stu-id="379ff-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="379ff-111">Lataa favicon sivuston resurssikokoelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="379ff-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="379ff-112">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="379ff-112">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="379ff-113">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="379ff-113">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="379ff-114">Siirry Resurssienhallinnan ikkunassa ladattavan favicon-kuvaketiedoston kohdalle, valitse se ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="379ff-114">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="379ff-115">Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="379ff-115">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="379ff-116">Jos haluat julkaista kuvan heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="379ff-116">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="379ff-117">Jos et valitse **Julkaise mediakohteet lataamisen jälkeen** -valintaruutua, palaa **Mediakohteet**-sivulle ja julkaise favicon myöhemmin manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="379ff-117">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="379ff-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="379ff-118">Select **OK**.</span></span>
1. <span data-ttu-id="379ff-119">Kopioi oikealla olevaan ominaisuusruutuun favicon-tiedoston julkinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="379ff-119">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="379ff-120">Tätä URL-osoitetta käytetään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="379ff-120">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="379ff-121">Luo favicon-tiedostollesi HTML-koodia</span><span class="sxs-lookup"><span data-stu-id="379ff-121">Create the HTML for your favicon</span></span>

<span data-ttu-id="379ff-122">Jos haluat luoda favicon-tiedostolle HTML-koodia, käytä seuraavaa HTML-merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="379ff-122">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="379ff-123">Korvaa **href**-määritteessä **Public\_URL\_for\_your\_favicon** aiemmin kopioimallasi julkisella URL-osoitteella.</span><span class="sxs-lookup"><span data-stu-id="379ff-123">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="379ff-124">Luo osa, joka sisältää metatunnisteen omalle faviconillesi</span><span class="sxs-lookup"><span data-stu-id="379ff-124">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="379ff-125">Seuraa näitä ohjeita luodaksesi osan, joka sisältää metatunnisteen omalle faviconillesi.</span><span class="sxs-lookup"><span data-stu-id="379ff-125">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="379ff-126">Siirry kohtaan **Osat** ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="379ff-126">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="379ff-127">Valitse **Uusi osa** -valintaikkunan **Metatunnisteet** moduulina, johon osa perustuu.</span><span class="sxs-lookup"><span data-stu-id="379ff-127">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="379ff-128">Kirjoita osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="379ff-128">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="379ff-129">Valitse fragmentti hierarkiapuussa **Oletusmetatunnisteet**-alikohde.</span><span class="sxs-lookup"><span data-stu-id="379ff-129">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="379ff-130">Valitse oikeanpuoleisessa ruudussa **Metatunnisteet**-kohdasta **Lisää** ja kirjoita sitten aiemmin luomasi favicon-HTML-merkkijono.</span><span class="sxs-lookup"><span data-stu-id="379ff-130">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="379ff-131">Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi osan.</span><span class="sxs-lookup"><span data-stu-id="379ff-131">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="379ff-132">Lisää metatunnisteen osa sivujesi HTML-pääosaan</span><span class="sxs-lookup"><span data-stu-id="379ff-132">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="379ff-133">Seuraa näitä ohjeita lisätäksesi metatunnisteen osa sivujesi HTML-**pää**-osaan.</span><span class="sxs-lookup"><span data-stu-id="379ff-133">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="379ff-134">Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä faviconisi ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="379ff-134">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="379ff-135">Valitse mallihierarkiapuussa **HTML-pääsäilön** oikealla puolella oleva ellipsi- ( **...**)-painike ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="379ff-135">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="379ff-136">Valitse **Uusi osa** -valintaikkunassa metatunnistesivukatkelma, jonka loit aiemmin ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="379ff-136">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="379ff-137">Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.</span><span class="sxs-lookup"><span data-stu-id="379ff-137">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="379ff-138">Jos sivustossa käytetään useampaa kuin yhtä mallia, sinun on lisättävä metatunnisteen osa kaikkiin.</span><span class="sxs-lookup"><span data-stu-id="379ff-138">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="379ff-139">Kun esikatselet sivuja, jotka perustuvat malliin, johon lisäsit metatunnisteen osan, sinun pitäisi nyt nähdä favicon selaimen välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="379ff-139">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="379ff-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="379ff-140">Additional resources</span></span>

[<span data-ttu-id="379ff-141">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="379ff-141">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="379ff-142">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="379ff-142">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="379ff-143">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="379ff-143">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="379ff-144">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="379ff-144">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="379ff-145">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="379ff-145">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="379ff-146">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="379ff-146">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="379ff-147">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="379ff-147">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

