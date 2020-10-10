---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818272"
---
# <a name="cart-module"></a><span data-ttu-id="d8ed3-103">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8ed3-104">Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8ed3-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d8ed3-105">Overview</span></span>

<span data-ttu-id="d8ed3-106">Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="d8ed3-107">Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="d8ed3-108">Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="d8ed3-109">Se tukee myös **Jatka ostoksia** -linkkejä.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="d8ed3-110">Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="d8ed3-111">Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="d8ed3-112">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Esimerkki ostoskorimoduulista Fabrikam-sivustolla](./media/cart2.PNG)

<span data-ttu-id="d8ed3-114">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="d8ed3-115">Tässä esimerkissä rivinimikkeelle on käsittelymaksu.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-115">In this example, there is a handling fee for a line item.</span></span>

![Esimerkki ostoskorimoduulista, jossa on käsittelymaksu rivinimikkeelle](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="d8ed3-117">Ostoskorimoduulin ominaisuudet ja paikat</span><span class="sxs-lookup"><span data-stu-id="d8ed3-117">Cart module properties and slots</span></span>

| <span data-ttu-id="d8ed3-118">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="d8ed3-118">Property</span></span> | <span data-ttu-id="d8ed3-119">Arvot</span><span class="sxs-lookup"><span data-stu-id="d8ed3-119">Values</span></span> | <span data-ttu-id="d8ed3-120">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d8ed3-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d8ed3-121">Otsikko</span><span class="sxs-lookup"><span data-stu-id="d8ed3-121">Heading</span></span> | <span data-ttu-id="d8ed3-122">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="d8ed3-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d8ed3-123">Otsikko ostoskorille, kuten Ostoskassi tai Ostoskorin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="d8ed3-124">Näytä Loppunut varastosta -virheet</span><span class="sxs-lookup"><span data-stu-id="d8ed3-124">Show out of stock errors</span></span> | <span data-ttu-id="d8ed3-125">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="d8ed3-125">**True** or **False**</span></span> | <span data-ttu-id="d8ed3-126">Jos tämän ominaisuuden arvo on **Tosi**, ostoskori-sivulla näkyvät varastoon liittyvät virheet.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="d8ed3-127">On suositeltavaa määrittää tämän ominaisuuden arvoksi **Tosi**, jos varastotarkistuksia käytetään toimipaikassa.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="d8ed3-128">Näytä rivinimikkeiden kuljetusmaksut</span><span class="sxs-lookup"><span data-stu-id="d8ed3-128">Show shipping charges for line items</span></span> | <span data-ttu-id="d8ed3-129">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="d8ed3-129">**True** or **False**</span></span> | <span data-ttu-id="d8ed3-130">Jos tämän ominaisuuden arvo on **Tosi**, ostoskorin rivinimikkeissä näkyy kuljetusmaksut, jos nämä tiedot ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="d8ed3-131">Tämä toiminto ei ole tuettu Fabrikam-teemassa, koska käyttäjät valitsevat lähetyksen vain kassavirrasta.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="d8ed3-132">Tämä toiminto voidaan kuitenkin ottaa käyttöön muissa työnkuluissa, jos se on sovellettavissa.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="d8ed3-133">Moduulit, joita voidaan käyttää ostoskorimoduulissa</span><span class="sxs-lookup"><span data-stu-id="d8ed3-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="d8ed3-134">**Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="d8ed3-135">Sisällönhallintajärjestelmä (CMS) ohjaa viestintää.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="d8ed3-136">Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="d8ed3-137">**Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="d8ed3-138">Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="d8ed3-139">Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d8ed3-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="d8ed3-140">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d8ed3-140">Module properties</span></span>

<span data-ttu-id="d8ed3-141">Seuraavat ostoskorimoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:</span><span class="sxs-lookup"><span data-stu-id="d8ed3-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="d8ed3-142">**Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="d8ed3-143">Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="d8ed3-144">**Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d8ed3-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="d8ed3-145">**Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="d8ed3-146">Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="d8ed3-147">Commerce Scale Unit -käyttö</span><span class="sxs-lookup"><span data-stu-id="d8ed3-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="d8ed3-148">Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="d8ed3-149">Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="d8ed3-150">Ostoskorimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="d8ed3-150">Add a cart module to a page</span></span>

<span data-ttu-id="d8ed3-151">Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d8ed3-152">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d8ed3-153">Valitse **Uusi osa** -valintaikkunassa **Ostoskori**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="d8ed3-154">Kirjoita **Osan nimi** -kohtaan **Ostoskorin osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="d8ed3-155">Valitse **Ostoskori**-paikka.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="d8ed3-156">Valitse oikealla olevassa ominaisuudet-ruudussa kynäsymboli, kirjoita otsikko tekstikenttään ja valitse sitten valintamerkkisymboli.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="d8ed3-157">Valitse kolme pistettä (**...**) **Ostoskori**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8ed3-158">Valitse **Lisää moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d8ed3-159">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d8ed3-160">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d8ed3-161">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="d8ed3-162">Valitse jäsennyspuussa **Tekstiosa**-paikka. Valitse kolme pistettä (**...**) ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d8ed3-163">Valitse **Valitse osa** -valintaikkunassa **Ostoskorin osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d8ed3-164">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d8ed3-165">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d8ed3-166">Valitse **Valitse malli** -valintaikkunassa malli, jonka loit aiemmin, lisää sivun nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="d8ed3-167">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d8ed3-168">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8ed3-169">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d8ed3-169">Additional resources</span></span>

[<span data-ttu-id="d8ed3-170">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d8ed3-171">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d8ed3-172">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d8ed3-173">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d8ed3-174">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d8ed3-175">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d8ed3-176">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="d8ed3-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="d8ed3-177">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="d8ed3-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
