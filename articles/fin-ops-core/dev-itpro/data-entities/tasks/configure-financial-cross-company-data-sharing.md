---
title: Määritä yritysten välinen taloustietojen jakaminen
description: Tässä menettelyssä kuvataan yritysten välisen tietojenjaon määrittäminen, käyttöönotto, tarkistaminen, sekä siihen liittyvien ristiriitojen ratkaisu.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35ec8fc809841c0830224646fb57b0e4e4d40ef4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752289"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="e7e36-103">Määritä yritysten välinen taloustietojen jakaminen</span><span class="sxs-lookup"><span data-stu-id="e7e36-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7e36-104">Tässä menettelyssä kuvataan yritysten välisen tietojenjaon määrittäminen, käyttöönotto, tarkistaminen, sekä siihen liittyvien ristiriitojen ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="e7e36-105">Se käyttää USMF-yritystä ja kirjanpitotietojen jakamismallia.</span><span class="sxs-lookup"><span data-stu-id="e7e36-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="e7e36-106">Tämä tehtäväopas vaatii Dynamics AX -ympäristön version 7.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="e7e36-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="e7e36-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Työtilat > Tietojen hallinta**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="e7e36-108">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-108">Click **Import**.</span></span>
3. <span data-ttu-id="e7e36-109">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e7e36-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e7e36-110">Valitse **Lähdetietojen muoto** -kentässä pakkaustyyppi.</span><span class="sxs-lookup"><span data-stu-id="e7e36-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="e7e36-111">Valitse **Lataa palvelimeen**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-111">Click **Upload**.</span></span> <span data-ttu-id="e7e36-112">Siirry sijaintiin, jossa kirjanpitotietojen jakamismallin pakettitiedosto on ja valitse tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e7e36-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="e7e36-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-113">Click **Save**.</span></span>
6. <span data-ttu-id="e7e36-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e7e36-114">In the list, mark the selected row.</span></span> <span data-ttu-id="e7e36-115">Valitse juuri luotu tietojen jakamiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="e7e36-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="e7e36-116">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-116">Click **Import**.</span></span>
8. <span data-ttu-id="e7e36-117">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-117">Click **Close**.</span></span>
9. <span data-ttu-id="e7e36-118">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-118">Refresh the page.</span></span>
10. <span data-ttu-id="e7e36-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-119">Close the page.</span></span>
11. <span data-ttu-id="e7e36-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-120">Close the page.</span></span>
12. <span data-ttu-id="e7e36-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-121">Close the page.</span></span>
13. <span data-ttu-id="e7e36-122">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Asetukset > Määritä yritysten välinen tietojen jakaminen**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="e7e36-123">Etsi ja valitse luettelossa **Maksupäivät**</span><span class="sxs-lookup"><span data-stu-id="e7e36-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="e7e36-124">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-124">Click **Add**.</span></span>
16. <span data-ttu-id="e7e36-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e7e36-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="e7e36-126">Kirjoita **Yritys**-kenttään arvoksi USSI.</span><span class="sxs-lookup"><span data-stu-id="e7e36-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="e7e36-127">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-127">Click **Add**.</span></span>
19. <span data-ttu-id="e7e36-128">Kirjoita **Yritys**-kentän arvoksi USMF.</span><span class="sxs-lookup"><span data-stu-id="e7e36-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="e7e36-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-129">Click **Save**.</span></span>
21. <span data-ttu-id="e7e36-130">Valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-130">Click **Enable**.</span></span>
22. <span data-ttu-id="e7e36-131">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-131">Click **Yes**.</span></span>
23. <span data-ttu-id="e7e36-132">Valitse **Etsi jakamisongelmia**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="e7e36-133">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-133">Click **Yes**.</span></span>
25. <span data-ttu-id="e7e36-134">Valitse **Päivitä kentän arvo**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="e7e36-135">Valitse **Käytä arvoa yrityksestä 1**.</span><span class="sxs-lookup"><span data-stu-id="e7e36-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="e7e36-136">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-136">Refresh the page.</span></span>
28. <span data-ttu-id="e7e36-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e36-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]