---
title: Kanban-töiden ajoitus
description: Tässä menettelyssä keskitytään tietyn työsolun aikataulutusprosessin kanban-töihin.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30f7c431b3d27a534e53540c41768ea55c8dd39f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222798"
---
# <a name="schedule-kanban-jobs"></a>Kanban-töiden ajoitus

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä keskitytään tietyn työsolun aikataulutusprosessin kanban-töihin. Valmistele kanban-työn kun materiaalit eivät ole käytettävissä työsolulle -menettely on tämän menettelyn luomisen edellytys. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä tehtävä on tarkoitettu työnohjauksen esimiehelle ja tuotannon suunnittelijalle, jotka käsittelevät kanbaneita.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Työsolun kanban-töiden valitseminen
1. Siirry kohtaan Tuotannonhallinta > Kanban > Kanban-työn aikataulutus.
2. Laajenna Kauden kapasiteetti -tietokenttä.
    * Laajenna Kanban-tietoruutu.  
3. Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.
4. Merkitse valittu rivi luettelossa.
    * Valitse työsolu 1250. Nyt näkymä suodatetaan niin, että se näyttää vain työsolun 1250 työt.  
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Klikkaa Valitse.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Kanban-työn aikatauluttaminen ensimmäiselle käytettävissä olevalle kaudelle
1. Merkitse valittu rivi luettelossa.
    * Valitse luettelon ensimmäinen rivi, jonka tila on Ei suunniteltu. Työn tila -kentän pisteviivakuvake osoittaa, että tila on Ei suunniteltu.  
2. Valitse Aikatauluta.
    * Tämä aikatauluttaa kanban-työn ensimmäisellä käytettävissä olevalla kaudella.  
    * Huomioi, että kanban-työ siirretään luettelon loppuun, koska se on lisätty tänään alkavalle kaudelle.  
    * Jos kuluvasta päivästä alkava kausi on kokonaan varattu, työ siirretään ensimmäiseen käytettävissä olevaan kauteen.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Kahden kanban-työn aikatauluttaminen tietylle päivälle
1. Valitse luettelosta rivi 1.
    * Ensimmäisen rivin Työn tila -kentässä tulisi olla Ei suunniteltu -tila.  
2. Valitse luettelosta rivi 2.
    * Toisen rivin Työn tila -kentässä tulisi olla Ei suunniteltu -tila. Nyt kaksi ensimmäistä työtä on valittu.  
3. Avaa valintaikkuna valitsemalla Aikataulun alkupäivä.
4. Valitse Ohita kapasiteetin puutteen aiheuttama reaktio -ruutu tai poista sen valinta.
    * Tämän asetuksen avulla voit korvata kapasiteetin puutteen aiheuttaman oletusreaktion.  
5. Valitse Kapasiteetin puutteen aiheuttama reaktio -kentässä Lisää pyydetty kausi.
    * Tämä asetus varmistaa, että työ lisätään pyydetylle kaudelle myös silloin, jos työsolu on ylikuormittunut.  
6. Valitse Aikatauluta.
    * Huomioi myös se, että molemmat työt lisätään haluttuun kauteen.  
    * Kauden kapasiteetti -osassa näkyy kunkin kauden kuormitus. Kulutus-kentässä näkyy tämän kauden suunniteltu kulutus. Jos suunniteltu kulutus on korkeampi kuin tämän kauden käytettävissä oleva kapasiteetti, valitaan ylikuormitettu kulutus.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]