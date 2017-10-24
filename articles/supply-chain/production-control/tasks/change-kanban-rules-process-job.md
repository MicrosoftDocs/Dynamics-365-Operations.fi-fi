--- 
title: "Muuta prosessityön kanban-sääntöjä"
description: "Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>Muuta prosessityön kanban-sääntöjä

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


