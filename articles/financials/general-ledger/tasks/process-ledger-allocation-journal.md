---
title: Käsittele kirjanpidon kohdistuskirjauskansio
description: Voit luoda Käsittele kohdistuspyyntö -sivulla kohdistuskirjauskansion, joka voidaan tarkistaa ja hyväksyä ennen kirjanpitoon kirjaamista tai kirjata kirjanpitoon suoraan.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550818"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="6f15d-103">Käsittele kirjanpidon kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="6f15d-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f15d-104">Voit luoda Käsittele kohdistuspyyntö -sivulla kohdistuskirjauskansion, joka voidaan tarkistaa ja hyväksyä ennen kirjanpitoon kirjaamista tai kirjata kirjanpitoon suoraan.</span><span class="sxs-lookup"><span data-stu-id="6f15d-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="6f15d-105">Ennen kohdistuskirjauskansion luomista käytössä on oltava vähintään yksi aktiivinen kirjanpidon kohdistussääntö.</span><span class="sxs-lookup"><span data-stu-id="6f15d-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="6f15d-106">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="6f15d-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6f15d-107">Valitse Kirjanpito > Kohdistukset > Käsittele kohdistuspyyntö.</span><span class="sxs-lookup"><span data-stu-id="6f15d-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="6f15d-108">Avaa haku napsauttamalla Sääntö-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f15d-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6f15d-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6f15d-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6f15d-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6f15d-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6f15d-111">Lisää Alkupäivämäärä -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="6f15d-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="6f15d-112">Alkupäivämäärä on erittäin tärkeä, kun kirjanpito on säännön tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6f15d-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="6f15d-113">Tämä päivämäärä määrittää, mitkä kirjanpidon saldot sisällytetään kohdistukseen.</span><span class="sxs-lookup"><span data-stu-id="6f15d-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="6f15d-114">Valitse Lähdearvo nolla -kentässä Pysäytä.</span><span class="sxs-lookup"><span data-stu-id="6f15d-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="6f15d-115">Kohdistusprosessi pysäytetään ja näyttöön avautuu sanoma, jonka mukaan lähdesumma on nolla.</span><span class="sxs-lookup"><span data-stu-id="6f15d-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="6f15d-116">Valitse Ehdotuksen asetukset -kentässä Vain ehdotus.</span><span class="sxs-lookup"><span data-stu-id="6f15d-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="6f15d-117">Valitsemalla Vain ehdotus voit tarkastella ja halutessasi hyväksyä tuloksen kohdistuskirjauskansioissa ennen kohdistuksen kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="6f15d-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="6f15d-118">Lisää päivämäärä Kirjanpidon kirjauspäivä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f15d-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="6f15d-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6f15d-119">Click OK.</span></span>
9. <span data-ttu-id="6f15d-120">Valitse Kirjanpito > Kohdistukset > Kohdistuskirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="6f15d-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="6f15d-121">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="6f15d-121">Click Lines.</span></span>
11. <span data-ttu-id="6f15d-122">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="6f15d-122">Click Post.</span></span>
12. <span data-ttu-id="6f15d-123">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="6f15d-123">Click Post.</span></span>

