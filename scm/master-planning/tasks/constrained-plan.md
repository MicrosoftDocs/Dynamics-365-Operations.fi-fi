--- 
title: Rajoitetun suunnitelman luominen
description: "Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset."
author: YuyuScheller
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6735f0287e7a61ff494a48c97c44480c6038097c
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-constrained-plan"></a>Rajoitetun suunnitelman luominen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset. Suunnitelma varmistaa, että valmistus aloitetaan vasta sitten, kun materiaalit ovat käytettävissä. Se myös estää resurssien ylivaraamisen. 

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu tuotannon suunnittelijalle.


## <a name="set-up-a-constrained-plan"></a>Rajoitetun suunnitelman määrittäminen
1. Valitse Pääsuunnittelu.
2. Valitse Pääsuunnitelmat.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Esimerkki: StaticPlan  
4. Valitse Rajallinen kapasiteetti -kentässä Kyllä.
5. Syötä Rajallisen kapasiteetin aikaraja -kenttään 30.
6. Laajenna Päivät-osan aikarajat.
7. Valitse Kapasiteetti-kentässä Kyllä.
8. Syötä Kapasiteetin aikataulutuksen aikaraja (päivää) -kenttään numero.
    * Esimerkki: 60  
9. Valitse Lasketut viiveet -kentässä Kyllä.
10. Syötä Laskettujen viiveiden aikaraja (päivää) -kenttään numero.
    * Esimerkki: 60  
11. Laajenna Lasketut viiveet -osa.
12. Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.
13. Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.
14. Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.
15. Sulje sivu.

## <a name="create-a-constrained-plan"></a>Rajoitetun suunnitelman luominen
1. Valitse Suorita.
2. Syötä tai valitse arvo Pääsuunnitelma-kentässä.
    * Valitse suunnitelma, jolle määritit rajoitukset.  
3. Valitse OK.
    * Tämä saattaa kestää jonkin aikaa.  
4. Valitse Suunnitellut tilaukset.


