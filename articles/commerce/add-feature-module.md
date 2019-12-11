---
title: Omaisuusmoduuli
description: Tässä ohjeaiheessa on tietoja ominaisuusmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785280"
---
# <a name="feature-module"></a><span data-ttu-id="aad39-103">Omaisuusmoduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="aad39-104">Tässä ohjeaiheessa on tietoja ominaisuusmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="aad39-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aad39-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="aad39-105">Overview</span></span>

<span data-ttu-id="aad39-106">Ominaisuusmoduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa kuvien ja tekstin yhdistelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="aad39-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="aad39-107">Esimerkiksi jälleenmyyjä voi lisätä ominaisuusmoduulin tuotetietosivulle ja näin korostaa tuotteen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="aad39-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="aad39-108">Ominaisuusmoduulia ohjaavat sisällönhallintajärjestelmän (CMS) tiedot.</span><span class="sxs-lookup"><span data-stu-id="aad39-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="aad39-109">Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="aad39-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="aad39-110">Ominaisuusmoduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).</span><span class="sxs-lookup"><span data-stu-id="aad39-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="aad39-111">Esimerkkejä sähköisen kaupankäynnin ominaisuusmoduuleista</span><span class="sxs-lookup"><span data-stu-id="aad39-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="aad39-112">Ominaisuusmoduulia voi käyttää seuraavilla sivuilla:</span><span class="sxs-lookup"><span data-stu-id="aad39-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="aad39-113">Tuotetietosivu, jossa esitellään tuotteen ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="aad39-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="aad39-114">Aloitussivu, jolla mainostetaan tuotteita</span><span class="sxs-lookup"><span data-stu-id="aad39-114">The home page, to promote products</span></span>
- <span data-ttu-id="aad39-115">Luokkasivu, jolla kerrotaan tuoteluokista</span><span class="sxs-lookup"><span data-stu-id="aad39-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="aad39-116">Ominaisuusmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="aad39-116">Feature module properties</span></span>

