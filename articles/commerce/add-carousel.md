---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785234"
---
# <a name="carousel-module"></a><span data-ttu-id="912ef-103">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="912ef-104">Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="912ef-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="912ef-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="912ef-105">Overview</span></span>

<span data-ttu-id="912ef-106">Karusellimoduulia käytetään useiden kampanjanimikkeiden sijoittamisessa karuselliin, jota asiakkaat voivat selata.</span><span class="sxs-lookup"><span data-stu-id="912ef-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="912ef-107">Se on erityinen säilömoduuli, joka isännöi muita moduuleja.</span><span class="sxs-lookup"><span data-stu-id="912ef-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="912ef-108">Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="912ef-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="912ef-109">Voit lisätä hero-ja ominaisuusmoduuleja karusellimoduulin sisälle.</span><span class="sxs-lookup"><span data-stu-id="912ef-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="912ef-110">Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.</span><span class="sxs-lookup"><span data-stu-id="912ef-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="912ef-111">Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista</span><span class="sxs-lookup"><span data-stu-id="912ef-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="912ef-112">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="912ef-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="912ef-113">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="912ef-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="912ef-114">Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.</span><span class="sxs-lookup"><span data-stu-id="912ef-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="912ef-115">Karusellimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="912ef-115">Carousel module properties</span></span>

| <span data-ttu-id="912ef-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="912ef-116">Property name</span></span>             | <span data-ttu-id="912ef-117">Arvo</span><span class="sxs-lookup"><span data-stu-id="912ef-117">Value</span></span>                                | <span data-ttu-id="912ef-118">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="912ef-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="912ef-119">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="912ef-119">Autoplay</span></span>                  | <span data-ttu-id="912ef-120">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="912ef-120">**True** or **False**</span></span>                | <span data-ttu-id="912ef-121">Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="912ef-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="912ef-122">Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla.</span><span class="sxs-lookup"><span data-stu-id="912ef-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="912ef-123">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="912ef-123">Slide transition interval</span></span> | <span data-ttu-id="912ef-124">Arvo sekunteina</span><span class="sxs-lookup"><span data-stu-id="912ef-124">A value in seconds</span></span>                   | <span data-ttu-id="912ef-125">Nimikkeiden välisten siirtojen aikaväli.</span><span class="sxs-lookup"><span data-stu-id="912ef-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="912ef-126">Siirtymän animointi</span><span class="sxs-lookup"><span data-stu-id="912ef-126">Transition animation</span></span>      | <span data-ttu-id="912ef-127">**Dia** tai **häivytys**</span><span class="sxs-lookup"><span data-stu-id="912ef-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="912ef-128">Siirtymätehoste.</span><span class="sxs-lookup"><span data-stu-id="912ef-128">The transition effect.</span></span> |
| <span data-ttu-id="912ef-129">Leveys</span><span class="sxs-lookup"><span data-stu-id="912ef-129">Width</span></span>                     | <span data-ttu-id="912ef-130">**Sisällytä säilöön** tai **Täytä näyttö**</span><span class="sxs-lookup"><span data-stu-id="912ef-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="912ef-131">Jos arvoksi on määritetty **Sisällytä säilöön** karusellin sisällä olevat nimikkeet ovat korkeintaan karusellin levyisiä.</span><span class="sxs-lookup"><span data-stu-id="912ef-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="912ef-132">Jos arvoksi on määritetty **Täytä näyttö**, karusellin leveys ei rajoita leveyttä, vaan nimikkeet voivat olla koko näytön levyisiä.</span><span class="sxs-lookup"><span data-stu-id="912ef-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="912ef-133">Voit muuttaa arvoa halutun asettelun saavuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="912ef-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="912ef-134">Karusellimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="912ef-134">Add a carousel module to a page</span></span>

<span data-ttu-id="912ef-135">Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="912ef-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="912ef-136">Luo sivumalli, jonka nimi on **Karusellimalli**.</span><span class="sxs-lookup"><span data-stu-id="912ef-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="912ef-137">Lisää karusellimoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="912ef-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="912ef-138">Lisää hero-moduuli karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="912ef-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="912ef-139">Lisää ominaisuusmoduuli karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="912ef-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="912ef-140">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="912ef-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="912ef-141">Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.</span><span class="sxs-lookup"><span data-stu-id="912ef-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="912ef-142">Lisää karusellimoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="912ef-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="912ef-143">Määritä karusellimoduulin **Leveys**-ominaisuudeksi **Täytä näyttö**.</span><span class="sxs-lookup"><span data-stu-id="912ef-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="912ef-144">Määritä **Siirtymän animointi** -ominaisuuden arvoksi **Dia**.</span><span class="sxs-lookup"><span data-stu-id="912ef-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="912ef-145">Lisää hero-moduuli karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="912ef-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="912ef-146">Lisää hero-moduuliin kuva ja otsikko ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="912ef-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="912ef-147">Lisää ominaisuusmoduuli karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="912ef-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="912ef-148">Lisää ominaisuusmoduuliin kuva, otsikko ja tekstikappale.</span><span class="sxs-lookup"><span data-stu-id="912ef-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="912ef-149">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="912ef-149">Save and preview the page.</span></span> <span data-ttu-id="912ef-150">Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli).</span><span class="sxs-lookup"><span data-stu-id="912ef-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="912ef-151">Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="912ef-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="912ef-152">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="912ef-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="912ef-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="912ef-153">Additional resources</span></span>

[<span data-ttu-id="912ef-154">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="912ef-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="912ef-155">Hälytysmoduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="912ef-156">Sisällöntäyteinen lohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="912ef-157">Sisällönsijoittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="912ef-158">Omaisuusmoduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="912ef-159">Hero-moduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="912ef-160">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="912ef-160">Video player module</span></span>](add-video-player.md)
