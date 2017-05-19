---
title: Taseen talousraportit
description: "Tässä artikkelissa kuvataan taseiden oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1e5d04c7baacab33c5a20a59aea8209f9c638aec
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="balance-sheet-financial-reports"></a>Taseen talousraportit

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan taseiden oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin. 

<a name="default-balance-sheet-reports"></a>Oletustaseraportit
-----------------------------

Oletustaseraportteja on kaksi. Osat on pinottu yhteen raporttiin. Osat ovat rinnakkain raportissa.

| Oletusraportti                       | Toiminnot                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Tase – oletus              | Määrittää organisaation vuoden rahoitusaseman näkymän.                                                                 |
| Tase rinnakkain – oletus | Määrittää organisaation vuoden rahoitusaseman näkymän. Käyttöomaisuus, velat ja osakkeenomistajien oma pääoma ovat rinnakkain. |

## <a name="building-blocks"></a>Rakenneosat
Taseen talousraporteissa käytetään seuraavia rakenneosia.

| Oletusraportti                       | Rivimääritys                       | Sarakemääritys             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Tase - oletusarvo              | Tase - oletusarvo              | Vuoden alusta ja varianssi - oletusarvo    |
| Tase rinnakkain – oletus | Tase rinnakkain – oletus | Vuoden alusta -sarake - oletusarvo |

### <a name="row-definition"></a>Rivimääritys

Molempien taseraporttien rivimääritykset sisältävät osia kunkin perinteisen taseen osista. Rinnakkainen raportti sisältää sarakkeen vaihdon, jolloin velat ja omistajan oma pääoma näkyvät käyttöomaisuuden vieressä. Päätilin luokan dimensiota käytetään molempien rivimääritysten muodostamisessa. Tämän vuoksi kuka tahansa voi luoda raportteja ilman muutosten tekemistä.

### <a name="column-definition"></a>Sarakemääritys

Sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.

-   **Vuoden alusta ja varianssi – oletussaraketyypit:**
    -   **DESC** – rivimäärityksen kuvaus
    -   **FD** – kuluvan vuoden taloushallinnon tiedot vuoden alusta
    -   **FD** – edellisen vuoden taloushallinnon tiedot vuoden alusta
    -   **CALC** – varianssi, kun kuluva vuosi vähennetään edellisestä vuodesta

<!-- -->

-   **Vuoden alusta -sarake – oletusarvo**
    -   **DESC** – rivimäärityksen kuvaus
    -   **FD** – kuluvan vuoden taloushallinnon tiedot vuoden alusta

 

<a name="see-also"></a>Lisätietoja
--------

[Taloushallinnan raportointi](financial-reporting-getting-started.md)

[Näytä raportit](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](http://blogs.msdn.com/b/dynamics_financial_reporting/)




