---
title: Välilehtimoduuli
description: Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c865d5e055e3fadf2dda225b49f13a163974768f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797452"
---
# <a name="tab-module"></a><span data-ttu-id="5d36a-103">Välilehtimoduuli</span><span class="sxs-lookup"><span data-stu-id="5d36a-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d36a-104">Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="5d36a-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5d36a-105">Välilehtimoduulit ovat kontin kaltaisia moduuleja, joita käytetään välilehtien sivujen tietojen järjestämiseen.</span><span class="sxs-lookup"><span data-stu-id="5d36a-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="5d36a-106">Niitä voidaan käyttää millä tahansa sivulla, jolla tiedot on esitettävä välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="5d36a-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="5d36a-107">Jokaisessa välilehtimoduulissa voidaan lisätä yksi tai useampia välilehtimoduuleja.</span><span class="sxs-lookup"><span data-stu-id="5d36a-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="5d36a-108">Jokainen välilehtinimikemoduuli edustaa yhtä välilehteä. Jokaiseen välilehtinimikemoduuliin voidaan lisätä yksi tai useita moduuleja.</span><span class="sxs-lookup"><span data-stu-id="5d36a-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="5d36a-109">Välilehtinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="5d36a-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="5d36a-110">Seuraavassa kuvassa on esimerkki välilehtimoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="5d36a-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="5d36a-111">Tässä esimerkissä valittu **Toimitus**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="5d36a-111">In this example, the **Shipping** tab selected.</span></span>

![Esimerkki välilehtimoduulista](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="5d36a-113">Välilehtimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5d36a-113">Tab module properties</span></span>

| <span data-ttu-id="5d36a-114">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5d36a-114">Property name</span></span> | <span data-ttu-id="5d36a-115">Arvot</span><span class="sxs-lookup"><span data-stu-id="5d36a-115">Values</span></span> | <span data-ttu-id="5d36a-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="5d36a-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5d36a-117">Otsikko</span><span class="sxs-lookup"><span data-stu-id="5d36a-117">Heading</span></span> | <span data-ttu-id="5d36a-118">Teksti</span><span class="sxs-lookup"><span data-stu-id="5d36a-118">Text</span></span> | <span data-ttu-id="5d36a-119">Tämä ominaisuus määrittää valinnaisen tekstiotsikon välilehtimoduulille.</span><span class="sxs-lookup"><span data-stu-id="5d36a-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="5d36a-120">Aktiivinen välilehden indeksi</span><span class="sxs-lookup"><span data-stu-id="5d36a-120">Active Tab Index</span></span> | <span data-ttu-id="5d36a-121">Numero</span><span class="sxs-lookup"><span data-stu-id="5d36a-121">Number</span></span> | <span data-ttu-id="5d36a-122">Tämä ominaisuus määrittää välilehden, joka on oletusarvoisesti aktiivinen, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="5d36a-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="5d36a-123">Jos arvoa ei ole annettu, ensimmäinen välilehti on oletusarvon mukaan aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="5d36a-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="5d36a-124">Välilehtinimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5d36a-124">Tab item module properties</span></span>

| <span data-ttu-id="5d36a-125">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="5d36a-125">Property name</span></span> | <span data-ttu-id="5d36a-126">Arvot</span><span class="sxs-lookup"><span data-stu-id="5d36a-126">Values</span></span> | <span data-ttu-id="5d36a-127">kuvaus</span><span class="sxs-lookup"><span data-stu-id="5d36a-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5d36a-128">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="5d36a-128">Title</span></span> | <span data-ttu-id="5d36a-129">Teksti</span><span class="sxs-lookup"><span data-stu-id="5d36a-129">Text</span></span> | <span data-ttu-id="5d36a-130">Tämä ominaisuus määrittää otsikkotekstin välilehtinimikemoduulille.</span><span class="sxs-lookup"><span data-stu-id="5d36a-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="5d36a-131">Välilehtimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="5d36a-131">Add a tab module to a page</span></span>

<span data-ttu-id="5d36a-132">Voit lisätä välilehtimoduulin sivulle ja määrittää ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5d36a-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="5d36a-133">Käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="5d36a-134">Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5d36a-135">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5d36a-136">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5d36a-137">Valitse **Lisää moduuli** -valintaikkunassa **Välilehti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5d36a-138">Valitse välilehtimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="5d36a-139">Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti** -kohtaan otsikkoteksti (esimerkiksi **Käytännöt**).</span><span class="sxs-lookup"><span data-stu-id="5d36a-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="5d36a-140">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-140">Then select **OK**.</span></span>
1. <span data-ttu-id="5d36a-141">Valitse kolme pistettä (**...**) **Välilehti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5d36a-142">Valitse **Lisää moduuli** -valintaikkunassa **Välilehtinimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5d36a-143">Kirjoita välilehtinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Toimitus**).</span><span class="sxs-lookup"><span data-stu-id="5d36a-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="5d36a-144">Valitse kolme pistettä (**...**) **Välilehtinimike**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5d36a-145">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5d36a-146">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään tekstikappale.</span><span class="sxs-lookup"><span data-stu-id="5d36a-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="5d36a-147">Lisää **Välilehti**-paikkaan muutamia otsikoita sisältävän välilehtinimikkeen moduuleja.</span><span class="sxs-lookup"><span data-stu-id="5d36a-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="5d36a-148">Lisää kuhunkin välilehtinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.</span><span class="sxs-lookup"><span data-stu-id="5d36a-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="5d36a-149">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="5d36a-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="5d36a-150">Sivulla näkyy välilehtimoduuli, joka sisältää välilehtinimikemoduulit, joissa on lisäämäsi sisältö.</span><span class="sxs-lookup"><span data-stu-id="5d36a-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="5d36a-151">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="5d36a-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d36a-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5d36a-152">Additional resources</span></span>

[<span data-ttu-id="5d36a-153">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5d36a-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5d36a-154">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="5d36a-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5d36a-155">Haitarivalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="5d36a-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="5d36a-156">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="5d36a-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]