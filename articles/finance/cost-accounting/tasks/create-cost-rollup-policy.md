---
title: Kustannusten koontikäytännön luominen
description: Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50a50dc359dc4c2741ac4d280a9f97c6a7f2c259
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810012"
---
# <a name="create-a-cost-rollup-policy"></a>Kustannusten koontikäytännön luominen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan. Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USP2.


## <a name="create-a-policy"></a>Käytännön luominen
1. Valitse Kustannuslaskenta > Käytännöt > Kustannusten koontikäytännöt.
2. Valitse Uusi.
3. Kirjoita arvo Käytännön nimi -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.
    * Valitse Kustannusten koonnin CC.  
6. Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.
    * Valitse Kustannusten koonnin CC.  
7. Valitse Tallenna.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Käytännön sääntöjen luominen
1. Valitse Uusi.
2. Merkitse valittu rivi luettelossa.
3. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
    * Valitse 007.  
4. Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.
    * Valitse Kustannusten koonnin CE.  
5. Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.
    * Tässä esimerkissä määritetään toissijaisen kustannustason CC-007 ja kustannuspaikan vastaavuus.  
6. Valitse Uusi.
7. Merkitse valittu rivi luettelossa.
8. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
    * Valitse 008.  
9. Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.
    * Valitse Kustannusten koonnin CE.  
10. Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.
    * Tässä esimerkissä määritetään toissijaisen kustannustason CC-008 ja kustannuspaikan vastaavuus.  
11. Valitse Uusi.
12. Merkitse valittu rivi luettelossa.
13. Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.
    * Valitse 009.  
14. Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.
    * Valitse Kustannusten koonnin CE.  
15. Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.
    * Tässä esimerkissä määritetään toissijaisen kustannustason CC-009 ja kustannuspaikan vastaavuus.  
    * Jatka, kunnes kaikkien kustannuspaikkojen ja niiden vastaavien toissijaisten kustannustasojen vastaavuus on määritetty.  
16. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]