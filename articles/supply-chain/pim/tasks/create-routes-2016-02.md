---
title: Reittien luominen (helmikuu 2016)
description: Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuotantoreitityksen luomiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844558"
---
# <a name="create-routes-february-2016"></a>Reittien luominen (helmikuu 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävässä keskitytään valmiin ja puolivalmiin tuotteen tuotantoreitityksen luomiseen. Se on tuoterakenteen laskentasarjan viides tehtävä. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Puolivalmiin tuotteen reitin luominen
1. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse nimiketunnus BOM_2.  
3. Valitse toimintoruudussa Suunnittele.
4. Valitse Reitti.
5. Valitse Uusi.
6. Valitse Reitti ja reittiversio.
7. Kirjoita arvo Kuvaus-kenttään.
    * Kirjoita tässä esimerkissä ROUTE_2.  
8. Syötä tai valitse arvo Toimipaikka-kenttään.
    * Anna tai valitse tässä esimerkissä Toimipaikka 1.  
9. Valitse OK.
10. Valitse Uusi.
11. Anna tai valitse Toiminto-kentässä arvo.
    * Valitse tässä esimerkissä Kokoonpano.  
12. Lisää Ajoaika-kenttään numero.
    * Kirjoita esimerkiksi 1. Suoritusajat sisältyvät usein nimikkeelle laskettavaan hintaan.  
13. Anna tai valitse arvo Reititysryhmä-kentässä.
    * Valitse tässä esimerkissä Std.  
14. Valitse Asetukset-välilehti.
15. Syötä tai valitse arvo Asetusluokka-kenttään.
    * Valitse tässä esimerkissä Kokoonpano.  
16. Valitse Ajat-välilehti.
17. Anna Asetusaika-kentässä luku.
    * Kirjoita tässä esimerkissä 1. Asetusajat sisältyvät usein nimikkeelle laskettavaan hintaan.  
18. Valitse toimintoruudussa Reittiversio.
19. Valitse Hyväksy.
20. Valitse Kyllä Haluatko hyväksyä myös reitin? -kentässä.
21. Valitse OK.
22. Valitse toimintoruudussa Reittiversio.
23. Valitse Aktivoi.
24. Sulje sivu.
25. Sulje sivu.

## <a name="create-a-route-for-a-finished-product"></a>Valmiin tuotteen reitin luominen
1. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse nimiketunnus BOM_1.  
2. Valitse toimintoruudussa Suunnittele.
3. Valitse Reitti.
4. Valitse Uusi.
5. Valitse Reitti ja reittiversio.
6. Kirjoita arvo Kuvaus-kenttään.
    * Kirjoita tässä esimerkissä ROUTE_1.  
7. Syötä tai valitse arvo Toimipaikka-kenttään.
    * Anna tai valitse tässä esimerkissä Toimipaikka 1.  
8. Valitse OK.
9. Valitse Uusi.
10. Anna tai valitse Toiminto-kentässä arvo.
    * Valitse tässä esimerkissä Pakkaus.  
11. Lisää Ajoaika-kenttään numero.
    * Kirjoita tässä esimerkissä 1.  
12. Anna tai valitse arvo Reititysryhmä-kentässä.
    * Valitse tässä esimerkissä Std.  
13. Valitse Asetukset-välilehti.
14. Syötä tai valitse arvo Asetusluokka-kenttään.
    * Valitse tässä esimerkissä Pakkaus.  
15. Valitse Ajat-välilehti.
16. Anna Asetusaika-kentässä luku.
    * Kirjoita tässä esimerkissä 1.  
17. Valitse toimintoruudussa Reittiversio.
18. Valitse Hyväksy.
19. Valitse OK.
20. Valitse toimintoruudussa Reittiversio.
21. Valitse Aktivoi.
22. Sulje sivu.
23. Sulje sivu.

## <a name="enable-automatic-consumption-of-setup-time"></a>Asetusajan automaattisen kulutuksen ottaminen käyttöön
1. Valitse Tuotannonhallinta > Asetukset > Reitit > Reititysryhmät.
2. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse luettelossa Std.  
3. Valitse Muokkaa.
4. Valitse Asetusaika-kentässä Kyllä.
    * Asetusajat sisältyvät usein nimikkeelle laskettavaan hintaan.  
5. Valitse Tallenna.
6. Sulje sivu.

