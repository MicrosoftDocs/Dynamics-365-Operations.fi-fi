---
title: Kampanjabannerimoduuli
description: Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025617"
---
# <a name="promo-banner-module"></a><span data-ttu-id="4b764-103">Kampanjabannerimoduuli</span><span class="sxs-lookup"><span data-stu-id="4b764-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4b764-104">Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="4b764-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4b764-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4b764-105">Overview</span></span>

<span data-ttu-id="4b764-106">Kampanjabannerimoduuleja käytetään sivun sisäisten tietosanomien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="4b764-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="4b764-107">Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="4b764-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="4b764-108">Kampanjamoduulitmoduulit tukevat tekstisanomaa ja linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4b764-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="4b764-109">Jos kampanjabannerimoduuliin lisätään useita sanomia, siitä tulee kiertävä karusellibanneri, jossa asiakkaat voidaan kierrättää kaikki sanomat.</span><span class="sxs-lookup"><span data-stu-id="4b764-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="4b764-110">Kampanjabannerimoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="4b764-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="4b764-111">Esimerkkejä kampanjabannerien käytöstä sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="4b764-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="4b764-112">Kampanjabannereita voidaan käyttää sivuston ylätunnisteissa, jossa niissä voidaan näyttää koko sivustoa koskevia kampanjoita tai sanomia, kuten seuraavissa esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="4b764-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="4b764-113">Vuosittainen alennusmyynti loppuu 10 päivän kuluttua</span><span class="sxs-lookup"><span data-stu-id="4b764-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="4b764-114">Alennusmyynnit ennen koulujen alkamista.</span><span class="sxs-lookup"><span data-stu-id="4b764-114">"Save big with back to school sale.</span></span> <span data-ttu-id="4b764-115">Osta nyt.</span><span class="sxs-lookup"><span data-stu-id="4b764-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="4b764-116">Kampanjabannerimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4b764-116">Promo banner module properties</span></span>

| <span data-ttu-id="4b764-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="4b764-117">Property name</span></span>             | <span data-ttu-id="4b764-118">Value</span><span class="sxs-lookup"><span data-stu-id="4b764-118">Value</span></span>                              | <span data-ttu-id="4b764-119">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4b764-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="4b764-120">Banneriviestit</span><span class="sxs-lookup"><span data-stu-id="4b764-120">Banner messages</span></span>           | <span data-ttu-id="4b764-121">Teksti ja linkit</span><span class="sxs-lookup"><span data-stu-id="4b764-121">Text and links</span></span>                     | <span data-ttu-id="4b764-122">Teksti-ja linkkitaulukko</span><span class="sxs-lookup"><span data-stu-id="4b764-122">An array of text and links.</span></span> |
| <span data-ttu-id="4b764-123">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="4b764-123">Autoplay</span></span>                  | <span data-ttu-id="4b764-124">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="4b764-124">**True** or **False**</span></span>              | <span data-ttu-id="4b764-125">Arvo, joka ilmaisee kierrätetäänkö sanomia automaattisesti, jos useita sanomia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="4b764-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="4b764-126">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="4b764-126">Slide transition interval</span></span> | <span data-ttu-id="4b764-127">Millisekuntien (ms) määrä</span><span class="sxs-lookup"><span data-stu-id="4b764-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="4b764-128">Aikaväli, jota käytetään sanomien kierrättämiseen.</span><span class="sxs-lookup"><span data-stu-id="4b764-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="4b764-129">Salli ohittaminen</span><span class="sxs-lookup"><span data-stu-id="4b764-129">Allow dismiss</span></span>             | <span data-ttu-id="4b764-130">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="4b764-130">**True** or **False**</span></span>              | <span data-ttu-id="4b764-131">Jos arvoksi on määritetty **Tosi**, asiakkaat voivat hylätä hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="4b764-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="4b764-132">Näytä karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="4b764-132">Show carousel flipper</span></span>     | <span data-ttu-id="4b764-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="4b764-133">**True** or **False**</span></span>              | <span data-ttu-id="4b764-134">Arvo, joka ilmaisee, näytetäänkö karusellin valitsimet, jotta asiakkaan voivat kierrättää useita bannerikohteita manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="4b764-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="4b764-135">Tekstin tasaus</span><span class="sxs-lookup"><span data-stu-id="4b764-135">Text alignment</span></span>            | <span data-ttu-id="4b764-136">**Oikealla**, **vasemmalla** tai **keskellä**</span><span class="sxs-lookup"><span data-stu-id="4b764-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="4b764-137">Tekstin kohdistus kampanjabannerimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="4b764-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="4b764-138">Linkitä</span><span class="sxs-lookup"><span data-stu-id="4b764-138">Link</span></span>                      | <span data-ttu-id="4b764-139">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="4b764-139">A URL</span></span>                              | <span data-ttu-id="4b764-140">Vapaavalintaisen linkin URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4b764-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="4b764-141">Kampanjabannerimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="4b764-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="4b764-142">Voit lisätä kampanjabannerimoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4b764-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4b764-143">Luo sivumalli, jonka nimi on **Kampanjabannerimalli**.</span><span class="sxs-lookup"><span data-stu-id="4b764-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="4b764-144">Lisää **Oletussivu**-moduuli **Tekstiosa**-paikkaan **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="4b764-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="4b764-145">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="4b764-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="4b764-146">Luo **Kampanjabannerisivu**-niminen sivu käyttämällä juuri luotua mallia.</span><span class="sxs-lookup"><span data-stu-id="4b764-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="4b764-147">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="4b764-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="4b764-148">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="4b764-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="4b764-149">Lisää kampanjabannerimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="4b764-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="4b764-150">Lisää vähintään yksi bannerisanoma bannerimoduulin asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="4b764-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="4b764-151">Kussakin sanomassa voi olla tekstiä ja linkki.</span><span class="sxs-lookup"><span data-stu-id="4b764-151">Each message can have text together with a link.</span></span> <span data-ttu-id="4b764-152">Voit mukauttaa moduulia entisestään muokkaamalla muita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="4b764-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="4b764-153">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="4b764-153">Save and preview the page.</span></span> <span data-ttu-id="4b764-154">Sivun yläosassa pitäisi nyt olla hälytys, joka näyttää lisäämäsi tekstin.</span><span class="sxs-lookup"><span data-stu-id="4b764-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="4b764-155">Kun sivun muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="4b764-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b764-156">Kampanjabanneria käytetään yleensä sivun ylätunniste- ja alaotsikkopaikassa.</span><span class="sxs-lookup"><span data-stu-id="4b764-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="4b764-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4b764-157">Additional resources</span></span>

[<span data-ttu-id="4b764-158">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4b764-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4b764-159">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="4b764-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="4b764-160">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="4b764-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="4b764-161">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="4b764-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="4b764-162">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="4b764-162">Video player module</span></span>](add-video-player.md)
