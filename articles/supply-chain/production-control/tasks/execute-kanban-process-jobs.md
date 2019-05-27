---
title: Suorita kanban-prosessin töitä
description: Nämä toimet keskittyvät kanban-prosessitöiden suorittamiseen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62be1f116dfecbc4c6ba11053b94efc874baa3e3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567122"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="89554-103">Suorita kanban-prosessin töitä</span><span class="sxs-lookup"><span data-stu-id="89554-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89554-104">Nämä toimet keskittyvät kanban-prosessitöiden suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="89554-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="89554-105">Ensimmäinen työ on valmis, määrä on odotettu, eikä virheitä ole.</span><span class="sxs-lookup"><span data-stu-id="89554-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="89554-106">Toinen työ valmistuu, mutta siinä on virheitä.</span><span class="sxs-lookup"><span data-stu-id="89554-106">The second job is completed with errors.</span></span> <span data-ttu-id="89554-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="89554-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="89554-108">Tämä menettely on tarkoitettu koneenkäyttäjille.</span><span class="sxs-lookup"><span data-stu-id="89554-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="89554-109">Valitse kanban-työ.</span><span class="sxs-lookup"><span data-stu-id="89554-109">Select a kanban job</span></span>
1. <span data-ttu-id="89554-110">Siirry kohtaan Tuotannonhallinta > Kanban > Prosessitöiden kanban-taulu.</span><span class="sxs-lookup"><span data-stu-id="89554-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="89554-111">Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="89554-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="89554-112">Napsauta riviä, jonka resurssiryhmä on 1250.</span><span class="sxs-lookup"><span data-stu-id="89554-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="89554-113">Työluettelo suodatetaan niin, että se näyttää vain työsolun 1250 työt.</span><span class="sxs-lookup"><span data-stu-id="89554-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="89554-114">Valitse rivi, jonka työn tila on Suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="89554-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="89554-115">Viimeistele työ odotetulla määrällä</span><span class="sxs-lookup"><span data-stu-id="89554-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="89554-116">Laajenna tai tiivistä Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="89554-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="89554-117">Tässä osassa näkyy tärkeitä tietoja kortin numerosta, nimiketunnuksesta, tilatusta määrästä ja tehtävän nimestä.</span><span class="sxs-lookup"><span data-stu-id="89554-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="89554-118">Laajenna tai tiivistä Tuotanto-ohjeet-osa.</span><span class="sxs-lookup"><span data-stu-id="89554-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="89554-119">Tässä osassa näytetään tehtävän tuotanto-ohjeet.</span><span class="sxs-lookup"><span data-stu-id="89554-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="89554-120">Ohjeet voivat olla tekstiä, kuvia, piirroksia tai muita asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="89554-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="89554-121">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="89554-121">Click Start.</span></span>
    * <span data-ttu-id="89554-122">Valitse työ, joka ei ole valmis.</span><span class="sxs-lookup"><span data-stu-id="89554-122">Select a job that is not completed.</span></span> <span data-ttu-id="89554-123">Näet työn tilan Työn tila -kentän tilakuvakkeista.</span><span class="sxs-lookup"><span data-stu-id="89554-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="89554-124">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="89554-124">Click Complete.</span></span>
    * <span data-ttu-id="89554-125">Työ on valmis ja sen laatu vastaa odotuksia.</span><span class="sxs-lookup"><span data-stu-id="89554-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="89554-126">Viimeistele työ virheettömänä</span><span class="sxs-lookup"><span data-stu-id="89554-126">Complete a job with errors</span></span>
1. <span data-ttu-id="89554-127">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="89554-127">Click Start.</span></span>
    * <span data-ttu-id="89554-128">Kun työ valmistuu, luettelon seuraava työ valitaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="89554-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="89554-129">Tämän vuoksi sinun ei tarvitse valita työtä, ennen kuin napsautat Aloita-painiketta.</span><span class="sxs-lookup"><span data-stu-id="89554-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="89554-130">Valitse toimintoruudussa Valmista.</span><span class="sxs-lookup"><span data-stu-id="89554-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="89554-131">Napsauta Valmis (tiedot).</span><span class="sxs-lookup"><span data-stu-id="89554-131">Click Complete (details).</span></span>
4. <span data-ttu-id="89554-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="89554-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="89554-133">Syötä numero Virhemäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="89554-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="89554-134">Lisää Hyväksytty määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="89554-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="89554-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="89554-135">Click OK.</span></span>

