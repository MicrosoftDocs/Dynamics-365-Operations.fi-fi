---
title: Kirjaa kausittaiset kirjauskansiot
description: Kausikirjauskansioita kutsutaan joskus toistuviksi kirjauskansioiksi, koska summa, teksti ja muut tiedot toistetaan aina kausikirjauskansion haun yhteydessä.
author: aprilolson
ms.date: 11/21/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc1d9f67a515e3cdc45e173b88982feceb0ebfd
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799364"
---
# <a name="post-periodic-journals"></a>Kirjaa kausittaiset kirjauskansiot

[!include [banner](../../includes/banner.md)]

Kausikirjauskansioita kutsutaan joskus toistuviksi kirjauskansioiksi, koska summa, teksti ja muut tiedot toistetaan aina kausikirjauskansion haun yhteydessä. Kausikirjauskansion luomisen yhteydessä määritetään toistumisen kausiväli, kuten päivät tai kuukaudet. Tässä tehtävän ohjauksessa luodaan kausikirjauskansio, jonka toiston kausiväli on kuukausi.

1. Valitse **siirtymisruutu > Moduulit > Kirjanpito > Kausittaiset tehtävät > Kausikirjauskansiot**.
2. Valitse **Uusi**.
3. Anna tai valitse arvo **Nimi**-kentässä.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita **Kuvaus**-kenttään arvo. Kuvaus on myöhemmin haettavan kausikirjauskansion nimi, joten varmista, että annat sopivan nimen.
6. Valitse **toimintoruudussa** **Rivit**. Kausikirjauskansio sisältää yleensä useita kirjauskansion rivejä. Tässä tehtävän ohjauksessa lisätään kuitenkin vain yksi rivi.
7. Syötä **Päivämäärä**-kenttään päivämäärä. **Päivämäärä**-kenttä sisältää seuraavan kirjauskansioon siirron kirjauspäivämäärän. Jos kirjauskansio haetaan joka kuukausi, kannattaa käyttää kirjauskuukauden päivämäärää. Tämä on yleensä kauden ensimmäinen tai viimeinen päivämäärä. Käyttämällä **Tyhjä päivämäärä** -kenttää on mahdollista jättää **päivämäärä**-kenttä tyhjäksi ja antaa päivämäärä kirjauskansion haun yhteydessä. Kentän arvoksi päivitetään automaattisesti seuraava toistuva päivämäärä, kun tapahtumat haetaan. 
8. Määritä **Tili**-kenttään haluamasi arvot.
9. Valitse arvo kentässä **Kuvaus**.
10. Sulje sivu.
11. Syötä **Debet**-kenttään numero.
12. Määritä **Vastatili**-kenttään haluamasi arvot.
13. Valitse **Yksikkö**-kentässä **Kuukaudet**.
14. Syötä **Yksiköiden määrä**-kenttään **1**.
15. Syötä päivämäärä **Viimeinen päivämäärä** -kenttään. Edellisen kauden viimeisen päivämäärän syöttäminen estää toistuvan kirjauskansion luomisen vahingossa väärälle aloituskaudelle. Viimeinen päivämäärä päivitetään myöhemmin aina, kun kausikirjauskansio haetaan. 
16. Valitse **Tallenna**.
17. Siirry kohtaan **Siirtymisruutu > Moduulit > kirjanpito > kirjauskansioviennit > Yleiset kirjauskansiot**.
18. Valitse **Uusi**.
19. Anna tai valitse arvo **Nimi**-kentässä.
20. Etsi haluamasi tietue luettelosta ja valitse se.
21. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
22. Kirjoita **Kuvaus**-kenttään arvo.
23. Valitse **toimintoruudussa** **Rivit**.
24. Napsauta **Toimintoruudussa** **Kausikirjauskansio**.
25. Valitse **Nouda kirjauskansio**.
26. Kirjoita päivämäärä **Päivämäärään**-kenttään. **Loppupäivämäärä** toimii kausittaisen tositteen rivien katkaisupäivämääränä. Toistoasetuksen perusteella **viimeinen päivämäärä** ja **loppupäivämäärä** voidaan sisällyttää usean kerran samalle riville tuloksena olevassa kirjauskansiossa. **Loppupäivämääräksi** päivitetään automaattisesti sen istunnon päivämäärä, jonka aikana kausittainen rivi siirrettiin kirjauskansioon. 
27. Syötä tai valitse arvo **Kausikirjauskansion numero**-kenttään.
28. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
29. Valitse **OK**. Kausikirjauskansio voidaan nyt tarkistaa, hyväksyä tai kirjata tarpeiden ja asetusten perusteella.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
