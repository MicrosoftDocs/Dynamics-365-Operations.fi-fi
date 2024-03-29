---
title: Luo oton kanban-sääntö
description: Seuraavassa menettelyssä kuvataan tarvittavat määritykset ottamisen kanban-säännön luomiseen materiaalin siirtämiseksi lean-ympäristössä.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba30e9d09e9eeb0cd7428aafc1195d6b7e7caaa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574470"
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