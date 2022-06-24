---
title: ER Luo sähköisiä maksuasiakirjoja muotokokoonpanon avulla
description: Tässä artikkelissa käsitellään uuden sähköisen raportoinnin (ER) muotomäärityksen käyttöä luomaan sähköisten asiakirjojen luontia maksujen käsittelyä varten.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a79c32372402fcd49f20c855cbfa8d9bcd8ba524
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864598"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER Luo sähköisiä maksuasiakirjoja muotokokoonpanon avulla

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]