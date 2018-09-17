--- 
title: Muodosta asiakkaan maksuehdot
description: "Tämä menettely määrittää käteisalennuksen ja eräpäivän asetukset."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e0e43962bea3ff1c3adafa73da4ce3862963a51
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-terms"></a>Muodosta asiakkaan maksuehdot

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely määrittää käteisalennuksen ja eräpäivän asetukset. Tässä tehtävän ohjauksessa käytetään esittely-yritystä USMF.

1. Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksupäivät.
    * Myynti- ja ostoreskontran maksuehdot ovat samat. Jos määrität ne moduulissa, ne ovat käytettävissä myös toisessa moduulissa. Tätä tehtävän ohjausta varten määritetään maksuehdot myyntireskontran puolella.  
2. Valitse Uusi.
    * Luo maksupäivä, jos maksuehdot vaativat tietyn viikonpäivän (maanantai, tiistai jne.) tai tietyn kuukaudenpäivän (5., 10. jne.).  
3. Syötä Maksupäivä-kenttään maksupäiväkentän tunnus.
4. Syötä Kuvaus-kenttään maksupäivän kuvaus.
5. Valitse Viikko/Kuukausi-kentässä Viikko tai Kuukausi.
    * Jos haluat syöttää viikonpäivän, kuten maanantain, valitse Viikko. Jos haluat syöttää kuukaudenpäivän, kuten 10. päivä, valitse Kuukausi. Tässä esimerkissä valitaan Kuukausi.  
6. Syötä Kuukaudenpäivä-kenttään päivämäärä.
    * Päivämäärä syötetään numeroina, eli esim. 10. päivä.  
7. Valitse Tallenna.
8. Sulje sivu.
9. Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksuehdot.
10. Valitse Uusi.
    * Maksuehtoja käytetään eräpäivien laskennassa. Käteisalennuksen päivämäärän asetukset määritetään erillisellä sivulla.  
11. Syötä Maksuehdot-kenttään maksuehtokentän tunnus.
12. Syötä Kuvaus-kenttään kuvaus.
13. Valitse maksutapa, kuten postiennakko, netto, nykyinen kuukausi jne.
    * Maksuehtoa käytetään erääntymisen laskennan aloittamisen määrittämisessä.  Esimerkiksi Netto-kohtaa käytetään, jos eräpäivä on aina tietty laskupäivämäärän jälkeisten kuukausien tai päivien määrä. Postiennakko-kohtaa käytetään, kun maksu vaaditaan laskun yhteydessä. Tällöin eräpäivää ei voida laskea. Valitaan tässä tehtävän ohjauksessa Nykyinen kuukausi.  
14. Valitse maksupäivä, jos laskennassa tarvitaan tiettyä viikonpäivää tai päivämäärää.
    * Voit syöttää määrän maksuehdoista riippuen kuukausina tai päivinä. Voit myös käyttää maksusuunnitelmaa tai maksupäivää tehdessäsi lisäyksen maksutavan loppuun. Jos eräpäivä on aina seuraavan kuukauden 10. päivä, valitse maksupäiväksi 10. päivä.  
15. Valitse Tallenna.
16. Sulje sivu.
17. Siirry kohtaan Myyntireskontra > Maksujen asetukset > Käteisalennukset.
18. Valitse Uusi.
    * Tällä sivulla määritetään, miten käteisalennus lasketaan.  
19. Syötä Käteisalennus-kenttään käteisalennuskentän tunnus.
20. Syötä Kuvaus-kenttään kuvaus.
21. Jos käytettävissä on käteisalennustasoja, valitse tämän uuden käteisalennuksen jälkeen soveltuva seuraava alennuskoodi.
22. Syötä käteisalennuksen päivämäärän laskennassa käytettävien päivien määrä.
    * Jos valittuna on Nettoperiaate, päivien määrä lisätään laskupäivämäärään, kun käteisalennuksen päivämäärä lasketaan.  
23. Anna käteisalennuksen prosentti.
24. Syötä päätili, jolle myyntilaskujen käteisalennus kirjataan.
25. Valitse vaihtoehto Alennuksen vastatilit -kentässä.
    * Jos valitset Laskurivien tilit -kohdan, käteisalennus kirjataan samalle toimittajan laskun käyttöomaisuuserän/kulujen päätilille. Jos valitset Käytä toimittajan laskuissa päätiliä -kohdan, käteisalennus kirjataan Toimittajan laskujen päätili -kohdassa määritetylle päätilille. Tässä esimerkissä valitaan Käytä toimittajan laskuissa päätiliä.  
26. Syötä päätili, jolle toimittajan laskujen käteisalennus kirjataan.
27. Valitse Tallenna.


