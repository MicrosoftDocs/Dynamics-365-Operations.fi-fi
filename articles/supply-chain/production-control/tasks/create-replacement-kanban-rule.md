---
title: Luo korvaava kanban-sääntö
description: Tämän menetelmä keskittyy korvaamaan vanhoja kanban-sääntöjä uusilla säännöillä tiettynä päivämääränä.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8a9367d4796999857e473bcbe36a709d534f3b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564060"
---
# <a name="create-a-replacement-kanban-rule"></a>Luo korvaava kanban-sääntö

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämän menetelmä keskittyy korvaamaan vanhoja kanban-sääntöjä uusilla säännöillä tiettynä päivämääränä. Tästä on hyötyä, kun muutoksia tuotantovirtaan tai täydennyssääntöihin on koordinoitava ja ajoitettava. Tämän menettelyn luonnissa käytettiin esittely-yrityksenä USMF-yritystä. Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle muutetun tuotantovirran tai uuden täydennyssäännön tuotannon valmisteluun. Tämän tehtävä korvaa kanban-säännön 000022 uudella säännöllä ja nostaa enimmäismäärän 48:sta 100:an uudessa säännössä.


## <a name="select-a-kanban-rule-to-replace"></a>Valitse korvattava kanban-sääntö
1. Valitse Kanban-säännöt.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse kanban-sääntö 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Luo korvaava kanban-sääntö
1. Napsauta kohtaa Korvaa kanban-sääntö.
2. Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.
    * Valitse tuleva päivämäärä, esimerkiksi viikon kuluttua. Tämä on päivämäärä ja aika, jona uusi kanban-sääntö aktivoituu ja korvaa vanhan kanban-säännön.  
    * Jos kanban-sääntö muuttaa polkua tuotantovirrassa, toisen tehtävän voi valita.  Näissä toimintaohjeissa on tehtävää ei muuteta.  
3. Valitse OK.
    * Huomaa, että kanban-sääntö 000022 korvataan uudella kanban-säännöllä.  
    * Voimaantulopäivä määritetään kanban-sääntöä korvatessa valitun päivämäärän mukaan.  
4. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse korvattu kanban-sääntö 000022.  
    * Huomaa, että korvatulla kanban-säännöllä on sama päivämäärä kuin päättymispäivämäärä, sillä tämä on päivämäärä, jona se vanhenee.  
5. Valitse luettelosta rivi 1.
    * Valitse uusi kanban-sääntö luettelon alusta. Tällä kanban-säännölle on suurin kanban-säännön numero.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Avaa kanban-sääntö napsauttamalla sen numeroa.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Muokkaa korvaavan kanban-säännön enimmäismäärää
1. Määritä Enimmäismäärä-arvoksi 100.
    * Laajenna Määrät-pikavälilehti nähdäksesi Suurin määrä -kentän. Jos muutat enimmäismääräksi 100, voit käsitellä enintään 100:a kanbania.    Tämä on tämän tehtävän viimeinen vaihe.  

