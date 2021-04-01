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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1401d51491205731843abe6e2278f798c5c979
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232734"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="f11a5-103">Määritä ja suorita työ laskelmien kirjaamiseksi</span><span class="sxs-lookup"><span data-stu-id="f11a5-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f11a5-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle kirjataan laskelmia.</span><span class="sxs-lookup"><span data-stu-id="f11a5-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="f11a5-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="f11a5-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f11a5-106">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="f11a5-106">Go to All workspaces > ..</span></span> <span data-ttu-id="f11a5-107">> Myymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="f11a5-107">> Store financials.</span></span>
2. <span data-ttu-id="f11a5-108">Napsauta Laskelmien kirjaaminen eräajona.</span><span class="sxs-lookup"><span data-stu-id="f11a5-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="f11a5-109">Valitse organisaatiohierarkia ja sitten organisaatiosolmujen puu. Valitse yksittäinen myymälä tai solmu.</span><span class="sxs-lookup"><span data-stu-id="f11a5-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="f11a5-110">Valitse solmu, jos haluat luoda myymäläryhmän erätyön.</span><span class="sxs-lookup"><span data-stu-id="f11a5-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="f11a5-111">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="f11a5-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="f11a5-112">Valitse Suorita taustalla -välilehti. ![Suorita taustalla](../dev-itpro/media/runbackground.png "Suorita taustalla")</span><span class="sxs-lookup"><span data-stu-id="f11a5-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="f11a5-113">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="f11a5-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="f11a5-114">![Eräkäsittely](../dev-itpro/media/batchprocessing.png "Eräkäsittely & toistuvuus")</span><span class="sxs-lookup"><span data-stu-id="f11a5-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="f11a5-115">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="f11a5-115">Click Recurrence.</span></span>
6. <span data-ttu-id="f11a5-116">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f11a5-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="f11a5-117">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="f11a5-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="f11a5-118">Määritä, päätetäänkö toisto tietyn suoritusmäärän jälkeen, tiettynä päivänä vai ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="f11a5-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="f11a5-119">Määritä sitten työn toistovälit eri vaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="f11a5-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="f11a5-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f11a5-120">Click OK.</span></span>
9. <span data-ttu-id="f11a5-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f11a5-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]