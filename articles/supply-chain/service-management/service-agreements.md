---
title: Huoltosopimusten laatiminen ja luominen – yleiskatsaus
description: Huoltosopimuksessa voi määrittää tavallisella huoltokäynnillä käytettävät resurssit. Voit myös määrittää, miten nämä resurssit laskutetaan asiakkaalta.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54a3612d11976c86ec1412bb0a599c772d7edeb5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573246"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]