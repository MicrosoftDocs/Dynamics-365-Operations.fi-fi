---
title: Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka sitten konsolidoidaan lähetyksiksi lähetysten konsolidoinnin työtilassa.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9b7dc72d789fd331c3636c406ac6a45566ba81ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242178"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="e2e89-103">Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa</span><span class="sxs-lookup"><span data-stu-id="e2e89-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2e89-104">Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka sitten konsolidoidaan lähetyksiksi lähetysten konsolidoinnin työtilassa.</span><span class="sxs-lookup"><span data-stu-id="e2e89-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="e2e89-105">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e2e89-105">Make demo data available</span></span>

<span data-ttu-id="e2e89-106">Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="e2e89-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e2e89-107">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="e2e89-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="e2e89-108">Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e2e89-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="e2e89-109">Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu.</span><span class="sxs-lookup"><span data-stu-id="e2e89-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="e2e89-110">Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="e2e89-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="e2e89-111">Manuaalisen lähetyksen konsolidointitoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="e2e89-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="e2e89-112">*Lähetyksen manuaalinen konsolidointi* -toiminto on otettava järjestelmässä käyttöön, ennen kuin sitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="e2e89-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="e2e89-113">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="e2e89-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e2e89-114">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="e2e89-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e2e89-115">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="e2e89-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e2e89-116">**Toiminnon nimi:** *Manuaalinen lähetyksen konsolidointi*</span><span class="sxs-lookup"><span data-stu-id="e2e89-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="e2e89-117">Kuten ohjeaiheessa [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) mainittiin, myös *Konsolidoi lähetys* -toiminto on otettava käyttöön ennen käytäntöjen luontia.</span><span class="sxs-lookup"><span data-stu-id="e2e89-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="e2e89-118">Tämä vaihe pitäisi kuitenkin olla jo tehtynä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="e2e89-119">Myyntitilausten luonti skenaarioon</span><span class="sxs-lookup"><span data-stu-id="e2e89-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="e2e89-120">Aloita luomalla myyntitilauskokoelma, jota voit käyttää.</span><span class="sxs-lookup"><span data-stu-id="e2e89-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="e2e89-121">Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e2e89-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="e2e89-122">Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="e2e89-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="e2e89-123">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.</span><span class="sxs-lookup"><span data-stu-id="e2e89-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="e2e89-124">Tilausjoukon 1 luonti</span><span class="sxs-lookup"><span data-stu-id="e2e89-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="e2e89-125">Myyntitilaukset 1-1 ja 1-2</span><span class="sxs-lookup"><span data-stu-id="e2e89-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="e2e89-126">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-127">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e2e89-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e2e89-128">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="e2e89-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e2e89-129">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-130">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-131">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-132">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="e2e89-133">Myyntitilaus 1-3</span><span class="sxs-lookup"><span data-stu-id="e2e89-133">Sales order 1-3</span></span>

1. <span data-ttu-id="e2e89-134">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-135">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e2e89-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e2e89-136">**Toimitustapa:** *10*</span><span class="sxs-lookup"><span data-stu-id="e2e89-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="e2e89-137">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-138">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-139">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-140">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="e2e89-141">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-142">**Nimiketunnus:** *A0002* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-143">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="e2e89-144">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="e2e89-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e2e89-145">Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="e2e89-146">Tilausjoukon 2 luonti</span><span class="sxs-lookup"><span data-stu-id="e2e89-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="e2e89-147">Myyntitilaukset 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="e2e89-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="e2e89-148">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-149">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="e2e89-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="e2e89-150">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="e2e89-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e2e89-151">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-152">**Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)</span><span class="sxs-lookup"><span data-stu-id="e2e89-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="e2e89-153">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-154">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="e2e89-155">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-156">**Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)</span><span class="sxs-lookup"><span data-stu-id="e2e89-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="e2e89-157">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="e2e89-158">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="e2e89-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="e2e89-159">Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="e2e89-160">Tilausjoukon 3 luonti</span><span class="sxs-lookup"><span data-stu-id="e2e89-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="e2e89-161">Myyntitilaukset 3-1 ja 3-2</span><span class="sxs-lookup"><span data-stu-id="e2e89-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="e2e89-162">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-163">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e2e89-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e2e89-164">**Asiakkaan ehdotus:** *1*</span><span class="sxs-lookup"><span data-stu-id="e2e89-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="e2e89-165">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-166">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-167">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-168">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="e2e89-169">Myyntitilaukset 3-3 ja 3-4</span><span class="sxs-lookup"><span data-stu-id="e2e89-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="e2e89-170">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-171">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e2e89-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e2e89-172">**Asiakkaan ehdotus:** *2*</span><span class="sxs-lookup"><span data-stu-id="e2e89-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="e2e89-173">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-174">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-175">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-176">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="e2e89-177">Tilausjoukon 4 luonti</span><span class="sxs-lookup"><span data-stu-id="e2e89-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="e2e89-178">Myyntitilaukset 4-1 ja 4-2</span><span class="sxs-lookup"><span data-stu-id="e2e89-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="e2e89-179">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-180">**Asiakastili:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="e2e89-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="e2e89-181">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-182">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-183">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-184">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="e2e89-185">Myyntitilaukset 4-3 ja 4-4</span><span class="sxs-lookup"><span data-stu-id="e2e89-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="e2e89-186">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-187">**Asiakastili:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="e2e89-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="e2e89-188">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-189">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-190">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-191">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="e2e89-192">Myyntitilaukset 4-5 ja 4-6</span><span class="sxs-lookup"><span data-stu-id="e2e89-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="e2e89-193">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-194">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e2e89-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e2e89-195">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="e2e89-195">**Site:** *6*</span></span>
    - <span data-ttu-id="e2e89-196">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="e2e89-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e2e89-197">**Pooli:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="e2e89-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="e2e89-198">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-199">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-200">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-201">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="e2e89-202">Myyntitilaukset 4-7 ja 4-8</span><span class="sxs-lookup"><span data-stu-id="e2e89-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="e2e89-203">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e2e89-204">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e2e89-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e2e89-205">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="e2e89-205">**Site:** *6*</span></span>
    - <span data-ttu-id="e2e89-206">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="e2e89-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="e2e89-207">**Pooli:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="e2e89-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="e2e89-208">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e2e89-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e89-209">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="e2e89-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e2e89-210">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e2e89-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e2e89-211">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="e2e89-212">Tilausten vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="e2e89-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="e2e89-213">Vapauta jokainen tähän skenaarioon luotu myyntitilaus varastoon seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="e2e89-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="e2e89-214">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e2e89-215">Etsi ja valitse vapautettava myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e2e89-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="e2e89-216">Vapauta valittu myyntitilaus valitsemalla toimintoruudun **Varasto**-välilehdessä **Toiminnot \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="e2e89-217">Toista tämä menettely jokaisen tähän skenaarioon luodun myyntitilauksen osalta.</span><span class="sxs-lookup"><span data-stu-id="e2e89-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="e2e89-218">Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa</span><span class="sxs-lookup"><span data-stu-id="e2e89-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="e2e89-219">Valitse **Varastonhallinta \> Vapauta varastoon \> Lähetyksen konsolidoinnin työtila**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="e2e89-220">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e2e89-221">Lisää kyselyeditoriin valintaikkunassa seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Alue**-välilehdessä **Lisää**:</span><span class="sxs-lookup"><span data-stu-id="e2e89-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="e2e89-222">**Taulu:** *Myyntitilaukset*</span><span class="sxs-lookup"><span data-stu-id="e2e89-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="e2e89-223">**Kenttä:** *Myyntitilaus*</span><span class="sxs-lookup"><span data-stu-id="e2e89-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="e2e89-224">**Ehdot:** anna kunkin tähän skenaarion luodun tilausjoukon pilkuin eroteltu myyntitilausnumeroiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="e2e89-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="e2e89-225">Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="e2e89-226">Valitse toimintoruudussa **Konsolidoi lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="e2e89-227">Valitse ensin kaikki lähetykset ja sitten toimintoruudussa **Konsolidoi**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="e2e89-228">Lähetysten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e2e89-228">Verify the shipments</span></span>

