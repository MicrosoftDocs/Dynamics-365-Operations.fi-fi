---
title: Määritä ja suorita työ laskelmien laskemiseksi
description: Tässä menettelyssä kerrotaan, miten toistuvat erätyöt määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle luodaan ja lasketaan laskelmat.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 402ddf9a2646b2db0346e01504e8188120f16ae5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982210"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="ea216-103">Määritä ja suorita työ laskelmien laskemiseksi</span><span class="sxs-lookup"><span data-stu-id="ea216-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea216-104">Tässä menettelyssä kerrotaan, miten toistuvat erätyöt määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle luodaan ja lasketaan laskelmat.</span><span class="sxs-lookup"><span data-stu-id="ea216-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="ea216-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="ea216-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ea216-106">Siirry kohtaan Kaikki työtilat > Myymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="ea216-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="ea216-107">Valitse Laske laskelmat.</span><span class="sxs-lookup"><span data-stu-id="ea216-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="ea216-108">Valitse tietty myymälä tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="ea216-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ea216-109">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="ea216-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="ea216-110">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="ea216-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="ea216-111">Valitse Eräkäsittely-kohdassa Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ea216-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="ea216-112">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="ea216-112">Click Recurrence.</span></span>
6. <span data-ttu-id="ea216-113">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea216-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ea216-114">Syötä Aloitusaika-kenttään aika.</span><span class="sxs-lookup"><span data-stu-id="ea216-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="ea216-115">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="ea216-115">Select the No end date option.</span></span>
9. <span data-ttu-id="ea216-116">Syötä PatternUnit-kenttään Päivät.</span><span class="sxs-lookup"><span data-stu-id="ea216-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="ea216-117">Syötä numero Per-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ea216-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="ea216-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea216-118">Click OK.</span></span>
12. <span data-ttu-id="ea216-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea216-119">Click OK.</span></span>

