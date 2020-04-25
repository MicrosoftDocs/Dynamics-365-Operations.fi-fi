---
title: Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten
description: Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e860a54c2306f8140947b77cdcb538160a84e06f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216801"
---
# <a name="set-up-short-picking-item-reallocation"></a>Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa. On mahdollista käyttää automaattista uudelleenkohdistusta, jossa tavarat noudetaan toisesta sijainnista, jossa ne ovat saatavilla, sijaintidirektiivien avulla. Vaihtoehtona, jos käytössä on manuaalinen uudelleenkohdistus, mobiililaitteella voidaan näyttää luettelo sijainneista, joissa tarvittu määrä on saatavilla, jolloin varastotyöntekijä voi valita käytettävän sijainnin. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="set-up-work-exceptions"></a>Määritä työn poikkeukset
1. Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Asetukset > Työ-> Työn poikkeukset**.
2. Valitse **Uusi**. On mahdollista määrittää useita työn poikkeuksia, joilla on eri nimikkeen uudelleenkohdistuskäytännöt, joista varaston työntekijä voi valita käsittelyssä olevan lähetyksen tarpeisiin sopivan.  
3. Kirjoita **Työn poikkeuskoodi** -kenttään arvo. Anna työn poikkeukselle nimi, joka ilmaisee, mitä varten se on. Esimerkiksi, Lyhyt keräily käsin.  
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Poikkeustyyppi**-kenttään "Lyhyt keräily".
6. Valitse **Varaston oikaiseminen** -valintaruutu. Tämä vaihtoehto tarkoittaa, että varaston arvoksi asetetaan automaattisesti 0 lyhyen keräilyn sijainnissa.  
7. Syötä tai valitse arvo **Oikaisutyypin oletuskoodi** -kentässä. Esimerkiksi USMF-yrityksessä voit valita "Poista Res Adj Out".  
8. Valitse **Nimikkeen uudelleenkohdistus** -kentässä Manuaalinen. Jos valitset asetukseksi Manuaalinen tai Automaattinen ja manuaalinen, varastotyöntekijän on voitava käyttää manuaalista uudelleenkohdistusta.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Määritä manuaalinen nimikkeiden uudelleenkohdistus työntekijän käyttöön
1. Sulje sivu.
2. Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Asetukset > Työntekijä**.
3. Valitse **Muokkaa**.
4. Valitse luettelosta työntekijä 24.
5. Laajenna **Työ**-pikavälilehti.
6. Valitse **Salli manuaalinen nimikkeen uudelleenkohdistus** -kentässä Kyllä.

