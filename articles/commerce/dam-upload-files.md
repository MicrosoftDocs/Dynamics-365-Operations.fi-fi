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
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097006"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="bdb8b-103">Muiden kuin kuva- ja videotiedostojen lataaminen</span><span class="sxs-lookup"><span data-stu-id="bdb8b-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bdb8b-104">Tässä ohjeaiheessa kerrotaan, miten muita kuin kuva- ja videotiedostoja ladataan Microsoft Dynamics 365 Commercen sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="bdb8b-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="bdb8b-105">Overview</span></span>

<span data-ttu-id="bdb8b-106">Commerce-sivuston luontiohjelman mediakirjasto tukee sellaisten binaariresurssien lataamista, jotka eivät ole kuvia ja videoita.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="bdb8b-107">Voit esimerkiksi ladata Microsoft Excel-, Microsoft Word-, Microsoft PowerPoint- tai PDF-tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="bdb8b-108">Seuraavia asiakirjatyyppejä tuetaan:</span><span class="sxs-lookup"><span data-stu-id="bdb8b-108">The following document types are supported:</span></span>
- <span data-ttu-id="bdb8b-109">7Z</span><span class="sxs-lookup"><span data-stu-id="bdb8b-109">7Z</span></span>
- <span data-ttu-id="bdb8b-110">AVI</span><span class="sxs-lookup"><span data-stu-id="bdb8b-110">AVI</span></span>
- <span data-ttu-id="bdb8b-111">CS</span><span class="sxs-lookup"><span data-stu-id="bdb8b-111">CS</span></span>
- <span data-ttu-id="bdb8b-112">CSS</span><span class="sxs-lookup"><span data-stu-id="bdb8b-112">CSS</span></span>
- <span data-ttu-id="bdb8b-113">DOC</span><span class="sxs-lookup"><span data-stu-id="bdb8b-113">DOC</span></span>
- <span data-ttu-id="bdb8b-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="bdb8b-114">DOCX</span></span>
- <span data-ttu-id="bdb8b-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="bdb8b-115">EPUB</span></span>
- <span data-ttu-id="bdb8b-116">GIF</span><span class="sxs-lookup"><span data-stu-id="bdb8b-116">GIF</span></span>
- <span data-ttu-id="bdb8b-117">INDD</span><span class="sxs-lookup"><span data-stu-id="bdb8b-117">INDD</span></span>
- <span data-ttu-id="bdb8b-118">JAR</span><span class="sxs-lookup"><span data-stu-id="bdb8b-118">JAR</span></span>
- <span data-ttu-id="bdb8b-119">JPG</span><span class="sxs-lookup"><span data-stu-id="bdb8b-119">JPG</span></span>
- <span data-ttu-id="bdb8b-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="bdb8b-120">JPEG</span></span>
- <span data-ttu-id="bdb8b-121">JS</span><span class="sxs-lookup"><span data-stu-id="bdb8b-121">JS</span></span>
- <span data-ttu-id="bdb8b-122">MP3</span><span class="sxs-lookup"><span data-stu-id="bdb8b-122">MP3</span></span>
- <span data-ttu-id="bdb8b-123">MP4</span><span class="sxs-lookup"><span data-stu-id="bdb8b-123">MP4</span></span>
- <span data-ttu-id="bdb8b-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="bdb8b-124">MPEG</span></span>
- <span data-ttu-id="bdb8b-125">MPG</span><span class="sxs-lookup"><span data-stu-id="bdb8b-125">MPG</span></span>
- <span data-ttu-id="bdb8b-126">ODP</span><span class="sxs-lookup"><span data-stu-id="bdb8b-126">ODP</span></span>
- <span data-ttu-id="bdb8b-127">ODS</span><span class="sxs-lookup"><span data-stu-id="bdb8b-127">ODS</span></span>
- <span data-ttu-id="bdb8b-128">ODT</span><span class="sxs-lookup"><span data-stu-id="bdb8b-128">ODT</span></span>
- <span data-ttu-id="bdb8b-129">PDF</span><span class="sxs-lookup"><span data-stu-id="bdb8b-129">PDF</span></span>
- <span data-ttu-id="bdb8b-130">PNG</span><span class="sxs-lookup"><span data-stu-id="bdb8b-130">PNG</span></span>
- <span data-ttu-id="bdb8b-131">PPT</span><span class="sxs-lookup"><span data-stu-id="bdb8b-131">PPT</span></span>
- <span data-ttu-id="bdb8b-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="bdb8b-132">PPTX</span></span>
- <span data-ttu-id="bdb8b-133">PS</span><span class="sxs-lookup"><span data-stu-id="bdb8b-133">PS</span></span>
- <span data-ttu-id="bdb8b-134">QXP</span><span class="sxs-lookup"><span data-stu-id="bdb8b-134">QXP</span></span>
- <span data-ttu-id="bdb8b-135">RAR</span><span class="sxs-lookup"><span data-stu-id="bdb8b-135">RAR</span></span>
- <span data-ttu-id="bdb8b-136">RTF</span><span class="sxs-lookup"><span data-stu-id="bdb8b-136">RTF</span></span>
- <span data-ttu-id="bdb8b-137">SVG</span><span class="sxs-lookup"><span data-stu-id="bdb8b-137">SVG</span></span>
- <span data-ttu-id="bdb8b-138">TAR</span><span class="sxs-lookup"><span data-stu-id="bdb8b-138">TAR</span></span>
- <span data-ttu-id="bdb8b-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="bdb8b-139">TGZ</span></span>
- <span data-ttu-id="bdb8b-140">TXT</span><span class="sxs-lookup"><span data-stu-id="bdb8b-140">TXT</span></span>
- <span data-ttu-id="bdb8b-141">WMV</span><span class="sxs-lookup"><span data-stu-id="bdb8b-141">WMV</span></span>
- <span data-ttu-id="bdb8b-142">XLS</span><span class="sxs-lookup"><span data-stu-id="bdb8b-142">XLS</span></span>
- <span data-ttu-id="bdb8b-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="bdb8b-143">XLSX</span></span>
- <span data-ttu-id="bdb8b-144">XML</span><span class="sxs-lookup"><span data-stu-id="bdb8b-144">XML</span></span>
- <span data-ttu-id="bdb8b-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="bdb8b-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="bdb8b-146">Lataa tiedosto palveluun</span><span class="sxs-lookup"><span data-stu-id="bdb8b-146">Upload a file</span></span>

<span data-ttu-id="bdb8b-147">Voit ladata tiedoston Commerce-sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bdb8b-148">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="bdb8b-149">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="bdb8b-150">Valitse Resurssienhallinnassa vähintään yksi tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="bdb8b-151">Syötä **Lataa medianimike** -valintaikkunaan otsikon, kuvauksen ja avainsanan metatiedot tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="bdb8b-152">Jos haluat julkaista tiedostot heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="bdb8b-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdb8b-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdb8b-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bdb8b-154">Additional resources</span></span>

[<span data-ttu-id="bdb8b-155">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bdb8b-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="bdb8b-156">Lataa kuvat</span><span class="sxs-lookup"><span data-stu-id="bdb8b-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="bdb8b-157">Lataa video</span><span class="sxs-lookup"><span data-stu-id="bdb8b-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="bdb8b-158">Rajaa kuvat</span><span class="sxs-lookup"><span data-stu-id="bdb8b-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="bdb8b-159">Mukauta kuvan keskipisteitä</span><span class="sxs-lookup"><span data-stu-id="bdb8b-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
