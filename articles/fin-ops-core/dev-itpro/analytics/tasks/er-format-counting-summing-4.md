---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 4 – Muodon suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4256864db8af5d2851c1203c1a85d79fd270b6a8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184896"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a><span data-ttu-id="d47bb-103">ER Määritä muoto suorittamaan laskenta ja summaus (osa 4: muodon suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="d47bb-103">ER Configure format to do counting and summing (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d47bb-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d47bb-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="d47bb-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d47bb-106">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 3: Käytä laskentoja tuotoksen luomiseen)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="d47bb-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="d47bb-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="d47bb-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="d47bb-108">Testaa konfiguraation Intrastat-raporttien luonti</span><span class="sxs-lookup"><span data-stu-id="d47bb-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="d47bb-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="d47bb-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d47bb-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="d47bb-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d47bb-111">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="d47bb-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="d47bb-112">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="d47bb-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="d47bb-113">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="d47bb-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="d47bb-114">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="d47bb-115">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-115">Click User parameters.</span></span>
8. <span data-ttu-id="d47bb-116">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="d47bb-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d47bb-117">Click OK.</span></span>
10. <span data-ttu-id="d47bb-118">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d47bb-118">Click Edit.</span></span>
11. <span data-ttu-id="d47bb-119">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="d47bb-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d47bb-120">Click Save.</span></span>
13. <span data-ttu-id="d47bb-121">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="d47bb-122">Laajenna Sähköinen raportointi -osa.</span><span class="sxs-lookup"><span data-stu-id="d47bb-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="d47bb-123">Valitse Intrastat (DE) with counting & summing -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="d47bb-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="d47bb-124">Valitse Intrastat (DE) with counting & summing -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="d47bb-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="d47bb-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d47bb-125">Click Save.</span></span>
18. <span data-ttu-id="d47bb-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d47bb-126">Close the page.</span></span>
19. <span data-ttu-id="d47bb-127">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d47bb-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="d47bb-128">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="d47bb-128">Click Output.</span></span>
21. <span data-ttu-id="d47bb-129">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="d47bb-129">Click Report.</span></span>
    * <span data-ttu-id="d47bb-130">Aja Intrastat-raportin luontiprosessi.</span><span class="sxs-lookup"><span data-stu-id="d47bb-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="d47bb-131">Syötä Päivämäärästä-kenttään päivämäärä 1.1.2000.</span><span class="sxs-lookup"><span data-stu-id="d47bb-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="d47bb-132">Määritä raportointikauden aloitus- ja päättymispäivämäärät, joka sisältää aiemmin luodin lomakkeen tapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="d47bb-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="d47bb-133">Lisää Päivämäärään-kenttään päivämäärä 31.12.2022.</span><span class="sxs-lookup"><span data-stu-id="d47bb-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="d47bb-134">Määritä raportointikauden aloitus- ja päättymispäivämäärät, joka sisältää aiemmin luodin lomakkeen tapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="d47bb-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="d47bb-135">Valitse Saapumiset-vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="d47bb-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="d47bb-136">Valitse Luo tiedosto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="d47bb-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d47bb-137">Click OK.</span></span>
    * <span data-ttu-id="d47bb-138">Tarkasta luotu tuotos ja sen yhteenvetorivit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="d47bb-139">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d47bb-139">Click New.</span></span>
28. <span data-ttu-id="d47bb-140">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d47bb-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="d47bb-141">Valitse Toimitukset-vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="d47bb-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="d47bb-142">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="d47bb-143">Syötä tai valitse arvo Kauppatavara-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="d47bb-144">Aseta painoarvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="d47bb-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="d47bb-145">Aseta laskun summaksi 10000.</span><span class="sxs-lookup"><span data-stu-id="d47bb-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="d47bb-146">Aseta tilastosummaksi 10000.</span><span class="sxs-lookup"><span data-stu-id="d47bb-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="d47bb-147">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="d47bb-147">Click Output.</span></span>
36. <span data-ttu-id="d47bb-148">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="d47bb-148">Click Report.</span></span>
37. <span data-ttu-id="d47bb-149">Valitse Toimitukset-vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="d47bb-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="d47bb-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d47bb-150">Click OK.</span></span>
    * <span data-ttu-id="d47bb-151">Tarkasta luotu tuotos ja sen yhteenvetorivit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="d47bb-152">Huomaa, että ne ovat muuttuneet ensimmäiseen ajoon verrattuna.</span><span class="sxs-lookup"><span data-stu-id="d47bb-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="d47bb-153">Tämän konfiguraation suorittaminen vianmääritystilassa kerättyjen laskenta- ja summaustietojen arvioimiseksi</span><span class="sxs-lookup"><span data-stu-id="d47bb-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="d47bb-154">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="d47bb-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d47bb-155">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="d47bb-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="d47bb-156">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="d47bb-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="d47bb-157">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="d47bb-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="d47bb-158">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="d47bb-159">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-159">Click User parameters.</span></span>
7. <span data-ttu-id="d47bb-160">Valitse Suorita vianmääritystilassa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="d47bb-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d47bb-161">Click OK.</span></span>
9. <span data-ttu-id="d47bb-162">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d47bb-162">Close the page.</span></span>
10. <span data-ttu-id="d47bb-163">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d47bb-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="d47bb-164">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="d47bb-164">Click Output.</span></span>
12. <span data-ttu-id="d47bb-165">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="d47bb-165">Click Report.</span></span>
13. <span data-ttu-id="d47bb-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d47bb-166">Click OK.</span></span>
14. <span data-ttu-id="d47bb-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d47bb-167">Close the page.</span></span>
15. <span data-ttu-id="d47bb-168">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="d47bb-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="d47bb-169">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="d47bb-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="d47bb-170">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="d47bb-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="d47bb-171">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="d47bb-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="d47bb-172">Valitse Vianmäärityslokit.</span><span class="sxs-lookup"><span data-stu-id="d47bb-172">Click Debug logs.</span></span>
    * <span data-ttu-id="d47bb-173">Huomaa, että valitun konfiguraation ajoprosessille on luotu vianmäärityslokitietue.</span><span class="sxs-lookup"><span data-stu-id="d47bb-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="d47bb-174">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="d47bb-174">Click Attach.</span></span>
21. <span data-ttu-id="d47bb-175">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="d47bb-175">Click Open.</span></span>
    * <span data-ttu-id="d47bb-176">Tarkista luotu XML-tiedosto, joka sisältää laskennan ja summauksen tiedot, jotka on kerättiin valitun konfiguraation ajon aikana.</span><span class="sxs-lookup"><span data-stu-id="d47bb-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

