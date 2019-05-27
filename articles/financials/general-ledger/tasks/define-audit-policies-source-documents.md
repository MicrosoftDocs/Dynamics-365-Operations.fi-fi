---
title: Määritä tarkistuskäytännöt lähdeasiakirjoille
description: Tässä menettelyssä kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558880"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="601b0-103">Määritä tarkistuskäytännöt lähdeasiakirjoille</span><span class="sxs-lookup"><span data-stu-id="601b0-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="601b0-104">Tässä menettelyssä kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="601b0-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="601b0-105">Tässä esimerkissä käytetään hotellin kululajin kuluraportteja.</span><span class="sxs-lookup"><span data-stu-id="601b0-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="601b0-106">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="601b0-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="601b0-107">Tilintarkistajan rooli sisältää näiden tehtävien suorittamisessa vaadittavat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="601b0-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="601b0-108">Siirry kohtaan Tarkastustyötila > Asetukset > Käytäntösäännön tyyppi.</span><span class="sxs-lookup"><span data-stu-id="601b0-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="601b0-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="601b0-109">Click New.</span></span>
3. <span data-ttu-id="601b0-110">Kirjoita arvo Säännön nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="601b0-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="601b0-112">Valitse kuluraportin rivillä Kyselyn nimi -kenttä</span><span class="sxs-lookup"><span data-stu-id="601b0-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="601b0-113">Valitse Kyselytyyppi-kentässä Yhdistä</span><span class="sxs-lookup"><span data-stu-id="601b0-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="601b0-114">Valitse Yritys-kentässä Yritys</span><span class="sxs-lookup"><span data-stu-id="601b0-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="601b0-115">Valitse Asiakirjan päivämääräviite -kentässä Muokkauksen päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="601b0-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="601b0-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="601b0-116">Click Save.</span></span>
10. <span data-ttu-id="601b0-117">Siirry kohtaan Tarkastustyötila > Asetukset > Tarkistuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="601b0-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="601b0-118">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="601b0-118">Click New.</span></span>
12. <span data-ttu-id="601b0-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="601b0-120">Laajenna Käytäntöorganisaatiot-osa.</span><span class="sxs-lookup"><span data-stu-id="601b0-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="601b0-121">Valitse puussa solmu Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="601b0-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="601b0-122">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-122">Click Add.</span></span>
16. <span data-ttu-id="601b0-123">Valitse puussa solmu Contoso Consulting USA.</span><span class="sxs-lookup"><span data-stu-id="601b0-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="601b0-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-124">Click Add.</span></span>
18. <span data-ttu-id="601b0-125">Valitse puussa solmu Contoso Retail USA.</span><span class="sxs-lookup"><span data-stu-id="601b0-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="601b0-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-126">Click Add.</span></span>
20. <span data-ttu-id="601b0-127">Tiivistä Käytäntöorganisaatiot-osa.</span><span class="sxs-lookup"><span data-stu-id="601b0-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="601b0-128">Laajenna Käytäntösäännöt-osa.</span><span class="sxs-lookup"><span data-stu-id="601b0-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="601b0-129">Etsi ja valitse luettelosta aiemmin luotu käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="601b0-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="601b0-130">Valitse Luo käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="601b0-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="601b0-131">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="601b0-132">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="601b0-132">Click Filter.</span></span>
26. <span data-ttu-id="601b0-133">Valitse luettelosta kululuokan rivi ja määritä hotellin tiedot</span><span class="sxs-lookup"><span data-stu-id="601b0-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="601b0-134">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="601b0-135">Valitse Yhdistä-välilehti.</span><span class="sxs-lookup"><span data-stu-id="601b0-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="601b0-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-136">Click Add.</span></span>
30. <span data-ttu-id="601b0-137">Valitse luettelosta tapahtumasumman kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="601b0-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="601b0-138">Syötä tai valitse arvo Kenttä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="601b0-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="601b0-139">Valitse AggregateFunction-kentässä Summa.</span><span class="sxs-lookup"><span data-stu-id="601b0-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="601b0-140">Valitse Ryhmittely-välilehti.</span><span class="sxs-lookup"><span data-stu-id="601b0-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="601b0-141">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-141">Click Add.</span></span>
35. <span data-ttu-id="601b0-142">Valitse luettelosta työntekijän arvo </span><span class="sxs-lookup"><span data-stu-id="601b0-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="601b0-143">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-143">Click Add.</span></span>
37. <span data-ttu-id="601b0-144">Valitse luettelosta työntekijäluokan arvo</span><span class="sxs-lookup"><span data-stu-id="601b0-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="601b0-145">Syötä tai valitse arvo Kenttä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="601b0-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="601b0-146">Valitse On-välilehti.</span><span class="sxs-lookup"><span data-stu-id="601b0-146">Click the Having tab.</span></span>
40. <span data-ttu-id="601b0-147">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="601b0-147">Click Add.</span></span>
41. <span data-ttu-id="601b0-148">Valitse tapahtumasumma</span><span class="sxs-lookup"><span data-stu-id="601b0-148">Select Transaction amount</span></span>
42. <span data-ttu-id="601b0-149">Syötä tai valitse arvo Kenttä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="601b0-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="601b0-150">Valitse AggregateFunction-kentässä Summa.</span><span class="sxs-lookup"><span data-stu-id="601b0-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="601b0-151">Kirjoita Ehdot-kenttään > 2 000.</span><span class="sxs-lookup"><span data-stu-id="601b0-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="601b0-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="601b0-152">Click OK.</span></span>
46. <span data-ttu-id="601b0-153">Valitse Testi.</span><span class="sxs-lookup"><span data-stu-id="601b0-153">Click Test.</span></span>
47. <span data-ttu-id="601b0-154">Syötä Asiakirjan valinnan aloituspäivämäärä -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="601b0-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="601b0-155">Syötä Asiakirjan valinnan lopetuspäivämäärä -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="601b0-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="601b0-156">Valitse Suorita testi.</span><span class="sxs-lookup"><span data-stu-id="601b0-156">Click Run test.</span></span>
50. <span data-ttu-id="601b0-157">Valitse toimintoruudussa Tarkistuskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="601b0-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="601b0-158">Valitse Lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="601b0-158">Click Additional options.</span></span>
52. <span data-ttu-id="601b0-159">Määritä päivämäärä ja kellonaika Aloituspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="601b0-160">Syötä päivämäärä ja kellonaika Päättymispäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="601b0-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="601b0-161">Valitse erä.</span><span class="sxs-lookup"><span data-stu-id="601b0-161">Click Batch.</span></span>
55. <span data-ttu-id="601b0-162">Laajenna Suorita taustalla -osa.</span><span class="sxs-lookup"><span data-stu-id="601b0-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="601b0-163">Valitse Eräkäsittely-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="601b0-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="601b0-164">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="601b0-164">Click OK.</span></span>
58. <span data-ttu-id="601b0-165">Siirry kohtaan Tarkastustyötila > Tarkistustapaukset</span><span class="sxs-lookup"><span data-stu-id="601b0-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="601b0-166">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="601b0-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="601b0-167">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="601b0-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="601b0-168">Laajenna Liitokset-osa.</span><span class="sxs-lookup"><span data-stu-id="601b0-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="601b0-169">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="601b0-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="601b0-170">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="601b0-170">In the list, click the link in the selected row.</span></span>

