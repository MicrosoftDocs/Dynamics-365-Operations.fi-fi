---
title: Myyntitilauksen luominen määritettävälle tuotteelle
description: Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882198bf07233867b54579b986f93f5c1b46c1b6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564198"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Myyntitilauksen luominen määritettävälle tuotteelle

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen. Tämä esimerkki käyttää USMF-yrityksen demotietojen kaiutinmallia D0006. Nämä toimet suorittaa yleensä myyntitilausten käsittelijä.


## <a name="create-a-sales-order"></a>Luo myyntitilaus
1. Valitse Myyntitilausten käsittely ja kysely.
2. Valitse Uusi.
3. Valitse Myyntitilaus.
4. Valitse Asiakastili-kentässä US-001. 
5. Valitse OK.
6. Valitse Nimiketunnus-kenttään D0006.
    * Tätä tehtävää varten on valittava määritettävissä oleva tuote.  
7. Valitse Tuote ja toimitus.
8. Napsauta Konfiguroi rivi.
    * Huomaa, että hinta on muuttunut valitun konfiguraation perusteella, ja Kaapeli mukana -kenttä on nyt arvoltaan Tosi.  
    * Pidä mielessä oletushinta ja kaapelille valitut asetukset.  
9. Valitse Lataa malli.
    * Tässä esimerkissä näytetään, miten voit käyttää mallia esimääritetyn konfiguraation valinnassa. Jos käytät tätä menettelyä tehtäväoppaana ja haluat nähdä käytettävissä olevat määritearvot, paina Poista lukitus -painiketta.  
10. Valitse OK.
11. Valitse OK.
12. Laajenna Rivin erittely -osa.
13. Valitse Tuote-välilehti.
    * Nimikkeen konfigurointi näytetään nyt tuotedimensioissa.  
14. Sulje sivu.

## <a name="select-the-product-configuration"></a>Valitse tuotteen konfiguraatio.

