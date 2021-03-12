---
title: Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys
description: Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4d3bd54f0f2329c8c0602171a7f3c1ca444672b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985408"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="e68f8-103">Laajennettu pankkitäsmäytys MT940 tuonti - yhdistelmätietoyksikkö päivitys</span><span class="sxs-lookup"><span data-stu-id="e68f8-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e68f8-104">Järjestysnumero täytyy lisätä tiliotteen tuonnin yksikköön tukemaan MT940-muotoa.</span><span class="sxs-lookup"><span data-stu-id="e68f8-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="e68f8-105">Seuraavien vaiheiden avulla voit lisätä tiliotteen tuonnin entiteetin tukemaan MT940 muotoa.</span><span class="sxs-lookup"><span data-stu-id="e68f8-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="e68f8-106">Käännä ja synkronoi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e68f8-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="e68f8-107">Composite Entity\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="e68f8-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="e68f8-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="e68f8-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="e68f8-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="e68f8-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="e68f8-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="e68f8-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="e68f8-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="e68f8-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="e68f8-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="e68f8-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="e68f8-113">Tietojen hallinta\\tietoprojektit</span><span class="sxs-lookup"><span data-stu-id="e68f8-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="e68f8-114">Lataa MT940 tuontiprojektit</span><span class="sxs-lookup"><span data-stu-id="e68f8-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="e68f8-115">Vaihda XSLT.</span><span class="sxs-lookup"><span data-stu-id="e68f8-115">Change XSLT.</span></span>
            -   <span data-ttu-id="e68f8-116">Valitse **Näytä yhdistämismääritykset**.</span><span class="sxs-lookup"><span data-stu-id="e68f8-116">Click **View map**.</span></span>
            -   <span data-ttu-id="e68f8-117">Valitse **Näytä yhdistämismääritykset** tiliote-asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="e68f8-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="e68f8-118">Valitse **Muunnokset**</span><span class="sxs-lookup"><span data-stu-id="e68f8-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="e68f8-119">Poista BankReconiliation-to-Composite.xslt -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e68f8-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="e68f8-120">Lisää uusi versio tiedostosta BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="e68f8-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="e68f8-121">Näytä **järjestysnumero** kohdassa **Lähdetiedot** asettelu.</span><span class="sxs-lookup"><span data-stu-id="e68f8-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="e68f8-122">Lähdetietojen muoto = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="e68f8-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="e68f8-123">Yksikön nimi = tiliotteet.</span><span class="sxs-lookup"><span data-stu-id="e68f8-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="e68f8-124">Lataa datatiedosto = SampleBankCompositeEntity.xml uusi versio.</span><span class="sxs-lookup"><span data-stu-id="e68f8-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="e68f8-125">Korvaa aiemmin luotu tiedosto napsauttamalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e68f8-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="e68f8-126">Valitse **Kyllä** jolloin luodaan uusi yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="e68f8-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="e68f8-127">Varmista, että S **equenceNumber** on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="e68f8-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="e68f8-128">Valitse **Näytä yhdistämismääritykset** tiliote-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="e68f8-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="e68f8-129">Varmista, että **SequenceNumber** liitetään lähteestä väliaikaiseen alueeseen.</span><span class="sxs-lookup"><span data-stu-id="e68f8-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="e68f8-130">Tuo uusi tilinpäätös.</span><span class="sxs-lookup"><span data-stu-id="e68f8-130">Import the new statement.</span></span>




