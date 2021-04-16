---
title: Kuvien lataaminen palveluun
description: Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799226"
---
# <a name="upload-images"></a><span data-ttu-id="5e183-103">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="5e183-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e183-104">Tässä ohjeaiheessa kerrotaan, miten kuvat ladataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="5e183-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="5e183-105">Commerce-sivuston luontiohjelman mediakirjasto sallii kuvien lataamisen yksittäin tai joukkona kansioiden avulla.</span><span class="sxs-lookup"><span data-stu-id="5e183-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="5e183-106">Lataa aina sellainen kuvaversio, jonka jonka resoluutio ja laatu ovat parhaat mahdolliset, koska kuvan kokoa muuttava osa optimoi kuvan automaattisesti eri näyttöjen ja niiden keskeytyskohtien avulla.</span><span class="sxs-lookup"><span data-stu-id="5e183-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="5e183-107">Latauksen aikana määritettävät kuvan tiedot</span><span class="sxs-lookup"><span data-stu-id="5e183-107">Image information specified during upload</span></span>

<span data-ttu-id="5e183-108">Kun lataat kuvan, seuraavat tiedot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="5e183-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="5e183-109">**Otsikko, vaihtoehtoinen teksti, kuvaus, avainsanat**: Kuvan tai kuvien metatiedot.</span><span class="sxs-lookup"><span data-stu-id="5e183-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="5e183-110">Otsikko ja vaihtoehtoinen teksti ovat pakolliset arvot.</span><span class="sxs-lookup"><span data-stu-id="5e183-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="5e183-111">**Valitse luokka**:</span><span class="sxs-lookup"><span data-stu-id="5e183-111">**Select category**:</span></span>
    - <span data-ttu-id="5e183-112">**Ei mitään**: Käytetään sähköisen kaupankäynnin tarinoiden kuvassa tai kuvissa.</span><span class="sxs-lookup"><span data-stu-id="5e183-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="5e183-113">**Tuote, luokka, asiakas, työntekijä, luettelo**: Käytetään Dynamics 365 Commercen monikanavan kuvassa tai kuvissa.</span><span class="sxs-lookup"><span data-stu-id="5e183-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="5e183-114">**Julkaise resurssit lataamisen jälkeen**: Kun tämä valintaruutu on valittu, kuva tai kuvat julkaistaan heti lataamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5e183-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="5e183-115">Kuvaresurssit, joihin on liitetty luokka, merkitään automaattisesti luokkaan avainsanana. Tämä auttaa tietyn luokan resurssien hakemisessa.</span><span class="sxs-lookup"><span data-stu-id="5e183-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="5e183-116">Monikanavan kuvien nimeämiskäytännöt</span><span class="sxs-lookup"><span data-stu-id="5e183-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="5e183-117">Jos olet määrittänyt mediakirjaston monikanavan kuvan taustalle, voit käyttää kuvaluokkia määrittäessäsi luokan, johon ladattu kuva kuuluu.</span><span class="sxs-lookup"><span data-stu-id="5e183-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="5e183-118">On olemassa myös nimeämiskäytäntö, jota on noudatettava. Se varmistaa, että kuvat haetaan oikein muissa kanavissa, kuten myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="5e183-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="5e183-119">Oletusnimeämiskäytäntö vaihtelee luokan mukaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5e183-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="5e183-120">Luettelon kuvat on nimettävä seuraavasti: "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="5e183-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="5e183-121">Luokan kuvat on nimettävä seuraavasti: "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="5e183-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="5e183-122">Asiakkaan kuvat on nimettävä seuraavasti: "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="5e183-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="5e183-123">Työntekijän kuvat on nimettävä seuraavasti: "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="5e183-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="5e183-124">Tuotekuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="5e183-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="5e183-125">001 on kuvan järjestysluku. Se voi olla 001, 002, 003, 004 tai 005</span><span class="sxs-lookup"><span data-stu-id="5e183-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="5e183-126">Tuotevariantin kuvat on nimettävä seuraavasti: "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="5e183-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="5e183-127">Esimerkki: 93039 \^ \^ 2 \^ Black \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="5e183-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="5e183-128">Kuvan lataaminen</span><span class="sxs-lookup"><span data-stu-id="5e183-128">Upload an image</span></span>

<span data-ttu-id="5e183-129">Voit ladata kuvan sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5e183-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5e183-130">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="5e183-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="5e183-131">Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="5e183-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="5e183-132">Siirry Resurssienhallinnan ikkunaan ja valitse jokin ladattava kuva. Valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="5e183-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="5e183-133">Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.</span><span class="sxs-lookup"><span data-stu-id="5e183-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="5e183-134">Syötä valinnainen kuvaus ja avainsanat. Valitse tarvittaessa luokka.</span><span class="sxs-lookup"><span data-stu-id="5e183-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="5e183-135">Jos haluat julkaista kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5e183-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="5e183-136">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e183-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="5e183-137">Kuvakansion lataaminen</span><span class="sxs-lookup"><span data-stu-id="5e183-137">Upload a folder of images</span></span>

<span data-ttu-id="5e183-138">Voit joukkoladata kuvakansion sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5e183-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="5e183-139">Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="5e183-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="5e183-140">Valitse komentopalkissa **Lataa \> Lataa kansio**.</span><span class="sxs-lookup"><span data-stu-id="5e183-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="5e183-141">Siirry Resurssienhallinnan ikkunaan ja valitse ladattava kansio. Valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="5e183-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="5e183-142">Anna **Lataa medianimikkeet** -valintaikkunaan vaihtoehtoiset avainsanat ja valitse tarvittaessa luokka.</span><span class="sxs-lookup"><span data-stu-id="5e183-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="5e183-143">Jos haluat julkaista kansion kuvat heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5e183-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="5e183-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e183-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e183-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5e183-145">Additional resources</span></span>

[<span data-ttu-id="5e183-146">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5e183-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="5e183-147">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="5e183-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="5e183-148">Lataa tiedostot</span><span class="sxs-lookup"><span data-stu-id="5e183-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="5e183-149">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="5e183-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="5e183-150">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="5e183-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="5e183-151">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5e183-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
