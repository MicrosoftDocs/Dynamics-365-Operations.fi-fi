--- 
title: "Lataa konfiguraatio Lifecycle Servicesiin sähköistä raportointia varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköisen raportoinnin (ER) konfiguraation ja ladata sen Microsoft Lifecycle Services -palveluun (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6aa6bf7e08285d18210741ba6618878955009280
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="upload-electronic-reporting-configurations-into-lifecycle-services"></a><span data-ttu-id="732c6-103">Lataa konfiguraatio Lifecycle Servicesiin sähköistä raportointia varten</span><span class="sxs-lookup"><span data-stu-id="732c6-103">Upload Electronic reporting configurations into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="732c6-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköisen raportoinnin (ER) konfiguraation ja ladata sen Microsoft Lifecycle Services -palveluun (LCS).</span><span class="sxs-lookup"><span data-stu-id="732c6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="732c6-105">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. ja ladataan sen LCS-palveluun. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="732c6-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="732c6-106">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="732c6-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="732c6-107">Näiden vaiheiden suorittamiseen tarvitaan myös LCS:n käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="732c6-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="732c6-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="732c6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="732c6-109">Valitse Litware, inc.</span><span class="sxs-lookup"><span data-stu-id="732c6-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="732c6-110">ja määritä aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="732c6-110">and set it as active.</span></span>
3. <span data-ttu-id="732c6-111">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="732c6-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="732c6-112">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="732c6-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="732c6-113">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="732c6-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="732c6-114">Luodaan konfiguraatio, joka sisältää tietomalliesimerkin sähköisiä asiakirjoja varten.</span><span class="sxs-lookup"><span data-stu-id="732c6-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="732c6-115">Tämä tietomallin konfiguraatio ladataan LCS:ään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="732c6-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="732c6-116">Syötä Nimi-kenttään Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="732c6-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="732c6-117">Mallikonfiguraation esimerkki</span><span class="sxs-lookup"><span data-stu-id="732c6-117">Sample model configuration</span></span>  
3. <span data-ttu-id="732c6-118">Syötä Kuvaus-kenttään Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="732c6-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="732c6-119">Mallikonfiguraation esimerkki</span><span class="sxs-lookup"><span data-stu-id="732c6-119">Sample model configuration</span></span>  
4. <span data-ttu-id="732c6-120">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="732c6-120">Click Create configuration.</span></span>
5. <span data-ttu-id="732c6-121">Valitse Mallin suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="732c6-121">Click Model designer.</span></span>
6. <span data-ttu-id="732c6-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="732c6-122">Click New.</span></span>
7. <span data-ttu-id="732c6-123">Syötä Nimi-kenttään Tulopaikka.</span><span class="sxs-lookup"><span data-stu-id="732c6-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="732c6-124">Tulopaikka</span><span class="sxs-lookup"><span data-stu-id="732c6-124">Entry point</span></span>  
8. <span data-ttu-id="732c6-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="732c6-125">Click Add.</span></span>
9. <span data-ttu-id="732c6-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="732c6-126">Click Save.</span></span>
10. <span data-ttu-id="732c6-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="732c6-127">Close the page.</span></span>
11. <span data-ttu-id="732c6-128">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="732c6-128">Click Change status.</span></span>
12. <span data-ttu-id="732c6-129">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="732c6-129">Click Complete.</span></span>
13. <span data-ttu-id="732c6-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="732c6-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="732c6-131">Rekisteröi uusi säilö</span><span class="sxs-lookup"><span data-stu-id="732c6-131">Register a new  repository</span></span>
1. <span data-ttu-id="732c6-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="732c6-132">Close the page.</span></span>
2. <span data-ttu-id="732c6-133">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="732c6-133">Click Repositories.</span></span>
    * <span data-ttu-id="732c6-134">Tämän avulla voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="732c6-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="732c6-135">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="732c6-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="732c6-136">Näin voit lisätä uuden säilön.</span><span class="sxs-lookup"><span data-stu-id="732c6-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="732c6-137">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi LCS.</span><span class="sxs-lookup"><span data-stu-id="732c6-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="732c6-138">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="732c6-138">Click Create repository.</span></span>
