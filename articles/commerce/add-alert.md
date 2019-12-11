---
title: Hälytysmoduuli
description: Tässä ohjeaiheessa on tietoja hälytysmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785349"
---
# <a name="alert-module"></a><span data-ttu-id="7334f-103">Hälytysmoduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7334f-104">Tässä ohjeaiheessa on tietoja hälytysmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="7334f-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7334f-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7334f-105">Overview</span></span>

<span data-ttu-id="7334f-106">Hälytysmoduulia käytetään sivun sisäisten tietosanomien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="7334f-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="7334f-107">Hälytysmoduulit tukevat tekstisanomaa ja linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7334f-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="7334f-108">Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla.</span><span class="sxs-lookup"><span data-stu-id="7334f-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="7334f-109">Hälytysmoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.</span><span class="sxs-lookup"><span data-stu-id="7334f-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="7334f-110">Esimerkkejä sähköisen kaupankäynnin hälytysmoduuleista</span><span class="sxs-lookup"><span data-stu-id="7334f-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="7334f-111">Hälytysmoduuleja voidaan käyttää sivuston ylätunnisteessa osoittamaan koko sivustoa koskevia kampanjoita tai sanomia.</span><span class="sxs-lookup"><span data-stu-id="7334f-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="7334f-112">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="7334f-112">Here are some examples:</span></span>

<span data-ttu-id="7334f-113">Vuosittainen alennusmyynti loppuu 10 päivän kuluttua</span><span class="sxs-lookup"><span data-stu-id="7334f-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="7334f-114">Alennusmyynnit ennen koulujen alkamista.</span><span class="sxs-lookup"><span data-stu-id="7334f-114">"Save big with back to school sale.</span></span> <span data-ttu-id="7334f-115">Osta nyt.</span><span class="sxs-lookup"><span data-stu-id="7334f-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="7334f-116">Hälytysmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="7334f-116">Alert module properties</span></span>

| <span data-ttu-id="7334f-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="7334f-117">Property name</span></span>  | <span data-ttu-id="7334f-118">Arvo</span><span class="sxs-lookup"><span data-stu-id="7334f-118">Value</span></span>                              | <span data-ttu-id="7334f-119">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7334f-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="7334f-120">Teksti</span><span class="sxs-lookup"><span data-stu-id="7334f-120">Text</span></span>           | <span data-ttu-id="7334f-121">Teksti</span><span class="sxs-lookup"><span data-stu-id="7334f-121">Text</span></span>                               | <span data-ttu-id="7334f-122">Hälytysmoduulissa näkyvä tekstisanoma.</span><span class="sxs-lookup"><span data-stu-id="7334f-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="7334f-123">Tekstin tasaus</span><span class="sxs-lookup"><span data-stu-id="7334f-123">Text alignment</span></span> | <span data-ttu-id="7334f-124">**Oikealla**, **vasemmalla** tai **keskellä**</span><span class="sxs-lookup"><span data-stu-id="7334f-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="7334f-125">Arvo, joka määrittää, miten teksti tasataan hälytysmoduulissa.</span><span class="sxs-lookup"><span data-stu-id="7334f-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="7334f-126">Hylkää hälytys</span><span class="sxs-lookup"><span data-stu-id="7334f-126">Dismiss alert</span></span>  | <span data-ttu-id="7334f-127">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="7334f-127">**True** or **False**</span></span>              | <span data-ttu-id="7334f-128">Jos arvoksi on määritetty **Tosi**, asiakas voi hylätä hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="7334f-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="7334f-129">Linkitä</span><span class="sxs-lookup"><span data-stu-id="7334f-129">Link</span></span>           | <span data-ttu-id="7334f-130">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="7334f-130">URL</span></span>                                | <span data-ttu-id="7334f-131">Vapaavalintaisen linkin URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="7334f-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="7334f-132">Hälytysmoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="7334f-132">Add an alert module to a page</span></span> 

<span data-ttu-id="7334f-133">Voit lisätä hälytysmoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7334f-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7334f-134">Luo sivumalli, jonka nimi on **Hälytysmalli**.</span><span class="sxs-lookup"><span data-stu-id="7334f-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="7334f-135">Lisää hälytysmoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="7334f-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="7334f-136">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="7334f-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="7334f-137">Käytä juuri luotua hälytysmallia, kun haluat luoda sivun nimeltä **Hälytyssivu**.</span><span class="sxs-lookup"><span data-stu-id="7334f-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="7334f-138">Lisää hälytysmoduuli uuden sivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="7334f-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="7334f-139">Syötä hälytysteksti hälytysmoduulin asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="7334f-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="7334f-140">Voit muokata muita ominaisuuksia, jos haluat mukauttaa hälytysmoduulia lisää.</span><span class="sxs-lookup"><span data-stu-id="7334f-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="7334f-141">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="7334f-141">Save and preview the page.</span></span> <span data-ttu-id="7334f-142">Sivun yläosassa pitäisi nyt olla hälytys, joka sisältää lisäämäsi tekstin.</span><span class="sxs-lookup"><span data-stu-id="7334f-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="7334f-143">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="7334f-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="7334f-144">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7334f-144">Additional resources</span></span>

[<span data-ttu-id="7334f-145">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7334f-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7334f-146">Karusellimoduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="7334f-147">Sisällöntäyteinen lohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="7334f-148">Sisällönsijoittelumoduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="7334f-149">Omaisuusmoduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="7334f-150">Hero-moduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="7334f-151">Videotoistinmoduuli</span><span class="sxs-lookup"><span data-stu-id="7334f-151">Video player module</span></span>](add-video-player.md)
