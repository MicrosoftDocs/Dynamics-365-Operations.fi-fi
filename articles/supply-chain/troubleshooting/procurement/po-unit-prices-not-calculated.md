---
title: Ostotilausten yksikköhintoja ei lasketa yksikkömuunnoksen perusteella
description: Ostotilausten yksikköhintoja ei lasketa yksikkömuunnoksen perusteella
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
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476223"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Ostotilausten yksikköhintoja ei lasketa yksikkömuunnoksen perusteella

## <a name="symptoms"></a>Oireet

Kun yksikköä muutetaan ostotilauksessa, kauppasopimuksen hintoja ei lasketa uudelleen yksikkömuunnoksen määritysten mukaisesti.

## <a name="cause"></a>Syy

Hinnat perustuvat aina kauppasopimuksiin (tai muihin järjestelmän hinta-asetuksiin, kuten myyntisopimuksiin tai nimikkeiden hintoihin), ja ne on määritetään yksikkökohtaisesti.

Jos yksikköä muutetaan tilausrivillä, järjestelmä hakee hinnan uudelle nimikkeelle ja soveltaa sitä. Jos yksikölle ei löydy hintaa, järjestelmä ei käytä hintaa. Yksikkömuunnosta ei voi käyttää hinnan uudelleenlaskemiseen toiseen yksikköön. Teoriassa yhden laatikon hinta ei ehkä vastaa kymmentä kertaa yhden laatikon hintaa.

## <a name="workaround"></a>Ongelman kiertäminen

Yksi tapa kiertää tämä ongelma on varmistaa, että nimikkeen tilausriveillä käytetään odottamiasi yksiköitä koskevia kauppasopimuksia.
