---
title: Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa kuormassa ja jotka sitten konsolidoidaan automaattisesti lähetyksiksi.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 396a038dbf2f4b6835ecbb5fd8cb39a3a3608af7
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383762"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="701b9-103">Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="701b9-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="701b9-104">Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa kuormassa ja jotka sitten konsolidoidaan automaattisesti lähetyksiksi.</span><span class="sxs-lookup"><span data-stu-id="701b9-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="701b9-105">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="701b9-105">Make demo data available</span></span>

<span data-ttu-id="701b9-106">Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="701b9-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="701b9-107">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="701b9-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="701b9-108">Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="701b9-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="701b9-109">Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu.</span><span class="sxs-lookup"><span data-stu-id="701b9-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="701b9-110">Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="701b9-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="701b9-111">Myyntitilausten luonti skenaarioon</span><span class="sxs-lookup"><span data-stu-id="701b9-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="701b9-112">Aloita luomalla myyntitilauskokoelma, jota voit käyttää.</span><span class="sxs-lookup"><span data-stu-id="701b9-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="701b9-113">Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="701b9-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="701b9-114">Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="701b9-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="701b9-115">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.</span><span class="sxs-lookup"><span data-stu-id="701b9-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="701b9-116">Tilausjoukon 1 luonti</span><span class="sxs-lookup"><span data-stu-id="701b9-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="701b9-117">Myyntitilaus 1-1</span><span class="sxs-lookup"><span data-stu-id="701b9-117">Sales order 1-1</span></span>

1. <span data-ttu-id="701b9-118">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="701b9-119">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="701b9-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="701b9-120">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="701b9-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="701b9-121">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-122">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-123">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-124">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="701b9-125">Myyntitilaus 1-2</span><span class="sxs-lookup"><span data-stu-id="701b9-125">Sales order 1-2</span></span>

1. <span data-ttu-id="701b9-126">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="701b9-127">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="701b9-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="701b9-128">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="701b9-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="701b9-129">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-130">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-131">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-132">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="701b9-133">Myyntitilaus 1-3</span><span class="sxs-lookup"><span data-stu-id="701b9-133">Sales order 1-3</span></span>

1. <span data-ttu-id="701b9-134">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="701b9-135">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="701b9-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="701b9-136">**Toimitustapa:** *10*</span><span class="sxs-lookup"><span data-stu-id="701b9-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="701b9-137">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-138">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-139">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-140">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="701b9-141">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-142">**Nimiketunnus:** *A0002* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-143">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="701b9-144">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="701b9-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="701b9-145">Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="701b9-146">Tilausjoukon 2 luonti</span><span class="sxs-lookup"><span data-stu-id="701b9-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="701b9-147">Myyntitilaukset 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="701b9-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="701b9-148">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-149">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="701b9-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="701b9-150">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-151">**Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)</span><span class="sxs-lookup"><span data-stu-id="701b9-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="701b9-152">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-153">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="701b9-154">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-155">**Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)</span><span class="sxs-lookup"><span data-stu-id="701b9-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="701b9-156">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="701b9-157">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="701b9-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="701b9-158">Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="701b9-159">Tilausjoukon 3 luonti</span><span class="sxs-lookup"><span data-stu-id="701b9-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="701b9-160">Myyntitilaukset 3-1 ja 3-2</span><span class="sxs-lookup"><span data-stu-id="701b9-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="701b9-161">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-162">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="701b9-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="701b9-163">**Asiakkaan ehdotus:** *1*</span><span class="sxs-lookup"><span data-stu-id="701b9-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="701b9-164">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-165">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-166">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-167">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="701b9-168">Myyntitilaukset 3-3 ja 3-4</span><span class="sxs-lookup"><span data-stu-id="701b9-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="701b9-169">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-170">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="701b9-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="701b9-171">**Asiakkaan ehdotus:** *2*</span><span class="sxs-lookup"><span data-stu-id="701b9-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="701b9-172">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-173">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-174">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-175">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="701b9-176">Tilausjoukon 4 luonti</span><span class="sxs-lookup"><span data-stu-id="701b9-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="701b9-177">Myyntitilaukset 4-1 ja 4-2</span><span class="sxs-lookup"><span data-stu-id="701b9-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="701b9-178">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-179">**Asiakastili:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="701b9-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="701b9-180">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-181">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-182">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-183">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="701b9-184">Myyntitilaukset 4-3 ja 4-4</span><span class="sxs-lookup"><span data-stu-id="701b9-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="701b9-185">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-186">**Asiakastili:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="701b9-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="701b9-187">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-188">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-189">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-190">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="701b9-191">Myyntitilaukset 4-5 ja 4-6</span><span class="sxs-lookup"><span data-stu-id="701b9-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="701b9-192">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-193">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="701b9-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="701b9-194">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="701b9-194">**Site:** *6*</span></span>
    - <span data-ttu-id="701b9-195">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="701b9-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="701b9-196">**Pooli:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="701b9-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="701b9-197">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-198">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-199">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-200">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="701b9-201">Myyntitilaukset 4-7 ja 4-8</span><span class="sxs-lookup"><span data-stu-id="701b9-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="701b9-202">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="701b9-203">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="701b9-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="701b9-204">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="701b9-204">**Site:** *6*</span></span>
    - <span data-ttu-id="701b9-205">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="701b9-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="701b9-206">**Pooli:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="701b9-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="701b9-207">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="701b9-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="701b9-208">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="701b9-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="701b9-209">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="701b9-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="701b9-210">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="701b9-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="701b9-211">Kuormien luonti ja niiden vapauttaminen varastoon kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="701b9-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="701b9-212">Luo jokaiselle tähän skenaarioon luodulle tilausjoukolle kuorma ja vapauta se sitten varaston näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="701b9-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="701b9-213">Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="701b9-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="701b9-214">Etsi ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit yhdestä tätä skenaariota varten luodusta tilausjoukosta.</span><span class="sxs-lookup"><span data-stu-id="701b9-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="701b9-215">Lisää valitut tilausrivit uuteen kuormaan valitsemalla toimintoruudun **Tarjonta ja kysyntä** -välilehdessä **Lisää \> Uuteen kuormaan**.</span><span class="sxs-lookup"><span data-stu-id="701b9-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="701b9-216">Valitse **Lataa mallin määritys** -valintaikkunan **Kuorman mallitunnus** -kentässä kuormamalli, kuten *Vakiokuormamalli*.</span><span class="sxs-lookup"><span data-stu-id="701b9-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="701b9-217">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="701b9-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="701b9-218">Etsi ja valitse juuri luotu kuorma **Kuormat**-osassa.</span><span class="sxs-lookup"><span data-stu-id="701b9-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="701b9-219">Vapauta valittu kuorma varastoon valitsemalla **Vapautus \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="701b9-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="701b9-220">Toista tämä menettely kolmen muun tähän skenaarioon luodun tilausjoukon osalta.</span><span class="sxs-lookup"><span data-stu-id="701b9-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="701b9-221">Lähetysten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="701b9-221">Verify the shipments</span></span>

