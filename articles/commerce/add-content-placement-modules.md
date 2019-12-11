---
title: Sisällönsijoittelumoduuli
description: Tässä ohjeaiheessa on tietoja sisällönsijoittelu- ja sisällönsijoittelunimikemoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785297"
---
# <a name="content-placement-module"></a><span data-ttu-id="0409f-103">Sisällönsijoittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0409f-104">Tässä ohjeaiheessa on tietoja sisällönsijoittelu- ja sisällönsijoittelunimikemoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="0409f-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0409f-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0409f-105">Overview</span></span>

<span data-ttu-id="0409f-106">Sisällönsijoittelumoduuli on esikoissäilö, jonka muut moduulit voivat sijoittaa tietyn asettelun sisälle.</span><span class="sxs-lookup"><span data-stu-id="0409f-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="0409f-107">Sisällönsijoittelumoduulit tukevat seuraavia moduulityyppejä alimoduuleina: sisällönsijoittelunimike, tilin tervetulonimike, tilin tilausnimike, tilin toivomuslistanimike ja tilin profiilinimike.</span><span class="sxs-lookup"><span data-stu-id="0409f-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="0409f-108">Sisällönsijoittelumoduulit saavat tietoja alimoduuleista, joita ne tukevat.</span><span class="sxs-lookup"><span data-stu-id="0409f-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="0409f-109">Siksi sisällönsijoittelumoduuleja voidaan käyttää eri tavoin siihen lisättyjen moduulien perusteella.</span><span class="sxs-lookup"><span data-stu-id="0409f-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="0409f-110">Sisällönsijoittelunimikemoduulit käyttävät sekä kuvia että tekstiä kampanjoiden, käytäntöjen ja tuoteominaisuuksien esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="0409f-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="0409f-111">Esimerkiksi sisällönsijoittelunimikemoduulia voi käyttää aloitussivulla myymälän käytäntöjen ja toimitustietojen näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="0409f-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="0409f-112">Sisällönsijoittelunimikemoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Ne voidaan sijoittaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="0409f-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="0409f-113">Niitä voidaan kuitenkin käyttää vain sisällönsijoittelumoduulin sisällä.</span><span class="sxs-lookup"><span data-stu-id="0409f-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="0409f-114">Esimerkkejä sähköisen kaupankäynnin sisällönsijoittelumoduuleista</span><span class="sxs-lookup"><span data-stu-id="0409f-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="0409f-115">Sisällönsijoittelumoduuleja, jotka sisältävät sisällönsijoittelunimikemoduuleja, voidaan käyttää aloitussivulla tai markkinointisivuilla, kun kuvien että tekstin avulla halutaan esitellä tuotteen toimintoja, kampanjoita, myymälän käytäntöjä, toimitustietoja ja muita tietoja.</span><span class="sxs-lookup"><span data-stu-id="0409f-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="0409f-116">Sisällönsijoittelumoduuleja, jotka sisältävät sisällönsijoittelunimikemoduuleja, voidaan käyttää tuotetietosivuilla tuoteominaisuuksien esittelyssä.</span><span class="sxs-lookup"><span data-stu-id="0409f-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="0409f-117">Sisällönsijoittelumoduuleja, jotka sisältävät tilin tervetulonimike- tai tilin tilausnimikemoduulin, voidaan käyttää tilinhallintasivuilla.</span><span class="sxs-lookup"><span data-stu-id="0409f-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="0409f-118">Sisällönsijoittelumoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="0409f-118">Content placement module properties</span></span>

| <span data-ttu-id="0409f-119">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="0409f-119">Property name</span></span> | <span data-ttu-id="0409f-120">Arvo</span><span class="sxs-lookup"><span data-stu-id="0409f-120">Value</span></span> | <span data-ttu-id="0409f-121">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="0409f-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="0409f-122">Leveys</span><span class="sxs-lookup"><span data-stu-id="0409f-122">Width</span></span>         | <span data-ttu-id="0409f-123">**Sisällytä säilöön** tai **Täytä näyttö**</span><span class="sxs-lookup"><span data-stu-id="0409f-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="0409f-124">Jos arvoksi on määritetty **Sisällytä säilöön**, sisällönsijoittelumoduulin sisällä olevat nimikkeet ovat korkeintaan sisällönsijoittelumoduulin levyisiä.</span><span class="sxs-lookup"><span data-stu-id="0409f-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="0409f-125">Jos arvoksi on määritetty **Täytä näyttö**, sisällönsijoittelumoduulin leveys ei rajoita leveyttä, vaan nimikkeet voivat olla koko näytön levyisiä.</span><span class="sxs-lookup"><span data-stu-id="0409f-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="0409f-126">Sisällönsijoittelunimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="0409f-126">Content placement item module properties</span></span>

