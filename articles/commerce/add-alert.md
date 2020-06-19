---
title: Kampanjabannerimoduuli
description: Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: dae824cdbaaf56f85f125c5f36aaa56171bbd6bc
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411362"
---
# <a name="promo-banner-module"></a><span data-ttu-id="a99ab-103">Kampanjabannerimoduuli</span><span class="sxs-lookup"><span data-stu-id="a99ab-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a99ab-104">Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="a99ab-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a99ab-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a99ab-105">Overview</span></span>

<span data-ttu-id="a99ab-106">Kampanjabannerimoduuleja käytetään sivun sisäisten tietosanomien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="a99ab-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="a99ab-107">Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="a99ab-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="a99ab-108">Kampanjamoduulitmoduulit tukevat tekstisanomaa ja linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a99ab-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="a99ab-109">Jos kampanjabannerimoduuliin lisätään useita sanomia, siitä tulee kiertävä karusellibanneri, jossa asiakkaat voidaan kierrättää kaikki sanomat.</span><span class="sxs-lookup"><span data-stu-id="a99ab-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="a99ab-110">Kampanjabannerimoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="a99ab-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="a99ab-111">Esimerkkejä kampanjabannerien käytöstä sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="a99ab-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="a99ab-112">Kampanjabannereita voidaan käyttää sivuston ylätunnisteissa, jossa niissä voidaan näyttää koko sivustoa koskevia kampanjoita tai sanomia, kuten seuraavissa esimerkeissä.</span><span class="sxs-lookup"><span data-stu-id="a99ab-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="a99ab-113">Vuosittainen alennusmyynti loppuu 10 päivän kuluttua</span><span class="sxs-lookup"><span data-stu-id="a99ab-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="a99ab-114">Alennusmyynnit ennen koulujen alkamista.</span><span class="sxs-lookup"><span data-stu-id="a99ab-114">"Save big with back to school sale.</span></span> <span data-ttu-id="a99ab-115">Osta nyt.</span><span class="sxs-lookup"><span data-stu-id="a99ab-115">Shop Now."</span></span>

<span data-ttu-id="a99ab-116">"Osta Kiitospäivän ALENNUSMYYNNISTÄ!"</span><span class="sxs-lookup"><span data-stu-id="a99ab-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="a99ab-117">Seuraavassa kuvassa on esimerkki kampanjabannerista.</span><span class="sxs-lookup"><span data-stu-id="a99ab-117">The following image shows an example of a promo banner.</span></span>

