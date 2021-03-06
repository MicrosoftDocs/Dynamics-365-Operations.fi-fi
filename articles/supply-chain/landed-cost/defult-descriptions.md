---
title: Kirjanpidon oletuskuvaukset
description: Oletuskuvauksia voidaan käyttää tositteiden kirjausten Kuvaus-kentän päivittämiseksi kirjanpitoon.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021609"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Kirjanpidon oletuskuvaukset

[!include [banner](../../includes/banner.md)]

Oletuskuvauksia voidaan käyttää tositteiden kirjausten **Kuvaus**-kentän päivittämiseksi kirjanpitoon. Tätä ominaisuutta on parannettu toimimaan aiheutuneen kustannuksen kanssa.

Voit määrittää oletuskuvauksia kirjanpidon kirjauksille valitsemalla **Organisaation hallinta \> Asetukset \> Oletuskuvaukset**.

Seuraavassa taulukossa luetellaan uudet arvot, jotka on lisätty **Oletuskuvaukset**-sivun **Kuvaus**-kentälle aiheutuneen kustannuksen tukemiseksi.

| Kuvauksen tyyppi | Muistiinpanot |
|---|---|
| Tuonnin kustannuslaskenta – Kustannusten jaksotus | Kun ostotilauslasku kirjataan, merikuljetuksen arvioiduille kustannuksille suoritetaan kustannusten jaksotus. Voit määrittää oletuskuvauksia lisätäksesi merikuljetuksen numeron kuvaukseen. Käytä lähetyksen numerona *%4*. |
| Tuonnin kustannuslaskenta – Matkalla olevien tavaroiden tilaus | Jos käytät kuljetettavien tuotteiden käsittelyä, ostotilauslasku kirjataan ja tavarat kirjataan kuljetustilin tavaroihin. Voit määrittää oletuskuvauksia lisätäksesi kuljetettavien tuotteiden numeron kuvaukseen. Käytä kuljetettavien tuotteiden tilausten numerona *%4*. |
| Varasto – Sulje – Oikaisu | Kun ostoreskontran lasku käsitellään merikuljetuksen kustannusta varten, merikuljetuksen kustannusten arvioimiseksi käsitellään varaston oikaisu. Voit määrittää oletuskuvauksia lisätäksesi merikuljetuksen numeron kuvaukseen. Käytä lähetyksen numerona *%4*. |

Lisätietoja **Oletuskuvaukset**-sivun käytöstä on kohdassa [Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
