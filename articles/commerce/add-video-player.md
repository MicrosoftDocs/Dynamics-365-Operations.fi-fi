---
title: Videotoistinmoduuli
description: Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025642"
---
# <a name="video-player-module"></a><span data-ttu-id="a3ff8-103">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="a3ff8-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a3ff8-104">Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a3ff8-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a3ff8-105">Overview</span></span>

<span data-ttu-id="a3ff8-106">Videotoistinmoduulia käytetään tukemaan videotoistoa.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="a3ff8-107">Se voidaan lisätä mille tahansa sivulle, kunhan videosisältö on ladattu ja käytettävissä sisällönhallintajärjestelmässä (CMS).</span><span class="sxs-lookup"><span data-stu-id="a3ff8-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="a3ff8-108">Videotoistinmoduuli tukee .mp4-mediatyypin.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="a3ff8-109">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="a3ff8-109">Video player module</span></span>

<span data-ttu-id="a3ff8-110">Videotoistinmoduulin avulla voit esitellä videoita sähköisen kaupankäynnin sivustossa.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="a3ff8-111">Se tukee kaikkia toisto-ominaisuuksia, kuten toistoa, pysäytystä, koko näytön tilaa, äänikuvauksia ja tekstityksiä.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="a3ff8-112">Videotoistinmoduuli tukee myös tekstitysten mukauttamista Microsoftin helppokäyttötoimintojen standardien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="a3ff8-113">Voit esimerkiksi mukauttaa fontin kokoa ja taustaväriä.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="a3ff8-114">Videosoitinmoduuli tukee myös toissijaisia ääniraitoja.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="a3ff8-115">Kun video ladataan CMS-järjestelmään, myös toissijainen ääniraita voidaan ladata.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="a3ff8-116">Videosoitinmoduuli voi sitten toistaa toissijaisen ääniraidan, jos käyttäjä valitsee sen.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="a3ff8-117">Esimerkkejä videotoistinmoduuleista sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="a3ff8-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="a3ff8-118">Tuotetietosivujen tai markkinointisivujen ohjevideot</span><span class="sxs-lookup"><span data-stu-id="a3ff8-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="a3ff8-119">Markkinointisivuilla olevat käytäntöjä koskevat kampanjavideot tai videot</span><span class="sxs-lookup"><span data-stu-id="a3ff8-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="a3ff8-120">Markkinointivideot, joissa kerrotaan tuotteen ominaisuuksista tuotetietosivuilla tai markkinointisivuilla</span><span class="sxs-lookup"><span data-stu-id="a3ff8-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="a3ff8-121">Videotoistinmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="a3ff8-121">Video player module properties</span></span>

