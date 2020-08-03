---
title: Tuotteiden ja varastoyksiköiden synkronointi Supply Chain Managementista Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementin varastoyksiköstä Dynamics 365 Field Serviceen.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 62ed33d101f7d7e47b560c417dc05e5aecc83478
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546335"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="cf948-103">Tuotteiden ja varastoyksiköiden synkronointi Supply Chain Managementista Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="cf948-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cf948-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementin varastoyksiköstä Dynamics 365 Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="cf948-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="cf948-105">[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="cf948-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="cf948-106">Käytetty **Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Field Serviceen)** -malli perustuu **Field Service -tuotteet (Supply Chain Managementista Field Serviceen)** -malliin.</span><span class="sxs-lookup"><span data-stu-id="cf948-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="cf948-107">Lisätietoja on kohdassa [Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="cf948-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="cf948-108">Tässä ohjeaiheessa käsitellään kahden mallin eroja:</span><span class="sxs-lookup"><span data-stu-id="cf948-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="cf948-109">**Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin)**</span><span class="sxs-lookup"><span data-stu-id="cf948-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="cf948-110">**Field Service -tuotteet (Supply Chain Managementista Field Serviceen)**</span><span class="sxs-lookup"><span data-stu-id="cf948-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="cf948-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="cf948-111">Templates and tasks</span></span>

<span data-ttu-id="cf948-112">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="cf948-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cf948-113">Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="cf948-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="cf948-114">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="cf948-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cf948-115">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="cf948-115">Products</span></span>

<span data-ttu-id="cf948-116">**Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, joka ei sisälly **Field Service -tuotteet (Supply Chain Managementista Field Serviceen)** -malliin.</span><span class="sxs-lookup"><span data-stu-id="cf948-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="cf948-117">Tämä yhdistämismääritys varmistaa, että varastotason synkronointiin tarvittava varastoyksikkö on mukana.</span><span class="sxs-lookup"><span data-stu-id="cf948-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cf948-118">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="cf948-118">Template mapping in Data integration</span></span>

<span data-ttu-id="cf948-119">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="cf948-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="cf948-120">Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Field Serviceen): Tuotteet</span><span class="sxs-lookup"><span data-stu-id="cf948-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="cf948-121">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="cf948-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
