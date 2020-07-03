---
title: Lähetysten konsolidointi manuaalisesti käyttämällä Konsolidoi lähetykset -sivua
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka myöhemmin konsolidoidaan Konsolidoi lähetykset -sivulla.
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
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383758"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="30d90-103">Lähetysten konsolidointi manuaalisesti käyttämällä Konsolidoi lähetykset -sivua</span><span class="sxs-lookup"><span data-stu-id="30d90-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30d90-104">Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka myöhemmin konsolidoidaan **Konsolidoi lähetykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="30d90-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="30d90-105">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="30d90-105">Make demo data available</span></span>

<span data-ttu-id="30d90-106">Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="30d90-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="30d90-107">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="30d90-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="30d90-108">Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="30d90-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="30d90-109">Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu.</span><span class="sxs-lookup"><span data-stu-id="30d90-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="30d90-110">Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="30d90-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="30d90-111">Myyntitilausten luonti skenaarioon</span><span class="sxs-lookup"><span data-stu-id="30d90-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="30d90-112">Aloita luomalla myyntitilauskokoelma, jota voit käyttää.</span><span class="sxs-lookup"><span data-stu-id="30d90-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="30d90-113">Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="30d90-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="30d90-114">Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="30d90-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="30d90-115">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.</span><span class="sxs-lookup"><span data-stu-id="30d90-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="30d90-116">Myyntitilausten 1 ja 2 luominen</span><span class="sxs-lookup"><span data-stu-id="30d90-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="30d90-117">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="30d90-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="30d90-118">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="30d90-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="30d90-119">**Pooli:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="30d90-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="30d90-120">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="30d90-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="30d90-121">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="30d90-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="30d90-122">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="30d90-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="30d90-123">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="30d90-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="30d90-124">Myyntitilausten 3 ja 4 luominen</span><span class="sxs-lookup"><span data-stu-id="30d90-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="30d90-125">Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="30d90-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="30d90-126">**Asiakastili:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="30d90-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="30d90-127">**Pooli:** jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="30d90-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="30d90-128">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="30d90-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="30d90-129">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="30d90-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="30d90-130">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="30d90-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="30d90-131">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="30d90-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="30d90-132">Tilausten vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="30d90-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="30d90-133">Vapauta jokainen tähän skenaarioon luotu myyntitilaus varastoon seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="30d90-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="30d90-134">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="30d90-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="30d90-135">Etsi ja valitse vapautettava myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="30d90-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="30d90-136">Vapauta valittu myyntitilaus valitsemalla toimintoruudun **Varasto**-välilehdessä **Toiminnot \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="30d90-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="30d90-137">Toista tämä menettely jokaisen tähän skenaarioon luodun myyntitilauksen osalta.</span><span class="sxs-lookup"><span data-stu-id="30d90-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="30d90-138">Konsolidoi lähetykset</span><span class="sxs-lookup"><span data-stu-id="30d90-138">Consolidate shipments</span></span>

1. <span data-ttu-id="30d90-139">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="30d90-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="30d90-140">Etsi ja valitse lähetys, joka luotiin, kun myyntitilaus 1 vapautettiin varastoon.</span><span class="sxs-lookup"><span data-stu-id="30d90-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="30d90-141">(Sen **Lähetyksen konsolidointikäytäntö** -kentän asetuksena on oltava *Tilauspooli*.)</span><span class="sxs-lookup"><span data-stu-id="30d90-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="30d90-142">Valitse toimintoruudun **Lähetykset**-välilehdessä **Lähetykset \> Konsolidoi lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="30d90-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="30d90-143">Tarkista konsolidointiin ehdotetut lähetykset.</span><span class="sxs-lookup"><span data-stu-id="30d90-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="30d90-144">Konsolidointiin pitäisi ehdottaa vain lähetystä, jossa on sama käytäntö.</span><span class="sxs-lookup"><span data-stu-id="30d90-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="30d90-145">Sulje **Lähetyksen konsolidointi** -sivu.</span><span class="sxs-lookup"><span data-stu-id="30d90-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="30d90-146">Etsi ja valitse lähetys, joka luotiin, kun myyntitilaus 3 vapautettiin varastoon.</span><span class="sxs-lookup"><span data-stu-id="30d90-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="30d90-147">(Sen **Lähetyksen konsolidointikäytäntö** -kentän asetuksena on oltava *Oletus*.)</span><span class="sxs-lookup"><span data-stu-id="30d90-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="30d90-148">Valitse toimintoruudun **Lähetykset**-välilehdessä **Lähetykset \> Konsolidoi lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="30d90-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="30d90-149">Tarkista, ettei konsolidointiin ole ehdotettu yhtään lähetystä.</span><span class="sxs-lookup"><span data-stu-id="30d90-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="30d90-150">Valitse **Näytä suodattimet**.</span><span class="sxs-lookup"><span data-stu-id="30d90-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="30d90-151">Poista **Tilausnumero**-suodatin **Suodattimet**-ruudussa ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="30d90-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="30d90-152">Tarkista konsolidointiin ehdotetut lähetykset.</span><span class="sxs-lookup"><span data-stu-id="30d90-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="30d90-153">Konsolidointiin pitäisi ehdottaa vain lähetystä, jossa on sama käytäntö.</span><span class="sxs-lookup"><span data-stu-id="30d90-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30d90-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="30d90-154">Additional resources</span></span>

- [<span data-ttu-id="30d90-155">Lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="30d90-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="30d90-156">Lähetyksen konsolidointikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="30d90-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)