---
title: Huoltokohteet – yleiskatsaus
description: Huoltokohteet ovat asiakkaan käyttöomaisuuseriä ja tuotteita, joille voidaan suorittaa huoltoja.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 161d17d14af6351409e2405ae104f2b87e363ce349dd9b8e26d2c14e5fb9fa14
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770165"
---
# <a name="service-objects-overview"></a>Huoltokohteet – yleiskatsaus

[!include [banner](../includes/banner.md)]

Huoltokohteet ovat asiakkaan käyttöomaisuuseriä ja tuotteita, joille voidaan suorittaa huoltoja. Objektit voivat olla tarjoamasi huollon mukaan aineellisia tai aineettomia:

-  Aineellisia objekteja ovat kohteet, joille voidaan tehdä fyysinen huoltotehtävä. Näitä objekteja ovat mm. kone tai rakennus.

    Aineellinen huolto-objekti voi myös olla varastonimike, joka luodaan Vapautetun tuotteen tiedot -lomakkeessa. Riippuen varaston dimensioryhmästä, johon liität nimikkeen, voit luoda palveluobjektin sellaisella yksityiskohtien tasolla, joka sisältää nimikkeen sarjanumeron. Se on hyödyllistä silloin, kun sinun on jäljitettävä huolto-objektin edustama tarkka nimike.

    Aineellinen huolto-objekti voi kuitenkin olla myös nimike, joka ei suoraan liity yrityksen suoraan tuotanto- tai toimitusketjuun. Esimerkiksi huoltotilauksen korjauksissa käytettävä työkalusarja voi olla huoltokohde, jota ei sisällytetä varastoon. Tässä tapauksessa et rekisteröi sitä varastonimikkeenä.

-  Aineettomia objekteja ovat ei-fyysiset asiat, kuten tilijoukko tai lakisääteinen tosite, jolle palvelutehtäviä suoritetaan.

## <a name="example-of-an-intangible-service-object"></a>Esimerkki aineettomasta huolto-objektista

Yritys A ylläpitää useiden pienten yritysten kirjanpitotietueita. Yksi yritys A:n asiakkaista on paikallinen jalkapalloseura, jonka viikoittaista kirjanpitoa ja vuosittaista tarkistusta yritys A hoitaa. Klubin tilit määritetään Huoltokohteet-lomakkeella ja määritetään kohteiksi huoltosopimuksessa. Objektille on kaksi palvelusopimusriviä. Rivi 1 on viikoittainen kirjanpito, joka sisältää riviin määritetyn viikoittaisen aikavälin, ja rivi 2 on vuosittainen tarkistus, johon on määritetty vuosittainen aikaväli.

## <a name="related-topics"></a>Liittyvät aiheet

[Huoltokohteiden luominen](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]