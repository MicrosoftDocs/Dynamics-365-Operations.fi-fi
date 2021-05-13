---
title: Viimeisen suljetun työrivin on oltava määritys
description: Viimeisen suljetun työrivin on oltava määritys
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924372"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="5af09-103">Viimeisen suljetun työrivin on oltava määritys</span><span class="sxs-lookup"><span data-stu-id="5af09-103">The last closed work line must be a put</span></span>

<span data-ttu-id="5af09-104">Virhekoodi: WAX1285</span><span class="sxs-lookup"><span data-stu-id="5af09-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="5af09-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="5af09-105">Symptoms</span></span>

<span data-ttu-id="5af09-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="5af09-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5af09-107">Viimeisen suljetun työrivin on oltava määritys.</span><span class="sxs-lookup"><span data-stu-id="5af09-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="5af09-108">Syy</span><span class="sxs-lookup"><span data-stu-id="5af09-108">Cause</span></span>

<span data-ttu-id="5af09-109">Työtä ei voi peruuttaa nykyisessä tilassaan.</span><span class="sxs-lookup"><span data-stu-id="5af09-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="5af09-110">Viimeisellä työrivillä **Työn tila** -kentän arvona on *Suljettu*, mutta **Työtyypi**-kentän arvona ei ole *Määritys*.</span><span class="sxs-lookup"><span data-stu-id="5af09-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="5af09-111">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5af09-111">Resolution</span></span>

<span data-ttu-id="5af09-112">Voit peruuttaa työn seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5af09-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="5af09-113">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="5af09-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="5af09-114">Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.</span><span class="sxs-lookup"><span data-stu-id="5af09-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="5af09-115">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5af09-115">Select **OK**.</span></span>
1. <span data-ttu-id="5af09-116">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5af09-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="5af09-117">Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="5af09-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
