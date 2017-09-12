--- 
title: "Tietomallin yhdistäminen valittuihin tietolähteisiin sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää sähköisen raportoinnin (ER) tietomallin valittuihin Dynamics 365 for Finance and Operations, Enterprise Editionin tietolähteisiin."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96974d7c1597db4ac31168be40cecbc7e12d6edd
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="f7741-103">Tietomallin yhdistäminen valittuihin tietolähteisiin sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="f7741-103">Map a data model to selected data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7741-104">Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää sähköisen raportoinnin (ER) tietomallin valittuihin Dynamics 365 for Finance and Operations, Enterprise Editionin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="f7741-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="f7741-105">Tätä malliyhdistämismääritystä käytetään myöhemmin tietolähteenä sähköisten maksuasiakirjojen hallinnan muotokonfiguraatiossa.</span><span class="sxs-lookup"><span data-stu-id="f7741-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="f7741-106">Tässä esimerkissä yhdistetään Litware, Inc. -esimerkkiyrityksen tietomalli tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="f7741-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="f7741-107">Voit tehdä nämä vaiheet, jos Valitse tietomallit mallin yhdistämismääritystä varten -menettelyn vaiheet on jo tehty.</span><span class="sxs-lookup"><span data-stu-id="f7741-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="f7741-108">ER-konfiguraatioiden puurakenteen avaaminen</span><span class="sxs-lookup"><span data-stu-id="f7741-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="f7741-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="f7741-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f7741-110">Valitse Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="f7741-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="f7741-111">Luodun malliyhdistämisvastaavuuden valitseminen</span><span class="sxs-lookup"><span data-stu-id="f7741-111">Select created model mapping</span></span>
1. <span data-ttu-id="f7741-112">Valitse puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="f7741-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="f7741-113">Varmista, että Maksut (yksinkertaistettu malli) -mallikonfiguraatio on luotu etukäteen.</span><span class="sxs-lookup"><span data-stu-id="f7741-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="f7741-114">Pysähdy muussa tapauksessa ja palaa Uuden määrityksen luonti valitun toimialueen tietomallilla -tehtäväoppaan suorittamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f7741-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="f7741-115">Valitse Mallin suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="f7741-115">Click Model designer.</span></span>
3. <span data-ttu-id="f7741-116">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="f7741-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="f7741-117">Valitse Tilisiirron yhdistämismääritys -tietue.</span><span class="sxs-lookup"><span data-stu-id="f7741-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="f7741-118">Tilisiirron yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="f7741-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="f7741-119">Luotujen tietolähteiden sitominen tietomallielementteihin</span><span class="sxs-lookup"><span data-stu-id="f7741-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="f7741-120">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="f7741-120">Click Designer.</span></span>
2. <span data-ttu-id="f7741-121">Valitse puussa solmu Processing date & time(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="f7741-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="f7741-122">Valitse puussa solmu Processing date(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="f7741-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="f7741-123">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-123">Click Bind.</span></span>
5. <span data-ttu-id="f7741-124">Valitse puussa solmu Payment message identification(MessageIdentification).</span><span class="sxs-lookup"><span data-stu-id="f7741-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="f7741-125">Laajenna puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="f7741-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="f7741-126">Valitse puussa solmu Transactions\Journal batch number(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="f7741-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="f7741-127">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-127">Click Bind.</span></span>
9. <span data-ttu-id="f7741-128">Valitse puussa solmu Payments.</span><span class="sxs-lookup"><span data-stu-id="f7741-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="f7741-129">Valitse puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="f7741-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="f7741-130">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-130">Click Bind.</span></span>
12. <span data-ttu-id="f7741-131">Laajenna puussa solmu Payments= Transactions.</span><span class="sxs-lookup"><span data-stu-id="f7741-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="f7741-132">Laajenna puussa solmu Payments= Transactions\Creditor.</span><span class="sxs-lookup"><span data-stu-id="f7741-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="f7741-133">Laajenna puussa solmu Payments= Transactions\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="f7741-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="f7741-134">Valitse puussa solmu Payments= Transactions\Creditor\Account\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="f7741-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="f7741-135">Laajenna puussa solmu Transactions\vendBankAccountInTransactionCompany().</span><span class="sxs-lookup"><span data-stu-id="f7741-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="f7741-136">Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="f7741-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="f7741-137">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-137">Click Bind.</span></span>
19. <span data-ttu-id="f7741-138">Valitse puussa solmu Payments= Transactions\Creditor\Account\IBAN code(IBAN).</span><span class="sxs-lookup"><span data-stu-id="f7741-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="f7741-139">Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).</span><span class="sxs-lookup"><span data-stu-id="f7741-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="f7741-140">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-140">Click Bind.</span></span>
22. <span data-ttu-id="f7741-141">Valitse puussa solmu Payments= Transactions\Creditor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="f7741-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="f7741-142">Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="f7741-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="f7741-143">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-143">Click Bind.</span></span>
25. <span data-ttu-id="f7741-144">Valitse puussa solmu Payments= Transactions\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="f7741-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="f7741-145">Valitse puussa solmu Payments= Transactions\Creditor\Agent\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="f7741-146">Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="f7741-147">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-147">Click Bind.</span></span>
29. <span data-ttu-id="f7741-148">Valitse puussa solmu Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="f7741-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="f7741-149">Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="f7741-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="f7741-150">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-150">Click Bind.</span></span>
32. <span data-ttu-id="f7741-151">Valitse puussa solmu Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="f7741-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="f7741-152">Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="f7741-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="f7741-153">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-153">Click Bind.</span></span>
35. <span data-ttu-id="f7741-154">Valitse puussa solmu Payments= Transactions\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="f7741-155">Laajenna puussa solmu Transactions\findVendTable().</span><span class="sxs-lookup"><span data-stu-id="f7741-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="f7741-156">Valitse puussa solmu Transactions\findVendTable()\name().</span><span class="sxs-lookup"><span data-stu-id="f7741-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="f7741-157">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-157">Click Bind.</span></span>
39. <span data-ttu-id="f7741-158">Valitse puussa solmu Payments= Transactions\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="f7741-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="f7741-159">Laajenna puussa Transactions\>Relations.</span><span class="sxs-lookup"><span data-stu-id="f7741-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="f7741-160">Laajenna puussa Transactions\>Relations\Currency table(Currency).</span><span class="sxs-lookup"><span data-stu-id="f7741-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="f7741-161">Valitse puussa Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO).</span><span class="sxs-lookup"><span data-stu-id="f7741-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="f7741-162">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-162">Click Bind.</span></span>
44. <span data-ttu-id="f7741-163">Laajenna puussa solmu Payments= Transactions\Debtor.</span><span class="sxs-lookup"><span data-stu-id="f7741-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="f7741-164">Laajenna puussa solmu Payments= Transactions\Debtor\Account.</span><span class="sxs-lookup"><span data-stu-id="f7741-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="f7741-165">Valitse puussa solmu Payments= Transactions\Debtor\Account\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="f7741-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="f7741-166">Valitse puussa solmu Bank Account(BankAccount).</span><span class="sxs-lookup"><span data-stu-id="f7741-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="f7741-167">Valitse puussa solmu Bank Account(BankAccount).</span><span class="sxs-lookup"><span data-stu-id="f7741-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="f7741-168">Valitse puussa solmu Bank Account(BankAccount)\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="f7741-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="f7741-169">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-169">Click Bind.</span></span>
51. <span data-ttu-id="f7741-170">Valitse puussa solmu Bank Account(BankAccount)\IBAN.</span><span class="sxs-lookup"><span data-stu-id="f7741-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="f7741-171">Valitse puussa solmu Payments= Transactions\Debtor\Account\IBAN code(IBAN).</span><span class="sxs-lookup"><span data-stu-id="f7741-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="f7741-172">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-172">Click Bind.</span></span>
54. <span data-ttu-id="f7741-173">Valitse puussa solmu Payments= Transactions\Debtor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="f7741-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="f7741-174">Valitse puussa solmu Bank Account(BankAccount)\Bank account number(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="f7741-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="f7741-175">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-175">Click Bind.</span></span>
57. <span data-ttu-id="f7741-176">Laajenna puussa solmu Payments= Transactions\Debtor\Agent.</span><span class="sxs-lookup"><span data-stu-id="f7741-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="f7741-177">Valitse puussa solmu Payments= Transactions\Debtor\Agent\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="f7741-178">Valitse puussa solmu Bank Account(BankAccount)\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="f7741-179">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-179">Click Bind.</span></span>
61. <span data-ttu-id="f7741-180">Valitse puussa solmu Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="f7741-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="f7741-181">Valitse puussa solmu Bank Account(BankAccount)\Routing number(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="f7741-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="f7741-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-182">Click Bind.</span></span>
64. <span data-ttu-id="f7741-183">Valitse puussa solmu Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="f7741-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="f7741-184">Valitse puussa solmu Bank Account(BankAccount)\SWIFT code(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="f7741-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="f7741-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-185">Click Bind.</span></span>
67. <span data-ttu-id="f7741-186">Valitse puussa solmu Payments= Transactions\Debtor\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="f7741-187">Valitse puussa solmu Company information(Company).</span><span class="sxs-lookup"><span data-stu-id="f7741-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="f7741-188">Laajenna puussa solmu Company information(Company).</span><span class="sxs-lookup"><span data-stu-id="f7741-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="f7741-189">Valitse puussa solmu Company information(Company)\Name.</span><span class="sxs-lookup"><span data-stu-id="f7741-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="f7741-190">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-190">Click Bind.</span></span>
72. <span data-ttu-id="f7741-191">Valitse puussa solmu Payments= Transactions\Description.</span><span class="sxs-lookup"><span data-stu-id="f7741-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="f7741-192">Valitse puussa solmu Transactions\Description(Txt).</span><span class="sxs-lookup"><span data-stu-id="f7741-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="f7741-193">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-193">Click Bind.</span></span>
75. <span data-ttu-id="f7741-194">Valitse puussa solmu Payments= Transactions\End to end identification code(End2EndID).</span><span class="sxs-lookup"><span data-stu-id="f7741-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="f7741-195">Laajenna puussa Transactions\$EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="f7741-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="f7741-196">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-196">Click Bind.</span></span>
78. <span data-ttu-id="f7741-197">Valitse puussa solmu Payments= Transactions\Instructed amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="f7741-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="f7741-198">Valitse puussa Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="f7741-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="f7741-199">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-199">Click Bind.</span></span>
81. <span data-ttu-id="f7741-200">Valitse puussa solmu Payments= Transactions\Transaction date(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="f7741-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="f7741-201">Valitse puussa solmu Transactions\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="f7741-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="f7741-202">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="f7741-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="f7741-203">Luodun yhdistämismäärityksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="f7741-203">Validate created mapping</span></span>
1. <span data-ttu-id="f7741-204">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="f7741-204">Click Validate.</span></span>
    * <span data-ttu-id="f7741-205">Varmista, että kaikki sidokset ovat kunnossa tarkistamalla uudet yhdistämismääritykset.</span><span class="sxs-lookup"><span data-stu-id="f7741-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="f7741-206">Laajenna tai tiivistä Virheluettelo-osa napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="f7741-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="f7741-207">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f7741-207">Click Save.</span></span>
4. <span data-ttu-id="f7741-208">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f7741-208">Close the page.</span></span>
5. <span data-ttu-id="f7741-209">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f7741-209">Close the page.</span></span>
6. <span data-ttu-id="f7741-210">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f7741-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="f7741-211">Muuta mallikonfiguraation nykyisen version tilaa</span><span class="sxs-lookup"><span data-stu-id="f7741-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="f7741-212">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="f7741-212">Click Change status.</span></span>
    * <span data-ttu-id="f7741-213">Muuta suunnitellun mallimäärityksen tila Luonnos-tilasta Valmis-tilaan. Tällöin se on käytettävissä maksumuotoilurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="f7741-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="f7741-214">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="f7741-214">Click Complete.</span></span>
    * <span data-ttu-id="f7741-215">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="f7741-215">Select Complete.</span></span>  
3. <span data-ttu-id="f7741-216">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f7741-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f7741-217">Esimerkki: versio 1.</span><span class="sxs-lookup"><span data-stu-id="f7741-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="f7741-218">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f7741-218">Click OK.</span></span>
5. <span data-ttu-id="f7741-219">Valitse nykyisen konfiguraation valmis versio.</span><span class="sxs-lookup"><span data-stu-id="f7741-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="f7741-220">Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.</span><span class="sxs-lookup"><span data-stu-id="f7741-220">Note that the created configuration is saved as completed version 1.</span></span>  


