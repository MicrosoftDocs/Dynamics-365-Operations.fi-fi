---
title: Poista kanban-työ aikataulusta
description: Tässä menettelyssä keskitytään prosessin suunnitellun kanban-työn poistamiseen aikataulusta palauttamalla työn tilaksi Ei suunniteltu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b2137268301beb85906bf7fb26c41f6eb09534c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148913"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="a5049-103">Poista kanban-työ aikataulusta</span><span class="sxs-lookup"><span data-stu-id="a5049-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5049-104">Tässä menettelyssä keskitytään prosessin suunnitellun kanban-työn poistamiseen aikataulusta palauttamalla työn tilaksi Ei suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="a5049-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="a5049-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a5049-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a5049-106">Tämä menettely on tarkoitettu työn ohjauksen esimiehelle tai tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="a5049-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="a5049-107">Suunnitellun kanban-työn etsiminen</span><span class="sxs-lookup"><span data-stu-id="a5049-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="a5049-108">Siirry kohtaan Tuotannonhallinta > Kanban > Kanban-työn aikataulutus.</span><span class="sxs-lookup"><span data-stu-id="a5049-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="a5049-109">Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a5049-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a5049-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a5049-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a5049-111">Valitse työsolu 1250.</span><span class="sxs-lookup"><span data-stu-id="a5049-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="a5049-112">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="a5049-112">Click Select.</span></span>
5. <span data-ttu-id="a5049-113">Valitse Näytä työn tila -kentässä Ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="a5049-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="a5049-114">Suunnitellun kanban-työn poistaminen aikataulusta</span><span class="sxs-lookup"><span data-stu-id="a5049-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="a5049-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a5049-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a5049-116">Valitse työ, jonka tila on Suunniteltu. Voit valita esimerkiksi työn, jonka päivämäärä on 19.12.2012.</span><span class="sxs-lookup"><span data-stu-id="a5049-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="a5049-117">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="a5049-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="a5049-118">Valitse Palauta työn tila.</span><span class="sxs-lookup"><span data-stu-id="a5049-118">Click Revert job status.</span></span>
4. <span data-ttu-id="a5049-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a5049-119">Click OK.</span></span>
    * <span data-ttu-id="a5049-120">Tällöin työn nykyinen tila muuttuu Suunniteltu-tilasta Ei suunniteltu -tilaan, ja työ poistetaan prosessitaululta.</span><span class="sxs-lookup"><span data-stu-id="a5049-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

