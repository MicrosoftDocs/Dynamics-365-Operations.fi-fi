---
title: Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835667"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin fyysiset varastot Microsoft Dynamics 365 for Field Serviceen.

**Tietojen integroinnin malli**
- Varastot (Fin and Opsista Field Serviceen)

**Tietojen integrointiprojektin tehtävä**
- Varasto

## <a name="entity-set"></a>Yksikköjoukko
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Varastot                             |

## <a name="entity-flow"></a>Yksikön työnkulku
Finance and Operationsissa luodut ja ylläpidetyt fyysiset varastot voidaan synkronoida Field Serviceen Common Data Servicen (CDS) tietojen integrointiprojektilla. Field Serviceen synkronoitavia varastoja voidaan ohjata projektin kyselyn ja suodatuksen lisäasetuksilla. Finance and Operationsista synkronoitavat fyysiset varastot luodaan Field Servicessä siten, että **Ylläpidetään ulkoisesti** -kentän asetukseksi määritetään **Kyllä**. Lisäksi tietue on vain luku -muotoinen.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
Field Servicen ja Finance and Operationsin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto. **Ylläpidetään ulkoisesti** -kenttä on lisätty ratkaisussa **Varasto (msdyn_warehouses)** -yksikköön. Tämä kenttä auttaa määrittämään, käsitelläänkö varastoa Finance and Operationsista vai onko se vain Field Servicessä. Tässä kentässä on seuraavat asetukset:
- **Kyllä** – varasto on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.
- **Ei** – varasto annettiin suoraan Field Servicessä, jossa sitä myös ylläpidetään.

**Ylläpidetään ulkoisesti** -kenttä auttaa hallitsemaan varaston tasojen, oikaisujen, siirtojen ja käytön synkronointia työtilauksissa. Vain varastoja, joiden **Ylläpidetään ulkoisesti** -asetuksena on **Kyllä**, voidaan käyttää suoraan synkronointiin toisessa järjestelmässä olevaan samaan varastoon. 

> [!NOTE]
> Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti** = Ei) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista. Lisätietoja on kohdissa [Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset
### <a name="data-integration-project"></a>Tietojen integrointiprojekti
Ennen varastojen synkronointia projektin kyselyn ja suodatuksen lisäasetukset on päivitettävä sisältämään vain varastot, jotka haluat tuoda Finance and Operationsista Field Serviceen. Huomaa, että Field Servicen varasto tarvitaan, jotta sitä voidaan käyttää työtilauksissa, oikaisuissa ja siirroissa.  

**msdyn_warehouses**-kohteen **integrointiavaimen** varmistaminen:
1. Siirry tietojen integrointiin.
2. Valitse **Yhteysjoukko**-välilehti.
3. Valitse yhteysjoukko, jota käytetään työtilauksen synkronointiin.
4. Valitse **Integrointiavain**-välilehti.
5. Etsi msdyn_warehouses ja varmista, että avain **msdyn_name (nimi)** on lisätty. Jos avainta ei näy, lisää se valitsemalla ensin **Lisää avain** ja sitten **Tallenna** sivun yläosassa.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Varastot (Fin and Opsista Field Serviceen): Varasto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/Warehouse1.png)](./media/Warehouse1.png)
