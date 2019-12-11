---
title: Hero-moduuli
description: Tässä ohjeaiheessa on tietoja hero-moduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785385"
---
# <a name="hero-module"></a><span data-ttu-id="1b9a5-103">Hero-moduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1b9a5-104">Tässä ohjeaiheessa on tietoja hero-moduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1b9a5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1b9a5-105">Overview</span></span>

<span data-ttu-id="1b9a5-106">Hero-moduulia käytetään tuotteiden tai kampanjoiden markkinoinnissa kuvien ja tekstin yhdistelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="1b9a5-107">Jälleenmyyjä voi lisätä hero-moduulin esimerkiksi sähköisen kaupankäynnin sivuston aloitussivulle ja mainostaa uutta tuotetta sekä houkutella asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="1b9a5-108">Hero-moduulia ohjaavat sisällönhallintajärjestelmän (CMS) tiedot.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="1b9a5-109">Se on itsenäinen moduuli, joka ei ole riippuvainen sivun muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="1b9a5-110">Hero-moduuli voidaan sijoittaa mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, myyntiä tai ominaisuuksia).</span><span class="sxs-lookup"><span data-stu-id="1b9a5-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="1b9a5-111">Esimerkkejä sähköisen kaupankäynnin hero-moduulista</span><span class="sxs-lookup"><span data-stu-id="1b9a5-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="1b9a5-112">Hero-moduulia voidaan käyttää sähköisen kaupankäynnin sivuston aloitussivulla kampanjoiden ja uusien tuotteiden esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="1b9a5-113">Hero-moduulia voi käyttää tuotetietosivulla tuotetietojen esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="1b9a5-114">Karusellimoduulin sisään voi asettaa useita hero-moduuleita. Näin voidaan esitellä useita tuotteita tai kampanjoita.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="1b9a5-115">Hero-moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1b9a5-115">Hero module properties</span></span>

| <span data-ttu-id="1b9a5-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="1b9a5-116">Property name</span></span>  | <span data-ttu-id="1b9a5-117">Arvot</span><span class="sxs-lookup"><span data-stu-id="1b9a5-117">Values</span></span> | <span data-ttu-id="1b9a5-118">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1b9a5-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1b9a5-119">Kuva</span><span class="sxs-lookup"><span data-stu-id="1b9a5-119">Image</span></span>          | <span data-ttu-id="1b9a5-120">Kuvatiedosto</span><span class="sxs-lookup"><span data-stu-id="1b9a5-120">Image file</span></span> | <span data-ttu-id="1b9a5-121">Kuvan avulla voidaan esitellä tuotetta tai kampanjaa.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="1b9a5-122">Kuvan voi ladata kuvavalikoimaan. Myös olemassa olevaa kuvaa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="1b9a5-123">Otsikko</span><span class="sxs-lookup"><span data-stu-id="1b9a5-123">Heading</span></span>        | <span data-ttu-id="1b9a5-124">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="1b9a5-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1b9a5-125">Jokaisella hero-moduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-125">Every hero module can have a heading.</span></span> <span data-ttu-id="1b9a5-126">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="1b9a5-127">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="1b9a5-128">Kappale</span><span class="sxs-lookup"><span data-stu-id="1b9a5-128">Paragraph</span></span>      | <span data-ttu-id="1b9a5-129">Kappaleen teksti</span><span class="sxs-lookup"><span data-stu-id="1b9a5-129">Paragraph text</span></span> | <span data-ttu-id="1b9a5-130">Hero-moduulit tukevat kappaleen tekstiä RTF-muodossa.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="1b9a5-131">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="1b9a5-132">Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="1b9a5-133">Linkitä</span><span class="sxs-lookup"><span data-stu-id="1b9a5-133">Link</span></span>           | <span data-ttu-id="1b9a5-134">Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä**</span><span class="sxs-lookup"><span data-stu-id="1b9a5-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="1b9a5-135">Hero-moduulit tukevat vähintään yhtä toimintokutsulinkkiä.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="1b9a5-136">Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="1b9a5-137">ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="1b9a5-138">Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="1b9a5-139">Tekstin sijoittelu</span><span class="sxs-lookup"><span data-stu-id="1b9a5-139">Text placement</span></span> | <span data-ttu-id="1b9a5-140">**Ylhäällä vasemmalla**, **ylhäällä oikealla**, **ylhäällä keskellä**, **alhaalla vasemmalla**, **alhaalla oikealla**, **alhaalla keskellä**, **keskellä vasemmalla**, **keskellä oikealla** tai **keskellä keskellä**</span><span class="sxs-lookup"><span data-stu-id="1b9a5-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="1b9a5-141">Tämä ominaisuus määrittää kuvan sijainnin suhteessa tekstiin.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="1b9a5-142">Jos valittuna on esimerkiksi **oikea**, kuva näkyy tekstin oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="1b9a5-143">Tekstin teema</span><span class="sxs-lookup"><span data-stu-id="1b9a5-143">Text theme</span></span>     | <span data-ttu-id="1b9a5-144">**Vaalea** tai **tumma**</span><span class="sxs-lookup"><span data-stu-id="1b9a5-144">**Light** or **Dark**</span></span> | <span data-ttu-id="1b9a5-145">Tekstille voi määrittää väriteeman taustakuvan perusteella.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="1b9a5-146">Jos kuvalla on esimerkiksi tumma tausta, voidaan käyttää vaaleampaa teemaa. Näin teksti näkyy paremmin ja helppokäyttötoimintojen värikontrastisuhde otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="1b9a5-147">Liukuväri</span><span class="sxs-lookup"><span data-stu-id="1b9a5-147">Gradient</span></span>       | <span data-ttu-id="1b9a5-148">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="1b9a5-148">**True** or **False**</span></span> | <span data-ttu-id="1b9a5-149">Kuvassa voidaan käyttää liukuväriä, jotta helppokäyttötoimintojen kontrastisuhteet otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="1b9a5-150">Hero-moduulin lisääminen uudelle sivulle</span><span class="sxs-lookup"><span data-stu-id="1b9a5-150">Add a hero module to a new page</span></span>

