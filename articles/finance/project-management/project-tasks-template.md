---
title: Projektitehtävien synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektitehtäviä synkronoidaan suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770263"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projektitehtävien synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektitehtäviä synkronoidaan suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeiin.

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytettävissä versiossa 8.0.
> - Jos käytät Enterprise edition -versiota 7.3.0 sen jälkeen, kun KB 4132657 ja KB 4132660 on asennettu, voit käyttää malleja integroidaksesi projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittääksesi toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.
> - Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tiedonkulku Project Service Automationista Financeen

Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä oleva integrointimalli mahdollistaa projektitehtäviä koskevan tiedonkulun Project Service Automationista Financeen.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Project Service Automationin ja Financen välisen integroinnin tiedonkulku](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Malli ja tehtävä

Saat mallin käyttöösi valitsemalla Microsoft Power Appsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektitehtävät Project Service Automationista Financeen:

- **Mallin nimi tietojen integroinnissa:** projektin tehtävät (PSA:sta Fin and Opsiin)
- **Tehtävän nimi projektissa:** Projektitehtävät

Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.

## <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Myyntitiedot                             |
|----------------------------|-------------------------------------|
| Projektitehtävät              | Projektitehtävän integrointiyksikkö |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektitehtäviä hallitaan Project Service Automationissa ja ne synkronoidaan Financeen projektitoimintoina.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.

## <a name="power-query"></a>Power Query

Jos seuraavat ehdot toteutuvat, tietojen suodattamiseen on käytettävä Microsoft Power Query for Exceliä:

- Projektitehtävässä on resurssikohtaisia tietueita.

Jos Power Queryä on käytettävä, noudata seuraavaa ohjeistusta:

- Projektitehtävät (PSA:sta Fin and Opsiiin) -mallissa on oletussuodatin, joka jättää projektitehtävän resurssikohtaiset tietueet pois, kun **IsLineTask**-suodatinasetukseksi on määritetty **Epätosi**. Jos luot oman mallin, tämä suodatin on lisättävä.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
