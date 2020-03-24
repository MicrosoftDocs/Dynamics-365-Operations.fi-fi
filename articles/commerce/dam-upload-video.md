---
title: Videoiden lataaminen
description: Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
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
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097009"
---
# <a name="upload-videos"></a><span data-ttu-id="09147-103">Videoiden lataaminen</span><span class="sxs-lookup"><span data-stu-id="09147-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09147-104">Tässä ohjeaiheessa kerrotaan, miten videot ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="09147-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="09147-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="09147-105">Overview</span></span>

<span data-ttu-id="09147-106">Commerce-sivuston luontiohjelman mediakirjaston avulla voit ladata videoita.</span><span class="sxs-lookup"><span data-stu-id="09147-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="09147-107">Lataa aina sellainen videoversio, jonka jonka bittinopeus ja resoluutio ovat parhaat mahdolliset, koska video muutetaan automaattisesti eri näyttöjen ja niiden keskeytyskohtien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="09147-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="09147-108">Latauksen aikana määritettävät videon tiedot</span><span class="sxs-lookup"><span data-stu-id="09147-108">Video information specified during upload</span></span>

<span data-ttu-id="09147-109">Kun lataat videon, seuraavat tiedot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="09147-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="09147-110">**Otsikko, kuvaus, avainsanat**: Videon metatiedot.</span><span class="sxs-lookup"><span data-stu-id="09147-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="09147-111">**Luo automaattisesti tekstitykset**: Määrittää, luodaanko videolle automaattisesti tekstitykset.</span><span class="sxs-lookup"><span data-stu-id="09147-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="09147-112">**Tekstitys**: Määrittää käytettävät tekstitykset.</span><span class="sxs-lookup"><span data-stu-id="09147-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="09147-113">**Tavallinen ääni**: Määrittää käytettävän tavallisen ääniraidan.</span><span class="sxs-lookup"><span data-stu-id="09147-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="09147-114">**Pikkukuva**: Määrittää videon pikkukuvan.</span><span class="sxs-lookup"><span data-stu-id="09147-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="09147-115">Jos tätä ei ole määritetty, se määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="09147-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="09147-116">**Kuvaava ääni**: Määrittää käytettävän kuvaavan ääniraidan.</span><span class="sxs-lookup"><span data-stu-id="09147-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="09147-117">Videon lataaminen</span><span class="sxs-lookup"><span data-stu-id="09147-117">Upload a video</span></span>

<span data-ttu-id="09147-118">Voit ladata videon sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="09147-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="09147-119">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="09147-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="09147-120">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="09147-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="09147-121">Siirry Resurssienhallinnan ikkunaan ja valitse jokin ladattava video. Valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="09147-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="09147-122">Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="09147-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="09147-123">Syötä valinnainen kuvaus ja avainsanat. Valitse tarvittaessa luokka.</span><span class="sxs-lookup"><span data-stu-id="09147-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="09147-124">Jos haluat julkaista kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu</span><span class="sxs-lookup"><span data-stu-id="09147-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="09147-125">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09147-125">Select **OK**.</span></span>

<span data-ttu-id="09147-126">Jos olet lataamassa useita resurssityyppejä samanaikaisesti (esimerkiksi kuvia ja videoita), **Lataa medianimike** -valintaikkunassa voit vain määrittää avainsanoja. Tiedostot tulee julkaista heti lataamisen jälkeen ja samoin määrittää, luodaanko tekstitykset automaattisesti videotiedostoille.</span><span class="sxs-lookup"><span data-stu-id="09147-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="09147-127">Kaikki resurssit jakavat samat avainsanat.</span><span class="sxs-lookup"><span data-stu-id="09147-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09147-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="09147-128">Additional resources</span></span>

[<span data-ttu-id="09147-129">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="09147-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="09147-130">Lataa kuvat</span><span class="sxs-lookup"><span data-stu-id="09147-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="09147-131">Lataa tiedostot</span><span class="sxs-lookup"><span data-stu-id="09147-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="09147-132">Rajaa kuvat</span><span class="sxs-lookup"><span data-stu-id="09147-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="09147-133">Mukauta kuvan keskipisteitä</span><span class="sxs-lookup"><span data-stu-id="09147-133">Customize image focal points</span></span>](dam-custom-focal-point.md)
