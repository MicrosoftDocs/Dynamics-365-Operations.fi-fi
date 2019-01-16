---
title: Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen
description: "Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektit synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen

[!include[banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektit synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.

[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin projektit Microsoft Dynamics 365 for Field Serviceen.

**Mallin nimi Tietojen integroinnissa:**
- Projektit (Finance and Operationsista Field Serviceen)

**Tehtävien nimet tietojen integrointiprojektissa:**
- Projektit

Seuraavat synkronointitehtävät tarvitaan, ennen kuin projektiluettelo voidaan synkronoida:
- Tilit (Salesista Finance and Operationsiin) 

## <a name="entity-set"></a>Yksikköjoukko
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektit                |

## <a name="entity-flow"></a>Yksikön työnkulku
Projektit luodaan Finance and Operationsissa. Projektit, joiden **projektityyppi** on aika ja joiden materiaali ja **projektin vaihe** on keskeneräinen, synkronoidaan Field Servicen **Ulkoinen projekti** -yksikköön. Myös projektin numero, nimi ja vaihe sekä asiakastilin tiedot synkronoidaan. **Ulkoinen projekti** -luettelon avulla Field Servicen työtilaukset muodostavat parin Finance and Operationsin projektien kanssa.
Field Service CRM -ratkaisun Ulkoinen projekti on uusi yksikkö, johon kaikki Operationsin projektit kerätään.
Ulkoinen projekti -kenttä on lisätty Työtilaus-yksikköön. Kenttä on valinta- ja ostokenttä, joka merkitsee työtilaukseen projektin tunnisteen, jonka jälkeen myyntitilaus yhdistetään Operationsin projektiin. Kun järjestelmän tila Avoin - käsittelyssä (690,970,000) muuttuu korkeammaksi tilaksi, Ulkoinen projekti -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset
### <a name="in-finance-and-operations"></a>Finance and Operationsissa
Muutosten seurannan ottaminen käyttöön tietoyksikköprojekteissa

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projektit (Finance and Operationsista Field Serviceen): projektit

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProject1.png)](./media/FSProject1.png)

