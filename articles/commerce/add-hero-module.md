---
title: Sisältölohkomoduuli
description: Tässä ohjeaiheessa on tietoja sisältölohkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: f91de93ce5ed4813f9f2adbe7678229189b5af2f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025755"
---
# <a name="content-block-module"></a><span data-ttu-id="5c348-103">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="5c348-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5c348-104">Tässä ohjeaiheessa on tietoja sisältölohkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="5c348-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c348-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5c348-105">Overview</span></span>

<span data-ttu-id="5c348-106">Sisältölohkomoduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa yhdistämällä kuvia ja tekstiä.</span><span class="sxs-lookup"><span data-stu-id="5c348-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="5c348-107">Jälleenmyyjä voi lisätä sisältölohkomoduulin esimerkiksi sähköisen kaupankäynnin sivuston aloitussivulle mainostamaan uutta tuotetta ja houkuttelemaan asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="5c348-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="5c348-108">Sisällönhallintajärjestelmän (CMS) tiedot ohjaavat sisältölohkomoduulia.</span><span class="sxs-lookup"><span data-stu-id="5c348-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="5c348-109">Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="5c348-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="5c348-110">Sisältölohkomoduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).</span><span class="sxs-lookup"><span data-stu-id="5c348-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="5c348-111">Esimerkkejä sähköisen kaupankäynnin sisältölohkomoduuleista</span><span class="sxs-lookup"><span data-stu-id="5c348-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="5c348-112">Sisältölohkomoduulia voidaan käyttää sähköisen kaupankäynnin sivuston aloitussivulla kampanjoiden ja uusien tuotteiden esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="5c348-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="5c348-113">Sisältölohkomoduulia voi käyttää tuotetietosivulla tuotetietojen esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="5c348-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="5c348-114">Karusellimoduulin sisään voi asettaa useita sisältölohkomoduuleita, joilla voidaan esitellä useita tuotteita tai kampanjoita.</span><span class="sxs-lookup"><span data-stu-id="5c348-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="5c348-115">Sisältölohkomoduulit ja teemat</span><span class="sxs-lookup"><span data-stu-id="5c348-115">Content block modules and themes</span></span>

<span data-ttu-id="5c348-116">Sisältölohkomoduulit voivat tukea erilaisia teemaan perustuvia asetteluja ja tyylejä.</span><span class="sxs-lookup"><span data-stu-id="5c348-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="5c348-117">Esimerkiksi Fabrikam-teema tukee kolmea sisältölohkomoduulin asetteluversiota: hero, ominaisuus ja ruutu.</span><span class="sxs-lookup"><span data-stu-id="5c348-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="5c348-118">Hero-asettelu näyttää taustalla kuvan ja sen päällä tekstin.</span><span class="sxs-lookup"><span data-stu-id="5c348-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="5c348-119">Ominaisuusasettelussa kuva ja teksti näytetään rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="5c348-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="5c348-120">Ruutuasettelu mahdollistaa useiden sisältölohkojen käytön ruutumuodossa.</span><span class="sxs-lookup"><span data-stu-id="5c348-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="5c348-121">Teema voi lisäksi tuoda esille kunkin asettelun erilaisia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="5c348-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="5c348-122">Teeman kehittäjä voi muodostaa sisältölohkomoduulin avulla lisää asetteluja ja tyylejä.</span><span class="sxs-lookup"><span data-stu-id="5c348-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="5c348-123">Seuraavassa kuvassa on esimerkki hero-asettelua käyttävästä sisältölohkomoduulista.</span><span class="sxs-lookup"><span data-stu-id="5c348-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Esimerkki hero-moduulista](./media/Hero.PNG)

<span data-ttu-id="5c348-125">Seuraavassa kuvassa on esimerkki ominaisuusasettelua käyttävästä sisältölohkomoduulista.</span><span class="sxs-lookup"><span data-stu-id="5c348-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Esimerkkejä ominaisuusmoduuleista](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="5c348-127">Sisältölohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5c348-127">Content block module properties</span></span>

