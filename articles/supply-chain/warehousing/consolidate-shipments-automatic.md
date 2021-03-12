---
title: Lähetysten konsolidointi, kun ne vapautetaan varastoon myyntitilausten automaattisella vapauttamisella
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa automatisoidussa varaston vapautuksen jaksottaisessa menettelyssä.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 376c7418b61c0192f9071a879b50b9ece7699894
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970353"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="8590e-103">Lähetysten konsolidointi, kun ne vapautetaan varastoon myyntitilausten automaattisella vapauttamisella</span><span class="sxs-lookup"><span data-stu-id="8590e-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8590e-104">Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa automatisoidussa varaston vapautuksen jaksottaisessa menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="8590e-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="8590e-105">Tilaukset konsolidoidaan automaattisesti lähetyksiksi lähetyksen konsolidointikäytännöiksi määritettyjen sääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="8590e-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="8590e-106">Tämän skenaarion aikana luodaan myyntitilausjoukkoja ja kukun joukko vapautetaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="8590e-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="8590e-107">Tämän jälkeen lähetyksen konsolidoinnin aikana luodut tai päivitetyt lähetykset tarkistetaan määritettyjen käytäntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="8590e-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="8590e-108">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="8590e-108">Make demo data available</span></span>

<span data-ttu-id="8590e-109">Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="8590e-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8590e-110">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="8590e-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="8590e-111">Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8590e-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="8590e-112">Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu.</span><span class="sxs-lookup"><span data-stu-id="8590e-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="8590e-113">Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="8590e-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="8590e-114">Myyntitilausten luonti skenaarioon</span><span class="sxs-lookup"><span data-stu-id="8590e-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="8590e-115">Aloita luomalla myyntitilauskokoelma, jota voit käyttää.</span><span class="sxs-lookup"><span data-stu-id="8590e-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="8590e-116">Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8590e-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="8590e-117">Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="8590e-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="8590e-118">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.</span><span class="sxs-lookup"><span data-stu-id="8590e-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="8590e-119">Tilausjoukon 1 luonti</span><span class="sxs-lookup"><span data-stu-id="8590e-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="8590e-120">Myyntitilaus 1-1</span><span class="sxs-lookup"><span data-stu-id="8590e-120">Sales order 1-1</span></span>

1. <span data-ttu-id="8590e-121">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8590e-122">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8590e-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8590e-123">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="8590e-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="8590e-124">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-125">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-126">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="8590e-127">Myyntitilaus 1-2</span><span class="sxs-lookup"><span data-stu-id="8590e-127">Sales order 1-2</span></span>

1. <span data-ttu-id="8590e-128">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8590e-129">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8590e-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8590e-130">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="8590e-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="8590e-131">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-132">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-133">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="8590e-134">Myyntitilaus 1-3</span><span class="sxs-lookup"><span data-stu-id="8590e-134">Sales order 1-3</span></span>

1. <span data-ttu-id="8590e-135">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8590e-136">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8590e-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8590e-137">**Toimitustapa:** *10*</span><span class="sxs-lookup"><span data-stu-id="8590e-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="8590e-138">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-139">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-140">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8590e-141">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-142">**Nimiketunnus:** *A0002* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-143">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="8590e-144">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="8590e-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="8590e-145">Tilausjoukon 2 luonti</span><span class="sxs-lookup"><span data-stu-id="8590e-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="8590e-146">Myyntitilaukset 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="8590e-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="8590e-147">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8590e-148">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="8590e-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="8590e-149">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-150">**Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)</span><span class="sxs-lookup"><span data-stu-id="8590e-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="8590e-151">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8590e-152">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-153">**Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)</span><span class="sxs-lookup"><span data-stu-id="8590e-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="8590e-154">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="8590e-155">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="8590e-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="8590e-156">Tilausjoukon 3 luonti</span><span class="sxs-lookup"><span data-stu-id="8590e-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="8590e-157">Myyntitilaus 3-1</span><span class="sxs-lookup"><span data-stu-id="8590e-157">Sales order 3-1</span></span>

