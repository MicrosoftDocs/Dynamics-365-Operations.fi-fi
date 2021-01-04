---
title: Vuokrasopimuksen käyttäjäroolien liittäminen
description: Tässä ohjeaiheessa kuvataan suojausroolit, joita käytetään resurssien vuokrauksessa. Aiheessa selitetään myös, miten käyttäjät liitetään näihin rooleihin.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442977"
---
# <a name="assign-lease-user-roles"></a>Vuokrasopimuksen käyttäjäroolien liittäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan suojausroolit, joita käytetään resurssien vuokrauksessa. Aiheessa selitetään myös, miten käyttäjät liitetään näihin rooleihin.

Resurssin vuokrauksessa on kolme erilaista käyttäjäroolia. Yksi rooli sopii vuokrasopimusten ylläpitämiseen, toinen vuokrasopimusten tarkasteluun ja kolmas vuokrasopimuksen tehtäviä suorittavalle vuokravirkailijalle. Kullakin roolilla on tietyt käyttöoikeudet kaikilla vuokrauksen sivuilla, ja kukin käyttäjä voi tarkastella, luoda, muokata tai poistaa vuokrasopimuksia työtehtäviensä mukaisesti.

| Rooli           | kuvaus |
|----------------|-------------|
| Vuokrasopimuksen ylläpitäminen | Tämän roolin käyttäjät voivat lisätä, muokata, poistaa ja tarkastella vuokrasopimuksia. Tämä rooli on suunniteltu päivittäiselle käyttäjälle, jonka tehtäviin kuuluu kuukausittaisten kirjauskansiovientien luominen ja kirjaaminen sekä uusien vuokrasopimusten lisääminen. Tämä rooli mahdollistaa kaikkien resurssin vuokrauksen toimintojen käyttämisen. |
| Vuokrasopimuksen tarkasteleminen     | Tämän roolin käyttäjät voivat tarkastella vain vuokrasopimuksen tietueita ja aikatauluja sekä suorittaa raportteja. He eivät voi luoda uusia vuokrasopimuksia, muokata olemassa olevia vuokrasopimuksia tai luoda kirjauskansiovientejä vuokrasopimuksille. Rooli on tarkoitettu käyttäjille, joiden on vain tarkasteltava vuokrasopimuksia, vuokrasopimusten aikatauluja ja tapahtumia, joita vuokrasopimuksille tehdään. |
| Vuokravirkailija    | Tämän roolin käyttäjät voivat vain luoda uusia vuokrasopimuksia. He eivät voi muokata tai poistaa olemassa olevia vuokrasopimuksia, tarkastella vuokrausaikatauluja tai kirjata leasingvuokrauskansiovientejä. Tämä rooli on suunniteltu käyttäjille, jotka syöttävät tietoja. |

Noudattamalla näitä ohjeita voit määrittää käyttäjät resurssin vuokrauksessa.

1. Siirry kohtaan **Järjestelmänhallinta \> Suojaus \> Liitä käyttäjät rooleihin**.
2. Valitse **Vuokrasopimuksen ylläpitäminen**-, **Vuokravirkailija**- tai **Vuokrasopimuksen tarkasteleminen** -rooli ja valitse sitten **Manualainen liittäminen / sulje pois käyttäjiä**.
3. Valitse rooliin liitettävä käyttäjä ja valitse sitten **Liitä rooliin**.
