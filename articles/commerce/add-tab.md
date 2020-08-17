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
ms.openlocfilehash: b4187dfd704c78d506d7840b04c986687fe807a3
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621010"
---
# <a name="tab-module"></a><span data-ttu-id="d2224-103">Välilehtimoduuli</span><span class="sxs-lookup"><span data-stu-id="d2224-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2224-104">Tässä ohjeaiheessa on tietoja välilehtimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="d2224-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d2224-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d2224-105">Overview</span></span>

<span data-ttu-id="d2224-106">Välilehtimoduulit ovat kontin kaltaisia moduuleja, joita käytetään välilehtien sivujen tietojen järjestämiseen.</span><span class="sxs-lookup"><span data-stu-id="d2224-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="d2224-107">Niitä voidaan käyttää millä tahansa sivulla, jolla tiedot on esitettävä välilehdissä.</span><span class="sxs-lookup"><span data-stu-id="d2224-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="d2224-108">Jokaisessa välilehtimoduulissa voidaan lisätä yksi tai useampia välilehtimoduuleja.</span><span class="sxs-lookup"><span data-stu-id="d2224-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="d2224-109">Jokainen välilehtinimikemoduuli edustaa yhtä välilehteä. Jokaiseen välilehtinimikemoduuliin voidaan lisätä yksi tai useita moduuleja.</span><span class="sxs-lookup"><span data-stu-id="d2224-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="d2224-110">Välilehtinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="d2224-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="d2224-111">Seuraavassa kuvassa on esimerkki välilehtimoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="d2224-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="d2224-112">Tässä esimerkissä valittu **Toimitus**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="d2224-112">In this example, the **Shipping** tab selected.</span></span>

![Esimerkki välilehtimoduulista](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="d2224-114">Välilehtimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d2224-114">Tab module properties</span></span>

| <span data-ttu-id="d2224-115">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="d2224-115">Property name</span></span> | <span data-ttu-id="d2224-116">Arvot</span><span class="sxs-lookup"><span data-stu-id="d2224-116">Values</span></span> | <span data-ttu-id="d2224-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d2224-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d2224-118">Otsikko</span><span class="sxs-lookup"><span data-stu-id="d2224-118">Heading</span></span> | <span data-ttu-id="d2224-119">Teksti</span><span class="sxs-lookup"><span data-stu-id="d2224-119">Text</span></span> | <span data-ttu-id="d2224-120">Tämä ominaisuus määrittää valinnaisen tekstiotsikon välilehtimoduulille.</span><span class="sxs-lookup"><span data-stu-id="d2224-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="d2224-121">Aktiivinen välilehden indeksi</span><span class="sxs-lookup"><span data-stu-id="d2224-121">Active Tab Index</span></span> | <span data-ttu-id="d2224-122">Numero</span><span class="sxs-lookup"><span data-stu-id="d2224-122">Number</span></span> | <span data-ttu-id="d2224-123">Tämä ominaisuus määrittää välilehden, joka on oletusarvoisesti aktiivinen, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="d2224-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="d2224-124">Jos arvoa ei ole annettu, ensimmäinen välilehti on oletusarvon mukaan aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="d2224-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="d2224-125">Välilehtinimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d2224-125">Tab item module properties</span></span>

| <span data-ttu-id="d2224-126">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="d2224-126">Property name</span></span> | <span data-ttu-id="d2224-127">Arvot</span><span class="sxs-lookup"><span data-stu-id="d2224-127">Values</span></span> | <span data-ttu-id="d2224-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d2224-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d2224-129">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="d2224-129">Title</span></span> | <span data-ttu-id="d2224-130">Teksti</span><span class="sxs-lookup"><span data-stu-id="d2224-130">Text</span></span> | <span data-ttu-id="d2224-131">Tämä ominaisuus määrittää otsikkotekstin välilehtinimikemoduulille.</span><span class="sxs-lookup"><span data-stu-id="d2224-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="d2224-132">Välilehtimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="d2224-132">Add a tab module to a page</span></span>

<span data-ttu-id="d2224-133">Voit lisätä välilehtimoduulin sivulle ja määrittää ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d2224-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="d2224-134">Käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="d2224-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="d2224-135">Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="d2224-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2224-136">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2224-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2224-137">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="d2224-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2224-138">Valitse **Lisää moduuli** -valintaikkunassa **Välilehti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2224-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2224-139">Valitse välilehtimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="d2224-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d2224-140">Kirjoita **Otsikko**-valintaikkunan **Otsikkoteksti** -kohtaan otsikkoteksti (esimerkiksi **Käytännöt**).</span><span class="sxs-lookup"><span data-stu-id="d2224-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="d2224-141">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2224-141">Then select **OK**.</span></span>
1. <span data-ttu-id="d2224-142">Valitse kolme pistettä (**...**) **Välilehti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="d2224-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2224-143">Valitse **Lisää moduuli** -valintaikkunassa **Välilehtinimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2224-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2224-144">Kirjoita välilehtinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Toimitus**).</span><span class="sxs-lookup"><span data-stu-id="d2224-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="d2224-145">Valitse kolme pistettä (**...**) **Välilehtinimike**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="d2224-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d2224-146">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2224-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d2224-147">Lisää tekstiä tekstilohkomoduulin ominaisuusruudun **RTF**-kenttään tekstikappale.</span><span class="sxs-lookup"><span data-stu-id="d2224-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="d2224-148">Lisää **Välilehti**-paikkaan muutamia otsikoita sisältävän välilehtinimikkeen moduuleja.</span><span class="sxs-lookup"><span data-stu-id="d2224-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="d2224-149">Lisää kuhunkin välilehtinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.</span><span class="sxs-lookup"><span data-stu-id="d2224-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="d2224-150">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="d2224-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d2224-151">Sivulla näkyy välilehtimoduuli, joka sisältää välilehtinimikemoduulit, joissa on lisäämäsi sisältö.</span><span class="sxs-lookup"><span data-stu-id="d2224-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="d2224-152">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="d2224-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2224-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d2224-153">Additional resources</span></span>

[<span data-ttu-id="d2224-154">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d2224-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d2224-155">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="d2224-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d2224-156">Haitarimoduuli</span><span class="sxs-lookup"><span data-stu-id="d2224-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="d2224-157">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="d2224-157">Text block module</span></span>](add-content-rich-block.md)
