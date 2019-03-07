---
title: Erätyön luominen
description: Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "313356"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="cbdcc-103">Erätyön luominen</span><span class="sxs-lookup"><span data-stu-id="cbdcc-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbdcc-104">Erätyö on joukko tehtäviä, jotka lähetetään Application Object Server -palvelinesiintymään (AOS) automaattista käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="cbdcc-105">Erätyöt suoritetaan sen käyttäjän käyttöoikeustiedoilla, joka on luonut työn.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="cbdcc-106">Luo erätyö seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="cbdcc-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="cbdcc-108">Luo erätyö</span><span class="sxs-lookup"><span data-stu-id="cbdcc-108">Create the batch job</span></span>
1. <span data-ttu-id="cbdcc-109">Valitse Järjestelmänhallinta > Kyselyt > Erätyöt.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="cbdcc-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-110">Click New.</span></span>
3. <span data-ttu-id="cbdcc-111">Kirjoita arvo Työnkuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="cbdcc-112">Määritä päivämäärä ja kellonaika kentässä Ajoitettu alkamispäivämäärä/-kellonaika.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="cbdcc-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="cbdcc-114">Luo toistuvuus</span><span class="sxs-lookup"><span data-stu-id="cbdcc-114">Create a recurrence</span></span>
1. <span data-ttu-id="cbdcc-115">Valitse toimintoruudussa Erätyö.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="cbdcc-116">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-116">Click Recurrence.</span></span>
    * <span data-ttu-id="cbdcc-117">Aseta toistumisalue ja -kuvio näiden asetusten avulla.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="cbdcc-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="cbdcc-119">Lisää hälytyksiä</span><span class="sxs-lookup"><span data-stu-id="cbdcc-119">Add alerts</span></span>
1. <span data-ttu-id="cbdcc-120">Valitse toimintoruudussa Erätyö.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="cbdcc-121">Valitse Hälytykset.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-121">Click Alerts.</span></span>
    * <span data-ttu-id="cbdcc-122">Ilmaise, haluatko lähettää hälytysviestin, kun erätyö on päättynyt tai peruutettu, tai jos siinä on kohdattu virhe.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="cbdcc-123">Määritä sitten, haluatko ilmoitukset ponnahdussanomina.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="cbdcc-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cbdcc-124">Click OK.</span></span>

