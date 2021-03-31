---
title: Sisältölohkomoduuli
description: Tässä ohjeaiheessa on tietoja sisältölohkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: ad95dc943f075e088f5e13b507fa08f11548282f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206268"
---
# <a name="content-block-module"></a><span data-ttu-id="d1295-103">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="d1295-103">Content block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1295-104">Tässä ohjeaiheessa on tietoja sisältölohkomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="d1295-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d1295-105">Sisältölohkomoduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa yhdistämällä kuvia ja tekstiä.</span><span class="sxs-lookup"><span data-stu-id="d1295-105">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="d1295-106">Jälleenmyyjä voi lisätä sisältölohkomoduulin esimerkiksi sähköisen kaupankäynnin sivuston aloitussivulle mainostamaan uutta tuotetta ja houkuttelemaan asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="d1295-106">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="d1295-107">Sisällönhallintajärjestelmän (CMS) tiedot ohjaavat sisältölohkomoduulia.</span><span class="sxs-lookup"><span data-stu-id="d1295-107">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="d1295-108">Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="d1295-108">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="d1295-109">Sisältölohkomoduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).</span><span class="sxs-lookup"><span data-stu-id="d1295-109">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="d1295-110">Esimerkkejä sähköisen kaupankäynnin sisältölohkomoduuleista</span><span class="sxs-lookup"><span data-stu-id="d1295-110">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="d1295-111">Sisältölohkomoduulia voidaan käyttää sähköisen kaupankäynnin sivuston aloitussivulla kampanjoiden ja uusien tuotteiden esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="d1295-111">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="d1295-112">Sisältölohkomoduulia voi käyttää tuotetietosivulla tuotetietojen esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="d1295-112">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="d1295-113">Karusellimoduulin sisään voi asettaa useita sisältölohkomoduuleita, joilla voidaan esitellä useita tuotteita tai kampanjoita.</span><span class="sxs-lookup"><span data-stu-id="d1295-113">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="d1295-114">Sisältölohkomoduulit ja teemat</span><span class="sxs-lookup"><span data-stu-id="d1295-114">Content block modules and themes</span></span>

<span data-ttu-id="d1295-115">Sisältölohkomoduulit voivat tukea erilaisia teemaan perustuvia asetteluja ja tyylejä.</span><span class="sxs-lookup"><span data-stu-id="d1295-115">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="d1295-116">Esimerkiksi Fabrikam-teema tukee kolmea sisältölohkomoduulin asetteluversiota: hero, ominaisuus ja ruutu.</span><span class="sxs-lookup"><span data-stu-id="d1295-116">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="d1295-117">Hero-asettelu näyttää taustalla kuvan ja sen päällä tekstin.</span><span class="sxs-lookup"><span data-stu-id="d1295-117">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="d1295-118">Ominaisuusasettelussa kuva ja teksti näytetään rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="d1295-118">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="d1295-119">Ruutuasettelu mahdollistaa useiden sisältölohkojen käytön ruutumuodossa.</span><span class="sxs-lookup"><span data-stu-id="d1295-119">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="d1295-120">Teema voi lisäksi tuoda esille kunkin asettelun erilaisia ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="d1295-120">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="d1295-121">Teeman kehittäjä voi muodostaa sisältölohkomoduulin avulla lisää asetteluja ja tyylejä.</span><span class="sxs-lookup"><span data-stu-id="d1295-121">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="d1295-122">Seuraavassa kuvassa on esimerkki hero-asettelua käyttävästä sisältölohkomoduulista.</span><span class="sxs-lookup"><span data-stu-id="d1295-122">The following image shows an example of a content block module with a hero layout.</span></span>

![Esimerkki hero-moduulista](./media/Hero.PNG)

<span data-ttu-id="d1295-124">Seuraavassa kuvassa on esimerkki ominaisuusasettelua käyttävästä sisältölohkomoduulista.</span><span class="sxs-lookup"><span data-stu-id="d1295-124">The following image shows an example of a content block module with a feature layout.</span></span>

