---
title: Määritä ja suorita työ laskelmien kirjaamiseksi
description: Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "346292"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="c87ca-103">Määritä ja suorita työ laskelmien kirjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="c87ca-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c87ca-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.</span><span class="sxs-lookup"><span data-stu-id="c87ca-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="c87ca-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="c87ca-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c87ca-106">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="c87ca-106">Go to All workspaces > ..</span></span> <span data-ttu-id="c87ca-107">> Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="c87ca-107">> Retail store financials.</span></span>
2. <span data-ttu-id="c87ca-108">Valitse Kirjaa laskelmat.</span><span class="sxs-lookup"><span data-stu-id="c87ca-108">Click Post statements.</span></span>
    * <span data-ttu-id="c87ca-109">Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu.</span><span class="sxs-lookup"><span data-stu-id="c87ca-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="c87ca-110">Valitse solmu, jos haluat luoda myymäläryhmän erätyön.</span><span class="sxs-lookup"><span data-stu-id="c87ca-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c87ca-111">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="c87ca-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="c87ca-112">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="c87ca-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="c87ca-113">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="c87ca-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="c87ca-114">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="c87ca-114">Click Recurrence.</span></span>
6. <span data-ttu-id="c87ca-115">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c87ca-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="c87ca-116">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="c87ca-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="c87ca-117">Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="c87ca-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="c87ca-118">Määritä sitten työn toistovälit eri vaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="c87ca-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="c87ca-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c87ca-119">Click OK.</span></span>
9. <span data-ttu-id="c87ca-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c87ca-120">Click OK.</span></span>

