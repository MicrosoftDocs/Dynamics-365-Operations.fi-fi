--- 
title: "Palauta kanban-työn tila"
description: "Tässä menettelyssä käsitellään virheellisen kanban-työtilan palauttamista."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 55d359232da5f3087b1e6baed182a20da09aeff7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="revert-kanban-job-status"></a>Palauta kanban-työn tila

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään virheellisen kanban-työtilan palauttamista. Tämä on kätevää, jos koneenkäyttäjä päivittää väärän työn tai määrittää vahingossa väärän tilan. Tässä menettelyssä kanban-työ on rekisteröidään vahingossa valmistelluksi ja tila palautetaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Menettely on tarkoitettu Lean-tuotantoyrityksessä työskentelevälle tuotannon osastonvalvojalle tai koneenkäyttäjälle.


## <a name="open-process-board-for-the-work-cell"></a>Avaa työsolun prosessitaulu.
1. Siirry Prosessitöiden kanban-taulu -kohtaan.
2. Anna tai valitse Työsolu-kentässä arvo.
    * Valitse työsolu 1260.  

## <a name="prepare-kanban-job"></a>Valmistele kanban-työ
1. Valitse Valmistele.
    * Jos voi valita Valmistele, koska se näkyy harmaana, valmista, että valitun kanban-työn tila Suunniteltu, minkä osoituksena on tyhjä kanban-kuvake. Jos Valmistele epäonnistuu, varmista, että kaikki keräysluettelon materiaalit ovat käytettävissä.  
2. Valitse luettelossa valmisteltu työ.
    * Valitse ensimmäinen juuri valmisteltu työ.  
    * Huomaa, että työn tila on valmisteltu, minkä osoittaa kanban-kuvakkeen sisällä oleva kolmio.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Palauta valmistellun kanban-työn tila
1. Merkitse valittu rivi luettelossa.
    * Valitse ensimmäinen juuri valmisteltu työ.  
2. Valitse toimintoruudussa Valmista.
3. Valitse Palauta tila.
    * Voit käyttää vaihtoehtoisia kanban-sääntöjä seuraavissa tilanteissa: – Säännöillä on sama täydennysstrategia.  - Kummallakin säännöllä on sama tuotantovirran versio.  - Kummallekin säännölle annetaan sama tuote.  - Kummallekin säännölle on määritetty samat kanban-sääntöjen viimeistä tehtävää edeltävät tehtävät.  - Kummallekin säännölle on oltava määritettynä samat varastodimensiot.  - Käsittely-yksikön tilan on oltava Ei määritetty.  - Tapahtuma-kanbanin määrityksen on oltava sama.  
    * Varmista, että uusi tila on Suunniteltu.  
4. Valitse OK.
5. Poista valitun rivin merkintä luettelossa.
    * Valitse sama työ.  
    * Huomaa, että kanban-työn työtilaksi on palautettu Suunniteltu, minkä osoituksena on tyhjä kanban-kuvake.  


