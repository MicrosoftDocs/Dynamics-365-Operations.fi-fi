---
title: Takausasiakirjan tapahtuma
description: Tässä menettelyssä käsitellään takuuasiakirjaprosessi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566849cfcedd29f4bb92d08a17b67e16b1cbc372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225366"
---
# <a name="letter-of-guarantee-transaction"></a>Takausasiakirjan tapahtuma

[!include [banner](../../includes/banner.md)]

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

## <a name="process-letter-of-guarantee_request"></a>Käsittele takausasiakirja_Pyyntö
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

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Käsittele takausasiakirja_Lähetä pankille
1. Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Avaa valintaikkuna valitsemalla Lähetä pankille.
4. Syötä tai valitse arvo Pankkitili-kentässä.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse OK.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Käsittele takausasiakirja_Ota vastaan pankista
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

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Käsittele takausasiakirja_Anna edunsaajalle
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

## <a name="process-letter-of-guarantee_increase-value"></a>Käsittele takausasiakirja_Kasvata arvoa
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

## <a name="process-letter-of-guarantee_liquidate"></a>Käsittele takausasiakirja_Realisoi
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]