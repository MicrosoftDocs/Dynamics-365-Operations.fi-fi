---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797884"
---
# <a name="carousel-module"></a><span data-ttu-id="f321a-103">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="f321a-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f321a-104">Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="f321a-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f321a-105">Karusellimoduulia käytetään useiden kampanjanimikkeiden (mukaan lukien kuvat) sijoittamisessa kiertävään karusellibanneriin, jota asiakkaat voivat selata.</span><span class="sxs-lookup"><span data-stu-id="f321a-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f321a-106">Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="f321a-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f321a-107">Voit lisätä sisältölohkomoduuleja karusellimoduulin sisälle.</span><span class="sxs-lookup"><span data-stu-id="f321a-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f321a-108">Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.</span><span class="sxs-lookup"><span data-stu-id="f321a-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f321a-109">Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista</span><span class="sxs-lookup"><span data-stu-id="f321a-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f321a-110">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="f321a-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f321a-111">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="f321a-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f321a-112">Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.</span><span class="sxs-lookup"><span data-stu-id="f321a-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="f321a-113">Seuraavassa kuvassa näkyy esimerkki karusellimoduulista, jota käytetään kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="f321a-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="f321a-114">Tämä karusellimoduuli sisältää useita sisältölohkon kohteita.</span><span class="sxs-lookup"><span data-stu-id="f321a-114">This carousel module contains multiple content block items.</span></span>

![Esimerkki karusellimoduulista](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="f321a-116">Karusellimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f321a-116">Carousel module properties</span></span>

| <span data-ttu-id="f321a-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="f321a-117">Property name</span></span>             | <span data-ttu-id="f321a-118">Arvo</span><span class="sxs-lookup"><span data-stu-id="f321a-118">Value</span></span>                 | <span data-ttu-id="f321a-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f321a-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f321a-120">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="f321a-120">Autoplay</span></span>                  | <span data-ttu-id="f321a-121">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="f321a-121">**True** or **False**</span></span> | <span data-ttu-id="f321a-122">Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f321a-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f321a-123">Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla.</span><span class="sxs-lookup"><span data-stu-id="f321a-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f321a-124">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="f321a-124">Slide transition interval</span></span> | <span data-ttu-id="f321a-125">Arvo sekunteina</span><span class="sxs-lookup"><span data-stu-id="f321a-125">A value in seconds</span></span>    | <span data-ttu-id="f321a-126">Nimikkeiden välisten siirtojen aikaväli.</span><span class="sxs-lookup"><span data-stu-id="f321a-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f321a-127">Siirtymätyyppi</span><span class="sxs-lookup"><span data-stu-id="f321a-127">Transition type</span></span>           | <span data-ttu-id="f321a-128">**Dia** tai **häivytys**</span><span class="sxs-lookup"><span data-stu-id="f321a-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="f321a-129">Nimikkeiden välinen siirtymistehoste.</span><span class="sxs-lookup"><span data-stu-id="f321a-129">The transition effect between items.</span></span> |
| <span data-ttu-id="f321a-130">Piilota karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="f321a-130">Hide carousel flipper</span></span>     | <span data-ttu-id="f321a-131">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="f321a-131">**True** or **False**</span></span> | <span data-ttu-id="f321a-132">Jos arvoksi on määritetty **Tosi**, karusellin valitsin ja järjestyksen osoitin piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="f321a-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f321a-133">Salli karusellin ohittaminen</span><span class="sxs-lookup"><span data-stu-id="f321a-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="f321a-134">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="f321a-134">**True** or **False**</span></span> | <span data-ttu-id="f321a-135">Jos arvoksi on määritetty **Tosi**, käyttäjät voivat ohittaa karusellin.</span><span class="sxs-lookup"><span data-stu-id="f321a-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f321a-136">Karusellimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="f321a-136">Add a carousel module to a page</span></span>

<span data-ttu-id="f321a-137">Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f321a-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f321a-138">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="f321a-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f321a-139">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Karusellimalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f321a-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f321a-140">Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="f321a-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f321a-141">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="f321a-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f321a-142">Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.</span><span class="sxs-lookup"><span data-stu-id="f321a-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f321a-143">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="f321a-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f321a-144">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä näyttö**.</span><span class="sxs-lookup"><span data-stu-id="f321a-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f321a-145">Lisää karusellimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="f321a-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f321a-146">Lisää sisältölohko karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="f321a-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f321a-147">Määritä sisältölohkomoduuliin ominaisuudet antamalla **Otsikko**-, **Linkki**-, **Asettelu**- ja muut ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="f321a-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f321a-148">Lisää ja määritä toinen sisältölohkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="f321a-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f321a-149">Määritä karusellimoduulin lisäominaisuudet tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f321a-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f321a-150">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="f321a-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f321a-151">Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli).</span><span class="sxs-lookup"><span data-stu-id="f321a-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f321a-152">Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f321a-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f321a-153">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="f321a-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f321a-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f321a-154">Additional resources</span></span>

[<span data-ttu-id="f321a-155">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f321a-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f321a-156">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="f321a-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f321a-157">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="f321a-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f321a-158">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="f321a-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f321a-159">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="f321a-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]