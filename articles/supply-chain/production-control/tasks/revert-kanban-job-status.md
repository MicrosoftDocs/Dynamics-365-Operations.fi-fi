---
title: Palauta kanban-työn tila
description: Tässä menettelyssä käsitellään virheellisen kanban-työtilan palauttamista.
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
ms.openlocfilehash: 771c3b95be05904c84483473a533c708964fbe62
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574398"
---
# <a name="revert-kanban-job-status"></a>Palauta kanban-työn tila

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]