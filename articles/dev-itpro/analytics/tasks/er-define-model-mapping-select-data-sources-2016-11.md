---
title: Määritä ER-mallin yhdistämismääritys ja valitse niille tietolähteet
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi valita sähköisen raportoinnin tietomallille tietolähteitä.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5f2f2c699514d723f42f5d1fb25724f46dfc4f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "348868"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="737ee-103">Määritä ER-mallin yhdistämismääritys ja valitse niille tietolähteet</span><span class="sxs-lookup"><span data-stu-id="737ee-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="737ee-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi valita sähköisen raportoinnin (ER) tietomallille tietolähteitä.</span><span class="sxs-lookup"><span data-stu-id="737ee-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="737ee-105">Tietolähteet sidotaan valittujen tietomallien yksittäisiin komponentteihin suunnittelun yhteydessä. Tietomallin liiketoimintatiedot täytetään suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="737ee-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="737ee-106">Tässä esimerkissä valitaan Litware, Inc. -malliyritykselle aiemmin luodun tietomallin tietolähteet. Voit suorittaa nämä vaiheet, jos Luo uusi tietomalli -menettelyn vaiheet ovat valmiit.</span><span class="sxs-lookup"><span data-stu-id="737ee-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="737ee-107">Sähköinen raportointi -määritysten puurakenteen avaaminen</span><span class="sxs-lookup"><span data-stu-id="737ee-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="737ee-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="737ee-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="737ee-109">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="737ee-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="737ee-110">Uuden malliyhdistämismäärityksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="737ee-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="737ee-111">Valitse puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="737ee-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="737ee-112">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="737ee-112">Click Designer.</span></span>
3. <span data-ttu-id="737ee-113">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="737ee-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="737ee-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="737ee-114">Click New.</span></span>
    * <span data-ttu-id="737ee-115">Näin luodaan uusi tietue, joka yhdistää tietomallin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="737ee-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="737ee-116">Tässä esimerkissä tietomalli yhdistetään halutun maksutyypin eli tilisiirron tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="737ee-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="737ee-117">Tietylle tietomallille voidaan suunnitella useita yhdistämismäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="737ee-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="737ee-118">Voit luoda yhdistämismäärityksen esimerkiksi erityyppisille maksuille, kuten suoraveloitukselle tai tilisiirroille.</span><span class="sxs-lookup"><span data-stu-id="737ee-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="737ee-119">Tässä esimerkissä luodaan tilisiirtojen yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="737ee-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="737ee-120">Syötä Nimi-kenttään Tilisiirron yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="737ee-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="737ee-121">Tilisiirron yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="737ee-121">CT mapping</span></span>  
6. <span data-ttu-id="737ee-122">Syötä Kuvaus-kenttään Maksumallin yhdistämismääritys, tilisiirto.</span><span class="sxs-lookup"><span data-stu-id="737ee-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="737ee-123">Maksumallin yhdistämismääritys, tilisiirto</span><span class="sxs-lookup"><span data-stu-id="737ee-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="737ee-124">Kirjoita Kuvaus-kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="737ee-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="737ee-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="737ee-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="737ee-126">ResolveChanges, määritelmä.</span><span class="sxs-lookup"><span data-stu-id="737ee-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="737ee-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="737ee-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="737ee-128">Pakollisten tietolähteiden määrittäminen nykyiselle malliyhdistämismääritykselle</span><span class="sxs-lookup"><span data-stu-id="737ee-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="737ee-129">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="737ee-129">Click Designer.</span></span>
2. <span data-ttu-id="737ee-130">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="737ee-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="737ee-131">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="737ee-131">Click Add root.</span></span>
    * <span data-ttu-id="737ee-132">Syötä tämä tietolähde, kun haluat käyttää maksutapahtumia.</span><span class="sxs-lookup"><span data-stu-id="737ee-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="737ee-133">Kirjoita Nimi-kenttään Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="737ee-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="737ee-134">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="737ee-134">Transactions</span></span>  
5. <span data-ttu-id="737ee-135">Syötä Etiketti-kenttään Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="737ee-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="737ee-136">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="737ee-136">Transactions</span></span>  
6. <span data-ttu-id="737ee-137">Syötä Ohje-kenttään Kirjanpidon kirjauskansion rivit.</span><span class="sxs-lookup"><span data-stu-id="737ee-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="737ee-138">Kirjanpidon kirjauskansiorivit</span><span class="sxs-lookup"><span data-stu-id="737ee-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="737ee-139">Valitse Kysy kyselyä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="737ee-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="737ee-140">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="737ee-140">Select Yes.</span></span>  
8. <span data-ttu-id="737ee-141">Syötä Taulu-kenttään LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="737ee-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="737ee-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="737ee-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="737ee-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="737ee-143">Click OK.</span></span>
    * <span data-ttu-id="737ee-144">Valitse nykyisen tietomallin tietolähteeksi LedgerJournalTrans-taulu.</span><span class="sxs-lookup"><span data-stu-id="737ee-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="737ee-145">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="737ee-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="737ee-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="737ee-146">Click Add.</span></span>
    * <span data-ttu-id="737ee-147">Lisää uusi laskettu kenttä valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="737ee-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="737ee-148">Syötä Nimi-kenttään $EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="737ee-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="737ee-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="737ee-149">$EndToEndID</span></span>  
