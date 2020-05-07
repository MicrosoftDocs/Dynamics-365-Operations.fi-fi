---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269725"
---
# <a name="carousel-module"></a><span data-ttu-id="a530d-103">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="a530d-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a530d-104">Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="a530d-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a530d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a530d-105">Overview</span></span>

<span data-ttu-id="a530d-106">Karusellimoduulia käytetään useiden kampanjanimikkeiden (mukaan lukien kuvat) sijoittamisessa kiertävään karusellibanneriin, jota asiakkaat voivat selata.</span><span class="sxs-lookup"><span data-stu-id="a530d-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="a530d-107">Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="a530d-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="a530d-108">Voit lisätä sisältölohkomoduuleja karusellimoduulin sisälle.</span><span class="sxs-lookup"><span data-stu-id="a530d-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="a530d-109">Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.</span><span class="sxs-lookup"><span data-stu-id="a530d-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="a530d-110">Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista</span><span class="sxs-lookup"><span data-stu-id="a530d-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="a530d-111">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="a530d-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="a530d-112">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="a530d-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="a530d-113">Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.</span><span class="sxs-lookup"><span data-stu-id="a530d-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="a530d-114">Karusellimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="a530d-114">Carousel module properties</span></span>

| <span data-ttu-id="a530d-115">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="a530d-115">Property name</span></span>             | <span data-ttu-id="a530d-116">Arvo</span><span class="sxs-lookup"><span data-stu-id="a530d-116">Value</span></span>                 | <span data-ttu-id="a530d-117">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a530d-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="a530d-118">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="a530d-118">Autoplay</span></span>                  | <span data-ttu-id="a530d-119">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a530d-119">**True** or **False**</span></span> | <span data-ttu-id="a530d-120">Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a530d-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="a530d-121">Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla.</span><span class="sxs-lookup"><span data-stu-id="a530d-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="a530d-122">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="a530d-122">Slide transition interval</span></span> | <span data-ttu-id="a530d-123">Arvo sekunteina</span><span class="sxs-lookup"><span data-stu-id="a530d-123">A value in seconds</span></span>    | <span data-ttu-id="a530d-124">Nimikkeiden välisten siirtojen aikaväli.</span><span class="sxs-lookup"><span data-stu-id="a530d-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="a530d-125">Siirtymätyyppi</span><span class="sxs-lookup"><span data-stu-id="a530d-125">Transition type</span></span>           | <span data-ttu-id="a530d-126">**Dia** tai **häivytys**</span><span class="sxs-lookup"><span data-stu-id="a530d-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="a530d-127">Nimikkeiden välinen siirtymistehoste.</span><span class="sxs-lookup"><span data-stu-id="a530d-127">The transition effect between items.</span></span> |
| <span data-ttu-id="a530d-128">Piilota karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="a530d-128">Hide carousel flipper</span></span>     | <span data-ttu-id="a530d-129">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a530d-129">**True** or **False**</span></span> | <span data-ttu-id="a530d-130">Jos arvoksi on määritetty **Tosi**, karusellin valitsin ja järjestyksen osoitin piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="a530d-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="a530d-131">Salli karusellin ohittaminen</span><span class="sxs-lookup"><span data-stu-id="a530d-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="a530d-132">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a530d-132">**True** or **False**</span></span> | <span data-ttu-id="a530d-133">Jos arvoksi on määritetty **Tosi**, käyttäjät voivat ohittaa karusellin.</span><span class="sxs-lookup"><span data-stu-id="a530d-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="a530d-134">Karusellimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="a530d-134">Add a carousel module to a page</span></span>

<span data-ttu-id="a530d-135">Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a530d-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a530d-136">Luo sivumalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a530d-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="a530d-137">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Karusellimalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="a530d-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a530d-138">Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="a530d-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="a530d-139">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="a530d-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="a530d-140">Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.</span><span class="sxs-lookup"><span data-stu-id="a530d-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="a530d-141">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="a530d-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="a530d-142">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä näyttö**.</span><span class="sxs-lookup"><span data-stu-id="a530d-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="a530d-143">Lisää karusellimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a530d-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="a530d-144">Lisää sisältölohko karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="a530d-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="a530d-145">Määritä sisältölohkomoduuliin ominaisuudet antamalla **Otsikko**-, **Linkki**-, **Asettelu**- ja muut ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="a530d-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="a530d-146">Lisää ja määritä toinen sisältölohkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="a530d-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="a530d-147">Määritä karusellimoduulin lisäominaisuudet tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a530d-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="a530d-148">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="a530d-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="a530d-149">Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli).</span><span class="sxs-lookup"><span data-stu-id="a530d-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="a530d-150">Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="a530d-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="a530d-151">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="a530d-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a530d-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a530d-152">Additional resources</span></span>

[<span data-ttu-id="a530d-153">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a530d-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a530d-154">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="a530d-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="a530d-155">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="a530d-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a530d-156">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="a530d-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="a530d-157">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="a530d-157">Video player module</span></span>](add-video-player.md)
