---
title: Varaston varausta ei voi poistaa myyntitilausrivillä
description: Jos myyntirivillä on avoimia töitä ja yrität poistaa rivin varaston varauksen, tuloksena on virhe. Vapauta varaus suorittamalla tai poistamalla työt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476237"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Varaston varausta ei voi poistaa myyntitilausrivillä

## <a name="symptoms"></a>Oireet

Jos myyntitilausrivillä on avoimia töitä ja yrität poistaa kyseisien rivin varaston varauksen, saat seuraavan virhesanoman:

> Varauksia ei voi poistaa, koska luotuna on niistä riippuvaisia töitä.

## <a name="resolution"></a>Ratkaisu

Selvitä, onko kyse avoimesta pakkausryhmän työstä ja siirrä nimike pakkausasemalta toiseen sijaintiin (kuten *lastausovelle*). Selvitä **Työn luontihistorian loki**- ja **Työn tiedot** -sivuilta, mikä fyysisesti varaa varastoa, ja vapauta varaus sitten suorittamalla tai poistamalla työ.
