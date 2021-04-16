---
title: Videoiden lataaminen
description: Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.
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
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799202"
---
# <a name="upload-videos"></a><span data-ttu-id="9163d-103">Videoiden lataaminen</span><span class="sxs-lookup"><span data-stu-id="9163d-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9163d-104">Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="9163d-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="9163d-105">Commerce-sivuston luontiohjelman mediakirjaston avulla voit ladata videoita.</span><span class="sxs-lookup"><span data-stu-id="9163d-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="9163d-106">Lataa aina sellainen videoversio, jonka jonka bittinopeus ja resoluutio ovat parhaat mahdolliset, koska video muutetaan automaattisesti eri näyttöjen ja niiden keskeytyskohtien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="9163d-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="9163d-107">Latauksen aikana määritettävät videon tiedot</span><span class="sxs-lookup"><span data-stu-id="9163d-107">Video information specified during upload</span></span>

<span data-ttu-id="9163d-108">Kun lataat videon, seuraavat tiedot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="9163d-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="9163d-109">**Otsikko, kuvaus, avainsanat**: Videon metatiedot.</span><span class="sxs-lookup"><span data-stu-id="9163d-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="9163d-110">**Luo automaattisesti tekstitykset**: Määrittää, luodaanko videolle automaattisesti tekstitykset.</span><span class="sxs-lookup"><span data-stu-id="9163d-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="9163d-111">**Tekstitys**: Määrittää käytettävät tekstitykset.</span><span class="sxs-lookup"><span data-stu-id="9163d-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="9163d-112">**Tavallinen ääni**: Määrittää käytettävän tavallisen ääniraidan.</span><span class="sxs-lookup"><span data-stu-id="9163d-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="9163d-113">**Pikkukuva**: Määrittää videon pikkukuvan.</span><span class="sxs-lookup"><span data-stu-id="9163d-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="9163d-114">Jos tätä ei ole määritetty, se määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="9163d-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="9163d-115">**Kuvaava ääni**: Määrittää käytettävän kuvaavan ääniraidan.</span><span class="sxs-lookup"><span data-stu-id="9163d-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="9163d-116">Videon lataaminen</span><span class="sxs-lookup"><span data-stu-id="9163d-116">Upload a video</span></span>

<span data-ttu-id="9163d-117">Voit ladata videon sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9163d-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="9163d-118">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="9163d-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="9163d-119">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="9163d-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="9163d-120">Siirry Resurssienhallinnan ikkunaan ja valitse jokin ladattava video. Valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="9163d-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="9163d-121">Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="9163d-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="9163d-122">Syötä valinnainen kuvaus ja avainsanat. Valitse tarvittaessa luokka.</span><span class="sxs-lookup"><span data-stu-id="9163d-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="9163d-123">Jos haluat julkaista kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu</span><span class="sxs-lookup"><span data-stu-id="9163d-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="9163d-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9163d-124">Select **OK**.</span></span>

<span data-ttu-id="9163d-125">Jos olet lataamassa useita resurssityyppejä samanaikaisesti (esimerkiksi kuvia ja videoita), **Lataa medianimike** -valintaikkunassa voit vain määrittää avainsanoja. Tiedostot tulee julkaista heti lataamisen jälkeen ja samoin määrittää, luodaanko tekstitykset automaattisesti videotiedostoille.</span><span class="sxs-lookup"><span data-stu-id="9163d-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="9163d-126">Kaikki resurssit jakavat samat avainsanat.</span><span class="sxs-lookup"><span data-stu-id="9163d-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9163d-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9163d-127">Additional resources</span></span>

[<span data-ttu-id="9163d-128">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9163d-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="9163d-129">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="9163d-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="9163d-130">Lataa tiedostot</span><span class="sxs-lookup"><span data-stu-id="9163d-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="9163d-131">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="9163d-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="9163d-132">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="9163d-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="9163d-133">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="9163d-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
