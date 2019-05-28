---
title: Taseen talousraportit
description: Tässä artikkelissa kuvataan taseiden oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff778af1bb3af3a10132ab3193ad1cd5daa24e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567326"
---
# <a name="balance-sheet-financial-reports"></a>Taseen talousraportit

[!include [banner](../includes/banner.md)]

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



<a name="additional-resources"></a>Lisäresurssit
--------

[Talousraportointi](financial-reporting-getting-started.md)

[Raporttien näyttäminen](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](http://blogs.msdn.com/b/dynamics_financial_reporting/)



