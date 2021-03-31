---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5b0ce69f57e6ba691803752280466b41ced7c521
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206484"
---
# <a name="cart-module"></a><span data-ttu-id="b532a-103">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b532a-104">Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="b532a-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b532a-105">Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle.</span><span class="sxs-lookup"><span data-stu-id="b532a-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="b532a-106">Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="b532a-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="b532a-107">Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana.</span><span class="sxs-lookup"><span data-stu-id="b532a-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="b532a-108">Se tukee myös **Jatka ostoksia** -linkkejä.</span><span class="sxs-lookup"><span data-stu-id="b532a-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="b532a-109">Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.</span><span class="sxs-lookup"><span data-stu-id="b532a-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="b532a-110">Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste.</span><span class="sxs-lookup"><span data-stu-id="b532a-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="b532a-111">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.</span><span class="sxs-lookup"><span data-stu-id="b532a-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Esimerkki ostoskorimoduulista Fabrikam-sivustolla](./media/cart2.PNG)

<span data-ttu-id="b532a-113">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.</span><span class="sxs-lookup"><span data-stu-id="b532a-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="b532a-114">Tässä esimerkissä rivinimikkeelle on käsittelymaksu.</span><span class="sxs-lookup"><span data-stu-id="b532a-114">In this example, there is a handling fee for a line item.</span></span>

