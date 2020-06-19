---
title: Tekstilohkomoduuli
description: Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 93ad09a05d188a30b099b9a44c35e15839be80a7
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411132"
---
# <a name="text-block-module"></a><span data-ttu-id="f4d18-103">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="f4d18-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f4d18-104">Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="f4d18-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f4d18-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f4d18-105">Overview</span></span>

<span data-ttu-id="f4d18-106">Tekstilohkomoduuli on moduuli, jolla lisätään tekstisisältöä.</span><span class="sxs-lookup"><span data-stu-id="f4d18-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="f4d18-107">Tämä sisältö voi olla tiedottavaa sisältöä tai kampanjasisältöä.</span><span class="sxs-lookup"><span data-stu-id="f4d18-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="f4d18-108">Tekstilohkomoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="f4d18-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="f4d18-109">Ne ovat itsenäisiä moduuleja, jotka eivät ole riippuvaisia sivun kontekstista tai muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="f4d18-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="f4d18-110">Esimerkkejä sähköisen kaupankäynnin tekstilohkomoduuleista</span><span class="sxs-lookup"><span data-stu-id="f4d18-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="f4d18-111">Tekstilohkomoduuleja voi käyttää seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f4d18-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="f4d18-112">Tuotteiden ominaisuuksien esittely tuotetietosivulla</span><span class="sxs-lookup"><span data-stu-id="f4d18-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="f4d18-113">Tiedoksi millä tahansa sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4d18-113">For informational purposes on any page.</span></span> <span data-ttu-id="f4d18-114">Ne voivat esimerkiksi selittää kanta-asiakasohjelmien etuja, kuvailla toimitus- ja palautuskäytäntöjä, vastata usein kysyttyihin kysymyksiin ja kertoa yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="f4d18-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="f4d18-115">Voit lisätä mukautettuja sanomia tuotetietosivulle.</span><span class="sxs-lookup"><span data-stu-id="f4d18-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="f4d18-116">(esimerkiksi Ilmainen tilaus uli 50 $ arvoisille tilauksille).</span><span class="sxs-lookup"><span data-stu-id="f4d18-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="f4d18-117">Tuotetieto-, ostoskori-, kassa- ja muiden sivujen vastuuvapauslausekkeet ja yhteystiedot (esimerkiksi Myymälän käytännöt koskevat toimituksia ja palautuksia).</span><span class="sxs-lookup"><span data-stu-id="f4d18-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="f4d18-118">Seuraavassa kuvassa näkyy esimerkki tekstilohkomoduulista, jota käytetään kotisivulla.</span><span class="sxs-lookup"><span data-stu-id="f4d18-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Esimerkki tekstilohkomoduulista](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="f4d18-120">Tekstilohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f4d18-120">Text block module properties</span></span>

| <span data-ttu-id="f4d18-121">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="f4d18-121">Property name</span></span>     | <span data-ttu-id="f4d18-122">Arvo</span><span class="sxs-lookup"><span data-stu-id="f4d18-122">Value</span></span>                                            | <span data-ttu-id="f4d18-123">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f4d18-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="f4d18-124">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="f4d18-124">Rich text</span></span>         | <span data-ttu-id="f4d18-125">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="f4d18-125">Rich text</span></span>                                        | <span data-ttu-id="f4d18-126">Kappaleen teksti.</span><span class="sxs-lookup"><span data-stu-id="f4d18-126">Paragraph text.</span></span> <span data-ttu-id="f4d18-127">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus ja kursiivi.</span><span class="sxs-lookup"><span data-stu-id="f4d18-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="f4d18-128">Mukautetun luokan nimi</span><span class="sxs-lookup"><span data-stu-id="f4d18-128">Custom class name</span></span> | <span data-ttu-id="f4d18-129">CSS-tyylisivujen luokan nimi</span><span class="sxs-lookup"><span data-stu-id="f4d18-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="f4d18-130">Mukautetun CSS-luokan nimi, jonka kehittäjä antaa moduulin muotoiluun.</span><span class="sxs-lookup"><span data-stu-id="f4d18-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="f4d18-131">Luokan nimi on määritettävä teemapaketissa.</span><span class="sxs-lookup"><span data-stu-id="f4d18-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="f4d18-132">Fontin koko</span><span class="sxs-lookup"><span data-stu-id="f4d18-132">Font size</span></span>         | <span data-ttu-id="f4d18-133">**Pieni**, **Keskisuuri**, **Suuri** tai **Erittäin suuri**</span><span class="sxs-lookup"><span data-stu-id="f4d18-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="f4d18-134">Sisällön fontin koko.</span><span class="sxs-lookup"><span data-stu-id="f4d18-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="f4d18-135">Tekstilohkomoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="f4d18-135">Add a text block module to a page</span></span>

<span data-ttu-id="f4d18-136">Voit lisätä tekstilohkomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f4d18-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f4d18-137">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="f4d18-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f4d18-138">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Sisältömalli**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="f4d18-139">Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4d18-140">Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4d18-141">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f4d18-142">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="f4d18-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f4d18-143">Valitse **Valitse malli** -valintaikkunassa **Sisältömalli**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="f4d18-144">Kirjoita **Sivun nimi** -kohtaan **Sisältösivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f4d18-145">Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4d18-146">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4d18-147">Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f4d18-148">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4d18-149">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="f4d18-150">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f4d18-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="f4d18-151">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="f4d18-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f4d18-152">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="f4d18-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4d18-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f4d18-153">Additional resources</span></span>

[<span data-ttu-id="f4d18-154">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f4d18-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f4d18-155">Promopalkkimoduuli</span><span class="sxs-lookup"><span data-stu-id="f4d18-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f4d18-156">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="f4d18-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="f4d18-157">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="f4d18-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f4d18-158">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="f4d18-158">Video player module</span></span>](add-video-player.md)

