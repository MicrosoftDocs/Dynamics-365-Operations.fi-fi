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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760367"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Asiakkaan ostohyvitysten kumulointi epäonnistuu, kun nimikkeen ostohyvitysryhmiä käytetään

Tietopankin numero: 4611372

## <a name="symptoms"></a>Oireet

Kun asiakkaan ostohyvityssopimuksia (*summa*-tyyppi) käytetään yhdessä nimikkeen ostohyvitysryhmien kanssa, ostohyvitykset lasketaan, mutta kumulaatio epäonnistuu.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla. Nimikeryhmät voivat ryhmitellä vain nimikkeitä, joilla on sama rajaehto. Ostohyvitysehto (raja) määritetään kunkin nimikkeen summaa vasten, ei jonkin nimikeryhmän nimikkeen kumulatiivista summaa vasten.
