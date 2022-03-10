---
title: Suorita kanban-prosessin töitä
description: Nämä toimet keskittyvät kanban-prosessitöiden suorittamiseen.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566576"
---
# <a name="execute-kanban-process-jobs"></a>Suorita kanban-prosessin töitä

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]