![Esimerkki kampanjabannerimoduulista](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="a99ab-119">Kampanjabannerimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="a99ab-119">Promo banner module properties</span></span>

| <span data-ttu-id="a99ab-120">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="a99ab-120">Property name</span></span>             | <span data-ttu-id="a99ab-121">Arvo</span><span class="sxs-lookup"><span data-stu-id="a99ab-121">Value</span></span>                              | <span data-ttu-id="a99ab-122">kuvaus</span><span class="sxs-lookup"><span data-stu-id="a99ab-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="a99ab-123">Banneriviestit</span><span class="sxs-lookup"><span data-stu-id="a99ab-123">Banner messages</span></span>           | <span data-ttu-id="a99ab-124">Teksti ja linkit</span><span class="sxs-lookup"><span data-stu-id="a99ab-124">Text and links</span></span>                     | <span data-ttu-id="a99ab-125">Teksti-ja linkkitaulukko</span><span class="sxs-lookup"><span data-stu-id="a99ab-125">An array of text and links.</span></span> |
| <span data-ttu-id="a99ab-126">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="a99ab-126">Autoplay</span></span>                  | <span data-ttu-id="a99ab-127">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a99ab-127">**True** or **False**</span></span>              | <span data-ttu-id="a99ab-128">Arvo, joka ilmaisee kierrätetäänkö sanomia automaattisesti, jos useita sanomia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="a99ab-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="a99ab-129">Dian vaihtoväli</span><span class="sxs-lookup"><span data-stu-id="a99ab-129">Slide transition interval</span></span> | <span data-ttu-id="a99ab-130">Millisekuntien (ms) määrä</span><span class="sxs-lookup"><span data-stu-id="a99ab-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="a99ab-131">Aikaväli, jota käytetään sanomien kierrättämiseen.</span><span class="sxs-lookup"><span data-stu-id="a99ab-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="a99ab-132">Salli ohittaminen</span><span class="sxs-lookup"><span data-stu-id="a99ab-132">Allow dismiss</span></span>             | <span data-ttu-id="a99ab-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a99ab-133">**True** or **False**</span></span>              | <span data-ttu-id="a99ab-134">Jos arvoksi on määritetty **Tosi**, asiakkaat voivat hylätä hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="a99ab-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="a99ab-135">Näytä karusellin valitsin</span><span class="sxs-lookup"><span data-stu-id="a99ab-135">Show carousel flipper</span></span>     | <span data-ttu-id="a99ab-136">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a99ab-136">**True** or **False**</span></span>              | <span data-ttu-id="a99ab-137">Arvo, joka ilmaisee, näytetäänkö karusellin valitsimet, jotta asiakkaan voivat kierrättää useita bannerikohteita manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a99ab-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="a99ab-138">Tekstin tasaus</span><span class="sxs-lookup"><span data-stu-id="a99ab-138">Text alignment</span></span>            | <span data-ttu-id="a99ab-139">**Oikealla**, **vasemmalla** tai **keskellä**</span><span class="sxs-lookup"><span data-stu-id="a99ab-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="a99ab-140">Tekstin kohdistus kampanjabannerimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="a99ab-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="a99ab-141">Linkitä</span><span class="sxs-lookup"><span data-stu-id="a99ab-141">Link</span></span>                      | <span data-ttu-id="a99ab-142">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="a99ab-142">A URL</span></span>                              | <span data-ttu-id="a99ab-143">Vapaavalintaisen linkin URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="a99ab-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="a99ab-144">Kampanjabannerimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="a99ab-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="a99ab-145">Voit lisätä kampanjabannerimoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a99ab-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a99ab-146">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="a99ab-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="a99ab-147">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99ab-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a99ab-148">Lisää **Oletussivu**-moduuli **Tekstiosa**-paikkaan **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a99ab-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="a99ab-149">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="a99ab-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="a99ab-150">Luo **Kampanjabannerisivu**-niminen sivu käyttämällä juuri luotua mallia.</span><span class="sxs-lookup"><span data-stu-id="a99ab-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="a99ab-151">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="a99ab-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="a99ab-152">Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="a99ab-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="a99ab-153">Lisää kampanjabannerimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a99ab-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="a99ab-154">Lisää vähintään yksi bannerisanoma bannerimoduulin asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="a99ab-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="a99ab-155">Kussakin sanomassa voi olla tekstiä ja linkki.</span><span class="sxs-lookup"><span data-stu-id="a99ab-155">Each message can have text together with a link.</span></span> <span data-ttu-id="a99ab-156">Voit mukauttaa moduulia entisestään muokkaamalla muita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="a99ab-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="a99ab-157">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="a99ab-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="a99ab-158">Sivun yläosassa pitäisi nyt olla hälytys, joka näyttää lisäämäsi tekstin.</span><span class="sxs-lookup"><span data-stu-id="a99ab-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="a99ab-159">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="a99ab-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="a99ab-160">Kampanjabanneria käytetään yleensä sivun ylätunniste- ja alaotsikkopaikassa.</span><span class="sxs-lookup"><span data-stu-id="a99ab-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a99ab-161">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a99ab-161">Additional resources</span></span>

[<span data-ttu-id="a99ab-162">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a99ab-162">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a99ab-163">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="a99ab-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a99ab-164">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="a99ab-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a99ab-165">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="a99ab-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="a99ab-166">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="a99ab-166">Video player module</span></span>](add-video-player.md)
