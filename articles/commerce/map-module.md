---
title: Karttamoduuli
description: Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: d2cbc67a186a76647a4f7ddc7942b15d3e469ece
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817203"
---
# <a name="map-module"></a><span data-ttu-id="d67f9-103">Karttamoduuli</span><span class="sxs-lookup"><span data-stu-id="d67f9-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="d67f9-104">Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="d67f9-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d67f9-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d67f9-105">Overview</span></span>

<span data-ttu-id="d67f9-106">Karttamoduuli, jossa näkyvät myymälöiden sijainnit [Bing Maps V8 -verkko-ohjausobjektin](https://docs.microsoft.com/bingmaps/v8-web-control/) avulla hahmonnetussa interaktiivisessa kartassa.</span><span class="sxs-lookup"><span data-stu-id="d67f9-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="d67f9-107">Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Commercen pääkonttorisovelluksen jaettuihin parametreihin.</span><span class="sxs-lookup"><span data-stu-id="d67f9-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="d67f9-108">Karttamoduulit tarjoavat erilaisia näkymiä, kuten maantie-, ilma- ja katunäkymät. Niiden avulla käyttäjät voivat tarkastella karttasijainteja.</span><span class="sxs-lookup"><span data-stu-id="d67f9-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="d67f9-109">Ne mahdollistavat myös vuorovaikutuksen, kuten zoomauksen ja käyttäjän sijainnin käyttämisen.</span><span class="sxs-lookup"><span data-stu-id="d67f9-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="d67f9-110">Karttamoduuli toimii yhdessä myymälän valitsinmoduulin kanssa ja määrittää kartalla muodostettujen myymälöiden maantieteelliset sijainnit.</span><span class="sxs-lookup"><span data-stu-id="d67f9-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="d67f9-111">Myymälän valitsin ja karttamoduulit ovat vuorovaikutuksessa, kun käyttäjä valitsee myymälän jollakin sivustosivulla olevista moduuleista.</span><span class="sxs-lookup"><span data-stu-id="d67f9-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="d67f9-112">Karttamoduuleja voidaan laajentaa muihin skenaarioihin myymälän valitsinmoduulien vuorovaikutuksen lisäksi.</span><span class="sxs-lookup"><span data-stu-id="d67f9-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="d67f9-113">Moduulin mukautus on kuitenkin pakollinen.</span><span class="sxs-lookup"><span data-stu-id="d67f9-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="d67f9-114">Karttamoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="d67f9-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="d67f9-115">Seuraavassa kuvassa näkyy esimerkki karttsmoduulista, jota käytetään myymälän sijaintien sivulla.</span><span class="sxs-lookup"><span data-stu-id="d67f9-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Esimerkki myymälän valitsinmoduulista](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="d67f9-117">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d67f9-117">Module properties</span></span>

| <span data-ttu-id="d67f9-118">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="d67f9-118">Property name</span></span>             | <span data-ttu-id="d67f9-119">Arvo</span><span class="sxs-lookup"><span data-stu-id="d67f9-119">Value</span></span>                 | <span data-ttu-id="d67f9-120">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d67f9-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="d67f9-121">Otsikko</span><span class="sxs-lookup"><span data-stu-id="d67f9-121">Heading</span></span> | <span data-ttu-id="d67f9-122">Teksti</span><span class="sxs-lookup"><span data-stu-id="d67f9-122">Text</span></span> | <span data-ttu-id="d67f9-123">Moduulin otsikko.</span><span class="sxs-lookup"><span data-stu-id="d67f9-123">The heading for the module.</span></span> |
| <span data-ttu-id="d67f9-124">Nuppineula-asetukset: Oletuskuvake</span><span class="sxs-lookup"><span data-stu-id="d67f9-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="d67f9-125">Kuva</span><span class="sxs-lookup"><span data-stu-id="d67f9-125">Image</span></span> | <span data-ttu-id="d67f9-126">Nuppineulasymbolin kuva, jota käytetään kartalla näkyvissä myymälöissä.</span><span class="sxs-lookup"><span data-stu-id="d67f9-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="d67f9-127">Nuppineula-asetukset: Aktiivinen-kuvake</span><span class="sxs-lookup"><span data-stu-id="d67f9-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="d67f9-128">Kuva</span><span class="sxs-lookup"><span data-stu-id="d67f9-128">Image</span></span> | <span data-ttu-id="d67f9-129">Nuppineulasymbolin kuva, jota käytetään kartalla valitussa myymälässä.</span><span class="sxs-lookup"><span data-stu-id="d67f9-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="d67f9-130">Nuppineula-asetukset: Oletuskuvakkeen väri</span><span class="sxs-lookup"><span data-stu-id="d67f9-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="d67f9-131">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="d67f9-131">Character string</span></span> | <span data-ttu-id="d67f9-132">Kartan nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo.</span><span class="sxs-lookup"><span data-stu-id="d67f9-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="d67f9-133">Nuppineula-asetukset: Aktiivinen-kuvakkeen väri</span><span class="sxs-lookup"><span data-stu-id="d67f9-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="d67f9-134">Merkkijono</span><span class="sxs-lookup"><span data-stu-id="d67f9-134">Character string</span></span> | <span data-ttu-id="d67f9-135">Kartan valittujen nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo.</span><span class="sxs-lookup"><span data-stu-id="d67f9-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="d67f9-136">Näytä indeksi</span><span class="sxs-lookup"><span data-stu-id="d67f9-136">Show index</span></span> | <span data-ttu-id="d67f9-137">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="d67f9-137">**True** or **False**</span></span> | <span data-ttu-id="d67f9-138">Jos tämän ominaisuuden arvoksi on määritetty **Tosi**, jokainen myymälän osoittava nuppineulasymboli näyttää indeksin.</span><span class="sxs-lookup"><span data-stu-id="d67f9-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="d67f9-139">Tämä indeksi vastaa sellaisen luettelonäkymän indeksiä, jonka myymälän valitsinmoduuli näyttää.</span><span class="sxs-lookup"><span data-stu-id="d67f9-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="d67f9-140">Sallittujen yhdistämismääritysten URL-osoitteiden lisääminen sivuston sisällön suojauskäytännön direktiiveihin</span><span class="sxs-lookup"><span data-stu-id="d67f9-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="d67f9-141">Jotta karttamoduuli voi toimia yhdessä Bing Mapsin kanssa, varmista, että seuraavat yhdistämismääritysten URL-osoitteet ovat sallittuja (sallittujen luettelo) sivuston sisällön suojauskäytännön mukaan.</span><span class="sxs-lookup"><span data-stu-id="d67f9-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="d67f9-142">Tämä asetus tehdään Commercen sivustonmuodostimessa lisäämällä sallitut URL-osoitteet eri sivustojen CSP-direktiiveihin (esimerkiksi **img-src**).</span><span class="sxs-lookup"><span data-stu-id="d67f9-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="d67f9-143">Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="d67f9-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="d67f9-144">Lisää **connect-src**-direktiiviin **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="d67f9-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="d67f9-145">Lisää **img-src**-direktiiviin **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="d67f9-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="d67f9-146">Lisää **script-src**-direktiiviin **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="d67f9-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="d67f9-147">Lisää **skriptin style-src** -direktiiviin **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="d67f9-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="d67f9-148">Karttamoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="d67f9-148">Add a map module to a page</span></span>

<span data-ttu-id="d67f9-149">Lisätietoja karttamoduulin määrittämisestä sivulla on kohdassa [Myymälän valitsinmoduuli](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d67f9-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="d67f9-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d67f9-150">Additional resources</span></span>

[<span data-ttu-id="d67f9-151">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d67f9-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d67f9-152">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="d67f9-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d67f9-153">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="d67f9-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d67f9-154">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="d67f9-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="d67f9-155">Bing Maps -karttapalvelun hallinta organisaatiossa</span><span class="sxs-lookup"><span data-stu-id="d67f9-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="d67f9-156">Bing Maps V8 -verkko-ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="d67f9-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
