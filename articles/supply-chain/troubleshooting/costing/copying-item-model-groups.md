---
title: Puuttuvat kenttäasetukset, kun nimikemalliryhmät kopioidaan toiseen yritykseen
description: Kenttäasetukset puuttuvat, kun nimikemalliryhmät kopioidaan toiseen yritykseen.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738840"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Puuttuvat kenttäasetukset, kun nimikemalliryhmät kopioidaan toiseen yritykseen

Tietopankin numero: 4612800

## <a name="symptoms"></a>Oireet

Kun kopioit nimikemalliryhmiä toiselle yritykselle *Nimikemalliryhmän varastokäytännöt* -yksikön avulla, jotkin kenttäasetukset (esimerkiksi varastomalli ja kuvaus) puuttuvat kohdeyrityksen uudesta malliryhmästä.

## <a name="resolution"></a>Ratkaisu

Voit luoda täydellisen kopion nimikemalliryhmästä toiseen yritykseen valitsemalla myös sekä nimikemalliryhmän varastokäytännöt (`InventInventoryPolicyEntity`) että nimikemalliryhmään liittyvät kustannusvirran oletuskäytännöt (`InventCostFlowAssumptionPolicyEntity`).
