---
title: Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "359241"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="29f9c-103">Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="29f9c-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29f9c-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="29f9c-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="29f9c-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="29f9c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="29f9c-106">Käytetty **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Finance and Operationsista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="29f9c-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="29f9c-107">Lisätietoja on kohdassa [Tuotteet (Finance and Operationsista Salesiin) – suora](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="29f9c-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="29f9c-108">Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)**- ja**Field Servicen tuotteet (Finance and Operationsista Field Serviceen) – suora** -mallien eroja.</span><span class="sxs-lookup"><span data-stu-id="29f9c-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="29f9c-109">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="29f9c-109">Templates and tasks</span></span>

<span data-ttu-id="29f9c-110">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="29f9c-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="29f9c-111">Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="29f9c-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="29f9c-112">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="29f9c-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="29f9c-113">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="29f9c-113">Products</span></span>

<span data-ttu-id="29f9c-114">**Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, jota ei ole **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -mallissa.</span><span class="sxs-lookup"><span data-stu-id="29f9c-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="29f9c-115">Tämä yhdistämismääritys varmistaa, että varastotason synkronointiin tarvittava varastoyksikkö on mukana.</span><span class="sxs-lookup"><span data-stu-id="29f9c-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="29f9c-116">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="29f9c-116">Template mapping in Data integration</span></span>

<span data-ttu-id="29f9c-117">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="29f9c-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="29f9c-118">Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen): tuotteet</span><span class="sxs-lookup"><span data-stu-id="29f9c-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="29f9c-119">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="29f9c-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>