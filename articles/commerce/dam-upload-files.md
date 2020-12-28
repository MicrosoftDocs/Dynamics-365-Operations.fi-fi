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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4acd3bec32cdfe627f6eb33dd5dc652f7cff74a8
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594209"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="0e5b9-103">Muiden kuin kuva- ja videotiedostojen lataaminen</span><span class="sxs-lookup"><span data-stu-id="0e5b9-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e5b9-104">Tässä ohjeaiheessa kerrotaan, miten muita kuin kuva- ja videotiedostoja ladataan Microsoft Dynamics 365 Commercen sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="0e5b9-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="0e5b9-105">Overview</span></span>

<span data-ttu-id="0e5b9-106">Commerce-sivuston luontiohjelman mediakirjasto tukee sellaisten binaariresurssien lataamista, jotka eivät ole kuvia ja videoita.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="0e5b9-107">Voit esimerkiksi ladata Microsoft Excel-, Microsoft Word-, Microsoft PowerPoint- tai PDF-tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="0e5b9-108">Seuraavia asiakirjatyyppejä tuetaan:</span><span class="sxs-lookup"><span data-stu-id="0e5b9-108">The following document types are supported:</span></span>
- <span data-ttu-id="0e5b9-109">7Z</span><span class="sxs-lookup"><span data-stu-id="0e5b9-109">7Z</span></span>
- <span data-ttu-id="0e5b9-110">AVI</span><span class="sxs-lookup"><span data-stu-id="0e5b9-110">AVI</span></span>
- <span data-ttu-id="0e5b9-111">CS</span><span class="sxs-lookup"><span data-stu-id="0e5b9-111">CS</span></span>
- <span data-ttu-id="0e5b9-112">CSS</span><span class="sxs-lookup"><span data-stu-id="0e5b9-112">CSS</span></span>
- <span data-ttu-id="0e5b9-113">DOC</span><span class="sxs-lookup"><span data-stu-id="0e5b9-113">DOC</span></span>
- <span data-ttu-id="0e5b9-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="0e5b9-114">DOCX</span></span>
- <span data-ttu-id="0e5b9-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="0e5b9-115">EPUB</span></span>
- <span data-ttu-id="0e5b9-116">GIF</span><span class="sxs-lookup"><span data-stu-id="0e5b9-116">GIF</span></span>
- <span data-ttu-id="0e5b9-117">INDD</span><span class="sxs-lookup"><span data-stu-id="0e5b9-117">INDD</span></span>
- <span data-ttu-id="0e5b9-118">JAR</span><span class="sxs-lookup"><span data-stu-id="0e5b9-118">JAR</span></span>
- <span data-ttu-id="0e5b9-119">JPG</span><span class="sxs-lookup"><span data-stu-id="0e5b9-119">JPG</span></span>
- <span data-ttu-id="0e5b9-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="0e5b9-120">JPEG</span></span>
- <span data-ttu-id="0e5b9-121">JS</span><span class="sxs-lookup"><span data-stu-id="0e5b9-121">JS</span></span>
- <span data-ttu-id="0e5b9-122">MP3</span><span class="sxs-lookup"><span data-stu-id="0e5b9-122">MP3</span></span>
- <span data-ttu-id="0e5b9-123">MP4</span><span class="sxs-lookup"><span data-stu-id="0e5b9-123">MP4</span></span>
- <span data-ttu-id="0e5b9-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="0e5b9-124">MPEG</span></span>
- <span data-ttu-id="0e5b9-125">MPG</span><span class="sxs-lookup"><span data-stu-id="0e5b9-125">MPG</span></span>
- <span data-ttu-id="0e5b9-126">ODP</span><span class="sxs-lookup"><span data-stu-id="0e5b9-126">ODP</span></span>
- <span data-ttu-id="0e5b9-127">ODS</span><span class="sxs-lookup"><span data-stu-id="0e5b9-127">ODS</span></span>
- <span data-ttu-id="0e5b9-128">ODT</span><span class="sxs-lookup"><span data-stu-id="0e5b9-128">ODT</span></span>
- <span data-ttu-id="0e5b9-129">PDF</span><span class="sxs-lookup"><span data-stu-id="0e5b9-129">PDF</span></span>
- <span data-ttu-id="0e5b9-130">PNG</span><span class="sxs-lookup"><span data-stu-id="0e5b9-130">PNG</span></span>
- <span data-ttu-id="0e5b9-131">PPT</span><span class="sxs-lookup"><span data-stu-id="0e5b9-131">PPT</span></span>
- <span data-ttu-id="0e5b9-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="0e5b9-132">PPTX</span></span>
- <span data-ttu-id="0e5b9-133">PS</span><span class="sxs-lookup"><span data-stu-id="0e5b9-133">PS</span></span>
- <span data-ttu-id="0e5b9-134">QXP</span><span class="sxs-lookup"><span data-stu-id="0e5b9-134">QXP</span></span>
- <span data-ttu-id="0e5b9-135">RAR</span><span class="sxs-lookup"><span data-stu-id="0e5b9-135">RAR</span></span>
- <span data-ttu-id="0e5b9-136">RTF</span><span class="sxs-lookup"><span data-stu-id="0e5b9-136">RTF</span></span>
- <span data-ttu-id="0e5b9-137">SVG</span><span class="sxs-lookup"><span data-stu-id="0e5b9-137">SVG</span></span>
- <span data-ttu-id="0e5b9-138">TAR</span><span class="sxs-lookup"><span data-stu-id="0e5b9-138">TAR</span></span>
- <span data-ttu-id="0e5b9-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="0e5b9-139">TGZ</span></span>
- <span data-ttu-id="0e5b9-140">TXT</span><span class="sxs-lookup"><span data-stu-id="0e5b9-140">TXT</span></span>
- <span data-ttu-id="0e5b9-141">WMV</span><span class="sxs-lookup"><span data-stu-id="0e5b9-141">WMV</span></span>
- <span data-ttu-id="0e5b9-142">XLS</span><span class="sxs-lookup"><span data-stu-id="0e5b9-142">XLS</span></span>
- <span data-ttu-id="0e5b9-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="0e5b9-143">XLSX</span></span>
- <span data-ttu-id="0e5b9-144">XML</span><span class="sxs-lookup"><span data-stu-id="0e5b9-144">XML</span></span>
- <span data-ttu-id="0e5b9-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="0e5b9-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="0e5b9-146">Lataa tiedosto palveluun</span><span class="sxs-lookup"><span data-stu-id="0e5b9-146">Upload a file</span></span>

<span data-ttu-id="0e5b9-147">Voit ladata tiedoston Commerce-sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0e5b9-148">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="0e5b9-149">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="0e5b9-150">Valitse Resurssienhallinnassa vähintään yksi tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="0e5b9-151">Syötä **Lataa medianimike** -valintaikkunaan otsikon, kuvauksen ja avainsanan metatiedot tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="0e5b9-152">Jos haluat julkaista tiedostot heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="0e5b9-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e5b9-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e5b9-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0e5b9-154">Additional resources</span></span>

[<span data-ttu-id="0e5b9-155">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0e5b9-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="0e5b9-156">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="0e5b9-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="0e5b9-157">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="0e5b9-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="0e5b9-158">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="0e5b9-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="0e5b9-159">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="0e5b9-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="0e5b9-160">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0e5b9-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
