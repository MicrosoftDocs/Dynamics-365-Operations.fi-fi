---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 1 – Tietomallin valmisteleminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29c13e729223a98d7f45244c5a796bca6e3baaf3
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550830"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="9f69a-103">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 1 – Tietomallin valmisteleminen)</span><span class="sxs-lookup"><span data-stu-id="9f69a-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f69a-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="9f69a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9f69a-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="9f69a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9f69a-106">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="9f69a-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="9f69a-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="9f69a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="9f69a-108">Saat luettelon Microsoftin tarjoamista kokoonpanoista</span><span class="sxs-lookup"><span data-stu-id="9f69a-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="9f69a-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="9f69a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9f69a-110">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9f69a-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="9f69a-111">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="9f69a-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="9f69a-112">Valitse Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="9f69a-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="9f69a-113">-tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="9f69a-113">provider.</span></span>
3. <span data-ttu-id="9f69a-114">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="9f69a-114">Click Repositories.</span></span>
    * <span data-ttu-id="9f69a-115">Jos säilön tyyppi "Operatiiviset resurssit" on jo olemassa, ohita tämän alitehtävän loput vaiheet.</span><span class="sxs-lookup"><span data-stu-id="9f69a-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="9f69a-116">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="9f69a-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="9f69a-117">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="9f69a-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="9f69a-118">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="9f69a-118">Click Create repository.</span></span>
7. <span data-ttu-id="9f69a-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9f69a-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="9f69a-120">Hae Microsoftin toimittamat myyntilaskumallin konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="9f69a-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="9f69a-121">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="9f69a-121">Click Show filters.</span></span>
2. <span data-ttu-id="9f69a-122">Käytä seuraavia suodattimia: anna suodattimeksi "Operatiivisen resurssit" Nimi-kenttään ja käytä "alkaa"-suodatinoperaattoria; kirjoita suodatinarvoksi "" Kuvaus-kenttään ja käytä "alkaa"-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="9f69a-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="9f69a-123">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="9f69a-123">Click Show filters.</span></span>
4. <span data-ttu-id="9f69a-124">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="9f69a-124">Click Open.</span></span>
5. <span data-ttu-id="9f69a-125">Valitse puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="9f69a-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="9f69a-126">Valitse tuotavaksi mallikonfiguraatio "Myyntilaskumalli".</span><span class="sxs-lookup"><span data-stu-id="9f69a-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="9f69a-127">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="9f69a-127">Click Import.</span></span>
    * <span data-ttu-id="9f69a-128">Valitse Tuo valitulle kokoonpanoversiolle 1</span><span class="sxs-lookup"><span data-stu-id="9f69a-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="9f69a-129">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9f69a-129">Click Yes.</span></span>
8. <span data-ttu-id="9f69a-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9f69a-130">Close the page.</span></span>
9. <span data-ttu-id="9f69a-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9f69a-131">Close the page.</span></span>
10. <span data-ttu-id="9f69a-132">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="9f69a-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="9f69a-133">Valitse puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="9f69a-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="9f69a-134">Luo johdettu malli, joka tukee tiedostonhallinnan tiedostojen käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="9f69a-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="9f69a-135">Luot oman myyntilaskumallin konfiguraation johtamalla sen Microsoftin tarjoamasta konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="9f69a-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="9f69a-136">Tätä konfiguraatiota käytetään tiedostonhallinnan käytön toteuttamiseen ja tiedostojen saattamiseen tällä mallilla luotavien sähköisten asiakirjojen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="9f69a-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="9f69a-137">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="9f69a-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="9f69a-138">Kirjoita Uusi-kenttään "Derive from Name: Customer invoice model, Microsoft".</span><span class="sxs-lookup"><span data-stu-id="9f69a-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="9f69a-139">Syötä Nimi-kenttään "Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="9f69a-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="9f69a-140">Myyntilaskumalli (mukautettu)</span><span class="sxs-lookup"><span data-stu-id="9f69a-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="9f69a-141">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="9f69a-141">Click Create configuration.</span></span>

