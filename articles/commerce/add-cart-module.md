---
title: Ostoskorimoduuli
description: Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621033"
---
# <a name="cart-module"></a><span data-ttu-id="13a6b-103">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13a6b-104">Tässä ohjeaiheessa on tietoja ostoskorimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="13a6b-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="13a6b-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="13a6b-105">Overview</span></span>

<span data-ttu-id="13a6b-106">Ostokorimoduuli näyttää ostoskoriin lisätyt nimikkeet ennen asiakkaan siirtymistä kassalle.</span><span class="sxs-lookup"><span data-stu-id="13a6b-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="13a6b-107">Moduuli näyttää myös tilauksen yhteenvedon ja asiakas voi käyttää tarjouskoodeja tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="13a6b-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="13a6b-108">Ostoskorimoduuli tukee kirjautuneiden kassan käyttämistä kirjautuneena ja vieraana.</span><span class="sxs-lookup"><span data-stu-id="13a6b-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="13a6b-109">Se tukee myös **Jatka ostoksia** -linkkejä.</span><span class="sxs-lookup"><span data-stu-id="13a6b-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="13a6b-110">Voit määrittää tämän linkin reitin valitsemalla **Sivuston asetukset \> Laajennukset \> Reitit**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="13a6b-111">Ostoskorimoduuli esittää tiedot ostoskorin tunnuksen mukaan, joka on koko sivuston käytettävissä oleva selaineväste.</span><span class="sxs-lookup"><span data-stu-id="13a6b-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="13a6b-112">Seuraavassa kuvassa on esimerkki Fabrikam-sivuston ostoskärrysivusta.</span><span class="sxs-lookup"><span data-stu-id="13a6b-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Esimerkki ostoskärrymoduulista](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="13a6b-114">Ostoskorimoduulin ominaisuudet ja paikat</span><span class="sxs-lookup"><span data-stu-id="13a6b-114">Cart module properties and slots</span></span>

<span data-ttu-id="13a6b-115">Ostoskorimoduulissa on **Otsikko**-ominaisuus, jonka arvoiksi voidaan määrittää esimerkiksi **Ostoskassi** ja **Ostoskorin nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="13a6b-116">Moduulit, joita voidaan käyttää ostoskorimoduulissa</span><span class="sxs-lookup"><span data-stu-id="13a6b-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="13a6b-117">**Tekstilohko** – Tämä moduuli tukee mukautettua viestintää ostoskorimoduulissa.</span><span class="sxs-lookup"><span data-stu-id="13a6b-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="13a6b-118">Sisällönhallintajärjestelmä (CMS) ohjaa viestintää.</span><span class="sxs-lookup"><span data-stu-id="13a6b-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="13a6b-119">Voit lisätä minkä tahansa viestin, esimerkiksi Jos tilauksessa on ongelmia, soita numeroon 1-800-Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="13a6b-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="13a6b-120">**Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="13a6b-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="13a6b-121">Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin.</span><span class="sxs-lookup"><span data-stu-id="13a6b-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="13a6b-122">Lisätietoja tästä moduulista on kohdassa [Kaupan valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="13a6b-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="13a6b-123">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="13a6b-123">Module properties</span></span>

<span data-ttu-id="13a6b-124">Seuraavat ostoskorimoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:</span><span class="sxs-lookup"><span data-stu-id="13a6b-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="13a6b-125">**Maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="13a6b-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="13a6b-126">Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.</span><span class="sxs-lookup"><span data-stu-id="13a6b-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="13a6b-127">**Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="13a6b-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="13a6b-128">**Jatka ostoksia** – Tällä ominaisuudella määritetään **Jatka ostoksia** -linkin reitti.</span><span class="sxs-lookup"><span data-stu-id="13a6b-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="13a6b-129">Reitti voidaan konfiguroida sivuston tasolla, jolloin jälleenmyyjät voivat ohjata asiakkaan takaisin kotisivulle tai mille tahansa muulle sivuston sivulle.</span><span class="sxs-lookup"><span data-stu-id="13a6b-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="13a6b-130">Commerce Scale Unit -käyttö</span><span class="sxs-lookup"><span data-stu-id="13a6b-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="13a6b-131">Ostoskorimoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="13a6b-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="13a6b-132">Selaimen evästeen ostoskorin tunnusta käytetään kaikkien tuotetietojen noutamisessa Commerce Scale Unitista.</span><span class="sxs-lookup"><span data-stu-id="13a6b-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="13a6b-133">Ostoskorimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="13a6b-133">Add a cart module to a page</span></span>

<span data-ttu-id="13a6b-134">Voit lisätä ostoskorimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="13a6b-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="13a6b-135">Siirry kohtaan **Sivun osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="13a6b-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="13a6b-136">Valitse **Uusi sivun osa** -valintaikkunassa **Ostoskori**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="13a6b-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="13a6b-137">Kirjoita **Sivun osan nimi** -kohtaan **Ostoskorin osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="13a6b-138">Valitse **Ostoskori**-paikka.</span><span class="sxs-lookup"><span data-stu-id="13a6b-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="13a6b-139">Valitse oikealla olevassa ominaisuudet-ruudussa kynäsymboli, kirjoita otsikko tekstikenttään ja valitse sitten valintamerkkisymboli.</span><span class="sxs-lookup"><span data-stu-id="13a6b-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="13a6b-140">Valitse kolme pistettä (**...**) **Ostoskori**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="13a6b-141">Valitse **Lisää moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="13a6b-142">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="13a6b-143">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="13a6b-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="13a6b-144">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="13a6b-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="13a6b-145">Valitse jäsennyspuussa **Tekstiosa**-paikka. Valitse kolme pistettä (**...**) ja valitse sitten **Lisää osa**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="13a6b-146">Valitse **Valitse sivun osa** -valintaikkunassa **Ostoskorin osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="13a6b-147">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="13a6b-148">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="13a6b-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="13a6b-149">Valitse **Valitse malli** -valintaikkunassa malli, jonka loit aiemmin, lisää sivun nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="13a6b-150">Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="13a6b-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="13a6b-151">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="13a6b-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13a6b-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="13a6b-152">Additional resources</span></span>

[<span data-ttu-id="13a6b-153">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="13a6b-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="13a6b-154">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="13a6b-155">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="13a6b-156">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="13a6b-157">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="13a6b-158">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="13a6b-159">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="13a6b-160">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="13a6b-161">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="13a6b-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="13a6b-162">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="13a6b-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
