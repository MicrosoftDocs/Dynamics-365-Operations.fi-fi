---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämistä aiemmin luotuun tekstiin perustuvaa laskentaa ja summien tuottamista. (Osa 1)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3639b5ac28f8a571642e983906d658dabf05b1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093019"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="a248d-104">ER Määritä muoto suorittamaan laskenta ja summaus (Osa 1 – Muodon luonti)</span><span class="sxs-lookup"><span data-stu-id="a248d-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a248d-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a248d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a248d-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="a248d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a248d-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="a248d-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="a248d-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="a248d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="a248d-109">Saat luettelon Microsoftin tarjoamista kokoonpanoista</span><span class="sxs-lookup"><span data-stu-id="a248d-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="a248d-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="a248d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a248d-111">Varmista, että Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a248d-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="a248d-112">-lähde on käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="a248d-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="a248d-113">Valitse Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a248d-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="a248d-114">-tarjoaja.</span><span class="sxs-lookup"><span data-stu-id="a248d-114">provider.</span></span>
3. <span data-ttu-id="a248d-115">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="a248d-115">Click Repositories.</span></span>
    * <span data-ttu-id="a248d-116">Jos säilön tyyppi "Operatiiviset resurssit" on jo olemassa, ohita tämän alitehtävän loput vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a248d-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="a248d-117">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="a248d-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="a248d-118">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="a248d-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="a248d-119">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="a248d-119">Click Create repository.</span></span>
7. <span data-ttu-id="a248d-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a248d-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="a248d-121">Hae Microsoftin Intrastat-kokoonpanot</span><span class="sxs-lookup"><span data-stu-id="a248d-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="a248d-122">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="a248d-122">Click Open.</span></span>
2. <span data-ttu-id="a248d-123">Valitse puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="a248d-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="a248d-124">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="a248d-124">Click Import.</span></span>
    * <span data-ttu-id="a248d-125">Valitse Tuo valitulle kokoonpanoversiolle 1.1</span><span class="sxs-lookup"><span data-stu-id="a248d-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="a248d-126">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a248d-126">Click Yes.</span></span>
5. <span data-ttu-id="a248d-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a248d-127">Close the page.</span></span>
6. <span data-ttu-id="a248d-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a248d-128">Close the page.</span></span>
7. <span data-ttu-id="a248d-129">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="a248d-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="a248d-130">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="a248d-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="a248d-131">Valitse puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="a248d-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

