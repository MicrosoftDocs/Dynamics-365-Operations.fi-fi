--- 
title: "Koontilaskelmien mallin yhdistämismäärityksen konfiguraation käyttäminen tietokantatasolla (ER)"
description: "Tämä menettely sisältää tietoja siitä, miten voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 3c3558d9e25dcfd56f3306e69884528d01324cbd
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="5d19d-103">Koontilaskelmien mallin yhdistämismäärityksen konfiguraation käyttäminen tietokantatasolla (ER)</span><span class="sxs-lookup"><span data-stu-id="5d19d-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d19d-104">Tämä menettely sisältää tietoja siitä, miten voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="5d19d-105">Tässä menettelyssä luodaan konfiguraatio malliyritykselle Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5d19d-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="5d19d-106">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="5d19d-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="5d19d-107">Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="5d19d-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="5d19d-108">Voit suorittaa nämä vaiheet, jos suoritat ensin vaiheet menettelystä ER parantaa koontilaskentojen tehokkuutta suorittamalla laskennat tietokannan tasolla (Osa 1: Konfiguraatioiden valmisteleminen).</span><span class="sxs-lookup"><span data-stu-id="5d19d-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="5d19d-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="5d19d-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5d19d-110">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="5d19d-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="5d19d-111">Valitse puussa Intrastat model\Intrastat sample mapping.</span><span class="sxs-lookup"><span data-stu-id="5d19d-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="5d19d-112">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="5d19d-112">Click Designer.</span></span>
5. <span data-ttu-id="5d19d-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="5d19d-113">Click Designer.</span></span>
6. <span data-ttu-id="5d19d-114">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="5d19d-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="5d19d-115">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="5d19d-115">Click Add root.</span></span>
    * <span data-ttu-id="5d19d-116">Lisää uusi tietolähde, joka edustaa ryhmiteltäviä tietueita.</span><span class="sxs-lookup"><span data-stu-id="5d19d-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="5d19d-117">Kirjoita Nimi-kenttään Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5d19d-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="5d19d-118">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="5d19d-118">Transactions</span></span>  
9. <span data-ttu-id="5d19d-119">Syötä Taulu-kenttään Intrastat.</span><span class="sxs-lookup"><span data-stu-id="5d19d-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="5d19d-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="5d19d-120">Intrastat</span></span>  
10. <span data-ttu-id="5d19d-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5d19d-121">Click OK.</span></span>
11. <span data-ttu-id="5d19d-122">Valitse valikkopuussa Toiminnot\Ryhmittely.</span><span class="sxs-lookup"><span data-stu-id="5d19d-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="5d19d-123">Tätä tietolähteen tyyppiä käytetään uuden tietolähteen esittelemisessä suorituksen aikana ryhmätietueille sekä vaadittujen koosteiden laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="5d19d-124">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="5d19d-124">Click Add root.</span></span>
13. <span data-ttu-id="5d19d-125">Kirjoita Nimi-kenttään TransactionsGroups.</span><span class="sxs-lookup"><span data-stu-id="5d19d-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="5d19d-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="5d19d-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="5d19d-127">Napsauta Muokkaa ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-127">Click Edit group by.</span></span>
15. <span data-ttu-id="5d19d-128">Valitse puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="5d19d-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="5d19d-129">Valitse lisätty tietolähde, jonka tyyppi on Tietueluettelo ja joka edustaa ryhmiteltäviä tietueita.</span><span class="sxs-lookup"><span data-stu-id="5d19d-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="5d19d-130">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-130">Click Add field to.</span></span>
17. <span data-ttu-id="5d19d-131">Napsauta Mitä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="5d19d-131">Click What to group.</span></span>
18. <span data-ttu-id="5d19d-132">Laajenna puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="5d19d-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="5d19d-133">Valitse puussa Transactions\Direction.</span><span class="sxs-lookup"><span data-stu-id="5d19d-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="5d19d-134">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-134">Click Add field to.</span></span>
21. <span data-ttu-id="5d19d-135">Napsauta Ryhmitellyt kentät.</span><span class="sxs-lookup"><span data-stu-id="5d19d-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="5d19d-136">Valitse kenttä ja määritä ryhmittelytaso.</span><span class="sxs-lookup"><span data-stu-id="5d19d-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="5d19d-137">Tämän valinnan perusteella tietolähde palauttaa suorituksen aikana niin monta tapahtumaryhmää Intrastat-taulukkoa vastaavia suuntakoodeja löytyy.</span><span class="sxs-lookup"><span data-stu-id="5d19d-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="5d19d-138">Valitse puussa Transactions\Invoice amount(AmountMST).</span><span class="sxs-lookup"><span data-stu-id="5d19d-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="5d19d-139">Valitse kenttä, kun haluat määrittää koontilaskelman lähteen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="5d19d-140">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-140">Click Add field to.</span></span>
24. <span data-ttu-id="5d19d-141">Napsauta Koostekentät.</span><span class="sxs-lookup"><span data-stu-id="5d19d-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="5d19d-142">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="5d19d-143">Valitse Menetelmä-kentässä Summa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="5d19d-144">Valitse koontityyppi.</span><span class="sxs-lookup"><span data-stu-id="5d19d-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="5d19d-145">Kirjoita Nimi-kenttään SumOfAmountMST.</span><span class="sxs-lookup"><span data-stu-id="5d19d-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="5d19d-146">Määritä tälle koonnille nimi määritetyssä tietolähteessä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="5d19d-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5d19d-147">Click Save.</span></span>
    * <span data-ttu-id="5d19d-148">Huomaa, että Suoritus-kenttä osoittaa tämän ryhmittelyn tapahtuvan suorituksen aikana SQL-tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="5d19d-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5d19d-149">Close the page.</span></span>
