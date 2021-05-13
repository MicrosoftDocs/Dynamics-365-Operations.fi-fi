---
title: Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.
description: Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938462"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Et voi vahvistaa lähetystä, koska nimikkeitä ei ole kerätty.

Virhekoodi: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:

> Osaa kuormaan %1 tarvittavista nimikkeistä ei ole vielä kerätty eikä siirretty lopulliseen lähetyssijaintiin.

Et siis voi vahvistaa lähetystä kuormaa varten.

## <a name="cause"></a>Syy

Kuormitusta tai lähetystä ei voi vahvistaa nykyisessä tilassaan, koska jokin seuraavista ehdoista voi olla olemassa:

- Liittyvää työtä ei ole vielä kerätty ja siirretty lopulliseen lähetyssijaintiin.
- Kerätyn työn määrä ei vastaa kuormitusrivillä luotua työmäärää.

## <a name="resolution"></a>Ratkaisu

Tarkista kuormituksen tai lähetyksen liittyvät myyntitilaukset tai siirtotilaukset. Varmista, että kaikki liittyvä työ on tehty loppuun lopullisessa lähetyssijainnissa ja että määrät vastaavat toisiaan.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Valitse kuormitus, jolle ei voi vahvistaa lähetystä.
1. Valitse kuormarivi **Kuormarivit**-pikavälilehdessä.
1. Huomioi **Työn luontimäärä** -kentän arvo.
1. Valitse toimintoruudun **Kuormat**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Työ**.
1. Varmista, että työ on tehty valmiiksi lopullisessa lähetyssijainnissa ja että kerätyn työn määrä vastaa kuormarivin luotua työmäärää.
1. Toista nämä vaiheet kaikille kuormariveille, kun haluat varmistaa, että kaikki ehdot täyttyvät.
