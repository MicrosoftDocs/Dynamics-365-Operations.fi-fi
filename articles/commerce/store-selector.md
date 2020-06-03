---
title: Myymälän valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään myymälän valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378205"
---
# <a name="store-selector-module"></a><span data-ttu-id="7a144-103">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="7a144-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a144-104">Tässä ohjeaiheessa käsitellään myymälän valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="7a144-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7a144-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7a144-105">Overview</span></span>

<span data-ttu-id="7a144-106">Myymälän valitsinmoduulia käytetään "Osta verkosta, nouto myymälässä" (BOPIS) -asiakasskenaariossa.</span><span class="sxs-lookup"><span data-stu-id="7a144-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="7a144-107">Se näyttää luettelon myymälöistä, joissa tuote on noudettavissa, sekä myymälän aukioloajat ja tuotteen varastosaldon kullekin myymälälle.</span><span class="sxs-lookup"><span data-stu-id="7a144-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="7a144-108">Myymälän valitsinmoduuli vaatii tuotteen kontekstin ja hakusijainnin myymälöiden löytämiseksi.</span><span class="sxs-lookup"><span data-stu-id="7a144-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="7a144-109">Jos hakusijaintia ei ole, oletusarvona käytetään asiakkaan selaimen sijaintia edellyttäen, että asiakas antaa suostumuksensa.</span><span class="sxs-lookup"><span data-stu-id="7a144-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="7a144-110">Moduulissa on syöttöruutu, jonka avulla asiakas voi kirjoittaa sijainnin (postinumeron tai kaupungin ja osavaltion) lähellä olevien myymälöiden löytämiseksi.</span><span class="sxs-lookup"><span data-stu-id="7a144-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="7a144-111">Myymälän valitsinmoduuli on integroitu Bing Maps -geokoodauksen ohjelmointirajapintaan, jota käytetään muuntamaan sijainti leveys- ja pituusasteiksi.</span><span class="sxs-lookup"><span data-stu-id="7a144-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="7a144-112">Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä kaupankäynnin yhteiset parametrit -sivulla Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="7a144-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7a144-113">Myymälän valitsinmoduuli voidaan lisätä tuotteen tietosivun (PDP) ostolaatikkomoduuliin, jossa näkyvät myymälät, joissa tuote on noudettavissa.</span><span class="sxs-lookup"><span data-stu-id="7a144-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="7a144-114">Se voidaan lisätä myös ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="7a144-114">It can also be added to a cart module.</span></span> <span data-ttu-id="7a144-115">Kun tuote lisätään ostoskorimoduuliin, myymälän valitsinmoduuli näyttää kunkin ostoskorin rivinimikkeen noutovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="7a144-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="7a144-116">Lisäksi mukautetulla koodauksella tämä moduuli voidaan lisätä muille sivuille tai moduuleihin laajennusten ja mukautuksien kautta.</span><span class="sxs-lookup"><span data-stu-id="7a144-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="7a144-117">Jotta BOPIS-skenaario toimisi, tuotteet on konfiguroitava Asiakasnouto-toimitustilaan.</span><span class="sxs-lookup"><span data-stu-id="7a144-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="7a144-118">Muussa tapauksessa moduulia ei näytetä vastaavilla sivuilla.</span><span class="sxs-lookup"><span data-stu-id="7a144-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="7a144-119">Lisätietoja toimitustilan konfiguroinnista on kohdassa [Toimitustapojen määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="7a144-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="7a144-120">Seuraavassa kuvassa on esimerkki PDP:n käytössä olevasta myymälän valitsinmoduulista.</span><span class="sxs-lookup"><span data-stu-id="7a144-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Esimerkki myymälän valitsinmoduulista](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="7a144-122">Myymälän valitsinmoduulin käyttö sähköisessä kaupankäynnissä</span><span class="sxs-lookup"><span data-stu-id="7a144-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="7a144-123">Myymälän valitsinmoduulia voidaan käyttää tuotteen tietosivulla (PDP), etsimään lähimyymälöitä, joissa tuote on noudettavissa.</span><span class="sxs-lookup"><span data-stu-id="7a144-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="7a144-124">Myymälän valitsinmoduulia voidaan käyttää ostoskorisivulla, etsimään lähimyymälöitä, joissa korissa oleva tuote on noudettavissa.</span><span class="sxs-lookup"><span data-stu-id="7a144-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="7a144-125">Myymälän valitsinmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="7a144-125">Store selector module properties</span></span>

| <span data-ttu-id="7a144-126">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="7a144-126">Property name</span></span>             | <span data-ttu-id="7a144-127">Arvo</span><span class="sxs-lookup"><span data-stu-id="7a144-127">Value</span></span>                 | <span data-ttu-id="7a144-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="7a144-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="7a144-129">Hakusäde</span><span class="sxs-lookup"><span data-stu-id="7a144-129">Search radius</span></span> | <span data-ttu-id="7a144-130">Numero</span><span class="sxs-lookup"><span data-stu-id="7a144-130">Number</span></span> | <span data-ttu-id="7a144-131">Määrittää myymälöiden hakusäteen maileina.</span><span class="sxs-lookup"><span data-stu-id="7a144-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="7a144-132">Jos arvoa ei määritetä, käytössä on oletushakusäde 50 mailia.</span><span class="sxs-lookup"><span data-stu-id="7a144-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="7a144-133">Palveluehdot</span><span class="sxs-lookup"><span data-stu-id="7a144-133">Terms of Service</span></span> | <span data-ttu-id="7a144-134">URL-osoite</span><span class="sxs-lookup"><span data-stu-id="7a144-134">URL</span></span>    |  <span data-ttu-id="7a144-135">Palveluehtojen URL-osoite, joka on pakollinen Bing Maps -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="7a144-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="7a144-136">Myymälän valitsinmoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="7a144-136">Add a store selector module to a page</span></span>

<span data-ttu-id="7a144-137">Myymälän valitsinmoduuli tarvitsee tuotteen kontekstin, joten sitä voi käyttää vain osto- ja ostoskorimoduuleissa.</span><span class="sxs-lookup"><span data-stu-id="7a144-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="7a144-138">Myymälän valitsinmoduulit eivät toimi näiden moduulien ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="7a144-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="7a144-139">Lisätietoja myymälän valitsinmoduulin lisäämisestä ostomoduuliin on kohdassa [Ostomoduuli](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="7a144-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="7a144-140">Lisätietoja myymälän valitsinmoduulin lisäämisestä ostoskorimoduuliin on kohdassa [Ostoskorimoduuli](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="7a144-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a144-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7a144-141">Additional resources</span></span>

[<span data-ttu-id="7a144-142">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7a144-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7a144-143">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="7a144-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7a144-144">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="7a144-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7a144-145">PDP:n esittely</span><span class="sxs-lookup"><span data-stu-id="7a144-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="7a144-146">Ostoskorin ja kassan pikaesittely</span><span class="sxs-lookup"><span data-stu-id="7a144-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="7a144-147">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="7a144-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="7a144-148">Organisaationi Bing Mapsin hallinta</span><span class="sxs-lookup"><span data-stu-id="7a144-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
