--- 
title: "Tuoterakenteen laskeminen käyttämällä monitasoista rakennetta (vain helmikuu 2016)"
description: "Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa monitasoista hajotusta."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 1ad38f67bba299bbd581aba6010b4028c91fbf3a
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Tuoterakenteen laskeminen käyttämällä monitasoista rakennetta (vain helmikuu 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa monitasoista hajotusta. Se on tuoterakenteen laskentasarjan seitsemäs tehtävä. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.

1. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tuotteen BOM_1.  
3. Valitse toimintoruudussa Hallitse kustannuksia.
4. Valitse Nimikkeen hinta.
5. Valitse Laske nimikekustannus.
    * Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.  
6. Anna tai valitse Kustannuslaskentaversio-kentässä arvo.
    * Valitse Kustannusversio 20, koska se on suunniteltu kustannustyyppi ja hajotustila on monitasoinen.   Monitasoinen hajotustila on tarkoitettu suunnitelluille kustannuksille ja simulaatioille. Sitä ei käytetä standardikustannuksille.  
7. Valitse OK.
8. Valitse Näytä laskennan tiedot.
    * Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.  Huomaa tässä tapauksessa, että BOM_2 on laskettu ottamalla huomioon raaka-aine, prosessi ja yleiskustannus, joiden yhteissumma on 29,40, eikä standardikustannuksella 10, joka aktivoitiin tämän sarjan alkuperäisessä tehtäväoppaassa.  
9. Valitse Kustannuslaskentalomake-välilehti.
    * Kun siirrytään Kustannuslaskentalomake-välilehteen kustannusryhmäkohtaiset yhteissummat poikkeavat edellisessä tehtäväoppaassa tehdyistä laskelmista.  
10. Valitse Taso-kentässä Monitasoinen.
    * Kun Monitasoinen valitaan, kustannukset luokitellaan BOM_2-kokoonpanon mukaan, jolloin 10 johdetaan M1-kustannusryhmästä (ITEM_C) ja 15,60 johdetaan sen tuotannosta, jossa kustannusryhmä on L2. Myös epäsuorat kustannukset vaihtelevat.  
11. Sulje sivu.
12. Sulje sivu.


