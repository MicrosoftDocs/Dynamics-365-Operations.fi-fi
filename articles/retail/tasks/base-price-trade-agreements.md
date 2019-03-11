---
title: Perushinta ja kauppasopimukset
description: Tässä menettelyssä esitellään kanavakohtaisen myyntihinnan kauppasopimusten luominen.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4830ac553318cfbb3cb74395d1662e74dff75290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "320417"
---
# <a name="base-price-and-trade-agreements"></a>Perushinta ja kauppasopimukset

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä esitellään kanavakohtaisen myyntihinnan kauppasopimusten luominen. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Vähittäismyynti ja kauppa > Hinnoittelu ja alennukset > Hintaryhmät > Kaikki hintaryhmät.
    * Hintaryhmät tarkoittava tapaa, jolla kauppasopimukset on liitetty tiettyihin kanaviin. Jos hintaryhmiä käytetään kauppasopimusten liittämisessä kanaviin, käytössä on kanavakohtainen hinnoittelu.  
2. Valitse Uusi.
3. Syötä arvo Hintaryhmät-kenttään.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Tallenna.
6. Sulje sivu.
7. Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.
8. Valitse luettelosta New York.
9. Valitse toimintoruudussa Myymälä.
10. Valitse Hintaryhmät.
11. Valitse Uusi.
12. Avaa haku valitsemalla Hintaryhmät-kentässä avattavan valikon painike.
13. Etsi haluamasi tietue luettelosta ja valitse se.
14. Valitse Tallenna.
15. Sulje sivu.
16. Sulje sivu.
17. Siirry kohtaan Vähittäismyynti ja kauppa > Tuotteet ja luokat > Vapautetut tuotteet luokittain.
18. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
19. Valitse Muokkaa.
20. Ota käyttöön Myynti-osan laajennus.
21. Syötä Hinta-kenttään numero.
    * Tätä hintaa ei käytetä, jos soveltuvia kauppasopimuksia ei löydy.  
22. Valitse Tallenna.
23. Valitse toimintoruudussa Myynti.
24. Valitse Luo kauppasopimukset.
25. Valitse Uusi.
26. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
27. Valitse luettelosta Vähittäismyynti.
    * Esittelytiedoissa Vähittäismyynti-kirjauskansion nimi on Hinta (myynti) -suhteen oletusarvo. Tämä tarkoittaa sitä, että kaikkien uusien rivien oletusarvoina käytetään myyntihinnan kauppasopimuksia.  
28. Valitse Rivit.
29. Valitse Tilikoodi-kentässä Ryhmä.
30. Avaa haku napsauttamalla Tilin valinta -kentässä avattavan valikon painiketta.
31. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tämä viimeistelee linkin kanavan, hintaryhmän ja kauppasopimuksen välillä.  
32. Syötä Nimikkeen suhde -kenttään arvo.
33. Lisää Summa valuuttana -kenttään numero.
34. Valitse Etsi seuraava -valintaruutu tai poista sen valinta.
    * Kun Etsi seuraava -kohdan arvoksi on määritetty Kyllä, hinnoittelumoduuli jatkaa sopivien alemman myyntihinnan omaavien kauppasopimusten etsimistä. Kun Etsi seuraava -kohdan arvoksi on määritetty Ei, hinnoittelumoduuli lopettaa etsimisen ja käyttää kauppasopimusta.  
35. Valitse Kirjaa.
36. Valitse OK.
37. Sulje sivu.
38. Valitse toimintoruudussa Myynti.
39. Valitse Myyntihinta.

