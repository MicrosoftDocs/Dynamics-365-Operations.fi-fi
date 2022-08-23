---
title: Määritä kanta-asiakkaan palkkiopisteet
description: Tässä menettelyssä esitellään kanta-asiakkaan palkkiopisteiden määrittäminen.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailLoyaltyRewardPoints
ms.openlocfilehash: 9acd1429d17393f19a5e059b90a48b0b103535d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268889"
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
