---
title: Varastoasetusten käyttäminen
description: Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7d25fd62efca52dd2d60ed3435104c3507a1d19
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817606"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="c3f37-103">Varastoasetusten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c3f37-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3f37-104">Tässä ohjeaiheessa käsitellään varastoasetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c3f37-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="c3f37-105">Overview</span></span>

<span data-ttu-id="c3f37-106">Varastoasetukset määrittävät, tuleeko varasto tarkistaa, ennen kuin tuotteet lisätään kärryyn.</span><span class="sxs-lookup"><span data-stu-id="c3f37-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="c3f37-107">Ne määrittävät myös varastoon liittyvät myynninedistämispalkkiosanomat, kuten "varastossa" ja "vain muutama jäljellä".</span><span class="sxs-lookup"><span data-stu-id="c3f37-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="c3f37-108">Nämä asetukset varmistavat, että tuotetta ei voi ostaa, jos sitä ei ole varastossa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="c3f37-109">Dynamics 365 Commerce sisältää arviot tuotteiden käytettävissä olevasta saatavuudesta.</span><span class="sxs-lookup"><span data-stu-id="c3f37-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="c3f37-110">Lisätietoja arvioidun käytettävissä olevan käytettävyyden laskemisesta on kohdassa [Jälleenmyyntikanavien varaston käytettävyyden laskeminen](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="c3f37-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="c3f37-111">Commercen sivustotyökalussa voidaan määrittää tuotteen tai luokan varastorajat ja -alueet.</span><span class="sxs-lookup"><span data-stu-id="c3f37-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="c3f37-112">Ne määräävät, voidaanko varaston arvoksi luokitella varastossa, vähissä vai loppunut.</span><span class="sxs-lookup"><span data-stu-id="c3f37-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="c3f37-113">Katso lisätietoja kohdasta [Varastopuskureiden ja varastotasojen konfiguroiminen](inventory-buffers-levels.md)</span><span class="sxs-lookup"><span data-stu-id="c3f37-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c3f37-114">Varaston raja-arvojen ja alueiden tuki on käytettävissä Dynamics 365 Commercen versiossa 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="c3f37-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="c3f37-115">Varastoasetukset</span><span class="sxs-lookup"><span data-stu-id="c3f37-115">Inventory settings</span></span>

