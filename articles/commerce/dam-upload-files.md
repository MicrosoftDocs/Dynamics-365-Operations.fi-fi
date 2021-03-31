---
title: Muiden kuin kuva- ja videotiedostojen lataaminen
description: Tässä ohjeaiheessa kerrotaan, miten muita kuin kuva- ja videobinaaritiedostoja ladataan Microsoft Dynamics 365 Commercen sivuston luontiohjelmassa.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222534"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="2e948-103">Muiden tiedostojen kuin kuvien ja videoiden lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="2e948-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e948-104">Tässä ohjeaiheessa kerrotaan, miten muita kuin kuva- ja videotiedostoja ladataan Microsoft Dynamics 365 Commercen sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="2e948-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="2e948-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="2e948-105">Overview</span></span>

<span data-ttu-id="2e948-106">Commerce-sivuston luontiohjelman mediakirjasto tukee sellaisten binaariresurssien lataamista, jotka eivät ole kuvia ja videoita.</span><span class="sxs-lookup"><span data-stu-id="2e948-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="2e948-107">Voit esimerkiksi ladata Microsoft Excel-, Microsoft Word-, Microsoft PowerPoint- tai PDF-tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="2e948-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="2e948-108">Seuraavia asiakirjatyyppejä tuetaan:</span><span class="sxs-lookup"><span data-stu-id="2e948-108">The following document types are supported:</span></span>
- <span data-ttu-id="2e948-109">7Z</span><span class="sxs-lookup"><span data-stu-id="2e948-109">7Z</span></span>
- <span data-ttu-id="2e948-110">AVI</span><span class="sxs-lookup"><span data-stu-id="2e948-110">AVI</span></span>
- <span data-ttu-id="2e948-111">CS</span><span class="sxs-lookup"><span data-stu-id="2e948-111">CS</span></span>
- <span data-ttu-id="2e948-112">CSS</span><span class="sxs-lookup"><span data-stu-id="2e948-112">CSS</span></span>
- <span data-ttu-id="2e948-113">DOC</span><span class="sxs-lookup"><span data-stu-id="2e948-113">DOC</span></span>
- <span data-ttu-id="2e948-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="2e948-114">DOCX</span></span>
- <span data-ttu-id="2e948-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="2e948-115">EPUB</span></span>
- <span data-ttu-id="2e948-116">GIF</span><span class="sxs-lookup"><span data-stu-id="2e948-116">GIF</span></span>
- <span data-ttu-id="2e948-117">INDD</span><span class="sxs-lookup"><span data-stu-id="2e948-117">INDD</span></span>
- <span data-ttu-id="2e948-118">JAR</span><span class="sxs-lookup"><span data-stu-id="2e948-118">JAR</span></span>
- <span data-ttu-id="2e948-119">JPG</span><span class="sxs-lookup"><span data-stu-id="2e948-119">JPG</span></span>
- <span data-ttu-id="2e948-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="2e948-120">JPEG</span></span>
- <span data-ttu-id="2e948-121">JS</span><span class="sxs-lookup"><span data-stu-id="2e948-121">JS</span></span>
- <span data-ttu-id="2e948-122">MP3</span><span class="sxs-lookup"><span data-stu-id="2e948-122">MP3</span></span>
- <span data-ttu-id="2e948-123">MP4</span><span class="sxs-lookup"><span data-stu-id="2e948-123">MP4</span></span>
- <span data-ttu-id="2e948-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="2e948-124">MPEG</span></span>
- <span data-ttu-id="2e948-125">MPG</span><span class="sxs-lookup"><span data-stu-id="2e948-125">MPG</span></span>
- <span data-ttu-id="2e948-126">ODP</span><span class="sxs-lookup"><span data-stu-id="2e948-126">ODP</span></span>
- <span data-ttu-id="2e948-127">ODS</span><span class="sxs-lookup"><span data-stu-id="2e948-127">ODS</span></span>
- <span data-ttu-id="2e948-128">ODT</span><span class="sxs-lookup"><span data-stu-id="2e948-128">ODT</span></span>
- <span data-ttu-id="2e948-129">PDF</span><span class="sxs-lookup"><span data-stu-id="2e948-129">PDF</span></span>
- <span data-ttu-id="2e948-130">PNG</span><span class="sxs-lookup"><span data-stu-id="2e948-130">PNG</span></span>
- <span data-ttu-id="2e948-131">PPT</span><span class="sxs-lookup"><span data-stu-id="2e948-131">PPT</span></span>
- <span data-ttu-id="2e948-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="2e948-132">PPTX</span></span>
- <span data-ttu-id="2e948-133">PS</span><span class="sxs-lookup"><span data-stu-id="2e948-133">PS</span></span>
- <span data-ttu-id="2e948-134">QXP</span><span class="sxs-lookup"><span data-stu-id="2e948-134">QXP</span></span>
- <span data-ttu-id="2e948-135">RAR</span><span class="sxs-lookup"><span data-stu-id="2e948-135">RAR</span></span>
- <span data-ttu-id="2e948-136">RTF</span><span class="sxs-lookup"><span data-stu-id="2e948-136">RTF</span></span>
- <span data-ttu-id="2e948-137">SVG</span><span class="sxs-lookup"><span data-stu-id="2e948-137">SVG</span></span>
- <span data-ttu-id="2e948-138">TAR</span><span class="sxs-lookup"><span data-stu-id="2e948-138">TAR</span></span>
- <span data-ttu-id="2e948-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="2e948-139">TGZ</span></span>
- <span data-ttu-id="2e948-140">TXT</span><span class="sxs-lookup"><span data-stu-id="2e948-140">TXT</span></span>
- <span data-ttu-id="2e948-141">WMV</span><span class="sxs-lookup"><span data-stu-id="2e948-141">WMV</span></span>
- <span data-ttu-id="2e948-142">XLS</span><span class="sxs-lookup"><span data-stu-id="2e948-142">XLS</span></span>
- <span data-ttu-id="2e948-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="2e948-143">XLSX</span></span>
- <span data-ttu-id="2e948-144">XML</span><span class="sxs-lookup"><span data-stu-id="2e948-144">XML</span></span>
- <span data-ttu-id="2e948-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="2e948-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="2e948-146">Lataa tiedosto palveluun</span><span class="sxs-lookup"><span data-stu-id="2e948-146">Upload a file</span></span>

<span data-ttu-id="2e948-147">Voit ladata tiedoston Commerce-sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2e948-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e948-148">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="2e948-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="2e948-149">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="2e948-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="2e948-150">Valitse Resurssienhallinnassa vähintään yksi tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="2e948-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="2e948-151">Syötä **Lataa medianimike** -valintaikkunaan otsikon, kuvauksen ja avainsanan metatiedot tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2e948-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="2e948-152">Jos haluat julkaista tiedostot heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2e948-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="2e948-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e948-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e948-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2e948-154">Additional resources</span></span>

[<span data-ttu-id="2e948-155">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2e948-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="2e948-156">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="2e948-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="2e948-157">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="2e948-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="2e948-158">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="2e948-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="2e948-159">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="2e948-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="2e948-160">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2e948-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]