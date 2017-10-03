--- 
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 4eb36b0de53f40f882950628d55d6ac08ac5fdde
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Oheistuotteiden materiaalisuunnitelman luominen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita. Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.


## <a name="create-requirement-for-a-co-product"></a>Oheistuotteen tarpeen luominen
1. Siirry oletuskoontinäyttöön.
2. Valitse Myyntitilausten käsittely ja kysely.
3. Valitse Uusi.
4. Valitse Myyntitilaus.
5. Kirjoita arvo Asiakastili-kenttään.
    * Esimerkki: US-001  
6. Valitse OK.
7. Kirjoita arvo Nimiketunnus-kenttään.
    * Esimerkki: P6003  
8. Kirjoita numero Määrä-kenttään.
    * Esimerkki: 50 000  
9. Valitse Tallenna.

## <a name="create-a-material-plan-for-co-products"></a>Oheistuotteiden materiaalisuunnitelman luominen
1. Valitse Pääsuunnittelu.
2. Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Esimerkki: MasterPlan  
4. Valitse Suorita.
5. Laajenna tai tiivistä Sisällytettävät tietueet -osa.
6. Valitse Suodatin.
7. Valitse luettelosta rivi Nimiketunnus-kentälle.
8. Kirjoita arvo Ehdot-kenttään.
    * Esimerkki: P6003  
9. Valitse OK.
10. Valitse OK.
11. Valitse Suunnitellut tilaukset.
12. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.
    * Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.  
13. Merkitse valittu rivi luettelossa.
    * Valitse mikä tahansa suodattimen palauttamista riveistä.  
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
15. Laajenna tai tiivistä Tarvekohdistus-osa.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.  
17. Sulje sivu.


