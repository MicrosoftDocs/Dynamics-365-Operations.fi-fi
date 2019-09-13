---
title: Huoltosopimusten laatiminen ja luominen – yleiskatsaus
description: Huoltosopimuksessa voi määrittää tavallisella huoltokäynnillä käytettävät resurssit. Voit myös määrittää, miten nämä resurssit laskutetaan asiakkaalta.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae7c3b6e1df9751d886f6eeff778e8045bd7df85
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865942"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Huoltosopimusten laatiminen ja luominen – yleiskatsaus

[!include [banner](../includes/banner.md)]

Huoltosopimuksessa voi määrittää tavallisella huoltokäynnillä käytettävät resurssit. Voit myös määrittää, miten nämä resurssit laskutetaan asiakkaalta.

Kukin huoltosopimus liitetään projektiin, jonka kautta tapahtumat kirjataan ja laskutetaan. Voit kuitenkin laskuttaa huoltotilaustapahtumia myös suoraan projektin kautta ilman, että huoltotilaus on ensin liitettävä huoltosopimukseen. Näin voidaan menetellä esimerkiksi silloin, kun huoltotilaus luodaan kertaluontoista huoltokäyntiä varten ja huoltotapahtumien nopea käsittely on tärkeämpää kuin asiakkaan yksityiskohtaisten huoltosopimustietojen ylläpito.

## <a name="service-agreement"></a>Huoltosopimus

Jokaisessa huoltosopimuksessa on määritettävä huoltosopimuksen tunnus ja ryhmä. Huoltosopimusryhmän avulla voidaan lajitella ja järjestää huoltosopimuksia.

Huoltosopimuksen otsikon asetukset koskevat kaikkia sopimusrivejä:

-  Keskeytetäänkö huoltosopimus. Jos huoltosopimus keskeytetään, et voi luoda huoltotilauksia huoltosopimuksesta.
-  Huoltosopimuksen kesto.
-  Miten huoltotilausrivit yhdistetään huoltotilauksiksi.
-  Onko huoltosopimus malli.

Huoltosopimuksen otsikossa määritetään myös huoltokohteet ja huoltotehtävät, joita voidaan käyttää huoltosopimuksessa. Se tehdään antamalla tietyt huoltotehtävät tai huoltokohteet, jotka on liitetty sopimuksen eri riveille.

Huoltosopimuksen otsikosta voidaan kopioida huoltosopimusrivejä tai huoltomallirivejä nykyiseen huoltosopimukseen.

Voit keskeyttää huoltosopimuksia ja pysäyttää yksittäisiä huoltosopimusrivejä.

Jos valitset huoltosopimuksessa **Keskeytetty**-valintaruudun, et voi

-    luoda huoltotilauksia automaattisesti tai manuaalisesti huoltosopimuksessa.

Jos valitset huoltosopimusrivillä **Pysäytetty**-valintaruudun, et voi

-    luoda huoltotilauksia automaattisesti tai manuaalisesti huoltosopimusrivillä
-    kopioida huoltosopimusriviä toiseen huoltosopimukseen tai toiselle huoltosopimusriville.


> [!NOTE]
> Jos huoltosopimus keskeytetään, kaikki siihen liittyvät rivit pysäytetään niiden yksittäisistä tiloista riippumatta.

## <a name="service-agreement-lines"></a>Huoltosopimuksen rivit

Kullakin huoltosopimusrivillä kuvataan tarkasti ehdotetun huoltotyön sisältö. Rivit sisältävät seuraavat asetukset:

-  Tapahtumatyyppi ja tapahtumatyypin kuvaus.
-  Työntekijä, joka suorittaa huoltotyön.
-  Huoltosopimuksen kohteet, jotka on huollettava.
-  Työn suoritustiheys sekä nimike-, kulu- ja maksutapahtumien kirjaustiheys.
-  Aikaikkuna, jonka sisällä huoltotilausrivit voidaan ryhmitellä huoltotilaukseksi.
-  Huoltotehtävät, joiden avulla sopimusrivien joukko ryhmitellään työtehtäviksi ja joissa on huoltoteknikoille ja asiakkaille yhteenveto suoritettavista huoltotehtävistä.
-  Pysäytetäänkö rivi. Jos rivi pysäytetään, et voi luoda huoltotilauksia kyseiselle riville.
-  Projektiasetukset, kuten luokka ja riviominaisuus.

## <a name="related-topics"></a>Liittyvät aiheet

[Huoltosopimusten luominen](create-service-agreements.md)
