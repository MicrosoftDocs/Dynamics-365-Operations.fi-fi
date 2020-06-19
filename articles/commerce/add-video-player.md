---
title: Videotoistinmoduuli
description: Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612682d310362c7523bf08db40faf51c80ea2e3
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411156"
---
# <a name="video-player-module"></a><span data-ttu-id="0d346-103">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="0d346-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0d346-104">Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="0d346-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0d346-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0d346-105">Overview</span></span>

<span data-ttu-id="0d346-106">Videotoistinmoduulia käytetään tukemaan videotoistoa.</span><span class="sxs-lookup"><span data-stu-id="0d346-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="0d346-107">Se voidaan lisätä mille tahansa sivulle, kunhan videosisältö on ladattu ja käytettävissä sisällönhallintajärjestelmässä (CMS).</span><span class="sxs-lookup"><span data-stu-id="0d346-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="0d346-108">Videotoistinmoduuli tukee .mp4-mediatyypin.</span><span class="sxs-lookup"><span data-stu-id="0d346-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="0d346-109">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="0d346-109">Video player module</span></span>

<span data-ttu-id="0d346-110">Videotoistinmoduulin avulla voit esitellä videoita sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="0d346-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="0d346-111">Se tukee kaikkia toisto-ominaisuuksia, kuten toistoa, pysäytystä, koko näytön tilaa, äänikuvauksia ja tekstityksiä.</span><span class="sxs-lookup"><span data-stu-id="0d346-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="0d346-112">Videotoistinmoduuli tukee myös tekstitysten mukauttamista Microsoftin helppokäyttötoimintojen standardien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="0d346-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="0d346-113">Voit esimerkiksi mukauttaa fontin kokoa ja taustaväriä.</span><span class="sxs-lookup"><span data-stu-id="0d346-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="0d346-114">Videosoitinmoduuli tukee myös toissijaisia ääniraitoja.</span><span class="sxs-lookup"><span data-stu-id="0d346-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="0d346-115">Kun video ladataan CMS-järjestelmään, myös toissijainen ääniraita voidaan ladata.</span><span class="sxs-lookup"><span data-stu-id="0d346-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="0d346-116">Videosoitinmoduuli voi sitten toistaa toissijaisen ääniraidan, jos käyttäjä valitsee sen.</span><span class="sxs-lookup"><span data-stu-id="0d346-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="0d346-117">Esimerkkejä videotoistinmoduuleista sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="0d346-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="0d346-118">Tuotetietosivujen tai markkinointisivujen ohjevideot</span><span class="sxs-lookup"><span data-stu-id="0d346-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="0d346-119">Markkinointisivuilla olevat käytäntöjä koskevat kampanjavideot tai videot</span><span class="sxs-lookup"><span data-stu-id="0d346-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="0d346-120">Markkinointivideot, joissa kerrotaan tuotteen ominaisuuksista tuotetietosivuilla tai markkinointisivuilla</span><span class="sxs-lookup"><span data-stu-id="0d346-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="0d346-121">Seuraavassa kuvassa on esimerkki videotoistinmoduulista kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="0d346-121">The following image shows an example of a video player module on a home page.</span></span>

