---
title: Karttamoduuli
description: Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646920"
---
# <a name="map-module"></a><span data-ttu-id="2b9c7-103">Karttamoduuli</span><span class="sxs-lookup"><span data-stu-id="2b9c7-103">Map module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2b9c7-104">Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b9c7-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="2b9c7-105">Overview</span></span>

<span data-ttu-id="2b9c7-106">Karttamoduuli, jossa näkyvät myymälöiden sijainnit [Bing Maps V8 -verkko-ohjausobjektin](https://docs.microsoft.com/bingmaps/v8-web-control/) avulla hahmonnetussa interaktiivisessa kartassa.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="2b9c7-107">Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Commercen pääkonttorisovelluksen jaettuihin parametreihin.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="2b9c7-108">Karttamoduulit tarjoavat erilaisia näkymiä, kuten maantie-, ilma- ja katunäkymät. Niiden avulla käyttäjät voivat tarkastella karttasijainteja.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="2b9c7-109">Ne mahdollistavat myös vuorovaikutuksen, kuten zoomauksen ja käyttäjän sijainnin käyttämisen.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="2b9c7-110">Karttamoduuli toimii yhdessä myymälän valitsinmoduulin kanssa ja määrittää kartalla muodostettujen myymälöiden maantieteelliset sijainnit.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="2b9c7-111">Myymälän valitsin ja karttamoduulit ovat vuorovaikutuksessa, kun käyttäjä valitsee myymälän jollakin sivustosivulla olevista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="2b9c7-112">Karttamoduuleja voidaan laajentaa muihin skenaarioihin myymälän valitsinmoduulien vuorovaikutuksen lisäksi.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="2b9c7-113">Moduulin mukautus on kuitenkin pakollinen.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-113">However, module customization is required.</span></span>

<span data-ttu-id="2b9c7-114">Karttamoduuli esiteltiin Commercen versiossa 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="2b9c7-115">Seuraavassa kuvassa näkyy esimerkki karttsmoduulista, jota käytetään myymälän sijaintien sivulla.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Esimerkki myymälän valitsinmoduulista](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="2b9c7-117">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2b9c7-117">Module properties</span></span>

| <span data-ttu-id="2b9c7-118">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="2b9c7-118">Property name</span></span>             | <span data-ttu-id="2b9c7-119">Arvo</span><span class="sxs-lookup"><span data-stu-id="2b9c7-119">Value</span></span>                 | <span data-ttu-id="2b9c7-120">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2b9c7-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2b9c7-121">Otsikko</span><span class="sxs-lookup"><span data-stu-id="2b9c7-121">Heading</span></span> | <span data-ttu-id="2b9c7-122">Teksti</span><span class="sxs-lookup"><span data-stu-id="2b9c7-122">Text</span></span> | <span data-ttu-id="2b9c7-123">Moduulin otsikko.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-123">The heading for the module.</span></span> |
| <span data-ttu-id="2b9c7-124">Nuppineula-asetukset: Oletuskuvake</span><span class="sxs-lookup"><span data-stu-id="2b9c7-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="2b9c7-125">Kuva</span><span class="sxs-lookup"><span data-stu-id="2b9c7-125">Image</span></span> | <span data-ttu-id="2b9c7-126">Nuppineulasymbolin kuva, jota käytetään kartalla näkyvissä myymälöissä.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="2b9c7-127">Nuppineula-asetukset: Aktiivinen-kuvake</span><span class="sxs-lookup"><span data-stu-id="2b9c7-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="2b9c7-128">Kuva</span><span class="sxs-lookup"><span data-stu-id="2b9c7-128">Image</span></span> | <span data-ttu-id="2b9c7-129">Nuppineulasymbolin kuva, jota käytetään kartalla valitussa myymälässä.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="2b9c7-130">Nuppineula-asetukset: Oletuskuvakkeen väri</span><span class="sxs-lookup"><span data-stu-id="2b9c7-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="2b9c7-131">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="2b9c7-131">Character string</span></span> | <span data-ttu-id="2b9c7-132">Kartan nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="2b9c7-133">Nuppineula-asetukset: Aktiivinen-kuvakkeen väri</span><span class="sxs-lookup"><span data-stu-id="2b9c7-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="2b9c7-134">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="2b9c7-134">Character string</span></span> | <span data-ttu-id="2b9c7-135">Kartan valittujen nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="2b9c7-136">Näytä indeksi</span><span class="sxs-lookup"><span data-stu-id="2b9c7-136">Show index</span></span> | <span data-ttu-id="2b9c7-137">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="2b9c7-137">**True** or **False**</span></span> | <span data-ttu-id="2b9c7-138">Jos tämän ominaisuuden arvoksi on määritetty **Tosi**, jokainen myymälän osoittava nuppineulasymboli näyttää indeksin.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="2b9c7-139">Tämä indeksi vastaa sellaisen luettelonäkymän indeksiä, jonka myymälän valitsinmoduuli näyttää.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="2b9c7-140">Sallittujen yhdistämismääritysten URL-osoitteiden lisääminen sivuston sisällön suojauskäytännön direktiiveihin</span><span class="sxs-lookup"><span data-stu-id="2b9c7-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="2b9c7-141">Jotta karttamoduuli voi toimia yhdessä Bing Mapsin kanssa, varmista, että seuraavat yhdistämismääritysten URL-osoitteet ovat sallittuja (sallittujen luettelo) sivuston sisällön suojauskäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="2b9c7-142">Tämä asetus tehdään Commercen sivustonmuodostimessa lisäämällä sallitut URL-osoitteet eri sivustojen CSP-direktiiveihin (esimerkiksi **img-src**).</span><span class="sxs-lookup"><span data-stu-id="2b9c7-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="2b9c7-143">Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="2b9c7-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="2b9c7-144">Lisää **connect-src**-direktiiviin **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="2b9c7-145">Lisää **img-src**-direktiiviin **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="2b9c7-146">Lisää **script-src**-direktiiviin **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="2b9c7-147">Lisää **skriptin style-src** -direktiiviin **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="2b9c7-148">Karttamoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="2b9c7-148">Add a map module to a page</span></span>

<span data-ttu-id="2b9c7-149">Lisätietoja karttamoduulin määrittämisestä sivulla on kohdassa [Myymälän valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="2b9c7-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="2b9c7-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2b9c7-150">Additional resources</span></span>

[<span data-ttu-id="2b9c7-151">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2b9c7-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2b9c7-152">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="2b9c7-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2b9c7-153">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="2b9c7-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2b9c7-154">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="2b9c7-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="2b9c7-155">Bing Maps -karttapalvelun hallinta organisaatiossa</span><span class="sxs-lookup"><span data-stu-id="2b9c7-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="2b9c7-156">Bing Maps V8 -verkko-ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="2b9c7-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
