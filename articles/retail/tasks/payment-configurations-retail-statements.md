--- 
title: "Vähittäismyynnin laskelmien maksun konfiguraatiot"
description: "Tässä menettelyssä esitellään vähittäismyymälän maksutavat, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f12d8ac9be11b92eaef4acce094ae183906278d4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a>Vähittäismyynnin laskelmien maksun konfiguraatiot

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä esitellään vähittäismyymälän maksutavat, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.

Tässä tallenteessa käytetään esittely-yritystä USRT.

1. Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse toimintoruudussa Määritä.
5. Valitse Maksutavat.
6. Laajenna tai tiivistä Kirjaus-osa.
7. Valitse Muokkaa.
    * Määritä, kirjataanko tälle maksulle vastaanotettavat summat kirjanpitotilille vai pankkitilille.  
    * Valitse tili, jolle tämän maksutavan vastaanotetut summat kirjataan.  
    * Valitse tili, jolle vastaanotettujen tapahtumien kokonaissumman ja tälle maksutavalle lasketun summan mahdolliset erot kirjataan.  
    * Tähän kenttään voi syöttää summan, joka määrittää, milloin erosumma tulee kirjata toiselle erotilille. Tätä voi käyttää suurien erojen seurannassa.  
    * Valitse tili, jolle vastaanotettujen tapahtumien kokonaissumman ja lasketun summan väliset erot kirjataan, kun ero ylittää Eron enimmäissumma -kentässä määritetyn arvo.  
    * Valitse Kyllä, kun pankkiin toimitettavat summat kirjataan erilliselle tilille.  
    * Tässä kentässä voit määrittää, kirjataanko pankkiin toimitettavat summat kirjanpitotilille vai pankkitilille.  
    * Valitse tili, jolle pankkiin toimitettavat summat kirjataan.  
    * Valitse pankkitapahtuman tyyppi, jota käytetään, kun pankkiin toimitettavat summat kirjataan pankkitilille.  
    * Valitse Kyllä, kun kassakaappiin toimitettavat summat kirjataan erilliselle tilille.  
    * Määritä, kirjataanko kassakaappiin toimitettavat summat kirjanpitotilille vai pankkitilille.  
    * Valitse tili, jolle kassakaappiin toimitettavat summat kirjataan.  
8. Valitse Tallenna.

