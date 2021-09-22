---
title: Tuoterakenteen hajotus toimii eri tavoin vahvistettujen ja arvioitujen tuotantotilausten osalta
description: Tuoterakenteen hajotus toimii eri tavalla vahvistetuissa tuotantotilauksissa ja manuaalisesti luodun työn ennakkolasketuissa tuotantotilauksissa
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476225"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Tuoterakenteen hajotus toimii eri tavoin vahvistettujen ja arvioitujen tuotantotilausten osalta

## <a name="symptoms"></a>Oireet

Kun tuotantotilaus vahvistetaan, nimikkeitä ei hajoteta, kun tuoterakenne hajotetaan. Kun työtilaus kuitenkin luodaan manuaalisesti ja tuotantotilaukselle tehdään ennakkolaskenta, nimikkeet hajotetaan.

### <a name="resolution"></a>Ratkaisu

Tuotantotilausta vahvistettaessa tapahtuva hajotus osoittaa suunniteltuun tilaukseen, mutta ei vaikuta siltä, että suunniteltu tilaus on tällä hetkellä vahvistettu tässä tapauksessa. Jos tuotantotilaus on kuitenkin ennakkolaskettu, hajotus käynnistetään vapautetusta tuotantotilauksesta, kun suunniteltua tilausta ei ole.
