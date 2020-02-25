---
title: Määritä ja suorita työ laskelmien kirjaamiseksi
description: Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09a47e268e271cf86e63ceff913435842f017bb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022365"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="a0e2b-103">Määritä ja suorita työ laskelmien kirjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="a0e2b-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a0e2b-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="a0e2b-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a0e2b-106">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="a0e2b-106">Go to All workspaces > ..</span></span> <span data-ttu-id="a0e2b-107">> Myymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-107">> Store financials.</span></span>
2. <span data-ttu-id="a0e2b-108">Napsauta Laskelmien kirjaaminen eräajona.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="a0e2b-109">Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="a0e2b-110">Valitse solmu, jos haluat luoda myymäläryhmän erätyön.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="a0e2b-111">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="a0e2b-112">Valitse Suorita taustalla -välilehti. ![Suorita taustalla](../dev-itpro/media/runbackground.png "Suorita taustalla")</span><span class="sxs-lookup"><span data-stu-id="a0e2b-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="a0e2b-113">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="a0e2b-114">![Eräkäsittely](../dev-itpro/media/batchprocessing.png "Eräkäsittely & toistuvuus")</span><span class="sxs-lookup"><span data-stu-id="a0e2b-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="a0e2b-115">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-115">Click Recurrence.</span></span>
6. <span data-ttu-id="a0e2b-116">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="a0e2b-117">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="a0e2b-118">Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="a0e2b-119">Määritä sitten työn toistovälit eri vaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="a0e2b-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-120">Click OK.</span></span>
9. <span data-ttu-id="a0e2b-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a0e2b-121">Click OK.</span></span>

