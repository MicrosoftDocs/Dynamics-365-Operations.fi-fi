--- 
title: "Konfiguraation suunnitteleminen raporttien luomiseksi OpenXML-muodossa sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 882799e12daf9a3b7b530201c913b8f921fb2ed3
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="c9339-103">Konfiguraation suunnitteleminen raporttien luomiseksi OpenXML-muodossa sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="c9339-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9339-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation, joka sisältää sähköisen asiakirjojen OPENXML-muodon luontimallin.</span><span class="sxs-lookup"><span data-stu-id="c9339-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="c9339-105">Tätä konfiguraatiota käytetään toimittajamaksujen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="c9339-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="c9339-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c9339-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="c9339-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="c9339-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="c9339-108">Lataa ja tallenna myös Microsoft Excel -tiedosto, [Maksuraportin malli](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="c9339-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="c9339-109">Lataa maksujen tietomallin konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="c9339-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="c9339-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="c9339-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c9339-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c9339-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c9339-112">Valitse malliyrityksen konfiguraation lähde Litware, Inc. Jos lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c9339-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="c9339-113">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="c9339-113">Click Set active.</span></span>
4. <span data-ttu-id="c9339-114">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="c9339-114">Click Repositories.</span></span>
    * <span data-ttu-id="c9339-115">Jos operatiivisen resurssityypin säilö on käytettävissä, valitse se.</span><span class="sxs-lookup"><span data-stu-id="c9339-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="c9339-116">Jos säilö on käytettävissä, ohita seuraavat, uuden säilön luomista koskevat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c9339-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="c9339-117">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="c9339-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="c9339-118">Kirjoita Konfiguraatiosäilön tyyppi -kentän arvoksi Operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="c9339-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="c9339-119">Valitse Luo säilö.</span><span class="sxs-lookup"><span data-stu-id="c9339-119">Click Create repository.</span></span>
8. <span data-ttu-id="c9339-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9339-120">Click OK.</span></span>
9. <span data-ttu-id="c9339-121">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="c9339-121">Click Open.</span></span>
10. <span data-ttu-id="c9339-122">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="c9339-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="c9339-123">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="c9339-123">Click Import.</span></span>
    * <span data-ttu-id="c9339-124">Tuo tämä tietomalli.</span><span class="sxs-lookup"><span data-stu-id="c9339-124">Import this data model.</span></span> <span data-ttu-id="c9339-125">Sitä käytetään uuden muotokonfiguraation tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="c9339-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="c9339-126">Ohita tämä vaihe, jos tämä konfiguraatio on tuotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="c9339-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="c9339-127">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c9339-127">Click Yes.</span></span>
13. <span data-ttu-id="c9339-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-128">Close the page.</span></span>
14. <span data-ttu-id="c9339-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="c9339-130">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="c9339-130">Create a new format configuration</span></span>
1. <span data-ttu-id="c9339-131">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="c9339-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="c9339-132">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="c9339-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="c9339-133">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="c9339-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="c9339-134">Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="c9339-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="c9339-135">Luo muoto, joka perustuu PaymentModel-tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="c9339-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="c9339-136">Kirjoita Nimi-kentän arvoksi Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="c9339-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="c9339-137">Laskentataulukkoraportin esimerkki</span><span class="sxs-lookup"><span data-stu-id="c9339-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="c9339-138">Kirjoita Kuvaus-kentän arvoksi Toimittajamaksujen laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="c9339-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="c9339-139">Toimittajamaksujen laskentataulukkoraportin esimerkki</span><span class="sxs-lookup"><span data-stu-id="c9339-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="c9339-140">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="c9339-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="c9339-141">Valitse CustomerCreditTransferInitiation-määritelmä.</span><span class="sxs-lookup"><span data-stu-id="c9339-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="c9339-142">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="c9339-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="c9339-143">Suunnittele uusi asiakirja OPENXML-laskentataulukkomuodossa</span><span class="sxs-lookup"><span data-stu-id="c9339-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="c9339-144">Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="c9339-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="c9339-145">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="c9339-145">Click Designer.</span></span>
3. <span data-ttu-id="c9339-146">Valitse toimintoruudussa Tuo.</span><span class="sxs-lookup"><span data-stu-id="c9339-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="c9339-147">Napsauta Tuo Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="c9339-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="c9339-148">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="c9339-148">Click Attachments.</span></span>
    * <span data-ttu-id="c9339-149">Liitä aiemmin luotu Excel-asiakirja mallina.</span><span class="sxs-lookup"><span data-stu-id="c9339-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="c9339-150">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c9339-150">Click New.</span></span>
7. <span data-ttu-id="c9339-151">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="c9339-151">Click File.</span></span>
    * <span data-ttu-id="c9339-152">Osoita aiemmin luotu Excel-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="c9339-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="c9339-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-153">Close the page.</span></span>
9. <span data-ttu-id="c9339-154">Syötä tai valitse Malli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="c9339-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="c9339-155">Valitse liitetty Excel-tiedosto käytettäväksi mallina.</span><span class="sxs-lookup"><span data-stu-id="c9339-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="c9339-156">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9339-156">Click OK.</span></span>
    * <span data-ttu-id="c9339-157">Huomaa, ER-muodon osat on luotu suunnittelumuodossa, joka perustuu viittaavan MS Excel -tiedoston rakenteeseen (nimetyt alueet).</span><span class="sxs-lookup"><span data-stu-id="c9339-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="c9339-158">Luo uusi tietolähde kokonaissummien laskentaan valuuttakoodien perusteella</span><span class="sxs-lookup"><span data-stu-id="c9339-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="c9339-159">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c9339-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c9339-160">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="c9339-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c9339-161">Valitse valikkopuussa Toiminnot\Ryhmittely.</span><span class="sxs-lookup"><span data-stu-id="c9339-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="c9339-162">Kirjoita Nimi-kenttään PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="c9339-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="c9339-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="c9339-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="c9339-164">Napsauta Muokkaa ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="c9339-164">Click Edit group by.</span></span>
6. <span data-ttu-id="c9339-165">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="c9339-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="c9339-166">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="c9339-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="c9339-167">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="c9339-167">Click Add field to.</span></span>
9. <span data-ttu-id="c9339-168">Napsauta Mitä ryhmään.</span><span class="sxs-lookup"><span data-stu-id="c9339-168">Click What to group.</span></span>
10. <span data-ttu-id="c9339-169">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="c9339-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="c9339-170">Valitse puussa solmu Malli\Maksut\Kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c9339-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="c9339-171">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="c9339-171">Click Add field to.</span></span>
13. <span data-ttu-id="c9339-172">Napsauta Ryhmitellyt kentät.</span><span class="sxs-lookup"><span data-stu-id="c9339-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="c9339-173">Valitse puussa solmu Malli\Maksut\Ohjattu summa(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="c9339-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="c9339-174">Napsauta Lisää kenttä kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="c9339-174">Click Add field to.</span></span>
16. <span data-ttu-id="c9339-175">Napsauta Koostekentät.</span><span class="sxs-lookup"><span data-stu-id="c9339-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="c9339-176">Valitse vaihtoehto Menetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c9339-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="c9339-177">Valitse koostefunktioksi SUMMA.</span><span class="sxs-lookup"><span data-stu-id="c9339-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="c9339-178">Kirjoita Nimi-kenttään TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="c9339-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="c9339-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="c9339-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="c9339-180">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c9339-180">Click Save.</span></span>
20. <span data-ttu-id="c9339-181">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-181">Close the page.</span></span>
21. <span data-ttu-id="c9339-182">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9339-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="c9339-183">Määritä muodon komponentit tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="c9339-183">Map format components to data sources</span></span>
1. <span data-ttu-id="c9339-184">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="c9339-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="c9339-185">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="c9339-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="c9339-186">Laajenna puussa solmu Malli\Maksut\Aloittava osapuoli(InitiatingParty).</span><span class="sxs-lookup"><span data-stu-id="c9339-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="c9339-187">Valitse puussa solmu Malli\Maksut\Aloittava osapuoli(InitiatingParty)\Nimi.</span><span class="sxs-lookup"><span data-stu-id="c9339-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="c9339-188">Valitse puussa Excel\ReportHeader.</span><span class="sxs-lookup"><span data-stu-id="c9339-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="c9339-189">Valitse puussa Excel\ReportHeader\CompanyName.</span><span class="sxs-lookup"><span data-stu-id="c9339-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="c9339-190">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-190">Click Bind.</span></span>
8. <span data-ttu-id="c9339-191">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="c9339-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="c9339-192">Laajenna puussa solmu Malli\Maksut\Laskuttaja\Tunnus.</span><span class="sxs-lookup"><span data-stu-id="c9339-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="c9339-193">Laajenna puussa Malli\Maksut\Laskuttaja\Tunnus\Lähdetunnus(SourceID).</span><span class="sxs-lookup"><span data-stu-id="c9339-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="c9339-194">Valitse puussa Excel\PaymLines.</span><span class="sxs-lookup"><span data-stu-id="c9339-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="c9339-195">Valitse puussa Excel\PaymLines\VendAccountName.</span><span class="sxs-lookup"><span data-stu-id="c9339-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="c9339-196">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-196">Click Bind.</span></span>
14. <span data-ttu-id="c9339-197">Valitse puussa solmu model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="c9339-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="c9339-198">Valitse puussa Excel\PaymLines\VendName.</span><span class="sxs-lookup"><span data-stu-id="c9339-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="c9339-199">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-199">Click Bind.</span></span>
17. <span data-ttu-id="c9339-200">Laajenna puussa Malli\Maksut\Laskuttajan edustaja(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="c9339-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="c9339-201">Valitse puussa solmu Malli\Maksut\Laskuttajan edustaja(CreditorAgent)\Nimi.</span><span class="sxs-lookup"><span data-stu-id="c9339-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="c9339-202">Valitse puussa Excel\PaymLines\Pankki.</span><span class="sxs-lookup"><span data-stu-id="c9339-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="c9339-203">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-203">Click Bind.</span></span>
21. <span data-ttu-id="c9339-204">Valitse puussa solmu Malli\Maksut\Laskuttajan edustaja(CreditorAgent)\Reititysnumero(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="c9339-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="c9339-205">Valitse puussa Excel\PaymLines\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="c9339-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="c9339-206">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-206">Click Bind.</span></span>
24. <span data-ttu-id="c9339-207">Laajenna puussa model\Payments\Creditor Account(CreditorAccount).</span><span class="sxs-lookup"><span data-stu-id="c9339-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="c9339-208">Laajenna puussa model\Payments\Creditor Account(CreditorAccount)\Identification.</span><span class="sxs-lookup"><span data-stu-id="c9339-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="c9339-209">Valitse puussa Malli\Maksut\Laskuttajan tili(CreditorAccount)\Tunnus\Numero.</span><span class="sxs-lookup"><span data-stu-id="c9339-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="c9339-210">Valitse puussa Excel\PaymLines\AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="c9339-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="c9339-211">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-211">Click Bind.</span></span>
29. <span data-ttu-id="c9339-212">Valitse puussa solmu Malli\Maksut\Ohjattu summa(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="c9339-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="c9339-213">Valitse puussa Excel\PaymLines\Veloitus.</span><span class="sxs-lookup"><span data-stu-id="c9339-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="c9339-214">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-214">Click Bind.</span></span>
32. <span data-ttu-id="c9339-215">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="c9339-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="c9339-216">Laajenna puussa model\Payments\Creditor Account(CreditorAccount).</span><span class="sxs-lookup"><span data-stu-id="c9339-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="c9339-217">Laajenna puussa Malli\Maksut\Laskuttajan edustaja(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="c9339-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="c9339-218">Valitse puussa solmu Malli\Maksut\Kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c9339-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="c9339-219">Valitse puussa Excel\PaymLines\Valuutta.</span><span class="sxs-lookup"><span data-stu-id="c9339-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="c9339-220">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-220">Click Bind.</span></span>
38. <span data-ttu-id="c9339-221">Laajenna puussa PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="c9339-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="c9339-222">Laajenna puussa PaymentByCurrency\ryhmitelty.</span><span class="sxs-lookup"><span data-stu-id="c9339-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="c9339-223">Valitse puussa PaymentByCurrency\ryhmitelty\Valuutta.</span><span class="sxs-lookup"><span data-stu-id="c9339-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="c9339-224">Laajenna puussa Excel\SummaryLines.</span><span class="sxs-lookup"><span data-stu-id="c9339-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="c9339-225">Valitse puussa Excel\SummaryLines\SummaryCurrency.</span><span class="sxs-lookup"><span data-stu-id="c9339-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="c9339-226">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-226">Click Bind.</span></span>
44. <span data-ttu-id="c9339-227">Laajenna puussa PaymentByCurrency\koottu.</span><span class="sxs-lookup"><span data-stu-id="c9339-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="c9339-228">Valitse puussa PaymentByCurrency\koottu\TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="c9339-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="c9339-229">Valitse puussa Excel\SummaryLines\SummaryAmount.</span><span class="sxs-lookup"><span data-stu-id="c9339-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="c9339-230">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-230">Click Bind.</span></span>
48. <span data-ttu-id="c9339-231">Valitse puussa solmu PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="c9339-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="c9339-232">Valitse puussa Excel\SummaryLines.</span><span class="sxs-lookup"><span data-stu-id="c9339-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="c9339-233">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-233">Click Bind.</span></span>
51. <span data-ttu-id="c9339-234">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="c9339-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="c9339-235">Valitse puussa Excel\PaymLines.</span><span class="sxs-lookup"><span data-stu-id="c9339-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="c9339-236">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c9339-236">Click Bind.</span></span>
54. <span data-ttu-id="c9339-237">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c9339-237">Click Save.</span></span>
55. <span data-ttu-id="c9339-238">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="c9339-239">Käytä luotua määritystä maksujen käsittelyssä</span><span class="sxs-lookup"><span data-stu-id="c9339-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="c9339-240">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="c9339-240">Click Change status.</span></span>
2. <span data-ttu-id="c9339-241">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="c9339-241">Click Complete.</span></span>
3. <span data-ttu-id="c9339-242">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9339-242">Click OK.</span></span>
4. <span data-ttu-id="c9339-243">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-243">Close the page.</span></span>
5. <span data-ttu-id="c9339-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-244">Close the page.</span></span>
6. <span data-ttu-id="c9339-245">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="c9339-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="c9339-246">Voit suodattaa Maksutapa-kentän pikasuodattimella käyttämällä Sähköinen-arvoa.</span><span class="sxs-lookup"><span data-stu-id="c9339-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="c9339-247">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="c9339-247">Electronic</span></span>  
8. <span data-ttu-id="c9339-248">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c9339-248">Click Edit.</span></span>
9. <span data-ttu-id="c9339-249">Laajenna Tiedostomuodot-osa.</span><span class="sxs-lookup"><span data-stu-id="c9339-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="c9339-250">Valitse Yleinen sähköinen raportointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c9339-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="c9339-251">Syötä Vie muotokonfiguraatio -kenttään arvo tai valitse arvo.</span><span class="sxs-lookup"><span data-stu-id="c9339-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="c9339-252">Valitse Laskentataulukkoraportin esimerkki -konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="c9339-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="c9339-253">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c9339-253">Click Save.</span></span>
13. <span data-ttu-id="c9339-254">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c9339-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="c9339-255">Käytä luotua konfiguraatiota maksukirjauskansioiden käsittelemisen testaamiseen</span><span class="sxs-lookup"><span data-stu-id="c9339-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="c9339-256">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="c9339-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c9339-257">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c9339-257">Click New.</span></span>
    * <span data-ttu-id="c9339-258">Luo uusi maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="c9339-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="c9339-259">Kirjoita Nimi-kenttään VendPay.</span><span class="sxs-lookup"><span data-stu-id="c9339-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="c9339-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="c9339-260">VendPay</span></span>  
4. <span data-ttu-id="c9339-261">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="c9339-261">Click Lines.</span></span>
5. <span data-ttu-id="c9339-262">Määritä Tili-kenttään arvo GB_SI_000001.</span><span class="sxs-lookup"><span data-stu-id="c9339-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="c9339-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="c9339-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="c9339-264">Aseta veloitusarvoksi 1000.</span><span class="sxs-lookup"><span data-stu-id="c9339-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="c9339-265">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c9339-265">Click New.</span></span>
8. <span data-ttu-id="c9339-266">Määritä Tili-kenttään arvo GB_SI_000005.</span><span class="sxs-lookup"><span data-stu-id="c9339-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="c9339-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="c9339-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="c9339-268">Aseta veloitusarvoksi 2000.</span><span class="sxs-lookup"><span data-stu-id="c9339-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="c9339-269">Anna Valuutta-kentän arvoksi EUR.</span><span class="sxs-lookup"><span data-stu-id="c9339-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="c9339-270">Euro</span><span class="sxs-lookup"><span data-stu-id="c9339-270">EUR</span></span>  
11. <span data-ttu-id="c9339-271">Määritä Vastatili-kenttään arvo GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="c9339-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="c9339-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="c9339-272">GBSI OPER</span></span>  
12. <span data-ttu-id="c9339-273">Syötä Maksutapa-kentän arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="c9339-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="c9339-274">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="c9339-274">Electronic</span></span>  
13. <span data-ttu-id="c9339-275">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c9339-275">Click Save.</span></span>
14. <span data-ttu-id="c9339-276">Valitse Muodosta maksut.</span><span class="sxs-lookup"><span data-stu-id="c9339-276">Click Generate payments.</span></span>
15. <span data-ttu-id="c9339-277">Syötä Maksutapa-kentän arvoksi Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="c9339-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="c9339-278">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="c9339-278">Electronic</span></span>  
16. <span data-ttu-id="c9339-279">Kirjoita Tiedostonimi-kenttään Maksut.</span><span class="sxs-lookup"><span data-stu-id="c9339-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="c9339-280">Kirjoita esimerkiksi Maksut.</span><span class="sxs-lookup"><span data-stu-id="c9339-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="c9339-281">Anna Pankkitili-kentän arvoksi GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="c9339-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="c9339-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="c9339-282">GBSI OPER</span></span>  
18. <span data-ttu-id="c9339-283">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9339-283">Click OK.</span></span>
19. <span data-ttu-id="c9339-284">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c9339-284">Click OK.</span></span>
    * <span data-ttu-id="c9339-285">Tarkista luotu taulukko, mukaan lukien maksutietorivit sekä jokaisen tässä maksusanomassa käytetyn valuuttakoodin kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="c9339-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


