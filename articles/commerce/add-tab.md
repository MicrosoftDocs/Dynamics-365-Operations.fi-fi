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
ms.openlocfilehash: 42c3cd99897627dbcdbdec91cfdb03d5743f7388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980179"
---
# <a name="tab-module"></a><span data-ttu-id="65534-103">Välilehtimoduuli</span><span class="sxs-lookup"><span data-stu-id="65534-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65534-104">Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="65534-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="65534-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="65534-105">Overview</span></span>

<span data-ttu-id="65534-106">Välilehtimoduulit ovat kontin kaltaisia moduuleja, joita käytetään välilehtien sivujen tietojen järjestämiseen.</span><span class="sxs-lookup"><span data-stu-id="65534-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="65534-107">Niitä voidaan käyttää millä tahansa sivulla, jolla tiedot on esitettävä välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="65534-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="65534-108">Jokaisessa välilehtimoduulissa voidaan lisätä yksi tai useampia välilehtimoduuleja.</span><span class="sxs-lookup"><span data-stu-id="65534-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="65534-109">Jokainen välilehtinimikemoduuli edustaa yhtä välilehteä. Jokaiseen välilehtinimikemoduuliin voidaan lisätä yksi tai useita moduuleja.</span><span class="sxs-lookup"><span data-stu-id="65534-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="65534-110">Välilehtinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="65534-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="65534-111">Seuraavassa kuvassa on esimerkki välilehtimoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="65534-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="65534-112">Tässä esimerkissä valittu **Toimitus**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="65534-112">In this example, the **Shipping** tab selected.</span></span>

![Esimerkki välilehtimoduulista](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="65534-114">Välilehtimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="65534-114">Tab module properties</span></span>

| <span data-ttu-id="65534-115">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="65534-115">Property name</span></span> | <span data-ttu-id="65534-116">Arvot</span><span class="sxs-lookup"><span data-stu-id="65534-116">Values</span></span> | <span data-ttu-id="65534-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="65534-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="65534-118">Otsikko</span><span class="sxs-lookup"><span data-stu-id="65534-118">Heading</span></span> | <span data-ttu-id="65534-119">Teksti</span><span class="sxs-lookup"><span data-stu-id="65534-119">Text</span></span> | <span data-ttu-id="65534-120">Tämä ominaisuus määrittää valinnaisen tekstiotsikon välilehtimoduulille.</span><span class="sxs-lookup"><span data-stu-id="65534-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="65534-121">Aktiivinen välilehden indeksi</span><span class="sxs-lookup"><span data-stu-id="65534-121">Active Tab Index</span></span> | <span data-ttu-id="65534-122">Numero</span><span class="sxs-lookup"><span data-stu-id="65534-122">Number</span></span> | <span data-ttu-id="65534-123">Tämä ominaisuus määrittää välilehden, joka on oletusarvoisesti aktiivinen, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="65534-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="65534-124">Jos arvoa ei ole annettu, ensimmäinen välilehti on oletusarvon mukaan aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="65534-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="65534-125">Välilehtinimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="65534-125">Tab item module properties</span></span>

| <span data-ttu-id="65534-126">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="65534-126">Property name</span></span> | <span data-ttu-id="65534-127">Arvot</span><span class="sxs-lookup"><span data-stu-id="65534-127">Values</span></span> | <span data-ttu-id="65534-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="65534-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="65534-129">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="65534-129">Title</span></span> | <span data-ttu-id="65534-130">Teksti</span><span class="sxs-lookup"><span data-stu-id="65534-130">Text</span></span> | <span data-ttu-id="65534-131">Tämä ominaisuus määrittää otsikkotekstin välilehtinimikemoduulille.</span><span class="sxs-lookup"><span data-stu-id="65534-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="65534-132">Välilehtimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="65534-132">Add a tab module to a page</span></span>

<span data-ttu-id="65534-133">Voit lisätä välilehtimoduulin sivulle ja määrittää ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="65534-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="65534-134">Käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="65534-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="65534-135">Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="65534-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65534-136">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65534-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65534-137">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="65534-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65534-138">Valitse **Lisää moduuli** -valintaikkunassa **Välilehti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65534-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65534-139">Valitse välilehtimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="65534-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="65534-140">Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti** -kohtaan otsikkoteksti (esimerkiksi **Käytännöt**).</span><span class="sxs-lookup"><span data-stu-id="65534-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="65534-141">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65534-141">Then select **OK**.</span></span>
1. <span data-ttu-id="65534-142">Valitse kolme pistettä (**...**) **Välilehti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="65534-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65534-143">Valitse **Lisää moduuli** -valintaikkunassa **Välilehtinimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65534-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65534-144">Kirjoita välilehtinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Toimitus**).</span><span class="sxs-lookup"><span data-stu-id="65534-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="65534-145">Valitse kolme pistettä (**...**) **Välilehtinimike**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="65534-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65534-146">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="65534-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65534-147">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään tekstikappale.</span><span class="sxs-lookup"><span data-stu-id="65534-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="65534-148">Lisää **Välilehti**-paikkaan muutamia otsikoita sisältävän välilehtinimikkeen moduuleja.</span><span class="sxs-lookup"><span data-stu-id="65534-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="65534-149">Lisää kuhunkin välilehtinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.</span><span class="sxs-lookup"><span data-stu-id="65534-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="65534-150">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="65534-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="65534-151">Sivulla näkyy välilehtimoduuli, joka sisältää välilehtinimikemoduulit, joissa on lisäämäsi sisältö.</span><span class="sxs-lookup"><span data-stu-id="65534-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="65534-152">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="65534-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65534-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="65534-153">Additional resources</span></span>

[<span data-ttu-id="65534-154">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="65534-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="65534-155">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="65534-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="65534-156">Haitarivalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="65534-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="65534-157">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="65534-157">Text block module</span></span>](add-content-rich-block.md)
