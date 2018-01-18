--- 
title: Luo ja suorita valmiit raportit
description: "Tämän tehtävän ohjauksen avulla voit suorittaa valmiita raportteja pääkonttorissa eri työtiloissa ja Vähittäismyynti ja kauppa -kohdassa olevissa kysely- ja myyntiraporteissa."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: f77b4289613adce27bda43d326d969c984ef01b6
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="f9f97-103">Luo ja suorita valmiit raportit</span><span class="sxs-lookup"><span data-stu-id="f9f97-103">Generate and run out-of-box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f9f97-104">Tämän tehtävän ohjauksen avulla voit suorittaa valmiita raportteja pääkonttorissa eri työtiloissa ja Vähittäismyynti ja kauppa -kohdassa olevissa kysely- ja myyntiraporteissa.</span><span class="sxs-lookup"><span data-stu-id="f9f97-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="f9f97-105">Tämän tallenteen luomisessa käytetty demotietojen yritys on USRT.</span><span class="sxs-lookup"><span data-stu-id="f9f97-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="f9f97-106">Tämä tallenne on tarkoitettu järjestelmänvalvojan roolille.</span><span class="sxs-lookup"><span data-stu-id="f9f97-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="f9f97-107">Käynnistä raportit työtiloista</span><span class="sxs-lookup"><span data-stu-id="f9f97-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="f9f97-108">Valitse Vähittäismyynti ja kauppa > Tuotteet ja luokat > Luokka- ja tuotehallinta.</span><span class="sxs-lookup"><span data-stu-id="f9f97-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="f9f97-109">Laajenna tai tiivistä Raportit-osa nuolella.</span><span class="sxs-lookup"><span data-stu-id="f9f97-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="f9f97-110">Valitse Parhaat tuotteet -raportti.</span><span class="sxs-lookup"><span data-stu-id="f9f97-110">Click Top products report.</span></span>
4. <span data-ttu-id="f9f97-111">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9f97-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="f9f97-112">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9f97-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="f9f97-113">Avaa haku valitsemalla Kanava-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f9f97-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f9f97-114">Valitse puussa solmu Contoso Retail\Contoso Retail USA\Central\Houston.</span><span class="sxs-lookup"><span data-stu-id="f9f97-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="f9f97-115">Tässä näkyy vähittäismyynnin raportoinnin merkityksen vähittäismyynnin oletusorganisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="f9f97-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="f9f97-116">Valitse Organisaation hallinto >Organisaatiot > Organisaatiohierarkian tarkoitukset ja valitse Vähittäismyynnin raportointi. Valitse Määritetyt hierarkiat -kohdassa sen hierarkian nimi, jonka oletussarake on valittuna.</span><span class="sxs-lookup"><span data-stu-id="f9f97-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="f9f97-117">Vähittäismyymälät alueen mukaan -kohta on vähimmäismyynnin raportoinnin tarkoituksen oletusorganisaatiohierarkia esittelytiedoissa (joita käytetään tämän tehtävän tallenteessa).</span><span class="sxs-lookup"><span data-stu-id="f9f97-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="f9f97-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f9f97-118">Click OK.</span></span>
9. <span data-ttu-id="f9f97-119">Valitse vaihtoehto Näytä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9f97-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="f9f97-120">Valitse vaihtoehto Peruste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9f97-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="f9f97-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f9f97-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="f9f97-122">Käynnistä raportit kyselyistä ja myyntiraporteista, jotka löytyvät Vähittäismyynti ja kauppa -sovelluslinkin avulla.</span><span class="sxs-lookup"><span data-stu-id="f9f97-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="f9f97-123">Valitse Vähittäismyynti ja kauppa > Kyselyt ja raportit > Myyntiraportit > Luokan myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="f9f97-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="f9f97-124">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9f97-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f9f97-125">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9f97-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f9f97-126">Avaa haku valitsemalla Kanava-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f9f97-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f9f97-127">Valitse puussa solmu Contoso Retail\Contoso Retail USA\West\Seattle.</span><span class="sxs-lookup"><span data-stu-id="f9f97-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="f9f97-128">Tässä näkyy vähittäismyynnin raportoinnin merkityksen vähittäismyynnin oletusorganisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="f9f97-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="f9f97-129">Valitse Organisaation hallinto >Organisaatiot > Organisaatiohierarkian tarkoitukset ja valitse Vähittäismyynnin raportointi. Valitse Määritetyt hierarkiat -kohdassa sen hierarkian nimi, jonka oletussarake on valittuna.</span><span class="sxs-lookup"><span data-stu-id="f9f97-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="f9f97-130">Vähittäismyymälät alueen mukaan -kohta on vähimmäismyynnin raportoinnin tarkoituksen oletusorganisaatiohierarkia esittelytiedoissa (joita käytetään tämän tehtävän tallenteessa).</span><span class="sxs-lookup"><span data-stu-id="f9f97-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="f9f97-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f9f97-131">Click OK.</span></span>
7. <span data-ttu-id="f9f97-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f9f97-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="f9f97-133">Vie HQ -raportit</span><span class="sxs-lookup"><span data-stu-id="f9f97-133">Export an HQ reports</span></span>
1. <span data-ttu-id="f9f97-134">Valitse Vähittäismyynti ja kauppa > Kyselyt ja raportit > Myyntiraportit > Organisaation myyntiraportti.</span><span class="sxs-lookup"><span data-stu-id="f9f97-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="f9f97-135">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9f97-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f9f97-136">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f9f97-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f9f97-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f9f97-137">Click OK.</span></span>
5. <span data-ttu-id="f9f97-138">Valitse Vie.</span><span class="sxs-lookup"><span data-stu-id="f9f97-138">Click Export.</span></span>
6. <span data-ttu-id="f9f97-139">Valitse PDF.</span><span class="sxs-lookup"><span data-stu-id="f9f97-139">Click PDF.</span></span>


