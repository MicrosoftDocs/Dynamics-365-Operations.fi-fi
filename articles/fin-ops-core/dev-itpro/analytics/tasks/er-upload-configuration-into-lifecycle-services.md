---
title: ER Lataa kokoonpano Lifecycle Services -palveluun
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköisen raportoinnin (ER) konfiguraation ja ladata sen Microsoft Lifecycle Services -palveluun (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5def757de8fb9d347f5fd0f828039dad5c989c19
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143280"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="180e1-103">ER Lataa kokoonpano Lifecycle Services -palveluun</span><span class="sxs-lookup"><span data-stu-id="180e1-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="180e1-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköisen raportoinnin (ER) konfiguraation ja ladata sen Microsoft Lifecycle Services -palveluun (LCS).</span><span class="sxs-lookup"><span data-stu-id="180e1-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="180e1-105">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. ja ladataan sen LCS-palveluun. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="180e1-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="180e1-106">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="180e1-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="180e1-107">Näiden vaiheiden suorittamiseen tarvitaan myös LCS:n käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="180e1-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="180e1-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="180e1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="180e1-109">Valitse Litware, inc.</span><span class="sxs-lookup"><span data-stu-id="180e1-109">Select 'Litware, Inc.'</span></span> <span data-ttu-id="180e1-110">ja määritä aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="180e1-110">and set it as active.</span></span>
3. <span data-ttu-id="180e1-111">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="180e1-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="180e1-112">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="180e1-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="180e1-113">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="180e1-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="180e1-114">Luodaan konfiguraatio, joka sisältää tietomalliesimerkin sähköisiä asiakirjoja varten.</span><span class="sxs-lookup"><span data-stu-id="180e1-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="180e1-115">Tämä tietomallin konfiguraatio ladataan LCS:ään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="180e1-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="180e1-116">Syötä Nimi-kenttään Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="180e1-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="180e1-117">Mallikonfiguraation esimerkki</span><span class="sxs-lookup"><span data-stu-id="180e1-117">Sample model configuration</span></span>  
3. <span data-ttu-id="180e1-118">Syötä Kuvaus-kenttään Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="180e1-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="180e1-119">Mallikonfiguraation esimerkki</span><span class="sxs-lookup"><span data-stu-id="180e1-119">Sample model configuration</span></span>  
4. <span data-ttu-id="180e1-120">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="180e1-120">Click Create configuration.</span></span>
5. <span data-ttu-id="180e1-121">Valitse Mallin suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="180e1-121">Click Model designer.</span></span>
6. <span data-ttu-id="180e1-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="180e1-122">Click New.</span></span>
7. <span data-ttu-id="180e1-123">Syötä Nimi-kenttään Tulopaikka.</span><span class="sxs-lookup"><span data-stu-id="180e1-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="180e1-124">Tulopaikka</span><span class="sxs-lookup"><span data-stu-id="180e1-124">Entry point</span></span>  
8. <span data-ttu-id="180e1-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="180e1-125">Click Add.</span></span>
9. <span data-ttu-id="180e1-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="180e1-126">Click Save.</span></span>
10. <span data-ttu-id="180e1-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="180e1-127">Close the page.</span></span>
11. <span data-ttu-id="180e1-128">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="180e1-128">Click Change status.</span></span>
12. <span data-ttu-id="180e1-129">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="180e1-129">Click Complete.</span></span>
13. <span data-ttu-id="180e1-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="180e1-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="180e1-131">Rekisteröi uusi säilö</span><span class="sxs-lookup"><span data-stu-id="180e1-131">Register a new  repository</span></span>
1. <span data-ttu-id="180e1-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="180e1-132">Close the page.</span></span>
2. <span data-ttu-id="180e1-133">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="180e1-133">Click Repositories.</span></span>
    * <span data-ttu-id="180e1-134">Tämän avulla voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="180e1-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="180e1-135">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="180e1-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="180e1-136">Näin voit lisätä uuden säilön.</span><span class="sxs-lookup"><span data-stu-id="180e1-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="180e1-137">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi LCS.</span><span class="sxs-lookup"><span data-stu-id="180e1-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="180e1-138">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="180e1-138">Click Create repository.</span></span>
6. <span data-ttu-id="180e1-139">Anna tai valitse Projekti-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="180e1-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="180e1-140">Valitse haluamasi LCS-projekti.</span><span class="sxs-lookup"><span data-stu-id="180e1-140">Select the desired LCS project.</span></span> <span data-ttu-id="180e1-141">Sinulla on oltava käyttöoikeus projektiin.</span><span class="sxs-lookup"><span data-stu-id="180e1-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="180e1-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="180e1-142">Click OK.</span></span>
    * <span data-ttu-id="180e1-143">Luo uusi säilön merkintä.</span><span class="sxs-lookup"><span data-stu-id="180e1-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="180e1-144">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="180e1-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="180e1-145">Valitse LCS-säilön tietue.</span><span class="sxs-lookup"><span data-stu-id="180e1-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="180e1-146">Huomaa, että rekisteröity säilö on nykyisen lähteen merkitsemä, eli ainoastaan kyseisen lähteen omistamia konfiguraatioita voidaan sijoittaa tähän säilöön ja sen mukaisesti ladata valittuun LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="180e1-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="180e1-147">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="180e1-147">Click Open.</span></span>
    * <span data-ttu-id="180e1-148">Avaa säilö, jotta voit tarkastella ER-konfiguraatioiden luetteloa.</span><span class="sxs-lookup"><span data-stu-id="180e1-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="180e1-149">Se on tyhjä, jos projektia ei ole vielä käytetty ER-konfiguraatioiden jakamiseen.</span><span class="sxs-lookup"><span data-stu-id="180e1-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="180e1-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="180e1-150">Close the page.</span></span>
11. <span data-ttu-id="180e1-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="180e1-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="180e1-152">Lataa konfiguraatio LCS:ään</span><span class="sxs-lookup"><span data-stu-id="180e1-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="180e1-153">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="180e1-153">Click Configurations.</span></span>
2. <span data-ttu-id="180e1-154">Valitse puussa solmu Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="180e1-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="180e1-155">Valitse luotu konfiguraatio, joka on jo valmis.</span><span class="sxs-lookup"><span data-stu-id="180e1-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="180e1-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="180e1-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="180e1-157">Valitse kyseisen konfiguraation versio, joka "Valmis"-tilassa.</span><span class="sxs-lookup"><span data-stu-id="180e1-157">Select the version of the selected configuration with the status of 'Completed'.</span></span>  
4. <span data-ttu-id="180e1-158">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="180e1-158">Click Change status.</span></span>
5. <span data-ttu-id="180e1-159">Valitse Jaa.</span><span class="sxs-lookup"><span data-stu-id="180e1-159">Click Share.</span></span>
    * <span data-ttu-id="180e1-160">Konfiguraation tila muutetaan valmiista jaetuksi, kun se julkaistaan LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="180e1-160">The configuration status will change from 'Completed' to 'Shared' when it is published in LCS.</span></span>  
6. <span data-ttu-id="180e1-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="180e1-161">Click OK.</span></span>
7. <span data-ttu-id="180e1-162">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="180e1-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="180e1-163">Valitse konfiguraation versio, jonka tila on "Jaettu".</span><span class="sxs-lookup"><span data-stu-id="180e1-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="180e1-164">Huomaa, että valitun version on tila on muuttunut valmiista jaetuksi.</span><span class="sxs-lookup"><span data-stu-id="180e1-164">Note that the status of the selected version has changed from 'Completed' to 'Shared'.</span></span>  
8. <span data-ttu-id="180e1-165">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="180e1-165">Close the page.</span></span>
9. <span data-ttu-id="180e1-166">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="180e1-166">Click Repositories.</span></span>
    * <span data-ttu-id="180e1-167">Tämän avulla voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="180e1-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="180e1-168">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="180e1-168">Click Open.</span></span>
    * <span data-ttu-id="180e1-169">Valitse LCS-säilö ja avaa se.</span><span class="sxs-lookup"><span data-stu-id="180e1-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="180e1-170">Huomaa, että valittu konfiguraatio näytetään resurssina valitussa LCS-projektissa.</span><span class="sxs-lookup"><span data-stu-id="180e1-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="180e1-171">Avaa LCS käyttämällä https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="180e1-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="180e1-172">Avaa aiemmin säilön rekisteröintiin käytetty projekti ja avaa projektin "Omaisuuskirjasto" ja laajenna GER-konfiguraatio -omaisuustyypin sisältö – ladattu ER-konfiguraatio on käytettävissä täällä.</span><span class="sxs-lookup"><span data-stu-id="180e1-172">Open a project that was used earlier for repository registration, open the 'Asset library' of this project, and expand the content of the 'GER configuration' asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="180e1-173">Huomaa, että ladattu LCS-konfiguraatio voidaan tuoda toiseen esiintymään, jos tarjoajilla on käyttöoikeus tähän LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="180e1-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

