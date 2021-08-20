---
title: Myyntitilauksen luominen määritettävälle tuotteelle
description: Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f128518af01911a29ae297670883ef425f9117d65cc952cc1ffdb044c4ce085f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781899"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Myyntitilauksen luominen määritettävälle tuotteelle

[!include [banner](../../includes/banner.md)]

Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen. Tämä esimerkki käyttää USMF-yrityksen demotietojen kaiutinmallia D0006. Nämä toimet suorittaa yleensä myyntitilausten käsittelijä.

## <a name="create-a-sales-order"></a>Luo myyntitilaus

1. Valitse **Myynti ja markkinointi \> Työtilat \> Myyntitilausten käsittely ja kysely**.
1. Valitse **Uusi**.
1. Valitse **Myyntitilaus**.
1. Valitse **Asiakastili**-kentässä *US-001*. 
1. Valitse **OK**.
1. Valitse **Nimikkeen numero** -kentässä *D0006*.
    * Tätä tehtävää varten on valittava määritettävissä oleva tuote.  
1. Valitse **Tuote ja toimitus**.
1. Valitse **Konfiguroi rivi**.
    * Huomaa, että hinta on muuttunut valitun konfiguraation perusteella, ja **Kaapeli mukana** -kenttä on nyt arvoltaan *Tosi*.  
    * Pidä mielessä oletushinta ja kaapelille valitut asetukset.  
1. Valitse **Kuormamalli**.
    * Tässä esimerkissä näytetään, miten voit käyttää mallia esimääritetyn konfiguraation valinnassa. Jos käytät tätä menettelyä tehtäväoppaana ja haluat nähdä käytettävissä olevat määritearvot, paina **Poista lukitus** -painiketta.  
1. Valitse **OK**.
1. Valitse **OK**.
1. Laajenna **Rivin erittely** -osa.
1. Valitse **Tuote**-välilehti.
    * Nimikkeen konfigurointi näytetään nyt tuotedimensioissa.  
1. Sulje sivu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]