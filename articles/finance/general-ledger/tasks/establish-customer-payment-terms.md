---
title: Muodosta asiakkaan maksuehdot
description: Tämä menettely määrittää käteisalennuksen ja eräpäivän asetukset.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f4adfd4231a39df6f17e8a131aa14d057eb8447
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809979"
---
# <a name="establish-customer-payment-terms"></a>Muodosta asiakkaan maksuehdot

[!include [banner](../../includes/banner.md)]

Tämä menettely määrittää käteisalennuksen ja eräpäivän asetukset. Tässä tehtävän ohjauksessa käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Maksujen asetukset > Maksupäivät**. **Myyntireskontran** ja **ostoreskontran** **maksuehdot** ovat samat. Jos määrität ne moduulissa, ne ovat käytettävissä myös toisessa moduulissa. Tätä tehtävän ohjausta varten määritetään maksuehdot **myyntireskontran** puolella.
2. Valitse **Uusi**. Luo maksupäivä, jos maksuehdot vaativat tietyn viikonpäivän (maanantai, tiistai jne.) tai tietyn kuukaudenpäivän (5., 10. jne.). 
3. Kirjoita **Maksupäivä**-kenttään tunnus.
4. Syötä **Kuvaus**-kenttään maksupäivän kuvaus.
5. Valitse **Viikko/Kuukausi**-kentässä Viikko tai Kuukausi. Jos haluat syöttää viikonpäivän, kuten maanantain, valitse Viikko. Jos haluat syöttää kuukaudenpäivän, kuten 10. päivä, valitse Kuukausi. Tässä esimerkissä valitaan Kuukausi. 
6. Syötä **Kuukaudenpäivä**-kenttään päivämäärä. Päivämäärä syötetään numeroina, eli esim. 10. päivä. 
7. Valitse **Tallenna**.
8. Sulje sivu.
9. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Maksujen asetukset > Maksuehdot**.
10. Valitse **Uusi**. Maksuehtoja käytetään eräpäivien laskennassa. Käteisalennuksen päivämäärän asetukset määritetään erillisellä sivulla. 
11. Kirjoita **Maksuehdot**-kenttään tunnus.
12. Syötä **Kuvaus**-kenttään kuvaus.
13. Valitse **Maksutapa**, kuten COD, netto, kuluva kuukausi jne. Maksutapaa käytetään määritettäessä, miten eräpäivä lasketaan. Esimerkiksi Netto-kohtaa käytetään, jos eräpäivä on aina tietty laskupäivämäärän jälkeisten kuukausien tai päivien määrä. Postiennakko-kohtaa käytetään, kun maksu vaaditaan laskun yhteydessä. Tällöin eräpäivää ei voida laskea. Valitaan tässä tehtävän ohjauksessa Nykyinen kuukausi.  
14. Valitse **Maksupäivä**, jos laskennassa tarvitaan tiettyä viikonpäivää tai päivämäärää. Voit syöttää määrän maksuehdoista riippuen kuukausina tai päivinä. Voit myös käyttää **maksusuunnitelmaa** tai **maksupäivää** tehdessäsi lisäyksen maksutavan loppuun. Jos eräpäivä on aina seuraavan kuukauden 10. päivä, valitse **maksupäiväksi** 10. päivä. 
15. Valitse **Tallenna**.
16. Sulje sivu.
17. Siirry kohtaan **Myyntireskontra > Maksujen asetukset > Käteisalennukset**.
18. Valitse **Uusi**. Tällä sivulla määritetään, miten käteisalennus lasketaan. 
19. Kirjoita **Käteisalennus**-kenttään tunnus.
20. Syötä **Kuvaus**-kenttään kuvaus.
21. Jos käytettävissä on käteisalennustasoja, valitse tämän uuden käteisalennuksen jälkeen soveltuva **Seuraava alennuskoodi**.
22. Syötä käteisalennuksen päivämäärän laskennassa käytettävien päivien määrä **Päivät**-kenttään. Jos valittuna on **Netto**-periaate, päivien määrä lisätään laskupäivämäärään, kun käteisalennuksen päivämäärä lasketaan.  
23. Syötä **Alennusprosentti**-kenttään käteisalennuksen prosentti.
24. Syötä **Asiakasalennusten päätili** -kohdassa päätili, jolle käteisalennus kirjataan asiakkaan laskuja varten.
25. Valitse vaihtoehto **Alennuksen vastatilit** -kentässä. Jos valitset Laskurivien tilit -kohdan, käteisalennus kirjataan samalle toimittajan laskun käyttöomaisuuserän/kulujen päätilille. Jos valitset Käytä toimittajan laskuissa päätiliä -kohdan, käteisalennus kirjataan Toimittajan laskujen päätili -kohdassa määritetylle päätilille. Tässä esimerkissä valitaan Käytä toimittajan laskuissa päätiliä. 
26. Syötä **Toimittajaalennusten päätili** -kohdassa päätili, jolle käteisalennus kirjataan toimittajan laskuja varten.
27. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]