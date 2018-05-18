--- 
title: "Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten"
description: "Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa. On mahdollista käyttää automaattista uudelleenkohdistusta, jossa tavarat noudetaan toisesta sijainnista, jossa ne ovat saatavilla, sijaintidirektiivien avulla. Vaihtoehtona, jos käytössä on manuaalinen uudelleenkohdistus, mobiililaitteella voidaan näyttää luettelo sijainneista, joissa tarvittu määrä on saatavilla, jolloin varastotyöntekijä voi valita käytettävän sijainnin. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="set-up-work-exceptions"></a>Määritä työn poikkeukset
1. Siirry kohtaan Varastonhallinta > Asetukset > Työ > Työn poikkeukset.
2. Valitse Uusi.
    * On mahdollista määrittää useita työn poikkeuksia, joilla on eri nimikkeen uudelleenkohdistuskäytännöt, joista varaston työntekijä voi valita käsittelyssä olevan lähetyksen tarpeisiin sopivan.  
3. Kirjoita Työn poikkeuskoodi -kenttään arvo.
    * Anna työn poikkeukselle nimi, joka ilmaisee, mitä varten se on. Esimerkiksi, Lyhyt keräily käsin.  
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Poikkeustyyppi-kenttään "Lyhyt keräily".
6. Valitse Varaston oikaiseminen -valintaruutu.
    * Tämä vaihtoehto tarkoittaa, että varaston arvoksi asetetaan automaattisesti 0 lyhyen keräilyn sijainnissa.  
7. Syötä tai valitse arvo Oikaisutyypin oletuskoodi -kentässä.
    * Esimerkiksi USMF-yrityksessä voit valita "Poista Res Adj Out".  
8. Valitse Nimikkeen uudelleenkohdistus -kentässä Manuaalinen.
    * Jos valitset asetukseksi Manuaalinen tai Automaattinen ja manuaalinen, varastotyöntekijän on voitava käyttää manuaalista uudelleenkohdistusta.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Määritä manuaalinen nimikkeiden uudelleenkohdistus työntekijän käyttöön
1. Sulje sivu.
2. Siirry kohtaan Varastonhallinta > Asetukset > Työntekijä.
3. Valitse Muokkaa.
4. Valitse luettelosta työntekijä 24.
5. Laajenna Työ-osa.
6. Valitse Salli manuaalinen nimikkeen uudelleenkohdistus -kentässä Kyllä.


