---
title: Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2019
ms.locfileid: "836299"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="957b9-103">Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="957b9-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="957b9-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="957b9-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="957b9-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="957b9-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="957b9-106">Käytetty **Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen)** -malli perustuu **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -malliin.</span><span class="sxs-lookup"><span data-stu-id="957b9-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="957b9-107">Lisätietoja on kohdassa [Field Service -tuotteet (Finance and Operationsista Field Serviceen)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="957b9-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="957b9-108">Tässä ohjeaiheessa käsitellään kahden mallin eroja:</span><span class="sxs-lookup"><span data-stu-id="957b9-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="957b9-109">**Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)**</span><span class="sxs-lookup"><span data-stu-id="957b9-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="957b9-110">**Field Service -tuotteet (Finance and Operationsista Field Serviceen)**</span><span class="sxs-lookup"><span data-stu-id="957b9-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="957b9-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="957b9-111">Templates and tasks</span></span>

<span data-ttu-id="957b9-112">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="957b9-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="957b9-113">Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="957b9-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="957b9-114">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="957b9-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="957b9-115">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="957b9-115">Products</span></span>

<span data-ttu-id="957b9-116">**Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, jota ei ole **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -mallissa.</span><span class="sxs-lookup"><span data-stu-id="957b9-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="957b9-117">Tämä yhdistämismääritys varmistaa, että varastotason synkronointiin tarvittava varastoyksikkö on mukana.</span><span class="sxs-lookup"><span data-stu-id="957b9-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="957b9-118">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="957b9-118">Template mapping in Data integration</span></span>

<span data-ttu-id="957b9-119">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="957b9-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="957b9-120">Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen): tuotteet</span><span class="sxs-lookup"><span data-stu-id="957b9-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="957b9-121">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="957b9-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
