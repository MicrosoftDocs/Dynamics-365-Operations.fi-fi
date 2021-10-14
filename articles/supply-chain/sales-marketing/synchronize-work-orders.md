---
title: Työtilausten ja projektin synkronointi Field Servicesta Supply Chain Managementiin
description: Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Dynamics 365 Field Servicestä Dynamics 365 Supply Chain Managementiin.
author: Henrikan
ms.date: 03/12/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: f0b3214aba5882a585664030d6c1aebe34de455c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572526"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Työtilausten ja projektin synkronointi Field Servicesta Supply Chain Managementiin

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Dynamics 365 Field Servicestä Dynamics 365 Supply Chain Managementiin.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Käytetty **Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)** -malli perustuu **Työtilaukset (Field Servicesta Supply Chain Managementiin)** -malliin. Lisätietoja on kohdassa [Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

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

[![Työtilauksista projektiin integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderHeaderProject

[![Työtilauksista projektiin integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderProduct

[![Työtilauksista projektiin integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderService

[![Työtilauksista projektiin integroitavien tietojen mallin yhdistämismääritys (Field Servicesta Supply Chain Managementiin): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]