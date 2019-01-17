---
title: Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen
description: "Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla fyysiset varastot synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla fyysiset varastot synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin fyysiset varastot Microsoft Dynamics 365 for Field Serviceen.

**Mallin nimi Tietojen integroinnissa:**
- Varastot (Finance and Operationsista Field Serviceen)

**Tehtävien nimet tietojen integrointiprojektissa:**
- Varasto

## <a name="entity-set"></a>Yksikköjoukko
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Varastot                             |

## <a name="entity-flow"></a>Yksikön työnkulku
Finance and Operationsissa luodut ja ylläpidetyt fyysiset varastot voidaan synkronoida Field Serviceen Common Data Servicen (CDS) tietojen integrointiprojektilla. Field Serviceen synkronoitavia varastoja voidaan ohjata projektin kyselyn ja suodatuksen lisäasetuksilla. Finance and Operationsista synkronoitavat fyysiset varastot luodaan Field Servicessä siten, että Ylläpidetään ulkoisesti -kentän asetukseksi määritetään Kyllä. Lisäksi tietue on vain luku -muotoinen.
Field Service CRM -ratkaisu Field Servicen ja Finance and Operationsin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto. Ratkaisu sisältää seuraavat muutokset.
**Ylläpidetään ulkoisesti** -kenttä on lisätty **Varasto (msdyn_warehouses)** -yksikköön. Tämä kenttä auttaa määrittämään, käsitelläänkö varastoa Operationsista vai onko se vain Field Servicessä.
- Kyllä – varasto on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.
- Ei – varasto annettiin suoraan Field Servicessä, jossa sitä myös ylläpidetään.

**Ylläpidetään ulkoisesti** -kenttää auttaa hallitsemaan varaston tasojen, oikaisujen, siirtojen ja käytön synkronointia työtilauksissa. Vain varastoja, joiden **Ylläpidetään ulkoisesti** = Kyllä, voidaan käyttää suoraan synkronointiin toisessa järjestelmässä olevaan samaan varastoon. 

Huomautus: Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti** = Ei) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla. Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin. Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista. Lisätietoja on kohdissa Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin ja Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset
### <a name="in-the-data-integration-project"></a>Tietojen integrointiprojektissa
Ennen varastojen synkronointia projektin kyselyn ja suodatuksen lisäasetukset on päivitettävä sisältämään vain varastot, jotka haluat tuoda Finance and Operationsista Field Serviceen. Huomaa, että Field Servicen varasto tarvitaan, jotta sitä voidaan käyttää työtilauksissa, oikaisuissa ja siirroissa.  

**msdyn_warehouses**-kohteen **integrointiavaimen** varmistaminen
1. Siirry tietojen integrointiin
2. Valitse **Yhteysjoukko**-välilehti
3. Valitse yhteysjoukko, jota käytetään työtilauksen synkronointiin
4. Valitse **Integrointiavain**-välilehti
5. Etsi msdyn_warehouses ja tarkista, että avain **msdyn_name (nimi)** on lisätty. Jos avainta ei näy, lisää se napsauttamalla **Lisää avain** ja **Tallenna** sivun yläosassa

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Varastot (Finance and Operationsista Field Serviceen): varasto

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/Warehouse1.png)](./media/Warehouse1.png)

