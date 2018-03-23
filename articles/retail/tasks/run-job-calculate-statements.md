--- 
title: "Määritä ja suorita työ laskelmien laskemiseksi"
description: "Tässä menettelyssä kerrotaan, miten toistuvat erätyöt määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle luodaan ja lasketaan laskelmat."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7bc936cdba771d322676565c2615ad75649cc50b
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="a6aa5-103">Määritä ja suorita työ laskelmien laskemiseksi</span><span class="sxs-lookup"><span data-stu-id="a6aa5-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a6aa5-104">Tässä menettelyssä kerrotaan, miten toistuvat erätyöt määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle luodaan ja lasketaan laskelmat.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="a6aa5-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a6aa5-106">Siirry kohtaan Kaikki työtilat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="a6aa5-107">Valitse Laske laskelmat.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="a6aa5-108">Valitse tietty myymälä tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="a6aa5-109">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="a6aa5-110">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="a6aa5-111">Valitse Eräkäsittely-kohdassa Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="a6aa5-112">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-112">Click Recurrence.</span></span>
6. <span data-ttu-id="a6aa5-113">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="a6aa5-114">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="a6aa5-115">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-115">Select the No end date option.</span></span>
9. <span data-ttu-id="a6aa5-116">Syötä PatternUnit-kenttään Päivät.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="a6aa5-117">Syötä numero Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="a6aa5-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-118">Click OK.</span></span>
12. <span data-ttu-id="a6aa5-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a6aa5-119">Click OK.</span></span>


