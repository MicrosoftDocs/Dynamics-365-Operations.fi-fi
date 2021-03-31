---
title: Kampanjabannerimoduuli
description: Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206580"
---
# <a name="promo-banner-module"></a><span data-ttu-id="2bd8f-103">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="2bd8f-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2bd8f-104">Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2bd8f-105">Kampanjabannerimoduuleja käytetään sivun sisäisten tietosanomien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="2bd8f-106">Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="2bd8f-107">Kampanjamoduulitmoduulit tukevat tekstisanomaa ja linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="2bd8f-108">Jos kampanjabannerimoduuliin lisätään useita sanomia, siitä tulee kiertävä karusellibanneri, jossa asiakkaat voidaan kierrättää kaikki sanomat.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="2bd8f-109">Kampanjabannerimoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="2bd8f-110">Esimerkkejä kampanjabannerien käytöstä sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="2bd8f-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="2bd8f-111">Kampanjabannereita voidaan käyttää sivuston ylätunnisteissa, jossa niissä voidaan näyttää koko sivustoa koskevia kampanjoita tai sanomia, kuten seuraavissa esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="2bd8f-112">Vuosittainen alennusmyynti loppuu 10 päivän kuluttua</span><span class="sxs-lookup"><span data-stu-id="2bd8f-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="2bd8f-113">Alennusmyynnit ennen koulujen alkamista.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-113">"Save big with back to school sale.</span></span> <span data-ttu-id="2bd8f-114">Osta nyt.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-114">Shop Now."</span></span>

<span data-ttu-id="2bd8f-115">"Osta Kiitospäivän ALENNUSMYYNNISTÄ!"</span><span class="sxs-lookup"><span data-stu-id="2bd8f-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="2bd8f-116">Seuraavassa kuvassa on esimerkki kampanjabannerista.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-116">The following image shows an example of a promo banner.</span></span>

![Esimerkki kampanjabannerimoduulista](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="2bd8f-118">Kampanjabannerimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2bd8f-118">Promo banner module properties</span></span>

| <span data-ttu-id="2bd8f-119">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="2bd8f-119">Property name</span></span>             | <span data-ttu-id="2bd8f-120">Arvo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-120">Value</span></span>                              | <span data-ttu-id="2bd8f-121">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2bd8f-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="2bd8f-122">Banneriviestit</span><span class="sxs-lookup"><span data-stu-id="2bd8f-122">Banner messages</span></span>           | <span data-ttu-id="2bd8f-123">Teksti ja linkit</span><span class="sxs-lookup"><span data-stu-id="2bd8f-123">Text and links</span></span>                     | <span data-ttu-id="2bd8f-124">Teksti-ja linkkitaulukko</span><span class="sxs-lookup"><span data-stu-id="2bd8f-124">An array of text and links.</span></span> |
| <span data-ttu-id="2bd8f-125">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="2bd8f-125">Autoplay</span></span>                  | <span data-ttu-id="2bd8f-126">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="2bd8f-126">**True** or **False**</span></span>              | <span data-ttu-id="2bd8f-127">Arvo, joka ilmaisee kierrätetäänkö sanomia automaattisesti, jos useita sanomia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="2bd8f-128">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="2bd8f-128">Slide transition interval</span></span> | <span data-ttu-id="2bd8f-129">Millisekuntien (ms) määrä</span><span class="sxs-lookup"><span data-stu-id="2bd8f-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="2bd8f-130">Aikaväli, jota käytetään sanomien kierrättämiseen.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="2bd8f-131">Salli ohittaminen</span><span class="sxs-lookup"><span data-stu-id="2bd8f-131">Allow dismiss</span></span>             | <span data-ttu-id="2bd8f-132">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="2bd8f-132">**True** or **False**</span></span>              | <span data-ttu-id="2bd8f-133">Jos arvoksi on määritetty **Tosi**, asiakkaat voivat hylätä hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="2bd8f-134">Näytä karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="2bd8f-134">Show carousel flipper</span></span>     | <span data-ttu-id="2bd8f-135">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="2bd8f-135">**True** or **False**</span></span>              | <span data-ttu-id="2bd8f-136">Arvo, joka ilmaisee, näytetäänkö karusellin valitsimet, jotta asiakkaan voivat kierrättää useita bannerikohteita manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="2bd8f-137">Tekstin tasaus</span><span class="sxs-lookup"><span data-stu-id="2bd8f-137">Text alignment</span></span>            | <span data-ttu-id="2bd8f-138">**Oikealla**, **vasemmalla** tai **keskellä**</span><span class="sxs-lookup"><span data-stu-id="2bd8f-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="2bd8f-139">Tekstin kohdistus kampanjabannerimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="2bd8f-140">Linkitä</span><span class="sxs-lookup"><span data-stu-id="2bd8f-140">Link</span></span>                      | <span data-ttu-id="2bd8f-141">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="2bd8f-141">A URL</span></span>                              | <span data-ttu-id="2bd8f-142">Vapaavalintaisen linkin URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="2bd8f-143">Kampanjabannerimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="2bd8f-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="2bd8f-144">Voit lisätä kampanjabannerimoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2bd8f-145">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2bd8f-146">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2bd8f-147">Lisää **Oletussivu**-moduuli **Tekstiosa**-paikkaan **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="2bd8f-148">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="2bd8f-149">Luo **Kampanjabannerisivu**-niminen sivu käyttämällä juuri luotua mallia.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="2bd8f-150">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="2bd8f-151">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="2bd8f-152">Lisää kampanjabannerimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="2bd8f-153">Lisää vähintään yksi bannerisanoma bannerimoduulin asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="2bd8f-154">Kussakin sanomassa voi olla tekstiä ja linkki.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-154">Each message can have text together with a link.</span></span> <span data-ttu-id="2bd8f-155">Voit mukauttaa moduulia entisestään muokkaamalla muita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="2bd8f-156">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2bd8f-157">Sivun yläosassa pitäisi nyt olla hälytys, joka näyttää lisäämäsi tekstin.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="2bd8f-158">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="2bd8f-159">Kampanjabanneria käytetään yleensä sivun ylätunniste- ja alaotsikkopaikassa.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2bd8f-160">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2bd8f-160">Additional resources</span></span>

[<span data-ttu-id="2bd8f-161">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2bd8f-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2bd8f-162">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="2bd8f-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2bd8f-163">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="2bd8f-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2bd8f-164">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="2bd8f-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2bd8f-165">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="2bd8f-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]