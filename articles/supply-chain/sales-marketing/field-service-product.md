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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: fi-fi
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Finance and Operationsin tuotteiden synkronointi Field Servicen tuotteisiin

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.

Käytetty **Field Servicen tuotteet (Fin and Opsista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Fin and Opsista Salesiin) – suora** -malliin. Lisätietoja on kohdassa [Tuotteet (Fin and Opsista Salesiin) - suora](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

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

