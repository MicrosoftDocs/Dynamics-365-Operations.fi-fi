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
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.

Käytetty **Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Supply Chain Managementista Salesiin) – suora** -malliin. Lisätietoja on kohdassa [Tuotteet (Supply Chain Managementista Salesiin) – suora](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)**- ja **Tuotteet (Supply Chain Managementista Salesiin) – suora** -mallien eroja.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

**Mallin nimi Tietojen integroinnissa**

- Field Service -tuotteet (Supply Chain Managementista Field Serviceen)

**Tehtävän nimi tietojen integrointiprojektissa**

- Tuotteet - tuotteet

**Field Servicen tuotteet (Supply Chain Managementista Field Serviceen)** -malli sisältää yhden määrityksen, joka ei sisälly **Tuotteet (Supply Chain Managementista Salesiin) – suora** -malliin. Tämä yhdistämismääritys varmistaa, että vaadittu Field Service -kohtainen kenttä **Huollon tuotetyyppi** on määritetty oikein.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Seuraavaa arvon määritystä käytetään.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Supply Chain Managementissa **Myytävät vapautetut tuotteet** -tietoyksikön **Kenttäpalvelun tuotetyyppi** -arvo lasketaan seuraavasti:

- **Varasto:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = tosi
- **NonInventory:** Tuotetyyppi = tuote- ja nimikemalliryhmä, varastotuote = epätosi
- **Huolto:** Tuotetyyppi = huolto

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service -tuotteet (Supply Chain Managementista Field Serviceen): Tuotteet – Tuotteet

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]