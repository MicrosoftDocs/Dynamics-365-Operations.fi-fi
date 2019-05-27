---
title: Muuta prosessityön kanban-sääntöjä
description: Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554273"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="79f5a-103">Muuta prosessityön kanban-sääntöjä</span><span class="sxs-lookup"><span data-stu-id="79f5a-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79f5a-104">Tässä menetelmässä käsitellään annetun kanbanin kanban-säännön vaihtamista.</span><span class="sxs-lookup"><span data-stu-id="79f5a-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="79f5a-105">Tämä kätevää tasoitettaessa resurssien kuormitusta tai vikaantumistapauksissa.</span><span class="sxs-lookup"><span data-stu-id="79f5a-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="79f5a-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="79f5a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="79f5a-107">Tämä menettely on tarkoitettu arvovirrasta vastaavalle Lean-tuotantoryrityksessä työskentelevälle suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="79f5a-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="79f5a-108">Kopioi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="79f5a-108">Copy kanban rule</span></span>
1. <span data-ttu-id="79f5a-109">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="79f5a-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="79f5a-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="79f5a-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="79f5a-111">Valitse L0001:lle tapahtuman kanban-sääntö 000022.</span><span class="sxs-lookup"><span data-stu-id="79f5a-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="79f5a-112">Valitse Kanban-säännön kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="79f5a-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="79f5a-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="79f5a-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="79f5a-114">Vaihda kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="79f5a-114">Change kanban rule</span></span>
1. <span data-ttu-id="79f5a-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="79f5a-115">Close the page.</span></span>
2. <span data-ttu-id="79f5a-116">Valitse Kanban-työn aikataulutus.</span><span class="sxs-lookup"><span data-stu-id="79f5a-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="79f5a-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79f5a-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="79f5a-118">Valitse rivi, jossa on kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="79f5a-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="79f5a-119">Valitse Käytä vaihtoehtoista kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="79f5a-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="79f5a-120">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="79f5a-120">Click Next.</span></span>
6. <span data-ttu-id="79f5a-121">Anna tai valitse Kanban-sääntö-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="79f5a-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="79f5a-122">Valitse aiemmin luotu kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="79f5a-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="79f5a-123">Tällä kanban-säännölle on suurin numero.</span><span class="sxs-lookup"><span data-stu-id="79f5a-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="79f5a-124">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="79f5a-124">Click Finish.</span></span>
    * <span data-ttu-id="79f5a-125">Kanban-työ käyttää nyt toista kanban-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="79f5a-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="79f5a-126">Tämä on kätevää työsolujen kuormituksen tasoittamisessa.</span><span class="sxs-lookup"><span data-stu-id="79f5a-126">This can be useful to level load work cells.</span></span>  

