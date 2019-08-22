---
title: Rajoitetun suunnitelman luominen
description: Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845287"
---
# <a name="generate-a-constrained-plan"></a>Rajoitetun suunnitelman luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

