---
title: Erätyön luominen
description: Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143670"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="bca9c-103">Erätyön luominen</span><span class="sxs-lookup"><span data-stu-id="bca9c-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bca9c-104">Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="bca9c-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="bca9c-105">Erätyöt suoritetaan sen käyttäjän käyttöoikeustiedoilla, joka on luonut työn.</span><span class="sxs-lookup"><span data-stu-id="bca9c-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="bca9c-106">Luo erätyö seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="bca9c-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="bca9c-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="bca9c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="bca9c-108">Luo erätyö</span><span class="sxs-lookup"><span data-stu-id="bca9c-108">Create the batch job</span></span>
1. <span data-ttu-id="bca9c-109">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Kyselyt > Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="bca9c-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-110">Click **New**.</span></span>
3. <span data-ttu-id="bca9c-111">Kirjoita arvo **Työnkuvaus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="bca9c-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="bca9c-112">Määritä päivämäärä ja kellonaika **Ajoitettu alkamispäivämäärä/-kellonaika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="bca9c-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="bca9c-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="bca9c-114">Luo toistuvuus</span><span class="sxs-lookup"><span data-stu-id="bca9c-114">Create a recurrence</span></span>
1. <span data-ttu-id="bca9c-115">Valitse toimintoruudussa **Erätyö**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="bca9c-116">Valitse **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-116">Click **Recurrence**.</span></span> <span data-ttu-id="bca9c-117">Aseta toistumisalue ja -kuvio näiden asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="bca9c-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="bca9c-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="bca9c-119">Lisää hälytyksiä</span><span class="sxs-lookup"><span data-stu-id="bca9c-119">Add alerts</span></span>
1. <span data-ttu-id="bca9c-120">Valitse toimintoruudussa **Erätyö**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="bca9c-121">Valitse **Hälytykset**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-121">Click **Alerts**.</span></span> <span data-ttu-id="bca9c-122">Ilmaise, haluatko lähettää hälytysviestin, kun erätyö on päättynyt tai peruutettu, tai jos siinä on kohdattu virhe.</span><span class="sxs-lookup"><span data-stu-id="bca9c-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="bca9c-123">Määritä sitten, haluatko ilmoitukset ponnahdussanomina.</span><span class="sxs-lookup"><span data-stu-id="bca9c-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="bca9c-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="bca9c-125">Erätyön tilan säätäminen</span><span class="sxs-lookup"><span data-stu-id="bca9c-125">Adjust batch job status</span></span>
1. <span data-ttu-id="bca9c-126">Valitse **Järjestelmän hallinta > Kyselyt > Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="bca9c-127">Valitse soveltuva erätyö.</span><span class="sxs-lookup"><span data-stu-id="bca9c-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="bca9c-128">Valitse toimintoruudussa **Erätyö > Toiminnot > Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="bca9c-129">Valitse sopiva tila:</span><span class="sxs-lookup"><span data-stu-id="bca9c-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="bca9c-130">**Pidätä**: Määritä erätyö **pidätettynä**, jolloin sitä ei anneta erätyön ajastukseen.</span><span class="sxs-lookup"><span data-stu-id="bca9c-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="bca9c-131">Vastaa *pysäyttämistä*.</span><span class="sxs-lookup"><span data-stu-id="bca9c-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="bca9c-132">**Odottaa**: Määritä erätyö **odottavaksi**, jolloin se odottaa erätyön ajastuksen tekemään poimimista.</span><span class="sxs-lookup"><span data-stu-id="bca9c-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="bca9c-133">Vastaa *siirtymistä*.</span><span class="sxs-lookup"><span data-stu-id="bca9c-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="bca9c-134">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bca9c-134">Click **OK**.</span></span>