<span data-ttu-id="e2e89-229">Seuraavan menettelyn avulla voi tarkistaa lähetykset, jotka on luotu tai päivitetty lähetyksen konsolidoinnin tuloksena.</span><span class="sxs-lookup"><span data-stu-id="e2e89-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="e2e89-230">Sen avulla voi tarkistaa kunkin skenaarioon luodun tilausjoukon sekä seuraavat osiot. Tällä tavoin voidaan varmistaa, että tulokset ovat odotetunkaltaiset.</span><span class="sxs-lookup"><span data-stu-id="e2e89-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="e2e89-231">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="e2e89-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="e2e89-232">Etsi ja valitse tarvittava lähetys.</span><span class="sxs-lookup"><span data-stu-id="e2e89-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="e2e89-233">Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="e2e89-234">Tilausjoukkoon 1 liittyvät lähetykset</span><span class="sxs-lookup"><span data-stu-id="e2e89-234">Related shipments for order set 1</span></span>

<span data-ttu-id="e2e89-235">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="e2e89-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="e2e89-236">Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="e2e89-237">Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.</span><span class="sxs-lookup"><span data-stu-id="e2e89-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="e2e89-238">Tilausjoukkoon 2 liittyvät lähetykset</span><span class="sxs-lookup"><span data-stu-id="e2e89-238">Related shipments for order set 2</span></span>

<span data-ttu-id="e2e89-239">Luotuja lähetyksiä on oltava kolme:</span><span class="sxs-lookup"><span data-stu-id="e2e89-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="e2e89-240">Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="e2e89-241">Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.</span><span class="sxs-lookup"><span data-stu-id="e2e89-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="e2e89-242">Tilausjoukkoon 3 liittyvät lähetykset</span><span class="sxs-lookup"><span data-stu-id="e2e89-242">Related shipments for order set 3</span></span>

<span data-ttu-id="e2e89-243">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="e2e89-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="e2e89-244">Ensimmäisessä lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *1*.</span><span class="sxs-lookup"><span data-stu-id="e2e89-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="e2e89-245">Toisessa lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *2*.</span><span class="sxs-lookup"><span data-stu-id="e2e89-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="e2e89-246">Tilausjoukkoon 4 liittyvät lähetykset</span><span class="sxs-lookup"><span data-stu-id="e2e89-246">Related shipments for order set 4</span></span>

<span data-ttu-id="e2e89-247">Luotuja lähetyksiä on oltava neljä:</span><span class="sxs-lookup"><span data-stu-id="e2e89-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="e2e89-248">Tilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e2e89-249">Tilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e2e89-250">Tilin *US-007* myyntitilausten 4–5 ja 4–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="e2e89-251">Tilin *US-007* myyntitilausten 4–7 ja 4–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *CrossOrder*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="e2e89-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2e89-252">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e2e89-252">Additional resources</span></span>

- [<span data-ttu-id="e2e89-253">Lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="e2e89-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="e2e89-254">Lähetyksen konsolidointikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e2e89-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]