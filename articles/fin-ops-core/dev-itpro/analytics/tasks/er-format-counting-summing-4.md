---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 4 – Muodon suorittaminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämistä aiemmin luotuun tekstiin perustuvaa laskentaa ja summien tuottamista. (Osa 4)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092944"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="19253-104">ER Määritä muoto suorittamaan laskenta ja summaus (Osa 4 – Muodon suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="19253-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19253-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="19253-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="19253-106">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="19253-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="19253-107">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 3: Käytä laskentoja tuotoksen luomiseen)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="19253-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="19253-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="19253-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="19253-109">Testaa konfiguraation Intrastat-raporttien luonti</span><span class="sxs-lookup"><span data-stu-id="19253-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="19253-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="19253-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="19253-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="19253-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="19253-112">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="19253-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="19253-113">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="19253-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="19253-114">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="19253-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="19253-115">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="19253-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="19253-116">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="19253-116">Click User parameters.</span></span>
8. <span data-ttu-id="19253-117">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="19253-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="19253-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="19253-118">Click OK.</span></span>
10. <span data-ttu-id="19253-119">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="19253-119">Click Edit.</span></span>
11. <span data-ttu-id="19253-120">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="19253-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="19253-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="19253-121">Click Save.</span></span>
13. <span data-ttu-id="19253-122">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.</span><span class="sxs-lookup"><span data-stu-id="19253-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="19253-123">Laajenna Sähköinen raportointi -osa.</span><span class="sxs-lookup"><span data-stu-id="19253-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="19253-124">Valitse Intrastat (DE) with counting & summing -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="19253-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="19253-125">Valitse Intrastat (DE) with counting & summing -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="19253-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="19253-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="19253-126">Click Save.</span></span>
18. <span data-ttu-id="19253-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="19253-127">Close the page.</span></span>
19. <span data-ttu-id="19253-128">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="19253-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="19253-129">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="19253-129">Click Output.</span></span>
21. <span data-ttu-id="19253-130">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="19253-130">Click Report.</span></span>
    * <span data-ttu-id="19253-131">Aja Intrastat-raportin luontiprosessi.</span><span class="sxs-lookup"><span data-stu-id="19253-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="19253-132">Syötä Päivämäärästä-kenttään päivämäärä 1.1.2000.</span><span class="sxs-lookup"><span data-stu-id="19253-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="19253-133">Määritä raportointikauden aloitus- ja päättymispäivämäärät, joka sisältää aiemmin luodin lomakkeen tapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="19253-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="19253-134">Lisää Päivämäärään-kenttään päivämäärä 31.12.2022.</span><span class="sxs-lookup"><span data-stu-id="19253-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="19253-135">Määritä raportointikauden aloitus- ja päättymispäivämäärät, joka sisältää aiemmin luodin lomakkeen tapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="19253-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="19253-136">Valitse Saapumiset-vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="19253-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="19253-137">Valitse Luo tiedosto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="19253-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="19253-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="19253-138">Click OK.</span></span>
    * <span data-ttu-id="19253-139">Tarkasta luotu tuotos ja sen yhteenvetorivit.</span><span class="sxs-lookup"><span data-stu-id="19253-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="19253-140">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="19253-140">Click New.</span></span>
28. <span data-ttu-id="19253-141">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="19253-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="19253-142">Valitse Toimitukset-vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="19253-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="19253-143">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="19253-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="19253-144">Syötä tai valitse arvo Kauppatavara-kentässä.</span><span class="sxs-lookup"><span data-stu-id="19253-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="19253-145">Aseta painoarvoksi 10.</span><span class="sxs-lookup"><span data-stu-id="19253-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="19253-146">Aseta laskun summaksi 10000.</span><span class="sxs-lookup"><span data-stu-id="19253-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="19253-147">Aseta tilastosummaksi 10000.</span><span class="sxs-lookup"><span data-stu-id="19253-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="19253-148">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="19253-148">Click Output.</span></span>
36. <span data-ttu-id="19253-149">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="19253-149">Click Report.</span></span>
37. <span data-ttu-id="19253-150">Valitse Toimitukset-vaihtoehto kentässä Suunta.</span><span class="sxs-lookup"><span data-stu-id="19253-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="19253-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="19253-151">Click OK.</span></span>
    * <span data-ttu-id="19253-152">Tarkasta luotu tuotos ja sen yhteenvetorivit.</span><span class="sxs-lookup"><span data-stu-id="19253-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="19253-153">Huomaa, että ne ovat muuttuneet ensimmäiseen ajoon verrattuna.</span><span class="sxs-lookup"><span data-stu-id="19253-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="19253-154">Tämän konfiguraation suorittaminen vianmääritystilassa kerättyjen laskenta- ja summaustietojen arvioimiseksi</span><span class="sxs-lookup"><span data-stu-id="19253-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="19253-155">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="19253-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="19253-156">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="19253-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="19253-157">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="19253-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="19253-158">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="19253-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="19253-159">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="19253-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="19253-160">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="19253-160">Click User parameters.</span></span>
7. <span data-ttu-id="19253-161">Valitse Suorita vianmääritystilassa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="19253-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="19253-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="19253-162">Click OK.</span></span>
9. <span data-ttu-id="19253-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="19253-163">Close the page.</span></span>
10. <span data-ttu-id="19253-164">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="19253-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="19253-165">Valitse Tulostus.</span><span class="sxs-lookup"><span data-stu-id="19253-165">Click Output.</span></span>
12. <span data-ttu-id="19253-166">Valitse Raportti.</span><span class="sxs-lookup"><span data-stu-id="19253-166">Click Report.</span></span>
13. <span data-ttu-id="19253-167">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="19253-167">Click OK.</span></span>
14. <span data-ttu-id="19253-168">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="19253-168">Close the page.</span></span>
15. <span data-ttu-id="19253-169">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="19253-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="19253-170">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="19253-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="19253-171">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="19253-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="19253-172">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="19253-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="19253-173">Valitse Vianmäärityslokit.</span><span class="sxs-lookup"><span data-stu-id="19253-173">Click Debug logs.</span></span>
    * <span data-ttu-id="19253-174">Huomaa, että valitun konfiguraation ajoprosessille on luotu vianmäärityslokitietue.</span><span class="sxs-lookup"><span data-stu-id="19253-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="19253-175">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="19253-175">Click Attach.</span></span>
21. <span data-ttu-id="19253-176">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="19253-176">Click Open.</span></span>
    * <span data-ttu-id="19253-177">Tarkista luotu XML-tiedosto, joka sisältää laskennan ja summauksen tiedot, jotka on kerättiin valitun konfiguraation ajon aikana.</span><span class="sxs-lookup"><span data-stu-id="19253-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

