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
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="6989f-103">Asiakkaan ostohyvitysten kumulointi epäonnistuu, kun nimikkeen ostohyvitysryhmiä käytetään</span><span class="sxs-lookup"><span data-stu-id="6989f-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="6989f-104">Tietopankin numero: 4611372</span><span class="sxs-lookup"><span data-stu-id="6989f-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="6989f-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="6989f-105">Symptoms</span></span>

<span data-ttu-id="6989f-106">Kun asiakkaan ostohyvityssopimuksia (*summa*-tyyppi) käytetään yhdessä nimikkeen ostohyvitysryhmien kanssa, ostohyvitykset lasketaan, mutta kumulaatio epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="6989f-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="6989f-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6989f-107">Resolution</span></span>

<span data-ttu-id="6989f-108">Järjestelmä käyttäytyy suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6989f-108">The system is behaving as designed.</span></span> <span data-ttu-id="6989f-109">Nimikeryhmät voivat ryhmitellä vain nimikkeitä, joilla on sama rajaehto.</span><span class="sxs-lookup"><span data-stu-id="6989f-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="6989f-110">Ostohyvitysehto (raja) määritetään kunkin nimikkeen summaa vasten, ei jonkin nimikeryhmän nimikkeen kumulatiivista summaa vasten.</span><span class="sxs-lookup"><span data-stu-id="6989f-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
