---
title: Organisaation raportointihierarkian luominen
description: Tämän menettelyn avulla voit luoda organisaation raportoinnin raporttihierarkian.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3db8465c462caffeaf6bd12d17c4b61355ed8eed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208748"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="098da-103">Organisaation raportointihierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="098da-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="098da-104">Tämän menettelyn avulla voit luoda organisaation raportoinnin raporttihierarkian.</span><span class="sxs-lookup"><span data-stu-id="098da-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="098da-105">Tämän tallenteen tarkoitus on ohjata käyttäjä dimensiohierarkian läpi niin, että käyttäjä voi jatkaa, kunnes koko organisaation raportointirakenne on luotu.</span><span class="sxs-lookup"><span data-stu-id="098da-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="098da-106">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="098da-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="098da-107">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="098da-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="098da-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-108">Click New.</span></span>
3. <span data-ttu-id="098da-109">Valitse HierarchyTypeComboBox-kentässä Dimension luokitteluhierarkia.</span><span class="sxs-lookup"><span data-stu-id="098da-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="098da-110">Valitse Dimension luokitteluhierarkia.</span><span class="sxs-lookup"><span data-stu-id="098da-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="098da-111">Dimension luokitteluhierarkia -tyyppiä käytetään sääntöjen määrittämiseen ja raportointiin.</span><span class="sxs-lookup"><span data-stu-id="098da-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="098da-112">Se tukee kaikkia dimensiota, kuten kustannusobjekteja, kustannustasoja ja tilastodimensioita.</span><span class="sxs-lookup"><span data-stu-id="098da-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="098da-113">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="098da-113">Click Create.</span></span>
5. <span data-ttu-id="098da-114">Kirjoita Dimensiohierakian nimi -kenttään Organisaatio USP2.</span><span class="sxs-lookup"><span data-stu-id="098da-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="098da-115">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="098da-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="098da-116">Valitse Kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="098da-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="098da-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-117">Click Save.</span></span>
8. <span data-ttu-id="098da-118">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="098da-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="098da-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-119">Click New.</span></span>
10. <span data-ttu-id="098da-120">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="098da-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="098da-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-121">Click Save.</span></span>
12. <span data-ttu-id="098da-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-122">Click New.</span></span>
13. <span data-ttu-id="098da-123">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="098da-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="098da-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-124">Click Save.</span></span>
15. <span data-ttu-id="098da-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-125">Click New.</span></span>
16. <span data-ttu-id="098da-126">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="098da-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="098da-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-127">Click Save.</span></span>
18. <span data-ttu-id="098da-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-128">Click New.</span></span>
19. <span data-ttu-id="098da-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="098da-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="098da-130">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="098da-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="098da-131">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="098da-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="098da-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-132">Click Save.</span></span>
22. <span data-ttu-id="098da-133">Valitse puussa Oganization USP2\CEO\CEO cost centers.</span><span class="sxs-lookup"><span data-stu-id="098da-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="098da-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-134">Click New.</span></span>
24. <span data-ttu-id="098da-135">Kirjoita Solmun nimi -kenttään Alue - länsi.</span><span class="sxs-lookup"><span data-stu-id="098da-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="098da-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-136">Click Save.</span></span>
26. <span data-ttu-id="098da-137">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-137">Click New.</span></span>
27. <span data-ttu-id="098da-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="098da-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="098da-139">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="098da-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="098da-140">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="098da-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="098da-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-141">Click Save.</span></span>
30. <span data-ttu-id="098da-142">Valitse puussa Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="098da-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="098da-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-143">Click New.</span></span>
32. <span data-ttu-id="098da-144">Kirjoita Solmun nimi -kenttään Talousjohtajan kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="098da-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="098da-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-145">Click Save.</span></span>
34. <span data-ttu-id="098da-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-146">Click New.</span></span>
35. <span data-ttu-id="098da-147">Kirjoita Solmun nimi -kenttään Markkinointikampanja.</span><span class="sxs-lookup"><span data-stu-id="098da-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="098da-148">Kirjoita Solmun nimi -kenttään Markkinointikampanja.</span><span class="sxs-lookup"><span data-stu-id="098da-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="098da-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-149">Click Save.</span></span>
38. <span data-ttu-id="098da-150">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-150">Click New.</span></span>
39. <span data-ttu-id="098da-151">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="098da-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="098da-152">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="098da-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="098da-153">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="098da-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="098da-154">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-154">Click Save.</span></span>
42. <span data-ttu-id="098da-155">Valitse puussa Organization USP2\CEO\CFO cost centers.</span><span class="sxs-lookup"><span data-stu-id="098da-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="098da-156">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-156">Click New.</span></span>
44. <span data-ttu-id="098da-157">Kirjoita Solmun nimi -kenttään Messut.</span><span class="sxs-lookup"><span data-stu-id="098da-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="098da-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-158">Click Save.</span></span>
46. <span data-ttu-id="098da-159">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-159">Click New.</span></span>
47. <span data-ttu-id="098da-160">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="098da-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="098da-161">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="098da-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="098da-162">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="098da-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="098da-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-163">Click Save.</span></span>
50. <span data-ttu-id="098da-164">Valitse puussa Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="098da-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="098da-165">Kirjoita Solmun nimi -kenttään Tietohallintojohtajan kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="098da-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="098da-166">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-166">Click Save.</span></span>
53. <span data-ttu-id="098da-167">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-167">Click New.</span></span>
54. <span data-ttu-id="098da-168">Kirjoita Solmun nimi -kenttään Puhelinkeskukset.</span><span class="sxs-lookup"><span data-stu-id="098da-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="098da-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-169">Click Save.</span></span>
56. <span data-ttu-id="098da-170">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="098da-170">Click New.</span></span>
57. <span data-ttu-id="098da-171">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="098da-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="098da-172">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="098da-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="098da-173">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="098da-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="098da-174">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="098da-174">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]