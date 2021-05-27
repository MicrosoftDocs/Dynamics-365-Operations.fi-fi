---
title: Asiakkaan ostohyvitysten kumulointi epäonnistuu, kun nimikkeen ostohyvitysryhmiä käytetään
description: Kun asiakkaan ostohyvityssopimuksia käytetään yhdessä nimikkeen ostohyvitysryhmien kanssa, ostohyvitykset lasketaan, mutta kumulaatio epäonnistuu.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026463"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Asiakkaan ostohyvitysten kumulointi epäonnistuu, kun nimikkeen ostohyvitysryhmiä käytetään

Tietopankin numero: 4611372

## <a name="symptoms"></a>Oireet

Kun asiakkaan ostohyvityssopimuksia (*summa*-tyyppi) käytetään yhdessä nimikkeen ostohyvitysryhmien kanssa, ostohyvitykset lasketaan, mutta kumulaatio epäonnistuu.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Nimikeryhmät voivat ryhmitellä vain nimikkeitä, joilla on sama rajaehto. Ostohyvitysehto (raja) määritetään kunkin nimikkeen summaa vasten, ei jonkin nimikeryhmän nimikkeen kumulatiivista summaa vasten.
