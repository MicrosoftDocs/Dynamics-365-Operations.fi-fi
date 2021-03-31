---
title: Kuvan keskipisteiden mukauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten kuvan keskipisteitä mukautetaan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: fca209c9827192f50c2f1a5bd9e78146214e1e0e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222558"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="ba423-103">Kuvien tarkennuspisteiden mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="ba423-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba423-104">Tässä ohjeaiheessa kerrotaan, miten kuvan keskipisteitä mukautetaan Microsoft Dynamics 365 Commerce -sivuston luontiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="ba423-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="ba423-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="ba423-105">Overview</span></span>

<span data-ttu-id="ba423-106">Kun kuva ladataan Commerce-sivuston luontiohjelman mediakirjastoon, järjestelmä yrittää määrittää kuvan keskipisteen.</span><span class="sxs-lookup"><span data-stu-id="ba423-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="ba423-107">Jos kuvassa on henkilö, järjestelmä määrittää oletusarvoisesti keskipisteeksi henkilön kasvot.</span><span class="sxs-lookup"><span data-stu-id="ba423-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="ba423-108">Useimmissa tapauksissa automaattisesti määritetyt keskipisteet toimivat hyvin näytöissä. Joskus on ehkä tarpeen muokata keskipistettä ja varmistaa, että kuvan tietty osa on aina näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="ba423-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="ba423-109">Kuvan mukautetun keskipisteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ba423-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="ba423-110">Voit määrittää kuvalle mukautetun keskipisteen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ba423-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="ba423-111">Valitse Commerce-sivuston luontiohjelman vasemmanpuoleisessa ruudussa **Mediakirjasto**.</span><span class="sxs-lookup"><span data-stu-id="ba423-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="ba423-112">Valitse pääikkunassa kuva, jota haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="ba423-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="ba423-113">Valitse komentopalkissa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ba423-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="ba423-114">Valitse kuva ja syötä **Muokkaustila**.</span><span class="sxs-lookup"><span data-stu-id="ba423-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="ba423-115">Valitse **Muokkaustila**-kohdassa **Muuta keskipistettä**.</span><span class="sxs-lookup"><span data-stu-id="ba423-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="ba423-116">Kuvan päälle ilmestyy pyöreä keskipiste.</span><span class="sxs-lookup"><span data-stu-id="ba423-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="ba423-117">Valitse keskipisteen ohjausobjekti, joka siirretään haluttuun keskipisteeseen.</span><span class="sxs-lookup"><span data-stu-id="ba423-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="ba423-118">Kun olet valmis, valitse komentopalkissa **Tallenna** ja valitse sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="ba423-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba423-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ba423-119">Additional resources</span></span>

[<span data-ttu-id="ba423-120">Digitaalisten resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ba423-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ba423-121">Kuvien lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="ba423-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ba423-122">Videon lataaminen palveluun</span><span class="sxs-lookup"><span data-stu-id="ba423-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="ba423-123">Lataa tiedostot</span><span class="sxs-lookup"><span data-stu-id="ba423-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="ba423-124">Kuvien rajaaminen</span><span class="sxs-lookup"><span data-stu-id="ba423-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="ba423-125">Staattisten tiedostojen lataaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ba423-125">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]