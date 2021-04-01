---
title: Tuloslaskelman talousraportti
description: Tässä artikkelissa kuvataan tuloilmoituksen oletusraporttia. Siinä myös kuvataan rakenneosat, jotka liittyvät tähän raporttiin.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fab0e9d5e550b1848c3483b3172836e258353ebb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249068"
---
# <a name="income-statement-financial-report"></a>Tuloslaskelman talousraportti

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan tuloilmoituksen oletusraporttia. Siinä myös kuvataan rakenneosat, jotka liittyvät tähän raporttiin. 

<a name="default-income-statement-report"></a>Tuloslaskelman oletusraportti
-------------------------------

| Oletusraportti             | Toiminnot                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Tuloslaskelma – oletus | Sisältää organisaation tuottavuusnäkymän sekä kuluvalle kaudelle että vuoden alusta tähän asti. |

## <a name="building-blocks"></a>Rakenneosat
Tuloslaskelman talousraportissa käytetään seuraavia rakenneosia.

| Oletusraportti             | Rivimääritys                     | Sarakemääritys          |
|----------------------------|------------------------------------|----------------------------|
| Tuloslaskelma - oletus | Yhteenvetotuloslaskelma - oletus | Kausittainen ja vuoden alusta - oletusarvo |

### <a name="row-definition"></a>Rivimääritys

Rivimääritys, yhteenvetotuloslaskelma – oletusarvo, sisältää osan perinteisen tuloslaskelman jokaiselle osalle. Päätilin luokan dimensiota käytetään tämän rivimäärityksen muodostamisessa. Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä.

### <a name="column-definition"></a>Sarakemääritys

Sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.

-   **Kausittainen ja vuoden alusta – oletussaraketyypit:**
    -   **DESC** – rivimäärityksen kuvaus
    -   **FD** – nykyisen kauden taloushallinnon tiedot
    -   **FD** – taloushallinnon tiedot vuoden alusta



<a name="additional-resources"></a>Lisäresurssit
--------

[Taloushallinnon raportoinnin yleiskatsaus](financial-reporting-getting-started.md)

[Raporttien tarkasteleminen](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]