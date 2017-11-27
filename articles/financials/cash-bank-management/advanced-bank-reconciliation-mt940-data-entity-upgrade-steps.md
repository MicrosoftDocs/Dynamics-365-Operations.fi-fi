---
title: "Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys"
description: "Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a76558d220e98de85060d23d6e5d8df1c0cd1baf
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="4871a-103">Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys</span><span class="sxs-lookup"><span data-stu-id="4871a-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4871a-104">Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.</span><span class="sxs-lookup"><span data-stu-id="4871a-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="4871a-105">Seuraavien vaiheiden avulla voit lisätä tiliotteen tuonnin entiteetin tukemaan MT940 muotoa.</span><span class="sxs-lookup"><span data-stu-id="4871a-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="4871a-106">Käännä ja synkronoi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4871a-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="4871a-107">Composite Entity\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="4871a-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="4871a-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="4871a-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="4871a-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="4871a-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="4871a-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="4871a-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="4871a-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="4871a-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="4871a-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="4871a-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="4871a-113">Tietojen hallinta\\tietoprojektit</span><span class="sxs-lookup"><span data-stu-id="4871a-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="4871a-114">Lataa MT940 tuontiprojektit</span><span class="sxs-lookup"><span data-stu-id="4871a-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="4871a-115">Vaihda XSLT.</span><span class="sxs-lookup"><span data-stu-id="4871a-115">Change XSLT.</span></span>
            -   <span data-ttu-id="4871a-116">Valitse **Näytä yhdistämismääritykset**.</span><span class="sxs-lookup"><span data-stu-id="4871a-116">Click **View map**.</span></span>
            -   <span data-ttu-id="4871a-117">Valitse **Näytä yhdistämismääritykset** tiliote-asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="4871a-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="4871a-118">Valitse **Muunnokset**</span><span class="sxs-lookup"><span data-stu-id="4871a-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="4871a-119">Poista BankReconiliation-to-Composite.xslt -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="4871a-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="4871a-120">Lisää uusi versio tiedostosta BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="4871a-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="4871a-121">Näytä **järjestysnumero** kohdassa **Lähdetiedot** asettelu.</span><span class="sxs-lookup"><span data-stu-id="4871a-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="4871a-122">Lähdetietojen muoto = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="4871a-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="4871a-123">Yksikön nimi = tiliotteet.</span><span class="sxs-lookup"><span data-stu-id="4871a-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="4871a-124">Lataa datatiedosto = SampleBankCompositeEntity.xml uusi versio.</span><span class="sxs-lookup"><span data-stu-id="4871a-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="4871a-125">Korvaa aiemmin luotu tiedosto napsauttamalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4871a-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="4871a-126">Valitse **Kyllä** jolloin luodaan uusi yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="4871a-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="4871a-127">Varmista, että S**equenceNumber** on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="4871a-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="4871a-128">Valitse **Näytä yhdistämismääritykset** tiliote-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="4871a-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="4871a-129">Varmista, että **SequenceNumber** liitetään lähteestä väliaikaiseen alueeseen.</span><span class="sxs-lookup"><span data-stu-id="4871a-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="4871a-130">Tuo uusi tilinpäätös.</span><span class="sxs-lookup"><span data-stu-id="4871a-130">Import the new statement.</span></span>





