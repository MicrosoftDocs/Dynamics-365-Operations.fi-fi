--- 
title: "Sähköisten maksuasiakirjojen luominen käyttämällä muotokonfiguraatiota sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi käyttää uutta sähköisen raportoinnin (ER) muotokonfiguraatiota maksukäsittelyn sähköisten asiakirjojen luomiseen."
author: NickSelin
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
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Sähköisten maksuasiakirjojen luominen käyttämällä muotokonfiguraatiota sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi käyttää uutta sähköisen raportoinnin (ER) muotokonfiguraatiota maksukäsittelyn sähköisten asiakirjojen luomiseen. Nämä vaiheet voidaan suorittaa GBSI-esimerkkiyrityksessä.

Konfiguraation luominen, joka sisältää maksuasiakirjan muodon -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Vaihda sähköisen maksutavan konfiguraatio
1. Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.
2. Laajenna tiedostomuodon valinta tarvittaessa.
3. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Maksutapa-kenttää arvolla Sähköinen.
4. Valitse Muokkaa.
5. Aseta Yleinen sähköinen raportointi -kentän arvoksi Kyllä.
    * Valitse Kyllä käyttääksesi yleistä sähköisen raportoinnin mallia maksutiedostojen luonnissa.  
6. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
7. Valitse BACS-muotokonfiguraatio (Iso-Britannia, kuvitteellinen).
8. Valitse Tallenna.
9. Sulje sivu.

## <a name="test-the-format-of-generated-payment-files"></a>Testaa luotujen maksutiedostojen muoto
1. Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse VendPay.  
6. Valitse Tallenna.
7. Valitse Rivit.
8. Kirjoita Yritys-kenttän arvoksi "DEMF".
    * DEMF  
9. Määritä Tili-kentässä arvoksi DE-01001.
    * DE - 01001  
10. Kirjoita Kuvaus-kentän arvoksi Maksu.
    * Maksu  
11. Syötä Debet-kenttään numero.
    * 1 000  
12. Valitse Maksu-välilehti.
13. Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.
14. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse arvoksi Sähköinen.  
15. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
16. Valitse Tallenna.
17. Valitse Muodosta maksut.
18. Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.
19. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse arvoksi Sähköinen.  
20. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse arvoksi Sähköinen.  
21. Kirjoita arvo Tiedostonimi-kenttään.
    * Kirjoita esimerkiksi Maksut.  
22. Avaa haku valitsemalla Pankkitili-kentässä avattavan valikon painike.
23. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse arvoksi GBSI OPER.  
24. Valitse OK.
25. Valitse OK.
    * Analysoi luotu, XML-muotoinen maksutiedosto. Vertaa tiedostoa suunniteltuun asiakirjan asetteluun ja määriteltyihin maksutapahtuman määritteisiin.  


