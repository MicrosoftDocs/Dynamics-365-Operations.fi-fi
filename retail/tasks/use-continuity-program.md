--- 
title: "Käytä jatkuvuusohjelmaa"
description: "Näissä toimintaohjeissa neuvotaan, miten jatkuvuusohjelman avulla tehdään myyntejä ja käsitellään niihin liittyviä myyntitilauksia."
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: bd584bbb49ea83c4debf11ad0169c346ef0f9637
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="use-a-continuity-program"></a>Käytä jatkuvuusohjelmaa

[!include[task guide banner](../includes/task-guide-banner.md)]

Näissä toimintaohjeissa neuvotaan, miten jatkuvuusohjelman avulla tehdään myyntejä ja käsitellään niihin liittyviä myyntitilauksia. Käyttäjä on määritettävä puhelinkeskuksen käyttäjäksi, jotta tämän menettelyn voi suorittaa. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Vähittäismyynti ja kauppa > Asiakkaat > Asiakaspalvelu.
2. Kirjoita SearchText-kenttään "Karen" ja paina sitten sarkainnäppäintä.
    * Tarkennettu haku -valintaikkunan tulisi aueta. Jos näin ei tapahdu, valitse Etsi kentän oikealla puolella.  
3. Merkitse valittu rivi luettelossa.
    * Tuloksissa tulisi olla vain yksi rivi nimellä Karen Berg. Valitse rivi napsauttamalla valintamerkkiä ruudukon vasemmassa laidassa.  
4. Klikkaa Valitse.
5. Valitse Uusi myyntitilaus.
    * Ota muistiin myyntitilauksen numero. Tarvitset sitä myöhemmin.  
6. Kirjoita Nimiketunnus-kenttään 88000 ja paina sitten sarkainnäppäintä.
    * Tämä on jatkuvuusnimike USRT-yrityksen esittelytiedoissa.  
7. Valitse Valmis.
8. Kirjoita Maksutapa-kenttään "Visa".
9. Valitse Lisää luottokortti.
    * Anna pakolliset luottokorttitiedot tällä sivulla.  
10. Valitse OK.
11. Laajenna Maksu-osa.
    * Jotta puhelinkeskus voi lähettää tilauksen, tilaukselle on syötettävä maksuja.  
12. Valitse OK.
13. Valitse Lähetä.
    * Jatkuvuustilauksen luonti on nyt valmis. Seuraavaksi ajat kaksi eräprosessia, jotka käsittelevät jatkuvuustilaukset.  
14. Sulje sivu.
15. Valitse Vähittäismyynti ja kauppa > Jatkuvuus > Käsittele jatkuvuusmaksut.
16. Kirjoita Jatkuvuusnimike-kenttään 88000 ja paina sitten sarkainnäppäintä.
17. Valitse OK.
18. Valitse Vähittäismyynti ja kauppa > Jatkuvuus > Luo jatkuvuuden alitilaukset.
    * Tämä prosessi luo uusia myyntitilauksia, jotka perustuvat jatkuvuusohjelmasi asetuksiin.  
19. Kirjoita Jatkuvuusnimike-kenttään 88000 ja paina sitten sarkainnäppäintä.
    * Nimike 88000 on jatkuvuusnimike USRT-yrityksen esittelytiedoissa.  
20. Syötä tai valitse arvo kentässä Myyntitilaus.
    * Anna aiemmin ohjeessa muistiin ottamasi myyntitilauksen numero. Tämä vähentää ohjeiden suoritusaikaa huomattavasti. Myyntitilaus-kenttä on valinnainen – voit käsitellä kaikki yhden ohjelman tilaukset.  
21. Valitse OK.

