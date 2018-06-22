---
title: Projektin kululuokkien synkronointi Project Service Automationista
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: fi-fi
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projektin kululuokkien synkronointi Finance and Operationsin ja Project Service Automationin välillä

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektin kululuokat synkronoidaan Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Project Service Automationin välillä.

> [!NOTE]
> Projektitehtävien integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automationin ja Finance and Operationsin tiedonkulku

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin kulutapahtumaluokkia koskevan tiedonkulun Project Service Automationin ja Finance and Operationsin välillä.

Jos projektin kululuokkia hallitaan Finance and Operationsissa, integrointi tapahtuu ensin Finance and Operationsista Project Service Automationiin. Sen jälkeen projektin kululuokkien integrointitunnukset päivitetään synkronoimalla Project Service Automationista Finance and Operationsiin.

Jos projektin kululuokkia hallitaan Project Service Automationista, integrointi tapahtuu ensin Project Service Automationista Finance and Operationsiin. Projektiluokkien on oltava määritettynä Finance and Operationsissa ennen synkronointia Project Service Automationista. Voit tämän jälkeen tehdä synkronoinnin Finance and Operationsista takaisin Project Service Automationiin ja sitten uudelleen Project Service Automationista Finance and Operationsiin. Näin varmistetaan, että luokat linkitetään ja ettei kaksoiskappaleita luoda.

> [!NOTE]
> Yleensä projektin kululuokkia hallitaan Finance and Operationsissa. Mikäli näin ei tehdä tai jos olet jo luonut kululuokat Project Service Automationin, sinun on synkronoitava ensin käyttämällä projektin kulutapahtumaluokkia (PSA:sta Fin and Opsiin) ja sitten käyttämällä projektin kulutapahtumaluokkia (Fin and Opsista PSA:han). Tämän jälkeen on tehtävä vielä kerran synkronointi PSA:sta Fin and Opsiin.

> Jos synkronointi tehdään ensin Project Service Automationista, projektiluokkien on oltava jo määritettyinä Finance and Operationsissa. Lisäksi Project Service Automationin tapahtumaluokkien kanssa synkronoitavien projektiluokkien määrityksen on oltava **Käytössä kirjauskansioissa**.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Finance and Operationsista Project Service Automationiin:

-  **Mallin nimi tietojen integroinnissa:** projektin kulutapahtumaluokat (Fin and Opsista PSA:han)
-  **Projektin tehtävän nimi:** luokkien synkronointi PSA:han

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Luokkien integrointiyksikkö    | Tapahtumaluokat        |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina.

## <a name="power-query"></a>Power Query

Tapahtumaluokan laskutustyyppi on määritettävä Microsoft Power Queryllä, kun synkronointi tehdään Project Service Automationiin. Projektin kulutapahtumaluokkien mallissa (Fin and Opsista PSA:han) on valmiina oletussarake ja yhdistämismääritys. Jos luot oman mallin, ehtosarake on lisättävä Power Queryssä.
- Avaa kyselyn ja suodatuksen lisäasetuslomake, kun yhdistät projektin kululuokkatehtävää.
- Valitse **Lisää ehtosarake**.
- Anna sarakkeelle uusi nimi, kuten Laskutustyyppi.
- Anna seuraava ehto: jos **CATEGORYID ei sama kuin tyhjäarvo sitten 19235001, muuten tyhjäarvo**.
- Valitse sarakkeessa **OK**.
- Varmista, että yhdistät tämän uuden sarakkeen yhdistämismäärityssivulle.

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Finance and Operationsista Project Service Automationiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kululuokat Project Service Automationista Finance and Operationsiin:

-**Mallin nimi tietojen integroinnissa:** Projektin kulutapahtumaluokat (PSA:sta Fin and Opsiin) - **Projektin tehtävän nimi:** Luokkien synkronointi Fin Opsiin

## <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Tapahtumaluokat          | Luokkien integrointiyksikkö  | 

## <a name="entity-flow"></a>Yksikön työnkulku

Projektin kululuokkia tietoja hallitaan Finance and Operationsissa ja ne synkronoidaan Project Service Automationiin tapahtumaluokkina. Synkronointi takaisin Finance and Operationsiin päivittää Project Service Automationin integrointitunnuksen Finance and Operationsin projektiluokassa.

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä.

> [!NOTE]
> Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

