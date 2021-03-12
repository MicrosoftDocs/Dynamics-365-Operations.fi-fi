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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c0af6764742532cbe181c8a20e7bf783b0e6d7cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983088"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="5eca8-103">Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="5eca8-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eca8-104">Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa kuormassa ja jotka sitten konsolidoidaan automaattisesti lähetyksiksi.</span><span class="sxs-lookup"><span data-stu-id="5eca8-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="5eca8-105">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="5eca8-105">Make demo data available</span></span>

<span data-ttu-id="5eca8-106">Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="5eca8-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5eca8-107">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="5eca8-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="5eca8-108">Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5eca8-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="5eca8-109">Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu.</span><span class="sxs-lookup"><span data-stu-id="5eca8-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="5eca8-110">Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="5eca8-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="5eca8-111">Myyntitilausten luonti skenaarioon</span><span class="sxs-lookup"><span data-stu-id="5eca8-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="5eca8-112">Aloita luomalla myyntitilauskokoelma, jota voit käyttää.</span><span class="sxs-lookup"><span data-stu-id="5eca8-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="5eca8-113">Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5eca8-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="5eca8-114">Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="5eca8-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="5eca8-115">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.</span><span class="sxs-lookup"><span data-stu-id="5eca8-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="5eca8-116">Tilausjoukon 1 luonti</span><span class="sxs-lookup"><span data-stu-id="5eca8-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="5eca8-117">Myyntitilaus 1-1</span><span class="sxs-lookup"><span data-stu-id="5eca8-117">Sales order 1-1</span></span>

1. <span data-ttu-id="5eca8-118">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-119">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5eca8-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5eca8-120">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="5eca8-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="5eca8-121">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-122">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-123">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-124">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="5eca8-125">Myyntitilaus 1-2</span><span class="sxs-lookup"><span data-stu-id="5eca8-125">Sales order 1-2</span></span>

1. <span data-ttu-id="5eca8-126">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-127">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5eca8-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5eca8-128">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="5eca8-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="5eca8-129">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-130">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-131">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-132">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="5eca8-133">Myyntitilaus 1-3</span><span class="sxs-lookup"><span data-stu-id="5eca8-133">Sales order 1-3</span></span>

1. <span data-ttu-id="5eca8-134">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-135">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5eca8-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5eca8-136">**Toimitustapa:** *10*</span><span class="sxs-lookup"><span data-stu-id="5eca8-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="5eca8-137">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-138">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-139">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-140">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="5eca8-141">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-142">**Nimiketunnus:** *A0002* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-143">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="5eca8-144">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="5eca8-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="5eca8-145">Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="5eca8-146">Tilausjoukon 2 luonti</span><span class="sxs-lookup"><span data-stu-id="5eca8-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="5eca8-147">Myyntitilaukset 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="5eca8-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="5eca8-148">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-149">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="5eca8-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="5eca8-150">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-151">**Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)</span><span class="sxs-lookup"><span data-stu-id="5eca8-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="5eca8-152">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-153">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="5eca8-154">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-155">**Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)</span><span class="sxs-lookup"><span data-stu-id="5eca8-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="5eca8-156">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="5eca8-157">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="5eca8-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="5eca8-158">Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="5eca8-159">Tilausjoukon 3 luonti</span><span class="sxs-lookup"><span data-stu-id="5eca8-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="5eca8-160">Myyntitilaukset 3-1 ja 3-2</span><span class="sxs-lookup"><span data-stu-id="5eca8-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="5eca8-161">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-162">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5eca8-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5eca8-163">**Asiakkaan ehdotus:** *1*</span><span class="sxs-lookup"><span data-stu-id="5eca8-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="5eca8-164">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-165">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-166">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-167">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="5eca8-168">Myyntitilaukset 3-3 ja 3-4</span><span class="sxs-lookup"><span data-stu-id="5eca8-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="5eca8-169">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-170">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5eca8-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5eca8-171">**Asiakkaan ehdotus:** *2*</span><span class="sxs-lookup"><span data-stu-id="5eca8-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="5eca8-172">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-173">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-174">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-175">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="5eca8-176">Tilausjoukon 4 luonti</span><span class="sxs-lookup"><span data-stu-id="5eca8-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="5eca8-177">Myyntitilaukset 4-1 ja 4-2</span><span class="sxs-lookup"><span data-stu-id="5eca8-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="5eca8-178">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-179">**Asiakastili:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="5eca8-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="5eca8-180">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-181">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-182">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-183">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="5eca8-184">Myyntitilaukset 4-3 ja 4-4</span><span class="sxs-lookup"><span data-stu-id="5eca8-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="5eca8-185">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-186">**Asiakastili:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="5eca8-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="5eca8-187">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-188">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-189">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-190">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="5eca8-191">Myyntitilaukset 4-5 ja 4-6</span><span class="sxs-lookup"><span data-stu-id="5eca8-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="5eca8-192">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-193">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="5eca8-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="5eca8-194">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="5eca8-194">**Site:** *6*</span></span>
    - <span data-ttu-id="5eca8-195">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="5eca8-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="5eca8-196">**Pooli:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="5eca8-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="5eca8-197">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-198">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-199">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-200">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="5eca8-201">Myyntitilaukset 4-7 ja 4-8</span><span class="sxs-lookup"><span data-stu-id="5eca8-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="5eca8-202">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5eca8-203">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="5eca8-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="5eca8-204">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="5eca8-204">**Site:** *6*</span></span>
    - <span data-ttu-id="5eca8-205">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="5eca8-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="5eca8-206">**Pooli:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="5eca8-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="5eca8-207">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="5eca8-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5eca8-208">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="5eca8-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5eca8-209">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5eca8-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5eca8-210">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="5eca8-211">Kuormien luonti ja niiden vapauttaminen varastoon kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="5eca8-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="5eca8-212">Luo jokaiselle tähän skenaarioon luodulle tilausjoukolle kuorma ja vapauta se sitten varaston näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="5eca8-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="5eca8-213">Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="5eca8-214">Etsi ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit yhdestä tätä skenaariota varten luodusta tilausjoukosta.</span><span class="sxs-lookup"><span data-stu-id="5eca8-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="5eca8-215">Lisää valitut tilausrivit uuteen kuormaan valitsemalla toimintoruudun **Tarjonta ja kysyntä** -välilehdessä **Lisää \> Uuteen kuormaan**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="5eca8-216">Valitse **Lataa mallin määritys** -valintaikkunan **Kuorman mallitunnus** -kentässä kuormamalli, kuten *Vakiokuormamalli*.</span><span class="sxs-lookup"><span data-stu-id="5eca8-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="5eca8-217">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="5eca8-218">Etsi ja valitse juuri luotu kuorma **Kuormat**-osassa.</span><span class="sxs-lookup"><span data-stu-id="5eca8-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="5eca8-219">Vapauta valittu kuorma varastoon valitsemalla **Vapautus \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="5eca8-220">Toista tämä menettely kolmen muun tähän skenaarioon luodun tilausjoukon osalta.</span><span class="sxs-lookup"><span data-stu-id="5eca8-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="5eca8-221">Lähetysten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="5eca8-221">Verify the shipments</span></span>

