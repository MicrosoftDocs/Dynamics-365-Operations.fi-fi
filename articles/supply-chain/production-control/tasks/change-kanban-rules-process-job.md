---
title: Muuta prosessityön kanban-sääntöjä
description: Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426803"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Muuta prosessityön kanban-sääntöjä

[!include [banner](../../includes/banner.md)]

Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista. Tämä kätevää tasoitettaessa resurssien kuormitusta tai vikaantumistapauksissa. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu arvovirrasta vastaavalle Lean-tuotantoryrityksessä työskentelevälle suunnittelijalle.


## <a name="copy-kanban-rule"></a>Kopioi kanban-sääntö
1. Valitse Kanban-säännöt.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse L0001:lle tapahtuman kanban-sääntö 000022.  
3. Valitse Kanban-säännön kaksoiskappale.
4. Valitse OK.

## <a name="change-kanban-rule"></a>Vaihda kanban-sääntö
1. Sulje sivu.
2. Valitse Kanban-työn aikataulutus.
3. Merkitse valittu rivi luettelossa.
    * Valitse rivi, jossa on kanban 000177.  
4. Valitse Käytä vaihtoehtoista kanban-sääntöä.
5. Valitse Seuraava.
6. Anna tai valitse Kanban-sääntö-kentässä arvo.
    * Valitse aiemmin luotu kanban-sääntö. Tällä kanban-säännölle on suurin numero.  
7. Valitse Valmis.
    * Kanban-työ käyttää nyt toista kanban-sääntöä. Tämä on kätevää työsolujen kuormituksen tasoittamisessa.  

