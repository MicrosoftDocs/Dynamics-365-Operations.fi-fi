---
title: Määritä yritysten välinen taloustietojen jakaminen
description: Tässä menettelyssä kuvataan yritysten välisen tietojenjaon määrittäminen, käyttöönotto, tarkistaminen, sekä siihen liittyvien ristiriitojen ratkaisu.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184367"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="6b0dc-103">Määritä yritysten välinen taloustietojen jakaminen</span><span class="sxs-lookup"><span data-stu-id="6b0dc-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b0dc-104">Tässä menettelyssä kuvataan yritysten välisen tietojenjaon määrittäminen, käyttöönotto, tarkistaminen, sekä siihen liittyvien ristiriitojen ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="6b0dc-105">Se käyttää USMF-yritystä ja kirjanpitotietojen jakamismallia.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="6b0dc-106">Tämä tehtäväopas vaatii Dynamics AX -ympäristön version 7.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="6b0dc-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Työtilat > Tietojen hallinta**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="6b0dc-108">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-108">Click **Import**.</span></span>
3. <span data-ttu-id="6b0dc-109">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="6b0dc-110">Valitse **Lähdetietojen muoto** -kentässä pakkaustyyppi.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="6b0dc-111">Valitse **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-111">Click **Upload**.</span></span> <span data-ttu-id="6b0dc-112">Siirry sijaintiin, jossa kirjanpitotietojen jakamismallin pakettitiedosto on ja valitse tiedosto.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="6b0dc-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-113">Click **Save**.</span></span>
6. <span data-ttu-id="6b0dc-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-114">In the list, mark the selected row.</span></span> <span data-ttu-id="6b0dc-115">Valitse juuri luotu tietojen jakamiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="6b0dc-116">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-116">Click **Import**.</span></span>
8. <span data-ttu-id="6b0dc-117">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-117">Click **Close**.</span></span>
9. <span data-ttu-id="6b0dc-118">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-118">Refresh the page.</span></span>
10. <span data-ttu-id="6b0dc-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-119">Close the page.</span></span>
11. <span data-ttu-id="6b0dc-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-120">Close the page.</span></span>
12. <span data-ttu-id="6b0dc-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-121">Close the page.</span></span>
13. <span data-ttu-id="6b0dc-122">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Asetukset > Määritä yritysten välinen tietojen jakaminen**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="6b0dc-123">Etsi ja valitse luettelossa **Maksupäivät**</span><span class="sxs-lookup"><span data-stu-id="6b0dc-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="6b0dc-124">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-124">Click **Add**.</span></span>
16. <span data-ttu-id="6b0dc-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="6b0dc-126">Kirjoita **Yritys**-kenttään arvoksi USSI.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="6b0dc-127">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-127">Click **Add**.</span></span>
19. <span data-ttu-id="6b0dc-128">Kirjoita **Yritys**-kentän arvoksi USMF.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="6b0dc-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-129">Click **Save**.</span></span>
21. <span data-ttu-id="6b0dc-130">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-130">Click **Enable**.</span></span>
22. <span data-ttu-id="6b0dc-131">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-131">Click **Yes**.</span></span>
23. <span data-ttu-id="6b0dc-132">Valitse **Etsi jakamisongelmia**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="6b0dc-133">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-133">Click **Yes**.</span></span>
25. <span data-ttu-id="6b0dc-134">Valitse **Päivitä kentän arvo**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="6b0dc-135">Valitse **Käytä arvoa yrityksestä 1**.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="6b0dc-136">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-136">Refresh the page.</span></span>
28. <span data-ttu-id="6b0dc-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6b0dc-137">Close the page.</span></span>