<span data-ttu-id="5eca8-222">Seuraavan menettelyn avulla voi tarkistaa lähetykset, jotka on luotu tai päivitetty lähetyksen konsolidoinnin tuloksena.</span><span class="sxs-lookup"><span data-stu-id="5eca8-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="5eca8-223">Sen avulla voi tarkistaa kunkin skenaarioon luodun tilausjoukon sekä seuraavat osiot. Tällä tavoin voidaan varmistaa, että tulokset ovat odotetunkaltaiset.</span><span class="sxs-lookup"><span data-stu-id="5eca8-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="5eca8-224">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="5eca8-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="5eca8-225">Etsi ja valitse tarvittava lähetys.</span><span class="sxs-lookup"><span data-stu-id="5eca8-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="5eca8-226">Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="5eca8-227">Tilausjoukon 1 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="5eca8-227">Release order set 1 in one load</span></span>

<span data-ttu-id="5eca8-228">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="5eca8-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="5eca8-229">Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="5eca8-230">Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.</span><span class="sxs-lookup"><span data-stu-id="5eca8-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="5eca8-231">Tilausjoukon 2 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="5eca8-231">Release order set 2 in one load</span></span>

<span data-ttu-id="5eca8-232">Luotuja lähetyksiä on oltava kolme:</span><span class="sxs-lookup"><span data-stu-id="5eca8-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="5eca8-233">Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="5eca8-234">Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.</span><span class="sxs-lookup"><span data-stu-id="5eca8-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="5eca8-235">Tilausjoukon 3 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="5eca8-235">Release order set 3 in one load</span></span>

<span data-ttu-id="5eca8-236">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="5eca8-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="5eca8-237">Ensimmäisessä lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *1*.</span><span class="sxs-lookup"><span data-stu-id="5eca8-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="5eca8-238">Toisessa lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *2*.</span><span class="sxs-lookup"><span data-stu-id="5eca8-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="5eca8-239">Tilausjoukon 4 vapauttaminen yhdessä kuormassa</span><span class="sxs-lookup"><span data-stu-id="5eca8-239">Release order set 4 in one load</span></span>

<span data-ttu-id="5eca8-240">Luotuja lähetyksiä on oltava neljä:</span><span class="sxs-lookup"><span data-stu-id="5eca8-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="5eca8-241">Asiakastilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="5eca8-242">Asiakastilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="5eca8-243">Asiakastilin *US-007* myyntitilausten 4–5 ja 4–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="5eca8-244">Asiakastilin *US-007* myyntitilausten 4–7 ja 4–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilaustenvälinen*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="5eca8-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eca8-245">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5eca8-245">Additional resources</span></span>

- [<span data-ttu-id="5eca8-246">Lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="5eca8-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="5eca8-247">Lähetyksen konsolidointikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5eca8-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
