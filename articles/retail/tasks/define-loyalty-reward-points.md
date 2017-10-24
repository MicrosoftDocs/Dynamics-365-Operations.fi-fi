--- 
title: "Määritä kanta-asiakkaan palkkiopisteet"
description: "Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen."
author: scott-tucker
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
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05237a0ba3aa785432c8b1fc36284a47f9aabd4a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-reward-points"></a>Määritä kanta-asiakkaan palkkiopisteet

[!include[task guide banner](../includes/task-guide-banner.md)]

Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen. Määritä kanta-asiakkaan palkkiopisteet ennen kanta-asiakkuusohjelman määrittämistä. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Vähittäismyynti ja kauppa > Asiakkaat> Kanta-asiakkaat> Kanta-asiakkaan palkkiopisteet.
2. Valitse Uusi.
3. Syötä Palkkiopisteen tunnus -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Palkkiopisteen tyyppi -kentässä vaihtoehto.
    * Valitse määrä, jos haluat pyöristää palkkiopisteet seuraavaan kokonaislukuun. Valitse Summa, jos haluat pyöristää palkkiopisteet valuutan pyöristyssääntöjen mukaan. Jos valitse Määrä, ohita menettelyn seuraava vaihe.  
6. Kirjoita arvo Valuutta-kenttään.
    * Jos palkkiopisteiden tyyppi on Summa, myönnetyille pisteille määritetään valittu valuutta. Jos palkkiopisteiden tyyppi on Määrä, tämä kenttä ei ole käytössä. Voit ohittaa tämän vaiheen.  
7. Valitse Lunastettavissa-valintaruutu tai poista sen valinta.
8. Syötä Lunasta sijoitus -kenttään numero.
    * Lunasta sijoitus -kohtaa käytetään, kun tuotteiden maksamisessa voidaan käyttää kahta tai useampaa lunastettavaa palkkiopistettä. Jos kahdella palkkiopisteellä on sama lunastusluokittelu, käytetään sitä, jonka pisteiden määrää tulee vähentää.  
9. Syötä Vanhentumisajan arvo -kenttään numero.
    * Palkkiopisteet vanhenevat määritettyjen päivien, kuukausien tai vuosien kuluttua siitä, kun pisteet on myönnetty. Arvo 0 tarkoittaa, että kanta-asiakkaan palkkiopisteet eivät vanhene koskaan.  
10. Valitse Vanhentumisajan yksikkö -kenttään vaihtoehto.
11. Valitse Tallenna.


