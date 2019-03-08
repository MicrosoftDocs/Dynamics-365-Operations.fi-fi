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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "365497"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="9d99d-103">Organisaation raportointihierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="9d99d-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d99d-104">Tämän menettelyn avulla voit luoda organisaation raportoinnin raporttihierarkian.</span><span class="sxs-lookup"><span data-stu-id="9d99d-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="9d99d-105">Tämän tallenteen tarkoitus on ohjata käyttäjä dimensiohierarkian läpi niin, että käyttäjä voi jatkaa, kunnes koko organisaation raportointirakenne on luotu.</span><span class="sxs-lookup"><span data-stu-id="9d99d-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="9d99d-106">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="9d99d-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="9d99d-107">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="9d99d-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="9d99d-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-108">Click New.</span></span>
3. <span data-ttu-id="9d99d-109">Valitse HierarchyTypeComboBox-kentässä Dimension luokitteluhierarkia.</span><span class="sxs-lookup"><span data-stu-id="9d99d-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="9d99d-110">Valitse Dimension luokitteluhierarkia.</span><span class="sxs-lookup"><span data-stu-id="9d99d-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="9d99d-111">Dimension luokitteluhierarkia -tyyppiä käytetään sääntöjen määrittämiseen ja raportointiin.</span><span class="sxs-lookup"><span data-stu-id="9d99d-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="9d99d-112">Se tukee kaikkia dimensiota, kuten kustannusobjekteja, kustannustasoja ja tilastodimensioita.</span><span class="sxs-lookup"><span data-stu-id="9d99d-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="9d99d-113">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="9d99d-113">Click Create.</span></span>
5. <span data-ttu-id="9d99d-114">Kirjoita Dimensiohierakian nimi -kenttään Organisaatio USP2.</span><span class="sxs-lookup"><span data-stu-id="9d99d-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="9d99d-115">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d99d-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="9d99d-116">Valitse Kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="9d99d-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="9d99d-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-117">Click Save.</span></span>
8. <span data-ttu-id="9d99d-118">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="9d99d-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="9d99d-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-119">Click New.</span></span>
10. <span data-ttu-id="9d99d-120">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="9d99d-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="9d99d-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-121">Click Save.</span></span>
12. <span data-ttu-id="9d99d-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-122">Click New.</span></span>
13. <span data-ttu-id="9d99d-123">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="9d99d-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="9d99d-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-124">Click Save.</span></span>
15. <span data-ttu-id="9d99d-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-125">Click New.</span></span>
16. <span data-ttu-id="9d99d-126">Kirjoita Solmun nimi -kenttään Toimitusjohtaja.</span><span class="sxs-lookup"><span data-stu-id="9d99d-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="9d99d-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-127">Click Save.</span></span>
18. <span data-ttu-id="9d99d-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-128">Click New.</span></span>
19. <span data-ttu-id="9d99d-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9d99d-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="9d99d-130">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d99d-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9d99d-131">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="9d99d-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="9d99d-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-132">Click Save.</span></span>
22. <span data-ttu-id="9d99d-133">Valitse puussa Oganization USP2\CEO\CEO cost centers.</span><span class="sxs-lookup"><span data-stu-id="9d99d-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="9d99d-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-134">Click New.</span></span>
24. <span data-ttu-id="9d99d-135">Kirjoita Solmun nimi -kenttään Alue - länsi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="9d99d-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-136">Click Save.</span></span>
26. <span data-ttu-id="9d99d-137">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-137">Click New.</span></span>
27. <span data-ttu-id="9d99d-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9d99d-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="9d99d-139">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d99d-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9d99d-140">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="9d99d-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="9d99d-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-141">Click Save.</span></span>
30. <span data-ttu-id="9d99d-142">Valitse puussa Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="9d99d-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="9d99d-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-143">Click New.</span></span>
32. <span data-ttu-id="9d99d-144">Kirjoita Solmun nimi -kenttään Talousjohtajan kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="9d99d-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="9d99d-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-145">Click Save.</span></span>
34. <span data-ttu-id="9d99d-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-146">Click New.</span></span>
35. <span data-ttu-id="9d99d-147">Kirjoita Solmun nimi -kenttään Markkinointikampanja.</span><span class="sxs-lookup"><span data-stu-id="9d99d-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="9d99d-148">Kirjoita Solmun nimi -kenttään Markkinointikampanja.</span><span class="sxs-lookup"><span data-stu-id="9d99d-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="9d99d-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-149">Click Save.</span></span>
38. <span data-ttu-id="9d99d-150">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-150">Click New.</span></span>
39. <span data-ttu-id="9d99d-151">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9d99d-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="9d99d-152">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d99d-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9d99d-153">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="9d99d-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="9d99d-154">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-154">Click Save.</span></span>
42. <span data-ttu-id="9d99d-155">Valitse puussa Organization USP2\CEO\CFO cost centers.</span><span class="sxs-lookup"><span data-stu-id="9d99d-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="9d99d-156">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-156">Click New.</span></span>
44. <span data-ttu-id="9d99d-157">Kirjoita Solmun nimi -kenttään Messut.</span><span class="sxs-lookup"><span data-stu-id="9d99d-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="9d99d-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-158">Click Save.</span></span>
46. <span data-ttu-id="9d99d-159">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-159">Click New.</span></span>
47. <span data-ttu-id="9d99d-160">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9d99d-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="9d99d-161">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d99d-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9d99d-162">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="9d99d-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="9d99d-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-163">Click Save.</span></span>
50. <span data-ttu-id="9d99d-164">Valitse puussa Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="9d99d-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="9d99d-165">Kirjoita Solmun nimi -kenttään Tietohallintojohtajan kustannuspaikat.</span><span class="sxs-lookup"><span data-stu-id="9d99d-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="9d99d-166">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-166">Click Save.</span></span>
53. <span data-ttu-id="9d99d-167">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-167">Click New.</span></span>
54. <span data-ttu-id="9d99d-168">Kirjoita Solmun nimi -kenttään Puhelinkeskukset.</span><span class="sxs-lookup"><span data-stu-id="9d99d-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="9d99d-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-169">Click Save.</span></span>
56. <span data-ttu-id="9d99d-170">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d99d-170">Click New.</span></span>
57. <span data-ttu-id="9d99d-171">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9d99d-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="9d99d-172">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9d99d-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9d99d-173">Valitse solmua vastaava dimension jäsen.</span><span class="sxs-lookup"><span data-stu-id="9d99d-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="9d99d-174">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d99d-174">Click Save.</span></span>

