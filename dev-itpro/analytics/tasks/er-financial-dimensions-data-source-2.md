--- 
title: "Mallien yhdistäminen käyttämään taloushallinnon dimensioita tietolähteenä sähköistä raportointia varten (ER)"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.openlocfilehash: 58a0ce881e5cb8d459256244a144cf51dc357299
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="38ea9-103">Mallien yhdistäminen käyttämään taloushallinnon dimensioita tietolähteenä sähköistä raportointia varten (ER)</span><span class="sxs-lookup"><span data-stu-id="38ea9-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38ea9-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="38ea9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="38ea9-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="38ea9-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 1: tietomallin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="38ea9-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="38ea9-107">Lisää vaaditut tietolähteet mallin yhdistämismäärityksiin</span><span class="sxs-lookup"><span data-stu-id="38ea9-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="38ea9-108">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="38ea9-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="38ea9-109">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="38ea9-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="38ea9-110">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="38ea9-110">Click Designer.</span></span>
4. <span data-ttu-id="38ea9-111">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="38ea9-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="38ea9-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="38ea9-112">Click New.</span></span>
6. <span data-ttu-id="38ea9-113">Valitse Määritelmä-kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="38ea9-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="38ea9-114">Kirjoita Nimi-kenttään "Dimensioiden tietojen yhdistäminen".</span><span class="sxs-lookup"><span data-stu-id="38ea9-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="38ea9-115">Kirjoita Kuvaus-kenttään "Dimensioiden tietojen yhdistäminen".</span><span class="sxs-lookup"><span data-stu-id="38ea9-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="38ea9-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="38ea9-116">Click Save.</span></span>
10. <span data-ttu-id="38ea9-117">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="38ea9-117">Click Designer.</span></span>
11. <span data-ttu-id="38ea9-118">Valitse puussa Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="38ea9-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="38ea9-119">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="38ea9-119">Click Add root.</span></span>
13. <span data-ttu-id="38ea9-120">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="38ea9-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="38ea9-121">Syötä Taulu-kenttään CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="38ea9-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="38ea9-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38ea9-122">Click OK.</span></span>
16. <span data-ttu-id="38ea9-123">Valitse puussa "Functions\Financial dimensions details".</span><span class="sxs-lookup"><span data-stu-id="38ea9-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="38ea9-124">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="38ea9-124">Click Add root.</span></span>
    * <span data-ttu-id="38ea9-125">Tämä tietolähde määrittää, miten taloushallinnon dimensioiden laajuus määritellään raporteille, jotka käyttävät tätä mallia tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="38ea9-126">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38ea9-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="38ea9-127">Valitse Kysy dimensioita -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="38ea9-128">Valitse Kyllä, jos haluat sallia käyttäjän valita dimensiot suorituksen aikana käyttäjän valintalomakkeelta.</span><span class="sxs-lookup"><span data-stu-id="38ea9-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="38ea9-129">Jos arvo on ei, kaikkia nykyisen ilmentymän taloushallinnon dimensioita käytetään oletuksena.</span><span class="sxs-lookup"><span data-stu-id="38ea9-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="38ea9-130">Valitse Taloushallinnon dimensioiden valinta -kentässä "Yritys".</span><span class="sxs-lookup"><span data-stu-id="38ea9-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="38ea9-131">Valitse Kaikki, jos haluat sallia käyttäjien valita haluamansa dimensiot nykyiselle ilmentymälle hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="38ea9-132">Valitse Yritys, jos haluat sallia käyttäjien valita haluamansa dimensiot yritykselle hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="38ea9-133">Valitse Dimensio, jos haluat, että käyttäjät voivat valita dimensiot yhdestä dimensiojoukosta.</span><span class="sxs-lookup"><span data-stu-id="38ea9-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="38ea9-134">Valitse Kysy päätiliä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="38ea9-135">Aseta "Kysy päätiliä" -asetuksen arvoksi Kyllä, jotta käyttäjät valita päätilin osaksi dimensioluetteloa.</span><span class="sxs-lookup"><span data-stu-id="38ea9-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="38ea9-136">Jos arvo on Ei, päätiliä ei sisällytetä dimensioluetteloon ja "Päätili on pakollinen" -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="38ea9-137">Jos "Onko päätili pakollinen" -asetuksen arvoksi on määritetty Kyllä, päätili luetaan dimensioluetteloon käyttäjän valinnasta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="38ea9-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="38ea9-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38ea9-138">Click OK.</span></span>
