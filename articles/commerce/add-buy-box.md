---
title: Ostoruutumoduuli
description: Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686667"
---
# <a name="buy-box-module"></a><span data-ttu-id="4458d-103">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4458d-104">Tässä ohjeaiheessa on tietoja ostoruutumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="4458d-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4458d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4458d-105">Overview</span></span>

<span data-ttu-id="4458d-106">Termi *ostoruutu* viittaa yleensä tuotetietojen sivun alueeseen, joka on sivun yläosassa ja joka isännöi kaikkein tärkeimpiä tuotteen ostamisessa tarvittavia tietoja.</span><span class="sxs-lookup"><span data-stu-id="4458d-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="4458d-107">(Alue, joka näkyy, kun sivu ladataan ensimmäisen kerran. Näin käyttäjien ei tarvitse vierittää sivua alaspäin nähdäkseen tiedot.)</span><span class="sxs-lookup"><span data-stu-id="4458d-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="4458d-108">Ostoruutumoduuli on erityinen säilö, jota käytetään kaikkien tuotetietosivun ostoruutualueella näkyvien moduulien isännöinnissä.</span><span class="sxs-lookup"><span data-stu-id="4458d-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="4458d-109">Tuotetietosivun URL-osoite sisältää tuotteen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="4458d-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="4458d-110">Kaikki ostoruudun hahmontamisessa vaadittavat tiedot saadaan tästä tuotteen tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="4458d-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="4458d-111">Jos tuotteen tunnusta ei ole annettu, ostoruutumoduulia ei hahmonneta sivulla oikein.</span><span class="sxs-lookup"><span data-stu-id="4458d-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="4458d-112">Tämän vuoksi ostoruutumoduulia voidaan käyttää vain sivuilla, joilla on tuotekonteksti.</span><span class="sxs-lookup"><span data-stu-id="4458d-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="4458d-113">Jos sitä halutaan käyttää sivulla, jolla ei ole tuotekontekstia (kuten aloitus- tai markkinointisivulla), sitä mukautettava lisää.</span><span class="sxs-lookup"><span data-stu-id="4458d-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="4458d-114">Seuraavassa kuvassa näkyy esimerkki ostoruutumoduulista tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="4458d-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Esimerkki ostoruutumoduulista](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="4458d-116">Ostoruutumoduulin ominaisuudet ja paikat</span><span class="sxs-lookup"><span data-stu-id="4458d-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="4458d-117">Ostoruutu jaetaan tuotetietosivulla kahteen alueeseen: media-alue vasemmalla ja sisältöalue oikealla.</span><span class="sxs-lookup"><span data-stu-id="4458d-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="4458d-118">Oletusarvoisesti media-aluesarakkeen leveyden ja sisältöaluesarakkeen leveyden välinen suhde on 2:1.</span><span class="sxs-lookup"><span data-stu-id="4458d-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="4458d-119">Mobiililaitteissa nämä kaksi aluetta pinotaan niin, että alueet näkyvät allekkain.</span><span class="sxs-lookup"><span data-stu-id="4458d-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="4458d-120">Sarakeleveyksiä ja pinoamisjärjestystä voi mukauttaa teemojen avulla.</span><span class="sxs-lookup"><span data-stu-id="4458d-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="4458d-121">Ostoruutumoduuli hahmontaa tuotteen otsikon, kuvauksen, hinnan ja luokitukset.</span><span class="sxs-lookup"><span data-stu-id="4458d-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="4458d-122">Lisäksi asiakkaat voivat valita sen avulla tuotevariantit, joilla on eri tuotemääritteet, kuten koko, tyyli ja väri.</span><span class="sxs-lookup"><span data-stu-id="4458d-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="4458d-123">Kun tuotevariantti on valittuna, muut ostoruudun ominaisuudet (esimerkiksi tuotteen kuvaus ja kuvat) päivitetään muuttujan tietojen mukaisiksi.</span><span class="sxs-lookup"><span data-stu-id="4458d-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="4458d-124">Asiakkaat voivat määrittää annetun määrävalitsimen avulla ostettavien nimikkeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="4458d-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="4458d-125">Sivuston asetuksissa voidaan määrittää suurin sallittu ostomäärä.</span><span class="sxs-lookup"><span data-stu-id="4458d-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="4458d-126">Asiakkaat voivat suorittaa ostoruudussa myös muita toimintoja, kuten lisätä tuotteen ostoskoriin tai toivelistalle ja valita noutosijainnin.</span><span class="sxs-lookup"><span data-stu-id="4458d-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="4458d-127">Nämä toiminnot voidaan tehdä tuotteen tai tuotevariantin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="4458d-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="4458d-128">Jos asiakas haluaa lisätä tuotteen toivelistaan, hänen on oltava kirjautuneena sisään.</span><span class="sxs-lookup"><span data-stu-id="4458d-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="4458d-129">Teemojen avulla voidaan poistaa ostoruudun tuoteominaisuuksien ja toimintojen ohjausobjekteja tai muuttaa niiden järjestystä.</span><span class="sxs-lookup"><span data-stu-id="4458d-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="4458d-130">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4458d-130">Module properties</span></span>