<span data-ttu-id="c3f37-116">Commercessa varastoasetukset määritetään sivustotyökalussa kohdassa **Sivuston asetukset \> Laajennukset \> Varaston hallinta**.</span><span class="sxs-lookup"><span data-stu-id="c3f37-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="c3f37-117">Varastoasetuksia on neljä, joista yksi on poistettu käytöstä (vanhentunut):</span><span class="sxs-lookup"><span data-stu-id="c3f37-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="c3f37-118">**Ota käyttöön varastotarkistus sovelluksessa** – Tämä asetus ottaa tuotevaraston tarkistuksen pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c3f37-118">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="c3f37-119">Osta-ruutu, ostoskori ja nouto myymälästä -moduulit tarkistavat tuotevaraston ja sallivat tuotteen lisäämisen ostoskoriin vain, jos varasto on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="c3f37-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="c3f37-120">**Varastotaso perustuu** – Tämä asetus määrittää, miten varastotasot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="c3f37-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="c3f37-121">Käytettävissä olevat arvot ovat **Käytettävissä olevat yhteensä**, **Fyysisesti käytettävissä olevat** ja **Loppu varastosta**.</span><span class="sxs-lookup"><span data-stu-id="c3f37-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="c3f37-122">Commercessa varaston kynnysarvo ja alueet voidaan määritellä jokaiselle tuotteelle ja luokalle.</span><span class="sxs-lookup"><span data-stu-id="c3f37-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="c3f37-123">Varasto-APIt palauttavat tuotevarastotiedot sekä **käytettävissä olevan kokonaismäärän** että **fyysisen käytettävissä olevan** ominaisuuden osalta.</span><span class="sxs-lookup"><span data-stu-id="c3f37-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="c3f37-124">Jälleenmyyjä päättää, käytetäänkö **Käytettävissä olevaa** tai **Fyysisesti käytettävissä olevaa** arvoa varaston inventoinnin ja varasto- ja loppuvarastotilojen vastaavien alueiden määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="c3f37-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="c3f37-125">**Loppunut varastosta** -arvo **Varastotason varaston kynnys arvo** asetuksen perusteella on vanha (aiempi), vanhentunut arvo.</span><span class="sxs-lookup"><span data-stu-id="c3f37-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="c3f37-126">Kun se on valittu, varaston inventoinnit määräytyvät **Käytettävissä olevan** kokonaisarvon perusteella, mutta kynnys määritetään myöhemmin annetun luvun **Loppu varastosta** -arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="c3f37-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="c3f37-127">Tämä raja-asetus koskee kaikkia tuotteita, jotka ovat verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-127">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="c3f37-128">Jos varasto on raja-arvon alapuolella, tuotetta ei pidetä varastossa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="c3f37-129">Muussa tapauksessa sitä pidetään varastossa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="c3f37-130">**Loppu varastosta** -arvo on rajallinen, emmekä suosittele sen käyttämistä versiossa 10.0.12 ja sitä uudemmissa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="c3f37-131">**Varastoalueet** – Tämä asetus määrittää, mitkä varastoalueet, joille sanoma näytetään sivustomoduuleissa.</span><span class="sxs-lookup"><span data-stu-id="c3f37-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="c3f37-132">Sitä voi käyttää vain, jos **Käytettävissä oleva kokonaisarvo** tai **Käytettävissä oleva fyysinen** arvo on valittu **Varastotaso perusteella** -asetukselle.</span><span class="sxs-lookup"><span data-stu-id="c3f37-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="c3f37-133">Käytettävissä olevat arvot ovat **Kaikki**, **Alhaiset ja loppunut varastosta** ja **Loppunut varastosta**.</span><span class="sxs-lookup"><span data-stu-id="c3f37-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="c3f37-134">Kun **Kaikki** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta varastossa ("käytettävissä" oleva sanoma) kohteeseen loppunut varastosta ("loppunut varastosta").</span><span class="sxs-lookup"><span data-stu-id="c3f37-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="c3f37-135">Kun **Vähissä ja loppunut varastosta** on valittu, näkyviin tulevat kaikkien varastoalueiden sanomat kohteesta paitsi varastossa ("käytettävissä" oleva sanoma).</span><span class="sxs-lookup"><span data-stu-id="c3f37-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="c3f37-136">Kun **Loppunut varastosta** on valittu, vain "loppunut varastosta" -sanoma tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="c3f37-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="c3f37-137">**Loppunut varastosta** – Tämä vanha numeerinen asetus tulee voimaan vain, jos **Loppunut varastosta** arvoksi on valittu **Varaston vähimmäisarvo** -asetuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c3f37-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="c3f37-138">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="c3f37-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="c3f37-139">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="c3f37-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="c3f37-140">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="c3f37-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="c3f37-141">Varastoasetuksia käyttävät moduulit</span><span class="sxs-lookup"><span data-stu-id="c3f37-141">Modules that use inventory settings</span></span>

<span data-ttu-id="c3f37-142">Ostolaatikko, toivelista, myymälänvalitsin, ostoskori ja ostoskorin kuvakemoduulit käyttävät varastoasetuksia näyttämään varastoalueet ja sanomat.</span><span class="sxs-lookup"><span data-stu-id="c3f37-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="c3f37-143">Seuraavassa kuvassa on esimerkki tuotetietosivusta (PDP), jossa näkyy varastossa oleva ("käytettävissä oleva") sanoma.</span><span class="sxs-lookup"><span data-stu-id="c3f37-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Esimerkki PDP-moduulista, jossa on varastossa oleva sanoma](./media/pdp-InStock.png)

<span data-ttu-id="c3f37-145">Seuraavassa kuvassa on esimerkki PDP:stä, jossa näkyy Loppunut varastosta -sanoma.</span><span class="sxs-lookup"><span data-stu-id="c3f37-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Esimerkki PDP-moduulista, jossa on loppunut varastosta -sanoma](./media/pdp-outofstock.png)

<span data-ttu-id="c3f37-147">Seuraavassa kuvassa on esimerkki ostoskorista, jossa näkyy Varastossa (Käytettävissä) -sanoma.</span><span class="sxs-lookup"><span data-stu-id="c3f37-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Esimerkki ostoskorimoduulista, jossa on varastossa oleva sanoma](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="c3f37-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c3f37-149">Additional resources</span></span>

[<span data-ttu-id="c3f37-150">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c3f37-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c3f37-151">Varastopuskureiden ja varastotasojen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="c3f37-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="c3f37-152">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="c3f37-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c3f37-153">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="c3f37-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c3f37-154">Tilin hallintasivut ja -moduulit</span><span class="sxs-lookup"><span data-stu-id="c3f37-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="c3f37-155">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="c3f37-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c3f37-156">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="c3f37-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
