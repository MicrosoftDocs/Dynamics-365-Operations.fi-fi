---
title: Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen
description: Seuraavat vaiheet ovat välttämättömät, jotta voit lisätä BankTransactionType-lisäkentän BankJournalEntity-yhdistelmäyksikköön.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442633"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="4c623-103">Pankin kirjauskansioiden yhdistelmäyksikön päivittäminen</span><span class="sxs-lookup"><span data-stu-id="4c623-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c623-104">Seuraavat vaiheet ovat välttämättömät, jotta voit lisätä BankTransactionType-lisäkentän BankJournalEntity-yhdistelmäyksikköön.</span><span class="sxs-lookup"><span data-stu-id="4c623-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="4c623-105">Seuraavien vaiheiden avulla voit lisätä BankTransactionType-lisäkentän BankJournalEntity-yhdistelmäyksikköön.</span><span class="sxs-lookup"><span data-stu-id="4c623-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="4c623-106">Kääntää ja synkronoi seuraavat pankin kirjauskansion yhdistelmäyksiköt, yksiköt ja valmistelutaulut:</span><span class="sxs-lookup"><span data-stu-id="4c623-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="4c623-107">Yhdistelmäyksikkö\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="4c623-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="4c623-108">Yksikkö\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="4c623-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="4c623-109">Yksikkö\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="4c623-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="4c623-110">Taulu\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="4c623-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="4c623-111">Taulu\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="4c623-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="4c623-112">Tietojen hallinta\\tietoprojektit</span><span class="sxs-lookup"><span data-stu-id="4c623-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="4c623-113">Näytä **pankkitapahtuma**-tyyppi **Lähdetiedot**-asettelussa.</span><span class="sxs-lookup"><span data-stu-id="4c623-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="4c623-114">Lähdetietojen muoto = XML-elementti</span><span class="sxs-lookup"><span data-stu-id="4c623-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="4c623-115">Yksikön nimi = pankin kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4c623-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="4c623-116">Lataa datatiedosto = SampleBankJournalCompositeEntity.xml uusi versio.</span><span class="sxs-lookup"><span data-stu-id="4c623-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="4c623-117">Korvaa aiemmin luotu tiedosto napsauttamalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4c623-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="4c623-118">Valitse **Kyllä** jolloin luodaan uusi yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="4c623-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="4c623-119">Tarkista, että pankkitapahtuman laji on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="4c623-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="4c623-120">Valitse **Näytä yhdistämismääritykset** rivi-yksikössä.</span><span class="sxs-lookup"><span data-stu-id="4c623-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="4c623-121">Varmista, että pankkitapahtuman laji liitetään lähteestä väliaikaiseen alueeseen.</span><span class="sxs-lookup"><span data-stu-id="4c623-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="4c623-122">Tuo uusi tilinpäätös.</span><span class="sxs-lookup"><span data-stu-id="4c623-122">Import the new statement.</span></span>




