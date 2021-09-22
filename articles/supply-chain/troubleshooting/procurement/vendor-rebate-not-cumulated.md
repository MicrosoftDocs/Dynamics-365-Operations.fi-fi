---
title: Toimittajan ostohyvitystä ei kerry laskujen perusteella
description: Toimittajan ostohyvitystä ei kerry laskujen perusteella
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
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476271"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Toimittajan ostohyvitystä ei kerry laskujen perusteella

## <a name="symptoms"></a>Oireet

Jos kirjatuilla laskuilla on eri eräpäivät, laskut eivät näy toimittajan ostohyvityksissä, jotka on luotu niiden perusteella.

## <a name="resolution"></a>Ratkaisu

Eräpäivää ei oteta huomioon toimittajan ostohyvitystä laskettaessa. Harkitse järjestelmän mukauttamista siten, että eräpäivä ja suhde ovat ilmeisempiä todellisen toimittajan ostohyvityksen osalta.
