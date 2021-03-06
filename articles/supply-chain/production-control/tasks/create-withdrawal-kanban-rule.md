---
title: Luo oton kanban-sääntö
description: Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adbcdbb2d278b25dce1d8c027e66367e9c0930e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828823"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Luo oton kanban-sääntö

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]