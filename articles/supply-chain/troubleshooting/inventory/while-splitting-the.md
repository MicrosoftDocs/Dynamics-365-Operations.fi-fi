---
title: Kun todellisen painon määrä jaetaan, käytetään nimellismäärän asemesta vähimmäismäärää
description: Kun todellisen painon määrä jaetaan eriin, Keräilymäärä-kentässä käytetään nimikkeelle määritettyä vähimmäismäärää, ei nimellismäärää.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026482"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="8c142-103">Kun todellisen painon määrä jaetaan, käytetään nimellismäärän asemesta vähimmäismäärää</span><span class="sxs-lookup"><span data-stu-id="8c142-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="8c142-104">Tietopankin numero: 4612073</span><span class="sxs-lookup"><span data-stu-id="8c142-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="8c142-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="8c142-105">Symptoms</span></span>

<span data-ttu-id="8c142-106">Kun todellisen painon määrä jaetaan eriin, **Keräilymäärä**-kentässä käytetään nimikkeelle määritettyä vähimmäismäärää, ei nimellismäärää.</span><span class="sxs-lookup"><span data-stu-id="8c142-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c142-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8c142-107">Resolution</span></span>

<span data-ttu-id="8c142-108">Järjestelmä käyttäytyy suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="8c142-108">The system is behaving as designed.</span></span> <span data-ttu-id="8c142-109">Järjestelmä käyttää jokaisen nimikkeen keräilyn vähimmäismääräasetuksia.</span><span class="sxs-lookup"><span data-stu-id="8c142-109">The system uses each item's minimum quantity setup for picking.</span></span>
