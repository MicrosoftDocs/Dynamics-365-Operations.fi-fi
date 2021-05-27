---
title: Et voi päivittää ennustettua yksikkökustannusta, kun tuot kysyntäennustetietueita
description: Kun tuot kysyntäennustetietueita tietoyksiköiden avulla, aiemmin luotujen tietueiden kustannushintaa ei päivitetä niin, että se vastaa tuotuja tietoja.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026477"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="8d24d-103">Et voi päivittää ennustettua yksikkökustannusta, kun tuot kysyntäennustetietueita</span><span class="sxs-lookup"><span data-stu-id="8d24d-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="8d24d-104">Tietopankin numero: 4614109</span><span class="sxs-lookup"><span data-stu-id="8d24d-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="8d24d-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="8d24d-105">Symptoms</span></span>

<span data-ttu-id="8d24d-106">Kun tuot kysyntäennustetietueita tietoyksiköiden avulla, aiemmin luotujen tietueiden **Ennustettu yksikkökustannus** -arvoa ei päivitetä niin, että se vastaa tuotuja tietoja.</span><span class="sxs-lookup"><span data-stu-id="8d24d-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="8d24d-107">Syy</span><span class="sxs-lookup"><span data-stu-id="8d24d-107">Cause</span></span>

<span data-ttu-id="8d24d-108">**Ennustettu yksikkökustannus** on vain luku -kenttä.</span><span class="sxs-lookup"><span data-stu-id="8d24d-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="8d24d-109">Arvo perustuu tuoteyksikön kustannuksiin, eikä sitä voi määrittää suoraan tuonnin kautta.</span><span class="sxs-lookup"><span data-stu-id="8d24d-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="8d24d-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8d24d-110">Resolution</span></span>

<span data-ttu-id="8d24d-111">Koska kenttä on vain luku -kenttä, sen arvoja ei voi tuoda.</span><span class="sxs-lookup"><span data-stu-id="8d24d-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="8d24d-112">Arvo lasketaan aiemmin luodun liiketoimintalogiikan mukaan.</span><span class="sxs-lookup"><span data-stu-id="8d24d-112">The value will be calculated according to the existing business logic.</span></span>
