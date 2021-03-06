---
title: Tuotteiden ja varastoyksiköiden synkronointi Supply Chain Managementista Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementin varastoyksiköstä Dynamics 365 Field Serviceen.
author: ChristianRytt
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 0ecb03d7d826fc6d79f1df800da22dc913177ee4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824867"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Tuotteiden ja varastoyksiköiden synkronointi Supply Chain Managementista Field Serviceen

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementin varastoyksiköstä Dynamics 365 Field Serviceen.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Käytetty **Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Field Serviceen)** -malli perustuu **Field Service -tuotteet (Supply Chain Managementista Field Serviceen)** -malliin. Lisätietoja on kohdassa [Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin](field-service-product.md).

Tässä ohjeaiheessa käsitellään kahden mallin eroja: 
- **Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin)**
- **Field Service -tuotteet (Supply Chain Managementista Field Serviceen)** 

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

**Mallin nimi Tietojen integroinnissa:**

- Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin)

**Tehtävän nimi tietojen integrointiprojektissa:**

- Tuotteet

**Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, joka ei sisälly **Field Service -tuotteet (Supply Chain Managementista Field Serviceen)** -malliin. Tämä yhdistämismääritys varmistaa, että varastotason synkronointiin tarvittava varastoyksikkö on mukana.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Field Serviceen): Tuotteet

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]