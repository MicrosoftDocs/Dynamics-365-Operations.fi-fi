---
title: Luo ja määritä kustannustoimintakäytäntö kustannusten hallinnan yksikköön
description: Kustannustoiminta on sekä kiinteiden että muuttuvien kustannusten luokittelu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 110ab87586c926d719537d2c30225d1630ce7710
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969300"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Luo ja määritä kustannustoimintakäytäntö kustannusten hallinnan yksikköön

[!include [banner](../../includes/banner.md)]

Kustannustoiminta on sekä kiinteiden että muuttuvien kustannusten luokittelu. Käytäntö ja vastaavat säännöt on delegoitava kustannusseurantayksikköön, jotta käytäntö astuu voimaan. Tämän menettelyn avulla luodaan käytäntö ja delegoidaan se sitten kustannusseurantayksikköön.


## <a name="create-a-cost-behavior-hierarchy"></a>Kustannustoiminnan hierarkian luominen
1. Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.
2. Valitse Uusi.
3. Valitse Luo.
4. Kirjoita Dimensiohierarkian nimi -kenttään Kustannustoiminnan hierarkia.
5. Syötä tai valitse arvo Dimensio-kenttään.
    * Valitse Kustannustasot.  
6. Valitse Tallenna.
7. Valitse Näytä hierarkia.
8. Valitse Uusi.
9. Kirjoita arvo Solmun nimi -kenttään.
    * Syötä Kiinteä kustannus.  
10. Valitse puussa Cost behavior hierarchy.
11. Valitse Uusi.
12. Kirjoita arvo Solmun nimi -kenttään.
    * Syötä Muuttuva kustannus.  
13. Valitse Tallenna.
14. Valitse puussa Cost behavior hierarchy\Fixed cost.
15. Valitse Uusi.
16. Merkitse valittu rivi luettelossa.
17. Syötä tai valitse arvo Lähtödimension jäsen -kenttään.
    * Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.  
18. Syötä tai valitse arvo Kohdedimension jäsen -kenttään.
    * Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.  
19. Valitse puussa Cost behavior hierarchy\Variable cost.
20. Valitse Uusi.
21. Merkitse valittu rivi luettelossa.
22. Syötä tai valitse arvo Lähtödimension jäsen -kenttään.
    * Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.  
23. Syötä tai valitse arvo Kohdedimension jäsen -kenttään.
    * Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.  
24. Valitse Tallenna.

## <a name="create-the-policy-and-rules"></a>Käytännön ja sääntöjen luominen
1. Valitse Kustannuslaskenta > Käytännöt > Kustannustoiminnan käytännöt.
2. Valitse Uusi.
3. Kirjoita arvo Käytännön nimi -kenttään.
4. Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.
    * Valitse äsken luotu käytäntöhierarkia.  
5. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.
    * Valitse Organisaatio.  
6. Valitse Tallenna.
7. Valitse Uusi.
8. Merkitse valittu rivi luettelossa.
9. Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.
    * Laajenna hierarkia ja valitse Muuttuva kustannus.  
10. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
    * Oletusarvoisesti muuttuva prosenttiosuus on 100.  
11. Valitse Kustannusseurantayksikön käytännön määritykset.
12. Valitse Uusi.
13. Merkitse valittu rivi luettelossa.
14. Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.
    * Säännöillä on voimaantulopäivämäärä. Käyttäjä tai järjestelmä voi määrittää säännön vanhentuneeksi, jos säännöstä luodaan uusi versio.  
15. Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.
16. Valitse Tallenna.

