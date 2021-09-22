---
title: Tuotantorakenteen ja reitin numeroiden aktiivista versiota ei voi lisätä
description: Jos oletussijainti ja varasto on jo määritetty valitulle tuotteelle, sinua ei kehoteta lisäämään tuotantorakenteen ja reitin numeroiden aktiivista versiota.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476181"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Tuoterakenteen ja reitityksen lisääminen ei onnistu uutta tuotantotilausta luotaessa

## <a name="symptoms"></a>Oireet

Kun uusi tuotantotilaus luodaan, nimiketunnuksen antamisen jälkeen **Toimipaikka**- ja **Varasto**-kenttien arvoksi määritetään automaattisesti valmiin tuotteen **Tilauksen oletusasetukset** -sivulla määritetty oletustoimipaikka ja -varasto. Lisäksi aktiiviset tuotantorakenteen ja reitin numerot täytetään automaattisesti, joten et saa seuraavaa sanomaa, jossa pyydetään kyseisiä arvoja:

> Lisätäänkö tuoterakenteen ja reitin aktiivinen versio?

## <a name="resolution"></a>Ratkaisu

Tuoterakenteen ja reitin numeroa ei pyydetään antamaan, jos valitulle tuotteelle on jo määritetty toimipaikka ja varasto **Tilauksen oletusasetukset** -sivulla. Näitä arvoja kysytään vain siinä tapauksessa, että niitä ei ole määritetty valitulle tuotteelle.
