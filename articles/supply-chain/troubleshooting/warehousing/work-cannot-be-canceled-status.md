---
title: Työtä ei voi peruuttaa sen tilan vuoksi
description: Työtä ei voi peruuttaa sen tilan vuoksi
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924252"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="6bd69-103">Työtä ei voi peruuttaa sen tilan vuoksi</span><span class="sxs-lookup"><span data-stu-id="6bd69-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="6bd69-104">Virhekoodi: WAX2190</span><span class="sxs-lookup"><span data-stu-id="6bd69-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="6bd69-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="6bd69-105">Symptoms</span></span>

<span data-ttu-id="6bd69-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="6bd69-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6bd69-107">Et voi peruuttaa työtä %1, koska sen tila on %2.</span><span class="sxs-lookup"><span data-stu-id="6bd69-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="6bd69-108">Syy</span><span class="sxs-lookup"><span data-stu-id="6bd69-108">Cause</span></span>

<span data-ttu-id="6bd69-109">Työtä ei voi peruuttaa nykyisessä tilassaan.</span><span class="sxs-lookup"><span data-stu-id="6bd69-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="6bd69-110">Työotsikolla tai työriveillä ei ole odotettua **Työn tila** -arvoa.</span><span class="sxs-lookup"><span data-stu-id="6bd69-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="6bd69-111">Työotsikon **Työn tila** -kentän arvoksi ei ole määritetty *Avoin* tai *Käsittelyssä*.</span><span class="sxs-lookup"><span data-stu-id="6bd69-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="6bd69-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6bd69-112">Resolution</span></span>

<span data-ttu-id="6bd69-113">Voit peruuttaa työn seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="6bd69-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6bd69-114">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="6bd69-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6bd69-115">Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.</span><span class="sxs-lookup"><span data-stu-id="6bd69-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6bd69-116">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6bd69-116">Select **OK**.</span></span>
1. <span data-ttu-id="6bd69-117">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6bd69-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6bd69-118">Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6bd69-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
