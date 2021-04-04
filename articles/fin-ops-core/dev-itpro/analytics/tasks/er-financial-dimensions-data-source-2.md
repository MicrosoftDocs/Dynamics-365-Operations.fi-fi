---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2 – Mallin yhdistäminen).
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) mallin määrittämistä käyttämään taloushallinnon dimensioita ER-raporttien tietolähteenä. (Osa 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59f65962ef8f6ae79190b6595a313831eca53830
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570165"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="efdc2-104">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2 – Mallin yhdistäminen).</span><span class="sxs-lookup"><span data-stu-id="efdc2-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efdc2-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="efdc2-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="efdc2-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="efdc2-107">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 1: tietomallin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="efdc2-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="efdc2-108">Lisää vaaditut tietolähteet mallin yhdistämismäärityksiin</span><span class="sxs-lookup"><span data-stu-id="efdc2-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="efdc2-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="efdc2-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="efdc2-110">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="efdc2-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="efdc2-111">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="efdc2-111">Click Designer.</span></span>
4. <span data-ttu-id="efdc2-112">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="efdc2-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="efdc2-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="efdc2-113">Click New.</span></span>
6. <span data-ttu-id="efdc2-114">Valitse Määritelmä-kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="efdc2-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="efdc2-115">Kirjoita Nimi-kenttään "Dimensioiden tietojen yhdistäminen".</span><span class="sxs-lookup"><span data-stu-id="efdc2-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="efdc2-116">Kirjoita Kuvaus-kenttään "Dimensioiden tietojen yhdistäminen".</span><span class="sxs-lookup"><span data-stu-id="efdc2-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="efdc2-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="efdc2-117">Click Save.</span></span>
10. <span data-ttu-id="efdc2-118">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="efdc2-118">Click Designer.</span></span>
11. <span data-ttu-id="efdc2-119">Valitse puussa Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="efdc2-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="efdc2-120">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="efdc2-120">Click Add root.</span></span>
13. <span data-ttu-id="efdc2-121">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="efdc2-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="efdc2-122">Syötä Taulu-kenttään CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="efdc2-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="efdc2-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="efdc2-123">Click OK.</span></span>
16. <span data-ttu-id="efdc2-124">Valitse puussa "Functions\Financial dimensions details".</span><span class="sxs-lookup"><span data-stu-id="efdc2-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="efdc2-125">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="efdc2-125">Click Add root.</span></span>
    * <span data-ttu-id="efdc2-126">Tämä tietolähde määrittää, miten taloushallinnon dimensioiden laajuus määritellään raporteille, jotka käyttävät tätä mallia tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="efdc2-127">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="efdc2-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="efdc2-128">Valitse Kysy dimensioita -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="efdc2-129">Valitse Kyllä, jos haluat sallia käyttäjän valita dimensiot suorituksen aikana käyttäjän valintalomakkeelta.</span><span class="sxs-lookup"><span data-stu-id="efdc2-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="efdc2-130">Jos arvo on ei, kaikkia nykyisen ilmentymän taloushallinnon dimensioita käytetään oletuksena.</span><span class="sxs-lookup"><span data-stu-id="efdc2-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="efdc2-131">Valitse Taloushallinnon dimensioiden valinta -kentässä "Yritys".</span><span class="sxs-lookup"><span data-stu-id="efdc2-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="efdc2-132">Valitse Kaikki, jos haluat sallia käyttäjien valita haluamansa dimensiot nykyiselle ilmentymälle hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="efdc2-133">Valitse Yritys, jos haluat sallia käyttäjien valita haluamansa dimensiot yritykselle hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="efdc2-134">Valitse Dimensio, jos haluat, että käyttäjät voivat valita dimensiot yhdestä dimensiojoukosta.</span><span class="sxs-lookup"><span data-stu-id="efdc2-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="efdc2-135">Valitse Kysy päätiliä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="efdc2-136">Aseta "Kysy päätiliä" -asetuksen arvoksi Kyllä, jotta käyttäjät valita päätilin osaksi dimensioluetteloa.</span><span class="sxs-lookup"><span data-stu-id="efdc2-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="efdc2-137">Jos arvo on Ei, päätiliä ei sisällytetä dimensioluetteloon ja "Päätili on pakollinen" -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="efdc2-138">Jos "Onko päätili pakollinen" -asetuksen arvoksi on määritetty Kyllä, päätili luetaan dimensioluetteloon käyttäjän valinnasta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="efdc2-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="efdc2-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="efdc2-139">Click OK.</span></span>
<span data-ttu-id="efdc2-140">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="efdc2-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="efdc2-141">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="efdc2-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="efdc2-142">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="efdc2-142">Click Add root.</span></span>
25. <span data-ttu-id="efdc2-143">Kirjoita Nimi-kenttään LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="efdc2-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="efdc2-144">Valitse Kysy kyselyä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="efdc2-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="efdc2-145">Kirjoita Taulu-kenttään LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="efdc2-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="efdc2-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="efdc2-146">Click OK.</span></span>
<span data-ttu-id="efdc2-147">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="efdc2-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="efdc2-148">Yhdistä tietomallielementit lisättyihin tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="efdc2-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="efdc2-149">Laajenna puussa "Journal".</span><span class="sxs-lookup"><span data-stu-id="efdc2-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="efdc2-150">Laajenna puussa "Journal\Transaction".</span><span class="sxs-lookup"><span data-stu-id="efdc2-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="efdc2-151">Laajenna puussa "Journal\Transaction\Dimensions data".</span><span class="sxs-lookup"><span data-stu-id="efdc2-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="efdc2-152">Laajenna puussa "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="efdc2-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="efdc2-153">Laajenna puussa solmu "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="efdc2-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="efdc2-154">Laajenna puussa LedgerJournal\<Relations.</span><span class="sxs-lookup"><span data-stu-id="efdc2-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="efdc2-155">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="efdc2-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="efdc2-156">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="efdc2-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="efdc2-157">Valitse puussa solmu "Journal\Transactions\Voucher".</span><span class="sxs-lookup"><span data-stu-id="efdc2-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="efdc2-158">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-158">Click Bind.</span></span>
11. <span data-ttu-id="efdc2-159">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="efdc2-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="efdc2-160">Huomaa, että kaikille viittauksille taloushallinnon dimensioihin, jotka on määritetty esimerkiksi arvolle LedgerDimension, on saatavilla vastaava tietolähdenimike (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="efdc2-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="efdc2-161">Tämä tietolähdenimike tarjoaa kyseisen dimensiojoukon taloushallinnon dimensiot tietueen luettelona.</span><span class="sxs-lookup"><span data-stu-id="efdc2-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="efdc2-162">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="efdc2-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="efdc2-163">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="efdc2-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="efdc2-164">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="efdc2-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="efdc2-165">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="efdc2-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="efdc2-166">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="efdc2-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="efdc2-167">Valitse puussa "Journal\Transaction\Dimensions data\Name".</span><span class="sxs-lookup"><span data-stu-id="efdc2-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="efdc2-168">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-168">Click Bind.</span></span>
19. <span data-ttu-id="efdc2-169">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="efdc2-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="efdc2-170">Valitse puussa "Journal\Transaction\Dimensions data\Description".</span><span class="sxs-lookup"><span data-stu-id="efdc2-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="efdc2-171">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-171">Click Bind.</span></span>
22. <span data-ttu-id="efdc2-172">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="efdc2-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="efdc2-173">Valitse puussa "Journal\Transaction\Dimensions data\Code".</span><span class="sxs-lookup"><span data-stu-id="efdc2-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="efdc2-174">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-174">Click Bind.</span></span>
25. <span data-ttu-id="efdc2-175">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="efdc2-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="efdc2-176">Valitse puussa "Journal\Transaction\Dimensions data".</span><span class="sxs-lookup"><span data-stu-id="efdc2-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="efdc2-177">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-177">Click Bind.</span></span>
<span data-ttu-id="efdc2-178">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="efdc2-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="efdc2-179">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="efdc2-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="efdc2-180">Valitse puussa solmu "Journal\Transactions\Debit".</span><span class="sxs-lookup"><span data-stu-id="efdc2-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="efdc2-181">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-181">Click Bind.</span></span>
31. <span data-ttu-id="efdc2-182">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="efdc2-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="efdc2-183">Valitse puussa solmu "Journal\Transactions\Date".</span><span class="sxs-lookup"><span data-stu-id="efdc2-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="efdc2-184">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-184">Click Bind.</span></span>
34. <span data-ttu-id="efdc2-185">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="efdc2-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="efdc2-186">Valitse puussa solmu "Journal\Transactions\Currency".</span><span class="sxs-lookup"><span data-stu-id="efdc2-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="efdc2-187">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-187">Click Bind.</span></span>
37. <span data-ttu-id="efdc2-188">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="efdc2-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="efdc2-189">Valitse puussa solmu "Journal\Transactions\Credit".</span><span class="sxs-lookup"><span data-stu-id="efdc2-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="efdc2-190">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-190">Click Bind.</span></span>
40. <span data-ttu-id="efdc2-191">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="efdc2-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="efdc2-192">Valitse puussa solmu "Journal\Transactions".</span><span class="sxs-lookup"><span data-stu-id="efdc2-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="efdc2-193">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-193">Click Bind.</span></span>
43. <span data-ttu-id="efdc2-194">Valitse puussa solmu "LedgerJournal\Journal batch number(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="efdc2-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="efdc2-195">Valitse puussa solmu "Journal\Batch".</span><span class="sxs-lookup"><span data-stu-id="efdc2-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="efdc2-196">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-196">Click Bind.</span></span>
46. <span data-ttu-id="efdc2-197">Valitse puussa "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="efdc2-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="efdc2-198">Valitse puussa "Journal".</span><span class="sxs-lookup"><span data-stu-id="efdc2-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="efdc2-199">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-199">Click Bind.</span></span>
49. <span data-ttu-id="efdc2-200">Laajenna puussa "Dimensions".</span><span class="sxs-lookup"><span data-stu-id="efdc2-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="efdc2-201">Laajenna puussa "Dimensions\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="efdc2-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="efdc2-202">Laajenna puussa "Dimensions\Main account and dimensions\Definition".</span><span class="sxs-lookup"><span data-stu-id="efdc2-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="efdc2-203">Valitse puussa "Dimensions\Main account and dimensions\Definition\Name".</span><span class="sxs-lookup"><span data-stu-id="efdc2-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="efdc2-204">Valitse puussa "Dimensioiden asetus\Code".</span><span class="sxs-lookup"><span data-stu-id="efdc2-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="efdc2-205">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-205">Click Bind.</span></span>
55. <span data-ttu-id="efdc2-206">Valitse puussa "Dimensions\Main account and dimensions\Definition\Report column name".</span><span class="sxs-lookup"><span data-stu-id="efdc2-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="efdc2-207">Valitse puussa "Dimensioiden asetus\Name".</span><span class="sxs-lookup"><span data-stu-id="efdc2-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="efdc2-208">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-208">Click Bind.</span></span>
58. <span data-ttu-id="efdc2-209">Valitse puussa "Dimensions\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="efdc2-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="efdc2-210">Valitse puussa "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="efdc2-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="efdc2-211">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="efdc2-211">Click Bind.</span></span>
61. <span data-ttu-id="efdc2-212">Valitse puussa "Yritys".</span><span class="sxs-lookup"><span data-stu-id="efdc2-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="efdc2-213">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="efdc2-213">Click Edit.</span></span>
63. <span data-ttu-id="efdc2-214">Kirjoita expressionAsStringText-kenttään "Company.'find()'.'name()".</span><span class="sxs-lookup"><span data-stu-id="efdc2-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="efdc2-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="efdc2-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="efdc2-216">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="efdc2-216">Click Save.</span></span>
<span data-ttu-id="efdc2-217">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="efdc2-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="efdc2-218">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="efdc2-218">Close the page.</span></span>
66. <span data-ttu-id="efdc2-219">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="efdc2-219">Click Save.</span></span>
67. <span data-ttu-id="efdc2-220">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="efdc2-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="efdc2-221">Viimeistele malliluonnoksen versio</span><span class="sxs-lookup"><span data-stu-id="efdc2-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="efdc2-222">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="efdc2-222">Close the page.</span></span>
2. <span data-ttu-id="efdc2-223">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="efdc2-223">Close the page.</span></span>
3. <span data-ttu-id="efdc2-224">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="efdc2-224">Click Change status.</span></span>
4. <span data-ttu-id="efdc2-225">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="efdc2-225">Click Complete.</span></span>
5. <span data-ttu-id="efdc2-226">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="efdc2-226">Click OK.</span></span>
<span data-ttu-id="efdc2-227">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="efdc2-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]