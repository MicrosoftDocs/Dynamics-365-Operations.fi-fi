---
title: Uuden varastoasettelun luonti
description: Tässä artikkelissa kuvataan, kuinka voit varastosijainteihin liittyvät tiedot.
author: yufeihuang
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143648e5317e6dce1b1a76a96d6069abe5d0e351
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859311"
---
# <a name="create-a-new-warehouse-layout"></a>Uuden varastoasettelun luonti

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka voit varastosijainteihin liittyvät tiedot. Tämä koskee vain varastoinninhallintamoduulissa Perusvarastointi-asetuksen avulla luotuja varastoja, ei varastonhallintamoduulissa luotuja varastoja. Voit käyttää tätä menettelyä emotietojen yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-the-default-location-capacity"></a>Oletussijainnin kapasiteetin määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit**.
2. Valitse **Sijainnit**-välilehti.
3. Syötä numero **Vakioleveys**-kenttään.
4. Syötä numero **Vakiosyvyys**-kenttään.
5. Syötä numero **Vakiokorkeus**-kenttään.
6. Valitse **Tallenna**.
7. Sulje sivu.

## <a name="define-the-location-name-format"></a>Sijainnin nimen muodon määrittäminen
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Varastoerittely > Varastot**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Varasto**-kenttään.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Toimipaikka**-kentän valikosta haluamasi tietue.
6. Ota käyttöön **Sijainnin nimet** -osan laajennus. Tämän osan valinnat määrittävät sijainnin nimien oletusmuodon. Esimerkissä käytetään käytävän, hyllykön ja hyllyn numeroa.  
7. Määritä **Sisällytä käytävä** -vaihtoehdon arvoksi **Kyllä**.
8. Määritä **Sisällytä hyllykkö** -vaihtoehdon arvoksi **Kyllä**. 
9. Kirjoita hyllykön arvo **Muoto**-kenttään.
10. Määritä **Sisällytä hylly** -vaihtoehdon arvoksi **Kyllä**.
11. Kirjoita hyllyn arvo **Muoto**-kenttään.

## <a name="define-warehouse-locations"></a>Varaston sijaintien määrittäminen
1. Valitse toimintoruudussa **Varasto**.
2. Valitse **Ohjattu sijaintien luontitoiminto**.
3. Valitse **Seuraava**.
4. Poista **Lähtevien laiturit** -vaihtoehdon valinta
5. Poista **Bulkkisijainnit**-vaihtoehdon valinta
6. Valitse **Seuraava**, kunnes valitset **Valmis**-vaihtoehdon.
7. Sulje sivu.
8. Päivitä sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]