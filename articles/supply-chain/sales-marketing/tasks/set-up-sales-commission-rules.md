--- 
title: "Määritä myyntiprovision säännöt"
description: "Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d81765884f741443d1c0f5b0cb8bc545945e1a1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-commission-rules"></a>Määritä myyntiprovision säännöt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään, miten myyntiprovision laskenta ja seuranta määritetään ja otetaan käyttöön. Menettely osoittaa, miten asiakas- ja nimikeprovisioryhmät luodaan ja miten valittu asiakas ja tuote linkitetään vastaaviin ryhmiin. Kyseisiä ryhmiä käytetään sitten provision laskenta-asetuksissa luomaan asiakas-, nimike- ja myyntiedustajayhdistelmä, joka on täsmäytettävä myyntitilaukseen, jotta myyjät saisivat provision. Asiakas- ja nimikeprovisioryhmien on vapaaehtoista, sillä provisio voidaan laskea yksittäisen asiakkaan ja/tai nimikkeen perusteella. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-up-commission-groups-and-commission-rates"></a>Määritä provisioryhmät ja provisioprosentit
1. Valitse Myynti ja markkinointi > Provisiot > Provision asiakasryhmät.
2. Valitse Uusi.
3. Kirjoita Ryhmä-kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Valitse Tallenna.
6. Sulje sivu.
7. Valitse Myynti ja markkinointi > Provisiot > Nimikeryhmät.
8. Valitse Uusi.
9. Kirjoita Ryhmä-kenttään arvo.
10. Kirjoita arvo Nimi-kenttään.
11. Sulje sivu.
12. Valitse Myynti ja markkinointi > Provisiot > Myyntiryhmät.
    * Provisiomyyntiryhmä määrittää, ketkä työntekijät, joilla on myyntiedustajan rooli, voivat saada provision, kun kyseiseen myyntiryhmään liitetty asiakas ostaa tiettyjä nimikkeitä.  
    * USMF-demotietoyrityksessä myyntiryhmä Sales reps US.  
13. Valitse toimintoruudussa Yleiset.
14. Valitse Myyjä.
    * Myyjä-sivulla näkyy luettelo yrityksen myyntihenkilöistä, jotka liittyvät määrättyyn provisioryhmään. Voit määrittää samaan ryhmään useita myyntiedustajia ja määrittää prosentteina kunkin osuuden kokonaisprovisiosta. Kaikkien työntekijöiden osuus kokonaisprovisiosta ei voi olla yli 100.  
15. Merkitse valittu rivi luettelossa.
16. Valitse Muokkaa.
17. Määritä provisio-osuudeksi 50.
18. Valitse Uusi.
19. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
20. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimi-kenttää arvolla Sudan Burk.
21. Klikkaa Valitse.
22. Määritä provisio-osuudeksi 50.
23. Valitse Tallenna.
24. Valitse Myynti ja markkinointi > Provisiot > Provisiolaskelma.
    * Voit määrittää Provisiolaskelma-sivulla provisioprosentin, jonka työntekijä saa myyntitapahtumasta, kun se sisältää ennaltamääritetyn asiakas- ja tuoteyhdistelmän. Provisioprosenttiasetusten osana on määritettävä provision laskentaperusta sekä alennusten sisällyttäminen tai poissulkeminen. Voit myös antaa voimassaoloajan, jolloin provisioprosentti on aktiivinen.  
25. Valitse Uusi.
26. Valitse Nimikekoodi-kentässä Ryhmä.
27. Avaa haku napsauttamalla Nimikesuhde-kentässä avattavan valikon painiketta.
28. Etsi ja valitse luettelosta aiemmin luomasi ryhmä.
29. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
30. Valitse Asiakaskoodi-kentässä Ryhmä.
31. Avaa haku napsauttamalla Asiakassuhde-kentässä avattavan valikon painiketta.
32. Valitse luettelosta aiemmin määrittämäsi ryhmä.
33. Avaa haku napsauttamalla Myyjän suhde -kentässä avattavan valikon painiketta.
34. Etsi haluamasi tietue luettelosta ja valitse se.
    * Säilytä Ennen rivialennusta -vaihtoehto.  
    * Säilytä Tuotto-vaihtoehto provision arvon laskennan perusteena.    
35. Lisää Provisioprosentti-kenttään numero.
36. Valitse Tallenna.

## <a name="setting-up-commission-posting"></a>Provision kirjauksen määrittäminen
1. Valitse Myynti ja markkinointi > Provisiot > Provision kirjaus.
    * Provisiot maksetaan työntekijöille, joten ne on määritettävä varmistamaan, että taloudellinen kirjaus tehdään oikein asianmukaisille tileille kirjanpidossa. Se tehdään Provision kirjaus -sivulle. Tarkista nykyisessä yrityksessä käytettävissä oleva asetus. Yleensä provisiosummat kirjataan erityiskulutilille ja vastakirjataan erityisostoreskontraan. Jos et ole määrittänyt provision kirjaussääntöjä, järjestelmä ei suorita provisioon oikeuttavien myyntitilausten laskutusta.  
2. Sulje sivu.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Määritä provisioryhmä asiakkaaseen ja tuotteeseen
1. Valitse Myynti ja markkinointi > Asiakkaat > Kaikki asiakkaat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse Muokkaa.
5. Laajenna Oletusmyyntitilaukset-osa.
6. Avaa haku napsauttamalla Provisioryhmä-kentässä avattavan valikon painiketta.
7. Valitse luettelosta aiemmin luomasi ryhmä.
8. Avaa haku napsauttamalla Myyntiryhmä-kentässä avattavan valikon painiketta.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Valitse Tallenna.
11. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
12. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla T0020.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Valitse Muokkaa.
15. Laajenna Myynti-osa.
16. Avaa haku napsauttamalla Provisioryhmä-kentässä avattavan valikon painiketta.
17. Etsi ja valitse luettelosta aiemmin luomasi provisioryhmä.


