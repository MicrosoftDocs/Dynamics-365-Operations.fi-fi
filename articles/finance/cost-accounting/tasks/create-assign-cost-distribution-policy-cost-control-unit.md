---
title: Luo ja määritä kustannusten jakokäytäntö kustannusten hallinnan yksikköön
description: Kustannusten jaon sääntöjä käytetään sellaisten kustannusten jaossa, jotka on laskettu rahoituksellisesti yhteisessä kustannuspaikassa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b269c731776e26df24658feedfa301181c309a14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969275"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Luo ja määritä kustannusten jakokäytäntö kustannusten hallinnan yksikköön

[!include [banner](../../includes/banner.md)]

Kustannusten jaon sääntöjä käytetään sellaisten kustannusten jaossa, jotka on laskettu rahoituksellisesti yhteisessä kustannuspaikassa. Kustannuslaskija varmistaa, että kustannus jaetaan kustannuspaikkoihin valitun kohdistusperusteen perusteella. Käytäntö ja vastaavat säännöt delegoidaan kustannusseurantayksikölle. Tämän tehtäväoppaan esimerkissä kerrotaan, miten kustannusten jaon käytäntö ja vastaavat säännöt luodaan.


## <a name="create-a-policy"></a>Käytännön luominen
1. Valitse Kustannuslaskenta > Käytännöt > Kustannusten jaon käytännöt.
2. Valitse Uusi.
3. Kirjoita arvo Käytännön nimi -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.
    * Valitse Organisaatio.  
6. Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.
    * Valitse CDS P/L.  
7. Syötä tai valitse arvo Dimensio-kenttään.
    * Valitse Jaetut tilastoelementit.  
8. Valitse Tallenna.

## <a name="create-rules-for-the-policy"></a>Käytännön sääntöjen luominen
1. Valitse Uusi.
2. Merkitse valittu rivi luettelossa.
3. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
    * Laajenna hierarkia ja valitse 094.  
4. Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.
    * Valitse Muut käyttökustannukset ja valitse sitten 605110 Puhdistus.  
5. Valitse vaihtoehto Kustannustoiminta-kentässä.
    * Valitse Kiinteä kustannus.  
6. Anna tai valitse arvo Kohdistusperuste-kenttään.
7. Valitse Uusi.
8. Merkitse valittu rivi luettelossa.
9. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
    * Laajenna hierarkia ja valitse 094.  
10. Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.
    * Valitse Muut käyttökustannukset ja valitse sitten 605150 Vuokra.  
11. Valitse vaihtoehto Kustannustoiminta-kentässä.
    * Valitse Kiinteä kustannus.  
12. Anna tai valitse arvo Kohdistusperuste-kenttään.
13. Valitse Tallenna.

## <a name="assign-rules-to-a-cost-control-unit"></a>Sääntöjen delegoiminen kustannusseurantayksikölle
1. Valitse Kustannusseurantayksikön käytännön määritykset.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.
    * Valitse sallitun tilikauden syyskuu 1.  
5. Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.
6. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]