| <span data-ttu-id="aad39-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="aad39-117">Property name</span></span>     | <span data-ttu-id="aad39-118">Arvot</span><span class="sxs-lookup"><span data-stu-id="aad39-118">Values</span></span> | <span data-ttu-id="aad39-119">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="aad39-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="aad39-120">Kuva</span><span class="sxs-lookup"><span data-stu-id="aad39-120">Image</span></span>             | <span data-ttu-id="aad39-121">Kuvatiedosto</span><span class="sxs-lookup"><span data-stu-id="aad39-121">Image file</span></span> | <span data-ttu-id="aad39-122">Kuvan avulla voidaan markkinoida tuotetta tai kampanjaa.</span><span class="sxs-lookup"><span data-stu-id="aad39-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="aad39-123">Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="aad39-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="aad39-124">Otsikko</span><span class="sxs-lookup"><span data-stu-id="aad39-124">Heading</span></span>           | <span data-ttu-id="aad39-125">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="aad39-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="aad39-126">Jokaisella ominaisuusmoduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="aad39-126">Every feature module can have a heading.</span></span> <span data-ttu-id="aad39-127">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="aad39-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="aad39-128">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="aad39-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="aad39-129">Kappale</span><span class="sxs-lookup"><span data-stu-id="aad39-129">Paragraph</span></span>         | <span data-ttu-id="aad39-130">Kappaleen teksti</span><span class="sxs-lookup"><span data-stu-id="aad39-130">Paragraph text</span></span> | <span data-ttu-id="aad39-131">Ominaisuusmoduulit tukevat kappaleen tekstiä RTF-muodossa.</span><span class="sxs-lookup"><span data-stu-id="aad39-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="aad39-132">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit.</span><span class="sxs-lookup"><span data-stu-id="aad39-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="aad39-133">Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="aad39-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="aad39-134">Linkitä</span><span class="sxs-lookup"><span data-stu-id="aad39-134">Link</span></span>              | <span data-ttu-id="aad39-135">Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä**</span><span class="sxs-lookup"><span data-stu-id="aad39-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="aad39-136">Ominaisuusmoduulit tukevat vähintään yhtä toimintokutsulinkkiä.</span><span class="sxs-lookup"><span data-stu-id="aad39-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="aad39-137">Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="aad39-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="aad39-138">ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="aad39-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="aad39-139">Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen.</span><span class="sxs-lookup"><span data-stu-id="aad39-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="aad39-140">Kuvan sijoittelu</span><span class="sxs-lookup"><span data-stu-id="aad39-140">Image placement</span></span>   | <span data-ttu-id="aad39-141">**Oikea**, **vasen**, **yläosa** tai **alaosa**</span><span class="sxs-lookup"><span data-stu-id="aad39-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="aad39-142">Tämä ominaisuus määrittää kuvan sijainnin suhteessa tekstiin.</span><span class="sxs-lookup"><span data-stu-id="aad39-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="aad39-143">Jos valittuna on esimerkiksi **oikea**, kuva näkyy tekstin oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="aad39-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="aad39-144">Kuvasarakkeen koko</span><span class="sxs-lookup"><span data-stu-id="aad39-144">Image column size</span></span> | <span data-ttu-id="aad39-145">Arvo väliltä **1**–**12**</span><span class="sxs-lookup"><span data-stu-id="aad39-145">A value from **1** through **12**</span></span> | <span data-ttu-id="aad39-146">Tämä ominaisuus määrittää kuvan koon suhteessa tekstiin.</span><span class="sxs-lookup"><span data-stu-id="aad39-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="aad39-147">Koko ilmaistaan sivulla olevien sarakkeiden määränä.</span><span class="sxs-lookup"><span data-stu-id="aad39-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="aad39-148">Sivulla on 12 saraketta.</span><span class="sxs-lookup"><span data-stu-id="aad39-148">There are 12 columns on a page.</span></span> <span data-ttu-id="aad39-149">Kuvan ja tekstin koko on sama oletusarvoisesti (kuusi saraketta kummallakin).</span><span class="sxs-lookup"><span data-stu-id="aad39-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="aad39-150">Kokoa voi kuitenkin muuttaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="aad39-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="aad39-151">Ominaisuusmoduulin lisääminen uudelle sivulle</span><span class="sxs-lookup"><span data-stu-id="aad39-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="aad39-152">Voit lisätä ominaisuusmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="aad39-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="aad39-153">Siirry kohtaan **Mallit**ja luo sivumalli, jonka nimi on **Ominaisuusmalli**.</span><span class="sxs-lookup"><span data-stu-id="aad39-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="aad39-154">Lisää ominaisuusmoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="aad39-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="aad39-155">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="aad39-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="aad39-156">Käytä juuri luotua ominaisuusmallia, kun haluat luoda sivun nimeltä **Ominaisuussivu**.</span><span class="sxs-lookup"><span data-stu-id="aad39-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="aad39-157">Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="aad39-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aad39-158">Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -kohdassa ominaisuusmoduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad39-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="aad39-159">Valitse vasemmanpuoleisen jäsennyspuun ominaisuusmoduuli.</span><span class="sxs-lookup"><span data-stu-id="aad39-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="aad39-160">Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää kuva**.</span><span class="sxs-lookup"><span data-stu-id="aad39-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="aad39-161">Valitse joko olemassa oleva kuva tai lataa uusi kuva.</span><span class="sxs-lookup"><span data-stu-id="aad39-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="aad39-162">Valitse **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="aad39-162">Select **Heading**.</span></span>
1. <span data-ttu-id="aad39-163">Lisää **Otsikko**-valintaikkunaan otsikon teksti. Valitse otsikkotaso ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad39-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="aad39-164">Lisää **Rich Text** -kohtaan haluamasi teksti.</span><span class="sxs-lookup"><span data-stu-id="aad39-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="aad39-165">Valitse **Lisää toimintolinkki**.</span><span class="sxs-lookup"><span data-stu-id="aad39-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="aad39-166">Lisää **Toimintolinkki**-valintaikkunaan linkin teksti, linkin URL-osoite ja linkin ARIA-otsikko. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="aad39-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="aad39-167">Tallenna sivu ja esikatsele muutokset.</span><span class="sxs-lookup"><span data-stu-id="aad39-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="aad39-168">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="aad39-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aad39-169">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="aad39-169">Additional resources</span></span>

[<span data-ttu-id="aad39-170">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="aad39-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aad39-171">Hälytysmoduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="aad39-172">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="aad39-173">Sisällöntäyteinen lohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="aad39-174">Sisällönsijoittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="aad39-175">Hero-moduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="aad39-176">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="aad39-176">Video player module</span></span>](add-video-player.md)
