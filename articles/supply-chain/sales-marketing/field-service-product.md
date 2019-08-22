---
title: Finance and Operationsin tuotteiden synkronointi Field Servicen tuotteisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.
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
ms.openlocfilehash: 06d7ff272ecb79abded3c3d3ade1f6bc0ef1f095
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742352"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Finance and Operationsin tuotteiden synkronointi Field Servicen tuotteisiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.

Käytetty **Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Fin and Opsista Salesiin) – suora** -malliin. Lisätietoja on kohdassa [Tuotteet (Fin and Opsista Salesiin) - suora](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Fin and Opsista Field Serviceen)**- ja**Tuotteet (Fin and Opsista Salesiin) – suora** -mallien eroja.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

**Mallin nimi Tietojen integroinnissa:**

- Field Servicen tuotteet (Fin and Opsista Field Serviceen)

**Tehtävän nimi tietojen integrointiprojektissa:**

- Tuotteet - tuotteet

**Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -malli sisältää yhden yhdistämismäärityksen, joka ei sisälly **Tuotteet (Fin and Opsista Salesiin) – suora** -malliin. Tämä yhdistämismääritys varmistaa, että vaadittu Field Service -kohtainen kenttä **Huollon tuotetyyppi** on määritetty oikein.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Seuraavaa arvon määritystä käytetään.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Finance and Operationsissa **Myytävät vapautetut tuotteet** -tietoyksikön **Kenttäpalvelun tuotetyyppi** -arvo lasketaan seuraavasti:

- **Varasto:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = tosi
- **NonInventory:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = epätosi
- **Huolto:** Tuotetyyppi = huolto

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Servicen tuotteet (Fin and Opsista Field Serviceen): Tuotteet - Tuotteet

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct.png)](./media/FSProduct.png)
