---
title: iFrame-moduuli
description: Tässä ohjeaiheessa käsitellään iFrame-moduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 58446289c9a53af30d4d6d331a1a609ae0d2a0ad
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818195"
---
# <a name="iframe-module"></a><span data-ttu-id="f7f45-103">iFrame-moduuli</span><span class="sxs-lookup"><span data-stu-id="f7f45-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7f45-104">Tässä ohjeaiheessa käsitellään iFrame-moduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="f7f45-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f7f45-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="f7f45-105">Overview</span></span>

<span data-ttu-id="f7f45-106">iFrame-moduuli sisältää iFrame-kehyksen (sisäinen kehys), joka isännöi sivuston ulkoista sisältöä.</span><span class="sxs-lookup"><span data-stu-id="f7f45-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="f7f45-107">Sen avulla voidaan esimerkiksi isännöidä YouTube-videota tai PDF-tiedoston katseluohjelmaa millä tahansa sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="f7f45-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="f7f45-108">iFrame-moduuli edellyttää kohde-URL-osoitetta.</span><span class="sxs-lookup"><span data-stu-id="f7f45-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="f7f45-109">Sen jälkeen se isännöi kohdesivun sisältöä HTML:n **iFrame**-elementin sisällä.</span><span class="sxs-lookup"><span data-stu-id="f7f45-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="f7f45-110">Ulkoisten URL-osoitteiden on oltava sallittujen luettelossa sivuston sisällön suojauskäytännön direktiivien mukaan.</span><span class="sxs-lookup"><span data-stu-id="f7f45-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="f7f45-111">iFrame-sisällössä URL-osoitteet tulisi sallia käyttämällä **frame-ancestor**-direktiiviä.</span><span class="sxs-lookup"><span data-stu-id="f7f45-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="f7f45-112">Lisätietoja on kohdassa [Sisällön suojauskäytännön hallinta](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="f7f45-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f7f45-113">iframe-moduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="f7f45-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="f7f45-114">Seuraavassa kuvassa näkyy esimerkkejä iFrame-moduuleista, jotka esittelevät sivuston sivujen ulkoisia videoita.</span><span class="sxs-lookup"><span data-stu-id="f7f45-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Esimerkki iFrame-moduuleista, jotka esittelevät ulkoisia videoita](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="f7f45-116">iFrame-moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f7f45-116">Iframe module properties</span></span>

| <span data-ttu-id="f7f45-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="f7f45-117">Property name</span></span>             | <span data-ttu-id="f7f45-118">Arvo</span><span class="sxs-lookup"><span data-stu-id="f7f45-118">Value</span></span>                 | <span data-ttu-id="f7f45-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f7f45-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f7f45-120">Otsikko</span><span class="sxs-lookup"><span data-stu-id="f7f45-120">Heading</span></span> | <span data-ttu-id="f7f45-121">Teksti</span><span class="sxs-lookup"><span data-stu-id="f7f45-121">Text</span></span> | <span data-ttu-id="f7f45-122">Moduulin otsikko.</span><span class="sxs-lookup"><span data-stu-id="f7f45-122">The heading for the module.</span></span> |
| <span data-ttu-id="f7f45-123">Kohde-URL-osoite</span><span class="sxs-lookup"><span data-stu-id="f7f45-123">Target URL</span></span> | <span data-ttu-id="f7f45-124">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="f7f45-124">URL</span></span> | <span data-ttu-id="f7f45-125">Moduulissa isännöity URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="f7f45-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="f7f45-126">Korkeus</span><span class="sxs-lookup"><span data-stu-id="f7f45-126">Height</span></span> | <span data-ttu-id="f7f45-127">Numero tai prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="f7f45-127">Number or percentage</span></span> | <span data-ttu-id="f7f45-128">Moduulin korkeus kuvapisteinä tai prosentteina.</span><span class="sxs-lookup"><span data-stu-id="f7f45-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="f7f45-129">Esimerkiksi arvoa **100** käsitellään kuvapisteinä ja arvoa **100 %** prosenttina.</span><span class="sxs-lookup"><span data-stu-id="f7f45-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="f7f45-130">Aria-otsikko</span><span class="sxs-lookup"><span data-stu-id="f7f45-130">Aria label</span></span> | <span data-ttu-id="f7f45-131">Teksti</span><span class="sxs-lookup"><span data-stu-id="f7f45-131">Text</span></span> | <span data-ttu-id="f7f45-132">ARIA-otsikko (Accessible Rich Internet Applications) voidaan määrittää helppokäyttöisyyttä varten.</span><span class="sxs-lookup"><span data-stu-id="f7f45-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="f7f45-133">iFrame-moduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="f7f45-133">Add an iframe module to a page</span></span>

<span data-ttu-id="f7f45-134">Voit lisätä sivulle ulkoisen videon näyttävän iFrame-moduulin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f7f45-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="f7f45-135">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="f7f45-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f7f45-136">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Markkinointimalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f45-137">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f7f45-138">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="f7f45-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f7f45-139">Valitse **Valitse malli** -valintaikkunassa **Markkinointimalli**-malli.</span><span class="sxs-lookup"><span data-stu-id="f7f45-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="f7f45-140">Kirjoita **Sivun nimi** -kohtaan **Markkinointisivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f45-141">Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f7f45-142">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f45-143">Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="f7f45-144">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f7f45-145">Valitse **Lisää moduuli** -valintaikkunassa **iFrame**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f7f45-146">Määritä moduulin ominaisuuksien ruudussa **kohde-URL:n** arvo videon ulkoiselle URL-osoitteelle.</span><span class="sxs-lookup"><span data-stu-id="f7f45-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="f7f45-147">Määritä halutessasi muut ominaisuudet, kuten **otsikko** ja **korkeus**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="f7f45-148">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f7f45-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f7f45-149">Siirry sivuston markkinointisivulle.</span><span class="sxs-lookup"><span data-stu-id="f7f45-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="f7f45-150">Videon tulisi olla hahmonnettu iFrame-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="f7f45-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="f7f45-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f7f45-151">Additional resources</span></span>

[<span data-ttu-id="f7f45-152">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f7f45-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f7f45-153">Sisällön suojauskäytännön (CSP) hallinta</span><span class="sxs-lookup"><span data-stu-id="f7f45-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
