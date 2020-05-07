---
title: Kampanjabannerimoduuli
description: Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269771"
---
# <a name="promo-banner-module"></a><span data-ttu-id="087ef-103">Kampanjabannerimoduuli</span><span class="sxs-lookup"><span data-stu-id="087ef-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="087ef-104">Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="087ef-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="087ef-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="087ef-105">Overview</span></span>

<span data-ttu-id="087ef-106">Kampanjabannerimoduuleja käytetään sivun sisäisten tietosanomien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="087ef-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="087ef-107">Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="087ef-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="087ef-108">Kampanjamoduulitmoduulit tukevat tekstisanomaa ja linkkiä.</span><span class="sxs-lookup"><span data-stu-id="087ef-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="087ef-109">Jos kampanjabannerimoduuliin lisätään useita sanomia, siitä tulee kiertävä karusellibanneri, jossa asiakkaat voidaan kierrättää kaikki sanomat.</span><span class="sxs-lookup"><span data-stu-id="087ef-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="087ef-110">Kampanjabannerimoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="087ef-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="087ef-111">Esimerkkejä kampanjabannerien käytöstä sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="087ef-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="087ef-112">Kampanjabannereita voidaan käyttää sivuston ylätunnisteissa, jossa niissä voidaan näyttää koko sivustoa koskevia kampanjoita tai sanomia, kuten seuraavissa esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="087ef-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="087ef-113">Vuosittainen alennusmyynti loppuu 10 päivän kuluttua</span><span class="sxs-lookup"><span data-stu-id="087ef-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="087ef-114">Alennusmyynnit ennen koulujen alkamista.</span><span class="sxs-lookup"><span data-stu-id="087ef-114">"Save big with back to school sale.</span></span> <span data-ttu-id="087ef-115">Osta nyt.</span><span class="sxs-lookup"><span data-stu-id="087ef-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="087ef-116">Kampanjabannerimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="087ef-116">Promo banner module properties</span></span>

| <span data-ttu-id="087ef-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="087ef-117">Property name</span></span>             | <span data-ttu-id="087ef-118">Value</span><span class="sxs-lookup"><span data-stu-id="087ef-118">Value</span></span>                              | <span data-ttu-id="087ef-119">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="087ef-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="087ef-120">Banneriviestit</span><span class="sxs-lookup"><span data-stu-id="087ef-120">Banner messages</span></span>           | <span data-ttu-id="087ef-121">Teksti ja linkit</span><span class="sxs-lookup"><span data-stu-id="087ef-121">Text and links</span></span>                     | <span data-ttu-id="087ef-122">Teksti-ja linkkitaulukko</span><span class="sxs-lookup"><span data-stu-id="087ef-122">An array of text and links.</span></span> |
| <span data-ttu-id="087ef-123">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="087ef-123">Autoplay</span></span>                  | <span data-ttu-id="087ef-124">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="087ef-124">**True** or **False**</span></span>              | <span data-ttu-id="087ef-125">Arvo, joka ilmaisee kierrätetäänkö sanomia automaattisesti, jos useita sanomia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="087ef-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="087ef-126">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="087ef-126">Slide transition interval</span></span> | <span data-ttu-id="087ef-127">Millisekuntien (ms) määrä</span><span class="sxs-lookup"><span data-stu-id="087ef-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="087ef-128">Aikaväli, jota käytetään sanomien kierrättämiseen.</span><span class="sxs-lookup"><span data-stu-id="087ef-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="087ef-129">Salli ohittaminen</span><span class="sxs-lookup"><span data-stu-id="087ef-129">Allow dismiss</span></span>             | <span data-ttu-id="087ef-130">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="087ef-130">**True** or **False**</span></span>              | <span data-ttu-id="087ef-131">Jos arvoksi on määritetty **Tosi**, asiakkaat voivat hylätä hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="087ef-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="087ef-132">Näytä karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="087ef-132">Show carousel flipper</span></span>     | <span data-ttu-id="087ef-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="087ef-133">**True** or **False**</span></span>              | <span data-ttu-id="087ef-134">Arvo, joka ilmaisee, näytetäänkö karusellin valitsimet, jotta asiakkaan voivat kierrättää useita bannerikohteita manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="087ef-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="087ef-135">Tekstin tasaus</span><span class="sxs-lookup"><span data-stu-id="087ef-135">Text alignment</span></span>            | <span data-ttu-id="087ef-136">**Oikealla**, **vasemmalla** tai **keskellä**</span><span class="sxs-lookup"><span data-stu-id="087ef-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="087ef-137">Tekstin kohdistus kampanjabannerimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="087ef-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="087ef-138">Linkitä</span><span class="sxs-lookup"><span data-stu-id="087ef-138">Link</span></span>                      | <span data-ttu-id="087ef-139">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="087ef-139">A URL</span></span>                              | <span data-ttu-id="087ef-140">Vapaavalintaisen linkin URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="087ef-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="087ef-141">Kampanjabannerimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="087ef-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="087ef-142">Voit lisätä kampanjabannerimoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="087ef-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="087ef-143">Luo sivumalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="087ef-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="087ef-144">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="087ef-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="087ef-145">Lisää **Oletussivu**-moduuli **Tekstiosa**-paikkaan **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="087ef-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="087ef-146">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="087ef-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="087ef-147">Luo **Kampanjabannerisivu**-niminen sivu käyttämällä juuri luotua mallia.</span><span class="sxs-lookup"><span data-stu-id="087ef-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="087ef-148">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="087ef-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="087ef-149">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="087ef-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="087ef-150">Lisää kampanjabannerimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="087ef-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="087ef-151">Lisää vähintään yksi bannerisanoma bannerimoduulin asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="087ef-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="087ef-152">Kussakin sanomassa voi olla tekstiä ja linkki.</span><span class="sxs-lookup"><span data-stu-id="087ef-152">Each message can have text together with a link.</span></span> <span data-ttu-id="087ef-153">Voit mukauttaa moduulia entisestään muokkaamalla muita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="087ef-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="087ef-154">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="087ef-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="087ef-155">Sivun yläosassa pitäisi nyt olla hälytys, joka näyttää lisäämäsi tekstin.</span><span class="sxs-lookup"><span data-stu-id="087ef-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="087ef-156">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="087ef-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="087ef-157">Kampanjabanneria käytetään yleensä sivun ylätunniste- ja alaotsikkopaikassa.</span><span class="sxs-lookup"><span data-stu-id="087ef-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="087ef-158">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="087ef-158">Additional resources</span></span>

[<span data-ttu-id="087ef-159">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="087ef-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="087ef-160">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="087ef-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="087ef-161">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="087ef-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="087ef-162">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="087ef-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="087ef-163">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="087ef-163">Video player module</span></span>](add-video-player.md)
