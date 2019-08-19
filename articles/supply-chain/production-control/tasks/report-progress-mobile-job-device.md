---
title: Edistymisen raportointi mobiililaitteella
description: Tässä menettelyssä näytetään, miten tuotantotyö aloitetaan ja miten sen edistyminen raportoidaan laitteen rekisteröintilomakkeessa.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 199ccc03cee1f6328ff42063a480146b0a361711
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843574"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="c9fff-103">Edistymisen raportointi mobiililaitteella</span><span class="sxs-lookup"><span data-stu-id="c9fff-103">Report progress on a mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9fff-104">Tässä menettelyssä näytetään, miten tuotantotyö aloitetaan ja miten sen edistyminen raportoidaan laitteen rekisteröintilomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="c9fff-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="c9fff-105">Tämän menettelyn suorittaminen edellyttää, että sinulla käyttäjätiliin liitetty järjestelmänvalvojan tai koneenkäyttäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="c9fff-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="c9fff-106">Valitse Tuotannonhallinta > Tuotannonohjaus > Työkorttilaite.</span><span class="sxs-lookup"><span data-stu-id="c9fff-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="c9fff-107">Kirjoita työntekijän nimilapun WorkerTextField-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c9fff-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="c9fff-108">Kirjoita USMF-demotiedoissa 123 kohteelle Christina Portra.</span><span class="sxs-lookup"><span data-stu-id="c9fff-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="c9fff-109">Valitse Kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="c9fff-109">Click Log in.</span></span>
4. <span data-ttu-id="c9fff-110">Napsauta suodatinpainiketta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-110">Click the Filter button.</span></span>
5. <span data-ttu-id="c9fff-111">Valitse Ota konfiguraatiosuodatin käyttöön -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="c9fff-112">Jos määrität suodattimen, voit käyttää USMF-yrityksen tuotantoyksikköä 110.</span><span class="sxs-lookup"><span data-stu-id="c9fff-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="c9fff-113">Valitse Tuotantoyksikkö-kentässä resurssiryhmä, jonka tuotantotöitä työntekijä voi tehdä.</span><span class="sxs-lookup"><span data-stu-id="c9fff-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="c9fff-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c9fff-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c9fff-115">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9fff-115">Click OK.</span></span>
9. <span data-ttu-id="c9fff-116">Valitse Aloita työ -painike.</span><span class="sxs-lookup"><span data-stu-id="c9fff-116">Click the Start job button.</span></span>
10. <span data-ttu-id="c9fff-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9fff-117">Click OK.</span></span>
11. <span data-ttu-id="c9fff-118">Valitse Raportointi on meneillään -painike.</span><span class="sxs-lookup"><span data-stu-id="c9fff-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="c9fff-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9fff-119">Click OK.</span></span>
13. <span data-ttu-id="c9fff-120">Valitse Seuraava työ -painike.</span><span class="sxs-lookup"><span data-stu-id="c9fff-120">Click the Next job button.</span></span>
14. <span data-ttu-id="c9fff-121">Valitsemalla Määritetty näkyviin tulee yhteenveto kaikista tuotantotöiden painikkeista.</span><span class="sxs-lookup"><span data-stu-id="c9fff-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="c9fff-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9fff-122">Close the page.</span></span>
16. <span data-ttu-id="c9fff-123">Napsauta Tauko-painiketta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-123">Click the Break button.</span></span>
17. <span data-ttu-id="c9fff-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c9fff-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="c9fff-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9fff-125">Click OK.</span></span>
19. <span data-ttu-id="c9fff-126">Napsauta Työsuhteen päättyminen -painiketta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="c9fff-127">Valitse uloskirjautuminen.</span><span class="sxs-lookup"><span data-stu-id="c9fff-127">Select to log out.</span></span>
21. <span data-ttu-id="c9fff-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9fff-128">Click OK.</span></span>
22. <span data-ttu-id="c9fff-129">Kirjaudu uudelleen sisään WorkerTextField-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c9fff-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="c9fff-130">Voit valita työntekijän 123 USMF-demotiedoissa.</span><span class="sxs-lookup"><span data-stu-id="c9fff-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="c9fff-131">Valitse Kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="c9fff-131">Click Log in.</span></span>
24. <span data-ttu-id="c9fff-132">Valitse Lopeta tauko.</span><span class="sxs-lookup"><span data-stu-id="c9fff-132">Click Stop break.</span></span>
25. <span data-ttu-id="c9fff-133">Napsauta Toiminto-painiketta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-133">Click the Activity button.</span></span>
26. <span data-ttu-id="c9fff-134">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-134">Click Cancel.</span></span>
27. <span data-ttu-id="c9fff-135">Napsauta Työsuhteen päättyminen -painiketta.</span><span class="sxs-lookup"><span data-stu-id="c9fff-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="c9fff-136">Valitse poistuminen.</span><span class="sxs-lookup"><span data-stu-id="c9fff-136">Select to clock out.</span></span>
29. <span data-ttu-id="c9fff-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9fff-137">Click OK.</span></span>
30. <span data-ttu-id="c9fff-138">Valitse syy, miksi poistut etuajassa.</span><span class="sxs-lookup"><span data-stu-id="c9fff-138">Select a reason why you are clocking out early.</span></span>

