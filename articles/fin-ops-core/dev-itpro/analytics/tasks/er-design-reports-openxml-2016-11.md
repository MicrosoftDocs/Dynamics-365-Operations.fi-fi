---
title: ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)
description: Tässä aiheessa käsitellään sellaisen uuden sähköisen raportoinnin määrityksen luontia, joka sisältää OPENXML-muotoisen sähköisten asiakirjojen luontimallin.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b832961061d05e3f1ae046f820bc7a37baaf90c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092663"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="0b200-103">ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="0b200-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b200-104">Tässä aiheessa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin.</span><span class="sxs-lookup"><span data-stu-id="0b200-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="0b200-105">Tätä konfiguraatiota käytetään toimittajamaksujen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="0b200-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="0b200-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="0b200-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="0b200-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="0b200-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="0b200-108">Sinulla on myös oltava Excel-tiedosto, joka tuodaan mallia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="0b200-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="0b200-109">Tätä tiedostoa voi käyttää kohdasta [Maksuilmoituksen malli](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="0b200-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="0b200-110">Lataa maksujen tietomallin konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="0b200-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="0b200-111">Siirry kohtaan **siirtymisruutu > Moduulit > organisaation hallinto > Työtilat > Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="0b200-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="0b200-112">Valitse luettelossa malliyrityksen määrityksen lähde Litware, Inc. Jos lähde ei ole näkyvissä, suorita ensin kohdan [Konfiguraation lähteiden luominen ja sen merkitseminen aktiiviseksi](er-configuration-provider-mark-it-active-2016-11.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0b200-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don't see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="0b200-113">Valitse **Määritä aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="0b200-113">Select **Set active**.</span></span>
4. <span data-ttu-id="0b200-114">Valitse **Säilöt**.</span><span class="sxs-lookup"><span data-stu-id="0b200-114">Select **Repositories**.</span></span> <span data-ttu-id="0b200-115">Jos operatiivisen resurssityypin säilö on käytettävissä, valitse se.</span><span class="sxs-lookup"><span data-stu-id="0b200-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="0b200-116">Jos säilö on käytettävissä, ohita seuraavat, uuden säilön luomista koskevat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0b200-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="0b200-117">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="0b200-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="0b200-118">Syötä **Konfiguraatiosäilön tyyppi** -kentän arvoksi `Operations resourcesdd`.</span><span class="sxs-lookup"><span data-stu-id="0b200-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="0b200-119">Valitse **Luo säilö**.</span><span class="sxs-lookup"><span data-stu-id="0b200-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="0b200-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b200-120">Select **OK**.</span></span>
9. <span data-ttu-id="0b200-121">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="0b200-121">Select **Open**.</span></span>
10. <span data-ttu-id="0b200-122">Valitse puussa solmu **Maksumalli**.</span><span class="sxs-lookup"><span data-stu-id="0b200-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="0b200-123">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="0b200-123">Select **Import**.</span></span> <span data-ttu-id="0b200-124">Tuo tämä tietomalli.</span><span class="sxs-lookup"><span data-stu-id="0b200-124">Import this data model.</span></span> <span data-ttu-id="0b200-125">Sitä käytetään uuden muotokonfiguraation tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="0b200-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="0b200-126">Ohita tämä vaihe, jos tämä konfiguraatio on tuotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="0b200-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="0b200-127">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0b200-127">Select **Yes**.</span></span>
13. <span data-ttu-id="0b200-128">Sulje sivut, kunnes palaat Sähköinen raportointi -sivulle.</span><span class="sxs-lookup"><span data-stu-id="0b200-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="0b200-129">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="0b200-129">Create a new format configuration</span></span>
1. <span data-ttu-id="0b200-130">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="0b200-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="0b200-131">Valitse puussa solmu **Maksumalli**.</span><span class="sxs-lookup"><span data-stu-id="0b200-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="0b200-132">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="0b200-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="0b200-133">Kirjoita **Uusi**- kenttään arvo `Format based on data model PaymentModel`.</span><span class="sxs-lookup"><span data-stu-id="0b200-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="0b200-134">Luo muoto, joka perustuu PaymentModel-tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="0b200-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="0b200-135">Syötä **Nimi**-kenttään `Sample worksheet report`.</span><span class="sxs-lookup"><span data-stu-id="0b200-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="0b200-136">Laskentataulukkoraportin esimerkki</span><span class="sxs-lookup"><span data-stu-id="0b200-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="0b200-137">Kirjoita **Kuvaus**-kenttään `Sample worksheet report for vendors' payments`.</span><span class="sxs-lookup"><span data-stu-id="0b200-137">In the **Description** field, type `Sample worksheet report for vendors' payments`.</span></span> <span data-ttu-id="0b200-138">Toimittajamaksujen laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="0b200-138">Sample worksheet report for vendors' payments.</span></span>  
7. <span data-ttu-id="0b200-139">Anna tai valitse **Tietomallin määritelmä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="0b200-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="0b200-140">Valitse **CustomerCreditTransferInitiation**-määritelmä.</span><span class="sxs-lookup"><span data-stu-id="0b200-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="0b200-141">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="0b200-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="0b200-142">Suunnittele uusi asiakirja OPENXML-laskentataulukkomuodossa</span><span class="sxs-lookup"><span data-stu-id="0b200-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="0b200-143">Valitse puusta **Maksumalli\Laskentataulukkoraportin esimerkki**.</span><span class="sxs-lookup"><span data-stu-id="0b200-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="0b200-144">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="0b200-144">Select **Designer**.</span></span>
3. <span data-ttu-id="0b200-145">Valitse toimintoruudussa **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="0b200-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="0b200-146">Valitse **Tuo Excelistä**.</span><span class="sxs-lookup"><span data-stu-id="0b200-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="0b200-147">Valitse **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="0b200-147">Select **Attachments**.</span></span> <span data-ttu-id="0b200-148">Liitä aiemmin luotu Excel-asiakirja mallina.</span><span class="sxs-lookup"><span data-stu-id="0b200-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="0b200-149">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b200-149">Select **New**.</span></span>
7. <span data-ttu-id="0b200-150">Valitse **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="0b200-150">Select **File**.</span></span> <span data-ttu-id="0b200-151">Osoita aiemmin luotu Excel-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="0b200-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="0b200-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b200-152">Close the page.</span></span>
9. <span data-ttu-id="0b200-153">Syötä tai valitse **Malli**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="0b200-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="0b200-154">Valitse liitetty Excel-tiedosto käytettäväksi mallina.</span><span class="sxs-lookup"><span data-stu-id="0b200-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="0b200-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b200-155">Select **OK**.</span></span> <span data-ttu-id="0b200-156">Huomaa, ER-muodon osat on luotu suunnittelumuodossa, joka perustuu viittaavan MS Excel -tiedoston rakenteeseen (nimetyt alueet).</span><span class="sxs-lookup"><span data-stu-id="0b200-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="0b200-157">Luo uusi tietolähde kokonaissummien laskentaan valuuttakoodien perusteella</span><span class="sxs-lookup"><span data-stu-id="0b200-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="0b200-158">Valitse **Yhdistämismääritys**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0b200-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="0b200-159">Avaa valintaikkuna valitsemalla **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="0b200-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="0b200-160">Valitse valikkopuussa **Toiminnot\Ryhmittely**.</span><span class="sxs-lookup"><span data-stu-id="0b200-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="0b200-161">Syötä **Nimi**-kenttään `PaymentByCurrency`.</span><span class="sxs-lookup"><span data-stu-id="0b200-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="0b200-162">Napsauta **Muokkaa ryhmittelyä**.</span><span class="sxs-lookup"><span data-stu-id="0b200-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="0b200-163">Laajenna puurakenteessa **model** ja valitse sitten **model\payments**.</span><span class="sxs-lookup"><span data-stu-id="0b200-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="0b200-164">Valitse **Lisää kenttä kohteeseen**.</span><span class="sxs-lookup"><span data-stu-id="0b200-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="0b200-165">Napsauta **Mitä ryhmään**.</span><span class="sxs-lookup"><span data-stu-id="0b200-165">Select **What to group**.</span></span>
9. <span data-ttu-id="0b200-166">Laajenna puurakenteessa **model\Payments** ja valitse sitten **model\Payments\Currency**.</span><span class="sxs-lookup"><span data-stu-id="0b200-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="0b200-167">Valitse **Lisää kenttä kohteeseen**.</span><span class="sxs-lookup"><span data-stu-id="0b200-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="0b200-168">Valitse **Ryhmitellyt kentät**.</span><span class="sxs-lookup"><span data-stu-id="0b200-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="0b200-169">Valitse puussa solmu **model\Payments\Instructed Amount(InstructedAmount)**.</span><span class="sxs-lookup"><span data-stu-id="0b200-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="0b200-170">Valitse **Lisää kenttä kohteeseen** ja valitse sitten **Koostekentät**.</span><span class="sxs-lookup"><span data-stu-id="0b200-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="0b200-171">Valitse vaihtoehto **Menetelmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b200-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="0b200-172">Valitse koostefunktioksi **SUMMA**.</span><span class="sxs-lookup"><span data-stu-id="0b200-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="0b200-173">Syötä **Nimi**-kenttään `TotalInstructuredAmount`.</span><span class="sxs-lookup"><span data-stu-id="0b200-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="0b200-174">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0b200-174">Select **Save**.</span></span>
17. <span data-ttu-id="0b200-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b200-175">Close the page.</span></span>
18. <span data-ttu-id="0b200-176">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b200-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="0b200-177">Määritä muodon komponentit tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="0b200-177">Map format components to data sources</span></span>
1. <span data-ttu-id="0b200-178">Valitse puussa **model\Payments\Initiating Party(InitiatingParty)\Name** ja **Excel\ReportHeader\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="0b200-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="0b200-179">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-179">Select **Bind**.</span></span>
3. <span data-ttu-id="0b200-180">Valitse puussa **model\Payments\Creditor\Identification\Source ID(SourceID)** ja **Excel\PaymLines\VendAccountName**.</span><span class="sxs-lookup"><span data-stu-id="0b200-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="0b200-181">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-181">Select **Bind**.</span></span>
5. <span data-ttu-id="0b200-182">Valitse puussa **model\Payments\Creditor\Name** ja **Excel\PaymLines\VendName**.</span><span class="sxs-lookup"><span data-stu-id="0b200-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="0b200-183">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-183">Select **Bind**.</span></span>
7. <span data-ttu-id="0b200-184">Valitse puussa **model\Payments\Creditor Agent(CreditorAgent)\Name** ja **Excel\PaymLines\Bank**.</span><span class="sxs-lookup"><span data-stu-id="0b200-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="0b200-185">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-185">Select **Bind**.</span></span>
9. <span data-ttu-id="0b200-186">Valitse puussa **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** ja **Excel\PaymLines\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="0b200-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="0b200-187">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-187">Select **Bind**.</span></span>
11. <span data-ttu-id="0b200-188">Valitse puussa **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** ja **Excel\PaymLines\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="0b200-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="0b200-189">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-189">Select **Bind**.</span></span>
13. <span data-ttu-id="0b200-190">Valitse puussa **model\Payments\Instructed Amount(InstructedAmount)** ja **Excel\PaymLines\Debit**.</span><span class="sxs-lookup"><span data-stu-id="0b200-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="0b200-191">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-191">Select **Bind**.</span></span>
15. <span data-ttu-id="0b200-192">Valitse puussa **model\Payments\Currency** ja **Excel\PaymLines\Currency**.</span><span class="sxs-lookup"><span data-stu-id="0b200-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="0b200-193">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-193">Select **Bind**.</span></span>
17. <span data-ttu-id="0b200-194">Valitse puussa **PaymentByCurrency\grouped\Currency** ja **Excel\SummaryLines\SummaryCurrency**.</span><span class="sxs-lookup"><span data-stu-id="0b200-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="0b200-195">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-195">Select **Bind**.</span></span>
19. <span data-ttu-id="0b200-196">Valitse puussa **PaymentByCurrency\aggregated\TotalInstructuredAmount** ja **Excel\SummaryLines\SummaryAmount**.</span><span class="sxs-lookup"><span data-stu-id="0b200-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="0b200-197">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-197">Select **Bind**.</span></span>
21. <span data-ttu-id="0b200-198">Valitse puussa **PaymentByCurrency** ja **Excel\SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="0b200-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="0b200-199">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-199">Select **Bind**.</span></span>
23. <span data-ttu-id="0b200-200">Valitse puussa **model\Payments** ja **Excel\PaymLines**.</span><span class="sxs-lookup"><span data-stu-id="0b200-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="0b200-201">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="0b200-201">Select **Bind**.</span></span>
25. <span data-ttu-id="0b200-202">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="0b200-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="0b200-203">Käytä luotua määritystä maksujen käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="0b200-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="0b200-204">Valitse **Muutoksen tila**.</span><span class="sxs-lookup"><span data-stu-id="0b200-204">Select **Change status**.</span></span>
2. <span data-ttu-id="0b200-205">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="0b200-205">Select **Complete**.</span></span>
3. <span data-ttu-id="0b200-206">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b200-206">Select **OK**.</span></span>
4. <span data-ttu-id="0b200-207">Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra >Maksujen asetukset > Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="0b200-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="0b200-208">Voit suodattaa **Maksutapa**-kentän pikasuodattimella käyttämällä **Sähköinen**-arvoa.</span><span class="sxs-lookup"><span data-stu-id="0b200-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="0b200-209">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="0b200-209">Select **Edit**.</span></span>
7. <span data-ttu-id="0b200-210">Laajenna **Tiedostomuodot**-osa.</span><span class="sxs-lookup"><span data-stu-id="0b200-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="0b200-211">Valitse **Yleinen sähköinen raportointi** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0b200-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="0b200-212">Syötä **Vie muotokonfiguraatio** -kenttään arvo tai valitse arvo.</span><span class="sxs-lookup"><span data-stu-id="0b200-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="0b200-213">Valitse **Laskentataulukkoraportin esimerkki** -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="0b200-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="0b200-214">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0b200-214">Select **Save**.</span></span>
11. <span data-ttu-id="0b200-215">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b200-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="0b200-216">Käytä luotua konfiguraatiota maksukirjauskansioiden käsittelemisen testaamiseen</span><span class="sxs-lookup"><span data-stu-id="0b200-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="0b200-217">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Maksut > Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="0b200-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="0b200-218">Luo uusi maksukirjauskansio valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b200-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="0b200-219">Kirjoita **Nimi**-kenttään **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="0b200-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="0b200-220">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="0b200-220">Select **Lines**.</span></span>
5. <span data-ttu-id="0b200-221">Määritä **Tili**-kentässä arvo `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="0b200-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="0b200-222">Aseta **Debet**-kentän arvoksi `1000`.</span><span class="sxs-lookup"><span data-stu-id="0b200-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="0b200-223">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b200-223">Select **New**.</span></span>
8. <span data-ttu-id="0b200-224">Määritä **Tili**-kentässä arvo `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="0b200-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="0b200-225">Aseta **Debet**-kentän arvoksi `2000`.</span><span class="sxs-lookup"><span data-stu-id="0b200-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="0b200-226">Anna **Valuutta**-kentän arvoksi `EUR`.</span><span class="sxs-lookup"><span data-stu-id="0b200-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="0b200-227">Määritä **Vastatili**-kenttään arvo `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="0b200-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="0b200-228">Kirjoita **Maksutapa**-kenttään `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="0b200-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="0b200-229">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0b200-229">Select **Save**.</span></span>
14. <span data-ttu-id="0b200-230">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="0b200-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="0b200-231">Kirjoita **Maksutapa**-kenttään `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="0b200-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="0b200-232">Kirjoita **Tiedoston nimi** -kenttään `Payments`.</span><span class="sxs-lookup"><span data-stu-id="0b200-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="0b200-233">Anna **Pankkitili**-kentän arvoksi `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="0b200-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="0b200-234">Valitse ensin **OK** ja sitten uudelleen **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b200-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="0b200-235">Tarkista luotu taulukko, mukaan lukien maksutietorivit sekä jokaisen tässä maksusanomassa käytetyn valuuttakoodin kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="0b200-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

