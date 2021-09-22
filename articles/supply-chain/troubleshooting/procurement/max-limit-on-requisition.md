---
title: Ostosopimuksen yläraja ei päde ostoehdotukseen
description: Ostosopimuksen yläraja ei päde ostoehdotukseen
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476206"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Ostosopimuksen yläraja ei päde ostoehdotukseen

## <a name="symptoms"></a>Oireet

Kun ostoehdotus linkitetään ostosopimukseen, ostosopimuksen yläraja ei päde ostoehdotukseen. Oletushintatiedot on syötetty oikein, mutta ostoehdotuksella voit tilata ostosopimuksen ylärajan ylittävän määrän.

## <a name="resolution"></a>Ratkaisu

Tämä toiminta on tarkoituksellista. Koska ehdotuksia ei aina hyväksytä, määrää tai summaa ei pitäisi varata ostosopimuksessa. Siksi ostosopimuksen ylärajaa ei saavuteta.
