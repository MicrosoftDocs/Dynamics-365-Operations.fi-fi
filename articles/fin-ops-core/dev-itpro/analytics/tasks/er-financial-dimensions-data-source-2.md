---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2 – Mallin yhdistäminen).
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3aabd622d15917d7e4549d0b0679aa20231c5815
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406517"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="2b322-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2 – Mallin yhdistäminen).</span><span class="sxs-lookup"><span data-stu-id="2b322-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b322-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="2b322-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="2b322-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2b322-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="2b322-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 1: tietomallin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="2b322-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="2b322-107">Lisää vaaditut tietolähteet mallin yhdistämismäärityksiin</span><span class="sxs-lookup"><span data-stu-id="2b322-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="2b322-108">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="2b322-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2b322-109">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="2b322-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2b322-110">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="2b322-110">Click Designer.</span></span>
4. <span data-ttu-id="2b322-111">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="2b322-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="2b322-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2b322-112">Click New.</span></span>
6. <span data-ttu-id="2b322-113">Valitse Määritelmä-kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="2b322-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="2b322-114">Kirjoita Nimi-kenttään "Dimensioiden tietojen yhdistäminen".</span><span class="sxs-lookup"><span data-stu-id="2b322-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="2b322-115">Kirjoita Kuvaus-kenttään "Dimensioiden tietojen yhdistäminen".</span><span class="sxs-lookup"><span data-stu-id="2b322-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="2b322-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2b322-116">Click Save.</span></span>
10. <span data-ttu-id="2b322-117">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="2b322-117">Click Designer.</span></span>
11. <span data-ttu-id="2b322-118">Valitse puussa Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="2b322-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="2b322-119">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="2b322-119">Click Add root.</span></span>
13. <span data-ttu-id="2b322-120">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="2b322-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="2b322-121">Syötä Taulu-kenttään CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="2b322-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="2b322-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2b322-122">Click OK.</span></span>
16. <span data-ttu-id="2b322-123">Valitse puussa "Functions\Financial dimensions details".</span><span class="sxs-lookup"><span data-stu-id="2b322-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="2b322-124">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="2b322-124">Click Add root.</span></span>
    * <span data-ttu-id="2b322-125">Tämä tietolähde määrittää, miten taloushallinnon dimensioiden laajuus määritellään raporteille, jotka käyttävät tätä mallia tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="2b322-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="2b322-126">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2b322-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="2b322-127">Valitse Kysy dimensioita -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2b322-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="2b322-128">Valitse Kyllä, jos haluat sallia käyttäjän valita dimensiot suorituksen aikana käyttäjän valintalomakkeelta.</span><span class="sxs-lookup"><span data-stu-id="2b322-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="2b322-129">Jos arvo on ei, kaikkia nykyisen ilmentymän taloushallinnon dimensioita käytetään oletuksena.</span><span class="sxs-lookup"><span data-stu-id="2b322-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="2b322-130">Valitse Taloushallinnon dimensioiden valinta -kentässä "Yritys".</span><span class="sxs-lookup"><span data-stu-id="2b322-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="2b322-131">Valitse Kaikki, jos haluat sallia käyttäjien valita haluamansa dimensiot nykyiselle ilmentymälle hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="2b322-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="2b322-132">Valitse Yritys, jos haluat sallia käyttäjien valita haluamansa dimensiot yritykselle hakukentässä.</span><span class="sxs-lookup"><span data-stu-id="2b322-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="2b322-133">Valitse Dimensio, jos haluat, että käyttäjät voivat valita dimensiot yhdestä dimensiojoukosta.</span><span class="sxs-lookup"><span data-stu-id="2b322-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="2b322-134">Valitse Kysy päätiliä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2b322-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="2b322-135">Aseta "Kysy päätiliä" -asetuksen arvoksi Kyllä, jotta käyttäjät valita päätilin osaksi dimensioluetteloa.</span><span class="sxs-lookup"><span data-stu-id="2b322-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="2b322-136">Jos arvo on Ei, päätiliä ei sisällytetä dimensioluetteloon ja "Päätili on pakollinen" -asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="2b322-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="2b322-137">Jos "Onko päätili pakollinen" -asetuksen arvoksi on määritetty Kyllä, päätili luetaan dimensioluetteloon käyttäjän valinnasta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="2b322-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="2b322-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2b322-138">Click OK.</span></span>
