---
title: Välilehtimoduuli
description: Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209224"
---
# <a name="tab-module"></a><span data-ttu-id="e845d-103">Välilehtimoduuli</span><span class="sxs-lookup"><span data-stu-id="e845d-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e845d-104">Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="e845d-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e845d-105">Välilehtimoduulit ovat kontin kaltaisia moduuleja, joita käytetään välilehtien sivujen tietojen järjestämiseen.</span><span class="sxs-lookup"><span data-stu-id="e845d-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="e845d-106">Niitä voidaan käyttää millä tahansa sivulla, jolla tiedot on esitettävä välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="e845d-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="e845d-107">Jokaisessa välilehtimoduulissa voidaan lisätä yksi tai useampia välilehtimoduuleja.</span><span class="sxs-lookup"><span data-stu-id="e845d-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="e845d-108">Jokainen välilehtinimikemoduuli edustaa yhtä välilehteä. Jokaiseen välilehtinimikemoduuliin voidaan lisätä yksi tai useita moduuleja.</span><span class="sxs-lookup"><span data-stu-id="e845d-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="e845d-109">Välilehtinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="e845d-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="e845d-110">Seuraavassa kuvassa on esimerkki välilehtimoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="e845d-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="e845d-111">Tässä esimerkissä valittu **Toimitus**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="e845d-111">In this example, the **Shipping** tab selected.</span></span>

![Esimerkki välilehtimoduulista](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="e845d-113">Välilehtimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e845d-113">Tab module properties</span></span>

| <span data-ttu-id="e845d-114">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="e845d-114">Property name</span></span> | <span data-ttu-id="e845d-115">Arvot</span><span class="sxs-lookup"><span data-stu-id="e845d-115">Values</span></span> | <span data-ttu-id="e845d-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e845d-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e845d-117">Otsikko</span><span class="sxs-lookup"><span data-stu-id="e845d-117">Heading</span></span> | <span data-ttu-id="e845d-118">Teksti</span><span class="sxs-lookup"><span data-stu-id="e845d-118">Text</span></span> | <span data-ttu-id="e845d-119">Tämä ominaisuus määrittää valinnaisen tekstiotsikon välilehtimoduulille.</span><span class="sxs-lookup"><span data-stu-id="e845d-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="e845d-120">Aktiivinen välilehden indeksi</span><span class="sxs-lookup"><span data-stu-id="e845d-120">Active Tab Index</span></span> | <span data-ttu-id="e845d-121">Numero</span><span class="sxs-lookup"><span data-stu-id="e845d-121">Number</span></span> | <span data-ttu-id="e845d-122">Tämä ominaisuus määrittää välilehden, joka on oletusarvoisesti aktiivinen, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="e845d-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="e845d-123">Jos arvoa ei ole annettu, ensimmäinen välilehti on oletusarvon mukaan aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="e845d-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="e845d-124">Välilehtinimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e845d-124">Tab item module properties</span></span>

| <span data-ttu-id="e845d-125">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="e845d-125">Property name</span></span> | <span data-ttu-id="e845d-126">Arvot</span><span class="sxs-lookup"><span data-stu-id="e845d-126">Values</span></span> | <span data-ttu-id="e845d-127">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e845d-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e845d-128">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="e845d-128">Title</span></span> | <span data-ttu-id="e845d-129">Teksti</span><span class="sxs-lookup"><span data-stu-id="e845d-129">Text</span></span> | <span data-ttu-id="e845d-130">Tämä ominaisuus määrittää otsikkotekstin välilehtinimikemoduulille.</span><span class="sxs-lookup"><span data-stu-id="e845d-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="e845d-131">Välilehtimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="e845d-131">Add a tab module to a page</span></span>

<span data-ttu-id="e845d-132">Voit lisätä välilehtimoduulin sivulle ja määrittää ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e845d-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="e845d-133">Käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="e845d-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="e845d-134">Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e845d-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e845d-135">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e845d-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e845d-136">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e845d-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e845d-137">Valitse **Lisää moduuli** -valintaikkunassa **Välilehti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e845d-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e845d-138">Valitse välilehtimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="e845d-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="e845d-139">Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti** -kohtaan otsikkoteksti (esimerkiksi **Käytännöt**).</span><span class="sxs-lookup"><span data-stu-id="e845d-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="e845d-140">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e845d-140">Then select **OK**.</span></span>
1. <span data-ttu-id="e845d-141">Valitse kolme pistettä (**...**) **Välilehti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e845d-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e845d-142">Valitse **Lisää moduuli** -valintaikkunassa **Välilehtinimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e845d-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e845d-143">Kirjoita välilehtinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Toimitus**).</span><span class="sxs-lookup"><span data-stu-id="e845d-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="e845d-144">Valitse kolme pistettä (**...**) **Välilehtinimike**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="e845d-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e845d-145">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e845d-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e845d-146">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään tekstikappale.</span><span class="sxs-lookup"><span data-stu-id="e845d-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="e845d-147">Lisää **Välilehti**-paikkaan muutamia otsikoita sisältävän välilehtinimikkeen moduuleja.</span><span class="sxs-lookup"><span data-stu-id="e845d-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="e845d-148">Lisää kuhunkin välilehtinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.</span><span class="sxs-lookup"><span data-stu-id="e845d-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="e845d-149">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="e845d-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="e845d-150">Sivulla näkyy välilehtimoduuli, joka sisältää välilehtinimikemoduulit, joissa on lisäämäsi sisältö.</span><span class="sxs-lookup"><span data-stu-id="e845d-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="e845d-151">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="e845d-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e845d-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e845d-152">Additional resources</span></span>

[<span data-ttu-id="e845d-153">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e845d-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e845d-154">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="e845d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e845d-155">Haitarivalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="e845d-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="e845d-156">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="e845d-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]