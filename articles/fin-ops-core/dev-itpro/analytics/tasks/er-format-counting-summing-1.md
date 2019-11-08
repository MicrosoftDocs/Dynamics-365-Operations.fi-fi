---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85109cd0448383ba231cbec1bdeeb9dcd2db805
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550783"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="d0188-103">ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)</span><span class="sxs-lookup"><span data-stu-id="d0188-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0188-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d0188-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="d0188-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d0188-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d0188-106">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="d0188-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="d0188-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="d0188-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="d0188-108">Saat luettelon Microsoftin tarjoamista kokoonpanoista</span><span class="sxs-lookup"><span data-stu-id="d0188-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="d0188-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="d0188-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d0188-110">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d0188-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="d0188-111">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="d0188-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="d0188-112">Valitse Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d0188-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="d0188-113">-tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="d0188-113">provider.</span></span>
3. <span data-ttu-id="d0188-114">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="d0188-114">Click Repositories.</span></span>
    * <span data-ttu-id="d0188-115">Jos säilön tyyppi "Operatiiviset resurssit" on jo olemassa, ohita tämän alitehtävän loput vaiheet.</span><span class="sxs-lookup"><span data-stu-id="d0188-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="d0188-116">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="d0188-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="d0188-117">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="d0188-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="d0188-118">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="d0188-118">Click Create repository.</span></span>
7. <span data-ttu-id="d0188-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d0188-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="d0188-120">Hae Microsoftin Intrastat-kokoonpanot</span><span class="sxs-lookup"><span data-stu-id="d0188-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="d0188-121">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="d0188-121">Click Open.</span></span>
2. <span data-ttu-id="d0188-122">Valitse puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="d0188-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="d0188-123">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="d0188-123">Click Import.</span></span>
    * <span data-ttu-id="d0188-124">Valitse Tuo valitulle kokoonpanoversiolle 1.1</span><span class="sxs-lookup"><span data-stu-id="d0188-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="d0188-125">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d0188-125">Click Yes.</span></span>
5. <span data-ttu-id="d0188-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d0188-126">Close the page.</span></span>
6. <span data-ttu-id="d0188-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d0188-127">Close the page.</span></span>
7. <span data-ttu-id="d0188-128">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="d0188-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="d0188-129">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="d0188-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="d0188-130">Valitse puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="d0188-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

