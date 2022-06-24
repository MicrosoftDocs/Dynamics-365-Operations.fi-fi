---
title: Kirjanpidon oletuskuvaukset
description: Oletuskuvauksia voidaan käyttää tositteiden kirjausten Kuvaus-kentän päivittämiseksi kirjanpitoon.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7020c39dd599be047e07caa391d6d4c69c426328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889545"
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
