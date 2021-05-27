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
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026468"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="a1b59-103">Puuttuvat kenttäasetukset, kun nimikemalliryhmät kopioidaan toiseen yritykseen</span><span class="sxs-lookup"><span data-stu-id="a1b59-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="a1b59-104">Tietopankin numero: 4612800</span><span class="sxs-lookup"><span data-stu-id="a1b59-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="a1b59-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="a1b59-105">Symptoms</span></span>

<span data-ttu-id="a1b59-106">Kun kopioit nimikemalliryhmiä toiselle yritykselle *Nimikemalliryhmän varastokäytännöt* -yksikön avulla, jotkin kenttäasetukset (esimerkiksi varastomalli ja kuvaus) puuttuvat kohdeyrityksen uudesta malliryhmästä.</span><span class="sxs-lookup"><span data-stu-id="a1b59-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1b59-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="a1b59-107">Resolution</span></span>

<span data-ttu-id="a1b59-108">Voit luoda täydellisen kopion nimikemalliryhmästä toiseen yritykseen valitsemalla myös sekä nimikemalliryhmän varastokäytännöt (`InventInventoryPolicyEntity`) että nimikemalliryhmään liittyvät kustannusvirran oletuskäytännöt (`InventCostFlowAssumptionPolicyEntity`).</span><span class="sxs-lookup"><span data-stu-id="a1b59-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
