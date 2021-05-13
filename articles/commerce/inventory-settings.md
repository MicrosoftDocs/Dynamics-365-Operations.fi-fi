---
title: Varastoasetusten käyttäminen
description: Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
author: anupamar-ms
manager: annbe
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
ms.openlocfilehash: dd3db0039525c18521ad6a42b2f281976b7b236a
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937407"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="a61a9-103">Varastoasetusten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="a61a9-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a61a9-104">Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a61a9-105">Varastoasetukset määrittävät, tuleeko varasto tarkistaa, ennen kuin tuotteet lisätään kärryyn.</span><span class="sxs-lookup"><span data-stu-id="a61a9-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="a61a9-106">Ne määrittävät myös varastoon liittyvät myynninedistämispalkkiosanomat, kuten "varastossa" ja "vain muutama jäljellä".</span><span class="sxs-lookup"><span data-stu-id="a61a9-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="a61a9-107">Nämä asetukset varmistavat, että tuotetta ei voi ostaa, jos sitä ei ole varastossa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="a61a9-108">Dynamics 365 Commerce sisältää arviot tuotteiden käytettävissä olevasta saatavuudesta.</span><span class="sxs-lookup"><span data-stu-id="a61a9-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="a61a9-109">Lisätietoja arvioidun käytettävissä olevan käytettävyyden laskemisesta on kohdassa [Jälleenmyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="a61a9-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="a61a9-110">Commercen sivustotyökalussa voidaan määrittää tuotteen tai luokan varastorajat ja -alueet.</span><span class="sxs-lookup"><span data-stu-id="a61a9-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="a61a9-111">Ne määräävät, voidaanko varaston arvoksi luokitella varastossa, vähissä vai loppunut.</span><span class="sxs-lookup"><span data-stu-id="a61a9-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="a61a9-112">Katso lisätietoja kohdasta [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)</span><span class="sxs-lookup"><span data-stu-id="a61a9-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a61a9-113">Varaston raja-arvojen ja alueiden tuki on käytettävissä Dynamics 365 Commercen versiossa 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="a61a9-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="a61a9-114">Varastoasetukset</span><span class="sxs-lookup"><span data-stu-id="a61a9-114">Inventory settings</span></span>

