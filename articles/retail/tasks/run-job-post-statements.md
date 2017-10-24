--- 
title: "Määritä ja suorita työ laskelmien kirjaamiseksi"
description: "Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="0e5c8-103">Määritä ja suorita työ laskelmien kirjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="0e5c8-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0e5c8-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="0e5c8-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0e5c8-106">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="0e5c8-106">Go to All workspaces > ..</span></span> <span data-ttu-id="0e5c8-107">> Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-107">> Retail store financials.</span></span>
2. <span data-ttu-id="0e5c8-108">Valitse Kirjaa laskelmat.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-108">Click Post statements.</span></span>
    * <span data-ttu-id="0e5c8-109">Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="0e5c8-110">Valitse solmu, jos haluat luoda myymäläryhmän erätyön.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="0e5c8-111">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="0e5c8-112">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="0e5c8-113">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="0e5c8-114">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-114">Click Recurrence.</span></span>
6. <span data-ttu-id="0e5c8-115">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="0e5c8-116">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="0e5c8-117">Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="0e5c8-118">Määritä sitten työn toistovälit eri vaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="0e5c8-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-119">Click OK.</span></span>
9. <span data-ttu-id="0e5c8-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5c8-120">Click OK.</span></span>