| <span data-ttu-id="5c348-128">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5c348-128">Property name</span></span>  | <span data-ttu-id="5c348-129">Arvot</span><span class="sxs-lookup"><span data-stu-id="5c348-129">Values</span></span> | <span data-ttu-id="5c348-130">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5c348-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="5c348-131">Kuva</span><span class="sxs-lookup"><span data-stu-id="5c348-131">Image</span></span>          | <span data-ttu-id="5c348-132">Kuvatiedosto</span><span class="sxs-lookup"><span data-stu-id="5c348-132">Image file</span></span> | <span data-ttu-id="5c348-133">Kuvan avulla voidaan esitellä tuotetta tai kampanjaa.</span><span class="sxs-lookup"><span data-stu-id="5c348-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="5c348-134">Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="5c348-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="5c348-135">Otsikko</span><span class="sxs-lookup"><span data-stu-id="5c348-135">Heading</span></span>        | <span data-ttu-id="5c348-136">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="5c348-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5c348-137">Jokaisella hero-moduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="5c348-137">Every hero module can have a heading.</span></span> <span data-ttu-id="5c348-138">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="5c348-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="5c348-139">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="5c348-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="5c348-140">Kappale</span><span class="sxs-lookup"><span data-stu-id="5c348-140">Paragraph</span></span>      | <span data-ttu-id="5c348-141">Kappaleen teksti</span><span class="sxs-lookup"><span data-stu-id="5c348-141">Paragraph text</span></span> | <span data-ttu-id="5c348-142">Hero-moduulit tukevat kappaleen tekstiä RTF-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5c348-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="5c348-143">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit.</span><span class="sxs-lookup"><span data-stu-id="5c348-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="5c348-144">Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="5c348-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="5c348-145">Linkitä</span><span class="sxs-lookup"><span data-stu-id="5c348-145">Link</span></span>           | <span data-ttu-id="5c348-146">Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä**</span><span class="sxs-lookup"><span data-stu-id="5c348-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="5c348-147">Hero-moduulit tukevat vähintään yhtä toimintokutsulinkkiä.</span><span class="sxs-lookup"><span data-stu-id="5c348-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="5c348-148">Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="5c348-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="5c348-149">ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="5c348-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="5c348-150">Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen.</span><span class="sxs-lookup"><span data-stu-id="5c348-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="5c348-151">Fabrikam-teeman näyttämät sisältölohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5c348-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="5c348-152">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5c348-152">Property name</span></span>  | <span data-ttu-id="5c348-153">Arvot</span><span class="sxs-lookup"><span data-stu-id="5c348-153">Values</span></span> | <span data-ttu-id="5c348-154">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5c348-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="5c348-155">Tekstin sijoittelu</span><span class="sxs-lookup"><span data-stu-id="5c348-155">Text placement</span></span> | <span data-ttu-id="5c348-156">**Vasen**, **Oikea**, **Keskitys**</span><span class="sxs-lookup"><span data-stu-id="5c348-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="5c348-157">Tämä ominaisuus määrittää kuvan päällä olevan tekstin sijainnin.</span><span class="sxs-lookup"><span data-stu-id="5c348-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="5c348-158">Se koskee vain hero-asettelua.</span><span class="sxs-lookup"><span data-stu-id="5c348-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="5c348-159">Tekstin teema</span><span class="sxs-lookup"><span data-stu-id="5c348-159">Text theme</span></span>     | <span data-ttu-id="5c348-160">**Vaalea** tai **tumma**</span><span class="sxs-lookup"><span data-stu-id="5c348-160">**Light** or **Dark**</span></span> | <span data-ttu-id="5c348-161">Tekstille voi määrittää väriteeman taustakuvan perusteella.</span><span class="sxs-lookup"><span data-stu-id="5c348-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="5c348-162">Jos kuvalla on esimerkiksi tumma tausta, voidaan käyttää vaaleampaa teemaa. Näin teksti näkyy paremmin ja helppokäyttötoimintojen värikontrastisuhde otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="5c348-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="5c348-163">Se koskee vain hero-asettelua.</span><span class="sxs-lookup"><span data-stu-id="5c348-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="5c348-164">Kuvan sijoittelu</span><span class="sxs-lookup"><span data-stu-id="5c348-164">Image placement</span></span>       | <span data-ttu-id="5c348-165">**Vasen**, **Oikea**</span><span class="sxs-lookup"><span data-stu-id="5c348-165">**Left**,  **Right**</span></span> | <span data-ttu-id="5c348-166">Tämä ominaisuus määrittää, onko kuvan oltava tekstin vasemmalla vai oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="5c348-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="5c348-167">Se koskee vain ominaisuusasettelua.</span><span class="sxs-lookup"><span data-stu-id="5c348-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="5c348-168">Sisältölohkomoduulin lisääminen uudelle sivulle</span><span class="sxs-lookup"><span data-stu-id="5c348-168">Add a content block module to a new page</span></span>

<span data-ttu-id="5c348-169">Voit lisätä hero-moduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5c348-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5c348-170">Valitse **Mallit**ja luo sivumalli, jonka nimi on **sisältölohkomalli**.</span><span class="sxs-lookup"><span data-stu-id="5c348-170">Go to **Templates**, and create a page template that is named **content block template**.</span></span>
1. <span data-ttu-id="5c348-171">Lisää hero-moduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="5c348-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="5c348-172">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="5c348-172">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="5c348-173">Luo **sisältölohkosivu**-niminen sivu käyttämällä juuri luotua hero-mallia.</span><span class="sxs-lookup"><span data-stu-id="5c348-173">Use the hero template that you just created to create a page that is named **content block page**.</span></span>
1. <span data-ttu-id="5c348-174">Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="5c348-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5c348-175">Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -kohdassa hero-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c348-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="5c348-176">Valitse vasemmanpuoleisen jäsennyspuun sisältölohkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="5c348-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="5c348-177">Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää kuva**.</span><span class="sxs-lookup"><span data-stu-id="5c348-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="5c348-178">Valitse joko olemassa oleva kuva tai lataa uusi kuva.</span><span class="sxs-lookup"><span data-stu-id="5c348-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="5c348-179">Valitse **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="5c348-179">Select **Heading**.</span></span>
1. <span data-ttu-id="5c348-180">Lisää **Otsikko**-valintaikkunaan otsikon teksti. Valitse otsikkotaso ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c348-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="5c348-181">Lisää **Rich Text** -kohtaan haluamasi teksti.</span><span class="sxs-lookup"><span data-stu-id="5c348-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="5c348-182">Valitse **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="5c348-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="5c348-183">Lisää **Linkki**-valintaikkunaan linkin teksti, linkin URL-osoite ja linkin ARIA-otsikko. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c348-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="5c348-184">Valitse **Hero**-asettelu.</span><span class="sxs-lookup"><span data-stu-id="5c348-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="5c348-185">Tallenna sivu ja esikatsele muutokset.</span><span class="sxs-lookup"><span data-stu-id="5c348-185">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="5c348-186">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="5c348-186">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c348-187">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5c348-187">Additional resources</span></span>

[<span data-ttu-id="5c348-188">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5c348-188">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5c348-189">Kampanjabannerimoduuli</span><span class="sxs-lookup"><span data-stu-id="5c348-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="5c348-190">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="5c348-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="5c348-191">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="5c348-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="5c348-192">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="5c348-192">Video player module</span></span>](add-video-player.md)
