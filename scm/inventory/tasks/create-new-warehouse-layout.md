--- 
title: Luo uusi varastoasettelu
description: "Tässä kuvataan, miten varaston sijaintien tiedot määritetään."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 15610bc797cf7e7abdec433d0a5cead60da7a555
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-new-warehouse-layout"></a>Luo uusi varastoasettelu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä kuvataan, miten varaston sijaintien tiedot määritetään. Tämä koskee vain varastoinninhallintamoduulissa Perusvarastointi-asetuksen avulla luotuja varastoja, ei varastonhallintamoduulissa luotuja varastoja. Voit käyttää tätä menettelyä emotietojen yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-the-default-location-capacity"></a>Oletussijainnin kapasiteetin määrittäminen
1. Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.
2. Valitse Sijainnit-välilehti.
3. Syötä numero Vakioleveys-kenttään.
4. Syötä numero Vakiosyvyys-kenttään.
5. Syötä numero Vakiokorkeus-kenttään.
6. Valitse Tallenna.
7. Sulje sivu.

## <a name="define-the-location-name-format"></a>Sijainnin nimen muodon määrittäminen
1. Mene Varastonhallinta > Asetukset > Inventaarioanalyysi > Varastot.
2. Valitse Uusi.
3. Kirjoita arvo Varasto-kenttään.
4. Kirjoita arvo Nimi-kenttään.
5. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Ota käyttöön Sijainnin nimet -osan laajennus.
    * Tämän osan valinnat määrittävät sijainnin nimien oletusmuodon. Esimerkissä käytetään käytävän, hyllykön ja hyllyn numeroa.  
8. Määritä Sisällytä käytävä -vaihtoehdon arvoksi Kyllä.
9. Määritä Sisällytä hyllykkö -vaihtoehdon arvoksi Kyllä. 
10. Kirjoita hyllykön arvo Muoto-kenttään.
    * Esimerkki: -##  
11. Määritä Sisällytä hylly -vaihtoehdon arvoksi Kyllä.
12. Kirjoita hyllyn arvo Muoto-kenttään.
    * Esimerkki: -##  

## <a name="define-warehouse-locations"></a>Varaston sijaintien määrittäminen
1. Valitse toimintoruudussa Varasto.
2. Valitse ohjattu sijaintien luontitoiminto.
3. Valitse Seuraava.
4. Poista Lähtevien laiturit -vaihtoehdon valinta
5. Poista Bulkkisijainnit-vaihtoehdon valinta
6. Valitse Seuraava.
7. Valitse Seuraava.
8. Valitse Seuraava.
9. Valitse Seuraava.
10. Valitse Seuraava.
11. Valitse Seuraava.
12. Valitse Seuraava.
    * Huomaa, että tällä sivulla näkyvät fyysiset dimensiot ovat tämän menettelyn alussa määrittämäsi dimensiot.  
13. Valitse Seuraava.
14. Valitse Valmis.
15. Sulje sivu.
16. Päivitä sivu.

