---
title: Vähittäismyynnin laskelmien maksun konfiguraatiot
description: Tässä menettelyssä esitellään Commercen maksutavat, jotka vaikuttavat Commercen laskelmien luomiseen ja kirjaamiseen.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8723f786c2eaf5f045007de32ce5cbe57563eaf9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205694"
---
# <a name="payment-configurations-for-retail-statements"></a>Vähittäismyynnin laskelmien maksun konfiguraatiot

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään Commercen maksutavat, jotka vaikuttavat Commercen laskelmien luomiseen ja kirjaamiseen.

Tässä tallenteessa käytetään esittely-yritystä USRT.

1. Valitse Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]