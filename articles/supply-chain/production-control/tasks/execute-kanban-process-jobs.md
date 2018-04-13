--- 
title: "Suorita kanban-prosessin töitä"
description: "Nämä toimet keskittyvät kanban-prosessitöiden suorittamiseen."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 752eab976f740606154d416678ba2381641697df
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="execute-kanban-process-jobs"></a>Suorita kanban-prosessin töitä

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Nämä toimet keskittyvät kanban-prosessitöiden suorittamiseen. Ensimmäinen työ on valmis, määrä on odotettu, eikä virheitä ole. Toinen työ valmistuu, mutta siinä on virheitä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu koneenkäyttäjille.


## <a name="select-a-kanban-job"></a>Valitse kanban-työ.
1. Siirry kohtaan Tuotannonhallinta > Kanban > Prosessitöiden kanban-taulu.
2. Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.
3. Napsauta riviä, jonka resurssiryhmä on 1250. Työluettelo suodatetaan niin, että se näyttää vain työsolun 1250 työt.
    * Valitse rivi, jonka työn tila on Suunniteltu.  

## <a name="complete-a-job-with-expected-quantity"></a>Viimeistele työ odotetulla määrällä
1. Laajenna tai tiivistä Tiedot-osa.
    * Tässä osassa näkyy tärkeitä tietoja kortin numerosta, nimiketunnuksesta, tilatusta määrästä ja tehtävän nimestä.  
2. Laajenna tai tiivistä Tuotanto-ohjeet-osa.
    * Tässä osassa näytetään tehtävän tuotanto-ohjeet. Ohjeet voivat olla tekstiä, kuvia, piirroksia tai muita asiakirjoja.  
3. Valitse Käynnistys.
    * Valitse työ, joka ei ole valmis. Näet työn tilan Työn tila -kentän tilakuvakkeista.      
4. Valitse Valmis.
    * Työ on valmis ja sen laatu vastaa odotuksia.  

## <a name="complete-a-job-with-errors"></a>Viimeistele työ virheettömänä
1. Valitse Käynnistys.
    * Kun työ valmistuu, luettelon seuraava työ valitaan automaattisesti. Tämän vuoksi sinun ei tarvitse valita työtä, ennen kuin napsautat Aloita-painiketta.  
2. Valitse toimintoruudussa Valmista.
3. Napsauta Valmis (tiedot).
4. Merkitse valittu rivi luettelossa.
5. Syötä numero Virhemäärä-kenttään.
6. Lisää Hyväksytty määrä -kenttään numero.
7. Valitse OK.


