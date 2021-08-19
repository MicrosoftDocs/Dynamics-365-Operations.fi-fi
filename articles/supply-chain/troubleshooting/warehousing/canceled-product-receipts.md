---
title: Peruutetut tuotevastaanotot eivät päivitä tapahtuman tilaksi Rekisteröity
description: Kun olet peruuttanut saapuvan kuorman tuotevastaanotot, järjestelmä päivittää varastotapahtuman tilaksi automaattisesti Vastaanotettu-tilasta Tilattu-tilaan.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731100"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Peruutetut tuotevastaanotot eivät päivitä tapahtuman tilaksi Rekisteröity

## <a name="symptoms"></a>Oireet

Kun olet suorittanut saapuvalle kuormalle **Peruuta tuotevastaanotot** -toiminnon, järjestelmä päivittää varastotapahtuman tilaksi automaattisesti *Vastaanotettu*-tilasta *Tilattu*-tilaan.

## <a name="resolution"></a>Ratkaisu

Kun lähtevien kuormien pakkausluettelot peruutetaan, varastotapahtumien tilana pysyy *Kerätty*. Kun saapuvan kuorman tuotevastaanotot peruutetaan, varastotapahtumien tilaksi ei kuitenkaan palauteta *Rekisteröity*. Kun siis saapuvan kuorman tuotevastaanotto on peruutettu, varastotyöntekijän on rekisteröitävä kuorman nimikemäärät uudelleen.

Lisätietoja on kohdassa [Saapuvan kuorman nimikemäärien rekisteröiminen](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
