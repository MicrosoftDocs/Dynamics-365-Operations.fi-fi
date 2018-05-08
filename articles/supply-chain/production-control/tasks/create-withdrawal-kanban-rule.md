--- 
title: "Luo oton kanban-sääntö"
description: "Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a>Luo oton kanban-sääntö

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun materiaalin täydennyksen valmisteluun.


## <a name="create-new-kanban-rule"></a>Luo uusi kanban-sääntö
1. Valitse Kanban-säännöt.
2. Valitse Uusi.
3. Valitse Tyyppi-kentän arvoksi "Otto".
    * Otto-tyyppiä käytetään kanban-säännössä tuotteiden tai materiaalin siirtoon.  
4. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Valitse ReplenishSpeakerComponents.   Tehtävä on määritetty siirtämään komponentteja varaston 11 toimipaikasta 11 varaston 12 toimipaikkaan 12.  
5. Anna tai valitse Tuote-kentässä arvo.
    * Valitse M0007.  
6. Lisää Läpimenoaika-kenttään numero.
    * Esimerkki: 60.  
7. Anna tai valitse Mittayksikkö-kentässä arvo.
    * Esimerkiksi minuutteja.  

## <a name="set-quantities-for-kanban"></a>Määritä kanban-määrät
1. Määritä Oletusmäärä-arvoksi 5.
    * Tämä määrä siirretään kullekin kanbanille.  
2. Syötä Kiinteä kanban-määrä -kentän arvoksi 2.
    * Tämä on sellaisten kanbanien määrä, joiden pitäisi olla aktiivisia. Tällä tapauksessa jokainen 2 kanbanista siirtää 5.  
3. Lisää Vähimmäisrajan hälytys -kenttään 1.
    * Käytetään seuraamaan sellaisten täysien kanbanien vähimmäismäärää, joiden pitäisi olla päämäärässä. Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.  
4. Lisää Enimmäisrajan hälytys -kenttään 2.
    * Käytetään seuraamaan sellaisten täysien kanbanien enimmäismäärää, joiden pitäisi olla päämäärässä. Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.  

## <a name="create-kanbans"></a>Luo kanbaneita
1. Valitse Tallenna.
    * Kanban-sääntö on tallennettava ennen kanbanien luomista.  
2. ValitseLisää.
    * Huomaa, että yksikään kanban ei ole aktiivinen, koska ehdotettu Uusien kanbanien määrä on 2. Tämä vastaa Kiinteä kanban-määrä -asetusta.  
3. Valitse Luo.
    * Tämä luo kaksi kanbania.  
    * Huomaa, että tälle ottamisen kanban-säännölle luotiin 2 kanbania, joista kunkin arvo on 5.  Tämä on tämän menettelyn viimeinen vaihe.  


