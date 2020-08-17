---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620983"
---
# <a name="carousel-module"></a><span data-ttu-id="1e81f-103">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="1e81f-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e81f-104">Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="1e81f-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1e81f-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1e81f-105">Overview</span></span>

<span data-ttu-id="1e81f-106">Karusellimoduulia käytetään useiden kampanjanimikkeiden (mukaan lukien kuvat) sijoittamisessa kiertävään karusellibanneriin, jota asiakkaat voivat selata.</span><span class="sxs-lookup"><span data-stu-id="1e81f-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="1e81f-107">Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="1e81f-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="1e81f-108">Voit lisätä sisältölohkomoduuleja karusellimoduulin sisälle.</span><span class="sxs-lookup"><span data-stu-id="1e81f-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="1e81f-109">Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.</span><span class="sxs-lookup"><span data-stu-id="1e81f-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="1e81f-110">Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista</span><span class="sxs-lookup"><span data-stu-id="1e81f-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="1e81f-111">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="1e81f-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="1e81f-112">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="1e81f-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="1e81f-113">Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.</span><span class="sxs-lookup"><span data-stu-id="1e81f-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="1e81f-114">Seuraavassa kuvassa näkyy esimerkki karusellimoduulista, jota käytetään kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="1e81f-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="1e81f-115">Tämä karusellimoduuli sisältää useita sisältölohkon kohteita.</span><span class="sxs-lookup"><span data-stu-id="1e81f-115">This carousel module contains multiple content block items.</span></span>

![Esimerkki karusellimoduulista](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="1e81f-117">Karusellimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1e81f-117">Carousel module properties</span></span>

| <span data-ttu-id="1e81f-118">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="1e81f-118">Property name</span></span>             | <span data-ttu-id="1e81f-119">Arvo</span><span class="sxs-lookup"><span data-stu-id="1e81f-119">Value</span></span>                 | <span data-ttu-id="1e81f-120">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1e81f-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="1e81f-121">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="1e81f-121">Autoplay</span></span>                  | <span data-ttu-id="1e81f-122">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1e81f-122">**True** or **False**</span></span> | <span data-ttu-id="1e81f-123">Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1e81f-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="1e81f-124">Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla.</span><span class="sxs-lookup"><span data-stu-id="1e81f-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="1e81f-125">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="1e81f-125">Slide transition interval</span></span> | <span data-ttu-id="1e81f-126">Arvo sekunteina</span><span class="sxs-lookup"><span data-stu-id="1e81f-126">A value in seconds</span></span>    | <span data-ttu-id="1e81f-127">Nimikkeiden välisten siirtojen aikaväli.</span><span class="sxs-lookup"><span data-stu-id="1e81f-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="1e81f-128">Siirtymätyyppi</span><span class="sxs-lookup"><span data-stu-id="1e81f-128">Transition type</span></span>           | <span data-ttu-id="1e81f-129">**Dia** tai **häivytys**</span><span class="sxs-lookup"><span data-stu-id="1e81f-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="1e81f-130">Nimikkeiden välinen siirtymistehoste.</span><span class="sxs-lookup"><span data-stu-id="1e81f-130">The transition effect between items.</span></span> |
| <span data-ttu-id="1e81f-131">Piilota karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="1e81f-131">Hide carousel flipper</span></span>     | <span data-ttu-id="1e81f-132">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1e81f-132">**True** or **False**</span></span> | <span data-ttu-id="1e81f-133">Jos arvoksi on määritetty **Tosi**, karusellin valitsin ja järjestyksen osoitin piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="1e81f-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="1e81f-134">Salli karusellin ohittaminen</span><span class="sxs-lookup"><span data-stu-id="1e81f-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="1e81f-135">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1e81f-135">**True** or **False**</span></span> | <span data-ttu-id="1e81f-136">Jos arvoksi on määritetty **Tosi**, käyttäjät voivat ohittaa karusellin.</span><span class="sxs-lookup"><span data-stu-id="1e81f-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="1e81f-137">Karusellimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="1e81f-137">Add a carousel module to a page</span></span>

<span data-ttu-id="1e81f-138">Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1e81f-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1e81f-139">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="1e81f-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1e81f-140">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Karusellimalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="1e81f-141">Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="1e81f-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="1e81f-142">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="1e81f-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="1e81f-143">Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="1e81f-144">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="1e81f-145">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä näyttö**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="1e81f-146">Lisää karusellimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="1e81f-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="1e81f-147">Lisää sisältölohko karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="1e81f-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="1e81f-148">Määritä sisältölohkomoduuliin ominaisuudet antamalla **Otsikko**-, **Linkki**-, **Asettelu**- ja muut ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="1e81f-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="1e81f-149">Lisää ja määritä toinen sisältölohkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="1e81f-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="1e81f-150">Määritä karusellimoduulin lisäominaisuudet tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1e81f-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="1e81f-151">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="1e81f-152">Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli).</span><span class="sxs-lookup"><span data-stu-id="1e81f-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="1e81f-153">Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="1e81f-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="1e81f-154">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="1e81f-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e81f-155">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1e81f-155">Additional resources</span></span>

[<span data-ttu-id="1e81f-156">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1e81f-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1e81f-157">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="1e81f-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="1e81f-158">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="1e81f-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1e81f-159">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="1e81f-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="1e81f-160">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="1e81f-160">Video player module</span></span>](add-video-player.md)