13. <span data-ttu-id="737ee-150">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="737ee-150">Click Edit formula.</span></span>
14. <span data-ttu-id="737ee-151">Valitse puussa solmu String\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="737ee-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="737ee-152">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="737ee-152">Click Add function.</span></span>
16. <span data-ttu-id="737ee-153">Laajenna puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="737ee-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="737ee-154">Valitse puussa solmu Transactions\Voucher.</span><span class="sxs-lookup"><span data-stu-id="737ee-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="737ee-155">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="737ee-155">Click Add data source.</span></span>
19. <span data-ttu-id="737ee-156">Kirjoita Kaava-kenttään CONCATENATE(Transactions.Voucher, "-",.</span><span class="sxs-lookup"><span data-stu-id="737ee-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="737ee-157">Kirjoita kaavan loppuun [ , “-“, ].</span><span class="sxs-lookup"><span data-stu-id="737ee-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="737ee-158">Valitse puussa solmu String\TEXT.</span><span class="sxs-lookup"><span data-stu-id="737ee-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="737ee-159">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="737ee-159">Click Add function.</span></span>
22. <span data-ttu-id="737ee-160">Valitse puussa solmu Transactions\Record-ID(RecId).</span><span class="sxs-lookup"><span data-stu-id="737ee-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="737ee-161">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="737ee-161">Click Add data source.</span></span>
24. <span data-ttu-id="737ee-162">Kirjoita Kaava-kenttään CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId)).</span><span class="sxs-lookup"><span data-stu-id="737ee-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="737ee-163">Kirjoita kaavan loppuun [))].</span><span class="sxs-lookup"><span data-stu-id="737ee-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="737ee-164">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="737ee-164">Click Save.</span></span>
    * <span data-ttu-id="737ee-165">Varmista, että luodussa kaavassa ei ole virheitä.</span><span class="sxs-lookup"><span data-stu-id="737ee-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="737ee-166">Katso kaavaeditorin hallinnan Virheet-välilehti.</span><span class="sxs-lookup"><span data-stu-id="737ee-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="737ee-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="737ee-167">Close the page.</span></span>
27. <span data-ttu-id="737ee-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="737ee-168">Click OK.</span></span>
    * <span data-ttu-id="737ee-169">Lisää laskettu kenttä tähän tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="737ee-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="737ee-170">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="737ee-170">Click Add.</span></span>
    * <span data-ttu-id="737ee-171">Lisää uusi laskettu kenttä valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="737ee-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="737ee-172">Syötä Nimi-kenttään $Amount.</span><span class="sxs-lookup"><span data-stu-id="737ee-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="737ee-173">Summa (€)</span><span class="sxs-lookup"><span data-stu-id="737ee-173">$Amount</span></span>  
30. <span data-ttu-id="737ee-174">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="737ee-174">Click Edit formula.</span></span>
31. <span data-ttu-id="737ee-175">Laajenna puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="737ee-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="737ee-176">Valitse puussa solmu Transactions\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="737ee-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="737ee-177">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="737ee-177">Click Add data source.</span></span>
34. <span data-ttu-id="737ee-178">Kirjoita Kaava-kenttään Transactions.AmountCurDebit - .</span><span class="sxs-lookup"><span data-stu-id="737ee-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="737ee-179">Kirjoita kaavan loppuun [ - ].</span><span class="sxs-lookup"><span data-stu-id="737ee-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="737ee-180">Valitse puussa solmu Transactions\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="737ee-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="737ee-181">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="737ee-181">Click Add data source.</span></span>
37. <span data-ttu-id="737ee-182">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="737ee-182">Click Save.</span></span>
38. <span data-ttu-id="737ee-183">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="737ee-183">Close the page.</span></span>
39. <span data-ttu-id="737ee-184">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="737ee-184">Click OK.</span></span>
    * <span data-ttu-id="737ee-185">Nyt lasketun kentän summa (€) lisätään nykyisen tietomallin valittuun tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="737ee-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="737ee-186">Valitse puussa Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="737ee-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="737ee-187">Laajenna puussa solmu Transactions.</span><span class="sxs-lookup"><span data-stu-id="737ee-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="737ee-188">Laajenna tai tiivistä puussa Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="737ee-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="737ee-189">Laajenna ta tiivistä puussa Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="737ee-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="737ee-190">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="737ee-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="737ee-191">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="737ee-191">Click Add root.</span></span>
    * <span data-ttu-id="737ee-192">Syötä tämä tietolähde, kun haluat käyttää yrityksen pankkitilin tietoja.</span><span class="sxs-lookup"><span data-stu-id="737ee-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="737ee-193">Syötä Nimi-kenttään BankAccount.</span><span class="sxs-lookup"><span data-stu-id="737ee-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="737ee-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="737ee-194">BankAccount</span></span>  
