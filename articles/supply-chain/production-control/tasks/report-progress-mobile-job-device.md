--- 
title: Edistymisen raportointi mobiililaitteella
description: "Tässä menettelyssä näytetään, miten tuotantotyö aloitetaan ja miten sen edistyminen raportoidaan laitteen rekisteröintilomakkeessa."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8096f703ecf2dc9e8ac33b3e93d698a2de7cf372
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="1265d-103">Edistymisen raportointi mobiililaitteella</span><span class="sxs-lookup"><span data-stu-id="1265d-103">Report progress on a mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1265d-104">Tässä menettelyssä näytetään, miten tuotantotyö aloitetaan ja miten sen edistyminen raportoidaan laitteen rekisteröintilomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="1265d-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="1265d-105">Tämän menettelyn suorittaminen edellyttää, että sinulla käyttäjätiliin liitetty järjestelmänvalvojan tai koneenkäyttäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="1265d-105">To be able to run this procedure you must have the System administrator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="1265d-106">Valitse Tuotannonhallinta > Tuotannonohjaus > Työkorttilaite.</span><span class="sxs-lookup"><span data-stu-id="1265d-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="1265d-107">Kirjoita työntekijän nimilapun WorkerTextField-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1265d-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="1265d-108">Kirjoita USMF-demotiedoissa 123 kohteelle Christina Portra.</span><span class="sxs-lookup"><span data-stu-id="1265d-108">In the USMF demo data type '123' for Christina Portra.</span></span>
3. <span data-ttu-id="1265d-109">Valitse Kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="1265d-109">Click Log in.</span></span>
4. <span data-ttu-id="1265d-110">Napsauta suodatinpainiketta.</span><span class="sxs-lookup"><span data-stu-id="1265d-110">Click the Filter button.</span></span>
5. <span data-ttu-id="1265d-111">Valitse Ota konfiguraatiosuodatin käyttöön -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="1265d-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="1265d-112">Jos määrität suodattimen, voit käyttää USMF-yrityksen tuotantoyksikköä 110.</span><span class="sxs-lookup"><span data-stu-id="1265d-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="1265d-113">Valitse Tuotantoyksikkö-kentässä resurssiryhmä, jonka tuotantotöitä työntekijä voi tehdä.</span><span class="sxs-lookup"><span data-stu-id="1265d-113">In the Production unit field, select the resource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="1265d-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1265d-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1265d-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1265d-115">Click OK.</span></span>
9. <span data-ttu-id="1265d-116">Valitse Aloita työ -painike.</span><span class="sxs-lookup"><span data-stu-id="1265d-116">Click the Start job button.</span></span>
10. <span data-ttu-id="1265d-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1265d-117">Click OK.</span></span>
11. <span data-ttu-id="1265d-118">Valitse Raportointi on meneillään -painike.</span><span class="sxs-lookup"><span data-stu-id="1265d-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="1265d-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1265d-119">Click OK.</span></span>
13. <span data-ttu-id="1265d-120">Valitse Seuraava työ -painike.</span><span class="sxs-lookup"><span data-stu-id="1265d-120">Click the Next job button.</span></span>
14. <span data-ttu-id="1265d-121">Valitsemalla Määritetty näkyviin tulee yhteenveto kaikista tuotantotöiden painikkeista.</span><span class="sxs-lookup"><span data-stu-id="1265d-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="1265d-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1265d-122">Close the page.</span></span>
16. <span data-ttu-id="1265d-123">Napsauta Tauko-painiketta.</span><span class="sxs-lookup"><span data-stu-id="1265d-123">Click the Break button.</span></span>
17. <span data-ttu-id="1265d-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1265d-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="1265d-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1265d-125">Click OK.</span></span>
19. <span data-ttu-id="1265d-126">Napsauta Työsuhteen päättyminen -painiketta.</span><span class="sxs-lookup"><span data-stu-id="1265d-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="1265d-127">Valitse uloskirjautuminen.</span><span class="sxs-lookup"><span data-stu-id="1265d-127">Select to log out.</span></span>
21. <span data-ttu-id="1265d-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1265d-128">Click OK.</span></span>
22. <span data-ttu-id="1265d-129">Kirjaudu uudelleen sisään WorkerTextField-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1265d-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="1265d-130">Voit valita työntekijän 123 USMF-demotiedoissa.</span><span class="sxs-lookup"><span data-stu-id="1265d-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="1265d-131">Valitse Kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="1265d-131">Click Log in.</span></span>
24. <span data-ttu-id="1265d-132">Valitse Lopeta tauko.</span><span class="sxs-lookup"><span data-stu-id="1265d-132">Click Stop break.</span></span>
25. <span data-ttu-id="1265d-133">Napsauta Toiminto-painiketta.</span><span class="sxs-lookup"><span data-stu-id="1265d-133">Click the Activity button.</span></span>
26. <span data-ttu-id="1265d-134">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="1265d-134">Click Cancel.</span></span>
27. <span data-ttu-id="1265d-135">Napsauta Työsuhteen päättyminen -painiketta.</span><span class="sxs-lookup"><span data-stu-id="1265d-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="1265d-136">Valitse poistuminen.</span><span class="sxs-lookup"><span data-stu-id="1265d-136">Select to clock out.</span></span>
29. <span data-ttu-id="1265d-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1265d-137">Click OK.</span></span>
30. <span data-ttu-id="1265d-138">Valitse syy, miksi poistut etuajassa.</span><span class="sxs-lookup"><span data-stu-id="1265d-138">Select a reason why you are clocking out early.</span></span>


