---
title: Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c87e4cbfa375ef99d00c9a145c190af78e912d56
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029402"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="85889-103">Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="85889-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85889-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="85889-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="85889-105">Käytetty **Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Supply Chain Managementista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="85889-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="85889-106">Lisätietoja on kohdassa [Tuotteet (Supply Chain Managementista Salesiin) – suora](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="85889-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="85889-107">Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)**- ja**Tuotteet (Supply Chain Managementista Salesiin) – suora** -mallien eroja.</span><span class="sxs-lookup"><span data-stu-id="85889-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="85889-108">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="85889-108">Templates and tasks</span></span>

<span data-ttu-id="85889-109">**Mallin nimi Tietojen integroinnissa**</span><span class="sxs-lookup"><span data-stu-id="85889-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="85889-110">Field Service -tuotteet (Supply Chain Managementista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="85889-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="85889-111">**Tehtävän nimi tietojen integrointiprojektissa**</span><span class="sxs-lookup"><span data-stu-id="85889-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="85889-112">Tuotteet - tuotteet</span><span class="sxs-lookup"><span data-stu-id="85889-112">Products - Products</span></span>

<span data-ttu-id="85889-113">**Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)** -malli sisältää yhden määrityksen, joka ei sisälly **Tuotteet (Supply Chain Managementista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="85889-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="85889-114">Tämä yhdistämismääritys varmistaa, että vaadittu Field Service -kohtainen kenttä **Huollon tuotetyyppi** on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="85889-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```Text
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="85889-115">Seuraavaa arvon määritystä käytetään.</span><span class="sxs-lookup"><span data-stu-id="85889-115">The following value mapping is used.</span></span>

```Text
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="85889-116">Supply Chain Managementissa **Myytävät vapautetut tuotteet** -tietoyksikön **Kenttäpalvelun tuotetyyppi** -arvo lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85889-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="85889-117">**Varasto:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = tosi</span><span class="sxs-lookup"><span data-stu-id="85889-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="85889-118">**NonInventory:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = epätosi</span><span class="sxs-lookup"><span data-stu-id="85889-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="85889-119">**Huolto:** Tuotetyyppi = huolto</span><span class="sxs-lookup"><span data-stu-id="85889-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="85889-120">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="85889-120">Template mapping in Data integration</span></span>

<span data-ttu-id="85889-121">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="85889-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="85889-122">Field Service -tuotteet (Supply Chain Managementista Field Serviceen): Tuotteet – Tuotteet</span><span class="sxs-lookup"><span data-stu-id="85889-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="85889-123">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="85889-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
