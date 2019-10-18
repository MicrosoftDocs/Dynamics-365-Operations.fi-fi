---
title: Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Microsoft Dynamics 365 Financen ja Dynamics 365 Project Service Automationin välillä.
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
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250504"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 Financein ja Dynamics 365 Project Service Automationin välillä.

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytettävissä versiossa 8.0.
> - Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.
> - Jos käytät Enterprise edition -versiota 7.3.0 sen jälkeen, kun KB 4132657 ja KB 4132660 on asennettu, voit käyttää malleja integroidaksesi projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittääksesi toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Tiedonkulku Project Service Automation ja Financen välillä

Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin kulutapahtumaluokkia koskevan tiedonkulun Project Service Automationin ja Financen välillä.

Jos projektin kululuokkia hallitaan Financesta, integrointi tapahtuu ensin Financesta Project Service Automationiin. Projektin kustannusluokkien integraatiotunnukset päivitetään sitten synkronoinnin avulla Project Service Automationista Financeen.

Jos projektin kululuokkia hallitaan Project Service Automationista, integrointi tapahtuu ensin Project Service Automationista Financeen. Projektiluokkien on oltava määritettynä Financessa ennen synkronointia Project Service Automationista. Synkronoi tiedot sitten Financesta takaisin Project Service Automationiin ja sitten uudelleen Project Service Automationista Financeen. Tällöin voit varmistua, että kategoriat on linkitetty eikä kaksoiskappaleita luoda.

> [!NOTE]
> Tavallisesti projektin kululuokkia hallitaan Financessa. Jos näin ei kuitenkaan ole tai kululuokat on jo luotu Project Service Automationissa, synkronoi ensin käyttämällä projektin kulutapahtumaluokkien mallia (PSA:sta Fin and Opsiin). Synkronoi käyttämällä Project expense transactionin kategoriatemplaattia (Fin ja Ops PSA). Sinun tulisi suorittaa synkronointi Project Service Automationista Financeen vielä kerran.
>
> Jos synkronoit ensin Project Service Automationista, Financen täytyy täyttää seuraavat vaatimukset ennen kuin synkronointi suoritetaan:
>
> - Jaetun kategorian, joka vastaa projektikategoriaa, joka on Project Service Automationissa täytyy olla olemassa ja sen pitää olla käytössä sekä kohdissa **Projekti** että **Kulu**.
> - Jokaisella integroitavalla Finance-yrityksellä täytyy olla seuraavat projektiluokat:
>
>     - **Projektikategoria** on olemassa. 
>     - **Käytä kuluissa** on käytössä.
>     - **Aktiivinen kirjauskansiossa** on käytössä.
>     - **Transaktiotyyppi** on **Kulu**.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Project Service Automationin ja Financen välisen integroinnin tiedonkulku](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projektin kululuokkien synkronointi Financesta Project Service Automationiin

### <a name="template-and-task"></a>Malli ja tehtävä

Saat mallin käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Financesta Project Service Automationiin:

- **Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (Fin and Opsista PSA:han)
- **Projektin tehtävän nimi:** luokkien synkronointi PSA:han

### <a name="entity-set"></a>Yksikköjoukko

| Myyntitiedot                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Luokkien integrointiyksikkö | Tapahtumaluokat     |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin kululuokkia tietoja hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.

### <a name="power-query"></a>Power Query

Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Query for Excelillä, kun synkronointi tehdään Project Service Automationiin. Projektin kulutapahtumaluokkien malli (Fin and Opsista PSA:han) tarjoaa oletussarakkeen ja yhdistämismäärityksen. Jos luot oman mallin, ehtosarake on lisättävä Power Queryssä. Noudata näitä ohjeita.

1. Avaa projektikustannusluokkatehtävän kartoitus napsauttamalla nuolta projektin kulukirjausmallissa (Fin ja Ops to PSA).
2. Napsauta **Kyselyn ja suodatuksen lisäasetukset** avataksesi Power Queryn.
2. Valitse **Lisää ehtosarake**.
3. Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**.
4. Anna seuraava ehto: **jos CATEGORYID ei sama kuin tyhjäarvo sitten 19235001, muuten tyhjäarvo**.
5. Valitse sarakkeessa **OK**.
6. Varmista, että yhdistät tämän uuden sarakkeen yhdistämismäärityssivulla.

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Financesta Project Service Automationiin synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projektin kululuokkien synkronointi Project Service Automationista Financeen

### <a name="template-and-task"></a>Malli ja tehtävä

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Project Service Automationista Financeen:

- **Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (PSA to Fin and Ops:iin)
- **Projektin tehtävän nimi:** luokkien synkronointi Fin Ops:iin

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Myyntitiedot                           |
|----------------------------|-----------------------------------|
| Tapahtumaluokat     | Luokkien integrointiyksikkö |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin kululuokkia tietoja hallitaan Financessa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina. Synkronointi takaisin Financeen päivittää projektiluokan Financessa Project Service Automationin integrointitunnuksella.

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.

> [!NOTE]
> Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
