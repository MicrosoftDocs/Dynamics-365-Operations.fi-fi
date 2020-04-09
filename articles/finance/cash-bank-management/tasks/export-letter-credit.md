---
title: Vientiremburssit
description: Tässä menettelyssä käsitellään vientiremburssiprosessi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cd18320ca8505b1357ce505dfb4c94e81aaae91
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141646"
---
# <a name="export-letter-of-credit"></a>Vientiremburssit

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään vientiremburssiprosessi.

Remburssi on pankin antama sopimus, jossa pankki suostuu varmistamaan maksun ostajan puolesta, jos ostajan ja myyjän väliset ehdot täyttyvät.



Suorittaa Määritä pankin limiitit ja kirjausprofiilit - ja Luo pankin limiittisopimus remburssia varten -menettelyt ennen tätä menettelyä. USMF-demoyritys on oltava valittuna, muuten menettelyn suorittaminen ei onnistu.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Luo myyntitilaus vientiremburssille
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Laajenna tai tiivistä Yleiset-osa.
7. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
    * Valitse toimipaikka, johon otettava nimike on varastoitu.  
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
    * Valitse varasto, johon otettava nimike on varastoitu.  
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Huomautus: Pankkitositteen tyyppi -kenttään on valittava arvo Remburssi.  
11. Valitse Pankkitositteen tyyppi -kentässä Remburssi.
12. Laajenna tai tiivistä Toimitus-osa.
    * Valitse Toimituspäivän tarkistus = Ei mitään.  
13. Kirjoita päivämäärä Pyydetty vastaanottopäivämäärä -kenttään.
14. Valitse OK.
15. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
    * Valitse otettava tai myytävä pakollinen nimike.  
16. Etsi haluamasi tietue luettelosta ja valitse se.
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Syötä Yksikköhinta-kenttään numero.
19. Laajenna tai tiivistä Rivitiedot-osa.
20. Valitse Toimitus-välilehti.
21. Kirjoita päivämäärä Pyydetty lähetyspäivämäärä -kenttään.
22. Kirjoita päivämäärä Vahvistettu lähetyspäivämäärä -kenttään.
23. Valitse toimintoruudussa Hallitse.
24. Valitse Remburssi.
25. Kirjoita arvo Pankkitositteen numero -kenttään.
26. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
27. Laajenna tai tiivistä Pankin tiedot -osa.
28. Avaa haku napsauttamalla Liikkeelle laskeva pankki -kentässä avattavan valikon painiketta.
29. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
30. Avaa haku napsauttamalla Neuvova pankki -kentässä avattavan valikon painiketta.
31. Etsi haluamasi tietue luettelosta ja valitse se.
32. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
33. Valitse Hae myyntitilauksen lähetykset.
34. Valitse Liikkeeseen laskevan pankin asiakirja.
35. Sulje sivu.

## <a name="post-packing-slip"></a>Kirjaa pakkausluettelo
1. Valitse toimintoruudussa Kerää ja pakkaa.
2. Valitse Kirjaa pakkausluettelo.
3. Laajenna tai tiivistä Parametrit-osa.
4. Valitse Määrä-kentässä Kaikki.
5. Laajenna tai tiivistä Asetukset-osa.
6. Kirjoita päivämäärä Pakkausluettelon päiväys -kenttään.
7. Valitse Lähetyksen numero.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse OK.
10. Valitse OK.

## <a name="post-sales-invoice"></a>Kirjaa myyntilasku
1. Valitse toimintoruudussa Lasku.
2. Valitse Lasku.
3. Laajenna tai tiivistä Yhteenveto-osa.
4. Valitse Lähetyksen numero.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Laajenna tai tiivistä Asetukset-osa.
7. Kirjoita päivämäärä Laskun päivämäärä -kenttään.
8. Valitse OK.
9. Valitse OK.

## <a name="shipment-document-submitted-status"></a>Lähetysasiakirjojen lähetystila
1. Valitse toimintoruudussa Hallitse.
2. Valitse Remburssi.
3. Laajenna tai tiivistä Rivit-osa.
    * Huomautus: Asiakirja lähetetty -kentässä on oltava valittuna Kyllä.  

## <a name="verify-export-letter-of-credit"></a>Tarkista vientiremburssi
1. Valitse Maksuliikenteen hallinta > Luottokirjeet > Vientiremburssi ja tuontiperintä.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tarkista, vientiremburssin lähetyksen tila on Laskutettu.  

## <a name="customer-payment"></a>Asiakkaan maksu
1. Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse Rivit.
7. Syötä Päivämäärään-kenttään päivämäärä.
8. Määritä Tili-kenttään haluamasi arvot.
9. Valitse Tilitys.
10. Valitse Summat-otsikon valintaruutu.
    * Huomautus: valitse Näytä-kentän asetukseksi Remburssi.  
11. Etsi haluamasi tietue luettelosta ja valitse se.
12. Valitse Merkitse-valintaruutu tai poista sen valinta.
13. Valitse OK.
14. Valitse Maksu-välilehti.
    * Tarkista Pankkitositteen numero- ja Lähetyksen numero -asetusten tiedot  
15. Valitse Kirjaa.

## <a name="verify-export-letter-of-credit-after-payment"></a>Tarkista vientiremburssi maksun jälkeen
1. Valitse Maksuliikenteen hallinta > Luottokirjeet > Vientiremburssi ja tuontiperintä.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Tarkista, että Lähetyksen tila = Maksu vastaanotettu ja saldon summa = 0,00.  

