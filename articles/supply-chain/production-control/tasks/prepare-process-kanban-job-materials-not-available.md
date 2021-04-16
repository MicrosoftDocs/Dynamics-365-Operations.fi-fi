---
title: Prosessin kanban-työn valmisteleminen kun materiaalit eivät ole käytettävissä työsolulle
description: Tässä menettelyssä keskitytään prosessin kanban-töiden valmisteluun, kun osa työsolun materiaalista ei ole valmiina. Materiaalit on siis kerättävä varastosta.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72fd083edc48504b35f540ea7bdc8c8c736418f3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828631"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="33e34-103">Prosessin kanban-työn valmisteleminen kun materiaalit eivät ole käytettävissä työsolulle</span><span class="sxs-lookup"><span data-stu-id="33e34-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33e34-104">Tässä menettelyssä keskitytään prosessin kanban-töiden valmisteluun, kun osa työsolun materiaalista ei ole valmiina. Materiaalit on siis kerättävä varastosta.</span><span class="sxs-lookup"><span data-stu-id="33e34-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="33e34-105">Valmistele prosessin kanban-työ kun materiaalit ovat käytettävissä työsolulle -menettely on tämän menettelyn luomisen edellytys.</span><span class="sxs-lookup"><span data-stu-id="33e34-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="33e34-106">Tämä menettely on tarkoitettu koneenkäyttäjille.</span><span class="sxs-lookup"><span data-stu-id="33e34-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="33e34-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="33e34-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="33e34-108">Siirry kohtaan Tuotannonhallinta > Kanban > Prosessitöiden kanban-taulu.</span><span class="sxs-lookup"><span data-stu-id="33e34-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="33e34-109">Avaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="33e34-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="33e34-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="33e34-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="33e34-111">Valitse työsolu 1250.</span><span class="sxs-lookup"><span data-stu-id="33e34-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="33e34-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="33e34-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33e34-113">Valitse kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="33e34-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="33e34-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="33e34-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33e34-115">Poista luettelossa rivin 4 valinta.</span><span class="sxs-lookup"><span data-stu-id="33e34-115">In the list, deselect row 4.</span></span> <span data-ttu-id="33e34-116">Tai valitse rivi 4, jos Käsittele prosessin kanban-työ, kun materiaalit ovat käytettävissä -tehtävä ei ole valmis.</span><span class="sxs-lookup"><span data-stu-id="33e34-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="33e34-117">Ota käyttöön Keräysluettelo-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="33e34-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="33e34-118">Jos toimituksen tilan yhteydessä on Ei kirjausta -kuvake, työsolun nimikkeestä P0002 puuttuu 48 kappaletta.</span><span class="sxs-lookup"><span data-stu-id="33e34-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="33e34-119">Materiaalien siirtäminen työsoluun</span><span class="sxs-lookup"><span data-stu-id="33e34-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="33e34-120">Ota käyttöön Siirtotyöt-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="33e34-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="33e34-121">Pikasuodattimen avulla voit suodattaa Nimiketunnus-kentän arvon P0002 mukaan.</span><span class="sxs-lookup"><span data-stu-id="33e34-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="33e34-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="33e34-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="33e34-123">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="33e34-123">Click Start.</span></span>
    * <span data-ttu-id="33e34-124">Siirto on meneillään.</span><span class="sxs-lookup"><span data-stu-id="33e34-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="33e34-125">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="33e34-125">Click Complete.</span></span>
    * <span data-ttu-id="33e34-126">Nimike P0002 on nyt käytettävissä kanban-työnä keräysluettelossa.</span><span class="sxs-lookup"><span data-stu-id="33e34-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="33e34-127">Voit siis alkaa valmistella kanbania ja tarvittavia materiaaleja.</span><span class="sxs-lookup"><span data-stu-id="33e34-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="33e34-128">Valitse Valmistele.</span><span class="sxs-lookup"><span data-stu-id="33e34-128">Click Prepare.</span></span>
    * <span data-ttu-id="33e34-129">Huomaa, että työn tilan kuvake osoittaa työn olevan valmis.</span><span class="sxs-lookup"><span data-stu-id="33e34-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]