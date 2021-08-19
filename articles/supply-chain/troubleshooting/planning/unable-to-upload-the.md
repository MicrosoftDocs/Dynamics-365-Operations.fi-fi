---
title: Et voi päivittää ennustettua yksikkökustannusta, kun tuot kysyntäennustetietueita
description: Kun tuot kysyntäennustetietueita tietoyksiköiden avulla, aiemmin luotujen tietueiden kustannushintaa ei päivitetä niin, että se vastaa tuotuja tietoja.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765367"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Et voi päivittää ennustettua yksikkökustannusta, kun tuot kysyntäennustetietueita

Tietopankin numero: 4614109

## <a name="symptoms"></a>Oireet

Kun tuot kysyntäennustetietueita tietoyksiköiden avulla, aiemmin luotujen tietueiden **Ennustettu yksikkökustannus** -arvoa ei päivitetä niin, että se vastaa tuotuja tietoja.

## <a name="cause"></a>Syy

**Ennustettu yksikkökustannus** on vain luku -kenttä. Arvo perustuu tuoteyksikön kustannuksiin, eikä sitä voi määrittää suoraan tuonnin kautta.

## <a name="resolution"></a>Ratkaisu

Koska kenttä on vain luku -kenttä, sen arvoja ei voi tuoda. Arvo lasketaan aiemmin luodun liiketoimintalogiikan mukaan.