<span data-ttu-id="1b9a5-151">Voit lisätä hero-moduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1b9a5-152">Siirry kohtaan **Mallit**ja luo sivumalli, jonka nimi on **Hero-malli**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="1b9a5-153">Lisää hero-moduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="1b9a5-154">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="1b9a5-155">Käytä juuri luotua hero-mallia, kun haluat luoda sivun nimeltä **Hero-sivu**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="1b9a5-156">Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1b9a5-157">Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -kohdassa hero-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="1b9a5-158">Valitse vasemmanpuoleisen jäsennyspuun hero-moduuli.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="1b9a5-159">Valitse oikeanpuoleisessa ominaisuusruudussa **Lisää kuva**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="1b9a5-160">Valitse joko olemassa oleva kuva tai lataa uusi kuva.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="1b9a5-161">Valitse **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-161">Select **Heading**.</span></span>
1. <span data-ttu-id="1b9a5-162">Lisää **Otsikko**-valintaikkunaan otsikon teksti. Valitse otsikkotaso ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="1b9a5-163">Lisää **Rich Text** -kohtaan haluamasi teksti.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="1b9a5-164">Valitse **Lisää toimintolinkki**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="1b9a5-165">Lisää **Toimintolinkki**-valintaikkunaan linkin teksti, linkin URL-osoite ja linkin ARIA-otsikko. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="1b9a5-166">Tallenna sivu ja esikatsele muutokset.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="1b9a5-167">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="1b9a5-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b9a5-168">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1b9a5-168">Additional resources</span></span>

[<span data-ttu-id="1b9a5-169">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1b9a5-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1b9a5-170">Hälytysmoduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="1b9a5-171">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1b9a5-172">Sisällöntäyteinen lohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1b9a5-173">Sisällönsijoittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="1b9a5-174">Omaisuusmoduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="1b9a5-175">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="1b9a5-175">Video player module</span></span>](add-video-player.md)
