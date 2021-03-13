---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 1 – Tietomallin valmisteleminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja (liitteitä) ER-tuotoksissa. (Osa 1)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bff518c60f0f36bdc88245d79bd82f0c4d0599ed
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092638"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="4010c-104">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 1 – Tietomallin valmisteleminen)</span><span class="sxs-lookup"><span data-stu-id="4010c-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4010c-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="4010c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4010c-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="4010c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4010c-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="4010c-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="4010c-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="4010c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="4010c-109">Saat luettelon Microsoftin tarjoamista kokoonpanoista</span><span class="sxs-lookup"><span data-stu-id="4010c-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="4010c-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="4010c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="4010c-111">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4010c-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="4010c-112">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="4010c-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="4010c-113">Valitse Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4010c-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="4010c-114">-tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="4010c-114">provider.</span></span>
3. <span data-ttu-id="4010c-115">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="4010c-115">Click Repositories.</span></span>

    <span data-ttu-id="4010c-116">Jos säilön tyyppi "Operatiiviset resurssit" on jo olemassa, ohita tämän alitehtävän loput vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4010c-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="4010c-117">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="4010c-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="4010c-118">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="4010c-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="4010c-119">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="4010c-119">Click Create repository.</span></span>
7. <span data-ttu-id="4010c-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4010c-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="4010c-121">Hae Microsoftin toimittamat myyntilaskumallin konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="4010c-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="4010c-122">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="4010c-122">Click Show filters.</span></span>
2. <span data-ttu-id="4010c-123">Käytä seuraavia suodattimia: anna suodattimeksi "Operatiivisen resurssit" Nimi-kenttään ja käytä "alkaa"-suodatinoperaattoria; kirjoita suodatinarvoksi "" Kuvaus-kenttään ja käytä "alkaa"-suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="4010c-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="4010c-124">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="4010c-124">Click Show filters.</span></span>
4. <span data-ttu-id="4010c-125">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="4010c-125">Click Open.</span></span>
5. <span data-ttu-id="4010c-126">Valitse puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="4010c-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="4010c-127">Valitse tuotavaksi mallikonfiguraatio "Myyntilaskumalli".</span><span class="sxs-lookup"><span data-stu-id="4010c-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="4010c-128">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="4010c-128">Click Import.</span></span>

    <span data-ttu-id="4010c-129">Valitse Tuo valitulle kokoonpanoversiolle 1</span><span class="sxs-lookup"><span data-stu-id="4010c-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="4010c-130">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4010c-130">Click Yes.</span></span>
8. <span data-ttu-id="4010c-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4010c-131">Close the page.</span></span>
9. <span data-ttu-id="4010c-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4010c-132">Close the page.</span></span>
10. <span data-ttu-id="4010c-133">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="4010c-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="4010c-134">Valitse puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="4010c-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="4010c-135">Luo johdettu malli, joka tukee tiedostonhallinnan tiedostojen käyttämistä.</span><span class="sxs-lookup"><span data-stu-id="4010c-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="4010c-136">Luot oman myyntilaskumallin konfiguraation johtamalla sen Microsoftin tarjoamasta konfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="4010c-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="4010c-137">Tätä konfiguraatiota käytetään tiedostonhallinnan käytön toteuttamiseen ja tiedostojen saattamiseen tällä mallilla luotavien sähköisten asiakirjojen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4010c-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="4010c-138">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="4010c-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="4010c-139">Kirjoita Uusi-kenttään "Derive from Name: Customer invoice model, Microsoft".</span><span class="sxs-lookup"><span data-stu-id="4010c-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="4010c-140">Syötä Nimi-kenttään "Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="4010c-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="4010c-141">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="4010c-141">Click Create configuration.</span></span>

