---
title: Manuaalisen pakkaamisen määrittäminen (helmikuu 2016 ja toukokuu 2016)
description: Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e1e99b479752a027c60a878c57bd35d4219981
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427457"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a>Manuaalisen pakkaamisen määrittäminen (helmikuu 2016 ja toukokuu 2016)

[!include [banner](../../includes/banner.md)]

Pakkaamisprosessin avulla voit vahvistaa ja pakata tuotteita kontteihin. Tässä prosessissa varastotyöntekijät poimivat tuotteita varastopaikoista ja siirtävät ne pakkausasemalle, jossa nimikemäärät ja -tyypit tarkistetaan ja tuotteet liitetään asianmukaisiin kontteihin. Kun kontti on täysin pakattu, sen voi sulkea ja siirtää lähtevien tuotteiden laiturille – tuotteet ovat valmiina toimitettavaksi. Näissä toimintaohjeissa käytetään esittely-yritystä USMF. Tämä ohje koskee vain helmikuun 2016 ja toukokuun 2016 Dynamics 365 for Operationsin versioita.


## <a name="set-up-location-profiles"></a>Määritä sijaintiprofiilit
1. Valitse Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit.
2. Valitse Uusi.
    * Sijaintiprofiilia käytetään pakkausasemilla ja se sisältää toimipaikan tietoja ja säännöt.  
3. Kirjoita Sijainnin profiilitunnus -kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Syötä tai valitse arvo Sijainnin muoto -kenttään.
6. Anna tai valitse Sijainnin tyyppi -kentän arvo.
7. Valitse Salli yhdistetyt nimikkeet -kentässä Kyllä.
8. Valitse Salli yhdistetyt varastotilat -kentässä Kyllä.
9. Valitse Erän käsittelypäivien ohitussäännöt -kentän arvoksi Kyllä.
10. Sulje sivu.

## <a name="set-up-warehouse-management-parameters"></a>Määritä varastonhallinnan parametrit 
1. Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.
2. Napsauta Pakkaus-välilehteä.
3. Syötä tai valitse arvo Pakkauksen sijainnin profiilitunnus -kenttään.
    * Valitse sijaintiprofiili, joita haluat käyttää pakkaukseen.  
4. Sulje sivu.

## <a name="set-up-container-types"></a>Määritä konttityypit
1. Valitse Varastonhallinta > Asetukset > Kontit > Konttityypit.
2. Valitse Uusi.
    * Voit määrittää käytettävät kontit. Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja painon.  Määritteet ovat mukautettuja kenttiä, joiden avulla voit lisätä konttityyppiin ylimääräisiä dimensioita.     
3. Kirjoita arvo Konttityyppi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä Taarapaino-kenttään numero.
6. Lisää Enimmäispaino-kenttään numero.
7. Syötä Tilavuus-kenttään numero.
8. Lisää Pituus-kenttään numero.
9. Kirjoita Leveys-kenttään numero.
10. Kirjoita Korkeus-kenttään numero.
11. Valitse Tallenna.
12. Sulje sivu.

## <a name="set-up-packing-profiles"></a>Määritä pakkausprofiilit
1. Valitse Varastonhallinta > Asetukset > Pakkaus > Pakkausprofiilit.
2. Valitse Uusi.
3. Kirjoita arvo Pakkausprofiilin tunnus -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Syötä tai valitse arvo Kontin sulkemisprofiilin tunnus -kenttään.
    * Kontin sulkemisprofiilin tunnus on valinnainen ja on suljetun kontin oletusprofiili tälle pakkausprofiilille.  
6. Valitse Kontin tunnuksen tila -kentässä vaihtoehto.
    * Tämä asetus määrittää, luodaanko kontin tunnus automaattisesti kontin luomisen yhteydessä, vai luodaanko kontin tunnus manuaalisesti.  
7. Anna tai valitse arvo Konttityyppi -kentässä.
    * Kontin tyyppiä käytetään oletusarvon uutta konttia luotaessa.  
8. Merkitse Luo kontti automaattisesti kontin sulkemisessa -valintaruutu.
9. Valitse Tallenna.
10. Sulje sivu.

## <a name="set-up-container-closing-profiles"></a>Määritä kontin sulkemisprofiilit
1. Valitse Varastonhallinta > Asetukset > Kontit > Kontin sulkemisprofiilit.
    * Kontin sulkemisprofiili määrittää, mitä tapahtuu, kun kontti suljetaan. Voit määrittää useita suljetun kontin profiileja.       
2. Valitse Uusi.
3. Kirjoita arvo Kontin sulkemisprofiilin tunnus -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse vaihtoehto Luettelo kohteessa -kentässä .
    * Määritä, tapahtuuko luettelointi kontteja suljettaessa vai lähetystä vahvistettaessa. Huomaa, että luettelointi edellyttää, että Kuljetustenhallinta on käytössä. Luettelointi on toteutettava kuljetusmoottoreissa, jotta se toimii.  
6. Anna tai valitse Varasto-kentässä arvo.
7. Syötä tai valitse arvo Lopullisen lähetyksen oletussijainti -kenttään.
    * Tämä on toimipaikka, johon tuotteet siirretään konttien sulkemisen jälkeen. Toimipaikalle on määritettävä sijaintiprofiili varaston parametreissa.  
8. Syötä tai valitse arvo kentässä Painoyksikkö.
9. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]