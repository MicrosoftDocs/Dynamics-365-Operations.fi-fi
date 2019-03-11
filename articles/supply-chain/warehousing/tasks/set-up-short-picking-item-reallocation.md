---
title: Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten
description: Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf56a0811c4793ee2e3eaf78c8696c3c29e984c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "361219"
---
# <a name="set-up-short-picking-item-reallocation"></a>Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa. On mahdollista käyttää automaattista uudelleenkohdistusta, jossa tavarat noudetaan toisesta sijainnista, jossa ne ovat saatavilla, sijaintidirektiivien avulla. Vaihtoehtona, jos käytössä on manuaalinen uudelleenkohdistus, mobiililaitteella voidaan näyttää luettelo sijainneista, joissa tarvittu määrä on saatavilla, jolloin varastotyöntekijä voi valita käytettävän sijainnin. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


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

