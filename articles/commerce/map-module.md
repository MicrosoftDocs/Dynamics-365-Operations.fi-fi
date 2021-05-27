---
title: Karttamoduuli
description: Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 659211f3a74c38389f991cd2385366d175b0c7c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020256"
---
# <a name="map-module"></a><span data-ttu-id="9c1ab-103">Karttamoduuli</span><span class="sxs-lookup"><span data-stu-id="9c1ab-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="9c1ab-104">Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9c1ab-105">Karttamoduuli, jossa näkyvät myymälöiden sijainnit [Bing Maps V8 -verkko-ohjausobjektin](/bingmaps/v8-web-control/) avulla hahmonnetussa interaktiivisessa kartassa.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="9c1ab-106">Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Commercen pääkonttorisovelluksen jaettuihin parametreihin.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="9c1ab-107">Karttamoduulit tarjoavat erilaisia näkymiä, kuten maantie-, ilma- ja katunäkymät. Niiden avulla käyttäjät voivat tarkastella karttasijainteja.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="9c1ab-108">Ne mahdollistavat myös vuorovaikutuksen, kuten zoomauksen ja käyttäjän sijainnin käyttämisen.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="9c1ab-109">Karttamoduuli toimii yhdessä myymälän valitsinmoduulin kanssa ja määrittää kartalla muodostettujen myymälöiden maantieteelliset sijainnit.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="9c1ab-110">Myymälän valitsin ja karttamoduulit ovat vuorovaikutuksessa, kun käyttäjä valitsee myymälän jollakin sivustosivulla olevista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="9c1ab-111">Karttamoduuleja voidaan laajentaa muihin skenaarioihin myymälän valitsinmoduulien vuorovaikutuksen lisäksi.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="9c1ab-112">Moduulin mukautus on kuitenkin pakollinen.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="9c1ab-113">Karttamoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="9c1ab-114">Seuraavassa kuvassa näkyy esimerkki karttsmoduulista, jota käytetään myymälän sijaintien sivulla.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Esimerkki myymälän valitsinmoduulista](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="9c1ab-116">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="9c1ab-116">Module properties</span></span>

| <span data-ttu-id="9c1ab-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="9c1ab-117">Property name</span></span>             | <span data-ttu-id="9c1ab-118">Arvo</span><span class="sxs-lookup"><span data-stu-id="9c1ab-118">Value</span></span>                 | <span data-ttu-id="9c1ab-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="9c1ab-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="9c1ab-120">Otsikko</span><span class="sxs-lookup"><span data-stu-id="9c1ab-120">Heading</span></span> | <span data-ttu-id="9c1ab-121">Teksti</span><span class="sxs-lookup"><span data-stu-id="9c1ab-121">Text</span></span> | <span data-ttu-id="9c1ab-122">Moduulin otsikko.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-122">The heading for the module.</span></span> |
| <span data-ttu-id="9c1ab-123">Nuppineula-asetukset: Oletuskuvake</span><span class="sxs-lookup"><span data-stu-id="9c1ab-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="9c1ab-124">Kuva</span><span class="sxs-lookup"><span data-stu-id="9c1ab-124">Image</span></span> | <span data-ttu-id="9c1ab-125">Nuppineulasymbolin kuva, jota käytetään kartalla näkyvissä myymälöissä.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="9c1ab-126">Nuppineula-asetukset: Aktiivinen-kuvake</span><span class="sxs-lookup"><span data-stu-id="9c1ab-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="9c1ab-127">Kuva</span><span class="sxs-lookup"><span data-stu-id="9c1ab-127">Image</span></span> | <span data-ttu-id="9c1ab-128">Nuppineulasymbolin kuva, jota käytetään kartalla valitussa myymälässä.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="9c1ab-129">Nuppineula-asetukset: Oletuskuvakkeen väri</span><span class="sxs-lookup"><span data-stu-id="9c1ab-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="9c1ab-130">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="9c1ab-130">Character string</span></span> | <span data-ttu-id="9c1ab-131">Kartan nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="9c1ab-132">Nuppineula-asetukset: Aktiivinen-kuvakkeen väri</span><span class="sxs-lookup"><span data-stu-id="9c1ab-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="9c1ab-133">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="9c1ab-133">Character string</span></span> | <span data-ttu-id="9c1ab-134">Kartan valittujen nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="9c1ab-135">Näytä indeksi</span><span class="sxs-lookup"><span data-stu-id="9c1ab-135">Show index</span></span> | <span data-ttu-id="9c1ab-136">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="9c1ab-136">**True** or **False**</span></span> | <span data-ttu-id="9c1ab-137">Jos tämän ominaisuuden arvoksi on määritetty **Tosi**, jokainen myymälän osoittava nuppineulasymboli näyttää indeksin.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="9c1ab-138">Tämä indeksi vastaa sellaisen luettelonäkymän indeksiä, jonka myymälän valitsinmoduuli näyttää.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="9c1ab-139">Sallittujen yhdistämismääritysten URL-osoitteiden lisääminen sivuston sisällön suojauskäytännön direktiiveihin</span><span class="sxs-lookup"><span data-stu-id="9c1ab-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="9c1ab-140">Jotta karttamoduuli voi toimia yhdessä Bing Mapsin kanssa, varmista, että seuraavat yhdistämismääritysten URL-osoitteet ovat sallittuja sivuston sisällön suojauskäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="9c1ab-141">Tämä asetus tehdään Commercen sivustonmuodostimessa lisäämällä sallitut URL-osoitteet eri sivustojen CSP-direktiiveihin (esimerkiksi **img-src**).</span><span class="sxs-lookup"><span data-stu-id="9c1ab-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="9c1ab-142">Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="9c1ab-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="9c1ab-143">Lisää **connect-src**-direktiiviin **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="9c1ab-144">Lisää **img-src**-direktiiviin **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="9c1ab-145">Lisää **script-src**-direktiiviin **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="9c1ab-146">Lisää **skriptin style-src** -direktiiviin **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="9c1ab-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="9c1ab-147">Karttamoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="9c1ab-147">Add a map module to a page</span></span>

<span data-ttu-id="9c1ab-148">Lisätietoja karttamoduulin määrittämisestä sivulla on kohdassa [Myymälän valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="9c1ab-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="9c1ab-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9c1ab-149">Additional resources</span></span>

[<span data-ttu-id="9c1ab-150">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9c1ab-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9c1ab-151">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="9c1ab-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9c1ab-152">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="9c1ab-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9c1ab-153">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="9c1ab-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="9c1ab-154">Bing Maps -karttapalvelun hallinta organisaatiossa</span><span class="sxs-lookup"><span data-stu-id="9c1ab-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="9c1ab-155">Bing Maps V8 -verkko-ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="9c1ab-155">Bing Maps V8 Web Control</span></span>](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]