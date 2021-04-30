---
title: Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.
author: ChristianRytt
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909988"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="36c11-103">Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="36c11-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="36c11-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="36c11-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="36c11-105">Käytetty **Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Supply Chain Managementista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="36c11-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="36c11-106">Lisätietoja on kohdassa [Tuotteet (Supply Chain Managementista Salesiin) – suora](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="36c11-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="36c11-107">Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)**- ja **Tuotteet (Supply Chain Managementista Salesiin) – suora** -mallien eroja.</span><span class="sxs-lookup"><span data-stu-id="36c11-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="36c11-108">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="36c11-108">Templates and tasks</span></span>

<span data-ttu-id="36c11-109">**Mallin nimi Tietojen integroinnissa**</span><span class="sxs-lookup"><span data-stu-id="36c11-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="36c11-110">Field Service -tuotteet (Supply Chain Managementista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="36c11-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="36c11-111">**Tehtävän nimi tietojen integrointiprojektissa**</span><span class="sxs-lookup"><span data-stu-id="36c11-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="36c11-112">Tuotteet - tuotteet</span><span class="sxs-lookup"><span data-stu-id="36c11-112">Products - Products</span></span>

<span data-ttu-id="36c11-113">**Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)** -malli sisältää yhden määrityksen, joka ei sisälly **Tuotteet (Supply Chain Managementista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="36c11-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="36c11-114">Tämä yhdistämismääritys varmistaa, että vaadittu Field Service -kohtainen kenttä **Huollon tuotetyyppi** on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="36c11-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="36c11-115">Seuraavaa arvon määritystä käytetään.</span><span class="sxs-lookup"><span data-stu-id="36c11-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="36c11-116">Supply Chain Managementissa **Myytävät vapautetut tuotteet** -tietoyksikön **Kenttäpalvelun tuotetyyppi** -arvo lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="36c11-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="36c11-117">**Varasto:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = tosi</span><span class="sxs-lookup"><span data-stu-id="36c11-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="36c11-118">**NonInventory:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = epätosi</span><span class="sxs-lookup"><span data-stu-id="36c11-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="36c11-119">**Huolto:** Tuotetyyppi = huolto</span><span class="sxs-lookup"><span data-stu-id="36c11-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="36c11-120">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="36c11-120">Template mapping in Data integration</span></span>

<span data-ttu-id="36c11-121">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="36c11-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="36c11-122">Field Service -tuotteet (Supply Chain Managementista Field Serviceen): Tuotteet – Tuotteet</span><span class="sxs-lookup"><span data-stu-id="36c11-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="36c11-123">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="36c11-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]