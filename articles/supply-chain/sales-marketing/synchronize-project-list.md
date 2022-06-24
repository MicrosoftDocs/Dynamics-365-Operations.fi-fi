---
title: Projektiluettelon synkronointi Supply Chain Managementista Field Serviceen
description: Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceeen.
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
ms.openlocfilehash: 71c0580953f01c2d29e99fa2928a0b4a3937d5c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899350"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Projektiluettelon synkronointi Supply Chain Managementista Field Serviceen

[!include[banner](../includes/banner.md)]

Tässä artikkelissa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceeen.

[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Mallit ja tehtävät
Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa projekteja Supply Chain Managementista Field Serviceen.

**Tietojen integroinnin malli**
- Projektit (Supply Chain Managementista Field Serviceen)

**Tietojen integrointiprojektin tehtävä**
- Projektit

Seuraavat synkronointitehtävät tarvitaan, ennen kuin projektiluettelo voidaan synkronoida:
- Tilit (Salesista Supply Chain Managementiin) 

## <a name="entity-set"></a>Yksikköjoukko
| Field Service           | Toimitusketjun hallinta  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektit                |

## <a name="entity-flow"></a>Yksikön työnkulku
Projektit luodaan Supply Chain Managementissa. Projektit, joiden **projektityypiksi** on määritetty **Aika ja materiaali** ja **projektin vaiheeksi** on määritetty **Keskeneräinen**, synkronoidaan Field Servicen **Ulkoinen projekti** -yksikköön. Myös projektin numero, nimi ja vaihe sekä asiakastilin tiedot synkronoidaan. **Ulkoinen projekti** -luettelon avulla Field Servicen työtilaukset muodostavat parin Supply Chain Managementin projektien kanssa.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu
**Ulkoinen projekti** -yksikkö hakee kaikki Supply Chain Managementin projektit. **Ulkoinen projekti** -kenttä on lisätty **Työtilaus**-yksikköön. Tämä on valintakenttä, joten työtilauksen merkitseminen projektiin aiheuttaa myyntitilaus yhdistämisen Supply Chain Managementin projektiin. Kun **järjestelmän tila** **Avoin - käsittelyssä (690 970 000)** muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset
### <a name="supply-chain-management"></a>Toimitusketjun hallinta
Ota muutosten seuranta käyttöön tietoyksikköprojekteissa.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projektit (Supply Chain Managementista Field Serviceen): Projektit

[![Mallin yhdistäminen tietojen integroinnin yhteydessä.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]