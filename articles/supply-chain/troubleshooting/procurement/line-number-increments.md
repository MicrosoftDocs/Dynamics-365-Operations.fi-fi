---
title: Tuoduissa ostotilauksissa näkyy virheellisiä rivinumeroita
description: Kun ostotilaukset tuodaan tiedonhallinnan kautta, ostotilausten rivi numerot eivät noudata järjestelmän parametreissa määritettyä korotusta.
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
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476183"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Tuoduissa ostotilauksissa näkyy virheellisiä rivinumeroita

## <a name="symptoms"></a>Oireet

Oletusarvoisesti automaattisesti luodut *Ostotilausrivit V2* -tietoyksikön kautta tuotujen tilausrivien rivinumerot eivät käytä järjestelmän parametreissa määritettyä rivinumeron korotusta. Jos luot ostotilauksen manuaalisesti ja lisäät rivejä käyttöliittymän kautta, rivinumerot kasvavat oikein. Jos kuitenkin käytät tiedonhallinnan kehystä (DMF), niitä ei koroteta oikein.

Tämä ongelma ilmenee, koska tuotaessa rivejä DMF-kehyksen kautta järjestelmä käyttää DMF:n menetelmää niiden määrittämiseen, jos tuodussa yksikössä ei ole määritetty rivinumeroita valmiiksi. Tässä menetelmässä rivinumeroita kasvatetaan aina yhdellä.

## <a name="workaround"></a>Ongelman kiertäminen

Varmista, että halutut rivinumerot on jo määritetty tietoyksikön numerokentissä, kun tuot ostotilauksen rivit. Tällöin DMF ei korvaa rivinumeroita.
