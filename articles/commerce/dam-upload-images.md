---
title: Lataa kuvat
description: Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
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
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594281"
---
# <a name="upload-images"></a><span data-ttu-id="09b14-103">Lataa kuvat</span><span class="sxs-lookup"><span data-stu-id="09b14-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09b14-104">Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="09b14-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="09b14-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="09b14-105">Overview</span></span>

<span data-ttu-id="09b14-106">Commerce-sivuston luontiohjelman mediakirjasto sallii kuvien lataamisen yksittäin tai joukkona kansioiden avulla.</span><span class="sxs-lookup"><span data-stu-id="09b14-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="09b14-107">Lataa aina sellainen kuvaversio, jonka jonka resoluutio ja laatu ovat parhaat mahdolliset, koska kuvan kokoa muuttava osa optimoi kuvan automaattisesti eri näyttöjen ja niiden keskeytyskohtien avulla.</span><span class="sxs-lookup"><span data-stu-id="09b14-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="09b14-108">Latauksen aikana määritettävät kuvan tiedot</span><span class="sxs-lookup"><span data-stu-id="09b14-108">Image information specified during upload</span></span>

<span data-ttu-id="09b14-109">Kun lataat kuvan, seuraavat tiedot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="09b14-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="09b14-110">**Otsikko, vaihtoehtoinen teksti, kuvaus, avainsanat**: Kuvan tai kuvien metatiedot.</span><span class="sxs-lookup"><span data-stu-id="09b14-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="09b14-111">Otsikko ja vaihtoehtoinen teksti ovat pakolliset arvot.</span><span class="sxs-lookup"><span data-stu-id="09b14-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="09b14-112">**Valitse luokka**:</span><span class="sxs-lookup"><span data-stu-id="09b14-112">**Select category**:</span></span>
    - <span data-ttu-id="09b14-113">**Ei mitään**: Käytetään sähköisen kaupankäynnin tarinoiden kuvassa tai kuvissa.</span><span class="sxs-lookup"><span data-stu-id="09b14-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="09b14-114">**Tuote, luokka, asiakas, työntekijä, luettelo**: Käytetään Dynamics 365 Commercen monikanavan kuvassa tai kuvissa.</span><span class="sxs-lookup"><span data-stu-id="09b14-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="09b14-115">**Julkaise resurssit lataamisen jälkeen**: Kun tämä valintaruutu on valittu, kuva tai kuvat julkaistaan heti lataamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="09b14-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="09b14-116">Kuvaresurssit, joihin on liitetty luokka, merkitään automaattisesti luokkaan avainsanana. Tämä auttaa tietyn luokan resurssien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="09b14-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="09b14-117">Monikanavan kuvien nimeämiskäytännöt</span><span class="sxs-lookup"><span data-stu-id="09b14-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="09b14-118">Jos olet määrittänyt mediakirjaston monikanavan kuvan taustalle, voit käyttää kuvaluokkia määrittäessäsi luokan, johon ladattu kuva kuuluu.</span><span class="sxs-lookup"><span data-stu-id="09b14-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="09b14-119">On olemassa myös nimeämiskäytäntö, jota on noudatettava. Se varmistaa, että kuvat haetaan oikein muissa kanavissa, kuten myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="09b14-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="09b14-120">Oletusnimeämiskäytäntö vaihtelee luokan mukaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="09b14-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="09b14-121">Luettelon kuvat on nimettävä seuraavasti: "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="09b14-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="09b14-122">Luokan kuvat on nimettävä seuraavasti: "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="09b14-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="09b14-123">Asiakkaan kuvat on nimettävä seuraavasti: "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="09b14-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="09b14-124">Työntekijän kuvat on nimettävä seuraavasti: "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="09b14-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="09b14-125">Tuotekuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="09b14-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="09b14-126">001 on kuvan järjestysluku. Se voi olla 001, 002, 003, 004 tai 005</span><span class="sxs-lookup"><span data-stu-id="09b14-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="09b14-127">Tuotevariantin kuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="09b14-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="09b14-128">Kuvan lataaminen</span><span class="sxs-lookup"><span data-stu-id="09b14-128">Upload an image</span></span>

<span data-ttu-id="09b14-129">Voit ladata kuvan sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="09b14-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="09b14-130">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="09b14-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="09b14-131">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="09b14-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="09b14-132">Siirry Resurssienhallinnan ikkunaan ja valitse jokin ladattava kuva. Valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="09b14-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="09b14-133">Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="09b14-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="09b14-134">Syötä valinnainen kuvaus ja avainsanat. Valitse tarvittaessa luokka.</span><span class="sxs-lookup"><span data-stu-id="09b14-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="09b14-135">Jos haluat julkaista kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="09b14-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="09b14-136">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09b14-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="09b14-137">Kuvakansion lataaminen</span><span class="sxs-lookup"><span data-stu-id="09b14-137">Upload a folder of images</span></span>

<span data-ttu-id="09b14-138">Voit joukkoladata kuvakansion sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="09b14-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="09b14-139">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="09b14-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="09b14-140">Valitse komentopalkissa **Lataa \> Lataa kansio**.</span><span class="sxs-lookup"><span data-stu-id="09b14-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="09b14-141">Siirry Resurssienhallinnan ikkunaan ja valitse ladattava kansio. Valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="09b14-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="09b14-142">Anna **Lataa medianimikkeet** -valintaikkunaan vaihtoehtoiset avainsanat ja valitse tarvittaessa luokka.</span><span class="sxs-lookup"><span data-stu-id="09b14-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="09b14-143">Jos haluat julkaista kansion kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="09b14-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="09b14-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="09b14-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09b14-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="09b14-145">Additional resources</span></span>

[<span data-ttu-id="09b14-146">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="09b14-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="09b14-147">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="09b14-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="09b14-148">Lataa tiedostot</span><span class="sxs-lookup"><span data-stu-id="09b14-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="09b14-149">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="09b14-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="09b14-150">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="09b14-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="09b14-151">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="09b14-151">Upload and serve static files</span></span>](upload-serve-static-files.md)
