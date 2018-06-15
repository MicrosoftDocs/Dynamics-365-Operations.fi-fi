---
title: Finance and Operationsin tuotteiden synkronointi Field Servicen tuotteisiin
description: "Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="6fcf0-103">Finance and Operationsin tuotteiden synkronointi Field Servicen tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="6fcf0-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6fcf0-104">Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6fcf0-105">Käytetty **Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Fin and Opsista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="6fcf0-106">Lisätietoja on kohdassa [Tuotteet (Fin and Opsista Salesiin) - suora](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="6fcf0-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="6fcf0-107">Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Fin and Opsista Field Serviceen)**- ja**Tuotteet (Fin and Opsista Salesiin) – suora** -mallien eroja.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6fcf0-108">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="6fcf0-108">Templates and tasks</span></span>

<span data-ttu-id="6fcf0-109">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="6fcf0-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="6fcf0-110">Field Servicen tuotteet (Fin and Opsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="6fcf0-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="6fcf0-111">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="6fcf0-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="6fcf0-112">Tuotteet - tuotteet</span><span class="sxs-lookup"><span data-stu-id="6fcf0-112">Products - Products</span></span>

<span data-ttu-id="6fcf0-113">**Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, joka ei sisälly **Tuotteet (Fin and Opsista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="6fcf0-114">Tämä yhdistämismääritys varmistaa, että vaadittu Field Service -kohtainen kenttä **Huollon tuotetyyppi** on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="6fcf0-115">Seuraavaa arvon määritystä käytetään.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="6fcf0-116">Finance and Operationsissa **Myytävät vapautetut tuotteet** -tietoyksikön **Kenttäpalvelun tuotetyyppi** -arvo lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6fcf0-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="6fcf0-117">**Varasto:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = tosi</span><span class="sxs-lookup"><span data-stu-id="6fcf0-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="6fcf0-118">**NonInventory:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = epätosi</span><span class="sxs-lookup"><span data-stu-id="6fcf0-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="6fcf0-119">**Huolto:** Tuotetyyppi = huolto</span><span class="sxs-lookup"><span data-stu-id="6fcf0-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6fcf0-120">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="6fcf0-120">Template mapping in Data integration</span></span>

<span data-ttu-id="6fcf0-121">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6fcf0-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="6fcf0-122">Field Servicen tuotteet (Fin and Opsista Field Serviceen): Tuotteet - Tuotteet</span><span class="sxs-lookup"><span data-stu-id="6fcf0-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="6fcf0-123">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="6fcf0-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
