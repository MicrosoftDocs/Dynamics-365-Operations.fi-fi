---
title: "Projektitehtävien synkronointi Project Service Automationista"
description: "Tässä ohjeaiheessa käsitellään mallia ja taustalla olevaa tehtävää, joilla projektitehtävät tiedot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Projektitehtävien synkronointi Project Service Automationista suoraan Finance and Operationsin projektitoimintoihin

Tässä ohjeaiheessa käsitellään mallia ja taustalla olevaa tehtävää, joilla projektitehtävät tiedot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin.

> [!NOTE]
> Projektitehtävien integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tiedonkulku Project Service Automationista Finance and Operationsiin

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä oleva integrointimalli mahdollistaa projektitehtäviä koskevan tiedonkulun Project Service Automationista Finance and Operationsiin.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Malli ja tehtävä

Saat mallin käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektitehtävät Project Service Automationista Finance and Operationsiin:

-**Mallin nimi tietojen integroinnissa:** Projektitehtävät (PSA:sta Fin and Opsiin) -**Projektin tehtävän nimi:** Projektitehtävät

Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.

## <a name="entity-set"></a>Yksikköjoukko

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Projektitehtävät                           | Projektitehtävän integrointiyksikkö.   |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektitehtäviä hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektitoimintoina.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.

## <a name="power-query"></a>Power Query

Jos seuraavat ehdot toteutuvat, tietojen suodattamiseen on käytettävä Microsoft Power Queryä:

- Projektitehtävässä on resurssikohtaisia tietueita.

Jos Power Queryä on käytettävä, noudata seuraavaa ohjeistusta:

- Projektitehtävät (PSA:sta Fin and Opsiiin) -mallissa on oletussuodatin, joka jättää projektitehtävän resurssikohtaiset tietueet pois, kun **IsLineTask**-suodatinasetukseksi on määritetty **Epätosi**. Jos luot oman mallin, tämä suodatin on lisättävä.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


