---
title: Sisällöntäyteinen lohkomoduuli
description: Tässä ohjeaiheessa on tietoja sisällöntäyteisistä lohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785418"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="5e7a8-103">Sisällöntäyteinen lohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5e7a8-104">Tässä ohjeaiheessa on tietoja sisällöntäyteisistä lohkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5e7a8-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5e7a8-105">Overview</span></span>

<span data-ttu-id="5e7a8-106">Sisällöntäyteinen lohkomoduuli on erityinen säilö, jonka sisään voi asettaa yhden tai useita sisällöntäyteisiä lohkonimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="5e7a8-107">Sisällöntäyteisiä lohkomoduuleja käytetään sivun tekstisisällössä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="5e7a8-108">Tämä sisältö voi olla joko tiedottavaa sisältöä tai kampanjasisältöä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="5e7a8-109">Sisällöntäyteisiä lohkomoduuleja ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Ne voidaan sijoittaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="5e7a8-110">Ne ovat itsenäisiä moduuleja, jotka eivät ole riippuvaisia sivun kontekstista tai muista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="5e7a8-111">Esimerkkejä sähköisen kaupankäynnin sisällöntäyteisistä lohkomoduuleista</span><span class="sxs-lookup"><span data-stu-id="5e7a8-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="5e7a8-112">Sisällöntäyteisiä lohkomoduuleja voi käyttää seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5e7a8-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="5e7a8-113">Tuotteiden ominaisuuksien esittely tuotetietosivulla</span><span class="sxs-lookup"><span data-stu-id="5e7a8-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="5e7a8-114">Tiedoksi millä tahansa sivulla.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-114">For informational purposes on any page.</span></span> <span data-ttu-id="5e7a8-115">Ne voivat esimerkiksi selittää kanta-asiakasohjelmien etuja, kuvailla toimitus- ja palautuskäytäntöjä, vastata usein kysyttyihin kysymyksiin ja kertoa yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="5e7a8-116">Voit lisätä mukautettuja sanomia tuotetietosivulle.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="5e7a8-117">(esimerkiksi Ilmainen tilaus uli 50 $ arvoisille tilauksille).</span><span class="sxs-lookup"><span data-stu-id="5e7a8-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="5e7a8-118">Tuotetieto-, ostoskori-, kassa- ja muiden sivujen vastuuvapauslausekkeet ja yhteystiedot (esimerkiksi Myymälän käytännöt koskevat toimituksia ja palautuksia).</span><span class="sxs-lookup"><span data-stu-id="5e7a8-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="5e7a8-119">Sisällöntäyteisen lohkomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5e7a8-119">Content rich block module properties</span></span>

| <span data-ttu-id="5e7a8-120">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5e7a8-120">Property name</span></span>     | <span data-ttu-id="5e7a8-121">Arvo</span><span class="sxs-lookup"><span data-stu-id="5e7a8-121">Value</span></span>                                 | <span data-ttu-id="5e7a8-122">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="5e7a8-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="5e7a8-123">Sarakkeiden määrä</span><span class="sxs-lookup"><span data-stu-id="5e7a8-123">Number of columns</span></span> | <span data-ttu-id="5e7a8-124">Numero väliltä **1**–**4**</span><span class="sxs-lookup"><span data-stu-id="5e7a8-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="5e7a8-125">Sisällöntäyteisen lohkon sarakkeiden määrä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="5e7a8-126">Sarakkeita voi olla enintään neljä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="5e7a8-127">Leveys</span><span class="sxs-lookup"><span data-stu-id="5e7a8-127">Width</span></span>             | <span data-ttu-id="5e7a8-128">**Täytä säilö** tai **Täytä näyttö**</span><span class="sxs-lookup"><span data-stu-id="5e7a8-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="5e7a8-129">Jos arvoksi on määritetty **Täytä säilö** säilön sisällä olevat nimikkeet ovat korkeintaan säilön levyisiä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="5e7a8-130">Jos arvoksi on määritetty **Täytä näyttö**, säilön leveys ei rajoita leveyttä, vaan nimikkeet voivat olla koko näytön levyisiä.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="5e7a8-131">Voit muuttaa arvoa halutun asettelun saavuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="5e7a8-132">Sisällöntäyteisen lohkonimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5e7a8-132">Content rich block item module properties</span></span>