6. <span data-ttu-id="732c6-139">Anna tai valitse Projekti-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="732c6-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="732c6-140">Valitse haluamasi LCS-projekti.</span><span class="sxs-lookup"><span data-stu-id="732c6-140">Select the desired LCS project.</span></span> <span data-ttu-id="732c6-141">Sinulla on oltava käyttöoikeus projektiin.</span><span class="sxs-lookup"><span data-stu-id="732c6-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="732c6-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="732c6-142">Click OK.</span></span>
    * <span data-ttu-id="732c6-143">Luo uusi säilön merkintä.</span><span class="sxs-lookup"><span data-stu-id="732c6-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="732c6-144">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="732c6-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="732c6-145">Valitse LCS-säilön tietue.</span><span class="sxs-lookup"><span data-stu-id="732c6-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="732c6-146">Huomaa, että rekisteröity säilö on nykyisen lähteen merkitsemä, eli ainoastaan kyseisen lähteen omistamia konfiguraatioita voidaan sijoittaa tähän säilöön ja sen mukaisesti ladata valittuun LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="732c6-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="732c6-147">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="732c6-147">Click Open.</span></span>
    * <span data-ttu-id="732c6-148">Avaa säilö, jotta voit tarkastella ER-konfiguraatioiden luetteloa.</span><span class="sxs-lookup"><span data-stu-id="732c6-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="732c6-149">Se on tyhjä, jos projektia ei ole vielä käytetty ER-konfiguraatioiden jakamiseen.</span><span class="sxs-lookup"><span data-stu-id="732c6-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="732c6-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="732c6-150">Close the page.</span></span>
11. <span data-ttu-id="732c6-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="732c6-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="732c6-152">Lataa konfiguraatio LCS:ään</span><span class="sxs-lookup"><span data-stu-id="732c6-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="732c6-153">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="732c6-153">Click Configurations.</span></span>
2. <span data-ttu-id="732c6-154">Valitse puussa solmu Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="732c6-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="732c6-155">Valitse luotu konfiguraatio, joka on jo valmis.</span><span class="sxs-lookup"><span data-stu-id="732c6-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="732c6-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="732c6-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="732c6-157">Valitse kyseisen konfiguraation versio, joka "Valmis"-tilassa.</span><span class="sxs-lookup"><span data-stu-id="732c6-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="732c6-158">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="732c6-158">Click Change status.</span></span>
5. <span data-ttu-id="732c6-159">Valitse Jaa.</span><span class="sxs-lookup"><span data-stu-id="732c6-159">Click Share.</span></span>
    * <span data-ttu-id="732c6-160">Konfiguraation tila muutetaan valmiista jaetuksi, kun se julkaistaan LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="732c6-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="732c6-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="732c6-161">Click OK.</span></span>
7. <span data-ttu-id="732c6-162">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="732c6-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="732c6-163">Valitse konfiguraation versio, jonka tila on "Jaettu".</span><span class="sxs-lookup"><span data-stu-id="732c6-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="732c6-164">Huomaa, että valitun version on tila on muuttunut valmiista jaetuksi.</span><span class="sxs-lookup"><span data-stu-id="732c6-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="732c6-165">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="732c6-165">Close the page.</span></span>
9. <span data-ttu-id="732c6-166">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="732c6-166">Click Repositories.</span></span>
    * <span data-ttu-id="732c6-167">Tämän avulla voit avata Litware, Inc. -konfiguraatiolähteen säilöluettelon.</span><span class="sxs-lookup"><span data-stu-id="732c6-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="732c6-168">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="732c6-168">Click Open.</span></span>
    * <span data-ttu-id="732c6-169">Valitse LCS-säilö ja avaa se.</span><span class="sxs-lookup"><span data-stu-id="732c6-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="732c6-170">Huomaa, että valittu konfiguraatio näytetään resurssina valitussa LCS-projektissa.</span><span class="sxs-lookup"><span data-stu-id="732c6-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="732c6-171">Avaa LCS käyttämällä https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="732c6-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="732c6-172">Avaa aiemmin säilön rekisteröintiin käytetty projekti ja avaa projektin "Omaisuuskirjasto" ja laajenna GER-konfiguraatio -omaisuustyypin sisältö – ladattu ER-konfiguraatio on käytettävissä täällä.</span><span class="sxs-lookup"><span data-stu-id="732c6-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="732c6-173">Huomaa, että ladattu LCS-konfiguraatio voidaan tuoda toiseen Microsoft Dynamics 365 for Finance and Operations -esiintymään, jos lähteillä on käyttöoikeus tähän LCS-projektiin.</span><span class="sxs-lookup"><span data-stu-id="732c6-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations instance if providers have access to this LCS project.</span></span>  


