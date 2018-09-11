--- 
title: "Erätyön luominen"
description: "Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 7c5408f331473d677c84dbfc7f2524be9d98c5c6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-batch-job"></a><span data-ttu-id="69ccc-103">Erätyön luominen</span><span class="sxs-lookup"><span data-stu-id="69ccc-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69ccc-104">Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="69ccc-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="69ccc-105">Erätyöt suoritetaan sen käyttäjän käyttöoikeustiedoilla, joka on luonut työn.</span><span class="sxs-lookup"><span data-stu-id="69ccc-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="69ccc-106">Luo erätyö seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="69ccc-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="69ccc-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="69ccc-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="69ccc-108">Luo erätyö</span><span class="sxs-lookup"><span data-stu-id="69ccc-108">Create the batch job</span></span>
1. <span data-ttu-id="69ccc-109">Valitse Järjestelmänhallinta > Kyselyt > Erätyöt.</span><span class="sxs-lookup"><span data-stu-id="69ccc-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="69ccc-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="69ccc-110">Click New.</span></span>
3. <span data-ttu-id="69ccc-111">Kirjoita arvo Työnkuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="69ccc-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="69ccc-112">Määritä päivämäärä ja kellonaika kentässä Ajoitettu alkamispäivämäärä/-kellonaika.</span><span class="sxs-lookup"><span data-stu-id="69ccc-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="69ccc-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="69ccc-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="69ccc-114">Luo toistuvuus</span><span class="sxs-lookup"><span data-stu-id="69ccc-114">Create a recurrence</span></span>
1. <span data-ttu-id="69ccc-115">Valitse toimintoruudussa Erätyö.</span><span class="sxs-lookup"><span data-stu-id="69ccc-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="69ccc-116">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="69ccc-116">Click Recurrence.</span></span>
    * <span data-ttu-id="69ccc-117">Aseta toistumisalue ja -kuvio näiden asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="69ccc-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="69ccc-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="69ccc-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="69ccc-119">Lisää hälytyksiä</span><span class="sxs-lookup"><span data-stu-id="69ccc-119">Add alerts</span></span>
1. <span data-ttu-id="69ccc-120">Valitse toimintoruudussa Erätyö.</span><span class="sxs-lookup"><span data-stu-id="69ccc-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="69ccc-121">Valitse Hälytykset.</span><span class="sxs-lookup"><span data-stu-id="69ccc-121">Click Alerts.</span></span>
    * <span data-ttu-id="69ccc-122">Ilmaise, haluatko lähettää hälytysviestin, kun erätyö on päättynyt tai peruutettu, tai jos siinä on kohdattu virhe.</span><span class="sxs-lookup"><span data-stu-id="69ccc-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="69ccc-123">Määritä sitten, haluatko ilmoitukset ponnahdussanomina.</span><span class="sxs-lookup"><span data-stu-id="69ccc-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="69ccc-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="69ccc-124">Click OK.</span></span>


