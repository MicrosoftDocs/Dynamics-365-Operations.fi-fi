--- 
title: Aseta menettelytavat hankintaluokkien hierarkioille
description: "Tämän toiminnon avulla voit määrittää säännöt luokan tuotteiden tilaamista varten."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Aseta menettelytavat hankintaluokkien hierarkioille

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämän toiminnon avulla voit määrittää säännöt luokan tuotteiden tilaamista varten. Käytäntösäännöt määritetään tietylle ostokäytännölle. Luokan käyttöoikeuskäytäntösääntö ohjaa, mihin hankintaluokkiin työntekijöillä on käyttöoikeus luodessaan ehdotuksia. Ehdotusta luotaessa käytettävä ostokäytäntö ja luokan käyttöoikeussääntö määräytyvät perustuen yritykseen ja toimintayksikköön, johon työntekijä kuuluu. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Yleensä ostopäällikkö tekee tämän tehtävän.


## <a name="find-the-procurement-policy"></a>Paikanna hankintakäytäntö
1. Siirry kohtaan Hankinnat > Asetukset > Käytännöt > Ostokäytännöt.
2. Napsauta hankintakäytännön USMF linkkiä.
    * Tämä on käytäntö, johon sääntö lisätään. Käytännön on oltava aktiivinen.  

## <a name="create-a-category-access-rule"></a>Luokan käyttöoikeussäännön luominen
1. Valitse luokan käyttöoikeuskäytäntöjen sääntö.
    * Jos Luo käytäntösääntö -painike näkyy himmennettynä, luokan käytössä on jo aktiivinen käytäntösääntö. Tarkista voimassaolo- ja erääntymispäiväkentistä mikä säännöistä on kyseessä, valitse se ja napsauta Keskeytä käytäntösääntö -painiketta. Mitään ei tarvitse tehdä, jos Luo käytäntösääntö -painike on käytettävissä.  
2. Valitse Luo käytäntösääntö.
3. Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.
    * Aika ei saa olla päällekkäinen toisen, aktiivisen säännön kanssa.  
    * Valitse luokka, jota sääntö koskee. Kirjaa luokka muistiin – sitä tarvitaan myöhemmin. Kun valitset jonkin luokan, myös sen pääluokka tai -luokat lisätään myös Valitut luokat -luetteloon.  
    * Valitse Sisällytä aliluokat -asetus, jos haluat käyttää sääntöä kaikkiin valitun luokan alaluokkiin.  
4. ValitseLisää.
    * Jos asetat Sisällytä yläluokka -vaihtoehdon käyttöön, pääluokalle määrittämäsi käytäntösääntö määritetään myös tämän alaluokille, jos alaluokille ei ole määritetty käytäntösääntöä.  
5. Valitse OK.

## <a name="create-a-category-policy-rule"></a>Luokan käytäntösäännön luominen
1. Valitse luokan käytäntösääntö
    * Jos Luo käytäntösääntö -painike on himmennettynä, valitse aktiivinen käytäntösääntö ja napsauta Keskeytä käytäntösääntö -painiketta.  
2. Valitse Luo käytäntösääntö.
3. Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.
4. ValitseLisää.
5. Valitse sama luokka, jota käytit luokan käyttöoikeussäännölle.
6. Valitse vaihtoehto Toimittajan valinta -kentässä.
    * Valitse sääntö, joka ohjaa luokan toimittajavalintaa, kun ostoehdotuksia luodaan.  
7. Valitse Sulje.
    * Määrittämäsi käytäntösäännöt ovat olleet kulutustyypin ostoehdotuksille. Jos haluat määrittää täydennystyypin ostoehdotusten käytäntöjä, luo sääntö käytäntösäännön tyypille "Täydennysluokan käyttöoikeuskäytäntöjen sääntö".  


