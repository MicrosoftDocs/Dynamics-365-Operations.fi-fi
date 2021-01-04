---
title: Tarkistuskäytäntöjen määrittäminen lähdeasiakirjoille
description: Tässä aiheessa kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442850"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="e685d-103">Tarkistuskäytäntöjen määrittäminen lähdeasiakirjoille</span><span class="sxs-lookup"><span data-stu-id="e685d-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e685d-104">Tässä aiheessa kuvataan, miten tarkistuskäytännön säännöt määritetään ja suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="e685d-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="e685d-105">Tässä esimerkissä käytetään hotellin kululajin kuluraportteja.</span><span class="sxs-lookup"><span data-stu-id="e685d-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="e685d-106">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="e685d-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="e685d-107">Tilintarkistajan rooli sisältää näiden tehtävien suorittamisessa vaadittavat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e685d-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="e685d-108">Siirry siirtymisruudussa kohtaan **Moduulit > Tarkastustyötila > Asetukset > Käytäntösäännön tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="e685d-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="e685d-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e685d-109">Select **New**.</span></span>
3. <span data-ttu-id="e685d-110">Kirjoita arvo **Säännön nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e685d-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="e685d-111">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e685d-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e685d-112">Valitse **Kyselyn nimi** -kentässä **Kuluraportin rivi**</span><span class="sxs-lookup"><span data-stu-id="e685d-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="e685d-113">Valitse **Kyselytyyppi**-kentässä **Yhdistä**</span><span class="sxs-lookup"><span data-stu-id="e685d-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="e685d-114">Valitse **Yritys**-kentässä **Yritys**</span><span class="sxs-lookup"><span data-stu-id="e685d-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="e685d-115">Valitse **Asiakirjan päivämääräviite** -kentässä **Muokkauksen päivämäärä ja aika**</span><span class="sxs-lookup"><span data-stu-id="e685d-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="e685d-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e685d-116">Select **Save**.</span></span>
10. <span data-ttu-id="e685d-117">Siirry siirtymisruudussa kohtaan **Moduulit > Tarkastustyötila > Asetukset > Tarkistuskäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="e685d-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="e685d-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e685d-118">Select **New**.</span></span>
12. <span data-ttu-id="e685d-119">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e685d-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="e685d-120">Laajenna **Käytäntöorganisaatiot**-osa.</span><span class="sxs-lookup"><span data-stu-id="e685d-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="e685d-121">Valitse puussa solmu **Contoso Entertainment System USA** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="e685d-122">Valitse puussa solmu **Contoso Consulting USA** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="e685d-123">Valitse puussa solmu **Contoso Retail USA** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="e685d-124">Tiivistä **Käytäntöorganisaatiot**-osa.</span><span class="sxs-lookup"><span data-stu-id="e685d-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="e685d-125">Laajenna **Käytäntösäännöt**-osa.</span><span class="sxs-lookup"><span data-stu-id="e685d-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="e685d-126">Etsi ja valitse luettelosta aiemmin luotu käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="e685d-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="e685d-127">Valitse **Luo käytäntösääntö**.</span><span class="sxs-lookup"><span data-stu-id="e685d-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="e685d-128">Syötä päivämäärä ja kellonaika **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e685d-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="e685d-129">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="e685d-129">Select **Filter**.</span></span>
23. <span data-ttu-id="e685d-130">Valitse luettelosta **kululuokan** rivi ja määritä **hotellin** tiedot.</span><span class="sxs-lookup"><span data-stu-id="e685d-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="e685d-131">Anna tai valitse arvo **Ehdot**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e685d-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="e685d-132">Valitse **Yhdistelmä**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e685d-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="e685d-133">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-133">Select **Add**.</span></span>
27. <span data-ttu-id="e685d-134">Valitse luettelosta **Tapahtumasumma**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="e685d-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="e685d-135">Syötä tai valitse arvo **Kenttä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e685d-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="e685d-136">Valitse **AggregateFunction**-kentässä **Summa**.</span><span class="sxs-lookup"><span data-stu-id="e685d-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="e685d-137">Valitse **Ryhmittely**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e685d-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="e685d-138">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-138">Select **Add**.</span></span>
32. <span data-ttu-id="e685d-139">Valitse luettelosta **Työntekijä**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="e685d-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="e685d-140">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-140">Select **Add**.</span></span>
34. <span data-ttu-id="e685d-141">Valitse luettelosta **Kululuokka**-kentän arvo</span><span class="sxs-lookup"><span data-stu-id="e685d-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="e685d-142">Syötä tai valitse arvo **Kenttä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e685d-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="e685d-143">Valitse **On**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e685d-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="e685d-144">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e685d-144">Select **Add**.</span></span>
38. <span data-ttu-id="e685d-145">Valitse **Tapahtumasumma**.</span><span class="sxs-lookup"><span data-stu-id="e685d-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="e685d-146">Syötä tai valitse arvo **Kenttä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e685d-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="e685d-147">Valitse **AggregateFunction**-kentässä **Summa**.</span><span class="sxs-lookup"><span data-stu-id="e685d-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="e685d-148">Kirjoita **Ehdot**-kenttään `>2000`.</span><span class="sxs-lookup"><span data-stu-id="e685d-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="e685d-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e685d-149">Select **OK**.</span></span>
43. <span data-ttu-id="e685d-150">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="e685d-150">Select **Test**.</span></span>
44. <span data-ttu-id="e685d-151">Syötä **Asiakirjan valinnan aloituspäivämäärä** -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="e685d-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="e685d-152">Syötä **Asiakirjan valinnan lopetuspäivämäärä** -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="e685d-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="e685d-153">Valitse **Suorita testi**.</span><span class="sxs-lookup"><span data-stu-id="e685d-153">Select **Run test**.</span></span>
47. <span data-ttu-id="e685d-154">Valitse toimintoruudussa **Tarkistuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="e685d-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="e685d-155">Valitse **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="e685d-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="e685d-156">Määritä päivämäärä ja kellonaika **Aloituspäivämäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e685d-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="e685d-157">Syötä päivämäärä ja kellonaika **Päättymispäivämäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e685d-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="e685d-158">Valitse **Erä**.</span><span class="sxs-lookup"><span data-stu-id="e685d-158">Select **Batch**.</span></span>
52. <span data-ttu-id="e685d-159">Laajenna **Suorita taustalla** -osa.</span><span class="sxs-lookup"><span data-stu-id="e685d-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="e685d-160">Valitse **Eräkäsittely**-kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e685d-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="e685d-161">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e685d-161">Select **OK**.</span></span>
55. <span data-ttu-id="e685d-162">Siirry siirtymisruudussa kohtaan **Moduulit > Tarkastustyötila > Tarkistusasiat**.</span><span class="sxs-lookup"><span data-stu-id="e685d-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="e685d-163">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e685d-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="e685d-164">Laajenna **Liitokset**-osa.</span><span class="sxs-lookup"><span data-stu-id="e685d-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="e685d-165">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e685d-165">In the list, find and select the desired record.</span></span>

