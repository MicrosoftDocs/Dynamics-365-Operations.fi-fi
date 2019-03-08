---
title: Luo mallin määrityksen konfiguraatioita sähköistä raportointia (ER) varten
description: Tämän toiminnon avulla voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "357171"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="dbfac-103">Luo mallin määrityksen konfiguraatioita sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="dbfac-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbfac-104">Tämän toiminnon avulla voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa.</span><span class="sxs-lookup"><span data-stu-id="dbfac-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="dbfac-105">Tässä menettelyssä luodaan konfiguraatio malliyritykselle Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="dbfac-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="dbfac-106">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="dbfac-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="dbfac-107">Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="dbfac-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="dbfac-108">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="dbfac-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="dbfac-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="dbfac-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="dbfac-110">Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="dbfac-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="dbfac-111">Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="dbfac-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="dbfac-112">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="dbfac-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="dbfac-113">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="dbfac-113">Click Show filters.</span></span>
4. <span data-ttu-id="dbfac-114">Syötä Nimi-kenttään suodattimen arvo Intrastat ja käytä alkaa-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="dbfac-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="dbfac-115">Käytä tätä suodatinta, kun haluat löytää Intrastat-tietomallin konfiguraation.</span><span class="sxs-lookup"><span data-stu-id="dbfac-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="dbfac-116">Tämä malli voi jo olla konfiguraatioiden puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="dbfac-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="dbfac-117">Jos se on puurakenteessa, ohita seuraava alitehtävä.</span><span class="sxs-lookup"><span data-stu-id="dbfac-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="dbfac-118">Hae Microsoftin Intrastat-mallikonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="dbfac-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="dbfac-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dbfac-119">Close the page.</span></span>
2. <span data-ttu-id="dbfac-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dbfac-120">Close the page.</span></span>
3. <span data-ttu-id="dbfac-121">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="dbfac-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="dbfac-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="dbfac-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dbfac-123">Valitse Microsoft-toimittaja-ruutu.</span><span class="sxs-lookup"><span data-stu-id="dbfac-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="dbfac-124">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="dbfac-124">Click Repositories.</span></span>
    * <span data-ttu-id="dbfac-125">Valitse Microsoft-toimittaja-ruudussa Säilöt.</span><span class="sxs-lookup"><span data-stu-id="dbfac-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="dbfac-126">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="dbfac-126">Click Show filters.</span></span>
7. <span data-ttu-id="dbfac-127">Syötä Tyypin nimi -kenttään suodattimen arvo resources ja käytä sisältää-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="dbfac-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="dbfac-128">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="dbfac-128">Click Open.</span></span>
9. <span data-ttu-id="dbfac-129">Valitse puussa 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="dbfac-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="dbfac-130">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="dbfac-130">Click Import.</span></span>
11. <span data-ttu-id="dbfac-131">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="dbfac-131">Click Yes.</span></span>
    * <span data-ttu-id="dbfac-132">Toit ER-muotokonfiguraation, joka tietomallin. Tämän tietomallin avulla voit tutustua uuteen ER-toimintoon.</span><span class="sxs-lookup"><span data-stu-id="dbfac-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="dbfac-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dbfac-133">Close the page.</span></span>
13. <span data-ttu-id="dbfac-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dbfac-134">Close the page.</span></span>
14. <span data-ttu-id="dbfac-135">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="dbfac-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="dbfac-136">Uuden mallin yhdistämismäärityksen konfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="dbfac-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="dbfac-137">Valitse puussa 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="dbfac-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="dbfac-138">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="dbfac-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="dbfac-139">Syötä Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Intrastat.</span><span class="sxs-lookup"><span data-stu-id="dbfac-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="dbfac-140">Syötä Nimi-kenttään Intrastat-esimerkkiyhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="dbfac-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="dbfac-141">Intrastat-esimerkkiyhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="dbfac-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="dbfac-142">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="dbfac-142">Click Create configuration.</span></span>