30. <span data-ttu-id="5d19d-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5d19d-150">Click OK.</span></span>
31. <span data-ttu-id="5d19d-151">Laajenna puussa 'Totals'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="5d19d-152">Laajenna puussa 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="5d19d-153">Laajenna puussa TransactionsGroups\aggregated.</span><span class="sxs-lookup"><span data-stu-id="5d19d-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="5d19d-154">Valitse puussa TransactionsGroups\aggregated\SumOfAmountMST.</span><span class="sxs-lookup"><span data-stu-id="5d19d-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="5d19d-155">Valitse puussa Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded').</span><span class="sxs-lookup"><span data-stu-id="5d19d-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="5d19d-156">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="5d19d-156">Click Bind.</span></span>
    * <span data-ttu-id="5d19d-157">Tämän asetuksen perusteella tietoläde laskee AmountMST-kentän arvojen summan kaikille tapahtumaryhmille.</span><span class="sxs-lookup"><span data-stu-id="5d19d-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="5d19d-158">Tämä koontilaskelma on käytettävissä TransactionsGroups.aggregated.TotalAmount-nimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="5d19d-159">Laajenna puussa 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="5d19d-160">Valitse puussa 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="5d19d-161">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-161">Click Edit.</span></span>
40. <span data-ttu-id="5d19d-162">Napsauta Muokkaa ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-162">Click Edit group by.</span></span>
41. <span data-ttu-id="5d19d-163">Laajenna puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="5d19d-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="5d19d-164">Valitse puussa Transactions\Invoice amount(AmountMST).</span><span class="sxs-lookup"><span data-stu-id="5d19d-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="5d19d-165">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-165">Click Add field to.</span></span>
44. <span data-ttu-id="5d19d-166">Napsauta Koostekentät.</span><span class="sxs-lookup"><span data-stu-id="5d19d-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="5d19d-167">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="5d19d-168">Valitse Menetelmä-kentässä Enintään.</span><span class="sxs-lookup"><span data-stu-id="5d19d-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="5d19d-169">Kirjoita Nimi-kenttään MaxOfAmountMST.</span><span class="sxs-lookup"><span data-stu-id="5d19d-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="5d19d-170">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5d19d-170">Click Save.</span></span>
    * <span data-ttu-id="5d19d-171">Tällä hetkellä GROUPBY-tietolähteiden suoritus voidaan kääntää SQL-tietokannan tasolle tietyin rajoituksin.</span><span class="sxs-lookup"><span data-stu-id="5d19d-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="5d19d-172">Käännökset voidaan tehdä joko Tietueluettelo-tyypin tietolähteille tai FILTER-toimintoa käyttävää lauseketta edustaville tietolähteille.</span><span class="sxs-lookup"><span data-stu-id="5d19d-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="5d19d-173">Se voidaan tehdä myös, kun ryhmittelytietueiden yhdelle kentälle on määritetty yksi koonti.</span><span class="sxs-lookup"><span data-stu-id="5d19d-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="5d19d-174">Huomaa, että AmountMST-kentälle määritettiin useita koosteita, Suoritus:-kenttä ilmaisee edelleen, että tämä ryhmittely suoritetaan ajoaikana SQL-tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="5d19d-175">Tämä johtuu siitä, että vain yksi kooste on sidottu tietomallinimikkeeseen ja vain sillä noudetaan ajoaikana tietoja tästä tietolähteestä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="5d19d-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5d19d-176">Close the page.</span></span>
