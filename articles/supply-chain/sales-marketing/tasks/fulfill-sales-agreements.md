--- 
title: "Täytä myyntisopimuksia"
description: "Tässä menettelyssä käsitellään, miten myyntisopimus toteutetaan liittämällä siihen myyntitilauksia."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f0894bf962c139c2e9e4c9f8d1589fd933afcedb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="fulfill-sales-agreements"></a>Täytä myyntisopimuksia

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten myyntisopimus toteutetaan liittämällä siihen myyntitilauksia. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Varmista ennen tämän opastuksen aloittamista, että sinulla on voimassaoleva myyntisopimus, jonka tyyppi on Tuotteen arvon vahvistus. Vaihtoehtoisesti voit suorittaa Luo myyntisopimuksia -tehtäväopastuksen.  




## <a name="release-a-sales-order-from-the-agreement"></a>Vapauta myyntitilaus sopimuksista
1. Valitse Myynti ja markkinointi > Myyntisopimukset > Myyntisopimukset.
2. Avaa luettelossa sopimus, jonka mukaisesti haluat vapauttaa tilauksen.
3. Valitse toimintoruudussa Myyntisopimus.
4. Valitse Vapauta tilaus.
    * Luo vapautustilaus -sivun yläosassa oleva teksti ilmaisee, että myyntitilausrivin edellyttävät tiedot vaihtelevat sen mukaan, onko sopimus määrä- vai arvoperusteinen.  
    * Tämän opastuksen sopimuksen tyyppi on Tuotteen arvon vahvistus. Tämän vuoksi tämän sivun Rivit-osa on tyhjä. Jos sitoutuminen perustuisi määrään, rivitiedot kopioitaisiin sopimuksesta.  
5. Valitse Luo.
    * Sanoma ilmoittaa, että myyntitilaus on luotu. Koska tilauksessa ei ole rivejä, sinun on viimeisteltävä vapautusprosessi lisäämällä tilausrivin tiedot.   
6. Sulje sivu.
7. Sulje sivu.
8. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
9. Etsi ja avaa luettelossa tilaus, joka luotiin edellisessä tehtävässä vapautetun tilauksen vuoksi.
10. Valitse Lisää rivi.
11. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
12. Kirjoita tai valitse Nimiketunnus-kentässä nimike, joka määritettiin liitetyssä myyntisopimuksessa.
13. Kirjoita numero Määrä-kenttään.
    * Varmista, että annat määrän, jonka mukainen nettosumma alittaa liittyvän myyntisopimuksen arvon.  
    * Huomaa, että koska myyntitilaus on linkitetty sopimukseen, neuvoteltua alennusprosenttia käytetään tilausrivillä.  
14. Valitse Päivitä rivi.
15. Valitse Liitetty.
    * Liitetty sopimus -sivulla on sen sopimuksen tunnus ja ehdot, josta rivi on vapautettu.  
16. Sulje sivu.
17. Valitse toimintoruudussa Yleiset.
18. Valitse Liittyvä myyntisopimus.
19. Laajenna Rivin erittely -osa.
20. Valitse Täytäntöönpano-välilehti.
    * Täytäntöönpano-välilehdessä on kaikkien tähän sitoutumiseen liitettyjen myyntitilausrivien yhteenveto ja niiden täytäntöönpanotila sekä vielä vapauttamaton summa tai määrä.   
21. Sulje sivu.
22. Sulje sivu.
23. Sulje sivu.

## <a name="apply-sales-agreement-in-the-order-process"></a>Käytä myyntisopimuksia tilausprosessissa
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Etsi ja valitse luettelossa asiakas, joka on määritetty myyntisopimuksessa.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Laajenna Yleinen-osa.
7. Avaa haku napsauttamalla Myyntisopimuksen tunnus -kentässä avattavan valikon painiketta.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse Kyllä.
10. Valitse OK.
11. Merkitse valittu rivi luettelossa.
12. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
13. Kirjoita tai valitse Nimiketunnus-kentässä nimike, joka määritettiin liitetyssä myyntisopimuksessa.
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
15. Valitse Tallenna.
16. Valitse toimintoruudussa Kerää ja pakkaa.
17. Valitse Kirjaa pakkausluettelo.
18. Laajenna Parametrit-osa.
19. Valitse Kirjaus-kentässä Kyllä.
20. Valitse OK.
21. Valitse OK.
22. Valitse toimintoruudussa Yleiset.
23. Valitse Liittyvä myyntisopimus.
24. Valitse Täytäntöönpano-välilehti.


