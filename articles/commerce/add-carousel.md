---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206508"
---
# <a name="carousel-module"></a><span data-ttu-id="8b605-103">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="8b605-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8b605-104">Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="8b605-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8b605-105">Karusellimoduulia käytetään useiden kampanjanimikkeiden (mukaan lukien kuvat) sijoittamisessa kiertävään karusellibanneriin, jota asiakkaat voivat selata.</span><span class="sxs-lookup"><span data-stu-id="8b605-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="8b605-106">Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.</span><span class="sxs-lookup"><span data-stu-id="8b605-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="8b605-107">Voit lisätä sisältölohkomoduuleja karusellimoduulin sisälle.</span><span class="sxs-lookup"><span data-stu-id="8b605-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="8b605-108">Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.</span><span class="sxs-lookup"><span data-stu-id="8b605-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="8b605-109">Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista</span><span class="sxs-lookup"><span data-stu-id="8b605-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="8b605-110">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="8b605-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="8b605-111">Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="8b605-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="8b605-112">Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.</span><span class="sxs-lookup"><span data-stu-id="8b605-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="8b605-113">Seuraavassa kuvassa näkyy esimerkki karusellimoduulista, jota käytetään kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="8b605-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="8b605-114">Tämä karusellimoduuli sisältää useita sisältölohkon kohteita.</span><span class="sxs-lookup"><span data-stu-id="8b605-114">This carousel module contains multiple content block items.</span></span>

![Esimerkki karusellimoduulista](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="8b605-116">Karusellimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8b605-116">Carousel module properties</span></span>

| <span data-ttu-id="8b605-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="8b605-117">Property name</span></span>             | <span data-ttu-id="8b605-118">Arvo</span><span class="sxs-lookup"><span data-stu-id="8b605-118">Value</span></span>                 | <span data-ttu-id="8b605-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8b605-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8b605-120">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="8b605-120">Autoplay</span></span>                  | <span data-ttu-id="8b605-121">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="8b605-121">**True** or **False**</span></span> | <span data-ttu-id="8b605-122">Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="8b605-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="8b605-123">Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla.</span><span class="sxs-lookup"><span data-stu-id="8b605-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="8b605-124">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="8b605-124">Slide transition interval</span></span> | <span data-ttu-id="8b605-125">Arvo sekunteina</span><span class="sxs-lookup"><span data-stu-id="8b605-125">A value in seconds</span></span>    | <span data-ttu-id="8b605-126">Nimikkeiden välisten siirtojen aikaväli.</span><span class="sxs-lookup"><span data-stu-id="8b605-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="8b605-127">Siirtymätyyppi</span><span class="sxs-lookup"><span data-stu-id="8b605-127">Transition type</span></span>           | <span data-ttu-id="8b605-128">**Dia** tai **häivytys**</span><span class="sxs-lookup"><span data-stu-id="8b605-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="8b605-129">Nimikkeiden välinen siirtymistehoste.</span><span class="sxs-lookup"><span data-stu-id="8b605-129">The transition effect between items.</span></span> |
| <span data-ttu-id="8b605-130">Piilota karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="8b605-130">Hide carousel flipper</span></span>     | <span data-ttu-id="8b605-131">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="8b605-131">**True** or **False**</span></span> | <span data-ttu-id="8b605-132">Jos arvoksi on määritetty **Tosi**, karusellin valitsin ja järjestyksen osoitin piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="8b605-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="8b605-133">Salli karusellin ohittaminen</span><span class="sxs-lookup"><span data-stu-id="8b605-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="8b605-134">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="8b605-134">**True** or **False**</span></span> | <span data-ttu-id="8b605-135">Jos arvoksi on määritetty **Tosi**, käyttäjät voivat ohittaa karusellin.</span><span class="sxs-lookup"><span data-stu-id="8b605-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="8b605-136">Karusellimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="8b605-136">Add a carousel module to a page</span></span>

<span data-ttu-id="8b605-137">Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8b605-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8b605-138">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="8b605-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="8b605-139">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Karusellimalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b605-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="8b605-140">Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="8b605-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="8b605-141">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="8b605-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="8b605-142">Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.</span><span class="sxs-lookup"><span data-stu-id="8b605-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="8b605-143">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="8b605-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="8b605-144">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä näyttö**.</span><span class="sxs-lookup"><span data-stu-id="8b605-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="8b605-145">Lisää karusellimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="8b605-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="8b605-146">Lisää sisältölohko karusellimoduuliin.</span><span class="sxs-lookup"><span data-stu-id="8b605-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="8b605-147">Määritä sisältölohkomoduuliin ominaisuudet antamalla **Otsikko**-, **Linkki**-, **Asettelu**- ja muut ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="8b605-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="8b605-148">Lisää ja määritä toinen sisältölohkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="8b605-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="8b605-149">Määritä karusellimoduulin lisäominaisuudet tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="8b605-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="8b605-150">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="8b605-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="8b605-151">Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli).</span><span class="sxs-lookup"><span data-stu-id="8b605-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="8b605-152">Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="8b605-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="8b605-153">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="8b605-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b605-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8b605-154">Additional resources</span></span>

[<span data-ttu-id="8b605-155">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8b605-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8b605-156">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="8b605-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="8b605-157">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="8b605-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="8b605-158">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="8b605-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="8b605-159">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="8b605-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]