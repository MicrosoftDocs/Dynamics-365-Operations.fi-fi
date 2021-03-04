---
title: Luo kanban-sääntö usealle tehtävälle
description: Seuraavassa menettelyssä kuvataan, miten luot kanban-säännön, joka sisältää useita tuotantovirran toimenpiteitä.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68cac0f581e786cdb3801e03fb60db7bc05ffb2f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426792"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Luo kanban-sääntö usealle tehtävälle

[!include [banner](../../includes/banner.md)]

Seuraavassa menettelyssä kuvataan, miten luot kanban-säännön, joka sisältää useita tuotantovirran toimenpiteitä. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun lean-ympäristössä.


## <a name="create-a-new-kanban-rule"></a>Luo uusi kanban-sääntö
1. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
2. Valitse Uusi.
3. Valitse Täydennysstrategia-kentässä Ajoitettu.
4. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Valitse SpeakerAssemblyAndPolish.  
5. Valitse useiden tehtävien valintaruutu.
    * Kanban-sääntöön on tarkoitus sisällyttää useampi kuin yksi tehtävä. Valitset polun tuotantovirrassa, kun valitset viimeisen suunnitelman tehtävän.  
6. Anna tai valitse Viimeinen suunnitelman tehtävä -kentässä arvo.
    * Valitse SpeakerTestAndPackaging. Sivu aukeaa automaattisesti, kun olet valinnut arvon. Valitse kanban-työnkulku SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Valitse OK.  
7. Laajenna Tiedot-osa.
8. Anna tai valitse Tuote-kentässä arvo.
    * Valitse nimike L0006.  

## <a name="create-kanban-and-view-jobs"></a>Luo kanban ja näytä työt
1. Laajenna Kanbanit-osa.
2. ValitseLisää.
3. Syötä Uusien kanbanien määrä -kenttän arvoksi "1".
    * Tämä luo yhden kanbanin.  
4. Määritä tuotemääräksi 3.
    * Kanban käsittelee 3 tuotetta.  
5. Syötä päivämäärä ja kellonaika Eräpäivä/-kellonaika -kenttään.
    * Voit antaa arvoksi Tänään.  
6. Valitse Luo.
7. Valitse Erittely.
    * Huomaa, että kanbanilla on kaksi tuotantovirran prosessityötä. Ensimmäinen on SpeakerAssemblyAndPolish ja toinen SpeakerTestAndPackaging.  
    * Tämä on viimeinen vaihe!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]