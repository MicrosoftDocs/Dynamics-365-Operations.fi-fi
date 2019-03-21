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
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Käytetty **Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen)** -malli perustuu **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -malliin. Lisätietoja on kohdassa [Field Service -tuotteet (Finance and Operationsista Field Serviceen)](field-service-product.md).

Tässä ohjeaiheessa käsitellään kahden mallin eroja: 
- **Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)**
- **Field Service -tuotteet (Finance and Operationsista Field Serviceen)** 

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

**Mallin nimi Tietojen integroinnissa:**

- Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)

**Tehtävän nimi tietojen integrointiprojektissa:**

- Tuotteet

**Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, jota ei ole **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -mallissa. Tämä yhdistämismääritys varmistaa, että varastotason synkronointiin tarvittava varastoyksikkö on mukana.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Field Serviceen): tuotteet

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct1.png)](./media/FSProduct1.png)