![Esimerkkejä ominaisuusmoduuleista](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="d1295-126">Sisältölohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d1295-126">Content block module properties</span></span>

| <span data-ttu-id="d1295-127">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="d1295-127">Property name</span></span>  | <span data-ttu-id="d1295-128">Arvot</span><span class="sxs-lookup"><span data-stu-id="d1295-128">Values</span></span> | <span data-ttu-id="d1295-129">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1295-129">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d1295-130">Kuva</span><span class="sxs-lookup"><span data-stu-id="d1295-130">Image</span></span>          | <span data-ttu-id="d1295-131">Kuvatiedosto</span><span class="sxs-lookup"><span data-stu-id="d1295-131">Image file</span></span> | <span data-ttu-id="d1295-132">Kuvan avulla voidaan esitellä tuotetta tai kampanjaa.</span><span class="sxs-lookup"><span data-stu-id="d1295-132">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="d1295-133">Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="d1295-133">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="d1295-134">Otsikko</span><span class="sxs-lookup"><span data-stu-id="d1295-134">Heading</span></span>        | <span data-ttu-id="d1295-135">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="d1295-135">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d1295-136">Jokaisella hero-moduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="d1295-136">Every hero module can have a heading.</span></span> <span data-ttu-id="d1295-137">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="d1295-137">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="d1295-138">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="d1295-138">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="d1295-139">Kappale</span><span class="sxs-lookup"><span data-stu-id="d1295-139">Paragraph</span></span>      | <span data-ttu-id="d1295-140">Kappaleen teksti</span><span class="sxs-lookup"><span data-stu-id="d1295-140">Paragraph text</span></span> | <span data-ttu-id="d1295-141">Hero-moduulit tukevat kappaleen tekstiä RTF-muodossa.</span><span class="sxs-lookup"><span data-stu-id="d1295-141">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="d1295-142">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit.</span><span class="sxs-lookup"><span data-stu-id="d1295-142">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="d1295-143">Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="d1295-143">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="d1295-144">Linkitä</span><span class="sxs-lookup"><span data-stu-id="d1295-144">Link</span></span>           | <span data-ttu-id="d1295-145">Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä**</span><span class="sxs-lookup"><span data-stu-id="d1295-145">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="d1295-146">Hero-moduulit tukevat vähintään yhtä toimintokutsulinkkiä.</span><span class="sxs-lookup"><span data-stu-id="d1295-146">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="d1295-147">Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="d1295-147">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="d1295-148">ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="d1295-148">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="d1295-149">Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen.</span><span class="sxs-lookup"><span data-stu-id="d1295-149">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="d1295-150">Fabrikam-teeman näyttämät sisältölohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d1295-150">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="d1295-151">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="d1295-151">Property name</span></span>  | <span data-ttu-id="d1295-152">Arvot</span><span class="sxs-lookup"><span data-stu-id="d1295-152">Values</span></span> | <span data-ttu-id="d1295-153">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d1295-153">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d1295-154">Tekstin sijoittelu</span><span class="sxs-lookup"><span data-stu-id="d1295-154">Text placement</span></span> | <span data-ttu-id="d1295-155">**Vasen**, **Oikea**, **Keskitys**</span><span class="sxs-lookup"><span data-stu-id="d1295-155">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="d1295-156">Tämä ominaisuus määrittää kuvan päällä olevan tekstin sijainnin.</span><span class="sxs-lookup"><span data-stu-id="d1295-156">This property defines the position of the text on the image.</span></span> <span data-ttu-id="d1295-157">Se koskee vain hero-asettelua.</span><span class="sxs-lookup"><span data-stu-id="d1295-157">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="d1295-158">Tekstin teema</span><span class="sxs-lookup"><span data-stu-id="d1295-158">Text theme</span></span>     | <span data-ttu-id="d1295-159">**Vaalea** tai **tumma**</span><span class="sxs-lookup"><span data-stu-id="d1295-159">**Light** or **Dark**</span></span> | <span data-ttu-id="d1295-160">Tekstille voi määrittää väriteeman taustakuvan perusteella.</span><span class="sxs-lookup"><span data-stu-id="d1295-160">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="d1295-161">Jos kuvalla on esimerkiksi tumma tausta, voidaan käyttää vaaleampaa teemaa. Näin teksti näkyy paremmin ja helppokäyttötoimintojen värikontrastisuhde otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="d1295-161">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="d1295-162">Se koskee vain hero-asettelua.</span><span class="sxs-lookup"><span data-stu-id="d1295-162">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="d1295-163">Kuvan sijoittelu</span><span class="sxs-lookup"><span data-stu-id="d1295-163">Image placement</span></span>       | <span data-ttu-id="d1295-164">**Vasen**, **Oikea**</span><span class="sxs-lookup"><span data-stu-id="d1295-164">**Left**,  **Right**</span></span> | <span data-ttu-id="d1295-165">Tämä ominaisuus määrittää, onko kuvan oltava tekstin vasemmalla vai oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="d1295-165">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="d1295-166">Se koskee vain ominaisuusasettelua.</span><span class="sxs-lookup"><span data-stu-id="d1295-166">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="d1295-167">Sisältölohkomoduulin lisääminen uudelle sivulle</span><span class="sxs-lookup"><span data-stu-id="d1295-167">Add a content block module to a new page</span></span>

<span data-ttu-id="d1295-168">Voit lisätä hero-moduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d1295-168">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d1295-169">Valitse **Mallit** ja luo sivumalli, jonka nimi on **Sisältölohkomalli**.</span><span class="sxs-lookup"><span data-stu-id="d1295-169">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="d1295-170">Lisää hero-moduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="d1295-170">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="d1295-171">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="d1295-171">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d1295-172">Luo **Sisältölohkosivu**-niminen sivu käyttämällä juuri luotua hero-mallia.</span><span class="sxs-lookup"><span data-stu-id="d1295-172">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="d1295-173">Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="d1295-173">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d1295-174">Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -kohdassa hero-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1295-174">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="d1295-175">Valitse vasemmanpuoleisen jäsennyspuun sisältölohkomoduuli.</span><span class="sxs-lookup"><span data-stu-id="d1295-175">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="d1295-176">Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää kuva**.</span><span class="sxs-lookup"><span data-stu-id="d1295-176">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="d1295-177">Valitse joko olemassa oleva kuva tai lataa uusi kuva.</span><span class="sxs-lookup"><span data-stu-id="d1295-177">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="d1295-178">Valitse **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="d1295-178">Select **Heading**.</span></span>
1. <span data-ttu-id="d1295-179">Lisää **Otsikko**-valintaikkunaan otsikon teksti. Valitse otsikkotaso ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1295-179">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="d1295-180">Lisää **Rich Text** -kohtaan haluamasi teksti.</span><span class="sxs-lookup"><span data-stu-id="d1295-180">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="d1295-181">Valitse **Lisää linkki**.</span><span class="sxs-lookup"><span data-stu-id="d1295-181">Select **Add Link**.</span></span>
1. <span data-ttu-id="d1295-182">Lisää **Linkki**-valintaikkunaan linkin teksti, linkin URL-osoite ja linkin ARIA-otsikko. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1295-182">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="d1295-183">Valitse **Hero**-asettelu.</span><span class="sxs-lookup"><span data-stu-id="d1295-183">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="d1295-184">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="d1295-184">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d1295-185">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="d1295-185">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d1295-186">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d1295-186">Additional resources</span></span>

[<span data-ttu-id="d1295-187">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d1295-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d1295-188">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="d1295-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="d1295-189">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="d1295-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d1295-190">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="d1295-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d1295-191">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="d1295-191">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]