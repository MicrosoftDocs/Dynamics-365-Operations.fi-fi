---
title: Varastojen synkronointi Supply Chain Managementista Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 28445592d7a2a8964b1642ae52cff08be6feabbe
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529503"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Varastojen synkronointi Supply Chain Managementista Field Serviceen

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa varastoja Supply Chain Managementista Field Serviceen.

**Tietojen integroinnin malli**
- Varastot (Supply Chain Managementista Field Serviceen)

**Tietojen integrointiprojektin tehtävä**
- Varasto

## <a name="entity-set"></a>Yksikköjoukko
| Field Service    | Toimitusketjun hallinta                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Varastot                             |

## <a name="entity-flow"></a>Yksikön työnkulku
Supply Chain Managementissa luodut ja ylläpidetyt fyysiset varastot voidaan synkronoida Field Serviceen Common Data Servicen (CDS) tietojen integrointiprojektilla. Field Serviceen synkronoitavia varastoja voidaan ohjata projektin kyselyn ja suodatuksen lisäasetuksilla. Supply Chain Managementista synkronoitavat fyysiset varastot luodaan Field Servicessa siten, että **Ylläpidetään ulkoisesti** -kentän asetukseksi määritetään **Kyllä**. Lisäksi tietue on Vain luku -muotoinen.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
Field Servicen ja Supply Chain Managementin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto. **Ylläpidetään ulkoisesti** -kenttä on lisätty ratkaisussa **Varasto (msdyn_warehouses)** -yksikköön. Tämä kenttä auttaa määrittämään, käsitelläänkö varastoa Supply Chain Managementista vai onko se vain Field Servicessa. Tässä kentässä on seuraavat asetukset:
- **Kyllä** – Varasto on peräisin Supply Chain Managementista eikä sitä voi muokata Salesissa.
- **Ei** – varasto annettiin suoraan Field Servicessä, jossa sitä myös ylläpidetään.

**Ylläpidetään ulkoisesti** -kenttä auttaa hallitsemaan varaston tasojen, oikaisujen, siirtojen ja käytön synkronointia työtilauksissa. Vain varastoja, joiden **Ylläpidetään ulkoisesti** -asetuksena on **Kyllä**, voidaan käyttää suoraan synkronointiin toisessa järjestelmässä olevaan samaan varastoon. 

> [!NOTE]
> Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti** = Ei) ja ne voi sitten yhdistää yhteen varastoon kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicella halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Supply Chain Managementiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Supply Chain Managementista. Lisätietoja on kohdissa [Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset
### <a name="data-integration-project"></a>Tietojen integrointiprojekti
Ennen varastojen synkronointia projektin kyselyn ja suodatuksen lisäasetukset on päivitettävä sisältämään vain varastot, jotka haluat tuoda Supply Chain Managementista Field Serviceen. Huomaa, että Field Servicen varasto tarvitaan, jotta sitä voidaan käyttää työtilauksissa, oikaisuissa ja siirroissa.  

**msdyn_warehouses**-kohteen **integrointiavaimen** varmistaminen:
1. Siirry tietojen integrointiin.
2. Valitse **Yhteysjoukko**-välilehti.
3. Valitse yhteysjoukko, jota käytetään työtilauksen synkronointiin.
4. Valitse **Integrointiavain**-välilehti.
5. Etsi msdyn_warehouses ja varmista, että avain **msdyn_name (nimi)** on lisätty. Jos avainta ei näy, lisää se valitsemalla ensin **Lisää avain** ja sitten **Tallenna** sivun yläosassa.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Varastot (Supply Chain Managementista Field Serviceen): Varasto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]