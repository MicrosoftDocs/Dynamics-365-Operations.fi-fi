---
title: Aiemmin luodun tehtävän lisääminen tuotantovirran versioon
description: Kun luot uusia tuotantovirtojen versioita, voit lisätä aiemmille versioille luotuja tehtäviä uuteen versioon.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032855125ccd14fbdc1e1bdb735c92ce70853fb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568373"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="6a9ce-103">Aiemmin luodun tehtävän lisääminen tuotantovirran versioon</span><span class="sxs-lookup"><span data-stu-id="6a9ce-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a9ce-104">Kun luot uusia tuotantovirtojen versioita, voit lisätä aiemmille versioille luotuja tehtäviä uuteen versioon.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="6a9ce-105">Tässä menettelyssä kuvataan, miten vanhalle tuotantovirralle luodaan uusi versio ilman, että tehtäviä kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="6a9ce-106">Vanha tehtävä lisätään uuteen versioon seuraavassa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="6a9ce-107">Tämän tehtävän edellytyksenä on tuotantovirran versio ja olemassa olevat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="6a9ce-108">Luo uusi tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="6a9ce-108">Create a new production flow version</span></span>
1. <span data-ttu-id="6a9ce-109">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6a9ce-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6a9ce-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6a9ce-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-112">Click Edit.</span></span>
5. <span data-ttu-id="6a9ce-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6a9ce-114">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="6a9ce-115">Huomaa, että ennen kuin luot uuden tuotantovirran version, varmista aktiivisen version vanhentumispäivämäärä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="6a9ce-116">Uudelle versiolle luodaan voimaantulon aloituspäivä, joka liittyy valitun version erääntymispäivään.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="6a9ce-117">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-117">Click Add.</span></span>
8. <span data-ttu-id="6a9ce-118">Valitse Kopioi versiosta -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="6a9ce-119">Valitse Ei, jos haluat aloittaa tyhjällä versiolla, jos suurin osa kopioidun version tehtävistä korvataan uusilla tehtävillä.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="6a9ce-120">Lisää muuttumattomat tehtävät manuaalisesti Lisää aiemmin luotu -toimintoon aktiviteettilomakkeella.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="6a9ce-121">Valitse Kanban-sääntöjen kaksoiskappaleet -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="6a9ce-122">Kun tehtäviä ei kopioida uuteen versioon, kanban-sääntöjä ei voi kopioida samalla, kun uusi versio luodaan.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="6a9ce-123">Käytät sen sijaan Luo korvaava kanban -toimintoa myöhemmin kanban-säännön lomakkeella korvataksesi vanhan tuotantovirran version kanban-säännöillä, jotka perustuvat uuden version tehtäviin.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="6a9ce-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-124">Click OK.</span></span>
11. <span data-ttu-id="6a9ce-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="6a9ce-126">Lisää aiemmin luotu tehtävä</span><span class="sxs-lookup"><span data-stu-id="6a9ce-126">Add an existing activity</span></span>
1. <span data-ttu-id="6a9ce-127">Valitse Tehtävät.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-127">Click Activities.</span></span>
2. <span data-ttu-id="6a9ce-128">Avaa valintaikkuna valitsemalla Lisää aiemmin luotu.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="6a9ce-129">Etsi ja valitse uuteen tuotantovirran versioon lisättävä vanha tehtävä.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="6a9ce-130">Huomaa, että luettelossa näkyvät kaikki ne tehtävät, jotka on luotu tämän tuotantovirran kaikkia aiempia versioita varten.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="6a9ce-131">Syötä tai valitse arvo Tehtävä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="6a9ce-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6a9ce-132">Click OK.</span></span>