- <span data-ttu-id="4458d-131">**Otsikon tunniste** – Tämä ominaisuus määrittää tuoteotsikon otsikon tunnisteen.</span><span class="sxs-lookup"><span data-stu-id="4458d-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="4458d-132">Jos ostoruutu on sivun yläosassa, helppokäyttöisyysstandardit täyttyvät, kun tämän ominaisuuden arvona on **h1**.</span><span class="sxs-lookup"><span data-stu-id="4458d-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="4458d-133">Moduulit, joita voidaan käyttää ostoruutumoduulissa</span><span class="sxs-lookup"><span data-stu-id="4458d-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="4458d-134">**Mediavalikoima** – Tämän moduulin avulla esitellään tuotteen kuvat tuotetietosivulla.</span><span class="sxs-lookup"><span data-stu-id="4458d-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="4458d-135">Lisätietoja tästä moduulista on kohdassa [Mediavalikoimamoduuli](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="4458d-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="4458d-136">**Myymälän valitsin** – Tämä moduuli näyttää luettelon lähellä olevista myymälöistä, joista nimikkeen voi noutaa.</span><span class="sxs-lookup"><span data-stu-id="4458d-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="4458d-137">Käyttäjät voivat etsiä lähellä olevia myymälöitä antamalla sijainnin.</span><span class="sxs-lookup"><span data-stu-id="4458d-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="4458d-138">Lisätietoja tästä moduulista on kohdassa [Myymälävalitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="4458d-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="4458d-139">Ostoruutumoduulin asetukset</span><span class="sxs-lookup"><span data-stu-id="4458d-139">Buy box module settings</span></span>

<span data-ttu-id="4458d-140">Seuraavat ostoruutumoduuliasetukset voidaan määrittää valitsemalla **Sivuston asetukset \> Laajennukset**:</span><span class="sxs-lookup"><span data-stu-id="4458d-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="4458d-141">**Ostoskorin rivien maksimimäärä** – Tätä ominaisuutta käytetään määrittämään kunkin ostoskoriin lisättävän nimikkeen enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="4458d-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="4458d-142">Jälleenmyyjä voi esimerkiksi päättää, että yhdessä tapahtumassa voidaan myydä vain 10 kappaletta kutakin tuotetta.</span><span class="sxs-lookup"><span data-stu-id="4458d-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="4458d-143">**Varasto** – lisätietoja varastoasetusten ottamisesta käyttöön on kohdassa [Varastoasetusten käyttäminen](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4458d-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="4458d-144">**Lisää ostoskoriin** - Tämän ominaisuuden avulla määritetään, mitä tapahtuu, kun nimike on lisätty ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="4458d-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="4458d-145">Mahdolliset arvot ovat **Siirry ostoskoriin**, **Älä siirry ostoskoriin** ja **Näytä ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="4458d-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="4458d-146">Kun arvoksi on määritetty **Siirry ostoskoriin**, käyttäjät lähetetään ostoskorisivulle, kun he lisäävät nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="4458d-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="4458d-147">Kun arvoksi on määritetty **Älä siirry ostoskoriin**, käyttäjiä ei lähetetä ostoskorisivulle, kun he lisäävät nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="4458d-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="4458d-148">Kun arvoksi on määritetty **Näytä ilmoitukset**, käyttäjille näytetään vahvistusilmoitus ja he voivat jatkaa selaamista tuotteen tiedot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4458d-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="4458d-149">Seuraavassa kuvassa on esimerkki Siirretty ostoskoriin -vahvistusilmoituksesta Fabrikam-sivustolla.</span><span class="sxs-lookup"><span data-stu-id="4458d-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Esimerkki ilmoitusmoduulista](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="4458d-151">Commerce Scale Unit -käyttö</span><span class="sxs-lookup"><span data-stu-id="4458d-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="4458d-152">Ostoruutumoduuli hakee tuotetiedot Commerce Scale Unitin ohjelmistorajapintojen (API) avulla.</span><span class="sxs-lookup"><span data-stu-id="4458d-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="4458d-153">Tuotetietosivulla olevaa tuotteen tunnusta käytetään kaikkien tietojen noutamisessa.</span><span class="sxs-lookup"><span data-stu-id="4458d-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="4458d-154">Ostoruutumoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="4458d-154">Add a buy box module to a page</span></span>

<span data-ttu-id="4458d-155">Voit lisätä ostoruutumoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4458d-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4458d-156">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="4458d-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="4458d-157">Valitse **Uusi sivun osa** -valintaikkunassa **Ostoruutu**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="4458d-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="4458d-158">Kirjoita **Sivun osan nimi** -kohtaan **Ostoruudun osa** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-159">Valitse ostoruutumoduulissa **Mediavalikoima**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="4458d-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4458d-160">Valitse **Lisää moduuli** -valintaikkunassa **Mediavalikoima**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-161">Valitse ostoruutumoduulissa **Myymälävalitsin**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="4458d-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4458d-162">Valitse **Lisää moduuli** -valintaikkunassa **Myymälävalitsin**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-163">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="4458d-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4458d-164">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="4458d-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="4458d-165">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **PDP-malli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-166">Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="4458d-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4458d-167">Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-168">Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="4458d-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="4458d-169">Valitse **Valitse sivun osa** -valintaikkunassa **Ostoruutuosa**, jonka loit aiemmin ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-170">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="4458d-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4458d-171">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="4458d-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="4458d-172">Valitse **Valitse malli** -valintaikkunassa **PDP-malli**-pohja.</span><span class="sxs-lookup"><span data-stu-id="4458d-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="4458d-173">Kirjoita **Sivun nimi** -kohtaan **PDP-sivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-174">Valitse uudella sivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="4458d-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="4458d-175">Valitse **Valitse sivun osa** -valintaikkunassa **Ostoruutuosa**, jonka loit aiemmin ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4458d-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="4458d-176">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="4458d-176">Save and preview the page.</span></span> <span data-ttu-id="4458d-177">Lisää **?productid=&lt;tuotteen tunnus&gt;** -kyselymerkkijonoparametri esikatselusivun URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="4458d-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="4458d-178">Näin tuotekontekstia käytetään esikatselusivun lataamiseen ja käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="4458d-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="4458d-179">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="4458d-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="4458d-180">Tuotetietosivulla näkyy ostoruutu.</span><span class="sxs-lookup"><span data-stu-id="4458d-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4458d-181">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4458d-181">Additional resources</span></span>

[<span data-ttu-id="4458d-182">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="4458d-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4458d-183">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="4458d-184">Mediavalikoimamoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="4458d-185">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4458d-186">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4458d-187">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4458d-188">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4458d-189">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4458d-190">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4458d-191">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="4458d-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="4458d-192">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="4458d-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
