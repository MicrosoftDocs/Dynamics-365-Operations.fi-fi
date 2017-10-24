--- 
title: Takausasiakirjan tapahtuma
description: "Tässä menettelyssä käsitellään takuuasiakirjaprosessi."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a>Takausasiakirjan tapahtuma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään takuuasiakirjaprosessi.



Seuraavat tehtävät on suoritettava, ennen kuin tämä menettely tehdään:

- Määritä pankin limiitit ja kirjausprofiilit takauskirjaa varten.

- Luo pankin limiittisopimus takausasiakirjaa varten.



Näissä toimintaohjeissa käytetään esittely-yritystä USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Luo myyntitilaus, jossa on takausasiakirja
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
4. Laajenna Yleinen-osa.
5. Syötä tai valitse arvo Toimipaikka-kenttään.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Anna tai valitse Varasto-kentässä arvo.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse Pankkitositteen tyyppi -kentässä Takausasiakirja.
10. Valitse OK.
11. Syötä tai valitse arvo Nimiketunnus-kentässä.
12. Syötä Yksikköhinta-kenttään numero.
13. Laajenna Rivin erittely -osa.
14. Valitse Toimitus-välilehti.
    * Huomautus: Valitse Toimituspäivän tarkistus = Ei mitään.  
15. Kirjoita päivämäärä Pyydetty lähetyspäivämäärä -kenttään.
16. Kirjoita päivämäärä Vahvistettu lähetyspäivämäärä -kenttään.

## <a name="process-letter-of-guaranteerequest"></a>Käsittele takausasiakirja_Pyyntö
1. Valitse toimintoruudussa Hallitse.
2. Valitse Takausasiakirja.
3. Valitse toimintoruudussa Takausasiakirja.
4. Avaa valintaikkuna valitsemalla Pyyntö.
5. Anna tai valitse Tyyppi-kentässä arvo.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Kirjoita numero Arvo-kenttään.
8. Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.
9. Valitse OK.
10. Sulje sivu.

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>Käsittele takausasiakirja_Lähetä pankille
1. Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Avaa valintaikkuna valitsemalla Lähetä pankille.
4. Syötä tai valitse arvo Pankkitili-kentässä.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse OK.

## <a name="process-letter-of-guaranteereceive-from-bank"></a>Käsittele takausasiakirja_Ota vastaan pankista
1. Avaa valintaikkuna valitsemalla Vastaanota pankilta.
2. Kirjoita arvo Pankin rekisteröintinumero -kenttään.
    * Tarkista Kate- ja Kulu-kentissä lasketut arvot.  
3. Valitse OK.
4. Laajenna Toiminnot-osa.
    * Tarkista Vastaanota pankilta -tietue.  
5. Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.
6. Valitse Rivit.
    * Tarkista kirjauskansiovientien kirjaus.  
7. Sulje sivu.

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>Käsittele takausasiakirja_Anna edunsaajalle
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
3. Valitse toimintoruudussa Hallitse.
4. Valitse Takausasiakirja.
5. Valitse toimintoruudussa Takausasiakirja.
6. Avaa valintaikkuna valitsemalla Anna edunsaajalle.
7. Valitse OK.
8. Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Avaa valintaikkuna valitsemalla Anna edunsaajalle.
11. Valitse OK.
12. Laajenna Toiminnot-osa.
    * Vahvista Anna edunsaajalle -tietue.  

## <a name="process-letter-of-guaranteeincrease-value"></a>Käsittele takausasiakirja_Kasvata arvoa
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
3. Valitse toimintoruudussa Hallitse.
4. Valitse Takausasiakirja.
5. Valitse toimintoruudussa Takausasiakirja.
6. Avaa valintaikkuna valitsemalla Kasvata arvoa.
7. Lisää Lisättävä arvo -kenttään numero.
8. Valitse OK.
9. Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.
10. Etsi haluamasi tietue luettelosta ja valitse se.
11. Avaa valintaikkuna valitsemalla Kasvata arvoa.
12. Valitse OK.
13. Laajenna Toiminnot-osa.
    * Tarkista Kasvata arvoa -tietue.  
14. Etsi haluamasi tietue luettelosta ja valitse se.
15. Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.
16. Valitse Rivit.
    * Tarkista kirjatut kirjauskansioviennit.  

## <a name="process-letter-of-guaranteeliquidate"></a>Käsittele takausasiakirja_Realisoi
1. Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.
2. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
3. Valitse toimintoruudussa Hallitse.
4. Valitse Takausasiakirja.
5. Valitse toimintoruudussa Takausasiakirja.
6. Avaa valintaikkuna valitsemalla Realisoi.
7. Valitse OK.
8. Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Avaa valintaikkuna valitsemalla Realisoi.
11. Valitse OK.
12. Laajenna Toiminnot-osa.
    * Tarkista Realisoi-tietue.  
13. Etsi haluamasi tietue luettelosta ja valitse se.
14. Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.
15. Valitse Rivit.
    * Tarkista kirjatut kirjauskansioviennit.  
16. Sulje sivu.