1. <span data-ttu-id="8590e-158">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8590e-159">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="8590e-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="8590e-160">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-161">**Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)</span><span class="sxs-lookup"><span data-stu-id="8590e-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="8590e-162">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8590e-163">Lisää toinen tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-164">**Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)</span><span class="sxs-lookup"><span data-stu-id="8590e-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="8590e-165">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="8590e-166">**Toimitustapa:** *Lento-Ilma*</span><span class="sxs-lookup"><span data-stu-id="8590e-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="8590e-167">Tämä tilaus on samanlainen kuin kaksi tilausjoukkoon 2 luotua tilausta.</span><span class="sxs-lookup"><span data-stu-id="8590e-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="8590e-168">Se mainitaan kuitenkin omana tilausjoukkona, koska se julkaistaan erikseen myöhemmin tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="8590e-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="8590e-169">Tilausjoukon 4 luonti</span><span class="sxs-lookup"><span data-stu-id="8590e-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="8590e-170">Myyntitilaus 4-1</span><span class="sxs-lookup"><span data-stu-id="8590e-170">Sales order 4-1</span></span>

1. <span data-ttu-id="8590e-171">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8590e-172">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8590e-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8590e-173">**Asiakkaan ehdotus:** *1*</span><span class="sxs-lookup"><span data-stu-id="8590e-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="8590e-174">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-175">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-176">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="8590e-177">Tilausjoukon 5 luonti</span><span class="sxs-lookup"><span data-stu-id="8590e-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="8590e-178">Myyntitilaukset 5-1 ja 5-2</span><span class="sxs-lookup"><span data-stu-id="8590e-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="8590e-179">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8590e-180">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8590e-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8590e-181">**Asiakkaan ehdotus:** *2*</span><span class="sxs-lookup"><span data-stu-id="8590e-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="8590e-182">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-183">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-184">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="8590e-185">Myyntitilaus 5-3</span><span class="sxs-lookup"><span data-stu-id="8590e-185">Sales order 5-3</span></span>

