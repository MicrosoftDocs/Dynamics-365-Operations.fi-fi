---
title: Tapahtumat voidaan kirjata keskeytetylle kirjanpitotilille
description: Jos tuotteen vastaanotto peruutetaan, järjestelmä sallii tapahtumien kirjaamisen keskeytetyille kirjanpitotileille, vaikka päätilit olisivat keskeytettynä
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476276"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Tapahtumat voidaan kirjata keskeytetylle kirjanpitotilille

## <a name="symptoms"></a>Oireet

Jos tuotteen vastaanotto peruutetaan, järjestelmä sallii tapahtumien kirjaamisen keskeytetyille kirjanpitotileille, vaikka päätilit olisivat keskeytettynä.

## <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Varmista **Ostoreskontran parametrit** -sivun **Yleiset**-välilehdessä, että **Kirjaa vastaanotto kirjanpitoon** -asetuksen arvona on *Kyllä*.
1. Luo ostotilaus ja lisää tilausrivi, jossa tietyn tuotteen määrä on *1 000*.
1. Vahvista ostotilaus.
1. Kirjaa tuotteen vastaanotto ja tarkista tositteet.
1. Keskeytä tarvittavat päätilit eli *200140* ja *140200*.
1. Peruuta kirjattu tuotteen vastaanotto.
1. Huomaa, että tapahtumat voidaan kirjata keskeytetyille kirjanpitotileille.

## <a name="resolution"></a>Ratkaisu

Tapahtumat voidaan kirjata keskeytetyille kirjanpitotileille, kun tuotteiden vastaanotot peruutetaan, koska tämä toimintatapa mahdollistaa oikeelliset kirjaukset.
