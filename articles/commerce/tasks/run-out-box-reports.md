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
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3dd941eb4e682e61c8b3d10ef0ccd14239f090c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232710"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="31c5c-103">Luo ja suorita valmiit raportit</span><span class="sxs-lookup"><span data-stu-id="31c5c-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31c5c-104">Tämän tehtävän ohjauksen avulla voit suorittaa valmiita raportteja Headquartersissa eri työtiloissa ja Commercessa olevissa kysely- ja myyntiraporteissa.</span><span class="sxs-lookup"><span data-stu-id="31c5c-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="31c5c-105">Tämän tallenteen luomisessa käytetty demotietojen yritys on USRT.</span><span class="sxs-lookup"><span data-stu-id="31c5c-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="31c5c-106">Tämä tallenne on tarkoitettu järjestelmänvalvojan roolille.</span><span class="sxs-lookup"><span data-stu-id="31c5c-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="31c5c-107">Käynnistä raportit työtiloista</span><span class="sxs-lookup"><span data-stu-id="31c5c-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="31c5c-108">Valitse Retail ja Commerce > Tuotteet ja luokat > Luokka- ja tuotehallinta.</span><span class="sxs-lookup"><span data-stu-id="31c5c-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="31c5c-109">Laajenna tai tiivistä Raportit-osa nuolella.</span><span class="sxs-lookup"><span data-stu-id="31c5c-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="31c5c-110">Valitse Parhaat tuotteet -raportti.</span><span class="sxs-lookup"><span data-stu-id="31c5c-110">Click Top products report.</span></span>
4. <span data-ttu-id="31c5c-111">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31c5c-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="31c5c-112">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31c5c-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="31c5c-113">Avaa haku valitsemalla Kanava-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="31c5c-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="31c5c-114">Valitse puussa solmu Contoso Retail\Contoso Retail USA\Central\Houston.</span><span class="sxs-lookup"><span data-stu-id="31c5c-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="31c5c-115">Tässä näkyy vähittäismyynnin raportoinnin merkityksen Commercen oletusorganisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="31c5c-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="31c5c-116">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkian tarkoitukset ja valitse Commercen raportointi. Valitse Määritetyt hierarkiat -osiosta sen hierarkian nimi, jonka Oletus-sarake on valittuna.</span><span class="sxs-lookup"><span data-stu-id="31c5c-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="31c5c-117">Myymälät alueen mukaan -kohta on myynnin raportoinnin tarkoituksen oletusorganisaatiohierarkia esittelytiedoissa (joita käytetään tämän tehtävän tallenteessa).</span><span class="sxs-lookup"><span data-stu-id="31c5c-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="31c5c-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31c5c-118">Click OK.</span></span>
9. <span data-ttu-id="31c5c-119">Valitse vaihtoehto Näytä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="31c5c-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="31c5c-120">Valitse vaihtoehto Peruste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="31c5c-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="31c5c-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31c5c-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="31c5c-122">Raporttien käynnistäminen kyselyt ja myynti -raporteista</span><span class="sxs-lookup"><span data-stu-id="31c5c-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="31c5c-123">Valitse Retail ja Commerce > Kyselyt ja raportit > Myyntiraportit > Luokan myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="31c5c-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="31c5c-124">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31c5c-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="31c5c-125">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31c5c-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="31c5c-126">Avaa haku valitsemalla Kanava-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="31c5c-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="31c5c-127">Valitse puussa solmu Contoso Retail\Contoso Retail USA\West\Seattle.</span><span class="sxs-lookup"><span data-stu-id="31c5c-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="31c5c-128">Tässä näkyy vähittäismyynnin raportoinnin merkityksen Commercen oletusorganisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="31c5c-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="31c5c-129">Valitse Organisaation hallinto > Organisaatiot > Organisaatiohierarkian tarkoitukset ja valitse Commercen raportointi. Valitse Määritetyt hierarkiat -osiosta sen hierarkian nimi, jonka Oletus-sarake on valittuna.</span><span class="sxs-lookup"><span data-stu-id="31c5c-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="31c5c-130">Myymälät alueen mukaan -kohta on myynnin raportoinnin tarkoituksen oletusorganisaatiohierarkia esittelytiedoissa (joita käytetään tämän tehtävän tallenteessa).</span><span class="sxs-lookup"><span data-stu-id="31c5c-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="31c5c-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31c5c-131">Click OK.</span></span>
7. <span data-ttu-id="31c5c-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31c5c-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="31c5c-133">Vie HQ -raportit</span><span class="sxs-lookup"><span data-stu-id="31c5c-133">Export an HQ reports</span></span>
1. <span data-ttu-id="31c5c-134">Valitse Retail ja Commerce > Kyselyt ja raportit > Myyntiraportit > Organisaation myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="31c5c-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="31c5c-135">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31c5c-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="31c5c-136">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31c5c-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="31c5c-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31c5c-137">Click OK.</span></span>
5. <span data-ttu-id="31c5c-138">Valitse Vie.</span><span class="sxs-lookup"><span data-stu-id="31c5c-138">Click Export.</span></span>
6. <span data-ttu-id="31c5c-139">Valitse PDF.</span><span class="sxs-lookup"><span data-stu-id="31c5c-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]