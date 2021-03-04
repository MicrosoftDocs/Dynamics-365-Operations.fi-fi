---
title: Määritä konttiinpakkaus
description: Tässä aiheessa kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen Varastonhallinnassa.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f961dc379ceeeae9bbceec1baaa9b9be21316f3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427404"
---
# <a name="set-up-containerization"></a>Määritä konttiinpakkaus

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen Varastonhallinnassa. Automaattinen konttiinpakkaus luo lähetyksille kontit ja keräilytyöt kun aalto käsitellään, ja työrivit voidaan jakaa määriin, jotka sopivat kontteihin. Tämän avulla varastotyöntekijän voivat keräillä nimikkeet suoraan valittuun konttiin. Manuaaliseen pakkauskäsittelyyn verrattuna järjestelmä automatisoi tehtäviä, kuten konttien luonnin, nimikkeiden liittämisen ja konttien sulkemisen. Tässä menettelyssä käytetään esittely-yritystä USMF, ja sen suorittaa varastopäällikkö.


## <a name="set-up-a-wave-template"></a>Aaltomallin asetuksien määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Aallot > Aaltomallit**.
2. Valitse **Uusi**.
3. Syötä **Aaltomallin nimi** -kenttään arvo.
4. Kirjoita **Aaltomallin kuvaus** -kenttään arvo.
5. Syötä tai valitse arvo **Toimipaikka**-kenttään.
6. Anna tai valitse **Varasto**-kentässä arvo.
7. Laajenna **Menetelmät**-osa. **Valitut menetelmät** -ruudussa näkyvät valitun aaltomallin tyypin menetelmät. Aaltomallin on sisällettävä pakkaa konttiin -menetelmä.  
8. Kirjoita arvo **Aallon vaihekoodi** -kenttään. Kirjoita aaltovaiheen koodi lisätylle menetelmälle, joka voi olla mikä tahansa koodi. Voit lisätä menetelmän useammin kuin kerran ja määrittää sille eri aaltovaiheen koodit. Valitse tällöin **Toistettava tälle menetelmälle** **Aallon käsittelymenetelmät** -sivulla.  
9. Valitse **Tallenna**.
10. Sulje sivu.

## <a name="set-up-a-container-type"></a>Määritä konttityyppi
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Kontit > Konttityypit**. Voit määrittää haluamasi kontit **Konttityypit**-sivulla. Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja korkeuden. Tässä esimerkissä on kolmea eri kokoista laatikkoa.  
2. Valitse **Uusi**.
3. Kirjoita arvo **Kontin tyyppikoodi**-kenttään.
4. Syötä **Taarapaino**-kenttään numero.
5. Lisää **Enimmäispaino**-kenttään numero.
6. Syötä **Tilavuus**-kenttään numero.
7. Lisää **Pituus**-kenttään numero.
8. Kirjoita **Leveys**-kenttään numero.
9. Kirjoita **Korkeus**-kenttään numero.
10. Kirjoita **Kuvaus**-kenttään arvo.
11. Valitse **Tallenna**.
13. Toista vaiheet 2-11 vielä kaksi kertaa, jotta voit tehdä kolme kokonaista konttityyppiä.
14. Sulje sivu.

## <a name="set-up-a-container-group"></a>Määritä konttiryhmä
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Kontit > Konttiryhmät**.
2. Valitse toimintoruudussa **Uusi**. Voit määrittää konttityyppien loogiset ryhmät. Voit määrittää kullekin ryhmälle konttien pakkausjärjestyksen ja prosenttiosuuden, jonka perusteella kontit täytetään. Nimikkeen kokodimensiota käytetään määrittämään, onko kontissa tilaa. Järjestelmä valitsee kontin, jonka kokodimensiot ovat lähimpänä nimikettä. Jos ryhmässä on useita konttityyppejä, suosittelemme, että järjestät järjestyksen koon mukaan niin, että suurin kontti on ensimmäinen, numero 1 sarjassa, ja pienin kontti on viimeinen.    
3. Kirjoita **Konttiryhmän tunnus** -kenttään aiemmin luomasi arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Toista vaiheet 2-4 kaikille kolmelle aiemmin luomallesi konttityypille.
6. Valitse **Tallenna**.
7. Sulje sivu.

## <a name="set-up-a-container-build-template"></a>Aseta kontin muodostusmalli
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Kontit > Kontin rakennusmallit**.
2. Valitse **Uusi**. Kontin rakennusmalli perustuu suoritettavaan konttiinpakkauksen prosessiin. Kukin kontin rakennusmalli määrittää yhden konttiinpakkauksen prosessin, jota käytetään aaltomallissa. **Muokkaa kyselyä** -komennon avulla voit määrittää ehdot, jonka perusteella valittu malli käsitellään. Voit esimerkiksi haluta suorittaa konttiinpakkauksen vain tietyille asiakkaille, tuotteille tai varastoille, tai voit lisätä vastaavan kyselyalueen malliin. Kontin rakennusmalli linkitetään aaltomallin vaiheisiin **Aallon vaihekoodi** -kentän avulla. Kun aalto suoritetaan, se määrittää, mitä kontin rakennusmalleja käytetään konttiinpakkauksen aloittamiseen. Peruskyselytyyppi-kenttä määrittää pakattavat kohteet ja suodattimen perusteen. 
3. Kirjoita **Konttimallin tunnus** -kenttään arvo.
4. Anna tai valitse **Konttiryhmän tunnus** -kentässä arvo.
5. Kirjoita arvo **Aallon vaihekoodi** -kenttään.
6. Merkitse **Salli jaetut keräilyt** -valintaruutu.
7. Valitse **Tallenna**.
8. Valitse **Säilön yhdistämisrajoitukset**. Yhdistämislogiikan keskeytysten avulla voit määrittää sääntöjä pakkauksen kohdistusriveille konteissa. Jos esimerkiksi lisäät **Nimiketunnus**-kentän, kun nimikkeet on liitetty kontteihin, luodaan uusi kontti aina silloin, kun kohdataan uusi nimiketunnus. Tämä estää työntekijöitä pakkaamasta kahden eri asiakkaan kohdistusrivejä samaan konttiin.  
9. Valitse **Uusi**.
10. Valitse vaihtoehto **Taulukko**-kentässä.
11. Syötä tai valitse arvo **Kentän valinta** -kentässä.
12. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]