![Esimerkki ostoskorimoduulista, jossa on käsittelymaksu rivinimikkeelle](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="b532a-116">Ostoskorimoduulin ominaisuudet ja paikat</span><span class="sxs-lookup"><span data-stu-id="b532a-116">Cart module properties and slots</span></span>

| <span data-ttu-id="b532a-117">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="b532a-117">Property</span></span> | <span data-ttu-id="b532a-118">Arvot</span><span class="sxs-lookup"><span data-stu-id="b532a-118">Values</span></span> | <span data-ttu-id="b532a-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="b532a-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b532a-120">Otsikko</span><span class="sxs-lookup"><span data-stu-id="b532a-120">Heading</span></span> | <span data-ttu-id="b532a-121">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="b532a-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b532a-122">Otsikko ostoskorille, kuten Ostoskassi tai Ostoskorin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="b532a-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="b532a-123">Näytä Loppunut varastosta -virheet</span><span class="sxs-lookup"><span data-stu-id="b532a-123">Show out of stock errors</span></span> | <span data-ttu-id="b532a-124">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="b532a-124">**True** or **False**</span></span> | <span data-ttu-id="b532a-125">Jos tämän ominaisuuden arvo on **Tosi**, ostoskori-sivulla näkyvät varastoon liittyvät virheet.</span><span class="sxs-lookup"><span data-stu-id="b532a-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="b532a-126">On suositeltavaa määrittää tämän ominaisuuden arvoksi **Tosi**, jos varastotarkistuksia käytetään toimipaikassa.</span><span class="sxs-lookup"><span data-stu-id="b532a-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="b532a-127">Näytä rivinimikkeiden kuljetusmaksut</span><span class="sxs-lookup"><span data-stu-id="b532a-127">Show shipping charges for line items</span></span> | <span data-ttu-id="b532a-128">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="b532a-128">**True** or **False**</span></span> | <span data-ttu-id="b532a-129">Jos tämän ominaisuuden arvo on **Tosi**, ostoskorin rivinimikkeissä näkyy kuljetusmaksut, jos nämä tiedot ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b532a-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="b532a-130">Tämä toiminto ei ole tuettu Fabrikam-teemassa, koska käyttäjät valitsevat lähetyksen vain kassavirrasta.</span><span class="sxs-lookup"><span data-stu-id="b532a-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="b532a-131">Tämä toiminto voidaan kuitenkin ottaa käyttöön muissa työnkuluissa, jos se on sovellettavissa.</span><span class="sxs-lookup"><span data-stu-id="b532a-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="b532a-132">Näytä käytettävissä olevat kampanjat</span><span class="sxs-lookup"><span data-stu-id="b532a-132">Show available promotions</span></span>| <span data-ttu-id="b532a-133">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="b532a-133">**True** or **False**</span></span> | <span data-ttu-id="b532a-134">Jos ominaisuuden arvoksi määritetään **Tosi**, ostoskorissa näkyvät käytettävissä olevat kampanja-tarjoukset kärryssä olevien nimikkeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b532a-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="b532a-135">Tämä ominaisuus on saatavana Dynamics 365 Commercen versiossa 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="b532a-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="b532a-136">Moduulit, joita voidaan käyttää ostoskorimoduulissa</span><span class="sxs-lookup"><span data-stu-id="b532a-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="b532a-137">**Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="b532a-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="b532a-138">Sisällönhallintajärjestelmä (CMS) ohjaa viestintää.</span><span class="sxs-lookup"><span data-stu-id="b532a-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="b532a-139">Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b532a-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="b532a-140">**Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="b532a-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b532a-141">Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin.</span><span class="sxs-lookup"><span data-stu-id="b532a-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b532a-142">Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b532a-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="b532a-143">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b532a-143">Module properties</span></span>

<span data-ttu-id="b532a-144">Seuraavat ostoskorimoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:</span><span class="sxs-lookup"><span data-stu-id="b532a-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b532a-145">**Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="b532a-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b532a-146">Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.</span><span class="sxs-lookup"><span data-stu-id="b532a-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b532a-147">**Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b532a-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="b532a-148">**Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti.</span><span class="sxs-lookup"><span data-stu-id="b532a-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="b532a-149">Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.</span><span class="sxs-lookup"><span data-stu-id="b532a-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b532a-150">Dynamics 365 Commerce versiossa 10.0.14 ja sitä uudemmissa versioissa nimikkeet kerätään ostoskoriin Commercen pääkonttoriversion verkkokaupan verkkotoimintoprofiilissa määritettyjen asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="b532a-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="b532a-151">Lisätietoja verkkotoimintoprofiilin luomisesta ja koostamiseen tarvittavien ominaisuuksien määrittämisestä on kohdassa [Verkkotoimintoprofiilin luominen](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="b532a-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b532a-152">Commerce Scale Unit -käyttö</span><span class="sxs-lookup"><span data-stu-id="b532a-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b532a-153">Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="b532a-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="b532a-154">Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.</span><span class="sxs-lookup"><span data-stu-id="b532a-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="b532a-155">Ostoskorimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="b532a-155">Add a cart module to a page</span></span>

<span data-ttu-id="b532a-156">Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b532a-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b532a-157">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="b532a-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b532a-158">Valitse **Uusi osa** -valintaikkunassa **Ostoskori**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="b532a-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="b532a-159">Kirjoita **Osan nimi** -kohtaan **Ostoskorin osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b532a-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="b532a-160">Valitse **Ostoskori**-paikka.</span><span class="sxs-lookup"><span data-stu-id="b532a-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="b532a-161">Valitse oikealla olevassa ominaisuudet-ruudussa kynäsymboli, kirjoita otsikko tekstikenttään ja valitse sitten valintamerkkisymboli.</span><span class="sxs-lookup"><span data-stu-id="b532a-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="b532a-162">Valitse kolme pistettä (**...**) **Ostoskori**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="b532a-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b532a-163">Valitse **Lisää moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b532a-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b532a-164">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b532a-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b532a-165">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="b532a-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b532a-166">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="b532a-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="b532a-167">Valitse jäsennyspuussa **Tekstiosa**-paikka. Valitse kolme pistettä (**...**) ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="b532a-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="b532a-168">Valitse **Valitse osa** -valintaikkunassa **Ostoskorin osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b532a-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b532a-169">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="b532a-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b532a-170">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="b532a-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b532a-171">Valitse **Valitse malli** -valintaikkunassa malli, jonka loit aiemmin, lisää sivun nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b532a-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="b532a-172">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="b532a-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b532a-173">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="b532a-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b532a-174">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b532a-174">Additional resources</span></span>

[<span data-ttu-id="b532a-175">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b532a-176">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b532a-177">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b532a-178">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b532a-179">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b532a-180">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b532a-181">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b532a-182">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="b532a-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b532a-183">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="b532a-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="b532a-184">Luo online-toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="b532a-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]