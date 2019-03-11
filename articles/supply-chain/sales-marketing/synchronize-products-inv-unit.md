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
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Finance and Operationsin tuotteiden ja varastoyksiköiden synkronointi Field Serviceen

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin varastoyksiköstä Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Käytetty **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Finance and Operationsista Salesiin) – suora** -malliin. Lisätietoja on kohdassa [Tuotteet (Finance and Operationsista Salesiin) – suora](products-template-mapping-direct.md).

Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)**- ja**Field Servicen tuotteet (Finance and Operationsista Field Serviceen) – suora** -mallien eroja.

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
