---
title: Keskeneräiset epäsuorat kustannukset -raportti sisältää poistetut tuotantotilaukset
description: Keskeneräiset epäsuorat kustannukset -raportissa näkyvät osittain käsiteltyjen ja myöhemmin poistettujen tuotantotilausten tiedot.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026474"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="48cdc-103">Keskeneräiset epäsuorat kustannukset -raportti sisältää poistetut tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="48cdc-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="48cdc-104">Tietopankin numero: 4612748</span><span class="sxs-lookup"><span data-stu-id="48cdc-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="48cdc-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="48cdc-105">Symptoms</span></span>

<span data-ttu-id="48cdc-106">**Keskeneräiset epäsuorat kustannukset** -raportissa näkyvät osittain käsiteltyjen ja myöhemmin poistettujen tuotantotilausten tiedot.</span><span class="sxs-lookup"><span data-stu-id="48cdc-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="48cdc-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="48cdc-107">Resolution</span></span>

<span data-ttu-id="48cdc-108">Kun käännät tuotantotilauksen, palautat myös kaikki tuotantotilauksen tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="48cdc-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="48cdc-109">Kun poistat tuotantotilauksen, alareskontran taulut ja kirjanpito säilyvät kaikilla siihen liitetyillä tapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="48cdc-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="48cdc-110">Raportit näyttävät alareskontran taulujen tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="48cdc-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="48cdc-111">Tietyn tuotantotilauksen nettoarvon on oltava 0,00.</span><span class="sxs-lookup"><span data-stu-id="48cdc-111">For the specific production order, the net value should be 0.00.</span></span>
