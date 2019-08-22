---
title: Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838364"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä.

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.
> - Todellisten tietojen integrointi on mahdollista Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.1 tai sitä uudemmassa versiossa.
> - Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automationin ja Finance and Operationsin tiedonkulku

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin kulutapahtumaluokkia koskevan tiedonkulun Project Service Automationin ja Finance and Operationsin välillä.

Jos projektin kululuokkia hallitaan Finance and Operationsista, integrointi tapahtuu ensin Finance and Operationsista Project Service Automationiin. Projektin kustannusluokkien integraatiotunnukset päivitetään sitten synkronoinnin avulla Project Service Automationista Finance and Operationsiin.

Jos projektin kululuokkia hallitaan Project Service Automationista, integrointi tapahtuu ensin Project Service Automationista Finance and Operationsiin. Projektiluokkien on oltava määritettynä Finance and Operationsissa ennen synkronointia Project Service Automationista. Voit tämän jälkeen tehdä synkronoinnin Finance and Operationsista takaisin Project Service Automationiin ja sitten uudelleen Project Service Automationista Finance and Operationsiin. Tällöin voit varmistua, että kategoriat on linkitetty eikä kaksoiskappaleita luoda.

> [!NOTE]
> Yleensä projektin kululuokkia hallitaan Finance and Operationsissa. Jos niitä ei kuitenkaan hallita Finance and Operationssa tai kululuokat on jo luotu Project Service Automationissa, synkronoi ensin käyttämällä Project expense transactionin (Fin ja Ops PSA) -kategoriatemplaattia. Synkronoi käyttämällä Project expense transactionin kategoriatemplaattia (Fin ja Ops PSA). Suorita synkronointi vielä kerran Project Service Automationista Finance and Operationsiin.
>
> Jos synkronoit ensin Project Service Automationista, Finance and Operationsin täytyy täyttää seuraavat vaatimukset ennen kuin synkronointi suoritetaan:
>
> - Jaetun kategorian, joka vastaa projektikategoriaa, joka on Project Service Automationissa täytyy olla olemassa ja sen pitää olla käytössä sekä kohdissa **Projekti** että **Kulu**.
> - Seuraavien projektiluokkien täytyy olla olemassa kullakin Finance and Operations -yrityksellä, joka on integroitava:
>
>     - **Projektikategoria** on olemassa. 
>     - **Käytä kuluissa** on käytössä.
>     - **Aktiivinen kirjauskansiossa** on käytössä.
>     - **Transaktiotyyppi** on **Kulu**.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Projektin kululuokkien synkronointi Finance and Operationsista ja Project Service Automationiin

### <a name="template-and-task"></a>Malli ja tehtävä

Saat mallin käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Finance and Operationsista Project Service Automationiin:

- **Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (Fin and Opsista PSA:han)
- **Projektin tehtävän nimi:** luokkien synkronointi PSA:han

### <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Luokkien integrointiyksikkö | Tapahtumaluokat     |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.

### <a name="power-query"></a>Power Query

Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Query for Excelillä, kun synkronointi tehdään Project Service Automationiin. Projektin kulutapahtumaluokkien malli (Fin and Opsista PSA:han) tarjoaa oletussarakkeen ja yhdistämismäärityksen. Jos luot oman mallin, ehtosarake on lisättävä Power Queryssä. Noudata näitä ohjeita.

1. Avaa projektikustannusluokkatehtävän kartoitus napsauttamalla nuolta projektin kulukirjausmallissa (Fin ja Ops to PSA).
2. Napsauta **Kyselyn ja suodatuksen lisäasetukset** avataksesi Power Queryn.
2. Valitse **Lisää ehtosarake**.
3. Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**.
4. Anna seuraava ehto: **jos CATEGORYID ei sama kuin tyhjäarvo sitten 19235001, muuten tyhjäarvo**.
5. Valitse sarakkeessa **OK**.
6. Varmista, että yhdistät tämän uuden sarakkeen yhdistämismäärityssivulla.

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Finance and Operationsista Project Service Automationiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Projektin kululuokkien synkronointi Project Service Automationista Finance and Operationsiin

### <a name="template-and-task"></a>Malli ja tehtävä

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Project Service Automationista Finance and Operationsiin:

- **Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (PSA to Fin and Ops:iin)
- **Projektin tehtävän nimi:** luokkien synkronointi Fin Ops:iin

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Tapahtumaluokat     | Luokkien integrointiyksikkö |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina. Synkronointi takaisin Finance and Operationsiin päivittää projektiluokan Finance and Operationsissa Project Service Automationin integrointitunnuksella.

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.

> [!NOTE]
> Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
