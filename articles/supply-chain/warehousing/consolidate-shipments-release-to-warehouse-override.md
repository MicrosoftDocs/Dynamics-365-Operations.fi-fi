---
title: Lähetysten konsolidointi, kun lähetyksen konsolidointikäytäntö korvataan Vapauta varastoon -sivulta
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa vähintään yksi myyntirivi on vapautettava varastoon manuaalisesti Vapauta varastoon -sivulla ja järjestelmän määrittämä lähetyksen konsolidointikäytäntö on korvattava ennen vapautusta.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: be573f3a137fbd74ba2f5d8bb346e4bb9f9116c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237104"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="d4c2b-103">Lähetysten konsolidointi, kun lähetyksen konsolidointikäytäntö korvataan Vapauta varastoon -sivulta</span><span class="sxs-lookup"><span data-stu-id="d4c2b-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4c2b-104">Tässä ohjeaiheessa käsitellään skenaariota, jossa vähintään yksi myyntirivi on vapautettava varastoon manuaalisesti **Vapauta varastoon** -sivulla ja järjestelmän määrittämä lähetyksen konsolidointikäytäntö on korvattava ennen vapautusta.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="d4c2b-105">Lähetyksen konsolidointikäytäntö on ehkä korvattava, jos esimerkiksi tilaus, jota ei yleensä konsolidoida avoimien lähetysten kanssa, on konsolidoitava avoimien lähetysten kanssa.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="d4c2b-106">Tämän skenaarion aikana luodaan myyntitilausjoukko ja korvataan sitten lähetyksen oletuskonsolidointikäytäntö ennen tilausten vapauttamista varastoon.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="d4c2b-107">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="d4c2b-107">Make demo data available</span></span>

<span data-ttu-id="d4c2b-108">Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d4c2b-109">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="d4c2b-110">Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d4c2b-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="d4c2b-111">Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="d4c2b-112">Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="d4c2b-113">Myyntitilausten luonti skenaarioon</span><span class="sxs-lookup"><span data-stu-id="d4c2b-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="d4c2b-114">Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo siten kolme samanlaista myyntitilausta, joissa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="d4c2b-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d4c2b-115">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d4c2b-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="d4c2b-116">Lisää tilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="d4c2b-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d4c2b-117">**Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)</span><span class="sxs-lookup"><span data-stu-id="d4c2b-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d4c2b-118">**Määrä** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d4c2b-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d4c2b-119">Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="d4c2b-120">Myyntitilausten vapauttaminen Vapauta varastoon -sivulta</span><span class="sxs-lookup"><span data-stu-id="d4c2b-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="d4c2b-121">Korvaa lähetyksen konsolidointikäytäntö varastoon vapautuksen aikana seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d4c2b-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="d4c2b-122">Valitse **Varastonhallinta \> Vapauta varastoon \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="d4c2b-123">Valitse yläruudussa ensimmäinen tähän skenaarioon luotu myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="d4c2b-124">Lisää rivi varastoon vapautukseen valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="d4c2b-125">Huomaa, että *oletusarvoinen* lähetyksen konsolidointikäytäntöä käytetään alaruudussa.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="d4c2b-126">Valitse alaruudussa **Valitse uusi lähetyksen konsolidointikäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="d4c2b-127">Valitse käytäntö, joka sallii konsolidoinnin muiden samaa käytäntöä käyttävien avoimien lähetysten konsolidoinnin.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="d4c2b-128">Valitse esimerkiksi *CustomerOrderNo*-käytäntö.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="d4c2b-129">Valitse **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="d4c2b-130">Valitse toinen ja kolmas tähän skenaarioon luotu myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="d4c2b-131">Lisää rivit varastoon vapautukseen valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="d4c2b-132">Huomaa, että *oletusarvoista* käytäntöä käytetään alaruudussa.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="d4c2b-133">Valitse ensin toinen rivi ja valitse sitten **Valitse uusi lähetyksen konsolidointikäytäntö** -kentässä *CustomerOrderNo*-käytäntö.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="d4c2b-134">Valitse kummallakin rivillä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="d4c2b-135">Lähetysten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="d4c2b-135">Verify the shipments</span></span>

<span data-ttu-id="d4c2b-136">Luotuja lähetyksiä on oltava kaksi:</span><span class="sxs-lookup"><span data-stu-id="d4c2b-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="d4c2b-137">Ensimmäisessä lähetyksessä on kaksi riviä, ja se luotiin käyttämällä lähetysten *CustomerOrderNo*-konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="d4c2b-138">Toisessa lähetyksessä on yksi rivi, ja se luotiin käyttämällä *oletusarvoista* lähetysten konsolidointikäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="d4c2b-139">Tarkista luodut lähetykset seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="d4c2b-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="d4c2b-140">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="d4c2b-141">Etsi ja valitse tarvittava lähetys.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="d4c2b-142">Tarkista **Lähetyksen konsolidointikäytäntö** -kentässä konsolidointikäytäntö, jota käytettiin lähetystä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="d4c2b-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4c2b-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d4c2b-143">Additional resources</span></span>

- [<span data-ttu-id="d4c2b-144">Lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="d4c2b-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="d4c2b-145">Lähetyksen konsolidointikäytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d4c2b-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]