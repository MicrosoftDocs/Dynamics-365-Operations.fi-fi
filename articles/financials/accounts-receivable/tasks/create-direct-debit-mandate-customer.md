--- 
title: Luo suoraveloitusvaltakirja asiakkaalle
description: "Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Luo suoraveloitusvaltakirja asiakkaalle

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.


## <a name="create-a-bank-account"></a>Pankkitilin luominen
1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Voit valita esimerkiksi arvon US-001
3. Valitse toimintoruudussa Asiakas.
4. Valitse Pankkitilit.
5. Valitse Uusi.
6. Kirjoita arvo Pankkitili-kenttään.
7. Kirjoita arvo Nimi-kenttään.
8. Syötä arvon IBAN-kenttään.
9. Kirjoita arvo Valuutta-kenttään.
10. Valitse Tallenna.
11. Sulje sivu.
12. Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.
13. Etsi haluamasi tietue luettelosta ja valitse se.
14. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
15. Valitse Muokkaa.
16. Laajenna Lisätunnus-osa.
17. Syötä Suoraveloitustunnus-kenttään arvo.
18. Syötä arvon IBAN-kenttään.
19. Sulje sivu.
20. Sulje sivu.

## <a name="define-the-electronic-payment-method"></a>Sähköisen maksutavan määrittäminen
1. Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksutavat.
2. Valitse Uusi.
3. Syötä arvo Maksutapa-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Suoraveloitusvaltakirjan maksutavan maksutyypin on oltava Sähköinen maksu.
6. Valitse Vaadi valtakirjaa -kentässä Kyllä.
7. Sulje sivu.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Lisää suoraveloitusvaltakirja asiakkaalle.
1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Voit valita esimerkiksi arvon US-001
3. Valitse Muokkaa.
4. Laajenna Oletusmaksut-osa.
5. Anna tai valitse arvo Maksutapa-kentässä.
6. Laajenna Oletusmaksut-osa.
7. Laajenna Suoraveloitusvaltakirjat-osa.
8. ValitseLisää.
9. Syötä tai valitse arvo Pankkitili-kentässä.
10. Syötä tai valitse arvo Laskuttajan pankkitili -kentässä.
11. Syötä niiden maksujen määrä, jotka odotat käsiteltäväksi tämän valtakirjan osalta.
12. Valitse OK.
13. Valitse Tulosta.
14. Valitse Valtakirjaraportti.
15. Sulje sivu.
16. Valitse Muokkaa.
17. Syötä päivämäärä Allekirjoitus-kenttään.
18. Valitse Kyllä.
19. Syötä paikka, jossa valtakirja on allekirjoitettu.
20. Valitse OK.
21. Sulje sivu.

## <a name="create-a-free-text-invoice-with-mandate"></a>Vapaatekstilaskun ja valtakirjan luominen
1. Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.
2. Valitse Uusi.
3. Valitse asiakas, jolle valtakirja lisättiin.
4. Anna tai valitse Suoraveloitusvaltakirjan tunnus -kentässä arvo.


