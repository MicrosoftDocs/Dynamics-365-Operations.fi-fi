--- 
title: "Tietomallin valmistelu tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96195003c209c56c7ea4cbfec2f3543eb68453ff
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="842da-103">Tietomallin valmistelu tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="842da-103">Prepare data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="842da-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="842da-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="842da-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="842da-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="842da-106">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="842da-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="842da-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="842da-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="842da-108">Saat luettelon Microsoftin tarjoamista kokoonpanoista</span><span class="sxs-lookup"><span data-stu-id="842da-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="842da-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="842da-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="842da-110">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="842da-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="842da-111">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="842da-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="842da-112">Valitse Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="842da-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="842da-113">-tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="842da-113">provider.</span></span>
3. <span data-ttu-id="842da-114">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="842da-114">Click Repositories.</span></span>
    * <span data-ttu-id="842da-115">Jos säilön tyyppi "Operatiiviset resurssit" on jo olemassa, ohita tämän alitehtävän loput vaiheet.</span><span class="sxs-lookup"><span data-stu-id="842da-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="842da-116">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="842da-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="842da-117">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="842da-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="842da-118">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="842da-118">Click Create repository.</span></span>
7. <span data-ttu-id="842da-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="842da-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="842da-120">Hae Microsoftin toimittamat myyntilaskumallin konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="842da-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="842da-121">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="842da-121">Click Show filters.</span></span>
2. <span data-ttu-id="842da-122">Käytä seuraavia suodattimia: anna suodattimeksi "Operatiivisen resurssit" Nimi-kenttään ja käytä "alkaa"-suodatinoperaattoria; kirjoita suodatinarvoksi "" Kuvaus-kenttään ja käytä "alkaa"-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="842da-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="842da-123">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="842da-123">Click Show filters.</span></span>
4. <span data-ttu-id="842da-124">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="842da-124">Click Open.</span></span>
5. <span data-ttu-id="842da-125">Valitse puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="842da-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="842da-126">Valitse tuotavaksi mallikonfiguraatio "Myyntilaskumalli".</span><span class="sxs-lookup"><span data-stu-id="842da-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="842da-127">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="842da-127">Click Import.</span></span>
    * <span data-ttu-id="842da-128">Valitse Tuo valitulle kokoonpanoversiolle 1</span><span class="sxs-lookup"><span data-stu-id="842da-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="842da-129">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="842da-129">Click Yes.</span></span>
8. <span data-ttu-id="842da-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="842da-130">Close the page.</span></span>
9. <span data-ttu-id="842da-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="842da-131">Close the page.</span></span>
10. <span data-ttu-id="842da-132">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="842da-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="842da-133">Valitse puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="842da-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="842da-134">Luo johdettu malli, joka tukee tiedostonhallinnan tiedostojen käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="842da-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="842da-135">Luot oman myyntilaskumallin konfiguraation johtamalla sen Microsoftin tarjoamasta konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="842da-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="842da-136">Tätä konfiguraatiota käytetään tiedostonhallinnan käytön toteuttamiseen ja tiedostojen saattamiseen tällä mallilla luotavien sähköisten asiakirjojen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="842da-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="842da-137">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="842da-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="842da-138">Kirjoita Uusi-kenttään "Derive from Name: Customer invoice model, Microsoft".</span><span class="sxs-lookup"><span data-stu-id="842da-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="842da-139">Syötä Nimi-kenttään "Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="842da-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="842da-140">Myyntilaskumalli (mukautettu)</span><span class="sxs-lookup"><span data-stu-id="842da-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="842da-141">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="842da-141">Click Create configuration.</span></span>


