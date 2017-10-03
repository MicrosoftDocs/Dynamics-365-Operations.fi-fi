--- 
title: "Luo kanban-sääntö usealle tehtävälle"
description: "Seuraavassa menettelyssä kuvataan, miten luot kanban-säännön, joka sisältää useita tuotantovirran toimenpiteitä."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 5b4c6f919072dd6497b0eab548077f68fc46dbf5
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Luo kanban-sääntö usealle tehtävälle

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


