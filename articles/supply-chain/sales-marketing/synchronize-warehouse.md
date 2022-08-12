---
title: Varastojen synkronointi Supply Chain Managementista Field Serviceen
description: Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8b86b6a59344299a7a2d277543c3186ed2b8cee4
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103230"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Varastojen synkronointi Supply Chain Managementista Field Serviceen

[!include[banner](../includes/banner.md)]



Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceen.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa varastoja Supply Chain Managementista Field Serviceen.

**Tietojen integroinnin malli**
- Varastot (Supply Chain Managementista Field Serviceen)

**Tietojen integrointiprojektin tehtävä**
- Varasto

## <a name="table-set"></a>Taulujoukko
| Field Service    | Toimitusketjun hallinta                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Varastot                             |

## <a name="table-flow"></a>Taulutyönkulku
Supply Chain Managementissa luodut ja ylläpidetyt fyysiset varastot voidaan synkronoida Field Serviceen Microsoft Dataversen tietojen integrointiprojektilla. Field Serviceen synkronoitavia varastoja voidaan ohjata projektin kyselyn ja suodatuksen lisäasetuksilla. Supply Chain Managementista synkronoitavat fyysiset varastot luodaan Field Servicessa siten, että **Ylläpidetään ulkoisesti** -sarakkeen asetukseksi määritetään **Kyllä**. Lisäksi tietue on vain luku -muotoinen.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
Field Servicen ja Supply Chain Managementin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto. **Ylläpidetään ulkoisesti** -sarakeon lisätty ratkaisussa **Varasto (msdyn_warehouses)** -taulukkoon. Tämä sarake auttaa määrittämään, käsitelläänkö varastoa Supply Chain Managementista vai onko se vain Field Servicessa. Tässä sarakkeessa on seuraavat asetukset:
- **Kyllä** – Varasto on peräisin Supply Chain Managementista eikä sitä voi muokata Salesissa.
- **Ei** – varasto annettiin suoraan Field Servicessä, jossa sitä myös ylläpidetään.

**Ylläpidetään ulkoisesti** -sarake auttaa hallitsemaan varaston tasojen, oikaisujen, siirtojen ja käytön synkronointia työtilauksissa. Vain varastoja, joiden **Ylläpidetään ulkoisesti** -asetuksena on **Kyllä**, voidaan käyttää suoraan synkronointiin toisessa järjestelmässä olevaan samaan varastoon. 

> [!NOTE]
> Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti** = Ei) ja ne voi sitten yhdistää yhteen varastoon kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicella halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Supply Chain Managementiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Supply Chain Managementista. Lisätietoja on kohdissa [Varasto-oikaisujen synkronointi Field Servicesta Supply Chain Managementiin](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin linkitettyihin myyntitilauksiin Supply Chain Managementissa](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

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

[![Mallin yhdistäminen tietojen integroinnin yhteydessä.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
