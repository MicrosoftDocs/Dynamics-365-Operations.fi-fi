--- 
title: "Luo ja liitä laiteasema"
description: "Tässä menettelyssä kerrotaan, miten uusi laiteasema luodaan."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2720ba4060252ef6d6d27e310619ec5639f020ca
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="7e747-103">Luo ja liitä laiteasema</span><span class="sxs-lookup"><span data-stu-id="7e747-103">Create and associate a hardware station</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7e747-104">Tässä menettelyssä kerrotaan, miten uusi laiteasema luodaan.</span><span class="sxs-lookup"><span data-stu-id="7e747-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="7e747-105">Luodaan uusi laiteprofiili ja käytetään sitä uusien laiteasemien lisäämisessä ennalta määritettyyn myymälään (kanava).</span><span class="sxs-lookup"><span data-stu-id="7e747-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="7e747-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="7e747-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7e747-107">Valitse Commerce-perustiedot > Kanavat > ..</span><span class="sxs-lookup"><span data-stu-id="7e747-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="7e747-108">> ..</span><span class="sxs-lookup"><span data-stu-id="7e747-108">> ..</span></span> <span data-ttu-id="7e747-109">> ..</span><span class="sxs-lookup"><span data-stu-id="7e747-109">> ..</span></span> <span data-ttu-id="7e747-110">> Laiteaseman profiilit.</span><span class="sxs-lookup"><span data-stu-id="7e747-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="7e747-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7e747-111">Click New.</span></span>
3. <span data-ttu-id="7e747-112">Syötä Laiteaseman tunnus -kenttään TestHWProfile.</span><span class="sxs-lookup"><span data-stu-id="7e747-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="7e747-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7e747-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7e747-114">Lisää Portin numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7e747-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="7e747-115">Avaa haku valitsemalla Laiteprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7e747-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7e747-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7e747-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7e747-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7e747-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7e747-118">Avaa haku valitsemalla Paketin nimi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7e747-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="7e747-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7e747-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7e747-120">Tämä on vakiopaketti, joka sisältyy uuteen ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="7e747-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="7e747-121">Versionumero voi vaihdella.</span><span class="sxs-lookup"><span data-stu-id="7e747-121">The version number may vary.</span></span>  
11. <span data-ttu-id="7e747-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7e747-122">Click Save.</span></span>
12. <span data-ttu-id="7e747-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7e747-123">Close the page.</span></span>
13. <span data-ttu-id="7e747-124">Valitse Vähittäismyynti ja kauppa > Kanavat > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="7e747-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="7e747-125">Valitse luettelosta rivi 17.</span><span class="sxs-lookup"><span data-stu-id="7e747-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="7e747-126">Jos käytössä on esittelytietojen USRT-yritys, tämä on Houstonin myymälä.</span><span class="sxs-lookup"><span data-stu-id="7e747-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="7e747-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7e747-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="7e747-128">Ota käyttöön Laiteasemat-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="7e747-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="7e747-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="7e747-129">Click Add.</span></span>
18. <span data-ttu-id="7e747-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7e747-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="7e747-131">Avaa haku valitsemalla Profiilin tunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7e747-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="7e747-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7e747-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7e747-133">Tämän on oltava edellisissä vaiheissa luotu uusi laiteaseman profiili.</span><span class="sxs-lookup"><span data-stu-id="7e747-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="7e747-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7e747-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="7e747-135">Kirjoita arvo Isännän nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7e747-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="7e747-136">Syötä EFT-päätteen tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7e747-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="7e747-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7e747-137">Click Save.</span></span>


