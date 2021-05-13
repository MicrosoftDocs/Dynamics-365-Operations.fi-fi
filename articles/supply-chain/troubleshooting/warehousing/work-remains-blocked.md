---
title: Työ on edelleen estetty
description: Työ on edelleen estetty
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924127"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="ae4e0-103">Työ on edelleen estetty</span><span class="sxs-lookup"><span data-stu-id="ae4e0-103">Work remains blocked</span></span>

<span data-ttu-id="ae4e0-104">Virhekoodi: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ae4e0-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="ae4e0-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="ae4e0-105">Symptoms</span></span>

<span data-ttu-id="ae4e0-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="ae4e0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ae4e0-107">Työ %1 on edelleen estetty, koska liittyvän aallon %2 tila on %3.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="ae4e0-108">Syy</span><span class="sxs-lookup"><span data-stu-id="ae4e0-108">Cause</span></span>

<span data-ttu-id="ae4e0-109">Työtä käsitellään parhaillaan aallossa eikä sen estoa voi poistaa, kuten jokin seuraavista ehdoista on osoittanut:</span><span class="sxs-lookup"><span data-stu-id="ae4e0-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="ae4e0-110">**Eston syyt** -välilehdessä **Työn eston syy** -kentässä yhen tai usean rivin arvona on *Aallon käsittely*.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="ae4e0-111">Kun valitset **Aalto** **Aiheeseen liittyviä tietoja** -ryhmässä toimintoruudun **Aiheeseen liittyviä tietoja** -välilehdessä, **Aallon tila** -kentän arvoksi tulee *Käsitellään*.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ae4e0-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ae4e0-112">Resolution</span></span>

<span data-ttu-id="ae4e0-113">Valitse toimintoruudun **Aiheeseen liittyviä tietoja**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Aalto**.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="ae4e0-114">Sitten **Aallot**-sivulla toimintoruudussa **Aalto**-välilehdessä **Aalto**-ryhmässä valitse **Tyhjennä aallon tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="ae4e0-115">Ongelman kiertäminen</span><span class="sxs-lookup"><span data-stu-id="ae4e0-115">Workaround</span></span>

<span data-ttu-id="ae4e0-116">Jos edelliset vaiheet eivät korjaa ongelmaa, voit peruuttaa työn noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="ae4e0-117">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ae4e0-118">Määritä **Työtunnus**-kentässä peruutettavan työn tunnus ja jonka **Työn tila** -arvona on *Avoinna*, *Käsittelyssä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ae4e0-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-119">Select **OK**.</span></span>
1. <span data-ttu-id="ae4e0-120">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="ae4e0-121">Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ae4e0-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
