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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 87daaa3d2b516581e9925fe6b769683942893ff6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206916"
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