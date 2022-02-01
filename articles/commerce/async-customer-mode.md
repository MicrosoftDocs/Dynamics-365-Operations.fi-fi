---
title: Asynkroninen asiakkaan luontitila
description: Tässä aiheessa kuvataan asynkronista asiakkaan luontitilaa Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 43418b61778d187364d4d52a05178078a37623eb
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984267"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynkroninen asiakkaan luontitila

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan asynkronista asiakkaan luontitilaa Microsoft Dynamics 365 Commercessa.

Commercessa asiakkaan luomisessa on kaksi eri tilaa: Synkroninen ja Asynkroninen. Oletusarvon mukaan asiakkaat luodaan synkronisesti. Toisin sanoen ne luodaan Commerce headquarters -sovelluksessa reaaliaikaisesti. Synkroninen asiakkaan luontitila on hyödyllinen, koska uusia asiakkaita voidaan hakea välittömästi eri kanavien kautta. Sillä on kuitenkin myös haittapuolensa. Koska se luo [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) -kutsuja Commerce headquarters -sovelluksessa, suorituskykyyn voi vaikuttaa, jos tehdään samanaikaisia asiakkaan luontikutsuja.

Jos **Luo asiakas asynkronisessa tilassa** -asetus on **Kyllä** myymälän toimintoprofiilissa (**Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan määritys \> Toimintoprofiilit**), Real-time Service -kutsuja ei käytetä asiakastietueiden luomiseen kanavatietokannassa. Asynroninen asiakkaan luontitila ei vaikuta Commerce headquarters -ohjelman suorituskykyyn. Jokaiselle uudelle asynkroniselle asiakastietueelle liitetään väliaikainen, yleinen yksilöivä tunnus (GUID), jota käytetään asiakastilin tunnuksena. GUID ei näy myyntipisteen (POS) käyttäjille. Sen sijaan käyttäjät näkevät **Odottaa synkronointia** asiakastilin tunnuksena.

> [!IMPORTANT]
> Kun myyntipiste siirtyy offline-tilaan, järjestelmä luo asiakkaat automaattisesti asynkronisesti, vaikka asynkronisen asiakasluonnin tila olisi pois käytöstä. Siksi Commerce-pääkonttorin järjestelmänvalvojien on riippumatta siitä, oletko valinnut synkronisen vai asynkronisen asiakasluonnin, luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle (ennen "**Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ") ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce-pääkonttorissa synkronoiduiksi asiakkaiksi.

## <a name="async-customer-limitations"></a>Asynkronisen asiakkaan rajoitukset

Asynkronisen asiakkaan toiminnallisuuteen liittyy tällä hetkellä seuraavat rajoitukset:

- Asynkronisen asiakkaan tietueita ei voi muokata, ellei asiakasta ole luotu Commerce headquarters -sovelluksessa ja uutta asiakastilin tunnusta ole synkronoitu takaisin kanavaan.
- Kanta-asiakaskortteja ei voi myöntää asynkronisille asiakkaille, ellei uutta asiakastilitunnusta ole synkronoitu takaisin kanavaan.

## <a name="async-customer-enhancements"></a>Asynkronisen asiakkaan parannukset

Commerce 10.0.24 -versiosta alkaen voit ottaa käyttöön **Ota käyttöön laajennetun asiakkaan luonti** -ominaisuuden **Ominaisuuksien hallinta** -työtilassa. Tämä ominaisuus katkaisee kuilun asynkronisten ja synkronoitujen asiakkaiden luontitilojen välillä myyntipisteissä ja verkkokaupassa seuraavilla tavoilla:

- Liitoksia ei voi liittää asynkronisiin asiakkaisiin.
- Asynkronisiin asiakkaisiin voi lisätä otsikoita.
- Toissijaisia sähköpostiosoitteita ja puhelinnumeroita ei voi siepata asynkronisille asiakkaille.

Commerce 10.0.22 -versiosta alkaen voit ottaa käyttöön **Ota käyttöön asynkronoitu asiakkaan osoitteen luonti** -ominaisuuden **Ominaisuuksien hallinta** -työtilassa. Tämän ominaisuuden avulla uudet asiakkaan osoitteet voidaan tallentaa asynkronisesti sekä synkronoiduille että asynkronoiduille asiakkaille.

Kun olet ottanut aiemmin mainitut ominaisuudet käyttöön, sinun on ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja liikekumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan synkronointiasiakkaiksi Commerce headquartersissa.

### <a name="customer-creation-in-pos-offline-mode"></a>Asiakkaan luonti myyntipisteen offline-tilassa

Kuten aiemmin mainittiin, kun myyntipiste siirtyy offline-tilaan, järjestelmä luo asiakkaat automaattisesti asynkronisesti, vaikka asynkronisen asiakasluonnin tila olisi pois käytöstä. Siksi Commerce headquartersin järjestelmänvalvojien on luotava ja ajoitettava toistuva erätyö **P-työlle**, **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työlle ja **1010**-työlle, jotta kaikki asynkroniset asiakkaat muunnetaan Commerce headquartersissa synkronoiduiksi asiakkaiksi.

> [!NOTE]
> Jos **Suodata jaetut asiakastietotalut** -asetus on **Kyllä** **Commerce-kanavan rakenne** -sivulla (**Retail ja Commerce \> Headquartersin asetuukset \> Commerce-ajastus \> Kanavan tietokantaryhmä**), asiakastietueita ei luoda myyntipisteen offline-tilassa. Lisätietoja on kohdassa [Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Lisäresurssit

[Myymälöiden asiakashallinta](customer-mgmt-stores.md)

[Asynkronisten asiakkaiden muuntaminen synkronisiksi asiakkaiksi](convert-async-to-sync.md)

[Asiakkaan määritteet](dev-itpro/customer-attributes.md)

[Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
