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
ms.openlocfilehash: c6ba23af5f7eb517cc58994e54e918b2a305da17
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142157"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="c79c1-103">Luo mallin määrityksen konfiguraatioita sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="c79c1-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c79c1-104">Tämän toiminnon avulla voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa.</span><span class="sxs-lookup"><span data-stu-id="c79c1-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="c79c1-105">Tässä menettelyssä luodaan konfiguraatio malliyritykselle Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c79c1-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="c79c1-106">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="c79c1-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="c79c1-107">Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="c79c1-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="c79c1-108">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="c79c1-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="c79c1-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="c79c1-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c79c1-110">Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="c79c1-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c79c1-111">Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c79c1-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="c79c1-112">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="c79c1-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c79c1-113">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="c79c1-113">Click Show filters.</span></span>
4. <span data-ttu-id="c79c1-114">Syötä Nimi-kenttään suodattimen arvo Intrastat ja käytä alkaa-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="c79c1-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="c79c1-115">Käytä tätä suodatinta, kun haluat löytää Intrastat-tietomallin konfiguraation.</span><span class="sxs-lookup"><span data-stu-id="c79c1-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="c79c1-116">Tämä malli voi jo olla konfiguraatioiden puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="c79c1-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="c79c1-117">Jos se on puurakenteessa, ohita seuraava alitehtävä.</span><span class="sxs-lookup"><span data-stu-id="c79c1-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="c79c1-118">Hae Microsoftin Intrastat-mallikonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="c79c1-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="c79c1-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c79c1-119">Close the page.</span></span>
2. <span data-ttu-id="c79c1-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c79c1-120">Close the page.</span></span>
3. <span data-ttu-id="c79c1-121">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="c79c1-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="c79c1-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c79c1-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c79c1-123">Valitse Microsoft-toimittaja-ruutu.</span><span class="sxs-lookup"><span data-stu-id="c79c1-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="c79c1-124">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="c79c1-124">Click Repositories.</span></span>
    * <span data-ttu-id="c79c1-125">Valitse Microsoft-toimittaja-ruudussa Säilöt.</span><span class="sxs-lookup"><span data-stu-id="c79c1-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="c79c1-126">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="c79c1-126">Click Show filters.</span></span>
7. <span data-ttu-id="c79c1-127">Syötä Tyypin nimi -kenttään suodattimen arvo resources ja käytä sisältää-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="c79c1-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="c79c1-128">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="c79c1-128">Click Open.</span></span>
9. <span data-ttu-id="c79c1-129">Valitse puussa 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="c79c1-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="c79c1-130">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="c79c1-130">Click Import.</span></span>
11. <span data-ttu-id="c79c1-131">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c79c1-131">Click Yes.</span></span>
    * <span data-ttu-id="c79c1-132">Toit ER-muotokonfiguraation, joka tietomallin. Tämän tietomallin avulla voit tutustua uuteen ER-toimintoon.</span><span class="sxs-lookup"><span data-stu-id="c79c1-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="c79c1-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c79c1-133">Close the page.</span></span>
13. <span data-ttu-id="c79c1-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c79c1-134">Close the page.</span></span>
14. <span data-ttu-id="c79c1-135">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="c79c1-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="c79c1-136">Uuden mallin yhdistämismäärityksen konfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="c79c1-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="c79c1-137">Valitse puussa 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="c79c1-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="c79c1-138">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="c79c1-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="c79c1-139">Syötä Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c79c1-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="c79c1-140">Syötä Nimi-kenttään Intrastat-esimerkkiyhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="c79c1-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="c79c1-141">Intrastat-esimerkkiyhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="c79c1-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="c79c1-142">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="c79c1-142">Click Create configuration.</span></span>

