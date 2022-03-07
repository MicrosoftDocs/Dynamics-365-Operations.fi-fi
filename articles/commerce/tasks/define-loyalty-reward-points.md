---
title: Määritä kanta-asiakkaan palkkiopisteet
description: Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 509db13f1bae9f41537a5d91aeba862ed2e4291d72739e83e22fb860791d6355
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738669"
---
# <a name="define-loyalty-reward-points"></a>Määritä kanta-asiakkaan palkkiopisteet

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen. Määritä kanta-asiakkaan palkkiopisteet ennen kanta-asiakkuusohjelman määrittämistä. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Retail ja Commerce > Asiakkaat> Kanta-asiakkaat> Kanta-asiakkaan palkkiopisteet.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]