| <span data-ttu-id="0409f-127">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="0409f-127">Property name</span></span> | <span data-ttu-id="0409f-128">Arvo</span><span class="sxs-lookup"><span data-stu-id="0409f-128">Value</span></span> | <span data-ttu-id="0409f-129">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="0409f-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="0409f-130">Otsikko</span><span class="sxs-lookup"><span data-stu-id="0409f-130">Heading</span></span>       | <span data-ttu-id="0409f-131">Otsikkoteksti ja -tunnukset (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="0409f-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0409f-132">Jokaisella sisällönsijoittelunnimikemoduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="0409f-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="0409f-133">**Otsikko**-ominaisuus tukee otsikkotunnuksia.</span><span class="sxs-lookup"><span data-stu-id="0409f-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="0409f-134">Oletusarvoisesti käytetään **H2**-otsikkotunnusta. Otsikkotunnuksen voi kuitenkin muuttaa tarvittaessa, jotta se täyttää helppokäyttötoimintojen vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="0409f-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0409f-135">Kappale</span><span class="sxs-lookup"><span data-stu-id="0409f-135">Paragraph</span></span>     | <span data-ttu-id="0409f-136">Kappaleen teksti</span><span class="sxs-lookup"><span data-stu-id="0409f-136">Paragraph text</span></span> | <span data-ttu-id="0409f-137">Sisällönsijoittelunimikemoduulit tukevat kappaleen tekstiä RTF-muodossa.</span><span class="sxs-lookup"><span data-stu-id="0409f-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="0409f-138">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus, kursiivi ja hyperlinkit.</span><span class="sxs-lookup"><span data-stu-id="0409f-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="0409f-139">Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="0409f-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="0409f-140">Kuva</span><span class="sxs-lookup"><span data-stu-id="0409f-140">Image</span></span>         | <span data-ttu-id="0409f-141">Kuvatiedosto</span><span class="sxs-lookup"><span data-stu-id="0409f-141">Image file</span></span> | <span data-ttu-id="0409f-142">Kuvaan voi liittää tekstiä.</span><span class="sxs-lookup"><span data-stu-id="0409f-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="0409f-143">Linkitä</span><span class="sxs-lookup"><span data-stu-id="0409f-143">Link</span></span>          | <span data-ttu-id="0409f-144">Linkin URL-osoite ja linkin teksti</span><span class="sxs-lookup"><span data-stu-id="0409f-144">Link URL and link text</span></span> | <span data-ttu-id="0409f-145">Tekstiin voidaan lisätä linkki, jonka avulla käyttäjät ohjataan tietylle sivulle.</span><span class="sxs-lookup"><span data-stu-id="0409f-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="0409f-146">Ruudun koko</span><span class="sxs-lookup"><span data-stu-id="0409f-146">Tile size</span></span>     | <span data-ttu-id="0409f-147">Numero väliltä **1**–**12**</span><span class="sxs-lookup"><span data-stu-id="0409f-147">A number from **1** through **12**</span></span> | <span data-ttu-id="0409f-148">Tämä ominaisuus määrittää kunkin sisällönsijoittelunimikkeen niiden paikkojen määrän, jotka nimikkeen tulee täyttää sisällönsijoittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="0409f-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="0409f-149">Sisällönsijoittelumoduulin enimmäiskoko on 12 paikkaa.</span><span class="sxs-lookup"><span data-stu-id="0409f-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="0409f-150">Jos sisällönsijoittelumoduulin ensimmäisten *n* -nimikkeen ruutujen kokonaiskoko on yli 12 paikkaa, nimikkeet rivitetään seuraavalle riville.</span><span class="sxs-lookup"><span data-stu-id="0409f-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="0409f-151">Sisällönsijoittelunimikemoduulin sisältävän sisällönsijoittelumoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="0409f-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="0409f-152">Voit lisätä uudelle sivulle sisällönsijoittelumoduulin, joka sisältää sisällönsijoittelunimikemoduulin, ja määrittää vaaditut ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0409f-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0409f-153">Luo malli, jonka nimi on **Sisällönsijoittelumalli**.</span><span class="sxs-lookup"><span data-stu-id="0409f-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="0409f-154">Lisää sisällönsijoittelumoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="0409f-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="0409f-155">Lisää sisällönsijoittelumoduulissa sisällönsijoittelunimikemoduuli.</span><span class="sxs-lookup"><span data-stu-id="0409f-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="0409f-156">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="0409f-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="0409f-157">Käytä juuri luotua sisällönsijoittelumallia, kun haluat luoda sivun nimeltä **Sisällönsijoittelusivu**.</span><span class="sxs-lookup"><span data-stu-id="0409f-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="0409f-158">Lisää sisällönsijoittelumoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="0409f-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="0409f-159">Lisää sisällönsijoittelumoduulissa sisällönsijoittelunimikemoduuli.</span><span class="sxs-lookup"><span data-stu-id="0409f-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="0409f-160">Valitse sisällönsijoittelunimikemoduulin ominaisuusruudussa kuva ja lisää otsikko, kappale sekä linkki. Määritä linkin URL-osoite ja määritä ruudun kooksi **6**.</span><span class="sxs-lookup"><span data-stu-id="0409f-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="0409f-161">Toista vaiheet 7 ja 8 ja lisää toinen sisällönsijoittelunimikemoduuli, jolla on sama ruudun koko.</span><span class="sxs-lookup"><span data-stu-id="0409f-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="0409f-162">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="0409f-162">Save and preview the page.</span></span> <span data-ttu-id="0409f-163">Näkyviin pitäisi tulla kaksi sisällönsijoittelunimikettä vierekkäin.</span><span class="sxs-lookup"><span data-stu-id="0409f-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="0409f-164">Voit muokata kunkin sisällönsijoittelunimikemoduulin **Ruudun koko** -ominaisuutta tai lisätä moduuleja, jotta saat haluamasi asettelun.</span><span class="sxs-lookup"><span data-stu-id="0409f-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="0409f-165">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="0409f-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0409f-166">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0409f-166">Additional resources</span></span>

[<span data-ttu-id="0409f-167">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0409f-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0409f-168">Hälytysmoduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="0409f-169">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="0409f-170">Sisällöntäyteinen lohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="0409f-171">Omaisuusmoduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="0409f-172">Hero-moduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="0409f-173">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="0409f-173">Video player module</span></span>](add-video-player.md)