![Esimerkki videotoistinmoduulista](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="0d346-123">Videotoistinmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="0d346-123">Video player module properties</span></span>

| <span data-ttu-id="0d346-124">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="0d346-124">Property name</span></span>         | <span data-ttu-id="0d346-125">Arvo</span><span class="sxs-lookup"><span data-stu-id="0d346-125">Value</span></span>                               | <span data-ttu-id="0d346-126">kuvaus</span><span class="sxs-lookup"><span data-stu-id="0d346-126">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="0d346-127">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="0d346-127">Auto play</span></span>             | <span data-ttu-id="0d346-128">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-128">**True** or **False**</span></span>               | <span data-ttu-id="0d346-129">Kun arvoksi on määritetty **Tosi**, videota toistetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0d346-129">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="0d346-130">Vaimenna</span><span class="sxs-lookup"><span data-stu-id="0d346-130">Mute</span></span>                  | <span data-ttu-id="0d346-131">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-131">**True** or **False**</span></span>               | <span data-ttu-id="0d346-132">Kun arvoksi on määritetty **Tosi**, ääni on vaimennettu.</span><span class="sxs-lookup"><span data-stu-id="0d346-132">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="0d346-133">Tämän toistimen oletusarvo on **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="0d346-133">For this player, the default value is **False**.</span></span> <span data-ttu-id="0d346-134">Chrome-selaimessa automaattisen toiston videot vaimennetaan oletusarvoisesti. Ääni toistetaan vain, jos käyttäjä toistaa videon manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="0d346-134">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="0d346-135">Silmukka</span><span class="sxs-lookup"><span data-stu-id="0d346-135">Loop</span></span>                  | <span data-ttu-id="0d346-136">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-136">**True** or **False**</span></span>               | <span data-ttu-id="0d346-137">Kun arvoksi on määritetty **Tosi**, video toistetaan silmukassa.</span><span class="sxs-lookup"><span data-stu-id="0d346-137">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="0d346-138">Mediat</span><span class="sxs-lookup"><span data-stu-id="0d346-138">Media</span></span>                 | <span data-ttu-id="0d346-139">Videotiedostopolku ja -nimi</span><span class="sxs-lookup"><span data-stu-id="0d346-139">Video file path and name</span></span> | <span data-ttu-id="0d346-140">Videotiedosto, jota videotoistin toistaa.</span><span class="sxs-lookup"><span data-stu-id="0d346-140">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="0d346-141">Toista koko näyttössä</span><span class="sxs-lookup"><span data-stu-id="0d346-141">Play fullscreen</span></span>       | <span data-ttu-id="0d346-142">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-142">**True** or **False**</span></span>               | <span data-ttu-id="0d346-143">Kun arvoksi on määritetty **Tosi**, videota toistetaan koko näytön tilassa.</span><span class="sxs-lookup"><span data-stu-id="0d346-143">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="0d346-144">Toiston/keskeytyksen valitsin</span><span class="sxs-lookup"><span data-stu-id="0d346-144">Play pause trigger</span></span>    | <span data-ttu-id="0d346-145">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-145">**True** or **False**</span></span>               | <span data-ttu-id="0d346-146">Kun arvoksi on asetettu **Tosi**, videossa näkyy toisto/pysäytys-painike.</span><span class="sxs-lookup"><span data-stu-id="0d346-146">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="0d346-147">Videosoittimen säätimet</span><span class="sxs-lookup"><span data-stu-id="0d346-147">Video player controls</span></span> | <span data-ttu-id="0d346-148">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-148">**True** or **False**</span></span>               | <span data-ttu-id="0d346-149">Kun arvoksi on määritetty **Tosi**, kaikki videotoistimen ohjausobjektit näkyvät.</span><span class="sxs-lookup"><span data-stu-id="0d346-149">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="0d346-150">Näitä ohjausobjekteja ovat toisto- ja pysäytyspainikkeet, tilanneilmaisin ja tekstitysvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="0d346-150">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="0d346-151">Piilota julistekuva</span><span class="sxs-lookup"><span data-stu-id="0d346-151">Hide poster image</span></span>     | <span data-ttu-id="0d346-152">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="0d346-152">**True** or **False**</span></span>               | <span data-ttu-id="0d346-153">Videossa voi olla julistekehys.</span><span class="sxs-lookup"><span data-stu-id="0d346-153">A video can have a poster frame.</span></span> <span data-ttu-id="0d346-154">Kun tämän ominaisuuden arvoksi määritetään **Tosi**, julistekehys piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="0d346-154">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="0d346-155">Peitteen taso</span><span class="sxs-lookup"><span data-stu-id="0d346-155">Mask level</span></span>            | <span data-ttu-id="0d346-156">Numero väliltä **0**–**100**</span><span class="sxs-lookup"><span data-stu-id="0d346-156">A number from **0** through **100**</span></span> | <span data-ttu-id="0d346-157">Muoto, jota käytetään videon muotoiluun.</span><span class="sxs-lookup"><span data-stu-id="0d346-157">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="0d346-158">Videotoistinmoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="0d346-158">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="0d346-159">Video on ennen videotoistinmoduulin luontia ladattava mediakirjastoon.</span><span class="sxs-lookup"><span data-stu-id="0d346-159">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="0d346-160">Voit lisätä videotoistinmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0d346-160">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0d346-161">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="0d346-161">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0d346-162">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Videotoistimen malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-162">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-163">Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0d346-163">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d346-164">Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-164">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-165">Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0d346-165">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d346-166">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-166">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-167">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0d346-167">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d346-168">Valitse **Lisää moduuli** -valintaikkunassa **Videotoistin**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-168">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-169">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="0d346-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="0d346-170">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="0d346-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0d346-171">Valitse **Valitse malli** -valintaikkunassa luomasi videotoistimen malli.</span><span class="sxs-lookup"><span data-stu-id="0d346-171">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="0d346-172">Kirjoita **Sivun nimi** -kohtaan **Videotoistinsivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-172">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-173">Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0d346-173">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d346-174">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-175">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0d346-175">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d346-176">Valitse **Lisää moduuli** -valintaikkunassa **Videotoistin**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-176">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-177">Valitse videotoistinmoduulin ominaisuusruudussa **Lisää video**.</span><span class="sxs-lookup"><span data-stu-id="0d346-177">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="0d346-178">Valitse **Mediavalitsin**-valintaikkunassa video ja valitse sitten **Lataa uusi medianimike**.</span><span class="sxs-lookup"><span data-stu-id="0d346-178">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="0d346-179">Valitse Resurssienhallinnassa videotiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="0d346-179">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="0d346-180">Kirjoita **Lataa mediakohde** -valintaikkunaan otsikko ja muut tarvittavat tiedot ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d346-180">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="0d346-181">Valitse **Mediavalitsin**-valintaikkunassa **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="0d346-181">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="0d346-182">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="0d346-182">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0d346-183">Videomoduulin pitäisi näkyä sivulla.</span><span class="sxs-lookup"><span data-stu-id="0d346-183">You should see the video module on the page.</span></span> <span data-ttu-id="0d346-184">Voit muokata moduulin toimintaa muuttamalla lisäasetuksia.</span><span class="sxs-lookup"><span data-stu-id="0d346-184">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="0d346-185">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="0d346-185">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="0d346-186">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0d346-186">Additional resources</span></span>

[<span data-ttu-id="0d346-187">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0d346-187">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0d346-188">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="0d346-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="0d346-189">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="0d346-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="0d346-190">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="0d346-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="0d346-191">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="0d346-191">Content block module</span></span>](add-hero-module.md)
