---
title: Välilehtimoduuli
description: Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.openlocfilehash: 60af9b74f7e647e83229e352a03c09d63d0c7902
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417366"
---
# <a name="tab-module"></a><span data-ttu-id="8952b-103">Välilehtimoduuli</span><span class="sxs-lookup"><span data-stu-id="8952b-103">Tab module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8952b-104">Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="8952b-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8952b-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="8952b-105">Overview</span></span>

<span data-ttu-id="8952b-106">Välilehtimoduulit ovat kontin kaltaisia moduuleja, joita käytetään välilehtien sivujen tietojen järjestämiseen.</span><span class="sxs-lookup"><span data-stu-id="8952b-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="8952b-107">Niitä voidaan käyttää millä tahansa sivulla, jolla tiedot on esitettävä välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="8952b-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="8952b-108">Jokaisessa välilehtimoduulissa voidaan lisätä yksi tai useampia välilehtimoduuleja.</span><span class="sxs-lookup"><span data-stu-id="8952b-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="8952b-109">Jokainen välilehtinimikemoduuli edustaa yhtä välilehteä. Jokaiseen välilehtinimikemoduuliin voidaan lisätä yksi tai useita moduuleja.</span><span class="sxs-lookup"><span data-stu-id="8952b-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="8952b-110">Välilehtinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="8952b-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="8952b-111">Seuraavassa kuvassa on esimerkki välilehtimoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="8952b-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="8952b-112">Tässä esimerkissä valittu **Toimitus**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="8952b-112">In this example, the **Shipping** tab selected.</span></span>

![Esimerkki välilehtimoduulista](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="8952b-114">Välilehtimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8952b-114">Tab module properties</span></span>

| <span data-ttu-id="8952b-115">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="8952b-115">Property name</span></span> | <span data-ttu-id="8952b-116">Arvot</span><span class="sxs-lookup"><span data-stu-id="8952b-116">Values</span></span> | <span data-ttu-id="8952b-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8952b-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8952b-118">Otsikko</span><span class="sxs-lookup"><span data-stu-id="8952b-118">Heading</span></span> | <span data-ttu-id="8952b-119">Teksti</span><span class="sxs-lookup"><span data-stu-id="8952b-119">Text</span></span> | <span data-ttu-id="8952b-120">Tämä ominaisuus määrittää valinnaisen tekstiotsikon välilehtimoduulille.</span><span class="sxs-lookup"><span data-stu-id="8952b-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="8952b-121">Aktiivinen välilehden indeksi</span><span class="sxs-lookup"><span data-stu-id="8952b-121">Active Tab Index</span></span> | <span data-ttu-id="8952b-122">Numero</span><span class="sxs-lookup"><span data-stu-id="8952b-122">Number</span></span> | <span data-ttu-id="8952b-123">Tämä ominaisuus määrittää välilehden, joka on oletusarvoisesti aktiivinen, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="8952b-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="8952b-124">Jos arvoa ei ole annettu, ensimmäinen välilehti on oletusarvon mukaan aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="8952b-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="8952b-125">Välilehtinimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8952b-125">Tab item module properties</span></span>

| <span data-ttu-id="8952b-126">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="8952b-126">Property name</span></span> | <span data-ttu-id="8952b-127">Arvot</span><span class="sxs-lookup"><span data-stu-id="8952b-127">Values</span></span> | <span data-ttu-id="8952b-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8952b-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8952b-129">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="8952b-129">Title</span></span> | <span data-ttu-id="8952b-130">Teksti</span><span class="sxs-lookup"><span data-stu-id="8952b-130">Text</span></span> | <span data-ttu-id="8952b-131">Tämä ominaisuus määrittää otsikkotekstin välilehtinimikemoduulille.</span><span class="sxs-lookup"><span data-stu-id="8952b-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="8952b-132">Välilehtimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="8952b-132">Add a tab module to a page</span></span>

<span data-ttu-id="8952b-133">Voit lisätä välilehtimoduulin sivulle ja määrittää ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8952b-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="8952b-134">Käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="8952b-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="8952b-135">Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="8952b-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8952b-136">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8952b-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8952b-137">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="8952b-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8952b-138">Valitse **Lisää moduuli** -valintaikkunassa **Välilehti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8952b-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8952b-139">Valitse välilehtimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="8952b-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="8952b-140">Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti** -kohtaan otsikkoteksti (esimerkiksi **Käytännöt**).</span><span class="sxs-lookup"><span data-stu-id="8952b-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="8952b-141">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8952b-141">Then select **OK**.</span></span>
1. <span data-ttu-id="8952b-142">Valitse kolme pistettä (**...**) **Välilehti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="8952b-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8952b-143">Valitse **Lisää moduuli** -valintaikkunassa **Välilehtinimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8952b-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8952b-144">Kirjoita välilehtinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Toimitus**).</span><span class="sxs-lookup"><span data-stu-id="8952b-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="8952b-145">Valitse kolme pistettä (**...**) **Välilehtinimike**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="8952b-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8952b-146">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="8952b-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8952b-147">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään tekstikappale.</span><span class="sxs-lookup"><span data-stu-id="8952b-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="8952b-148">Lisää **Välilehti**-paikkaan muutamia otsikoita sisältävän välilehtinimikkeen moduuleja.</span><span class="sxs-lookup"><span data-stu-id="8952b-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="8952b-149">Lisää kuhunkin välilehtinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.</span><span class="sxs-lookup"><span data-stu-id="8952b-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="8952b-150">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="8952b-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="8952b-151">Sivulla näkyy välilehtimoduuli, joka sisältää välilehtinimikemoduulit, joissa on lisäämäsi sisältö.</span><span class="sxs-lookup"><span data-stu-id="8952b-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="8952b-152">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="8952b-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8952b-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8952b-153">Additional resources</span></span>

[<span data-ttu-id="8952b-154">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8952b-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8952b-155">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="8952b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8952b-156">Haitarimoduuli</span><span class="sxs-lookup"><span data-stu-id="8952b-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="8952b-157">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="8952b-157">Text block module</span></span>](add-content-rich-block.md)
