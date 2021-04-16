---
title: Aseta menettelytavat hankintaluokkien hierarkioille
description: Tämän toiminnon avulla voit määrittää säännöt luokan tuotteiden tilaamista varten.
author: kamaybac
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08669ceeca46ca415d9b0d19ddef3bc9b1100120
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821054"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Aseta menettelytavat hankintaluokkien hierarkioille

[!include [banner](../../includes/banner.md)]

Tämän toiminnon avulla voit määrittää säännöt luokan tuotteiden tilaamista varten. Käytäntösäännöt määritetään tietylle ostokäytännölle. Luokan käyttöoikeuskäytäntösääntö ohjaa, mihin hankintaluokkiin työntekijöillä on käyttöoikeus luodessaan ehdotuksia. Ehdotusta luotaessa käytettävä ostokäytäntö ja luokan käyttöoikeussääntö määräytyvät perustuen yritykseen ja toimintayksikköön, johon työntekijä kuuluu. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Yleensä ostopäällikkö tekee tämän tehtävän.


## <a name="find-the-procurement-policy"></a>Paikanna hankintakäytäntö
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostokäytännöt**.
2. Napsauta hankintakäytännön USMF linkkiä. Tämä on käytäntö, johon sääntö lisätään. Käytännön on oltava aktiivinen.  

## <a name="create-a-category-access-rule"></a>Luokan käyttöoikeussäännön luominen
1. Laajenna **Käytäntösäännöt**-pikavälilehti.
2. Valitse **Käytäntösäännön tyyppi** -luettelosta **Luokan käyttöoikeuskäytäntösääntö**. Jos **Luo käytäntösääntö** -painike näkyy himmennettynä, luokan käytössä on jo aktiivinen käytäntösääntö. Tarkista **Voimassa**- ja **Vanhentuminen**-kentistä mikä säännöistä on kyseessä, valitse se ja napsauta **Keskeytä käytäntösääntö** -painiketta. Mitään ei tarvitse tehdä, jos **Luo käytäntösääntö** -painike on käytettävissä.  
3. Valitse **Luo käytäntösääntö**.
4. Syötä päivämäärä ja kellonaika **Voimaantulopäivä**-kenttään. Aika ei saa olla päällekkäinen toisen, aktiivisen säännön kanssa.  
5. Valitse luokka, jota sääntö koskee. Kirjaa luokka muistiin – sitä tarvitaan myöhemmin. Kun valitset jonkin luokan, myös sen pääluokka tai -luokat lisätään myös Valitut luokat -luetteloon. Valitse **Sisällytä aliluokat** -asetus, jos haluat käyttää sääntöä kaikkiin valitun luokan alaluokkiin.
6. Valitse nuoli oikealle, jos haluat lisätä kohteen **Valitut luokat** -luetteloon.  
4. Valitse **OK**. Jos asetat **Sisällytä pääsääntö** -vaihtoehdon käyttöön, pääluokalle määrittämäsi käytäntösääntö määritetään myös tämän alaluokille, jos alaluokille ei ole määritetty käytäntösääntöä.

## <a name="create-a-category-policy-rule"></a>Luokan käytäntösäännön luominen
1. Valitse **Käytäntösäännön tyyppi** -luettelosta **Luokan käytäntösääntö**. Jos **Luo käytäntösääntö** -painike on himmennettynä, valitse aktiivinen käytäntösääntö ja napsauta **Keskeytä käytäntösääntö** -painiketta.  
2. Valitse **Luo käytäntösääntö**.
3. Syötä päivämäärä ja kellonaika **Voimaantulopäivä**-kenttään.
4. Valitse **Lisää**.
5. Valitse **Luokka**-kentässä sama luokka, jota käytit **luokan käyttöoikeussäännölle**.
6. Valitse vaihtoehto **Toimittajan valinta** -kentässä. Valitse sääntö, joka ohjaa luokan toimittajavalintaa, kun ostoehdotuksia luodaan.  
7. Valitse **Sulje**. Määrittämäsi käytäntösäännöt ovat olleet kulutustyypin ostoehdotuksille. Jos haluat määrittää täydennystyypin ostoehdotusten käytäntöjä, luo sääntö käytäntösäännön tyypille "Täydennysluokan käyttöoikeuskäytäntöjen sääntö".  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]