---
title: Nimikkeellä ei voi olla tuoterakennetta tai kaavaa
description: Kun yrität vahvistaa tilauksen, näyttöön tulee virhesanoma nimikkeen oikeellisuustarkistuksen aikana. Se määrittää, että nimikkeellä ei voi olla tuoterakennetta tai kaavaa.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730103"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Nimikkeellä ei voi olla tuoterakennetta tai kaavaa

Virhekoodi: PRO2614

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa tilauksen, näyttöön tulee seuraava virhesanoma nimikkeen oikeellisuustarkistuksen aikana:

> Nimikkeellä ei voi olla tuoterakennetta tai kaavaa

## <a name="resolution"></a>Ratkaisu

Nimikkeiden, joissa on tuoterakenne tai kaava, on oltava *suunnittelunimike*-, *tuoterakenne*- tai *kaava* -tyyppi. Voit muuttaa nimiketyypin seuraavasti.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa asiaankuuluva tuote.
1. Nimike on määritettävä *Suunnittelunimikkeeksi*, *Tuoterakenteeksi* tai *Kaavaksi* **Tuotantotyyppi**-kentän **Kehittäjä**-pikavälilehdessä.