| <span data-ttu-id="a3ff8-122">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="a3ff8-122">Property name</span></span>         | <span data-ttu-id="a3ff8-123">Arvo</span><span class="sxs-lookup"><span data-stu-id="a3ff8-123">Value</span></span>                               | <span data-ttu-id="a3ff8-124">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a3ff8-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="a3ff8-125">Automaattinen toisto</span><span class="sxs-lookup"><span data-stu-id="a3ff8-125">Auto play</span></span>             | <span data-ttu-id="a3ff8-126">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-126">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-127">Kun arvoksi on määritetty **Tosi**, videota toistetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="a3ff8-128">Vaimenna</span><span class="sxs-lookup"><span data-stu-id="a3ff8-128">Mute</span></span>                  | <span data-ttu-id="a3ff8-129">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-129">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-130">Kun arvoksi on määritetty **Tosi**, ääni on vaimennettu.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="a3ff8-131">Tämän toistimen oletusarvo on **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="a3ff8-132">Chrome-selaimessa automaattisen toiston videot vaimennetaan oletusarvoisesti. Ääni toistetaan vain, jos käyttäjä toistaa videon manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="a3ff8-133">Silmukka</span><span class="sxs-lookup"><span data-stu-id="a3ff8-133">Loop</span></span>                  | <span data-ttu-id="a3ff8-134">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-134">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-135">Kun arvoksi on määritetty **Tosi**, video toistetaan silmukassa.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="a3ff8-136">Mediat</span><span class="sxs-lookup"><span data-stu-id="a3ff8-136">Media</span></span>                 | <span data-ttu-id="a3ff8-137">Videotiedostopolku ja -nimi</span><span class="sxs-lookup"><span data-stu-id="a3ff8-137">Video file path and name</span></span> | <span data-ttu-id="a3ff8-138">Videotiedosto, jota videotoistin toistaa.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="a3ff8-139">Toista koko näyttössä</span><span class="sxs-lookup"><span data-stu-id="a3ff8-139">Play fullscreen</span></span>       | <span data-ttu-id="a3ff8-140">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-140">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-141">Kun arvoksi on määritetty **Tosi**, videota toistetaan koko näytön tilassa.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="a3ff8-142">Toiston/keskeytyksen valitsin</span><span class="sxs-lookup"><span data-stu-id="a3ff8-142">Play pause trigger</span></span>    | <span data-ttu-id="a3ff8-143">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-143">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-144">Kun arvoksi on asetettu **Tosi**, videossa näkyy toisto/pysäytys-painike.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="a3ff8-145">Videosoittimen säätimet</span><span class="sxs-lookup"><span data-stu-id="a3ff8-145">Video player controls</span></span> | <span data-ttu-id="a3ff8-146">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-146">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-147">Kun arvoksi on määritetty **Tosi**, kaikki videotoistimen ohjausobjektit näkyvät.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="a3ff8-148">Näitä ohjausobjekteja ovat toisto- ja pysäytyspainikkeet, tilanneilmaisin ja tekstitysvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="a3ff8-149">Piilota julistekuva</span><span class="sxs-lookup"><span data-stu-id="a3ff8-149">Hide poster image</span></span>     | <span data-ttu-id="a3ff8-150">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-150">**True** or **False**</span></span>               | <span data-ttu-id="a3ff8-151">Videossa voi olla julistekehys.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-151">A video can have a poster frame.</span></span> <span data-ttu-id="a3ff8-152">Kun tämän ominaisuuden arvoksi määritetään **Tosi**, julistekehys piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="a3ff8-153">Peitteen taso</span><span class="sxs-lookup"><span data-stu-id="a3ff8-153">Mask level</span></span>            | <span data-ttu-id="a3ff8-154">Numero väliltä **0**–**100**</span><span class="sxs-lookup"><span data-stu-id="a3ff8-154">A number from **0** through **100**</span></span> | <span data-ttu-id="a3ff8-155">Muoto, jota käytetään videon muotoiluun.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="a3ff8-156">Videotoistinmoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="a3ff8-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="a3ff8-157">Video on ennen videotoistinmoduulin luontia ladattava mediakirjastoon.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="a3ff8-158">Voit lisätä videotoistinmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a3ff8-159">Luo sivumalli, jonka nimi on **Videotoistinmalli**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="a3ff8-160">Lisää säilömoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="a3ff8-161">Lisää säilömoduulissa videotoistinmoduuli ja ympäristön videotoistinmoduuli.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="a3ff8-162">Kun mallin muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="a3ff8-163">Käytä luotua videotoistinmallia, kun haluat luoda sivun nimeltä **Videotoistimen sivu**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="a3ff8-164">Lisää videotoistinmoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="a3ff8-165">Valitse videotoistinmoduulin ominaisuusruudussa **Lisää video**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="a3ff8-166">Valitse **Mediavalitsin**-valintaikkunassa video ja valitse sitten **Lataa uusi medianimike**.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="a3ff8-167">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-167">Save and preview the page.</span></span> <span data-ttu-id="a3ff8-168">Videomoduulin pitäisi näkyä sivulla.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-168">You should see the video module on the page.</span></span> <span data-ttu-id="a3ff8-169">Voit muokata moduulin toimintaa muuttamalla lisäasetuksia.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="a3ff8-170">Kun sivun muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="a3ff8-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3ff8-171">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a3ff8-171">Additional resources</span></span>

[<span data-ttu-id="a3ff8-172">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a3ff8-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a3ff8-173">Kampanjabannerimoduuli</span><span class="sxs-lookup"><span data-stu-id="a3ff8-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="a3ff8-174">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="a3ff8-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a3ff8-175">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="a3ff8-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a3ff8-176">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="a3ff8-176">Content block module</span></span>](add-hero-module.md)
