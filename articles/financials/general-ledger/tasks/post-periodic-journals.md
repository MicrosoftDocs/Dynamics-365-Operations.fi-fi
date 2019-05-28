---
title: Kirjaa kausittaiset kirjauskansiot
description: Kausikirjauskansioita kutsutaan joskus toistuviksi kirjauskansioiksi, koska summa, teksti ja muut tiedot toistetaan aina kausikirjauskansion haun yhteydessä.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deae523d922e1d6a4f7bb05433e9b1568c9c1ee9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562227"
---
# <a name="post-periodic-journals"></a>Kirjaa kausittaiset kirjauskansiot

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kausikirjauskansioita kutsutaan joskus toistuviksi kirjauskansioiksi, koska summa, teksti ja muut tiedot toistetaan aina kausikirjauskansion haun yhteydessä. Kausikirjauskansion luomisen yhteydessä määritetään toistumisen kausiväli, kuten päivät tai kuukaudet. Tässä tehtävän ohjauksessa luodaan kausikirjauskansio, jonka toiston kausiväli on kuukausi.



1. Siirry kohtaan Kirjanpito > Kausittaiset tehtävät > Kausikirjauskansiot.
2. Valitse Uusi.
3. Syötä tai valitse arvo Nimi-kenttään.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita arvo Kuvaus-kenttään.
    * Kuvaus on myöhemmin haettavan kausikirjauskansion nimi, joten varmista, että annat sopivan nimen.  
6. Valitse Rivit.
    * Kausikirjauskansio sisältää yleensä useita kirjauskansion rivejä. tässä tehtävän ohjauksessa lisätään kuitenkin vain yksi rivi.  
7. Syötä Päivämäärään-kenttään päivämäärä.
    * Päivämäärä-kenttä sisältää seuraavan kirjauskansioon siirron kirjauspäivämäärän. Jos kirjauskansio haetaan joka kuukausi, kannattaa käyttää kirjauskuukauden päivämäärää. Yleensä se on kauden ensimmäinen tai viimeinen päivä. Päivämäärä-kentän voi jättää tyhjäksi, jolloin päivämäärä annetaan kirjauskansion haun yhteydessä Tyhjä päivämäärä -kentän avulla.    Kentän arvoksi päivitetään automaattisesti seuraava toistuva päivämäärä, kun tapahtumat haetaan.  
8. Määritä Tili-kenttään haluamasi arvot.
9. Kirjoita arvo Kuvaus-kenttään.
10. Sulje sivu.
11. Syötä Debet-kenttään numero.
12. Määritä Vastatili-kenttään haluamasi arvot.
13. Valitse Yksikkö-kentässä Kuukaudet.
14. Syötä Yksiköiden määrä -kenttään 1.
15. Syötä päivämäärä Viimeinen päivämäärä -kenttään.
    * Edellisen kauden viimeisen päivämäärän syöttäminen estää toistuvan kirjauskansion luomisen vahingossa väärälle aloituskaudelle. Viimeinen päivämäärä päivitetään myöhemmin aina, kun kausikirjauskansio haetaan.  
16. Valitse Tallenna.
17. Siirry oletuskoontinäyttöön.
18. Siirry kohtaan Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.
19. Valitse Uusi.
20. Syötä tai valitse arvo Nimi-kenttään.
21. Etsi haluamasi tietue luettelosta ja valitse se.
22. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
23. Kirjoita arvo Kuvaus-kenttään.
24. Valitse Rivit.
25. Valitse kausikirjauskansio.
26. Valitse Nouda kirjauskansio.
27. Kirjoita päivämäärä Päivämäärään-kenttään.
    * Loppupäivämäärä toimii kausittaisen tositteen rivien katkaisupäivämääränä. Toistoasetuksen perusteella viimeinen päivämäärä- ja loppupäivämäärä voidaan sisällyttää usean kerran samalle riville tuloksena olevassa kirjauskansiossa. Loppupäivämääräksi päivitetään automaattisesti sen istunnon päivämäärä, jonka aikana kausittainen rivi siirrettiin kirjauskansioon.  
28. Syötä tai valitse arvo Kausikirjauskansio-kenttään.
29. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
30. Valitse OK.
    * Kausikirjauskansio voidaan nyt tarkistaa, hyväksyä tai kirjata tarpeiden ja asetusten perusteella.  

