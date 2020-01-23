---
title: Favicon-kuvakkeen lisääminen
description: Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914568"
---
# <a name="add-a-favicon"></a><span data-ttu-id="f21bb-103">Favicon-kuvakkeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f21bb-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f21bb-104">Tässä ohjeaiheessa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.</span><span class="sxs-lookup"><span data-stu-id="f21bb-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="f21bb-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f21bb-105">Overview</span></span>

<span data-ttu-id="f21bb-106">Favicon on pieni grafiikkatiedosto, joka näkyy selaimen välilehdessä, osoitepalkissa, selaushistoriassa sekä muissa paikoissa, kuten kirjanmerkeissä tai suosikeissa.</span><span class="sxs-lookup"><span data-stu-id="f21bb-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="f21bb-107">Suosittelemme, että lisäät favicon-kuvakkeen sivustoon, koska se edustaa ja vahvistaa omaa tuotemerkkiä ja auttaa sivuston erottumisessa muista sivustoista, joilla asiakkaat käyvät.</span><span class="sxs-lookup"><span data-stu-id="f21bb-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="f21bb-108">Voit lisätä useita eri kokoisia favicon-kuvakkeita ja erilaisia favicon-tiedostoja sivustoon. Tässä ohjeaiheessa kerrotaan, miten voit lisätä yhden favicon-kohteen.</span><span class="sxs-lookup"><span data-stu-id="f21bb-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="f21bb-109">Samaa prosessia ja sijaintia käytetään useiden favicon-kohteiden lisäämisessä.</span><span class="sxs-lookup"><span data-stu-id="f21bb-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="f21bb-110">Lataa favicon sivuston resurssikokoelmaan</span><span class="sxs-lookup"><span data-stu-id="f21bb-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="f21bb-111">Lataa favicon sivuston resurssikokoelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f21bb-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="f21bb-112">Siirry kohtaan **Resurssit \> Lataa \> Lataa resurssit**.</span><span class="sxs-lookup"><span data-stu-id="f21bb-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="f21bb-113">Etsi ja valitse favicon paikallisessa tiedostojärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="f21bb-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="f21bb-114">Kirjoita otsikko ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f21bb-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="f21bb-115">Kopioi oikealla olevaan ominaisuusruutuun favicon-tiedoston julkinen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f21bb-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="f21bb-116">Jos et valitse **Julkaise resurssit lataamisen jälkeen** -vaihtoehtoa, palaa **Resurssit**-sivulle ja julkaise favicon myöhemmin manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f21bb-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="f21bb-117">Luo favicon-tiedostolle HTML-koodia</span><span class="sxs-lookup"><span data-stu-id="f21bb-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="f21bb-118">Jos haluat luoda favicon-tiedostolle HTML-koodia, käytä seuraavaa HTML-katkelmaa.</span><span class="sxs-lookup"><span data-stu-id="f21bb-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="f21bb-119">Korvaa **href**-määritteessä **"Public\_URL\_for\_your\_favicon"** aiemmin kopioimallasi julkisella URL-osoitteella.</span><span class="sxs-lookup"><span data-stu-id="f21bb-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="f21bb-120">Lisää favicon-tiedostoon HTML-koodia sivuston \<head\>-elementissä</span><span class="sxs-lookup"><span data-stu-id="f21bb-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="f21bb-121">Jos haluat lisätä favicon-tiedoston sivustoon, käytä samaa menetelmää, jonka avulla lisäät minkä tahansa HTML- tai komentosarjan **\<head\>**-elementtiin sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="f21bb-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f21bb-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f21bb-122">Additional resources</span></span>

[<span data-ttu-id="f21bb-123">Logon lisääminen</span><span class="sxs-lookup"><span data-stu-id="f21bb-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f21bb-124">Sivuston teeman valitseminen</span><span class="sxs-lookup"><span data-stu-id="f21bb-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f21bb-125">CSS-ohitustiedostojen parissa työskentely</span><span class="sxs-lookup"><span data-stu-id="f21bb-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f21bb-126">Tervetuloviestin lisääminen</span><span class="sxs-lookup"><span data-stu-id="f21bb-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f21bb-127">Copyright-ilmoituksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="f21bb-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f21bb-128">Kielten lisääminen sivustoon</span><span class="sxs-lookup"><span data-stu-id="f21bb-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f21bb-129">Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi</span><span class="sxs-lookup"><span data-stu-id="f21bb-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

