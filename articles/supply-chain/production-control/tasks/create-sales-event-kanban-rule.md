---
title: Luo myyntitapahtuman kanban-sääntö
description: Tässä menettelyssä käsitellään asetuksia, joita tarvitaan myyntitilauksen luonnin aikana käynnistettävän kanban-säännön luomiseen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cd2b579e542b9f905fc51b63f2120e5a5c883ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566644"
---
# <a name="create-a-sales-event-kanban-rule"></a>Luo myyntitapahtuman kanban-sääntö

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään asetuksia, joita tarvitaan myyntitilauksen luonnin aikana käynnistettävän kanban-säännön luomiseen. Tapahtuman kanban-sääntö täydentää myyntitilausriveiltä lähtevät vaatimukset. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Se on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.




## <a name="create-a-new-kanban-rule"></a>Luo uusi kanban-sääntö
1. Valitse Kanban-säännöt.
2. Valitse Uusi.
3. Valitse Täydennysstrategia-kentässä Tapahtuma.
    * Tapahtuman valitseminen tarkoittaa, että tapahtuma, kuten myyntitilausrivin luonti, käynnistää kanban-säännön.   Tätä käytetään alueilla, jossa kunkin kanbanin pitäisi kattaa tietty tarve.  
4. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Valitse Lopullinen kokoonpano.  
5. Laajenna Tiedot-osa.
6. Anna tai valitse Tuote-kentässä arvo.
    * Valitse L0050.  

## <a name="define-an-event"></a>Määritä tapahtuma
1. Laajenna Tapahtumat-osa.
2. Valitse Myyntitapahtuma-kentässä Automaattinen.
    * Kun automaattinen myyntitapahtuma valitaan, tämä kanban-sääntö käynnistetään automaattisesti, kun myyntirivi vastaa tuotetta ja vastaanottosijaintia. Tässä menettelyssä tuote L0050 on varastossa 13.  
3. Määritä tapahtuman vähimmäismääräksi 50.
    * Kun tapahtuman vähimmäismäärä on 50, vain tapahtumat, joiden määrä on vähintään 50, käynnistävät kanban-säännön.  
4. Laajenna Tuotantovirta-osa.
    * Huomaa, vastaanottosijainti on varasto 13. Tämä tarkoittaa, että kanban-sääntö käynnistetään tässä sijainnissa.  
    * Tässä esimerkissä myyntirivi tuotteelle L0050, jonka määrä varastossa 13 on vähintään 50, käynnistää tämän kanban-säännön.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Luo tapahtuman kanban-säännön käynnistävä myyntirivi
1. Siirry Kaikki myyntitilaukset -kohtaan.
    * Varoitus näytetään, kun kanban-sääntö tallennetaan, joten kanbanit luodaan reaaliaikaisesti myyntitilauksen luonnin aikana.  
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
    * Valitse esimerkiksi arvo US-003.  
4. Valitse OK.
5. Kirjoita Nimiketunnus-kenttään L0050.
6. Kirjoita Toimipaikka-kenttään 1.
    * Valitse toimipaikka 1, koska varasto 13 on toimipaikassa 1.  
7. Anna tai valitse Varasto-kentässä arvo.
    * Määritä Varasto-arvoksi 13.  
8. Valitse määräksi 75.
    * Anna määräksi vähintään 50, jotta luotu kanban-sääntö luodaan.  

## <a name="verify-that-kanban-is-created"></a>Varmista, että kanban on luotu
1. Valitse Tuote ja toimitus.
2. Valitse Näytä tarvekohdistuspuu.
    * Huomaa, että luotavalla kanbanilla on sama määrä kuin myyntirivillä. Näet myös mitä materiaaliottoja L0050:n tuotantoon tarvitaan. Tämä on tämän menettelyn viimeinen vaihe.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]