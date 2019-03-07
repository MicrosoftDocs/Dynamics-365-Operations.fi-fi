---
title: ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "326650"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="122cb-103">ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="122cb-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="122cb-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin.</span><span class="sxs-lookup"><span data-stu-id="122cb-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="122cb-105">Tätä konfiguraatiota käytetään toimittajamaksujen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="122cb-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="122cb-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="122cb-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="122cb-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="122cb-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="122cb-108">Sinulla on myös oltava Excel-tiedosto, joka tuodaan mallia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="122cb-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="122cb-109">Tätä tiedostoa voi käyttää kohdasta [Maksuilmoituksen malli](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="122cb-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="122cb-110">Lataa maksujen tietomallin konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="122cb-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="122cb-111">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="122cb-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="122cb-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="122cb-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="122cb-113">Valitse malliyrityksen konfiguraation lähde Litware, Inc. Jos lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="122cb-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="122cb-114">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="122cb-114">Click Set active.</span></span>
4. <span data-ttu-id="122cb-115">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="122cb-115">Click Repositories.</span></span>
    * <span data-ttu-id="122cb-116">Jos operatiivisen resurssityypin säilö on käytettävissä, valitse se.</span><span class="sxs-lookup"><span data-stu-id="122cb-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="122cb-117">Jos säilö on käytettävissä, ohita seuraavat, uuden säilön luomista koskevat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="122cb-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="122cb-118">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="122cb-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="122cb-119">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="122cb-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="122cb-120">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="122cb-120">Click Create repository.</span></span>
8. <span data-ttu-id="122cb-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="122cb-121">Click OK.</span></span>
9. <span data-ttu-id="122cb-122">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="122cb-122">Click Open.</span></span>
10. <span data-ttu-id="122cb-123">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="122cb-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="122cb-124">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="122cb-124">Click Import.</span></span>
    * <span data-ttu-id="122cb-125">Tuo tämä tietomalli.</span><span class="sxs-lookup"><span data-stu-id="122cb-125">Import this data model.</span></span> <span data-ttu-id="122cb-126">Sitä käytetään uuden muotokonfiguraation tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="122cb-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="122cb-127">Ohita tämä vaihe, jos tämä konfiguraatio on tuotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="122cb-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="122cb-128">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="122cb-128">Click Yes.</span></span>
13. <span data-ttu-id="122cb-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-129">Close the page.</span></span>
14. <span data-ttu-id="122cb-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="122cb-131">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="122cb-131">Create a new format configuration</span></span>
1. <span data-ttu-id="122cb-132">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="122cb-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="122cb-133">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="122cb-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="122cb-134">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="122cb-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="122cb-135">Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="122cb-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="122cb-136">Luo muoto, joka perustuu PaymentModel-tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="122cb-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="122cb-137">Kirjoita Nimi-kentän arvoksi Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="122cb-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="122cb-138">Laskentataulukkoraportin esimerkki</span><span class="sxs-lookup"><span data-stu-id="122cb-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="122cb-139">Kirjoita Kuvaus-kentän arvoksi Toimittajamaksujen laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="122cb-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="122cb-140">Toimittajamaksujen laskentataulukkoraportin esimerkki</span><span class="sxs-lookup"><span data-stu-id="122cb-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="122cb-141">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="122cb-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="122cb-142">Valitse CustomerCreditTransferInitiation-määritelmä.</span><span class="sxs-lookup"><span data-stu-id="122cb-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="122cb-143">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="122cb-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="122cb-144">Suunnittele uusi asiakirja OPENXML-laskentataulukkomuodossa</span><span class="sxs-lookup"><span data-stu-id="122cb-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="122cb-145">Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="122cb-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="122cb-146">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="122cb-146">Click Designer.</span></span>
3. <span data-ttu-id="122cb-147">Valitse toimintoruudussa Tuo.</span><span class="sxs-lookup"><span data-stu-id="122cb-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="122cb-148">Napsauta Tuo Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="122cb-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="122cb-149">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="122cb-149">Click Attachments.</span></span>
    * <span data-ttu-id="122cb-150">Liitä aiemmin luotu Excel-asiakirja mallina.</span><span class="sxs-lookup"><span data-stu-id="122cb-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="122cb-151">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="122cb-151">Click New.</span></span>
7. <span data-ttu-id="122cb-152">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="122cb-152">Click File.</span></span>
    * <span data-ttu-id="122cb-153">Osoita aiemmin luotu Excel-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="122cb-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="122cb-154">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-154">Close the page.</span></span>
