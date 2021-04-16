---
title: Määritä ja suorita työ laskelmien kirjaamiseksi
description: Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52baa707c36f3468263782dc8ec735e44af88e38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804230"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="be24d-103">Määritä ja suorita työ laskelmien kirjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="be24d-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be24d-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.</span><span class="sxs-lookup"><span data-stu-id="be24d-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="be24d-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="be24d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="be24d-106">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="be24d-106">Go to All workspaces > ..</span></span> <span data-ttu-id="be24d-107">> Myymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="be24d-107">> Store financials.</span></span>
2. <span data-ttu-id="be24d-108">Napsauta Laskelmien kirjaaminen eräajona.</span><span class="sxs-lookup"><span data-stu-id="be24d-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="be24d-109">Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu.</span><span class="sxs-lookup"><span data-stu-id="be24d-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="be24d-110">Valitse solmu, jos haluat luoda myymäläryhmän erätyön.</span><span class="sxs-lookup"><span data-stu-id="be24d-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="be24d-111">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="be24d-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="be24d-112">Valitse Suorita taustalla -välilehti. ![Suorita taustalla](../dev-itpro/media/runbackground.png "Suorita taustalla")</span><span class="sxs-lookup"><span data-stu-id="be24d-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="be24d-113">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="be24d-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="be24d-114">![Eräkäsittely](../dev-itpro/media/batchprocessing.png "Eräkäsittely & toistuvuus")</span><span class="sxs-lookup"><span data-stu-id="be24d-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="be24d-115">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="be24d-115">Click Recurrence.</span></span>
6. <span data-ttu-id="be24d-116">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="be24d-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="be24d-117">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="be24d-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="be24d-118">Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="be24d-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="be24d-119">Määritä sitten työn toistovälit eri vaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="be24d-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="be24d-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="be24d-120">Click OK.</span></span>
9. <span data-ttu-id="be24d-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="be24d-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]