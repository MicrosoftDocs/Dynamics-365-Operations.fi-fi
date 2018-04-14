--- 
title: Organisaation raportointihierarkian luominen
description: "Tämän menettelyn avulla voit luoda organisaation raportoinnin raporttihierarkian."
author: YuyuScheller
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: afac613bdf366c4abcac4ee551e2db3db041803c
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="3befb-103">Organisaation raportointihierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="3befb-103">Create an organization report hierarchy</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3befb-104">Tämän menettelyn avulla voit luoda organisaation raportoinnin raporttihierarkian.</span><span class="sxs-lookup"><span data-stu-id="3befb-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="3befb-105">Tämän tallenteen tarkoitus on ohjata käyttäjä dimensiohierarkian läpi niin, että käyttäjä voi jatkaa, kunnes koko organisaation raportointirakenne on luotu.</span><span class="sxs-lookup"><span data-stu-id="3befb-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="3befb-106">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="3befb-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="3befb-107">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="3befb-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="3befb-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-108">Click New.</span></span>
3. <span data-ttu-id="3befb-109">Valitse HierarchyTypeComboBox-kentässä Dimension luokitteluhierarkia.</span><span class="sxs-lookup"><span data-stu-id="3befb-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="3befb-110">Valitse Dimension luokitteluhierarkia.</span><span class="sxs-lookup"><span data-stu-id="3befb-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="3befb-111">Dimension luokitteluhierarkia -tyyppiä käytetään sääntöjen määrittämiseen ja raportointiin.</span><span class="sxs-lookup"><span data-stu-id="3befb-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="3befb-112">Se tukee kaikkia dimensiota, kuten kustannusobjekteja, kustannustasoja ja tilastodimensioita.</span><span class="sxs-lookup"><span data-stu-id="3befb-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="3befb-113">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="3befb-113">Click Create.</span></span>
5. <span data-ttu-id="3befb-114">Kirjoita Dimensiohierakian nimi -kenttään Organisaatio USP2.</span><span class="sxs-lookup"><span data-stu-id="3befb-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="3befb-115">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3befb-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="3befb-116">Valitse Kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="3befb-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="3befb-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-117">Click Save.</span></span>
8. <span data-ttu-id="3befb-118">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="3befb-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="3befb-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-119">Click New.</span></span>
10. <span data-ttu-id="3befb-120">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="3befb-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="3befb-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-121">Click Save.</span></span>
12. <span data-ttu-id="3befb-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-122">Click New.</span></span>
13. <span data-ttu-id="3befb-123">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="3befb-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="3befb-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-124">Click Save.</span></span>
15. <span data-ttu-id="3befb-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-125">Click New.</span></span>
16. <span data-ttu-id="3befb-126">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="3befb-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="3befb-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-127">Click Save.</span></span>
18. <span data-ttu-id="3befb-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-128">Click New.</span></span>
19. <span data-ttu-id="3befb-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3befb-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="3befb-130">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3befb-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3befb-131">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="3befb-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="3befb-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-132">Click Save.</span></span>
22. <span data-ttu-id="3befb-133">Valitse puussa Oganization USP2\CEO\CEO cost centers.</span><span class="sxs-lookup"><span data-stu-id="3befb-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="3befb-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-134">Click New.</span></span>
24. <span data-ttu-id="3befb-135">Kirjoita Solmun nimi -kenttään Alue - länsi.</span><span class="sxs-lookup"><span data-stu-id="3befb-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="3befb-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-136">Click Save.</span></span>
26. <span data-ttu-id="3befb-137">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-137">Click New.</span></span>
27. <span data-ttu-id="3befb-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3befb-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="3befb-139">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3befb-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3befb-140">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="3befb-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="3befb-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-141">Click Save.</span></span>
30. <span data-ttu-id="3befb-142">Valitse puussa Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="3befb-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="3befb-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-143">Click New.</span></span>
32. <span data-ttu-id="3befb-144">Kirjoita Solmun nimi -kenttään Talousjohtajan kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="3befb-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="3befb-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-145">Click Save.</span></span>
34. <span data-ttu-id="3befb-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-146">Click New.</span></span>
35. <span data-ttu-id="3befb-147">Kirjoita Solmun nimi -kenttään Markkinointikampanja.</span><span class="sxs-lookup"><span data-stu-id="3befb-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="3befb-148">Kirjoita Solmun nimi -kenttään Markkinointikampanja.</span><span class="sxs-lookup"><span data-stu-id="3befb-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="3befb-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-149">Click Save.</span></span>
38. <span data-ttu-id="3befb-150">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-150">Click New.</span></span>
39. <span data-ttu-id="3befb-151">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3befb-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="3befb-152">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3befb-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3befb-153">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="3befb-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="3befb-154">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-154">Click Save.</span></span>
42. <span data-ttu-id="3befb-155">Valitse puussa Organization USP2\CEO\CFO cost centers.</span><span class="sxs-lookup"><span data-stu-id="3befb-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="3befb-156">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-156">Click New.</span></span>
44. <span data-ttu-id="3befb-157">Kirjoita Solmun nimi -kenttään Messut.</span><span class="sxs-lookup"><span data-stu-id="3befb-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="3befb-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-158">Click Save.</span></span>
46. <span data-ttu-id="3befb-159">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-159">Click New.</span></span>
47. <span data-ttu-id="3befb-160">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3befb-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="3befb-161">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3befb-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3befb-162">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="3befb-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="3befb-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-163">Click Save.</span></span>
50. <span data-ttu-id="3befb-164">Valitse puussa Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="3befb-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="3befb-165">Kirjoita Solmun nimi -kenttään Tietohallintojohtajan kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="3befb-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="3befb-166">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-166">Click Save.</span></span>
53. <span data-ttu-id="3befb-167">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-167">Click New.</span></span>
54. <span data-ttu-id="3befb-168">Kirjoita Solmun nimi -kenttään Puhelinkeskukset.</span><span class="sxs-lookup"><span data-stu-id="3befb-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="3befb-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-169">Click Save.</span></span>
56. <span data-ttu-id="3befb-170">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3befb-170">Click New.</span></span>
57. <span data-ttu-id="3befb-171">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3befb-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="3befb-172">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3befb-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3befb-173">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="3befb-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="3befb-174">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3befb-174">Click Save.</span></span>


