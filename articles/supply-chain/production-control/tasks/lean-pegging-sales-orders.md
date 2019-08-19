---
title: Lean-tarvekohdistus myyntitilauksista
description: Tässä menettelyssä käsitellään sellaisen myyntirivin tarvekohdistuspuuta, jossa nimike tuotetaan kanbanien avulla.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90032539d59b310cb2d4c1324312eac6593fba6b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843597"
---
# <a name="lean-pegging-from-sales-orders"></a>Lean-tarvekohdistus myyntitilauksista

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään sellaisen myyntirivin tarvekohdistuspuuta, jossa nimike tuotetaan kanbanien avulla. Tarvekohdistuspuun vahvistamisen jälkeen kaikki kanban-työt on suunniteltu. Tämä on kätevää tilausskenaarioissa, joissa tilauksen vastaanottajan on varmistettava, että tuotanto voi alkaa heti. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu Lean-yrityksen ennakkotilausten vastaanottajille.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Luo kanban-ohjatun nimikkeen myyntitilaus
1. Siirry Kaikki myyntitilaukset -kohtaan.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
    * Käytä arvoa US-001.  
4. Valitse OK.
5. Kirjoita Nimiketunnus-kenttään L0001.
6. Valitse määräksi 30.
    * On tärkeää, että määrä on suurempi kuin 24, jotta tapahtuman kanban-sääntö käynnistyy.  

## <a name="open-a-pegging-tree"></a>Avaa tarvekohdistuspuu 
1. Valitse Tuote ja toimitus.
2. Valitse Näytä tarvekohdistuspuu.
    * Huomaa, että kaikki myyntitilausrivin tarvitsemat tarvekohdistustasot näkyvät tarvekohdistuspuussa. Tässä tapauksessa näkyvissä on kaksi kanban-tasoa ja kaikki pakolliset komponentit.  

## <a name="plan-the-pegging-tree"></a>Suunnittele tarvekohdistuspuu
1. Valitse puussa Myyntirivi 000832\Kanban 000558.
2. Laajenna Kanban-työt-osa.
    * Huomaa, että kanban-työn tila on Ei suunniteltu.  
3. Valitse Suunnittele koko tarvekohdistuspuu.
    * Tällöin kaikki kanban-työt suunnitellaan tarvekohdistuspuussa, mikä muuttaa työn tilan Ei suunniteltu tilaksi Suunniteltu.  
4. Päivitä sivu.
    * Huomaa, että kanban-työn tila muuttui ei suunnitellusta suunnitelluksi.  
5. Valitse puussa Myyntirivi 000832\Kanban 000558\Varasto-otto L0001\Kanban 000559.
    * Myös toisen kanbanin työ on suunniteltu, koska koko tarvekohdistuspuu on suunniteltu. Huomaa, että kanban-työn tila on muuttunut ei suunnitellusta suunnitelluksi.  

