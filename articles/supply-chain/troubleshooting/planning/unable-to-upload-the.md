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
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026477"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Et voi päivittää ennustettua yksikkökustannusta, kun tuot kysyntäennustetietueita

Tietopankin numero: 4614109

## <a name="symptoms"></a>Oireet

Kun tuot kysyntäennustetietueita tietoyksiköiden avulla, aiemmin luotujen tietueiden **Ennustettu yksikkökustannus** -arvoa ei päivitetä niin, että se vastaa tuotuja tietoja.

## <a name="cause"></a>Syy

**Ennustettu yksikkökustannus** on vain luku -kenttä. Arvo perustuu tuoteyksikön kustannuksiin, eikä sitä voi määrittää suoraan tuonnin kautta.

## <a name="resolution"></a>Ratkaisu

Koska kenttä on vain luku -kenttä, sen arvoja ei voi tuoda. Arvo lasketaan aiemmin luodun liiketoimintalogiikan mukaan.