47. <span data-ttu-id="737ee-195">Syötä Etiketti-kenttään Pankkitili.</span><span class="sxs-lookup"><span data-stu-id="737ee-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="737ee-196">Pankkitili</span><span class="sxs-lookup"><span data-stu-id="737ee-196">Bank Account</span></span>  
48. <span data-ttu-id="737ee-197">Syötä Ohje-kenttään Pankkitili.</span><span class="sxs-lookup"><span data-stu-id="737ee-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="737ee-198">Pankkitili</span><span class="sxs-lookup"><span data-stu-id="737ee-198">Bank Account</span></span>  
49. <span data-ttu-id="737ee-199">Valitse Kysy kyselyä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="737ee-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="737ee-200">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="737ee-200">Select Yes.</span></span>  
50. <span data-ttu-id="737ee-201">Syötä Taulu-kenttään BankAccountTable.</span><span class="sxs-lookup"><span data-stu-id="737ee-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="737ee-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="737ee-202">BankAccountTable</span></span>  
51. <span data-ttu-id="737ee-203">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="737ee-203">Click OK.</span></span>
    * <span data-ttu-id="737ee-204">Valitse nykyisen tietomallin tietolähteeksi BankAccountTable-taulu.</span><span class="sxs-lookup"><span data-stu-id="737ee-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="737ee-205">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="737ee-205">Click Add root.</span></span>
    * <span data-ttu-id="737ee-206">Syötä tämä tietolähde, kun haluat käyttää yrityksen pankkitilin edellytyksiä.</span><span class="sxs-lookup"><span data-stu-id="737ee-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="737ee-207">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="737ee-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="737ee-208">Yritys </span><span class="sxs-lookup"><span data-stu-id="737ee-208">Company</span></span>  
54. <span data-ttu-id="737ee-209">Syötä Etiketti-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="737ee-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="737ee-210">Yrityksen tiedot</span><span class="sxs-lookup"><span data-stu-id="737ee-210">Company information</span></span>  
55. <span data-ttu-id="737ee-211">Syötä Ohje-kenttään Yrityksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="737ee-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="737ee-212">Yrityksen tiedot</span><span class="sxs-lookup"><span data-stu-id="737ee-212">Company information</span></span>  
56. <span data-ttu-id="737ee-213">Valitse Kysy kyselyä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="737ee-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="737ee-214">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="737ee-214">Select Yes.</span></span>  
57. <span data-ttu-id="737ee-215">Syötä Taulu-kenttään CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="737ee-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="737ee-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="737ee-216">CompanyInfo</span></span>  
58. <span data-ttu-id="737ee-217">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="737ee-217">Click OK.</span></span>
    * <span data-ttu-id="737ee-218">Valitse nykyisen tietomallin tietolähteeksi CompanyInfo-taulu.</span><span class="sxs-lookup"><span data-stu-id="737ee-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="737ee-219">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="737ee-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="737ee-220">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="737ee-220">Click Add root.</span></span>
    * <span data-ttu-id="737ee-221">Lisää laskettu kenttä uutena tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="737ee-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="737ee-222">Syötä Nimi-kenttään ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="737ee-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="737ee-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="737ee-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="737ee-224">Syötä Etiketti-kenttään Käsittelypäivämäärä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="737ee-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="737ee-225">Käsittelypäivämäärä ja -aika</span><span class="sxs-lookup"><span data-stu-id="737ee-225">Processing date & time</span></span>  
63. <span data-ttu-id="737ee-226">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="737ee-226">Click Edit formula.</span></span>
64. <span data-ttu-id="737ee-227">Valitse puussa Päivämäärä/aika\SESSIONNOW.</span><span class="sxs-lookup"><span data-stu-id="737ee-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="737ee-228">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="737ee-228">Click Add function.</span></span>
66. <span data-ttu-id="737ee-229">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="737ee-229">Click Save.</span></span>
67. <span data-ttu-id="737ee-230">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="737ee-230">Close the page.</span></span>
68. <span data-ttu-id="737ee-231">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="737ee-231">Click OK.</span></span>
    * <span data-ttu-id="737ee-232">Lisää laskettu ProcessingDateTime-kenttä nykyisen tietomallin tietolähteeksi.</span><span class="sxs-lookup"><span data-stu-id="737ee-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="737ee-233">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="737ee-233">Click Save.</span></span>
70. <span data-ttu-id="737ee-234">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="737ee-234">Close the page.</span></span>
71. <span data-ttu-id="737ee-235">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="737ee-235">Close the page.</span></span>
72. <span data-ttu-id="737ee-236">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="737ee-236">Close the page.</span></span>

