---
title: Työtä ei voi peruuttaa, koska se on estetty.
description: Työtä ei voi peruuttaa, koska se on estetty.
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924276"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="e9e4f-103">Työtä ei voi peruuttaa, koska se on estetty.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="e9e4f-104">Virhekoodi: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="e9e4f-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="e9e4f-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="e9e4f-105">Symptoms</span></span>

<span data-ttu-id="e9e4f-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="e9e4f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="e9e4f-107">Työtä %1 ei voi peruuttaa, koska se on syytyyppi %2 on estänyt sen.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="e9e4f-108">Työ on peruutettava, ennen kuin se voidaan peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="e9e4f-109">Syy</span><span class="sxs-lookup"><span data-stu-id="e9e4f-109">Cause</span></span>

<span data-ttu-id="e9e4f-110">Työ on estetty eikä sitä voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="e9e4f-111">**Työ**-sivun **Yleiset**-välilehdessä **Estetty**-kohdan asetuksena on *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="e9e4f-112">Tämä asetus ilmaisee, että työ on estetty.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="e9e4f-113">**Eston syyt** -välilehdessä näkyy, miksi työ on estetty.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="e9e4f-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e9e4f-114">Resolution</span></span>

<span data-ttu-id="e9e4f-115">Voit poistaa työn eston valitsemalla **Eston syyt** -välilehden ja noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="e9e4f-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="e9e4f-116">Jos **Työn esto syy** -kentän arvoksi on määritetty *Määrittämätön syy*: Valitse toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Poista työn esto**.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="e9e4f-117">Jos **Työn esto syy** -kentän arvona on *Aallon käsittely*: Toimintoruudun **Aiheeseen liittyviä tietoja** -välilehden **Aiheeseen liittyviä tietoja** -ryhmässä valitse **Aalto**.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="e9e4f-118">Sitten **Aallot**-sivulla toimintoruudussa **Aalto**-välilehdessä **Aalto**-ryhmässä valitse **Tyhjennä aallon tiedot**.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="e9e4f-119">Ongelman kiertäminen</span><span class="sxs-lookup"><span data-stu-id="e9e4f-119">Workaround</span></span>

<span data-ttu-id="e9e4f-120">Jos edelliset vaiheet eivät korjaa ongelmaa, voit peruuttaa työn noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="e9e4f-121">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="e9e4f-122">Määritä **Työtunnus**-kentässä peruutettavan työn tunnus ja jonka **Työn tila** -arvona on *Avoinna*, *Käsittelyssä*, *Peruutettu*, *Yhdistetty* tai *Suljettu*.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="e9e4f-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-123">Select **OK**.</span></span>
1. <span data-ttu-id="e9e4f-124">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e9e4f-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="e9e4f-125">Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="e9e4f-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
