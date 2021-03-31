---
title: Haitarimoduuli
description: Tässä ohjeaiheessa on tietoja haitarivalikkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: a08441f5dffa9c2c65b304d0265dd107a838a685
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206604"
---
# <a name="accordion-module"></a><span data-ttu-id="7820e-103">Haitarivalikkomoduuli</span><span class="sxs-lookup"><span data-stu-id="7820e-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7820e-104">Tässä ohjeaiheessa on tietoja haitarivalikkomoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="7820e-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7820e-105">Haitarimoduulit ovat konttimoduulin kaltaisia ja niitä käytetään tietojen tai moduulien järjestämiseen sivulla tarjoamalla tiivistettävän laatikon kaltaisen ominaisuuden.</span><span class="sxs-lookup"><span data-stu-id="7820e-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="7820e-106">Haitarimoduulia voidaan käyttää millä tahansa sivulla.</span><span class="sxs-lookup"><span data-stu-id="7820e-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="7820e-107">Jokaisen haitarimoduulin sisällä voidaan lisätä yksi tai useampia haitarinimikemoduuleja.</span><span class="sxs-lookup"><span data-stu-id="7820e-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="7820e-108">Jokainen haitarinimikemoduuli edustaa tiivistettävää laatikkoa.</span><span class="sxs-lookup"><span data-stu-id="7820e-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="7820e-109">Jokaisen haitarinimikemoduulin sisällä voidaan lisätä yksi tai useampia moduuleja.</span><span class="sxs-lookup"><span data-stu-id="7820e-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="7820e-110">Haitarinimikemoduuleihin lisättävien moduulien tyyppiä ei ole rajoitettu.</span><span class="sxs-lookup"><span data-stu-id="7820e-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="7820e-111">Seuraavassa kuvassa on esimerkki haitarimoduulista, jota käytetään myymälän usein kysyttyjen kysymysten (FAQ) tietojen järjestämiseen.</span><span class="sxs-lookup"><span data-stu-id="7820e-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Esimerkki haitarimoduulista](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="7820e-113">Haitarimoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="7820e-113">Accordion module properties</span></span>

| <span data-ttu-id="7820e-114">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="7820e-114">Property name</span></span> | <span data-ttu-id="7820e-115">Arvot</span><span class="sxs-lookup"><span data-stu-id="7820e-115">Values</span></span> | <span data-ttu-id="7820e-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="7820e-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="7820e-117">Otsikko</span><span class="sxs-lookup"><span data-stu-id="7820e-117">Heading</span></span> | <span data-ttu-id="7820e-118">Teksti</span><span class="sxs-lookup"><span data-stu-id="7820e-118">Text</span></span> | <span data-ttu-id="7820e-119">Tämä ominaisuus määrittää valinnaisen tekstiotsikon haitarimoduulille.</span><span class="sxs-lookup"><span data-stu-id="7820e-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="7820e-120">Laajenna kaikki</span><span class="sxs-lookup"><span data-stu-id="7820e-120">Expand All</span></span> | <span data-ttu-id="7820e-121">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="7820e-121">**True** or **False**</span></span> | <span data-ttu-id="7820e-122">Jos arvoksi on määritetty **Tosi**, laajenna/tiivistä-toiminto on käytössä, jotta kaikki haitarimoduulin kohteet voidaan laajentaa ja tiivistää.</span><span class="sxs-lookup"><span data-stu-id="7820e-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="7820e-123">Vuorovaikutustyyli</span><span class="sxs-lookup"><span data-stu-id="7820e-123">Interaction Style</span></span> | <span data-ttu-id="7820e-124">**Itsenäinen** tai **Laajenna vain yksi nimike**</span><span class="sxs-lookup"><span data-stu-id="7820e-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="7820e-125">Tämä ominaisuus määrittää haitarinimikkeiden vuorovaikutuksen tyylin.</span><span class="sxs-lookup"><span data-stu-id="7820e-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="7820e-126">Jos arvoksi on määritetty **Itsenäinen**, jokainen haitarikohde voidaan laajentaa tai tiivistää itsenäisesti.</span><span class="sxs-lookup"><span data-stu-id="7820e-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="7820e-127">Jos arvo on määritetty niin, että **vain yksi nimike laajennetaan**, vain yksi nimike voidaan laajentaa kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="7820e-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="7820e-128">Kun nimikkeitä laajennetaan, aiemmin laajennetut nimikkeet tiivistetään.</span><span class="sxs-lookup"><span data-stu-id="7820e-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="7820e-129">Haitarinimikemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="7820e-129">Accordion item module properties</span></span>

