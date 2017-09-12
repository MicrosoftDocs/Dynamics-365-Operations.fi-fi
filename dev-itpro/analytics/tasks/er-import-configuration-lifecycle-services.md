--- 
title: "Konfiguraation tuonti Lifecycle Servicesista sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Lifecycle Services (LCS) -palvelusta."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0ea1e70f94e4b81919512127578d5927b36db56f
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="7ba62-103">Konfiguraation tuonti Lifecycle Servicesista sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="7ba62-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ba62-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Lifecycle Services (LCS) -palvelusta.</span><span class="sxs-lookup"><span data-stu-id="7ba62-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="7ba62-105">Tässä esimerkissä valitaan sopiva ER-konfiguraatio ja tuodaan se malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7ba62-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="7ba62-106">Lataa ER-kokoonpano Lifecycle Services -palveluun -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="7ba62-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="7ba62-107">Näiden vaiheiden suorittamiseen tarvitaan myös LCS:n käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="7ba62-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="7ba62-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="7ba62-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7ba62-109">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7ba62-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="7ba62-110">Poista tietomallin konfiguraation jaettu versio</span><span class="sxs-lookup"><span data-stu-id="7ba62-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="7ba62-111">Valitse puussa solmu Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="7ba62-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="7ba62-112">Ensimmäinen mallikonfiguraation esimerkkiversio on luotu ja julkaistu LCS:ään "Lataa ER-kokoonpano Lifecycle Services -palveluun" -menettelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="7ba62-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="7ba62-113">Tässä menettelyssä poistetaan kyseinen ER-konfiguraation versio.</span><span class="sxs-lookup"><span data-stu-id="7ba62-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="7ba62-114">Tämä tietomallin konfiguraation esimerkkiversio tuodaan LCS:stä myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="7ba62-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="7ba62-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7ba62-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ba62-116">Valitse tämän konfiguraation versio, jonka tila on "Jaettu".</span><span class="sxs-lookup"><span data-stu-id="7ba62-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="7ba62-117">Tämä tila ilmaisee, että konfiguraatio on julkaistu LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="7ba62-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="7ba62-118">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="7ba62-118">Click Change status.</span></span>
4. <span data-ttu-id="7ba62-119">Napsauta Lopeta.</span><span class="sxs-lookup"><span data-stu-id="7ba62-119">Click Discontinue.</span></span>
    * <span data-ttu-id="7ba62-120">Muuta valitun version tila jaetusta lopetetuksi, jotta se on poistettavissa.</span><span class="sxs-lookup"><span data-stu-id="7ba62-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="7ba62-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ba62-121">Click OK.</span></span>
6. <span data-ttu-id="7ba62-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7ba62-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ba62-123">Valitse tämän konfiguraation versio, jonka tila on "Lopetettu".</span><span class="sxs-lookup"><span data-stu-id="7ba62-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="7ba62-124">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="7ba62-124">Click Delete.</span></span>
8. <span data-ttu-id="7ba62-125">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7ba62-125">Click Yes.</span></span>
    * <span data-ttu-id="7ba62-126">Huomaa, että vain valitun tietomallin konfiguraation luonnosversio 2 on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7ba62-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="7ba62-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7ba62-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="7ba62-128">Tuo tietomallin konfiguraation jaettu versio LCS:stä</span><span class="sxs-lookup"><span data-stu-id="7ba62-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="7ba62-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7ba62-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7ba62-130">Avaa Litware, Inc:n säilöluettelo.</span><span class="sxs-lookup"><span data-stu-id="7ba62-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="7ba62-131">-konfiguraation lähteestä.</span><span class="sxs-lookup"><span data-stu-id="7ba62-131">configuration provider.</span></span>  
2. <span data-ttu-id="7ba62-132">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="7ba62-132">Click Repositories.</span></span>
3. <span data-ttu-id="7ba62-133">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="7ba62-133">Click Open.</span></span>
    * <span data-ttu-id="7ba62-134">Valitse LCS-säilö ja avaa se.</span><span class="sxs-lookup"><span data-stu-id="7ba62-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="7ba62-135">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7ba62-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7ba62-136">Valitse versioluettelosta ensimmäinen mallikonfiguraation esimerkkiversio.</span><span class="sxs-lookup"><span data-stu-id="7ba62-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="7ba62-137">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="7ba62-137">Click Import.</span></span>
6. <span data-ttu-id="7ba62-138">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7ba62-138">Click Yes.</span></span>
    * <span data-ttu-id="7ba62-139">Vahvista valitun version tuonti LCS:stä.</span><span class="sxs-lookup"><span data-stu-id="7ba62-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="7ba62-140">Huomaa, että valitun version tuonnin onnistuminen ilmaistaan tiedotuksella (lomakkeen yllä).</span><span class="sxs-lookup"><span data-stu-id="7ba62-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="7ba62-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7ba62-141">Close the page.</span></span>
8. <span data-ttu-id="7ba62-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7ba62-142">Close the page.</span></span>
9. <span data-ttu-id="7ba62-143">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7ba62-143">Click Configurations.</span></span>
10. <span data-ttu-id="7ba62-144">Valitse puussa solmu Mallikonfiguraation esimerkki.</span><span class="sxs-lookup"><span data-stu-id="7ba62-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="7ba62-145">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7ba62-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ba62-146">Valitse tämän konfiguraation versio, jonka tila on "Jaettu".</span><span class="sxs-lookup"><span data-stu-id="7ba62-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="7ba62-147">Huomaa, että valitun tietomallin konfiguraation jaettu versio 1 on nyt myös käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7ba62-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


