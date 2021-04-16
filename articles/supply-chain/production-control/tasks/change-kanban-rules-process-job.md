---
title: Muuta prosessityön kanban-sääntöjä
description: Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bdbbbf8a8b3d1596c251224cba996c0631050c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829303"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="8e02d-103">Muuta prosessityön kanban-sääntöjä</span><span class="sxs-lookup"><span data-stu-id="8e02d-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e02d-104">Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista.</span><span class="sxs-lookup"><span data-stu-id="8e02d-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="8e02d-105">Tämä kätevää tasoitettaessa resurssien kuormitusta tai vikaantumistapauksissa.</span><span class="sxs-lookup"><span data-stu-id="8e02d-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="8e02d-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="8e02d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8e02d-107">Tämä menettely on tarkoitettu arvovirrasta vastaavalle Lean-tuotantoryrityksessä työskentelevälle suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="8e02d-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="8e02d-108">Kopioi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="8e02d-108">Copy kanban rule</span></span>
1. <span data-ttu-id="8e02d-109">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="8e02d-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="8e02d-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8e02d-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8e02d-111">Valitse L0001:lle tapahtuman kanban-sääntö 000022.</span><span class="sxs-lookup"><span data-stu-id="8e02d-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="8e02d-112">Valitse Kanban-säännön kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="8e02d-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="8e02d-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8e02d-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="8e02d-114">Vaihda kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="8e02d-114">Change kanban rule</span></span>
1. <span data-ttu-id="8e02d-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8e02d-115">Close the page.</span></span>
2. <span data-ttu-id="8e02d-116">Valitse Kanban-työn aikataulutus.</span><span class="sxs-lookup"><span data-stu-id="8e02d-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="8e02d-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8e02d-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8e02d-118">Valitse rivi, jossa on kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="8e02d-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="8e02d-119">Valitse Käytä vaihtoehtoista kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="8e02d-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="8e02d-120">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="8e02d-120">Click Next.</span></span>
6. <span data-ttu-id="8e02d-121">Anna tai valitse Kanban-sääntö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8e02d-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="8e02d-122">Valitse aiemmin luotu kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="8e02d-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="8e02d-123">Tällä kanban-säännölle on suurin numero.</span><span class="sxs-lookup"><span data-stu-id="8e02d-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="8e02d-124">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="8e02d-124">Click Finish.</span></span>
    * <span data-ttu-id="8e02d-125">Kanban-työ käyttää nyt toista kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="8e02d-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="8e02d-126">Tämä on kätevää työsolujen kuormituksen tasoittamisessa.</span><span class="sxs-lookup"><span data-stu-id="8e02d-126">This can be useful to level load work cells.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]