---
title: Projektin sisältävien työtilausten synkronointi Field Servicestä Finance and Operationsiin
description: Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Microsoft Dynamics 365 for Field Servicestä Microsoft Dynamics 365 for Finance and Operationsiin.
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2019
ms.locfileid: "836439"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Projektin sisältävien työtilausten synkronointi Field Servicestä Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Microsoft Dynamics 365 for Field Servicestä Microsoft Dynamics 365 for Finance and Operationsiin.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Käytetty **Projektin työtilaukset (Field Servicestä Finance and Operationsiin)** -malli perustuu **Työtilaukset (Field Servicestä Finance and Operationsiin)** -malliin. Lisätietoja on kohdassa [Field Servicen työtilausten synkronointi Finance and Operationsin myyntitilauksiin](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Tässä ohjeaiheessa käsitellään kahden mallin eroja:
- **Projektin työtilaukset (Field Servicestä Finance and Operationsiin)**
- **Työtilaukset (Field Servicestä Finance and Operationsiin)**

Pääasiallisin ero on, että tämä malli sisältää työtilaukselle Field Servicessä määritetyn projektinumeron yhdistämismäärityksen, mikä varmistaa, että Finance and Operationsissa luotu myyntitilaus sisältää projektinumeron ja että laskutus voidaan tehdä liittyvässä projektissa. Tämän lisäksi malli käyttää kyselyn ja suodatuksen lisäasetuksia.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

**Mallin nimi Tietojen integroinnissa:**

- Projektin työtilaukset (Field Servicestä Finance and Operationsiin)

**Tehtävän nimi tietojen integrointiprojektissa:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
**Ulkoinen projekti** -kenttä on lisätty Työtilaus-yksikköön. Kenttä on valinta- ja ostokenttä, joka merkitsee työtilaukseen projektin tunnisteen, jonka jälkeen myyntitilaus yhdistetään Finance and Operationsin projektiin. Kun **järjestelmän tila** Avoin - käsittelyssä (690,970,000) muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderHeader

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderHeaderProject

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderProduct

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderService

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP4.png)](./media/FSWOP4.png)