| <span data-ttu-id="5e7a8-133">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5e7a8-133">Property name</span></span> | <span data-ttu-id="5e7a8-134">Arvo</span><span class="sxs-lookup"><span data-stu-id="5e7a8-134">Value</span></span>          | <span data-ttu-id="5e7a8-135">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5e7a8-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="5e7a8-136">Kappale</span><span class="sxs-lookup"><span data-stu-id="5e7a8-136">Paragraph</span></span>     | <span data-ttu-id="5e7a8-137">Kappaleen teksti</span><span class="sxs-lookup"><span data-stu-id="5e7a8-137">Paragraph text</span></span> | <span data-ttu-id="5e7a8-138">Kunkin sisällöntäyteisen lohkonimikkeen teksti.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="5e7a8-139">Joitakin RTF-ominaisuuksia tuetaan. Näitä ominaisuuksia ovat esimerkiksi lihavointi, alleviivaus ja kursiivi.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="5e7a8-140">Sisällöntäyteisen lohkomoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="5e7a8-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="5e7a8-141">Voit lisätä sisällöntäyteisen lohkomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5e7a8-142">Luo sivumalli, jonka nimi on **Sisältömalli**.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="5e7a8-143">Lisää sisällöntäyteinen lohkomoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="5e7a8-144">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="5e7a8-145">Käytä juuri luotua sisältömallia, kun haluat luoda sivun nimeltä **Sisältösivu**.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="5e7a8-146">Lisää sisällöntäyteinen lohkomoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="5e7a8-147">Määritä sisällöntäyteisen lohkomoduulin ominaisuuksissa sarakkeiden määräksi **2**.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="5e7a8-148">Valitse sisällöntäyteisessä lohkomoduulissa **Lisää moduuli** ja lisää sisällöntäyteinen lohkonimike (esimerkiksi **nimike1**).</span><span class="sxs-lookup"><span data-stu-id="5e7a8-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="5e7a8-149">Lisää uuteen sisällöntäyteiseen lohkonimikkeeseen kappaleen teksti.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="5e7a8-150">Valitse sisällöntäyteisessä lohkomoduulissa **Lisää moduuli** ja lisää sisällöntäyteinen lohkonimike (esimerkiksi **nimike2**).</span><span class="sxs-lookup"><span data-stu-id="5e7a8-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="5e7a8-151">Lisää uuteen sisällöntäyteiseen lohkonimikkeeseen kappaleen teksti.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="5e7a8-152">Tallenna sivu ja esikatsele muutokset.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="5e7a8-153">Kaksisarakkeisessa näkymässä on näkyvissä kaksi sisällöntäyteistä lohkoa.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="5e7a8-154">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="5e7a8-155">Jos lisäät kolmannen sisällöntäyteisen lohkonimikkeen, se pinotaan kahden aiemmin lisätyn nimikkeen alle.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="5e7a8-156">Jos muutat sarakkeiden ja nimikkeiden määrää säilössä, voit muodostaa erilaisia asetteluita tekstisisällölle.</span><span class="sxs-lookup"><span data-stu-id="5e7a8-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e7a8-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5e7a8-157">Additional resources</span></span>

[<span data-ttu-id="5e7a8-158">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5e7a8-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5e7a8-159">Hälytysmoduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="5e7a8-160">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="5e7a8-161">Sisällönsijoittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="5e7a8-162">Omaisuusmoduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="5e7a8-163">Hero-moduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="5e7a8-164">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="5e7a8-164">Video player module</span></span>](add-video-player.md)