9. <span data-ttu-id="122cb-155">Syötä tai valitse Malli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="122cb-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="122cb-156">Valitse liitetty Excel-tiedosto käytettäväksi mallina.</span><span class="sxs-lookup"><span data-stu-id="122cb-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="122cb-157">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="122cb-157">Click OK.</span></span>
    * <span data-ttu-id="122cb-158">Huomaa, ER-muodon osat on luotu suunnittelumuodossa, joka perustuu viittaavan MS Excel -tiedoston rakenteeseen (nimetyt alueet).</span><span class="sxs-lookup"><span data-stu-id="122cb-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="122cb-159">Luo uusi tietolähde kokonaissummien laskentaan valuuttakoodien perusteella</span><span class="sxs-lookup"><span data-stu-id="122cb-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="122cb-160">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="122cb-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="122cb-161">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="122cb-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="122cb-162">Valitse valikkopuussa Toiminnot\Ryhmittely.</span><span class="sxs-lookup"><span data-stu-id="122cb-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="122cb-163">Kirjoita Nimi-kenttään PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="122cb-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="122cb-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="122cb-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="122cb-165">Napsauta Muokkaa ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="122cb-165">Click Edit group by.</span></span>
6. <span data-ttu-id="122cb-166">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="122cb-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="122cb-167">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="122cb-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="122cb-168">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="122cb-168">Click Add field to.</span></span>
9. <span data-ttu-id="122cb-169">Napsauta Mitä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="122cb-169">Click What to group.</span></span>
10. <span data-ttu-id="122cb-170">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="122cb-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="122cb-171">Valitse puussa solmu Malli\Maksut\Kuvaus.</span><span class="sxs-lookup"><span data-stu-id="122cb-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="122cb-172">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="122cb-172">Click Add field to.</span></span>
13. <span data-ttu-id="122cb-173">Napsauta Ryhmitellyt kentät.</span><span class="sxs-lookup"><span data-stu-id="122cb-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="122cb-174">Valitse puussa solmu Malli\Maksut\Ohjattu summa(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="122cb-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="122cb-175">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="122cb-175">Click Add field to.</span></span>
16. <span data-ttu-id="122cb-176">Napsauta Koostekentät.</span><span class="sxs-lookup"><span data-stu-id="122cb-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="122cb-177">Valitse vaihtoehto Menetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="122cb-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="122cb-178">Valitse koostefunktioksi SUMMA.</span><span class="sxs-lookup"><span data-stu-id="122cb-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="122cb-179">Kirjoita Nimi-kenttään TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="122cb-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="122cb-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="122cb-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="122cb-181">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="122cb-181">Click Save.</span></span>
20. <span data-ttu-id="122cb-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-182">Close the page.</span></span>
21. <span data-ttu-id="122cb-183">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="122cb-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="122cb-184">Määritä muodon komponentit tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="122cb-184">Map format components to data sources</span></span>
1. <span data-ttu-id="122cb-185">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="122cb-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="122cb-186">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="122cb-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="122cb-187">Laajenna puussa solmu Malli\Maksut\Aloittava osapuoli(InitiatingParty).</span><span class="sxs-lookup"><span data-stu-id="122cb-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="122cb-188">Valitse puussa solmu Malli\Maksut\Aloittava osapuoli(InitiatingParty)\Nimi.</span><span class="sxs-lookup"><span data-stu-id="122cb-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="122cb-189">Valitse puussa Excel\ReportHeader.</span><span class="sxs-lookup"><span data-stu-id="122cb-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="122cb-190">Valitse puussa Excel\ReportHeader\CompanyName.</span><span class="sxs-lookup"><span data-stu-id="122cb-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="122cb-191">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-191">Click Bind.</span></span>
8. <span data-ttu-id="122cb-192">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="122cb-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="122cb-193">Laajenna puussa solmu Malli\Maksut\Laskuttaja\Tunnus.</span><span class="sxs-lookup"><span data-stu-id="122cb-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="122cb-194">Laajenna puussa Malli\Maksut\Laskuttaja\Tunnus\Lähdetunnus(SourceID).</span><span class="sxs-lookup"><span data-stu-id="122cb-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="122cb-195">Valitse puussa Excel\PaymLines.</span><span class="sxs-lookup"><span data-stu-id="122cb-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="122cb-196">Valitse puussa Excel\PaymLines\VendAccountName.</span><span class="sxs-lookup"><span data-stu-id="122cb-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="122cb-197">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-197">Click Bind.</span></span>
14. <span data-ttu-id="122cb-198">Valitse puussa solmu model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="122cb-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="122cb-199">Valitse puussa Excel\PaymLines\VendName.</span><span class="sxs-lookup"><span data-stu-id="122cb-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="122cb-200">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-200">Click Bind.</span></span>
17. <span data-ttu-id="122cb-201">Laajenna puussa Malli\Maksut\Laskuttajan edustaja(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="122cb-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="122cb-202">Valitse puussa solmu Malli\Maksut\Laskuttajan edustaja(CreditorAgent)\Nimi.</span><span class="sxs-lookup"><span data-stu-id="122cb-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="122cb-203">Valitse puussa Excel\PaymLines\Pankki.</span><span class="sxs-lookup"><span data-stu-id="122cb-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="122cb-204">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-204">Click Bind.</span></span>
21. <span data-ttu-id="122cb-205">Valitse puussa solmu Malli\Maksut\Laskuttajan edustaja(CreditorAgent)\Reititysnumero(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="122cb-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="122cb-206">Valitse puussa Excel\PaymLines\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="122cb-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="122cb-207">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-207">Click Bind.</span></span>
24. <span data-ttu-id="122cb-208">Laajenna puussa model\Payments\Creditor Account(CreditorAccount).</span><span class="sxs-lookup"><span data-stu-id="122cb-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="122cb-209">Laajenna puussa model\Payments\Creditor Account(CreditorAccount)\Identification.</span><span class="sxs-lookup"><span data-stu-id="122cb-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="122cb-210">Valitse puussa Malli\Maksut\Laskuttajan tili(CreditorAccount)\Tunnus\Numero.</span><span class="sxs-lookup"><span data-stu-id="122cb-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="122cb-211">Valitse puussa Excel\PaymLines\AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="122cb-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="122cb-212">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-212">Click Bind.</span></span>
29. <span data-ttu-id="122cb-213">Valitse puussa solmu Malli\Maksut\Ohjattu summa(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="122cb-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="122cb-214">Valitse puussa Excel\PaymLines\Veloitus.</span><span class="sxs-lookup"><span data-stu-id="122cb-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="122cb-215">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-215">Click Bind.</span></span>
32. <span data-ttu-id="122cb-216">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="122cb-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="122cb-217">Laajenna puussa model\Payments\Creditor Account(CreditorAccount).</span><span class="sxs-lookup"><span data-stu-id="122cb-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="122cb-218">Laajenna puussa Malli\Maksut\Laskuttajan edustaja(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="122cb-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="122cb-219">Valitse puussa solmu Malli\Maksut\Kuvaus.</span><span class="sxs-lookup"><span data-stu-id="122cb-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="122cb-220">Valitse puussa Excel\PaymLines\Valuutta.</span><span class="sxs-lookup"><span data-stu-id="122cb-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="122cb-221">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-221">Click Bind.</span></span>
38. <span data-ttu-id="122cb-222">Laajenna puussa PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="122cb-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="122cb-223">Laajenna puussa PaymentByCurrency\ryhmitelty.</span><span class="sxs-lookup"><span data-stu-id="122cb-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="122cb-224">Valitse puussa PaymentByCurrency\ryhmitelty\Valuutta.</span><span class="sxs-lookup"><span data-stu-id="122cb-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="122cb-225">Laajenna puussa Excel\SummaryLines.</span><span class="sxs-lookup"><span data-stu-id="122cb-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="122cb-226">Valitse puussa Excel\SummaryLines\SummaryCurrency.</span><span class="sxs-lookup"><span data-stu-id="122cb-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="122cb-227">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-227">Click Bind.</span></span>
44. <span data-ttu-id="122cb-228">Laajenna puussa PaymentByCurrency\koottu.</span><span class="sxs-lookup"><span data-stu-id="122cb-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="122cb-229">Valitse puussa PaymentByCurrency\koottu\TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="122cb-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="122cb-230">Valitse puussa Excel\SummaryLines\SummaryAmount.</span><span class="sxs-lookup"><span data-stu-id="122cb-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="122cb-231">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-231">Click Bind.</span></span>
48. <span data-ttu-id="122cb-232">Valitse puussa solmu PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="122cb-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="122cb-233">Valitse puussa Excel\SummaryLines.</span><span class="sxs-lookup"><span data-stu-id="122cb-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="122cb-234">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-234">Click Bind.</span></span>
51. <span data-ttu-id="122cb-235">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="122cb-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="122cb-236">Valitse puussa Excel\PaymLines.</span><span class="sxs-lookup"><span data-stu-id="122cb-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="122cb-237">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="122cb-237">Click Bind.</span></span>
54. <span data-ttu-id="122cb-238">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="122cb-238">Click Save.</span></span>
55. <span data-ttu-id="122cb-239">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="122cb-240">Käytä luotua määritystä maksujen käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="122cb-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="122cb-241">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="122cb-241">Click Change status.</span></span>
2. <span data-ttu-id="122cb-242">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="122cb-242">Click Complete.</span></span>
3. <span data-ttu-id="122cb-243">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="122cb-243">Click OK.</span></span>
4. <span data-ttu-id="122cb-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-244">Close the page.</span></span>
5. <span data-ttu-id="122cb-245">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-245">Close the page.</span></span>
6. <span data-ttu-id="122cb-246">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="122cb-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="122cb-247">Voit suodattaa Maksutapa-kentän pikasuodattimella käyttämällä Sähköinen-arvoa.</span><span class="sxs-lookup"><span data-stu-id="122cb-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="122cb-248">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="122cb-248">Electronic</span></span>  
8. <span data-ttu-id="122cb-249">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="122cb-249">Click Edit.</span></span>
9. <span data-ttu-id="122cb-250">Laajenna Tiedostomuodot-osa.</span><span class="sxs-lookup"><span data-stu-id="122cb-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="122cb-251">Valitse Yleinen sähköinen raportointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="122cb-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="122cb-252">Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.</span><span class="sxs-lookup"><span data-stu-id="122cb-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="122cb-253">Valitse Laskentataulukkoraportin esimerkki -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="122cb-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="122cb-254">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="122cb-254">Click Save.</span></span>
13. <span data-ttu-id="122cb-255">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="122cb-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="122cb-256">Käytä luotua konfiguraatiota maksukirjauskansioiden käsittelemisen testaamiseen</span><span class="sxs-lookup"><span data-stu-id="122cb-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="122cb-257">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="122cb-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="122cb-258">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="122cb-258">Click New.</span></span>
    * <span data-ttu-id="122cb-259">Luo uusi maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="122cb-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="122cb-260">Kirjoita Nimi-kenttään VendPay.</span><span class="sxs-lookup"><span data-stu-id="122cb-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="122cb-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="122cb-261">VendPay</span></span>  
4. <span data-ttu-id="122cb-262">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="122cb-262">Click Lines.</span></span>
5. <span data-ttu-id="122cb-263">Määritä Tili-kenttään arvo GB_SI_000001.</span><span class="sxs-lookup"><span data-stu-id="122cb-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="122cb-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="122cb-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="122cb-265">Aseta veloitusarvoksi 1000.</span><span class="sxs-lookup"><span data-stu-id="122cb-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="122cb-266">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="122cb-266">Click New.</span></span>
8. <span data-ttu-id="122cb-267">Määritä Tili-kenttään arvo GB_SI_000005.</span><span class="sxs-lookup"><span data-stu-id="122cb-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="122cb-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="122cb-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="122cb-269">Aseta veloitusarvoksi 2000.</span><span class="sxs-lookup"><span data-stu-id="122cb-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="122cb-270">Anna Valuutta-kentän arvoksi EUR.</span><span class="sxs-lookup"><span data-stu-id="122cb-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="122cb-271">Euro</span><span class="sxs-lookup"><span data-stu-id="122cb-271">EUR</span></span>  
11. <span data-ttu-id="122cb-272">Määritä Vastatili-kenttään arvo GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="122cb-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="122cb-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="122cb-273">GBSI OPER</span></span>  
12. <span data-ttu-id="122cb-274">Syötä Maksutapa-kentän arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="122cb-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="122cb-275">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="122cb-275">Electronic</span></span>  
13. <span data-ttu-id="122cb-276">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="122cb-276">Click Save.</span></span>
14. <span data-ttu-id="122cb-277">Valitse Muodosta maksut.</span><span class="sxs-lookup"><span data-stu-id="122cb-277">Click Generate payments.</span></span>
15. <span data-ttu-id="122cb-278">Syötä Maksutapa-kentän arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="122cb-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="122cb-279">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="122cb-279">Electronic</span></span>  
16. <span data-ttu-id="122cb-280">Kirjoita Tiedostonimi-kenttään Maksut.</span><span class="sxs-lookup"><span data-stu-id="122cb-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="122cb-281">Kirjoita esimerkiksi Maksut.</span><span class="sxs-lookup"><span data-stu-id="122cb-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="122cb-282">Anna Pankkitili-kentän arvoksi GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="122cb-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="122cb-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="122cb-283">GBSI OPER</span></span>  
18. <span data-ttu-id="122cb-284">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="122cb-284">Click OK.</span></span>
19. <span data-ttu-id="122cb-285">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="122cb-285">Click OK.</span></span>
    * <span data-ttu-id="122cb-286">Tarkista luotu taulukko, mukaan lukien maksutietorivit sekä jokaisen tässä maksusanomassa käytetyn valuuttakoodin kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="122cb-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