23. <span data-ttu-id="38ea9-139">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="38ea9-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="38ea9-140">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="38ea9-140">Click Add root.</span></span>
25. <span data-ttu-id="38ea9-141">Kirjoita Nimi-kenttään LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="38ea9-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="38ea9-142">Valitse Kysy kyselyä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="38ea9-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="38ea9-143">Kirjoita Taulu-kenttään LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="38ea9-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="38ea9-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38ea9-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="38ea9-145">Yhdistä tietomallielementit lisättyihin tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="38ea9-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="38ea9-146">Laajenna puussa "Journal".</span><span class="sxs-lookup"><span data-stu-id="38ea9-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="38ea9-147">Laajenna puussa "Journal\Transaction".</span><span class="sxs-lookup"><span data-stu-id="38ea9-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="38ea9-148">Laajenna puussa "Journal\Transaction\Dimensions data".</span><span class="sxs-lookup"><span data-stu-id="38ea9-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="38ea9-149">Laajenna puussa "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="38ea9-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="38ea9-150">Laajenna puussa solmu "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="38ea9-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="38ea9-151">Laajenna puussa LedgerJournal\<Relations.</span><span class="sxs-lookup"><span data-stu-id="38ea9-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="38ea9-152">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="38ea9-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="38ea9-153">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="38ea9-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="38ea9-154">Valitse puussa solmu "Journal\Transactions\Voucher".</span><span class="sxs-lookup"><span data-stu-id="38ea9-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="38ea9-155">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-155">Click Bind.</span></span>
11. <span data-ttu-id="38ea9-156">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="38ea9-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="38ea9-157">Huomaa, että kaikille viittauksille taloushallinnon dimensioihin, jotka on määritetty esimerkiksi arvolle LedgerDimension, on saatavilla vastaava tietolähdenimike (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="38ea9-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="38ea9-158">Tämä tietolähdenimike tarjoaa kyseisen dimensiojoukon taloushallinnon dimensiot tietueen luettelona.</span><span class="sxs-lookup"><span data-stu-id="38ea9-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="38ea9-159">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="38ea9-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="38ea9-160">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="38ea9-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="38ea9-161">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="38ea9-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="38ea9-162">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="38ea9-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="38ea9-163">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="38ea9-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="38ea9-164">Valitse puussa "Journal\Transaction\Dimensions data\Name".</span><span class="sxs-lookup"><span data-stu-id="38ea9-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="38ea9-165">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-165">Click Bind.</span></span>
19. <span data-ttu-id="38ea9-166">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="38ea9-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="38ea9-167">Valitse puussa "Journal\Transaction\Dimensions data\Description".</span><span class="sxs-lookup"><span data-stu-id="38ea9-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="38ea9-168">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-168">Click Bind.</span></span>
22. <span data-ttu-id="38ea9-169">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="38ea9-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="38ea9-170">Valitse puussa "Journal\Transaction\Dimensions data\Code".</span><span class="sxs-lookup"><span data-stu-id="38ea9-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="38ea9-171">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-171">Click Bind.</span></span>
25. <span data-ttu-id="38ea9-172">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="38ea9-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="38ea9-173">Valitse puussa "Journal\Transaction\Dimensions data".</span><span class="sxs-lookup"><span data-stu-id="38ea9-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="38ea9-174">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-174">Click Bind.</span></span>
28. <span data-ttu-id="38ea9-175">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="38ea9-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="38ea9-176">Valitse puussa solmu "Journal\Transactions\Debit".</span><span class="sxs-lookup"><span data-stu-id="38ea9-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="38ea9-177">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-177">Click Bind.</span></span>
31. <span data-ttu-id="38ea9-178">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="38ea9-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="38ea9-179">Valitse puussa solmu "Journal\Transactions\Date".</span><span class="sxs-lookup"><span data-stu-id="38ea9-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="38ea9-180">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-180">Click Bind.</span></span>
34. <span data-ttu-id="38ea9-181">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="38ea9-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="38ea9-182">Valitse puussa solmu "Journal\Transactions\Currency".</span><span class="sxs-lookup"><span data-stu-id="38ea9-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="38ea9-183">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-183">Click Bind.</span></span>
37. <span data-ttu-id="38ea9-184">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="38ea9-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="38ea9-185">Valitse puussa solmu "Journal\Transactions\Credit".</span><span class="sxs-lookup"><span data-stu-id="38ea9-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="38ea9-186">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-186">Click Bind.</span></span>
40. <span data-ttu-id="38ea9-187">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="38ea9-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="38ea9-188">Valitse puussa solmu "Journal\Transactions".</span><span class="sxs-lookup"><span data-stu-id="38ea9-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="38ea9-189">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-189">Click Bind.</span></span>
43. <span data-ttu-id="38ea9-190">Valitse puussa solmu "LedgerJournal\Journal batch number(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="38ea9-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="38ea9-191">Valitse puussa solmu "Journal\Batch".</span><span class="sxs-lookup"><span data-stu-id="38ea9-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="38ea9-192">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-192">Click Bind.</span></span>
46. <span data-ttu-id="38ea9-193">Valitse puussa "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="38ea9-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="38ea9-194">Valitse puussa "Journal".</span><span class="sxs-lookup"><span data-stu-id="38ea9-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="38ea9-195">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-195">Click Bind.</span></span>
49. <span data-ttu-id="38ea9-196">Laajenna puussa "Dimensions".</span><span class="sxs-lookup"><span data-stu-id="38ea9-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="38ea9-197">Laajenna puussa "Dimensions\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="38ea9-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="38ea9-198">Laajenna puussa "Dimensions\Main account and dimensions\Definition".</span><span class="sxs-lookup"><span data-stu-id="38ea9-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="38ea9-199">Valitse puussa "Dimensions\Main account and dimensions\Definition\Name".</span><span class="sxs-lookup"><span data-stu-id="38ea9-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="38ea9-200">Valitse puussa "Dimensioiden asetus\Code".</span><span class="sxs-lookup"><span data-stu-id="38ea9-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="38ea9-201">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-201">Click Bind.</span></span>
55. <span data-ttu-id="38ea9-202">Valitse puussa "Dimensions\Main account and dimensions\Definition\Report column name".</span><span class="sxs-lookup"><span data-stu-id="38ea9-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="38ea9-203">Valitse puussa "Dimensioiden asetus\Name".</span><span class="sxs-lookup"><span data-stu-id="38ea9-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="38ea9-204">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-204">Click Bind.</span></span>
58. <span data-ttu-id="38ea9-205">Valitse puussa "Dimensions\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="38ea9-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="38ea9-206">Valitse puussa "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="38ea9-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="38ea9-207">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38ea9-207">Click Bind.</span></span>
61. <span data-ttu-id="38ea9-208">Valitse puussa "Yritys".</span><span class="sxs-lookup"><span data-stu-id="38ea9-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="38ea9-209">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="38ea9-209">Click Edit.</span></span>
63. <span data-ttu-id="38ea9-210">Kirjoita expressionAsStringText-kenttään "Company.'find()'.'name()".</span><span class="sxs-lookup"><span data-stu-id="38ea9-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="38ea9-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="38ea9-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="38ea9-212">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="38ea9-212">Click Save.</span></span>
65. <span data-ttu-id="38ea9-213">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38ea9-213">Close the page.</span></span>
66. <span data-ttu-id="38ea9-214">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="38ea9-214">Click Save.</span></span>
67. <span data-ttu-id="38ea9-215">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38ea9-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="38ea9-216">Viimeistele malliluonnoksen versio</span><span class="sxs-lookup"><span data-stu-id="38ea9-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="38ea9-217">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38ea9-217">Close the page.</span></span>
2. <span data-ttu-id="38ea9-218">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38ea9-218">Close the page.</span></span>
3. <span data-ttu-id="38ea9-219">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="38ea9-219">Click Change status.</span></span>
4. <span data-ttu-id="38ea9-220">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="38ea9-220">Click Complete.</span></span>
5. <span data-ttu-id="38ea9-221">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38ea9-221">Click OK.</span></span>


