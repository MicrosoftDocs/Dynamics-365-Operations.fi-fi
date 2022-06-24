---
title: Vuokrasopimuksen käyttäjäroolien liittäminen
description: Tässä artikkelissa kuvataan suojausroolit, joita käytetään resurssien vuokrauksessa. Aiheessa selitetään myös, miten käyttäjät liitetään näihin rooleihin.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38c859d64742d582d0709506d83600ea26a21147
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878128"
---
# <a name="assign-lease-user-roles"></a>Vuokrasopimuksen käyttäjäroolien liittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan suojausroolit, joita käytetään resurssien vuokrauksessa. Aiheessa selitetään myös, miten käyttäjät liitetään näihin rooleihin.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
