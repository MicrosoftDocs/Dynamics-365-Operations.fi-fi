---
title: Keskeneräiset epäsuorat kustannukset -raportti sisältää poistetut tuotantotilaukset
description: Keskeneräiset epäsuorat kustannukset -raportissa näkyvät osittain käsiteltyjen ja myöhemmin poistettujen tuotantotilausten tiedot.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026474"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Keskeneräiset epäsuorat kustannukset -raportti sisältää poistetut tuotantotilaukset

Tietopankin numero: 4612748

## <a name="symptoms"></a>Oireet

**Keskeneräiset epäsuorat kustannukset** -raportissa näkyvät osittain käsiteltyjen ja myöhemmin poistettujen tuotantotilausten tiedot.

## <a name="resolution"></a>Ratkaisu

Kun käännät tuotantotilauksen, palautat myös kaikki tuotantotilauksen tapahtumat. Kun poistat tuotantotilauksen, alareskontran taulut ja kirjanpito säilyvät kaikilla siihen liitetyillä tapahtumilla. Raportit näyttävät alareskontran taulujen tapahtumat. Tietyn tuotantotilauksen nettoarvon on oltava 0,00.
