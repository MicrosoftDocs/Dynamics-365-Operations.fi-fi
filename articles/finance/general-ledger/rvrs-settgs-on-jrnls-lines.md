---
title: Kirjauskansioiden ja rivien asetusten palauttaminen
description: Tässä ohjeaiheessa kerrotaan, miksi kirjanpitoon syötettyä vastakirjausta ei ehkä sisällytetä kirjattuun tapahtumaan.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff8c0bda8e750e95261039b373cfb96a76034f6f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724442"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Kirjauskansioiden ja rivien asetusten palauttaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miksi kirjanpitoon syötettyä vastakirjausta ei ehkä sisällytetä kirjattuun tapahtumaan.  

## <a name="symptom"></a>Oire

Kirjanpito sisältää vastakirjauksen ja vastakirjauksen päivämäärän kirjauskansiossa. Kun kirjaat kirjauskansion, yhtäkään tositetta ei peruuteta. Miksi tapahtuu näin?

## <a name="resolution"></a>Ratkaisu

Kun kirjauskansio kirjataan, peruutusprosessi etsii vain **Vastakirjaus**- ja **Vastakirjauksen päivämäärä** -asetukset tositteen **Rivit**-osassa. Tämän menetelmän avulla kirjauskansio voi sisältää sekä peruutettaviksi merkittyjä että ei-peruutettavia tositteita.

Kirjauskansion arvoja käytetään oletusarvoina vain lisättäessä *uusia* rivejä. Kirjauskansion arvojen muuttaminen ei vaikuta aiemmin luotuihin riveihin. Tässä esimerkissä tositerivit syötettiin ensin. Kun syötät rivin tiedot ennen kirjauskansion määrittämistä peruutettavaksi, määritystä vastakirjauksena ja vastakirjauksen päivämääränä ei käytetä olemassa olevissa riveissä.

Jos olemassa olevan rivin vastakirjausta tai vastakirjauksen päivämäärää muutetaan, muutos kohdistetaan myös muihin saman tositteen riveihin. Suorituskyvyn parantamiseksi ruudukkoa ei päivitetä sen jälkeen, kun muutokset on lisätty muihin riveihin. Päivitetyt arvot tulevat näkyviin ruudukon päivittämisen jälkeen.


