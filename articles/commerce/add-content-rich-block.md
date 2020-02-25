---
title: Tekstilohkomoduuli
description: Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025594"
---
# <a name="text-block-module"></a><span data-ttu-id="1932d-103">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="1932d-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1932d-104">Tässä ohjeaiheessa on tietoja tekstilohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="1932d-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1932d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1932d-105">Overview</span></span>

<span data-ttu-id="1932d-106">Tekstilohkomoduuli on moduuli, jolla lisätään tekstisisältöä.</span><span class="sxs-lookup"><span data-stu-id="1932d-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="1932d-107">Tämä sisältö voi olla tiedottavaa sisältöä tai kampanjasisältöä.</span><span class="sxs-lookup"><span data-stu-id="1932d-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="1932d-108">Tekstilohkomoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="1932d-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="1932d-109">Ne ovat itsenäisiä moduuleja, jotka eivät ole riippuvaisia sivun kontekstista tai muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="1932d-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="1932d-110">Esimerkkejä sähköisen kaupankäynnin tekstilohkomoduuleista</span><span class="sxs-lookup"><span data-stu-id="1932d-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="1932d-111">Tekstilohkomoduuleja voi käyttää seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1932d-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="1932d-112">Tuotteiden ominaisuuksien esittely tuotetietosivulla</span><span class="sxs-lookup"><span data-stu-id="1932d-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="1932d-113">Tiedoksi millä tahansa sivulla.</span><span class="sxs-lookup"><span data-stu-id="1932d-113">For informational purposes on any page.</span></span> <span data-ttu-id="1932d-114">Ne voivat esimerkiksi selittää kanta-asiakasohjelmien etuja, kuvailla toimitus- ja palautuskäytäntöjä, vastata usein kysyttyihin kysymyksiin ja kertoa yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="1932d-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="1932d-115">Voit lisätä mukautettuja sanomia tuotetietosivulle.</span><span class="sxs-lookup"><span data-stu-id="1932d-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="1932d-116">(esimerkiksi Ilmainen tilaus uli 50 $ arvoisille tilauksille).</span><span class="sxs-lookup"><span data-stu-id="1932d-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="1932d-117">Tuotetieto-, ostoskori-, kassa- ja muiden sivujen vastuuvapauslausekkeet ja yhteystiedot (esimerkiksi Myymälän käytännöt koskevat toimituksia ja palautuksia).</span><span class="sxs-lookup"><span data-stu-id="1932d-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="1932d-118">Tekstilohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1932d-118">Text block module properties</span></span>

| <span data-ttu-id="1932d-119">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="1932d-119">Property name</span></span>     | <span data-ttu-id="1932d-120">Value</span><span class="sxs-lookup"><span data-stu-id="1932d-120">Value</span></span>                                            | <span data-ttu-id="1932d-121">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1932d-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="1932d-122">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="1932d-122">Rich text</span></span>         | <span data-ttu-id="1932d-123">Muotoiltu teksti</span><span class="sxs-lookup"><span data-stu-id="1932d-123">Rich text</span></span>                                        | <span data-ttu-id="1932d-124">Kappaleen teksti.</span><span class="sxs-lookup"><span data-stu-id="1932d-124">Paragraph text.</span></span> <span data-ttu-id="1932d-125">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus ja kursiivi.</span><span class="sxs-lookup"><span data-stu-id="1932d-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="1932d-126">Mukautetun luokan nimi</span><span class="sxs-lookup"><span data-stu-id="1932d-126">Custom class name</span></span> | <span data-ttu-id="1932d-127">CSS-tyylisivujen luokan nimi</span><span class="sxs-lookup"><span data-stu-id="1932d-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="1932d-128">Mukautetun CSS-luokan nimi, jonka kehittäjä antaa moduulin muotoiluun.</span><span class="sxs-lookup"><span data-stu-id="1932d-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="1932d-129">Luokan nimi on määritettävä teemapaketissa.</span><span class="sxs-lookup"><span data-stu-id="1932d-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="1932d-130">Fontin koko</span><span class="sxs-lookup"><span data-stu-id="1932d-130">Font size</span></span>         | <span data-ttu-id="1932d-131">**Pieni**, **Keskisuuri**, **Suuri** tai **Erittäin suuri**</span><span class="sxs-lookup"><span data-stu-id="1932d-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="1932d-132">Sisällön fontin koko.</span><span class="sxs-lookup"><span data-stu-id="1932d-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="1932d-133">Tekstilohkomoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="1932d-133">Add a text block module to a page</span></span>

<span data-ttu-id="1932d-134">Voit lisätä tekstilohkomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1932d-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1932d-135">Luo sivumalli, jonka nimi on **Sisältömalli**.</span><span class="sxs-lookup"><span data-stu-id="1932d-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="1932d-136">Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="1932d-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="1932d-137">Kun mallin muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="1932d-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="1932d-138">Käytä juuri luotua sisältömallia, kun haluat luoda sivun nimeltä **Sisältösivu**.</span><span class="sxs-lookup"><span data-stu-id="1932d-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="1932d-139">Lisää säilömoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="1932d-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="1932d-140">Määritä säilömoduulin ominaisuusruudun **Leveys**-ominaisuudeksi **Täytä säilö**.</span><span class="sxs-lookup"><span data-stu-id="1932d-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1932d-141">Lisää tekstilohkomoduuli säilömoduuliin.</span><span class="sxs-lookup"><span data-stu-id="1932d-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="1932d-142">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1932d-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="1932d-143">Kun sivun muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="1932d-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1932d-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1932d-144">Additional resources</span></span>

[<span data-ttu-id="1932d-145">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1932d-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1932d-146">Kampanjabannerimoduuli</span><span class="sxs-lookup"><span data-stu-id="1932d-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="1932d-147">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="1932d-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1932d-148">Sisältölohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="1932d-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="1932d-149">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="1932d-149">Video player module</span></span>](add-video-player.md)

