---
title: Kauppasopimuksen ehtoja ei sovelleta tuotuihin tilausriveihin
description: Kauppasopimuksen hintoja ja alennuksia ei käytetä myynti- tai ostotilausriveillä, jotka tuodaan tiedonhallinnan kautta
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476256"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Kauppasopimuksen ehtoja ei sovelleta tuotuihin tilausriveihin

## <a name="symptoms"></a>Oireet

Myynti- tai ostotilausriveissä käytettäviä kauppasopimuksia ei käytetä riveillä, jotka tuodaan tiedonhallinnan kautta. Samoja kauppasopimuksia käytetään kuitenkin manuaalisesti luoduissa myynti- tai ostotilausriveissä.

## <a name="cause"></a>Syy

Jos tiedonhallinnan kautta tuotavat ostotilausrivit sisältävät jo hintatietoja, kauppasopimusta ei arvioida uudelleen kyseisten rivien osalta. Jos riville on määritetty **Rivialennusprosentti** tai jokin hinnan ja alennuksen arvoista, kauppasopimuksia ei etsitä kyseiselle riville.

## <a name="workaround"></a>Ongelman kiertäminen

Tämä toiminta on odotettavissa, ja se on samanlainen sekä myynti- että ostotilauksissa.

Kiertotapana voit tuoda ostotilausrivit määrittämättä hintatietoja. Tällöin sovelletaan kauppasopimuksia ja ostotilausrivit päivitetään määritettyjen kauppasopimusten perusteella.
