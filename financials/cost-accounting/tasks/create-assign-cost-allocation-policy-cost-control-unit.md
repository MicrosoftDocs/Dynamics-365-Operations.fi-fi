--- 
title: "Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön"
description: "Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 82319d8d9c7b567f98dfd0e591cb99079fb577b7
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt. Tämä tallenne käyttää esittelytietojen USP2-yritystä.


## <a name="create-a-policy"></a>Käytännön luominen
1. Valitse Kustannuslaskenta > Käytännöt > Kustannusten kohdistuskäytännöt.
2. Valitse Uusi.
3. Kirjoita arvo Käytännön nimi -kenttään.
4. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.
    * Valitse Organisaatio.  
5. Syötä tai valitse arvo Dimensio-kenttään.
6. Valitse Tallenna.

## <a name="create-allocation-rules"></a>Kohdistussääntöjen luominen
1. Valitse Uusi.
2. Merkitse valittu rivi luettelossa.
3. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
4. Valitse Kustannustoiminta-kentässä Yhteensä.
5. Anna tai valitse arvo Kohdistusperuste-kenttään.
6. Valitse Uusi.
7. Merkitse valittu rivi luettelossa.
8. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
9. Valitse Kustannustoiminta-kentässä Yhteensä.
10. Anna tai valitse arvo Kohdistusperuste-kenttään.
11. Valitse Uusi.
12. Merkitse valittu rivi luettelossa.
13. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
14. Valitse Kustannustoiminta-kentässä Yhteensä.
15. Anna tai valitse arvo Kohdistusperuste-kenttään.
    * Jatka, kunnes olet luonut kaikki säännöt.  
16. Valitse Tallenna.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Käytännön delegoiminen kustannusseurantayksikköön
1. Valitse Kustannusseurantayksikön käytännön määritykset.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.
    * Säännöillä on voimaantulopäivämäärä. Käyttäjä tai järjestelmä voi määrittää säännöt vanhentuneeksi, jos säännöistä luodaan uusi versio.  
5. Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.
6. Valitse Tallenna.