1. <span data-ttu-id="8590e-186">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8590e-187">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8590e-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8590e-188">**Asiakkaan ehdotus:** *1*</span><span class="sxs-lookup"><span data-stu-id="8590e-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="8590e-189">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-190">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-191">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="8590e-192">Tilausjoukon 6 luonti</span><span class="sxs-lookup"><span data-stu-id="8590e-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="8590e-193">Myyntitilaukset 6-1 ja 6-2</span><span class="sxs-lookup"><span data-stu-id="8590e-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="8590e-194">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8590e-195">**Asiakastili:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="8590e-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="8590e-196">**Asiakkaan ehdotus:** *2*</span><span class="sxs-lookup"><span data-stu-id="8590e-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="8590e-197">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-198">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-199">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="8590e-200">Myyntitilaukset 6-3 ja 6-4</span><span class="sxs-lookup"><span data-stu-id="8590e-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="8590e-201">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8590e-202">**Asiakastili:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="8590e-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="8590e-203">**Asiakkaan ehdotus:** *1*</span><span class="sxs-lookup"><span data-stu-id="8590e-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="8590e-204">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-205">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-206">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="8590e-207">Myyntitilaukset 6-5 ja 6-6</span><span class="sxs-lookup"><span data-stu-id="8590e-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="8590e-208">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8590e-209">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8590e-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8590e-210">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="8590e-210">**Site:** *6*</span></span>
    - <span data-ttu-id="8590e-211">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="8590e-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="8590e-212">**Pooli:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="8590e-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="8590e-213">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-214">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-215">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="8590e-216">Myyntitilaukset 6-7 ja 6-8</span><span class="sxs-lookup"><span data-stu-id="8590e-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="8590e-217">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8590e-218">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8590e-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8590e-219">**Toimipaikka:** *6*</span><span class="sxs-lookup"><span data-stu-id="8590e-219">**Site:** *6*</span></span>
    - <span data-ttu-id="8590e-220">**Varasto**: *61*</span><span class="sxs-lookup"><span data-stu-id="8590e-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="8590e-221">**Pooli:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="8590e-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="8590e-222">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="8590e-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8590e-223">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="8590e-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8590e-224">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8590e-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="8590e-225">Myyntitilausten automaattinen vapautus varastoon</span><span class="sxs-lookup"><span data-stu-id="8590e-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="8590e-226">Jokaisen aiemmin luodun myyntitilausjoukon osalta suoritetaan automaattinen varastoon vapautusmenettely.</span><span class="sxs-lookup"><span data-stu-id="8590e-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="8590e-227">Kussakin tapauksessa käytetään tässä käsiteltyä [varastoon vapautuksen perusmenettelyä](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="8590e-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="8590e-228">Varastoon vapautuksen perusmenettely</span><span class="sxs-lookup"><span data-stu-id="8590e-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="8590e-229">Kunkin aiemmin luodun myyntitilausjoukon osalta suoritetaan kolme menettelyä, joita käsitellään seuraavissa aliosioissa.</span><span class="sxs-lookup"><span data-stu-id="8590e-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="8590e-230">Vapautuksen aikana käytetyn aaltomallin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="8590e-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="8590e-231">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="8590e-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="8590e-232">Määritä **Aaltomallin tyyppi** -kentän arvoksi *Lähetys*.</span><span class="sxs-lookup"><span data-stu-id="8590e-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="8590e-233">Etsi ja valitse siihen varastoon liitetty aaltomalli, jota käytit tätä skenaariota varten luoduissa tilausjoukoissa.</span><span class="sxs-lookup"><span data-stu-id="8590e-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="8590e-234">Jos esimerkiksi käytit varastoa *24*, valitse **24 Lähetysoletus** -aaltomalli.</span><span class="sxs-lookup"><span data-stu-id="8590e-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="8590e-235">Jos käytit varastoa *61*, valitse **61 Lähetys**-aaltomalli.</span><span class="sxs-lookup"><span data-stu-id="8590e-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="8590e-236">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8590e-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8590e-237">Määritä **Käsittele aalto, kun se vapautetaan varastoon** -asetuksen arvoksi *Ei*.</span><span class="sxs-lookup"><span data-stu-id="8590e-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="8590e-238">Vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="8590e-238">Release to the warehouse</span></span>

1. <span data-ttu-id="8590e-239">Valitse **Varastonhallinta \> Vapauta varastoon \> Myyntitilausten automaattinen vapautus**.</span><span class="sxs-lookup"><span data-stu-id="8590e-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="8590e-240">Määritä **Vapautettava määrä** -kentän arvoksi *Kaikki*.</span><span class="sxs-lookup"><span data-stu-id="8590e-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="8590e-241">Avaa kyselyvalintaikkuna valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.</span><span class="sxs-lookup"><span data-stu-id="8590e-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="8590e-242">Lisää seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Alue**-välilehdessä **Lisää**:</span><span class="sxs-lookup"><span data-stu-id="8590e-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="8590e-243">**Taulu:** *Myyntitilaus*</span><span class="sxs-lookup"><span data-stu-id="8590e-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="8590e-244">**Johdettu taulu:** *Myyntitilaus*</span><span class="sxs-lookup"><span data-stu-id="8590e-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="8590e-245">**Kenttä:** *Myyntitilaus*</span><span class="sxs-lookup"><span data-stu-id="8590e-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="8590e-246">**Ehdot:** anna toivotun tilausjoukon pilkuin eroteltu myyntitilausnumeroiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="8590e-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="8590e-247">Tallenna kysely valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="8590e-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="8590e-248">Käynnistä *Automaattinen vapautus varastoon* -menettely valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="8590e-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="8590e-249">Luodun tai päivitetyn lähetyksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="8590e-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="8590e-250">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="8590e-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="8590e-251">Etsi ja valitse tarvittava lähetys.</span><span class="sxs-lookup"><span data-stu-id="8590e-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="8590e-252">Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8590e-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="8590e-253">Myyntitilausten vapauttaminen tilausjoukosta 1</span><span class="sxs-lookup"><span data-stu-id="8590e-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="8590e-254">Vapauta myyntitilaukset tilausjoukosta 1 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8590e-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="8590e-255">Lopuksi näkyvissä pitäisi olla kaksi luotua lähetystä:</span><span class="sxs-lookup"><span data-stu-id="8590e-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="8590e-256">Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="8590e-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="8590e-257">Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.</span><span class="sxs-lookup"><span data-stu-id="8590e-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="8590e-258">Myyntitilausten vapauttaminen tilausjoukosta 2</span><span class="sxs-lookup"><span data-stu-id="8590e-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="8590e-259">Vapauta myyntitilaukset tilausjoukosta 2 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8590e-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="8590e-260">Lopuksi näkyvissä pitäisi olla kolme luotua lähetystä:</span><span class="sxs-lookup"><span data-stu-id="8590e-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="8590e-261">Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="8590e-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="8590e-262">Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.</span><span class="sxs-lookup"><span data-stu-id="8590e-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="8590e-263">Myyntitilausten vapauttaminen tilausjoukosta 3</span><span class="sxs-lookup"><span data-stu-id="8590e-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="8590e-264">Vapauta myyntitilaukset tilausjoukosta 3 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8590e-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="8590e-265">Lopputuloksena pitäisi näkyvä seuraavat tapahtuneet toiminnot:</span><span class="sxs-lookup"><span data-stu-id="8590e-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="8590e-266">Yksi aiemmin luotu lähetys (lähetys, joka luotiin vapauttamalla tilausjoukko 2 varastoon) päivitettiin.</span><span class="sxs-lookup"><span data-stu-id="8590e-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="8590e-267">Yhdelle riville on lisätty *Tulenarka*-nimike.</span><span class="sxs-lookup"><span data-stu-id="8590e-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="8590e-268">Luotiin yksi uusi lähetys, joka sisältää *Räjähdysherkkä*-nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="8590e-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="8590e-269">Myyntitilausten vapauttaminen tilausjoukosta 4</span><span class="sxs-lookup"><span data-stu-id="8590e-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="8590e-270">Vapauta myyntitilaukset tilausjoukosta 4 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8590e-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="8590e-271">Lopputuloksena pitäisi näkyä, että yksi aiemmin luotu lähetys (jossa **Asiakkaan ehdotus** -kentän arvoksi on määritetty *1*) päivitettiin.</span><span class="sxs-lookup"><span data-stu-id="8590e-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="8590e-272">Siihen lisättiin yksi uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="8590e-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="8590e-273">Myyntitilausten vapauttaminen tilausjoukosta 5</span><span class="sxs-lookup"><span data-stu-id="8590e-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="8590e-274">Vapauta myyntitilaukset tilausjoukosta 5 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8590e-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="8590e-275">Lopputuloksena pitäisi näkyvä seuraavat tapahtuneet toiminnot:</span><span class="sxs-lookup"><span data-stu-id="8590e-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="8590e-276">Yksi aiemmin luotu lähetys (jossa **Asiakkaan ehdotus** -kentän arvoksi on määritetty *1*) päivitettiin.</span><span class="sxs-lookup"><span data-stu-id="8590e-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="8590e-277">Siihen lisättiin myyntitilauksen 5-3 rivi (jossa **Asiakkaan ehdotus** -kentän arvoksi on määritetty *1*).</span><span class="sxs-lookup"><span data-stu-id="8590e-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="8590e-278">Luotiin yksi uusi lähetys, jossa myyntitilausten 5-1 ja 5-2 rivit ryhmitettiin yhdeksi lähetykseksi.</span><span class="sxs-lookup"><span data-stu-id="8590e-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="8590e-279">Myyntitilausten vapauttaminen tilausjoukosta 6</span><span class="sxs-lookup"><span data-stu-id="8590e-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="8590e-280">Vapauta myyntitilaukset tilausjoukosta 6 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8590e-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="8590e-281">Lopputuloksena pitäisi näkyä neljä luotua lähetystä:</span><span class="sxs-lookup"><span data-stu-id="8590e-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="8590e-282">Tilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="8590e-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="8590e-283">Tilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="8590e-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="8590e-284">Tilin *US-007* myyntitilausten 6–5 ja 6–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="8590e-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="8590e-285">Tilin *US-007* myyntitilausten 6–7 ja 6–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *CrossOrder*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="8590e-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8590e-286">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8590e-286">Additional resources</span></span>

- [<span data-ttu-id="8590e-287">Lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="8590e-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="8590e-288">Lähetyksen konsolidointikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8590e-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
