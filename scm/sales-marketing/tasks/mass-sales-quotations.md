--- 
title: Luo useita myyntitarjouksia
description: "Tässä menettelyssä käsitellään, miten luodaan tehokkaasti tarjouksia, jotka sisältävät useita monille asiakkaille lähetettäviä tuotteita tai palveluja."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bb32fbf14e7a96481dd78059e0299e33e754c0d7
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="mass-create-sales-quotations"></a>Luo useita myyntitarjouksia

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten luodaan tehokkaasti tarjouksia, jotka sisältävät useita monille asiakkaille lähetettäviä tuotteita tai palveluja. Tämä joukkotarjouksen luonti perustuu tarjousmalleihin. Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.


## <a name="create-a-quotation-template"></a>Luo tarjousmalli
1. Valitse Myynti ja markkinointi > Asetukset > Tarjoukset > Malliryhmät.
2. Valitse Uusi.
3. Kirjoita Ryhmän tunnus -kenttään haluamasi tunnus.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Tallenna.
6. Sulje sivu.
7. Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.
8. Valitse Uusi.
9. Valitse Tilityyppi-kentässä Asiakas.
10. Syötä tai valitse arvo Asiakastili-kentässä.
11. Valitse OK.
    * Jotta tarjouksesta tulisi malli, sinun on suoritettava tarjouksen otsikon määritysvaiheet. Se on tehtävä ennen rivien lisäämistä tarjoukseen.   
12. Valitse toimintoruudussa Asetukset.
13. Valitse Vaihda näkymä.
14. Valitse Otsikkonäkymä.
15. Laajenna osa Asetukset.
16. anna tai valitse Ryhmän tunnus -kentässä arvo.
17. Syötä Mallin nimi -kenttään arvo.
18. Valitse Aktiivinen-kentässä Kyllä.
    * Kun uuteen myyntitarjoukseen käytetään malleja, vain aktiivisia malleja voi käyttää.  
19. Valitse toimintoruudussa Asetukset.
20. Valitse Vaihda näkymä.
21. Valitse Rivinäkymä.
22. Anna tai valitse Nimike-kentässä arvo.
23. Kirjoita Nimike-kenttään arvo.
24. Sulje sivu.
25. Lisää Alennusprosentti-kenttään numero.
26. Valitse Lisää rivi.
27. Anna tai valitse Nimike-kentässä arvo.
28. Kirjoita Nimike-kenttään arvo.
29. Sulje sivu.
30. Anna Yksikköhinta-kentässä uusi hinta tai vaihda nykyistä hintaa.
31. Valitse Lisää rivi.
32. Anna tai valitse Nimike-kentässä arvo.
33. Kirjoita Nimike-kenttään arvo.
34. Sulje sivu.
35. Kirjoita numero Määrä-kenttään.
36. Lisää Alennus-kenttään numero.
37. Valitse Tallenna.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Luo mallilla yksittäinen tarjous
1. Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.
    * Huomaa, että juuri luomasi tarjous on merkitty malliksi.  
2. Valitse Uusi.
3. Valitse Tilityyppi-kentässä Asiakas.
4. Syötä tai valitse arvo Asiakastili-kentässä.
5. Laajenna Malli-osa.
6. anna tai valitse Ryhmän tunnus -kentässä arvo.
7. Anna tai valitse Mallin nimi -kentässä arvo.
8. Valitse Laskentatapa-kentässä Mallin arvojen perusteella.
9. Valitse OK.
    * Uusi tarjous on nyt luotu mallin tietojen ja ehtojen perusteella.  
10. Sulje sivu.
11. Sulje sivu.

## <a name="apply-the-template-to-mass-create-quotations"></a>Luo mallilla useita tarjouksia
1. Valitse Myynti ja markkinointi > Myyntitarjoukset > Tarjouksen päivittäminen > Luo useita tarjouksia.
2. Valitse Tilityyppi-kentässä Asiakas.
3. anna tai valitse Ryhmän tunnus -kentässä arvo.
4. Anna tai valitse Mallin nimi -kentässä arvo.
5. Valitse Laskentatapa-kentässä Mallin arvojen perusteella.
6. Laajenna Tietueet-kohta ja sisällytä osaan.
7. Valitse Suodatin.
8. Määritä Ehdot-kentässä suodatin kattamaan ne asiakkaat, jotka haluat sisällyttää tähän useiden tarjousten luontiin. Käytä muotoa Asiakas1...AsiakasN.
    * Voit esimerkiksi määrittää suodattimeksi US-001..US-004  
9. Valitse OK.
10. Valitse OK.
11. Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.
    * Varmista, että tarjoukset on luotu valitun mallin perusteella kaikille joukkopäivitysrutiinissa määritetyille asiakkaille.  


