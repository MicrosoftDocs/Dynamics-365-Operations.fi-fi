---
title: Taseen talousraportit
description: Tässä artikkelissa kuvataan taseiden oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin.
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643820"
---
# <a name="balance-sheet-financial-reports"></a>Taseen talousraportit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan taseiden oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin. 

## <a name="default-balance-sheet-reports"></a>Oletustaseraportit

Oletustaseraportteja on kaksi. Osat on pinottu yhteen raporttiin. Osat ovat rinnakkain raportissa.

| Oletusraportti                       | Toiminnot                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| Tase – oletus              | Määrittää organisaation vuoden rahoitusaseman näkymän.                    |
| Tase ja tuloslaskelma rinnakkain – oletusarvo | Näyttää organisaation vuoden rahoitusaseman näkymän rinnakkain. |

## <a name="building-blocks"></a>Rakenneosat
Taseen talousraporteissa käytetään seuraavia rakenneosia.

| Oletusraportti                       | Rivimääritys                       | Sarakemääritys             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Tase - oletusarvo              | Tase - oletusarvo              | Vuoden alusta ja varianssi - oletusarvo    |
| Tase ja tuloslaskelma rinnakkain – oletusarvo | Tase ja tuloslaskelma rinnakkain – oletusarvo | Vuoden alusta -sarake - oletusarvo |

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



## <a name="additional-resources"></a>Lisäresurssit

[Taloushallinnon raportoinnin yleiskatsaus](financial-reporting-getting-started.md)

[Raporttien tarkasteleminen](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