| <span data-ttu-id="7820e-130">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="7820e-130">Property name</span></span> | <span data-ttu-id="7820e-131">Arvot</span><span class="sxs-lookup"><span data-stu-id="7820e-131">Values</span></span> | <span data-ttu-id="7820e-132">kuvaus</span><span class="sxs-lookup"><span data-stu-id="7820e-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="7820e-133">Tehtävänimike</span><span class="sxs-lookup"><span data-stu-id="7820e-133">Title</span></span> | <span data-ttu-id="7820e-134">Teksti</span><span class="sxs-lookup"><span data-stu-id="7820e-134">Text</span></span> | <span data-ttu-id="7820e-135">Tämä ominaisuus määrittää otsikkotekstin haitarinimikemoduulille.</span><span class="sxs-lookup"><span data-stu-id="7820e-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="7820e-136">Kun valitset otsikkoalueen, käyttäjät voivat laajentaa tai tiivistää osan.</span><span class="sxs-lookup"><span data-stu-id="7820e-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="7820e-137">Laajenna oletusarvoisesti</span><span class="sxs-lookup"><span data-stu-id="7820e-137">Expand by default</span></span> | <span data-ttu-id="7820e-138">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="7820e-138">**True** or **False**</span></span> | <span data-ttu-id="7820e-139">Jos arvoksi on määritetty **Tosi**, haitarikohde laajennetaan oletuksena, kun sivu ladataan.</span><span class="sxs-lookup"><span data-stu-id="7820e-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="7820e-140">Haitarimoduulin lisääminen Usein kysyttyjä kysymyksiä -sivulle</span><span class="sxs-lookup"><span data-stu-id="7820e-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="7820e-141">Voit lisätä haitarimoduulin Usein kysyttyjä kysymyksiä -sivulle ja määrittää sen ominaisuudet sivuston luontityökalussa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7820e-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7820e-142">Siirry kohteeseen **Sivut** ja käytä Fabrikam-markkinointimallia (tai mitä tahansa mallia, jolla ei ole rajoituksia) luodaksesi uuden sivun nimeltä **Myymälän usein kysytyt kysymykset**.</span><span class="sxs-lookup"><span data-stu-id="7820e-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="7820e-143">Valitse **Oletussivulla** **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7820e-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7820e-144">Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7820e-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7820e-145">Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7820e-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7820e-146">Valitse **Lisää moduuli** -valintaikkunassa **Haitari**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7820e-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7820e-147">Valitse haitarimoduulin ominaisuusruudussa kynäsymbolin vieressä oleva **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="7820e-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="7820e-148">Lisää **Usein kysyttyjä kysymyksiä** **Otsikko**-valintaikkunan **Otsikon teksti** -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="7820e-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="7820e-149">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7820e-149">Then select **OK**.</span></span>
1. <span data-ttu-id="7820e-150">Valitse haitarimoduulin ominaisuusruudussa **Näytä Laajenna kaikki** -valintaruutu ja valitse sitten **Vuorovaikutustyyli**-kentästä **Itsenäinen**.</span><span class="sxs-lookup"><span data-stu-id="7820e-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="7820e-151">Valitse kolme pistettä (**...**) **Haitari**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7820e-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7820e-152">Valitse **Lisää moduuli** -valintaikkunassa **Haitarinimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7820e-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7820e-153">Kirjoita haitarinimikemoduulin ominaisuusruudussa **Otsikon** kohdalle otsikkoteksti (esimerkiksi **Miten palautus toimii?**).</span><span class="sxs-lookup"><span data-stu-id="7820e-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="7820e-154">Valitse kolme pistettä (**...**) **Haitarinimike**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7820e-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7820e-155">Valitse **Lisää moduuli** -valintaikkunassa **Tekstilohko**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7820e-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7820e-156">Kirjoita tekstilohkomoduulin ominaisuusruutuun tekstikappale (esimerkiksi **Palautus on käsiteltävä Call Centerin kautta. Ota yhteyttä 1-800-FABRIKAM palautuksiin liittyen. Tuotteilla on 30 päivän palautuskäytäntö. Palautus on aloitettava tämän aikavälin sisällä.**).</span><span class="sxs-lookup"><span data-stu-id="7820e-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="7820e-157">Lisää **Haitari**-paikassa muutama haitarinimikemoduuli.</span><span class="sxs-lookup"><span data-stu-id="7820e-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="7820e-158">Lisää kuhunkin haitarinimikemoduuliin tekstilohkomoduuli, jossa on sisältöä.</span><span class="sxs-lookup"><span data-stu-id="7820e-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="7820e-159">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="7820e-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="7820e-160">Sivulla näkyy haitarimoduuli, jossa on lisäämäsi sisältö.</span><span class="sxs-lookup"><span data-stu-id="7820e-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="7820e-161">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="7820e-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7820e-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7820e-162">Additional resources</span></span>

[<span data-ttu-id="7820e-163">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7820e-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7820e-164">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="7820e-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7820e-165">Välilehtimoduuli</span><span class="sxs-lookup"><span data-stu-id="7820e-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="7820e-166">Tekstilohkomoduuli</span><span class="sxs-lookup"><span data-stu-id="7820e-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]