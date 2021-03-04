---
title: Työtilausten ja projektin synkronointi Field Servicesta Supply Chain Managementiin
description: Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Dynamics 365 Field Servicestä Dynamics 365 Supply Chain Managementiin.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ebf23c5c831e9dad5d13c72f82eb3eeb30da853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426882"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Työtilausten ja projektin synkronointi Field Servicesta Supply Chain Managementiin

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Dynamics 365 Field Servicestä Dynamics 365 Supply Chain Managementiin.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Käytetty **Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)** -malli perustuu **Työtilaukset (Field Servicesta Supply Chain Managementiin)** -malliin. Lisätietoja on kohdassa [Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Tässä ohjeaiheessa käsitellään kahden mallin eroja:
- **Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)**
- **Työtilaukset (Field Servicesta Supply Chain Managementiin)**

Pääasiallisin ero on, että tämä malli sisältää työtilaukselle Field Servicessa määritetyn projektinumeron yhdistämismäärityksen, mikä varmistaa, että Supply Chain Managementissa luotu myyntitilaus sisältää projektinumeron ja että laskutus voidaan tehdä liittyvässä projektissa. Tämän lisäksi malli käyttää kyselyn ja suodatuksen lisäasetuksia.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

**Mallin nimi Tietojen integroinnissa:**

- Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)

**Tehtävän nimi tietojen integrointiprojektissa:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
**Ulkoinen projekti** -kenttä on lisätty Työtilaus-yksikköön. Tämä kenttä on valintakenttä ja työtilauksen merkitseminen projektiin aiheuttaa myyntitilauksen yhdistämisen Supply Chain Managementin projektiin. Kun **Järjestelmän tila** muuttuu Avoin - käsittelyssä (690 970 000) -tilasta korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderHeader

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderHeaderProject

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderProduct

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderService

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]