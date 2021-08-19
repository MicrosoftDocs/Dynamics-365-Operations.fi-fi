---
title: Luo suoraveloitusvaltakirja asiakkaalle
description: Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51fea2b9a0f25b078abc3ca83ee02c585eaf465128bebba0234ffadb030ef42a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740047"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Luo suoraveloitusvaltakirja asiakkaalle

[!include [banner](../../includes/banner.md)]

Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.


## <a name="create-a-bank-account"></a>Pankkitilin luominen
1. Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.
2. Valitse luettelosta tietue. Voit valita esimerkiksi arvon US-001
3. Valitse toimintoruudussa **Asiakas**.
4. Valitse **Pankkitilit**.
5. Valitse **Uusi**.
6. Kirjoita arvo **Pankkitili**-kenttään.
7. Kirjoita arvo **Nimi**-kenttään.
8. Syötä arvon **IBAN**-kenttään.
9. Kirjoita arvo **Valuutta**-kenttään.
10. Valitse **Tallenna**.
11. Sulje sivu.
12. Siirry **siirtymisruudussa** kohtaan **Moduulit > Maksuliikenteen hallinta > pankkitilit > pankkitilit.**
13. Etsi haluamasi tietue luettelosta ja valitse se.
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
15. Valitse **Muokkaa**.
16. Laajenna **Lisätunnus**-pikavälilehti.
17. Syötä **Suoraveloitustunnus**-kenttään arvo.
18. Syötä arvon **IBAN**-kenttään.
19. Sulje sivu.
20. Sulje sivu.

## <a name="define-the-electronic-payment-method"></a>Sähköisen maksutavan määrittäminen
1. Siirry kohtaan **Siirtymisruutu** **> Moduulit > Myyntireskontra >Maksujen asetukset > Maksutavat**.
2. Valitse **Uusi**.
3. Syötä arvo **Maksutapa**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Maksutyyppi**-kentässä Sähköinen maksu. Suoraveloitusvaltakirjan maksutavan maksutyypin on oltava Sähköinen maksu.
6. Valitse **Vaadi valtakirjaa** -kentässä Kyllä.
7. Sulje sivu.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Lisää suoraveloitusvaltakirja asiakkaalle.
1. Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.
2. Valitse luettelosta tietue. Voit valita esimerkiksi arvon US-001
3. Valitse **Muokkaa**.
4. Laajenna **Oletusmaksut**-pikavälilehti.
5. Anna tai valitse arvo **Maksutapa**-kentässä.
6. Laajenna **Oletusmaksut**-pikavälilehti.
7. Laajenna **Suoraveloitusvaltakirjat**-pikavälilehti.
8. Valitse **Lisää**.
9. Anna tai valitse arvo **Pankkitili**-kentässä.
10. Syötä tai valitse arvo **Laskuttajan pankkitili** -kentässä.
11. Syötä **Maksun toistuvuus** -kenttään niiden maksujen määrä, jotka odotat käsiteltäväksi tämän valtakirjan osalta.
12. Valitse **OK**.
13. Valitse **Tulosta**.
14. Valitse **Valtakirjaraportti**.
15. Sulje sivu.
16. Valitse **Muokkaa**.
17. Syötä päivämäärä **Allekirjoituksen päivämäärä** -kenttään.
18. Valitse **Kyllä**.
19. Syötä paikka, jossa valtakirja on allekirjoitettu.
20. Valitse **OK**.
21. Sulje sivu.

## <a name="create-a-free-text-invoice-with-mandate"></a>Vapaatekstilaskun ja valtakirjan luominen
1. Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Laskut > Kaikki vapaamuotoiset laskut**.
2. Valitse **Uusi**.
3. Valitse asiakas, jolle valtakirja lisättiin.
4. Anna tai valitse **Suoraveloitusvaltakirjan tunnus** -kentässä arvo.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]