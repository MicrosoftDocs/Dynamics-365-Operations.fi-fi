---
title: Määritä myyntiprovision säännöt
description: Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4507405039cd27a071e0f0ed8bfad31fd30f16f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203200"
---
# <a name="set-up-sales-commission-rules"></a>Määritä myyntiprovision säännöt

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön. Menettely osoittaa, miten asiakas- ja nimikeprovisioryhmät luodaan ja miten valittu asiakas ja tuote linkitetään vastaaviin ryhmiin. Kyseisiä ryhmiä käytetään sitten provision laskenta-asetuksissa luomaan asiakas-, nimike- ja myyntiedustajayhdistelmä, joka on täsmäytettävä myyntitilaukseen, jotta myyjät saisivat provision. Asiakas- ja nimikeprovisioryhmien on vapaaehtoista, sillä provisio voidaan laskea yksittäisen asiakkaan ja/tai nimikkeen perusteella. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-up-commission-groups-and-commission-rates"></a>Määritä provisioryhmät ja provisioprosentit
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Provisiot > Provision asiakasryhmät**.
2. Valitse **Uusi**.
3. Kirjoita **Ryhmä**-kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Tallenna**.
6. Sulje sivu.
7. Siirry kohtaan **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Provisiot > Nimikeryhmät**.
8. Valitse **Uusi**.
9. Kirjoita **Ryhmä**-kenttään arvo.
10. Kirjoita arvo **Nimi**-kenttään.
11. Valitse **Tallenna**.
12. Sulje sivu.
13. Siirry kohtaan **Myynti ja markkinointi > Provisiot > Myyntiryhmät**.
    - Provisiomyyntiryhmä määrittää, ketkä työntekijät, joilla on myyntiedustajan rooli, voivat saada provision, kun kyseiseen myyntiryhmään liitetty asiakas ostaa tiettyjä nimikkeitä.  
    - USMF-demotietoyrityksessä myyntiryhmä Sales reps US.  
14. Valitse **Toimintoruutu**-osiosta **Yleiset**.
15. Valitse **Myyjä**. Myyjä-sivulla näkyy luettelo yrityksen myyntihenkilöistä, jotka liittyvät määrättyyn provisioryhmään. Voit määrittää samaan ryhmään useita myyntiedustajia ja määrittää prosentteina kunkin osuuden kokonaisprovisiosta. Kaikkien työntekijöiden osuus kokonaisprovisiosta ei voi olla yli 100. 
16. Merkitse valittu rivi luettelossa.
17. Valitse **Muokkaa**.
18. Määritä **Provisio-osuus**-asetukseksi 50.
19. Valitse **Uusi**.
20. Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.
21. Käytä **Pikasuodatin**-vaihtoehtoa tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimi-kenttää arvolla Sudan Burk.
22. Klikkaa **Valitse**.
23. Määritä **Provisio-osuus**-asetukseksi 50.
24. Valitse **Tallenna**.
25. Siirry kohtaan **Myynti ja markkinointi > Provisiot > Provisiolaskelma**. Voit määrittää **Provisiolaskelma**-sivulla provisioprosentin, jonka työntekijä saa myyntitapahtumasta, kun se sisältää ennalta määritetyn asiakas- ja tuoteyhdistelmän. Provisioprosenttiasetusten osana on määritettävä provision laskentaperusta sekä alennusten sisällyttäminen tai poissulkeminen. Voit myös antaa voimassaoloajan, jolloin provisioprosentti on aktiivinen.  
26. Valitse **Uusi**.
27. Valitse **Nimikekoodi**-kentässä Ryhmä.
28. Avaa haku napsauttamalla **Nimikkeen suhde**-kentässä avattavan valikon painiketta.
29. Etsi ja valitse luettelosta aiemmin luomasi ryhmä.
30. Valitse **Asiakaskoodi**-kentässä Ryhmä.
31. Avaa haku napsauttamalla **Asiakassuhde**-kentästä avattavan valikon painiketta.
32. Valitse luettelosta aiemmin määrittämäsi ryhmä.
33. Avaa haku napsauttamalla **Myyjän suhde** -kentästä avattavan valikon painiketta.
34. Etsi haluamasi tietue luettelosta ja valitse se.
    - Säilytä Ennen rivialennusta -vaihtoehto.  
    - Säilytä Tuotto-vaihtoehto provision arvon laskennan perusteena.    
35. Lisää Provisioprosentti-kenttään numero.
36. Valitse **Tallenna**.

## <a name="setting-up-commission-posting"></a>Provision kirjauksen määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Myynti ja markkinointi > Provisiot > Provision kirjaus**. Provisiot maksetaan työntekijöille, joten ne on määritettävä varmistamaan, että taloudellinen kirjaus tehdään oikein asianmukaisille tileille **Kirjanpito**-osiossa. Tämä tehdään **Provision kirjaus** -sivulta. Tarkista nykyisessä yrityksessä käytettävissä oleva asetus. Yleensä provisiosummat kirjataan erityiskulutilille ja vastakirjataan erityisostoreskontraan. Jos et ole määrittänyt provision kirjaussääntöjä, järjestelmä ei suorita provisioon oikeuttavien myyntitilausten laskutusta.  
2. Sulje sivu.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Määritä provisioryhmä asiakkaaseen ja tuotteeseen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Asiakkaat > Kaikki asiakkaat**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse **Muokkaa**.
5. Laajenna **Oletusmyyntitilaukset**-osio.
6. Avaa haku napsauttamalla **Provisioryhmä**-kentästä avattavan valikon painiketta.
7. Valitse luettelosta aiemmin luomasi ryhmä.
8. Avaa haku napsauttamalla **Myyntiryhmä**-kentästä avattavan valikon painiketta.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Valitse **Tallenna**.
11. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
12. Käytä **Suodatin**-vaihtoehtoa tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla T0020.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Valitse **Muokkaa**.
15. Laajenna **Myynti**-osio.
16. Avaa haku napsauttamalla **Provisioryhmä**-kentästä avattavan valikon painiketta.
17. Etsi ja valitse luettelosta aiemmin luomasi provisioryhmä.
18. Valitse **Tallenna**.