<span data-ttu-id="a61a9-115">Commercessa varastoasetukset määritetään sivustotyökalussa kohdassa **Sivuston asetukset \> Laajennukset \> Varaston hallinta**.</span><span class="sxs-lookup"><span data-stu-id="a61a9-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="a61a9-116">Varastoasetuksia on viisi, joista yksi on poistettu käytöstä (vanhentunut):</span><span class="sxs-lookup"><span data-stu-id="a61a9-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="a61a9-117">**Ota käyttöön varastotarkistus sovelluksessa** – Tämä asetus ottaa tuotevaraston tarkistuksen pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="a61a9-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="a61a9-118">Osta-ruutu, ostoskori ja nouto myymälästä -moduulit tarkistavat tuotevaraston ja sallivat tuotteen lisäämisen ostoskoriin vain, jos varasto on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a61a9-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="a61a9-119">**Varastotaso perustuu** – Tämä asetus määrittää, miten varastotasot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a61a9-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="a61a9-120">Käytettävissä olevat arvot ovat **Käytettävissä olevat yhteensä**, **Fyysisesti käytettävissä olevat** ja **Loppu varastosta**.</span><span class="sxs-lookup"><span data-stu-id="a61a9-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="a61a9-121">Commercessa varaston kynnysarvo ja alueet voidaan määritellä jokaiselle tuotteelle ja luokalle.</span><span class="sxs-lookup"><span data-stu-id="a61a9-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="a61a9-122">Varasto-APIt palauttavat tuotevarastotiedot sekä **käytettävissä olevan kokonaismäärän** että **fyysisen käytettävissä olevan** ominaisuuden osalta.</span><span class="sxs-lookup"><span data-stu-id="a61a9-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="a61a9-123">Jälleenmyyjä päättää, käytetäänkö **Käytettävissä olevaa** tai **Fyysisesti käytettävissä olevaa** arvoa varaston inventoinnin ja varasto- ja loppuvarastotilojen vastaavien alueiden määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="a61a9-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="a61a9-124">**Loppunut varastosta** -arvo **Varastotason varaston kynnys arvo** asetuksen perusteella on vanha (aiempi), vanhentunut arvo.</span><span class="sxs-lookup"><span data-stu-id="a61a9-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="a61a9-125">Kun se on valittu, varaston inventoinnit määräytyvät **Käytettävissä olevan** kokonaisarvon perusteella, mutta kynnys määritetään myöhemmin annetun luvun **Loppu varastosta** -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="a61a9-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="a61a9-126">Tämä raja-asetus koskee kaikkia tuotteita, jotka ovat verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="a61a9-127">Jos varasto on raja-arvon alapuolella, tuotetta ei pidetä varastossa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="a61a9-128">Muussa tapauksessa sitä pidetään varastossa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="a61a9-129">**Loppu varastosta** -arvo on rajallinen, emmekä suosittele sen käyttämistä versiossa 10.0.12 ja sitä uudemmissa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="a61a9-130">**Usean varaston varastotaso** – Tämän asetuksen avulla varastotaso voidaan laskea oletusvarastoa tai useita varastoja vasten.</span><span class="sxs-lookup"><span data-stu-id="a61a9-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="a61a9-131">**Perustuu yksittäiseen varastoon** -vaihtoehto laskee varastotasot oletusvaraston perusteella.</span><span class="sxs-lookup"><span data-stu-id="a61a9-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="a61a9-132">Sähköisen kaupankäynnin toimipiste voi myös helpottaa täyttämistä viitaten useisiin varastoihin.</span><span class="sxs-lookup"><span data-stu-id="a61a9-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="a61a9-133">Tässä tapauksessa varaston käytettävyys ilmaistaan **lähetys- ja noutovarastojen koostamisen perusteella**.</span><span class="sxs-lookup"><span data-stu-id="a61a9-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="a61a9-134">Jos asiakas esimerkiksi ostaa nimikkeen ja valitsee toimitustyypiksi "lähetys", nimike voidaan lähettää mistä tahansa täyttämisryhmän varastosta, jossa on käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="a61a9-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="a61a9-135">Tuotetietosivulla näkyy lähetyssanoma "Varastossa", jos täyttämisryhmän käytettävissä olevalla lähetysvarastolla on varastoa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="a61a9-136">**Usean varaston varastotaso** -asetus on käytettävissä Commerce-versiosta 10.0.19 lähtien.</span><span class="sxs-lookup"><span data-stu-id="a61a9-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="a61a9-137">Jos päivität vanhemmasta Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a61a9-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a61a9-138">Ohjeita on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="a61a9-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="a61a9-139">**Varastoalueet** – Tämä asetus määrittää, mitkä varastoalueet, joille sanoma näytetään sivustomoduuleissa.</span><span class="sxs-lookup"><span data-stu-id="a61a9-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="a61a9-140">Sitä voi käyttää vain, jos **Käytettävissä oleva kokonaisarvo** tai **Käytettävissä oleva fyysinen** arvo on valittu **Varastotaso perusteella** -asetukselle.</span><span class="sxs-lookup"><span data-stu-id="a61a9-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="a61a9-141">Käytettävissä olevat arvot ovat **Kaikki**, **Alhaiset ja loppunut varastosta** ja **Loppunut varastosta**.</span><span class="sxs-lookup"><span data-stu-id="a61a9-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="a61a9-142">Kun **Kaikki** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta varastossa ("käytettävissä" oleva sanoma) kohteeseen loppunut varastosta ("loppunut varastosta").</span><span class="sxs-lookup"><span data-stu-id="a61a9-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="a61a9-143">Kun **Vähissä ja loppunut varastosta** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta paitsi varastossa ("käytettävissä" oleva sanoma).</span><span class="sxs-lookup"><span data-stu-id="a61a9-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="a61a9-144">Kun **Loppunut varastosta** on valittu, vain "loppunut varastosta" -sanoma tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="a61a9-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="a61a9-145">**Loppunut varastosta** – Tämä vanha numeerinen asetus tulee voimaan vain, jos **Loppunut varastosta** arvoksi on valittu **Varaston vähimmäisarvo** -asetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a61a9-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a61a9-146">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="a61a9-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="a61a9-147">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a61a9-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a61a9-148">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="a61a9-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="a61a9-149">Varastoasetuksia käyttävät moduulit</span><span class="sxs-lookup"><span data-stu-id="a61a9-149">Modules that use inventory settings</span></span>

<span data-ttu-id="a61a9-150">Ostolaatikko, toivelista, myymälänvalitsin, ostoskori ja ostoskorin kuvakemoduulit käyttävät varastoasetuksia näyttämään varastoalueet ja sanomat.</span><span class="sxs-lookup"><span data-stu-id="a61a9-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="a61a9-151">Seuraavan kuvan esimerkissä PDP näyttää Varastossa (Käytettävissä) -sanoman.</span><span class="sxs-lookup"><span data-stu-id="a61a9-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![Esimerkki PDP-moduulista, jossa on varastossa oleva sanoma](./media/pdp-InStock.png)

<span data-ttu-id="a61a9-153">Seuraavan kuvan esimerkissä PDP näyttää Loppunut varastosta (Käytettävissä) -sanoman.</span><span class="sxs-lookup"><span data-stu-id="a61a9-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![Esimerkki PDP-moduulista, jossa on loppunut varastosta -sanoma](./media/pdp-outofstock.png)

<span data-ttu-id="a61a9-155">Seuraavan kuvan esimerkissä ostoskori näyttää Varastossa (Käytettävissä) -sanoman.</span><span class="sxs-lookup"><span data-stu-id="a61a9-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Esimerkki ostoskorimoduulista, jossa on varastossa oleva sanoma](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="a61a9-157">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a61a9-157">Additional resources</span></span>

[<span data-ttu-id="a61a9-158">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a61a9-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a61a9-159">Varastopuskureiden ja varastotasojen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="a61a9-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="a61a9-160">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="a61a9-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a61a9-161">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="a61a9-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a61a9-162">Tilin hallintasivut ja -moduulit</span><span class="sxs-lookup"><span data-stu-id="a61a9-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="a61a9-163">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="a61a9-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="a61a9-164">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="a61a9-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