50. <span data-ttu-id="5d19d-177">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5d19d-177">Click OK.</span></span>
51. <span data-ttu-id="5d19d-178">Laajenna puussa 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="5d19d-179">Laajenna puussa TransactionsGroups\aggregated.</span><span class="sxs-lookup"><span data-stu-id="5d19d-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="5d19d-180">Valitse puussa TransactionsGroups\aggregated\MaxOfAmountMST.</span><span class="sxs-lookup"><span data-stu-id="5d19d-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="5d19d-181">Valitse puussa Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded').</span><span class="sxs-lookup"><span data-stu-id="5d19d-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="5d19d-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="5d19d-182">Click Bind.</span></span>
56. <span data-ttu-id="5d19d-183">Laajenna puussa 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="5d19d-184">Valitse puussa 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="5d19d-185">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-185">Click Edit.</span></span>
59. <span data-ttu-id="5d19d-186">Napsauta Muokkaa ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-186">Click Edit group by.</span></span>
    * <span data-ttu-id="5d19d-187">Huomaa, että Suoritus-kenttä osoittaa, että tämä ryhmittely tehdään suorituksen aikana muistissa, koska molemmat saman kentän koonnit on sidottu tietomallin nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="5d19d-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="5d19d-188">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5d19d-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="5d19d-189">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="5d19d-189">Click Delete.</span></span>
62. <span data-ttu-id="5d19d-190">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-190">Click Yes.</span></span>
63. <span data-ttu-id="5d19d-191">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="5d19d-191">Click Delete.</span></span>
64. <span data-ttu-id="5d19d-192">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5d19d-192">Click Yes.</span></span>
65. <span data-ttu-id="5d19d-193">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="5d19d-193">Click Add field to.</span></span>
66. <span data-ttu-id="5d19d-194">Napsauta Mitä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="5d19d-194">Click What to group.</span></span>
67. <span data-ttu-id="5d19d-195">Laajenna puussa 'Commodity record(Intrastat)'.</span><span class="sxs-lookup"><span data-stu-id="5d19d-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="5d19d-196">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5d19d-196">Click Save.</span></span>
    * <span data-ttu-id="5d19d-197">Huomaa, että Suoritus-kenttä osoittaa tämän ryhmittelyn tapahtuvan suorituksen aikana muistissa, vaikka koonteja ei ole määritetty ja valittu Taulukkotietueet-tyyppinen tietolähde viittaa samaan Intrastat-taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="5d19d-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="5d19d-198">Tämä johtuu siitä, että tietolähde sisältää joitakin laskettuja kenttiä, joita ei voi vielä kääntää SQL-tietokannan tasolle.</span><span class="sxs-lookup"><span data-stu-id="5d19d-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  

