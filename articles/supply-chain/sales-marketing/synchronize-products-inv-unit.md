---
title: Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835691"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="b3152-103">Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="b3152-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b3152-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="b3152-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b3152-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="b3152-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="b3152-106">Käytetty **Field Service -tuotteet, joissa varastoyksikkö (Fin and Opsista Field Serviceen)** -malli perustuu **Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -malliin.</span><span class="sxs-lookup"><span data-stu-id="b3152-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="b3152-107">Lisätietoja on kohdassa [Field Service -tuotteet (Finance and Operationsista Field Serviceen)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="b3152-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="b3152-108">Tässä ohjeaiheessa käsitellään kahden mallin eroja:</span><span class="sxs-lookup"><span data-stu-id="b3152-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="b3152-109">**Field Service -tuotteet, joissa varastoyksikkö (Fin and Opsista Salesiin)**</span><span class="sxs-lookup"><span data-stu-id="b3152-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="b3152-110">**Field Servicen tuotteet (Fin and Opsista Field Serviceen)**</span><span class="sxs-lookup"><span data-stu-id="b3152-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="b3152-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="b3152-111">Templates and tasks</span></span>

<span data-ttu-id="b3152-112">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="b3152-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="b3152-113">Field Service -tuotteet, joissa varastoyksikkö (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="b3152-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="b3152-114">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="b3152-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="b3152-115">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="b3152-115">Products</span></span>

<span data-ttu-id="b3152-116">**Field Service -tuotteet, joissa varastoyksikkö (Fin and Opsista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, jota ei ole **Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -mallissa.</span><span class="sxs-lookup"><span data-stu-id="b3152-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="b3152-117">Tämä yhdistämismääritys varmistaa, että varastotason synkronointiin tarvittava varastoyksikkö on mukana.</span><span class="sxs-lookup"><span data-stu-id="b3152-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b3152-118">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="b3152-118">Template mapping in Data integration</span></span>

<span data-ttu-id="b3152-119">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b3152-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="b3152-120">Field Service -tuotteet, joissa varastoyksikkö (Fin and Opsista Field Serviceen): tuotteet</span><span class="sxs-lookup"><span data-stu-id="b3152-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="b3152-121">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="b3152-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
