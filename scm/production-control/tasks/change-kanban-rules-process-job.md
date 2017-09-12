--- 
title: "Muuta prosessityön kanban-sääntöjä"
description: "Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="6be91-103">Muuta prosessityön kanban-sääntöjä</span><span class="sxs-lookup"><span data-stu-id="6be91-103">Change kanban rules for a process job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6be91-104">Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista.</span><span class="sxs-lookup"><span data-stu-id="6be91-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="6be91-105">Tämä kätevää tasoitettaessa resurssien kuormitusta tai vikaantumistapauksissa.</span><span class="sxs-lookup"><span data-stu-id="6be91-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="6be91-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="6be91-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6be91-107">Tämä menettely on tarkoitettu arvovirrasta vastaavalle Lean-tuotantoryrityksessä työskentelevälle suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="6be91-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="6be91-108">Kopioi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="6be91-108">Copy kanban rule</span></span>
1. <span data-ttu-id="6be91-109">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="6be91-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="6be91-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6be91-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6be91-111">Valitse L0001:lle tapahtuman kanban-sääntö 000022.</span><span class="sxs-lookup"><span data-stu-id="6be91-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="6be91-112">Valitse Kanban-säännön kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="6be91-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="6be91-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6be91-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="6be91-114">Vaihda kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="6be91-114">Change kanban rule</span></span>
1. <span data-ttu-id="6be91-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6be91-115">Close the page.</span></span>
2. <span data-ttu-id="6be91-116">Valitse Kanban-työn aikataulutus.</span><span class="sxs-lookup"><span data-stu-id="6be91-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="6be91-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6be91-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6be91-118">Valitse rivi, jossa on kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="6be91-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="6be91-119">Valitse Käytä vaihtoehtoista kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="6be91-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="6be91-120">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="6be91-120">Click Next.</span></span>
6. <span data-ttu-id="6be91-121">Anna tai valitse Kanban-sääntö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="6be91-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="6be91-122">Valitse aiemmin luotu kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="6be91-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="6be91-123">Tällä kanban-säännölle on suurin numero.</span><span class="sxs-lookup"><span data-stu-id="6be91-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="6be91-124">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="6be91-124">Click Finish.</span></span>
    * <span data-ttu-id="6be91-125">Kanban-työ käyttää nyt toista kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="6be91-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="6be91-126">Tämä on kätevää työsolujen kuormituksen tasoittamisessa.</span><span class="sxs-lookup"><span data-stu-id="6be91-126">This can be useful to level load work cells.</span></span>  


