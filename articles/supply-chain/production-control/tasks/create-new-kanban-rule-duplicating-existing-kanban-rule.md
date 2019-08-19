---
title: Luo uusi kanban-sääntö kopioimalla olemassa oleva sääntö
description: Tässä menettelyssä käsitellään aiemmin luodun kanban-säännön kaksoiskappaleen luomista.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3aef2725152d39e49070f33d0c56089200c94353
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837803"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="4b92f-103">Luo uusi kanban-sääntö kopioimalla olemassa oleva sääntö</span><span class="sxs-lookup"><span data-stu-id="4b92f-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b92f-104">Tässä menettelyssä käsitellään aiemmin luodun kanban-säännön kaksoiskappaleen luomista.</span><span class="sxs-lookup"><span data-stu-id="4b92f-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="4b92f-105">Tämä on kätevää, jos haluat luoda aiemmin luotuihin kanban-sääntöihin perustuvia uusia kanban-sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="4b92f-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="4b92f-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="4b92f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4b92f-107">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle muutetun tuotantovirran tai uuden täydennyssäännön tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="4b92f-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="4b92f-108">Valitse kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="4b92f-108">Select a kanban rule</span></span>
1. <span data-ttu-id="4b92f-109">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="4b92f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="4b92f-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4b92f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4b92f-111">Valitse tuotteelle M0006 kanban-sääntö 000017.</span><span class="sxs-lookup"><span data-stu-id="4b92f-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="4b92f-112">Kanban-säännön kaksoiskappale</span><span class="sxs-lookup"><span data-stu-id="4b92f-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="4b92f-113">Valitse Kanban-säännön kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="4b92f-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="4b92f-114">Kun kanban-säännöstä tehdään kaksoiskappale, tyyppi-, päivämäärä-, tehtävä -ja tuotevalintaa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="4b92f-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="4b92f-115">Tämän menettely vaihdetaan menettelyn seuraavassa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="4b92f-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="4b92f-116">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="4b92f-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="4b92f-117">Valitse M0007.</span><span class="sxs-lookup"><span data-stu-id="4b92f-117">Select M0007.</span></span>  
3. <span data-ttu-id="4b92f-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4b92f-118">Click OK.</span></span>
    * <span data-ttu-id="4b92f-119">Huomaa, että kanban-säännön 000017 kaksoiskappale luodaan.</span><span class="sxs-lookup"><span data-stu-id="4b92f-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

