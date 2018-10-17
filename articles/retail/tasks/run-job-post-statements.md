--- 
title: "Määritä ja suorita työ laskelmien kirjaamiseksi"
description: "Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="e6b98-103">Määritä ja suorita työ laskelmien kirjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="e6b98-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e6b98-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.</span><span class="sxs-lookup"><span data-stu-id="e6b98-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="e6b98-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="e6b98-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e6b98-106">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="e6b98-106">Go to All workspaces > ..</span></span> <span data-ttu-id="e6b98-107">> Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="e6b98-107">> Retail store financials.</span></span>
2. <span data-ttu-id="e6b98-108">Valitse Kirjaa laskelmat.</span><span class="sxs-lookup"><span data-stu-id="e6b98-108">Click Post statements.</span></span>
    * <span data-ttu-id="e6b98-109">Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu.</span><span class="sxs-lookup"><span data-stu-id="e6b98-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="e6b98-110">Valitse solmu, jos haluat luoda myymäläryhmän erätyön.</span><span class="sxs-lookup"><span data-stu-id="e6b98-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e6b98-111">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="e6b98-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="e6b98-112">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="e6b98-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="e6b98-113">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="e6b98-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="e6b98-114">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="e6b98-114">Click Recurrence.</span></span>
6. <span data-ttu-id="e6b98-115">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e6b98-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="e6b98-116">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="e6b98-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="e6b98-117">Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="e6b98-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="e6b98-118">Määritä sitten työn toistovälit eri vaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="e6b98-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="e6b98-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e6b98-119">Click OK.</span></span>
9. <span data-ttu-id="e6b98-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e6b98-120">Click OK.</span></span>