<span data-ttu-id="701b9-222">Seuraavan menettelyn avulla voi tarkistaa lähetykset, jotka on luotu tai päivitetty lähetyksen konsolidoinnin tuloksena.</span><span class="sxs-lookup"><span data-stu-id="701b9-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="701b9-223">Sen avulla voi tarkistaa kunkin skenaarioon luodun tilausjoukon sekä seuraavat osiot. Tällä tavoin voidaan varmistaa, että tulokset ovat odotetunkaltaiset.</span><span class="sxs-lookup"><span data-stu-id="701b9-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="701b9-224">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="701b9-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="701b9-225">Etsi ja valitse tarvittava lähetys.</span><span class="sxs-lookup"><span data-stu-id="701b9-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="701b9-226">Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="701b9-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="701b9-227">Tilausjoukon 1 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="701b9-227">Release order set 1 in one load</span></span>

<span data-ttu-id="701b9-228">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="701b9-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="701b9-229">Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="701b9-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="701b9-230">Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.</span><span class="sxs-lookup"><span data-stu-id="701b9-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="701b9-231">Tilausjoukon 2 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="701b9-231">Release order set 2 in one load</span></span>

<span data-ttu-id="701b9-232">Luotuja lähetyksiä on oltava kolme:</span><span class="sxs-lookup"><span data-stu-id="701b9-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="701b9-233">Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="701b9-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="701b9-234">Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.</span><span class="sxs-lookup"><span data-stu-id="701b9-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="701b9-235">Tilausjoukon 3 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="701b9-235">Release order set 3 in one load</span></span>

<span data-ttu-id="701b9-236">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="701b9-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="701b9-237">Ensimmäisessä lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *1*.</span><span class="sxs-lookup"><span data-stu-id="701b9-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="701b9-238">Toisessa lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *2*.</span><span class="sxs-lookup"><span data-stu-id="701b9-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="701b9-239">Tilausjoukon 4 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="701b9-239">Release order set 4 in one load</span></span>

<span data-ttu-id="701b9-240">Luotuja lähetyksiä on oltava neljä:</span><span class="sxs-lookup"><span data-stu-id="701b9-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="701b9-241">Asiakastilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="701b9-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="701b9-242">Asiakastilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="701b9-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="701b9-243">Asiakastilin *US-007* myyntitilausten 4–5 ja 4–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="701b9-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="701b9-244">Asiakastilin *US-007* myyntitilausten 4–7 ja 4–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilaustenvälinen*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="701b9-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="701b9-245">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="701b9-245">Additional resources</span></span>

- [<span data-ttu-id="701b9-246">Lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="701b9-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="701b9-247">Lähetyksen konsolidointikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="701b9-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)