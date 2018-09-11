--- 
title: "Projektilaskujen maksukuitin muodon määrittäminen"
description: "Yritykset liittävät usein asiakkaiden laskuihin tulostetun maksutositteen, jossa on maksuviite kirjaamista ja tilitystä varten."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9700571110a1b488e250dd8ee7b8c5c8f15cbc01
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Projektilaskujen maksukuitin muodon määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Yritykset liittävät usein asiakkaiden laskuihin tulostetun maksutositteen, jossa on maksuviite kirjaamista ja tilitystä varten. Maksutositetta voidaan käyttää myynti- ja vapaatekstilaskujen lisäksi projekti- tai palvelulaskuissa, maksukehotteissa, korkolaskussa ja tiliotteissa. Maksutositteiden käsittelyssä määritetään ensiksi laskuttajan tunnusnumeroja maksutositteen liitemuodot.

Näissä toimintaohjeissa käytetään esittely-yritystä DEMF. 

Toiminto on niiden yritysten käytettävissä, joiden ensisijainen osoite on Tanskassa.


## <a name="set-up-a-creditor-id-number"></a>Määritä laskuttajan tunnusnumero
1. Siirry kohtaan Organisaation hallinto > Organisaatiot > Yritykset.
2. Laajenna tai tiivistä Pankkitilin tiedot -osa.
3. Valitse Muokkaa.
4. Kirjoita FI – Laskuttajan tunnus -kenttään arvo.
5. Valitse Tallenna.
6. Sulje sivu.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Määritä laskujen, kehotusten ja ilmoitusten maksutosite
1. Valitse Myyntireskontra > Asetukset > Lomakkeet > Lomakeasetukset.
2. Valitse Lasku-välilehti.
3. Valitse Asiakkaan laskun liittyvä maksun liite -kentässä vaihtoehto.
    * Ei mitään – Älä tulosta maksutositetta. Valitse tämä vaihtoehto, jos maksun summan valuutta on muu kuin Tanskan kruunu (DKK).   FIK 751 – Tulosta FIK 751 -maksutosite, jos aiot kirjoittaa maksun summan ja eräpäivän manuaalisesti maksutositteeseen.   FIK 752 – Tulosta FIK 752 -maksutosite, jos aiot käyttää tietokoneen luomaa maksutositetta, jossa on esipainettu maksun summa ja eräpäivä.  
4. Valitse Tallenna.
5. Valitse Vapaatekstilasku-välilehti.
6. Valitse Liittyvän maksun liite vapaatekstilaskussa -kentässä vaihtoehto.
    * Ei mitään – Älä tulosta maksutositetta. Valitse tämä vaihtoehto, jos maksun summan valuutta on muu kuin Tanskan kruunu (DKK).   FIK 751 – Tulosta FIK 751 -maksutosite, jos aiot kirjoittaa maksun summan ja eräpäivän manuaalisesti maksutositteeseen.   FIK 752 – Tulosta FIK 752 -maksutosite, jos aiot käyttää tietokoneen luomaa maksutositetta, jossa on esipainettu maksun summa ja eräpäivä.  
7. Valitse Tallenna.
8. Valitse Korkolasku-välilehti.
9. Valitse Liittyvän maksun liite korkolaskussa -kentässä vaihtoehto.
    * Ei mitään – Älä tulosta maksutositetta. Valitse tämä vaihtoehto, jos maksun summan valuutta on muu kuin Tanskan kruunu (DKK).   FIK 751 – Tulosta FIK 751 -maksutosite, jos aiot kirjoittaa maksun summan ja eräpäivän manuaalisesti maksutositteeseen.   FIK 752 – Tulosta FIK 752 -maksutosite, jos aiot käyttää tietokoneen luomaa maksutositetta, jossa on esipainettu maksun summa ja eräpäivä.  
10. Valitse Tallenna.
11. Valitse Maksukehotus-välilehti.
12. Valitse Liittyvän maksun liite maksukehotuksessa -kentässä vaihtoehto.
    * Ei mitään – Älä tulosta maksutositetta. Valitse tämä vaihtoehto, jos maksun summan valuutta on muu kuin Tanskan kruunu (DKK).   FIK 751 – Tulosta FIK 751 -maksutosite, jos aiot kirjoittaa maksun summan ja eräpäivän manuaalisesti maksutositteeseen.   FIK 752 – Tulosta FIK 752 -maksutosite, jos aiot käyttää tietokoneen luomaa maksutositetta, jossa on esipainettu maksun summa ja eräpäivä.  
13. Valitse Tallenna.
14. Valitse Tiliote-välilehti.
15. Valitse Liittyvän maksun liite tiliotteessa -kentässä vaihtoehto.
    * Ei mitään – Älä tulosta maksutositetta. Valitse tämä vaihtoehto, jos maksun summan valuutta on muu kuin Tanskan kruunu (DKK).   FIK 751 – Tulosta FIK 751 -maksutosite, jos aiot kirjoittaa maksun summan ja eräpäivän manuaalisesti maksutositteeseen.   FIK 752 – Tulosta FIK 752 -maksutosite, jos aiot käyttää tietokoneen luomaa maksutositetta, jossa on esipainettu maksun summa ja eräpäivä.  
16. Valitse Tallenna.
17. Sulje sivu.


