---
title: Muiden kuin kuva- ja videotiedostojen lataaminen
description: Tässä ohjeaiheessa kerrotaan, miten muita kuin kuva- ja videobinaaritiedostoja ladataan Microsoft Dynamics 365 Commercen sivuston luontiohjelmassa.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799250"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="4065d-103">Muiden tiedostojen kuin kuvien ja videoiden lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="4065d-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4065d-104">Tässä ohjeaiheessa kerrotaan, miten muita kuin kuva- ja videotiedostoja ladataan Microsoft Dynamics 365 Commercen sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="4065d-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="4065d-105">Commerce-sivuston luontiohjelman mediakirjasto tukee sellaisten binaariresurssien lataamista, jotka eivät ole kuvia ja videoita.</span><span class="sxs-lookup"><span data-stu-id="4065d-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="4065d-106">Voit esimerkiksi ladata Microsoft Excel-, Microsoft Word-, Microsoft PowerPoint- tai PDF-tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="4065d-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="4065d-107">Seuraavia asiakirjatyyppejä tuetaan:</span><span class="sxs-lookup"><span data-stu-id="4065d-107">The following document types are supported:</span></span>
- <span data-ttu-id="4065d-108">7Z</span><span class="sxs-lookup"><span data-stu-id="4065d-108">7Z</span></span>
- <span data-ttu-id="4065d-109">AVI</span><span class="sxs-lookup"><span data-stu-id="4065d-109">AVI</span></span>
- <span data-ttu-id="4065d-110">CS</span><span class="sxs-lookup"><span data-stu-id="4065d-110">CS</span></span>
- <span data-ttu-id="4065d-111">CSS</span><span class="sxs-lookup"><span data-stu-id="4065d-111">CSS</span></span>
- <span data-ttu-id="4065d-112">DOC</span><span class="sxs-lookup"><span data-stu-id="4065d-112">DOC</span></span>
- <span data-ttu-id="4065d-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="4065d-113">DOCX</span></span>
- <span data-ttu-id="4065d-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="4065d-114">EPUB</span></span>
- <span data-ttu-id="4065d-115">GIF</span><span class="sxs-lookup"><span data-stu-id="4065d-115">GIF</span></span>
- <span data-ttu-id="4065d-116">INDD</span><span class="sxs-lookup"><span data-stu-id="4065d-116">INDD</span></span>
- <span data-ttu-id="4065d-117">JAR</span><span class="sxs-lookup"><span data-stu-id="4065d-117">JAR</span></span>
- <span data-ttu-id="4065d-118">JPG</span><span class="sxs-lookup"><span data-stu-id="4065d-118">JPG</span></span>
- <span data-ttu-id="4065d-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="4065d-119">JPEG</span></span>
- <span data-ttu-id="4065d-120">JS</span><span class="sxs-lookup"><span data-stu-id="4065d-120">JS</span></span>
- <span data-ttu-id="4065d-121">MP3</span><span class="sxs-lookup"><span data-stu-id="4065d-121">MP3</span></span>
- <span data-ttu-id="4065d-122">MP4</span><span class="sxs-lookup"><span data-stu-id="4065d-122">MP4</span></span>
- <span data-ttu-id="4065d-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="4065d-123">MPEG</span></span>
- <span data-ttu-id="4065d-124">MPG</span><span class="sxs-lookup"><span data-stu-id="4065d-124">MPG</span></span>
- <span data-ttu-id="4065d-125">ODP</span><span class="sxs-lookup"><span data-stu-id="4065d-125">ODP</span></span>
- <span data-ttu-id="4065d-126">ODS</span><span class="sxs-lookup"><span data-stu-id="4065d-126">ODS</span></span>
- <span data-ttu-id="4065d-127">ODT</span><span class="sxs-lookup"><span data-stu-id="4065d-127">ODT</span></span>
- <span data-ttu-id="4065d-128">PDF</span><span class="sxs-lookup"><span data-stu-id="4065d-128">PDF</span></span>
- <span data-ttu-id="4065d-129">PNG</span><span class="sxs-lookup"><span data-stu-id="4065d-129">PNG</span></span>
- <span data-ttu-id="4065d-130">PPT</span><span class="sxs-lookup"><span data-stu-id="4065d-130">PPT</span></span>
- <span data-ttu-id="4065d-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="4065d-131">PPTX</span></span>
- <span data-ttu-id="4065d-132">PS</span><span class="sxs-lookup"><span data-stu-id="4065d-132">PS</span></span>
- <span data-ttu-id="4065d-133">QXP</span><span class="sxs-lookup"><span data-stu-id="4065d-133">QXP</span></span>
- <span data-ttu-id="4065d-134">RAR</span><span class="sxs-lookup"><span data-stu-id="4065d-134">RAR</span></span>
- <span data-ttu-id="4065d-135">RTF</span><span class="sxs-lookup"><span data-stu-id="4065d-135">RTF</span></span>
- <span data-ttu-id="4065d-136">SVG</span><span class="sxs-lookup"><span data-stu-id="4065d-136">SVG</span></span>
- <span data-ttu-id="4065d-137">TAR</span><span class="sxs-lookup"><span data-stu-id="4065d-137">TAR</span></span>
- <span data-ttu-id="4065d-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="4065d-138">TGZ</span></span>
- <span data-ttu-id="4065d-139">TXT</span><span class="sxs-lookup"><span data-stu-id="4065d-139">TXT</span></span>
- <span data-ttu-id="4065d-140">WMV</span><span class="sxs-lookup"><span data-stu-id="4065d-140">WMV</span></span>
- <span data-ttu-id="4065d-141">XLS</span><span class="sxs-lookup"><span data-stu-id="4065d-141">XLS</span></span>
- <span data-ttu-id="4065d-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="4065d-142">XLSX</span></span>
- <span data-ttu-id="4065d-143">XML</span><span class="sxs-lookup"><span data-stu-id="4065d-143">XML</span></span>
- <span data-ttu-id="4065d-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="4065d-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="4065d-145">Lataa tiedosto palveluun</span><span class="sxs-lookup"><span data-stu-id="4065d-145">Upload a file</span></span>

<span data-ttu-id="4065d-146">Voit ladata tiedoston Commerce-sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4065d-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4065d-147">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="4065d-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="4065d-148">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="4065d-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="4065d-149">Valitse Resurssienhallinnassa vähintään yksi tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="4065d-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="4065d-150">Syötä **Lataa medianimike** -valintaikkunaan otsikon, kuvauksen ja avainsanan metatiedot tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="4065d-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="4065d-151">Jos haluat julkaista tiedostot heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4065d-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="4065d-152">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4065d-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4065d-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4065d-153">Additional resources</span></span>

[<span data-ttu-id="4065d-154">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4065d-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="4065d-155">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="4065d-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="4065d-156">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="4065d-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="4065d-157">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="4065d-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="4065d-158">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="4065d-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="4065d-159">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="4065d-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
