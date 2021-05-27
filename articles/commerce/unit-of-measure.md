---
title: Käytä mittayksikön asetuksia
description: Tässä ohjeaiheessa käsitellään mittayksikön asetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022371"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="678d2-103">Käytä mittayksikön asetuksia</span><span class="sxs-lookup"><span data-stu-id="678d2-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="678d2-104">Tässä ohjeaiheessa käsitellään mittayksikön asetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="678d2-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="678d2-105">Tuote voidaan myydä eri yksikköinä, esimerkiksi "kappale", "pari" ja "tusina".</span><span class="sxs-lookup"><span data-stu-id="678d2-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="678d2-106">Commerce-pääkonttorisovelluksessa tuotteen myyntimittayksikkö voidaan määrittää ja se voidaan näyttää sähköisenä kauppapaikkana.</span><span class="sxs-lookup"><span data-stu-id="678d2-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="678d2-107">Jos esimerkiksi jälleenmyyjä myy tuotteen sekä yksittäin että tusinana, käytettävissä olevat mittayksiköt voidaan näyttää yhdessä muiden tuotetietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="678d2-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="678d2-108">Seuraavassa esimerkissä on esitetty, että Commerce-pääkonttorisovelluksen tuotteelle on määritetty myyntimittayksikkö **kpl**.</span><span class="sxs-lookup"><span data-stu-id="678d2-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Esimerkki tuotteesta, joka on konfiguroitu mittayksiköllä Commerce-pääkonttorisovelluksessa](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="678d2-110">Mittayksikön kohdistamisen ja näyttämisen tuki on käytettävissä Commerce-versiosta 10.0.19 alkaen.</span><span class="sxs-lookup"><span data-stu-id="678d2-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="678d2-111">Mittayksikön asetukset</span><span class="sxs-lookup"><span data-stu-id="678d2-111">Unit of measure settings</span></span>

<span data-ttu-id="678d2-112">Mittayksikön näyttöasetukset määritetään Commercen sivustonmuodostimessa kohdassa **Sivuston asetukset \> Laajennukset \> Näytä tuotteiden mittayksikkö**.</span><span class="sxs-lookup"><span data-stu-id="678d2-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="678d2-113">Tuettuja asetuksia on kolme:</span><span class="sxs-lookup"><span data-stu-id="678d2-113">There are three supported settings:</span></span>

- <span data-ttu-id="678d2-114">**Älä näytä** – Kun tämä asetus on valittuna, sähköisen kaupankäynnin toimipaikka ei näytä tuotteen mittayksikköä.</span><span class="sxs-lookup"><span data-stu-id="678d2-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="678d2-115">Tämä on oletusasetus.</span><span class="sxs-lookup"><span data-stu-id="678d2-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="678d2-116">**Näytä tuotteen ostokokemuksessa** – Kun tämä asetus valitaan, mittayksikkö näkyy tuotetietosivuilla, ostoskorissa, kassalla, tilaushistoriassa ja tilausten erittelysivuilla.</span><span class="sxs-lookup"><span data-stu-id="678d2-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="678d2-117">**Näytä tuotteen selaus- ja ostokokemuksessa** – Kun tämä asetus valitaan, mittayksikkö näkyy tuotteen ostokokemussivuilla sekä tuotteen selauskokemuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="678d2-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="678d2-118">Osana tätä toimintatapaa mittayksiköt näkyvät hakutuloksissa ja tuotekokoelman moduuleissa.</span><span class="sxs-lookup"><span data-stu-id="678d2-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="678d2-119">Mittayksikön näyttöasetukset ovat käytettävissä Commerce-versiosta 10.0.19 alkaen.</span><span class="sxs-lookup"><span data-stu-id="678d2-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="678d2-120">Jos päivität vanhemmasta Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="678d2-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="678d2-121">Ohjeita on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="678d2-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="678d2-122">Mittayksikköasetuksia käyttävät moduulit</span><span class="sxs-lookup"><span data-stu-id="678d2-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="678d2-123">Mittayksikköasetuksia käyttävät moduulit sisältävät ostoruudun, toiveluettelon, ostoskorin, ostoskorikuvakkeen, hakutulossäilön, tuotekokoelman, kassan ja tilaustietojen moduulit.</span><span class="sxs-lookup"><span data-stu-id="678d2-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="678d2-124">Seuraavassa kuvan esimerkissä tuotetietosivu (PDP) näyttää tuotteen mittayksikön (**kpl**).</span><span class="sxs-lookup"><span data-stu-id="678d2-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Esimerkki tuotetietosivusta, jossa on näkyvissä mittayksikkö](./media/Productunit-PDP.png)

<span data-ttu-id="678d2-126">Seuraavassa kuvan esimerkissä tuotekokoelmamoduuli näyttää tuotteen mittayksikön (**kpl**).</span><span class="sxs-lookup"><span data-stu-id="678d2-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Esimerkki tuotekokoelmamoduulista, jossa on näkyvissä mittayksikkö](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="678d2-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="678d2-128">Additional resources</span></span>

[<span data-ttu-id="678d2-129">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="678d2-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="678d2-130">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="678d2-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="678d2-131">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="678d2-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="678d2-132">Tilin hallintasivut ja -moduulit</span><span class="sxs-lookup"><span data-stu-id="678d2-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="678d2-133">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="678d2-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
