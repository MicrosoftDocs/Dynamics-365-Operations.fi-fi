---
title: Esimääritettyjen asettelujen käyttö
description: Tässä ohjeaiheessa käsitellään esimääritettyjen asettelujen käsittelemistä Microsoft Dynamics 365 Commercessa.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2539880e76ffb1861e0d18227a935a2ef35c120
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210872"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="aa435-103">Esimääritettyjen asettelujen käyttö</span><span class="sxs-lookup"><span data-stu-id="aa435-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aa435-104">Tässä ohjeaiheessa käsitellään esimääritettyjen asettelujen käsittelemistä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="aa435-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aa435-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="aa435-105">Overview</span></span>

<span data-ttu-id="aa435-106">Ennen kuin suoritat tämän ohjeaiheen toiminnot, muista tutustua kohtaan [Esimääritetyt ja mukautetut asettelut](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="aa435-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="aa435-107">Yleinen yleiskuvaus on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="aa435-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="aa435-108">Uuden esimääritetyn asettelun luominen</span><span class="sxs-lookup"><span data-stu-id="aa435-108">Create a new preset layout</span></span>

<span data-ttu-id="aa435-109">Esimääritetty asettelu voidaan luoda kahdella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="aa435-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="aa435-110">Voit tallentaa aiemmin luodun mukautetun asettelun uudeksi esimääritetyksi asetteluksi tai luoda esimääritetyn asettelun alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="aa435-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="aa435-111">Esimääritetyn asettelun luominen aiemmin luodusta mukautetusta asettelusta</span><span class="sxs-lookup"><span data-stu-id="aa435-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="aa435-112">Voit luoda esimääritetyn asettelun aiemmin luodusta mukautetusta asettelusta seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="aa435-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="aa435-113">Avaa aiemmin luotu sivu, joka ei tällä hetkellä käytä esimääritettyä asettelua ja jonka moduulirakennetta haluat käyttää muilla sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="aa435-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="aa435-114">Valitse **Muokkaa** tarkistaaksesi sivun.</span><span class="sxs-lookup"><span data-stu-id="aa435-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="aa435-115">Valitse **Tallenna uutena asetteluna**.</span><span class="sxs-lookup"><span data-stu-id="aa435-115">Select **Save as new layout**.</span></span> <span data-ttu-id="aa435-116">**Tallenna uutena asetteluna** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="aa435-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="aa435-117">Kirjoita esimääritetyn asettelun nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="aa435-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="aa435-118">Syöttämäsi arvot näkyvät muille tekijöille, kun ne luovat uusia sivuja asettelusta tai siirtyvät siihen.</span><span class="sxs-lookup"><span data-stu-id="aa435-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="aa435-119">Anna sen vuoksi arvoja, joista on hyötyä sivujen tekijöille.</span><span class="sxs-lookup"><span data-stu-id="aa435-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="aa435-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa435-120">Select **OK**.</span></span>

<span data-ttu-id="aa435-121">Esimääritetty asettelu on nyt käytettävissä, kun luotu uusia sivuja tai valitset toisen asettelun saman mallihierarkian sivulle.</span><span class="sxs-lookup"><span data-stu-id="aa435-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="aa435-122">Voit tarkistaa nopeasti, onko tietty sivu sidottu esimääritettyyn asetteluun, valitsemalla sivuluettelonäkymän sivun ja tarkastamalla asettelun metatiedot oikeanpuoleisessa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="aa435-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="aa435-123">Uuden esimääritetyn asettelun luominen</span><span class="sxs-lookup"><span data-stu-id="aa435-123">Create a new preset layout</span></span>

<span data-ttu-id="aa435-124">Voit luoda esimääritetyn asettelun alusta alkaen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="aa435-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="aa435-125">Valitse vasemmanpuoleisessa siirtymisruudussa **Asettelut**.</span><span class="sxs-lookup"><span data-stu-id="aa435-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="aa435-126">Valitse **Uusi asettelu**.</span><span class="sxs-lookup"><span data-stu-id="aa435-126">Select **New Layout**.</span></span> <span data-ttu-id="aa435-127">**Uusi asettelu** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="aa435-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="aa435-128">Valitse esimääritetyssä asettelussa käytettävä malli.</span><span class="sxs-lookup"><span data-stu-id="aa435-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="aa435-129">Kirjoita esimääritetyn asettelun nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="aa435-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="aa435-130">Syöttämäsi arvot näkyvät muille tekijöille, kun ne luovat uusia sivuja asettelusta tai siirtyvät siihen.</span><span class="sxs-lookup"><span data-stu-id="aa435-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="aa435-131">Anna sen vuoksi arvoja, joista on hyötyä sivujen tekijöille.</span><span class="sxs-lookup"><span data-stu-id="aa435-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="aa435-132">Luo uusi esimääritetty asettelu ja avaa asettelueditori valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa435-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="aa435-133">Lisää moduulit asettelueditoriin ja määritä ne siellä käyttämällä jäsennyspuuta vasemmalla ja ominaisuusruutua oikealla.</span><span class="sxs-lookup"><span data-stu-id="aa435-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="aa435-134">(Prosessi muistuttaa moduulien lisäämistä ja määrittämistä mallieditorin mallissa.) Moduulien järjestys ja mahdolliset lukitut oletusasetukset ovat keskitetyn moduulin määrityksessä kaikissa tätä esimääritettyä asettelua käyttävillä sivuilla.</span><span class="sxs-lookup"><span data-stu-id="aa435-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="aa435-135">Esimääritetyn asettelun muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="aa435-135">Modify a preset layout</span></span>

<span data-ttu-id="aa435-136">Voit muokata esimääritettyä asettelua seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="aa435-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="aa435-137">Valitse vasemmanpuoleisessa siirtymisruudussa **Asettelut**.</span><span class="sxs-lookup"><span data-stu-id="aa435-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="aa435-138">Valitse muokattava moduuli asettelueditorissa jäsennyspuussa vasemmalla.</span><span class="sxs-lookup"><span data-stu-id="aa435-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="aa435-139">Tee sitten jokin seuraavista toiminnoista:</span><span class="sxs-lookup"><span data-stu-id="aa435-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="aa435-140">Jos haluat siirtää moduulia ylös- tai alaspäin päätasolla, valitse moduulin kolmen pisteen painike (**...**) ja valitse sitten **Siirrä ylös** tai **Siirrä alas**.</span><span class="sxs-lookup"><span data-stu-id="aa435-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="aa435-141">Jos haluat muuttaa moduulin oletusasetuksia, määritä oletusarvot ominaisuusruudun avulla. Halutessasi voit lukita ne verkosta tietoa lataavia sivuja varten.</span><span class="sxs-lookup"><span data-stu-id="aa435-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="aa435-142">Jos haluat lisätä uusia moduuleja tai osia säilömoduuleihin, valitse kolmen pisteen painike ja valitse sitten **Lisää moduuli**- tai **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="aa435-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="aa435-143">Jos haluat poistaa moduulin asettelusta, valitse kolmen pisteen painike ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="aa435-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="aa435-144">Esimääritetyn asettelun teeman muuttaminen</span><span class="sxs-lookup"><span data-stu-id="aa435-144">Change a preset layout theme</span></span>

<span data-ttu-id="aa435-145">Normaali käytäntö on määrittää oletusteema kaikille sivuille, jotka käyttävät esimääritettyä asettelua.</span><span class="sxs-lookup"><span data-stu-id="aa435-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="aa435-146">Seuraavalla tavalla voit määrittää kaikkien niiden alisivujen teeman, jotka käyttävät valmista asettelua, tai muuttaa sitä.</span><span class="sxs-lookup"><span data-stu-id="aa435-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="aa435-147">Valitse sivun säilömoduuli asettelueditorissa jäsennyspuussa vasemmalla.</span><span class="sxs-lookup"><span data-stu-id="aa435-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="aa435-148">(Yleensä tämä moduuli on toinen solmu, ja sen nimi on **Oletussivu**.)</span><span class="sxs-lookup"><span data-stu-id="aa435-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="aa435-149">Valitse oikealla olevan ominaisuusruudun **Teema**-kentässä teema.</span><span class="sxs-lookup"><span data-stu-id="aa435-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="aa435-150">Esimääritetyn asettelun tallentaminen kirjaaminen sisään, esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="aa435-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="aa435-151">Voit tallentaa esimääritetyn asettelun ja kirjata sen sisään seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="aa435-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="aa435-152">Valitse **Tallenna** asettelueditorin yläosassa.</span><span class="sxs-lookup"><span data-stu-id="aa435-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="aa435-153">Tallennetut muutokset eivät vaikuta verkosta tietoja lataaviin sivuihin, ennen kuin ne on kuitattu sisään.</span><span class="sxs-lookup"><span data-stu-id="aa435-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="aa435-154">Valitse **Viimeistele muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="aa435-154">Select **Finish editing**.</span></span> <span data-ttu-id="aa435-155">Tekemäsi muutokset ovat nyt verkosta tietoja lataavien työnkulkujen löydettävissä.</span><span class="sxs-lookup"><span data-stu-id="aa435-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="aa435-156">Voit esikatsella muutoksia avaamalla olemassa olevan esimääritettyä asettelua käyttävän sivun tai luomalla uuden sivun asettelusta.</span><span class="sxs-lookup"><span data-stu-id="aa435-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="aa435-157">Kun olet esikatsellut esimääritettyyn asetteluun tehdyt muutokset, julkaise asettelu live-sivustossa jonkin seuraavan vaiheen avulla.</span><span class="sxs-lookup"><span data-stu-id="aa435-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="aa435-158">Siirry **Asettelut**-kohtaan, valitse asettelu ja valitse sitten **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="aa435-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="aa435-159">Valitse asettelun nimi avataksesi asettelueditorin ja valitse sitten **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="aa435-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="aa435-160">Julkaise sivu, joka viittaa julkaisemattomaan asetteluun.</span><span class="sxs-lookup"><span data-stu-id="aa435-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="aa435-161">Asettelu julkaistaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="aa435-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="aa435-162">Useat sivut voivat viitata esimääritettyihin asetteluihin.</span><span class="sxs-lookup"><span data-stu-id="aa435-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="aa435-163">Kun julkaiset esimääritetyn asettelun, ota huomioon, että saatat vaikuttaa useiden sivujen asetteluun.</span><span class="sxs-lookup"><span data-stu-id="aa435-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa435-164">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="aa435-164">Additional resources</span></span>

[<span data-ttu-id="aa435-165">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="aa435-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="aa435-166">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="aa435-166">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]