<span data-ttu-id="2b322-139">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="2b322-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="2b322-140">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="2b322-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="2b322-141">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="2b322-141">Click Add root.</span></span>
25. <span data-ttu-id="2b322-142">Kirjoita Nimi-kenttään LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="2b322-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="2b322-143">Valitse Kysy kyselyä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2b322-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="2b322-144">Kirjoita Taulu-kenttään LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="2b322-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="2b322-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2b322-145">Click OK.</span></span>
<span data-ttu-id="2b322-146">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="2b322-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="2b322-147">Yhdistä tietomallielementit lisättyihin tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="2b322-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="2b322-148">Laajenna puussa "Journal".</span><span class="sxs-lookup"><span data-stu-id="2b322-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="2b322-149">Laajenna puussa "Journal\Transaction".</span><span class="sxs-lookup"><span data-stu-id="2b322-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="2b322-150">Laajenna puussa "Journal\Transaction\Dimensions data".</span><span class="sxs-lookup"><span data-stu-id="2b322-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="2b322-151">Laajenna puussa "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="2b322-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="2b322-152">Laajenna puussa solmu "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="2b322-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="2b322-153">Laajenna puussa LedgerJournal\<Relations.</span><span class="sxs-lookup"><span data-stu-id="2b322-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="2b322-154">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="2b322-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="2b322-155">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="2b322-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="2b322-156">Valitse puussa solmu "Journal\Transactions\Voucher".</span><span class="sxs-lookup"><span data-stu-id="2b322-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="2b322-157">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-157">Click Bind.</span></span>
11. <span data-ttu-id="2b322-158">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="2b322-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="2b322-159">Huomaa, että kaikille viittauksille taloushallinnon dimensioihin, jotka on määritetty esimerkiksi arvolle LedgerDimension, on saatavilla vastaava tietolähdenimike (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="2b322-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="2b322-160">Tämä tietolähdenimike tarjoaa kyseisen dimensiojoukon taloushallinnon dimensiot tietueen luettelona.</span><span class="sxs-lookup"><span data-stu-id="2b322-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="2b322-161">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="2b322-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="2b322-162">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="2b322-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="2b322-163">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="2b322-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="2b322-164">Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="2b322-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="2b322-165">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="2b322-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="2b322-166">Valitse puussa "Journal\Transaction\Dimensions data\Name".</span><span class="sxs-lookup"><span data-stu-id="2b322-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="2b322-167">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-167">Click Bind.</span></span>
19. <span data-ttu-id="2b322-168">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="2b322-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="2b322-169">Valitse puussa "Journal\Transaction\Dimensions data\Description".</span><span class="sxs-lookup"><span data-stu-id="2b322-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="2b322-170">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-170">Click Bind.</span></span>
22. <span data-ttu-id="2b322-171">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="2b322-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="2b322-172">Valitse puussa "Journal\Transaction\Dimensions data\Code".</span><span class="sxs-lookup"><span data-stu-id="2b322-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="2b322-173">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-173">Click Bind.</span></span>
25. <span data-ttu-id="2b322-174">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="2b322-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="2b322-175">Valitse puussa "Journal\Transaction\Dimensions data".</span><span class="sxs-lookup"><span data-stu-id="2b322-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="2b322-176">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-176">Click Bind.</span></span>
<span data-ttu-id="2b322-177">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="2b322-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="2b322-178">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="2b322-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="2b322-179">Valitse puussa solmu "Journal\Transactions\Debit".</span><span class="sxs-lookup"><span data-stu-id="2b322-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="2b322-180">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-180">Click Bind.</span></span>
31. <span data-ttu-id="2b322-181">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="2b322-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="2b322-182">Valitse puussa solmu "Journal\Transactions\Date".</span><span class="sxs-lookup"><span data-stu-id="2b322-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="2b322-183">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-183">Click Bind.</span></span>
34. <span data-ttu-id="2b322-184">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="2b322-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="2b322-185">Valitse puussa solmu "Journal\Transactions\Currency".</span><span class="sxs-lookup"><span data-stu-id="2b322-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="2b322-186">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-186">Click Bind.</span></span>
37. <span data-ttu-id="2b322-187">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="2b322-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="2b322-188">Valitse puussa solmu "Journal\Transactions\Credit".</span><span class="sxs-lookup"><span data-stu-id="2b322-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="2b322-189">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-189">Click Bind.</span></span>
40. <span data-ttu-id="2b322-190">Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="2b322-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="2b322-191">Valitse puussa solmu "Journal\Transactions".</span><span class="sxs-lookup"><span data-stu-id="2b322-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="2b322-192">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-192">Click Bind.</span></span>
43. <span data-ttu-id="2b322-193">Valitse puussa solmu "LedgerJournal\Journal batch number(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="2b322-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="2b322-194">Valitse puussa solmu "Journal\Batch".</span><span class="sxs-lookup"><span data-stu-id="2b322-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="2b322-195">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-195">Click Bind.</span></span>
46. <span data-ttu-id="2b322-196">Valitse puussa "LedgerJournal".</span><span class="sxs-lookup"><span data-stu-id="2b322-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="2b322-197">Valitse puussa "Journal".</span><span class="sxs-lookup"><span data-stu-id="2b322-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="2b322-198">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-198">Click Bind.</span></span>
49. <span data-ttu-id="2b322-199">Laajenna puussa "Dimensions".</span><span class="sxs-lookup"><span data-stu-id="2b322-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="2b322-200">Laajenna puussa "Dimensions\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="2b322-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="2b322-201">Laajenna puussa "Dimensions\Main account and dimensions\Definition".</span><span class="sxs-lookup"><span data-stu-id="2b322-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="2b322-202">Valitse puussa "Dimensions\Main account and dimensions\Definition\Name".</span><span class="sxs-lookup"><span data-stu-id="2b322-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="2b322-203">Valitse puussa "Dimensioiden asetus\Code".</span><span class="sxs-lookup"><span data-stu-id="2b322-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="2b322-204">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-204">Click Bind.</span></span>
55. <span data-ttu-id="2b322-205">Valitse puussa "Dimensions\Main account and dimensions\Definition\Report column name".</span><span class="sxs-lookup"><span data-stu-id="2b322-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="2b322-206">Valitse puussa "Dimensioiden asetus\Name".</span><span class="sxs-lookup"><span data-stu-id="2b322-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="2b322-207">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-207">Click Bind.</span></span>
58. <span data-ttu-id="2b322-208">Valitse puussa "Dimensions\Main account and dimensions".</span><span class="sxs-lookup"><span data-stu-id="2b322-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="2b322-209">Valitse puussa "Dimensioiden asetus".</span><span class="sxs-lookup"><span data-stu-id="2b322-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="2b322-210">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="2b322-210">Click Bind.</span></span>
61. <span data-ttu-id="2b322-211">Valitse puussa "Yritys".</span><span class="sxs-lookup"><span data-stu-id="2b322-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="2b322-212">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2b322-212">Click Edit.</span></span>
63. <span data-ttu-id="2b322-213">Kirjoita expressionAsStringText-kenttään "Company.'find()'.'name()".</span><span class="sxs-lookup"><span data-stu-id="2b322-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="2b322-214">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="2b322-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="2b322-215">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2b322-215">Click Save.</span></span>
<span data-ttu-id="2b322-216">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="2b322-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="2b322-217">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2b322-217">Close the page.</span></span>
66. <span data-ttu-id="2b322-218">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2b322-218">Click Save.</span></span>
67. <span data-ttu-id="2b322-219">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2b322-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="2b322-220">Viimeistele malliluonnoksen versio</span><span class="sxs-lookup"><span data-stu-id="2b322-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="2b322-221">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2b322-221">Close the page.</span></span>
2. <span data-ttu-id="2b322-222">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2b322-222">Close the page.</span></span>
3. <span data-ttu-id="2b322-223">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="2b322-223">Click Change status.</span></span>
4. <span data-ttu-id="2b322-224">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="2b322-224">Click Complete.</span></span>
5. <span data-ttu-id="2b322-225">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2b322-225">Click OK.</span></span>
<span data-ttu-id="2b322-226">![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="2b322-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
