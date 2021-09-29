---
title: Perintäprosessin automaation parametrien määrittäminen
description: Tässä aiheessa kuvataan automaattisen perinnän prosesseihin vaikuttavia parametreja ja annetaan ohjeita niiden määrittämisestä siten, että automaatisoitu prosessi vastaa aikomuksiasi ja odotuksiasi.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3055e10375f1b0be936e3ed0344cdf33dc7bc7e9
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487071"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Perintäprosessin automaation parametrien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan automaattisen perinnän prosesseihin vaikuttavia parametreja ja annetaan ohjeita niiden määrittämisestä siten, että automaatisoitu prosessi vastaa aikomuksiasi ja odotuksiasi. Lisätietoja perintäprosessien automatisoinnista on kohdassa [Perintäprosessin automatisointi](collections-process-automate.md).

## <a name="general"></a>Yleistä
Syötä numero kohtaan **Asiakkaiden prosentti erätyötä kohden** määrittääksesi erätöiden määrän automaatioprosessia kohden. Määritä **Kirjaa maksukehotuskirjeet automaattisesti** arvoon **Kyllä**, jotta maksukehotuskirjeen toimintotyyppi kirjaa kirjeen automaation aikana. Määritä **Luo aktiviteetteja automaatioille** arvoon **Kyllä** luodaksesi ja sulkeaksesi ei-aktiviteettia-toimintotyyppien aktiviteetit ja tarkastellaksesi kaikki asiakkaan automatisoidut vaiheet. Määritä päivien lukumäärä sille, miten kauan perintähistoriaa tallennetaan, kohtaan **Perintäprosessin automaatiohistorian säilytysaika päivinä**. Kun lasku tulee perintäprosessin viimeiseen vaiheeseen, sitä ei käytetä tulevien prosessiautomaation toimintotyyppien luomiseen, jos kohta **Jätä lasku pois viimeisen prosessivaiheen aktivoinnin jälkeen** on määritetty arvoon **Kyllä**. Seuraavaksi vanhin lasku määrittää seuraavan prosessien automaation vaiheen, jotta perintäprosessien automaatiotoimintojen jatkuminen varmistetaan. 

## <a name="payment-predictions"></a>Maksuennusteet
Versiosta 10.0.21 alkaen asiakkaan maksun ennusteet, jotka löytyvät Finance Insightsista, ennakoivat, maksetaanko lasku ajallaan, myöhässä vain paljon myöhässä. Voit määrittää nämä luokat Finance Insightsissa. Jos laskujen ennustetaan olevan myöhässä, on tärkeää, että perintäprosessi aloitetaan ennen laskun eräpäivää. Näiden ennusteiden avulla voidaan luoda perintäaktiviteetteja, kun perintäprosessien automaatioita suoritetaan. Määritä **Ota käyttöön maksuennusteet** arvoon **Kyllä**, jotta voit käyttää asiakkaan maksuennusteita perintäaktiviteettien luomiseen, perustuen laskun myöhässä maksamisen todennäköisyyteen. 

Lisätietoja asiakkaan maksuennusteista ja Finance Insightsista on kohdassa [Asiakkaan maksuennusteet](payment-insights-overview.md).

Kun asiakkaan maksuennustemalli suoritetaan, ohjelma määrittää prosenttiosuuden laskun maksamiselle ajallaan, myöhässä tai paljon myöhässä. Näitä tietoja käyttämällä voit aloittaa perintätoiminnot automaattisesti perintäprosessien automaation avulla, jos maksun odotetaan tapahtuvan myöhässä. Voit tarkastella näitä prosentteja **Maksuennusteet asiakasta kohden**- tai **Maksuennusteet tapahtumaa kohden** -sivulla kohdan **Luotonvalvonta > Perintä** alla. 

Jos asiakkaan laskun keskimääräinen maksuennuste on pienempi kuin vertailuprosentti, mitään aktiviteettia ei luoda. Jos laskun maksuennuste on suurempi tai yhtä kuin kuin vertailuprosentti, asiakasta kohden luodaan yksi aktiviteetti. Syötä kohtaan **Ennuste: Myöhässä** **Vertailuprosentti** sille, milloin perintäprosessin automaation pitäisi luoda perintäaktiviteetit. Tämä on sekä myöhäisen että erittäin myöhäisen yhteisarvo. Valitse **Liiketoiminta-asiakirjamalli** käytettäväksi luodun aktiviteetin kanssa tai luo uusi. Kentässä määritetään **Tyyppi**, **Tarkoitus** ja **Päivät, kunnes aktiviteetti suljetaan**. Syötä **Huomautukset**, jotka ovat kuvauksen oletusarvoja, kun aktiviteetti luodaan. Syötä kohtaan **Ennuste: Paljon myöhässä** **Vertailuprosentti** sille, milloin perintäprosessin automaation pitäisi luoda perintäaktiviteetit asiakkaalle, jonka ennustetaan maksavan laskun paljon myöhässä. Valitse **Liiketoiminta-asiakirjamalli** käytettäväksi luodun aktiviteetin kanssa. Kentässä määritetään **Tyyppi**, **Tarkoitus** ja **Päivät, kunnes aktiviteetti suljetaan**. Syötä **Huomautukset**, jotka ovat kuvauksen oletusarvoja, kun aktiviteetti luodaan. 

### <a name="example"></a>Esimerkki
Jos myöhäiseksi vertailuprosentiksi on määritetty 60 %. Kun asiakkaan maksuennuste suoritetaan kunkin laskun osalta, järjestelmä määrittää prosenttiosuuden laskun maksamiselle ajallaan, myöhässä tai paljon myöhässä. Jos maksuennusteen mukaan laskun maksamisen myöhästymisen todennäköisyys on 59 % tai vähemmän, automatisoitu perintäprosessi ei luo laskulle perintäaktiviteettia. Jos asiakkaan maksuennuste laskulle on suurempi tai yhtä suuri kuin 60 %, perintäaktiviteetti luodaan perintäprosessin automaation aikana. 

> [!NOTE]
> Paljon myöhässä -ennuste arvioidaan ennen myöhässä-ennustetta, koska paljon myöhässä sisältää laskut, jotka ennustetaan maksettavan myöhässä. Perintäprosessi luo vain yhden aktiviteetin, jos lasku vastaa sekä myöhässä- että paljon myöhässä -vertailukohtia. Tässä tapauksessa järjestelmä käyttää paljon myöhässä -aktiviteettia ja liiketoiminta-asiakirjaa, koska paljon myöhässä on korkeampi prioriteetti. Aiemmin luotuja toimintoja ei luoda toista kertaa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
