---
title: Luo ja suorita valmiit raportit
description: Tämän tehtävän ohjauksen avulla voit suorittaa valmiita raportteja Headquartersissa eri työtiloissa ja Commercessa olevissa kysely- ja myyntiraporteissa.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9931a39e4ca2141ed5b43086226c7fcc7cbd7c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022366"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="d23ce-103">Luo ja suorita valmiit raportit</span><span class="sxs-lookup"><span data-stu-id="d23ce-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d23ce-104">Tämän tehtävän ohjauksen avulla voit suorittaa valmiita raportteja Headquartersissa eri työtiloissa ja Commercessa olevissa kysely- ja myyntiraporteissa.</span><span class="sxs-lookup"><span data-stu-id="d23ce-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="d23ce-105">Tämän tallenteen luomisessa käytetty demotietojen yritys on USRT.</span><span class="sxs-lookup"><span data-stu-id="d23ce-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="d23ce-106">Tämä tallenne on tarkoitettu järjestelmänvalvojan roolille.</span><span class="sxs-lookup"><span data-stu-id="d23ce-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="d23ce-107">Käynnistä raportit työtiloista</span><span class="sxs-lookup"><span data-stu-id="d23ce-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="d23ce-108">Valitse Retail ja Commerce > Tuotteet ja luokat > Luokka- ja tuotehallinta.</span><span class="sxs-lookup"><span data-stu-id="d23ce-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="d23ce-109">Laajenna tai tiivistä Raportit-osa nuolella.</span><span class="sxs-lookup"><span data-stu-id="d23ce-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="d23ce-110">Valitse Parhaat tuotteet -raportti.</span><span class="sxs-lookup"><span data-stu-id="d23ce-110">Click Top products report.</span></span>
4. <span data-ttu-id="d23ce-111">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d23ce-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="d23ce-112">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d23ce-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="d23ce-113">Avaa haku valitsemalla Kanava-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d23ce-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d23ce-114">Valitse puussa solmu Contoso Retail\Contoso Retail USA\Central\Houston.</span><span class="sxs-lookup"><span data-stu-id="d23ce-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="d23ce-115">Tässä näkyy vähittäismyynnin raportoinnin merkityksen Commercen oletusorganisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="d23ce-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="d23ce-116">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkian tarkoitukset ja valitse Commercen raportointi. Valitse Määritetyt hierarkiat -osiosta sen hierarkian nimi, jonka Oletus-sarake on valittuna.</span><span class="sxs-lookup"><span data-stu-id="d23ce-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="d23ce-117">Myymälät alueen mukaan -kohta on myynnin raportoinnin tarkoituksen oletusorganisaatiohierarkia esittelytiedoissa (joita käytetään tämän tehtävän tallenteessa).</span><span class="sxs-lookup"><span data-stu-id="d23ce-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="d23ce-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d23ce-118">Click OK.</span></span>
9. <span data-ttu-id="d23ce-119">Valitse vaihtoehto Näytä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d23ce-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="d23ce-120">Valitse vaihtoehto Peruste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d23ce-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="d23ce-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d23ce-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="d23ce-122">Raporttien käynnistäminen kyselyt ja myynti -raporteista</span><span class="sxs-lookup"><span data-stu-id="d23ce-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="d23ce-123">Valitse Retail ja Commerce > Kyselyt ja raportit > Myyntiraportit > Luokan myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="d23ce-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="d23ce-124">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d23ce-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="d23ce-125">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d23ce-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="d23ce-126">Avaa haku valitsemalla Kanava-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d23ce-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d23ce-127">Valitse puussa solmu Contoso Retail\Contoso Retail USA\West\Seattle.</span><span class="sxs-lookup"><span data-stu-id="d23ce-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="d23ce-128">Tässä näkyy vähittäismyynnin raportoinnin merkityksen Commercen oletusorganisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="d23ce-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="d23ce-129">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkian tarkoitukset ja valitse Commercen raportointi. Valitse Määritetyt hierarkiat -osiosta sen hierarkian nimi, jonka Oletus-sarake on valittuna.</span><span class="sxs-lookup"><span data-stu-id="d23ce-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="d23ce-130">Myymälät alueen mukaan -kohta on myynnin raportoinnin tarkoituksen oletusorganisaatiohierarkia esittelytiedoissa (joita käytetään tämän tehtävän tallenteessa).</span><span class="sxs-lookup"><span data-stu-id="d23ce-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="d23ce-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d23ce-131">Click OK.</span></span>
7. <span data-ttu-id="d23ce-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d23ce-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="d23ce-133">Vie HQ -raportit</span><span class="sxs-lookup"><span data-stu-id="d23ce-133">Export an HQ reports</span></span>
1. <span data-ttu-id="d23ce-134">Valitse Retail ja Commerce > Kyselyt ja raportit > Myyntiraportit > Organisaation myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="d23ce-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="d23ce-135">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d23ce-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="d23ce-136">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d23ce-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="d23ce-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d23ce-137">Click OK.</span></span>
5. <span data-ttu-id="d23ce-138">Valitse Vie.</span><span class="sxs-lookup"><span data-stu-id="d23ce-138">Click Export.</span></span>
6. <span data-ttu-id="d23ce-139">Valitse PDF.</span><span class="sxs-lookup"><span data-stu-id="d23ce-139">Click PDF.</span></span>

