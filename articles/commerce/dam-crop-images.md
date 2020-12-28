---
title: Kuvien rajaaminen
description: Tässä ohjeaiheessa kerrotaan, miten kuvat rajataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: a8f52c22a57d465ce1c2bedac6e8f13db3e856c0
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594475"
---
# <a name="crop-images"></a><span data-ttu-id="d4e3e-103">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="d4e3e-103">Crop images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4e3e-104">Tässä ohjeaiheessa kerrotaan, miten kuvat rajataan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-104">This topic describes how to crop images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="d4e3e-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d4e3e-105">Overview</span></span>

<span data-ttu-id="d4e3e-106">Commerce-sivuston luontiohjelman mediakirjaston avulla voit rajata kuvat ja optimoida ne eri moduulityyppejä ja näyttöjä varten.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-106">The Commerce site builder Media Library allows you to crop images to optimize them for different module types and viewports.</span></span>

## <a name="crop-an-image"></a><span data-ttu-id="d4e3e-107">Kuvan rajaaminen</span><span class="sxs-lookup"><span data-stu-id="d4e3e-107">Crop an image</span></span>

<span data-ttu-id="d4e3e-108">Voit rajata kuvan sivuston luontiohjelmaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-108">To crop an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d4e3e-109">Valitse Commerce-sivuston luontiohjelman vasemmanpuoleisessa ruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-109">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="d4e3e-110">Valitse pääikkunassa kuva, jota haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-110">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="d4e3e-111">Valitse komentopalkissa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-111">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="d4e3e-112">Valitse kuva ja syötä **Muokkaustila**.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-112">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="d4e3e-113">Valitse **Muokkaustila**-kohdassa **Muokkaa näkymää moduulin mukaan**.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-113">Under **Edit Mode**, select **Edit View by Module**.</span></span>
1. <span data-ttu-id="d4e3e-114">Valitse avattavassa **Moduuli**-valikossa moduulityyppi.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-114">From the **Module** drop-down menu, select the module type.</span></span>
1. <span data-ttu-id="d4e3e-115">Valitse avattavassa **Näkymätyyppi**-valikossa näkymätyyppi.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-115">From the **View type** drop-down menu, select the view type.</span></span>
1. <span data-ttu-id="d4e3e-116">Valitse avattavassa **Sijoittelu**-luettelossa kuvan sijoittelu.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-116">From the **Placement** drop-down menu, select the image placement.</span></span>
1. <span data-ttu-id="d4e3e-117">Valitse avattavassa **Näyttö**-valikossa näytön koko.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-117">From the **Viewport** drop-down menu, select the viewport size.</span></span>
1. <span data-ttu-id="d4e3e-118">Kuva peittä alueen, joka edustaa rajausaluetta.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-118">The image is overlaid with the area representing the crop region.</span></span> <span data-ttu-id="d4e3e-119">Siirrä rajausaluetta ja muuta sen kokoa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-119">Move and resize the crop region as needed.</span></span> <span data-ttu-id="d4e3e-120">Kuvasuhdetta ylläpidetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-120">The aspect ratio will be maintained automatically.</span></span>
1. <span data-ttu-id="d4e3e-121">Kun olet valmis, valitse komentopalkissa **Tallenna** ja valitse sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-121">When you're done, on the command bar, select **Save**, and then select **Finish editing**.</span></span> 

<span data-ttu-id="d4e3e-122">Kun mukautettu rajaus on tehty, kuvien muutokset tulevat voimaan lähes välittömästi.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-122">After custom cropping is completed, image modifications will take effect almost immediately.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4e3e-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d4e3e-123">Additional resources</span></span>

[<span data-ttu-id="d4e3e-124">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d4e3e-124">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="d4e3e-125">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="d4e3e-125">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="d4e3e-126">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="d4e3e-126">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="d4e3e-127">Lataa tiedostot</span><span class="sxs-lookup"><span data-stu-id="d4e3e-127">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="d4e3e-128">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="d4e3e-128">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="d4e3e-129">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="d4e3e-129">Upload and serve static files</span></span>](upload-serve-static-files.md)
