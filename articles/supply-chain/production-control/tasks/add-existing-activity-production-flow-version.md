---
title: Aiemmin luodun tehtävän lisääminen tuotantovirran versioon
description: Kun luot uusia tuotantovirtojen versioita, voit lisätä aiemmille versioille luotuja tehtäviä uuteen versioon.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c01d988469ead4ab09d69b1cb6e2f9b417080c69
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149409"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Aiemmin luodun tehtävän lisääminen tuotantovirran versioon

[!include [banner](../../includes/banner.md)]

Kun luot uusia tuotantovirtojen versioita, voit lisätä aiemmille versioille luotuja tehtäviä uuteen versioon. Tässä menettelyssä kuvataan, miten vanhalle tuotantovirralle luodaan uusi versio ilman, että tehtäviä kopioidaan. Vanha tehtävä lisätään uuteen versioon seuraavassa vaiheessa. 

Tämän tehtävän edellytyksenä on tuotantovirran versio ja olemassa olevat tehtävät.


## <a name="create-a-new-production-flow-version"></a>Luo uusi tuotantovirran versio
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Muokkaa.
5. Merkitse valittu rivi luettelossa.
6. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
    * Huomaa, että ennen kuin luot uuden tuotantovirran version, varmista aktiivisen version vanhentumispäivämäärä ja -aika. Uudelle versiolle luodaan voimaantulon aloituspäivä, joka liittyy valitun version erääntymispäivään.  
7. ValitseLisää.
8. Valitse Kopioi versiosta -kentässä Ei.
    * Valitse Ei, jos haluat aloittaa tyhjällä versiolla, jos suurin osa kopioidun version tehtävistä korvataan uusilla tehtävillä. Lisää muuttumattomat tehtävät manuaalisesti Lisää aiemmin luotu -toimintoon aktiviteettilomakkeella.  
9. Valitse Kanban-sääntöjen kaksoiskappaleet -kentässä Ei.
    * Kun tehtäviä ei kopioida uuteen versioon, kanban-sääntöjä ei voi kopioida samalla, kun uusi versio luodaan.   Käytät sen sijaan Luo korvaava kanban -toimintoa myöhemmin kanban-säännön lomakkeella korvataksesi vanhan tuotantovirran version kanban-säännöillä, jotka perustuvat uuden version tehtäviin.  
10. Valitse OK.
11. Etsi haluamasi tietue luettelosta ja valitse se.

## <a name="add-an-existing-activity"></a>Lisää aiemmin luotu tehtävä
1. Valitse Tehtävät.
2. Avaa valintaikkuna valitsemalla Lisää aiemmin luotu.
    * Etsi ja valitse uuteen tuotantovirran versioon lisättävä vanha tehtävä.  Huomaa, että luettelossa näkyvät kaikki ne tehtävät, jotka on luotu tämän tuotantovirran kaikkia aiempia versioita varten.  
3. Syötä tai valitse arvo Tehtävä-kenttään.
4. Valitse OK.

