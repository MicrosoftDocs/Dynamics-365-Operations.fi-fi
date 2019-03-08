---
title: Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys
description: Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "343785"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="e2bbb-103">Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys</span><span class="sxs-lookup"><span data-stu-id="e2bbb-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2bbb-104">Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="e2bbb-105">Seuraavien vaiheiden avulla voit lisätä tiliotteen tuonnin entiteetin tukemaan MT940 muotoa.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="e2bbb-106">Käännä ja synkronoi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e2bbb-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="e2bbb-107">Composite Entity\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="e2bbb-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="e2bbb-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="e2bbb-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="e2bbb-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="e2bbb-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="e2bbb-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="e2bbb-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="e2bbb-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="e2bbb-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="e2bbb-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="e2bbb-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="e2bbb-113">Tietojen hallinta\\tietoprojektit</span><span class="sxs-lookup"><span data-stu-id="e2bbb-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="e2bbb-114">Lataa MT940 tuontiprojektit</span><span class="sxs-lookup"><span data-stu-id="e2bbb-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="e2bbb-115">Vaihda XSLT.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-115">Change XSLT.</span></span>
            -   <span data-ttu-id="e2bbb-116">Valitse **Näytä yhdistämismääritykset**.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-116">Click **View map**.</span></span>
            -   <span data-ttu-id="e2bbb-117">Valitse **Näytä yhdistämismääritykset** tiliote-asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="e2bbb-118">Valitse **Muunnokset**</span><span class="sxs-lookup"><span data-stu-id="e2bbb-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="e2bbb-119">Poista BankReconiliation-to-Composite.xslt -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="e2bbb-120">Lisää uusi versio tiedostosta BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="e2bbb-121">Näytä **järjestysnumero** kohdassa **Lähdetiedot** asettelu.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="e2bbb-122">Lähdetietojen muoto = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="e2bbb-123">Yksikön nimi = tiliotteet.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="e2bbb-124">Lataa datatiedosto = SampleBankCompositeEntity.xml uusi versio.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="e2bbb-125">Korvaa aiemmin luotu tiedosto napsauttamalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="e2bbb-126">Valitse **Kyllä** jolloin luodaan uusi yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="e2bbb-127">Varmista, että S**equenceNumber** on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="e2bbb-128">Valitse **Näytä yhdistämismääritykset** tiliote-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="e2bbb-129">Varmista, että **SequenceNumber** liitetään lähteestä väliaikaiseen alueeseen.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="e2bbb-130">Tuo uusi tilinpäätös.</span><span class="sxs-lookup"><span data-stu-id="e2bbb-130">Import the new statement.</span></span>




