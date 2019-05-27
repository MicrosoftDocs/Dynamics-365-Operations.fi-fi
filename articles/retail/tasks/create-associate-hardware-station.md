---
title: Luo ja liitä laiteasema
description: Tässä menettelyssä kerrotaan, miten uusi laiteasema luodaan.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80df4fa663d208e28f5c9b031b6610d29286171c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548390"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="37c48-103">Luo ja liitä laiteasema</span><span class="sxs-lookup"><span data-stu-id="37c48-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="37c48-104">Tässä menettelyssä kerrotaan, miten uusi laiteasema luodaan.</span><span class="sxs-lookup"><span data-stu-id="37c48-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="37c48-105">Luodaan uusi laiteprofiili ja käytetään sitä uusien laiteasemien lisäämisessä ennalta määritettyyn myymälään (kanava).</span><span class="sxs-lookup"><span data-stu-id="37c48-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="37c48-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="37c48-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="37c48-107">Valitse Commerce-perustiedot > Kanavat > ..</span><span class="sxs-lookup"><span data-stu-id="37c48-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="37c48-108">> ..</span><span class="sxs-lookup"><span data-stu-id="37c48-108">> ..</span></span> <span data-ttu-id="37c48-109">> ..</span><span class="sxs-lookup"><span data-stu-id="37c48-109">> ..</span></span> <span data-ttu-id="37c48-110">> Laiteaseman profiilit.</span><span class="sxs-lookup"><span data-stu-id="37c48-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="37c48-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="37c48-111">Click New.</span></span>
3. <span data-ttu-id="37c48-112">Syötä Laiteaseman tunnus -kenttään TestHWProfile.</span><span class="sxs-lookup"><span data-stu-id="37c48-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="37c48-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="37c48-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="37c48-114">Lisää Portin numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="37c48-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="37c48-115">Avaa haku valitsemalla Laiteprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="37c48-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="37c48-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="37c48-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="37c48-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="37c48-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="37c48-118">Avaa haku valitsemalla Paketin nimi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="37c48-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="37c48-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="37c48-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="37c48-120">Tämä on vakiopaketti, joka sisältyy uuteen ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="37c48-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="37c48-121">Versionumero voi vaihdella.</span><span class="sxs-lookup"><span data-stu-id="37c48-121">The version number may vary.</span></span>  
11. <span data-ttu-id="37c48-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="37c48-122">Click Save.</span></span>
12. <span data-ttu-id="37c48-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="37c48-123">Close the page.</span></span>
13. <span data-ttu-id="37c48-124">Valitse Vähittäismyynti ja kauppa > Kanavat > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="37c48-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="37c48-125">Valitse luettelosta rivi 17.</span><span class="sxs-lookup"><span data-stu-id="37c48-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="37c48-126">Jos käytössä on esittelytietojen USRT-yritys, tämä on Houstonin myymälä.</span><span class="sxs-lookup"><span data-stu-id="37c48-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="37c48-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="37c48-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="37c48-128">Ota käyttöön Laiteasemat-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="37c48-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="37c48-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="37c48-129">Click Add.</span></span>
18. <span data-ttu-id="37c48-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="37c48-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="37c48-131">Avaa haku valitsemalla Profiilin tunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="37c48-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="37c48-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="37c48-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="37c48-133">Tämän on oltava edellisissä vaiheissa luotu uusi laiteaseman profiili.</span><span class="sxs-lookup"><span data-stu-id="37c48-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="37c48-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="37c48-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="37c48-135">Kirjoita arvo Isännän nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="37c48-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="37c48-136">Syötä EFT-päätteen tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="37c48-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="37c48-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="37c48-137">Click Save.</span></span>

