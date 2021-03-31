---
title: Materiaalien siirtäminen kanban-töiden yhteydessä
description: Tässä menettelyssä keskitytään otto-kanbaneihin materiaalien siirtämiseksi.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df65ea59be29dbe4eaad30558fcff4394737158f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224927"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="ad95e-103">Materiaalien siirtäminen kanban-töiden yhteydessä</span><span class="sxs-lookup"><span data-stu-id="ad95e-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad95e-104">Tässä menettelyssä keskitytään otto-kanbaneihin materiaalien siirtämiseksi.</span><span class="sxs-lookup"><span data-stu-id="ad95e-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="ad95e-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ad95e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ad95e-106">Tämä menettely on tarkoitettu varastotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="ad95e-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="ad95e-107">Siirtotöiden näyttäminen</span><span class="sxs-lookup"><span data-stu-id="ad95e-107">Display transfer jobs</span></span>
1. <span data-ttu-id="ad95e-108">Siirry kohtaan Tuotannonhallinta > Kanban > Siirtotöiden Kanban-taulu.</span><span class="sxs-lookup"><span data-stu-id="ad95e-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="ad95e-109">Laajenna tai tiivistä Suodattimet-osa.</span><span class="sxs-lookup"><span data-stu-id="ad95e-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="ad95e-110">Suodattimet-osassa voit määrittää, mitkä työt näkyvät suodatettaessa tuotantovirran, tehtävän nimen, lähetysvaraston ja -sijainnin ja vastaanottovaraston ja -sijainnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="ad95e-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="ad95e-111">Syötä Varastosta-kenttään 11.</span><span class="sxs-lookup"><span data-stu-id="ad95e-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="ad95e-112">Syötä Varastoon-kenttään arvo 12.</span><span class="sxs-lookup"><span data-stu-id="ad95e-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="ad95e-113">Aloita siirtotyö</span><span class="sxs-lookup"><span data-stu-id="ad95e-113">Start a transfer job</span></span>
1. <span data-ttu-id="ad95e-114">Poista luettelosta mahdollisen valitun rivin valinta.</span><span class="sxs-lookup"><span data-stu-id="ad95e-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="ad95e-115">Valitse luettelosta rivi 4.</span><span class="sxs-lookup"><span data-stu-id="ad95e-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="ad95e-116">Valitse ensimmäisen työ, jonka tila on Ei Suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="ad95e-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="ad95e-117">Varmista, että tämä on ainoa valittu työ.</span><span class="sxs-lookup"><span data-stu-id="ad95e-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="ad95e-118">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="ad95e-118">Click Start.</span></span>
    * <span data-ttu-id="ad95e-119">Huomaa, että kuvake osoittaa työn alkaneen.</span><span class="sxs-lookup"><span data-stu-id="ad95e-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="ad95e-120">Toisen siirtotyön valitseminen ja määrän muuttaminen</span><span class="sxs-lookup"><span data-stu-id="ad95e-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="ad95e-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ad95e-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad95e-122">Voit valita useita töitä, mutta valitse tässä vaiheessa rivi 5.</span><span class="sxs-lookup"><span data-stu-id="ad95e-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="ad95e-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ad95e-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad95e-124">Varmista, että edellisen vaiheen työ on ainoa valittuna oleva.</span><span class="sxs-lookup"><span data-stu-id="ad95e-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="ad95e-125">Poista muiden töiden valinta.</span><span class="sxs-lookup"><span data-stu-id="ad95e-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="ad95e-126">Merkitse Työn määrä- kentän arvo muistiin myöhempää käyttöä varten</span><span class="sxs-lookup"><span data-stu-id="ad95e-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="ad95e-127">Määritä Työn määrä -kenttään arvo 30.</span><span class="sxs-lookup"><span data-stu-id="ad95e-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="ad95e-128">Huomaa varoitus!</span><span class="sxs-lookup"><span data-stu-id="ad95e-128">Notice the warning!</span></span> <span data-ttu-id="ad95e-129">30 on liikaa siirrettäväksi.</span><span class="sxs-lookup"><span data-stu-id="ad95e-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="ad95e-130">Kanban-säännön asetusten perusteella voit siirtää vain alkuperäisen määrän.</span><span class="sxs-lookup"><span data-stu-id="ad95e-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="ad95e-131">Käytä aiempaa Työn määrä -kentän arvoa</span><span class="sxs-lookup"><span data-stu-id="ad95e-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="ad95e-132">Määritä työn määräksi edellinen arvo.</span><span class="sxs-lookup"><span data-stu-id="ad95e-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="ad95e-133">Toisen siirtotyön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="ad95e-133">Start the second transfer job</span></span>
1. <span data-ttu-id="ad95e-134">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="ad95e-134">Click Start.</span></span>
    * <span data-ttu-id="ad95e-135">Nyt rivillä 5 olevan työn siirto alkaa.</span><span class="sxs-lookup"><span data-stu-id="ad95e-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="ad95e-136">Molempien siirtotöiden suorittaminen</span><span class="sxs-lookup"><span data-stu-id="ad95e-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="ad95e-137">Valitse luettelosta rivi 4.</span><span class="sxs-lookup"><span data-stu-id="ad95e-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="ad95e-138">Nyt on valittuna kaksi siirtotyötä rivillä 4 ja 5.</span><span class="sxs-lookup"><span data-stu-id="ad95e-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="ad95e-139">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="ad95e-139">Click Complete.</span></span>
    * <span data-ttu-id="ad95e-140">Molempien töiden siirto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="ad95e-140">This will complete the transfer of both jobs.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]