---
title: Määritä yritysten välinen taloustietojen jakaminen
description: Tässä menettelyssä kuvataan yritysten välisen tietojenjaon määrittäminen, käyttöönotto, tarkistaminen, sekä siihen liittyvien ristiriitojen ratkaisu.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "357838"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="2e430-103">Määritä yritysten välinen taloustietojen jakaminen</span><span class="sxs-lookup"><span data-stu-id="2e430-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e430-104">Tässä menettelyssä kuvataan yritysten välisen tietojenjaon määrittäminen, käyttöönotto, tarkistaminen, sekä siihen liittyvien ristiriitojen ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="2e430-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="2e430-105">Se käyttää USMF-yritystä ja kirjanpitotietojen jakamismallia.</span><span class="sxs-lookup"><span data-stu-id="2e430-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="2e430-106">Tämä tehtäväopas vaatii Dynamics AX -ympäristön version 7.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="2e430-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="2e430-107">Valitse Järjestelmänhallinta > Työtilat > Tietojen hallinta.</span><span class="sxs-lookup"><span data-stu-id="2e430-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="2e430-108">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="2e430-108">Click Import.</span></span>
3. <span data-ttu-id="2e430-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2e430-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2e430-110">Anna paketin tyyppi Lähdetietojen muoto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2e430-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="2e430-111">Valitse Lataa palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="2e430-111">Click Upload.</span></span> <span data-ttu-id="2e430-112">Siirry sijaintiin, jossa kirjanpitotietojen jakamismallin pakettitiedosto on ja valitse tiedosto.</span><span class="sxs-lookup"><span data-stu-id="2e430-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="2e430-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2e430-113">Click Save.</span></span>
6. <span data-ttu-id="2e430-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2e430-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2e430-115">Valitse juuri luotu tietojen jakamiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="2e430-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="2e430-116">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="2e430-116">Click Import.</span></span>
8. <span data-ttu-id="2e430-117">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="2e430-117">Click Close.</span></span>
9. <span data-ttu-id="2e430-118">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="2e430-118">Refresh the page.</span></span>
10. <span data-ttu-id="2e430-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2e430-119">Close the page.</span></span>
11. <span data-ttu-id="2e430-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2e430-120">Close the page.</span></span>
12. <span data-ttu-id="2e430-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2e430-121">Close the page.</span></span>
13. <span data-ttu-id="2e430-122">Valitse Järjestelmänhallinta > Asetukset > Määritä yritysten välinen tietojen jakaminen.</span><span class="sxs-lookup"><span data-stu-id="2e430-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="2e430-123">Etsi ja valitse luettelosta Maksupäivät.</span><span class="sxs-lookup"><span data-stu-id="2e430-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="2e430-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="2e430-124">Click Add.</span></span>
16. <span data-ttu-id="2e430-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2e430-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="2e430-126">Kirjoita Yritys-kenttän arvoksi "USSI".</span><span class="sxs-lookup"><span data-stu-id="2e430-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="2e430-127">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="2e430-127">Click Add.</span></span>
19. <span data-ttu-id="2e430-128">Kirjoita Yritys-kenttän arvoksi "USMF".</span><span class="sxs-lookup"><span data-stu-id="2e430-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="2e430-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2e430-129">Click Save.</span></span>
21. <span data-ttu-id="2e430-130">Napsauta Ota käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2e430-130">Click Enable.</span></span>
22. <span data-ttu-id="2e430-131">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2e430-131">Click Yes.</span></span>
23. <span data-ttu-id="2e430-132">Napsauta Etsi jakamisongelmia.</span><span class="sxs-lookup"><span data-stu-id="2e430-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="2e430-133">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2e430-133">Click Yes.</span></span>
25. <span data-ttu-id="2e430-134">Napsauta Päivitä kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="2e430-134">Click Update field value.</span></span>
26. <span data-ttu-id="2e430-135">Napsauta Käytä arvoa yrityksestä 1.</span><span class="sxs-lookup"><span data-stu-id="2e430-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="2e430-136">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="2e430-136">Refresh the page.</span></span>
28. <span data-ttu-id="2e430-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2e430-137">Close the page.</span></span>

