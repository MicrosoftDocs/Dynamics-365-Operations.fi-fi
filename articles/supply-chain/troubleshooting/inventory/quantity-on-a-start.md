---
title: Aloitetun karanteenitilauksen määrää ei päivitetä, kun tilaus jaetaan
description: Kun luot karanteenitilauksen ja yrität jakaa sen, tilauksen määrää ei päivitetä jaetun jäljellä olevan määrän mukaan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026486"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="6ad30-103">Aloitetun karanteenitilauksen määrää ei päivitetä, kun tilaus jaetaan</span><span class="sxs-lookup"><span data-stu-id="6ad30-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="6ad30-104">Tietopankin numero: 4613113</span><span class="sxs-lookup"><span data-stu-id="6ad30-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="6ad30-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="6ad30-105">Symptoms</span></span>

<span data-ttu-id="6ad30-106">Kun luot karanteenitilauksen ja yrität jakaa sen, tilauksen määrää ei päivitetä jaetun jäljellä olevan määrän mukaan jaon jälkeen.</span><span class="sxs-lookup"><span data-stu-id="6ad30-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ad30-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6ad30-107">Resolution</span></span>

<span data-ttu-id="6ad30-108">Järjestelmä ei muuta karanteenitilauksen alkuperäistä määrää, jotta voit seurata karanteenitilauksen alkuperäistä määrää.</span><span class="sxs-lookup"><span data-stu-id="6ad30-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="6ad30-109">Järjestelmä seuraa kuitenkin karanteenitilauksesta jaettua määrää.</span><span class="sxs-lookup"><span data-stu-id="6ad30-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="6ad30-110">Tätä seurantaa varten se käyttää tietokantakenttää, jonka nimi on `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="6ad30-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="6ad30-111">Tämä kenttä ei kuitenkaan näy käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="6ad30-111">However, this field isn't visible in the user interface (UI).</span></span>
