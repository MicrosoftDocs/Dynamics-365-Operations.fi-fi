---
title: Aalto ei ole puhdistuskelpoinen.
description: Aalto ei ole puhdistuskelpoinen.
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924324"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="786ba-103">Aalto ei ole puhdistuskelpoinen.</span><span class="sxs-lookup"><span data-stu-id="786ba-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="786ba-104">Virhekoodi: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="786ba-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="786ba-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="786ba-105">Symptoms</span></span>

<span data-ttu-id="786ba-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="786ba-106">The system shows the following error message:</span></span>

> <span data-ttu-id="786ba-107">Aaltoa %1 ei voi tyhjentää.</span><span class="sxs-lookup"><span data-stu-id="786ba-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="786ba-108">Aallon tietoja ei voi puhdistaa.</span><span class="sxs-lookup"><span data-stu-id="786ba-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="786ba-109">Syy</span><span class="sxs-lookup"><span data-stu-id="786ba-109">Cause</span></span>

<span data-ttu-id="786ba-110">Aaltoa käsitellään parhaillaan, kuten jokin seuraavista ehdoista on osoittanut:</span><span class="sxs-lookup"><span data-stu-id="786ba-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="786ba-111">**Aallon tila** -kentän arvona on *Suoritetaan*.</span><span class="sxs-lookup"><span data-stu-id="786ba-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="786ba-112">Kun valitset **Erätyö** **Aalto**-ryhmässä toimintoruudun **Aalto**-välilehdellä, **Tila**-kentän arvoksi ei määritetä *Päättynyt*, *Virhe* tai *Peruutettu*.</span><span class="sxs-lookup"><span data-stu-id="786ba-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="786ba-113">Siksi erätyö on tällä hetkellä käynnissä.</span><span class="sxs-lookup"><span data-stu-id="786ba-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="786ba-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="786ba-114">Resolution</span></span>

<span data-ttu-id="786ba-115">Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmässä **Erätyö** ja seuraa jotakin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="786ba-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="786ba-116">Jos **Tila**-kentän arvona on *Suoritetaan*: Valitse toimintoruudussa **Erätyö**-välilehdellä **Erätyö**-ryhmässä **Näytä tehtävät**.</span><span class="sxs-lookup"><span data-stu-id="786ba-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="786ba-117">Voit valvoa edistymistä päivittämällä **Etätehtävät**-sivun.</span><span class="sxs-lookup"><span data-stu-id="786ba-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="786ba-118">Jos **Tila**-kentän arvona ei ole *Suoritetaan*: Valitse toimintoruudussa **Erätyö**-välilehdellä **Toiminnot**-ryhmässä **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="786ba-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="786ba-119">Valitse **Valitse uusi tila** -kentässä *Odottaa*.</span><span class="sxs-lookup"><span data-stu-id="786ba-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="786ba-120">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="786ba-120">Then select **OK**.</span></span>
