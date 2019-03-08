---
title: Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa
description: Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää sähköisen raportoinnin muotoja luomaan raportteja Microsoft Word -tiedostoina.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "362346"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="df4cd-103">Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa</span><span class="sxs-lookup"><span data-stu-id="df4cd-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df4cd-104">Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää sähköisen raportoinnin (ER) muotoja luomaan raportteja Microsoft Word -tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="df4cd-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="df4cd-105">Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="df4cd-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="df4cd-106">Näiden vaiheiden suorittaminen edellyttää, että ER-määrityksen luonti OPENXML-muotoisten raporttien luomiseksi -tehtäväoppaan vaiheet on suoritettu ensin.</span><span class="sxs-lookup"><span data-stu-id="df4cd-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="df4cd-107">Lisäksi malliraporttia varten on etukäteen ladattava ja tallennettava paikallisesti seuraavat mallit:</span><span class="sxs-lookup"><span data-stu-id="df4cd-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="df4cd-108">Maksuraportin malli</span><span class="sxs-lookup"><span data-stu-id="df4cd-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="df4cd-109">Maksuraportin sidottu malli</span><span class="sxs-lookup"><span data-stu-id="df4cd-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="df4cd-110">Nämä ohjeet koskevat toimintoa, joka lisättiin Microsoft Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="df4cd-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="df4cd-111">Aiemmin luodun ER-raporttimäärityksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="df4cd-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="df4cd-112">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="df4cd-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="df4cd-113">Varmista, että konfiguraation lähde, Litware Inc.,</span><span class="sxs-lookup"><span data-stu-id="df4cd-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="df4cd-114">on valittu aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="df4cd-114">is selected as active.</span></span>  
2. <span data-ttu-id="df4cd-115">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="df4cd-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="df4cd-116">Käytämme aiemmin luotuja ER-määrityksiä, jotka on alun perin suunniteltu luomaan raportti OPENXML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="df4cd-117">Laajenna puussa solmu Payment model.</span><span class="sxs-lookup"><span data-stu-id="df4cd-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="df4cd-118">Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="df4cd-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="df4cd-119">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="df4cd-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="df4cd-120">Excel-malliin korvaaminen Word-mallilla</span><span class="sxs-lookup"><span data-stu-id="df4cd-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="df4cd-121">Tällä hetkellä OPENXML-muotoisen raportin luonnissa käytetään mallina Excel-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="df4cd-122">Raporttimalli tuodaan Word-muodossa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="df4cd-123">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="df4cd-123">Click Attachments.</span></span>
    * <span data-ttu-id="df4cd-124">Korvaa aiemmin luotu Excel-malli aiemmin ladatulla Word-mallilla SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="df4cd-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="df4cd-125">Huomaa, että tässä mallissa on vain ER-raporttina luotavan asiakirjan asettelu.</span><span class="sxs-lookup"><span data-stu-id="df4cd-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="df4cd-126">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="df4cd-126">Click Delete.</span></span>
3. <span data-ttu-id="df4cd-127">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="df4cd-127">Click Yes.</span></span>
4. <span data-ttu-id="df4cd-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="df4cd-128">Click New.</span></span>
5. <span data-ttu-id="df4cd-129">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="df4cd-129">Click File.</span></span>
6. <span data-ttu-id="df4cd-130">Valitse Selaa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-130">Click Browse.</span></span> <span data-ttu-id="df4cd-131">Siirry aiemmin ladattuun asiakirjaan SampleVendPaymDocReport.docx ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="df4cd-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="df4cd-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="df4cd-132">Click OK.</span></span>
    * <span data-ttu-id="df4cd-133">Valitse edellisessä vaiheessa lataamasi malli.</span><span class="sxs-lookup"><span data-stu-id="df4cd-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="df4cd-134">Syötä tai valitse Malli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="df4cd-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="df4cd-135">Word-mallin laajentaminen lisäämällä mukautettu XML-osa</span><span class="sxs-lookup"><span data-stu-id="df4cd-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="df4cd-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="df4cd-136">Click Save.</span></span>
    * <span data-ttu-id="df4cd-137">Määritysmuutosten tallennuksen lisäksi tallennustoiminto myös päivittää liitteenä olevan Word-mallin.</span><span class="sxs-lookup"><span data-stu-id="df4cd-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="df4cd-138">Suunnittelun muodon rakenne siirretään liitettyyn Word-asiakirjaan uutena mukautettuna, Raportti-nimisenä XML-osana.</span><span class="sxs-lookup"><span data-stu-id="df4cd-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="df4cd-139">Huomaa, että ER-raporttina luotavan asiakirjan asettelun lisäksi liitetty Word-malli sisältää myös tietorakenteen, jonka tiedot ER täyttää malliin suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="df4cd-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="df4cd-140">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="df4cd-140">Click Attachments.</span></span>
    * <span data-ttu-id="df4cd-141">Mukautetun Raportti-XML-osan elementit on nyt sidottava Word-asiakirjan osiin.</span><span class="sxs-lookup"><span data-stu-id="df4cd-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="df4cd-142">Jos olet käyttänyt Word-asiakirjoja, jotka on suunniteltu mukautettujen XML-osien elementteihin sidottuja sisällön ohjausobjekteja sisältäviksi lomakkeiksi, luo kyseinen asiakirja toistamalla kaikki seuraavan alitehtävän vaiheet.</span><span class="sxs-lookup"><span data-stu-id="df4cd-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="df4cd-143">Seuraavassa linkissä on lisätietoja: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="df4cd-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="df4cd-144">Muussa tapauksessa voit ohittaa kaikki seuraavan alitehtävän vaiheet.</span><span class="sxs-lookup"><span data-stu-id="df4cd-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="df4cd-145">Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen tietojen sidontaa varten</span><span class="sxs-lookup"><span data-stu-id="df4cd-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="df4cd-146">Avaa tämän asiakirja Wordissa ja toimi seuraavasti: – Avaa Word-kehittäjät-välilehti (muokkaa valintanauhaa, jos se ei ole vielä käytettävissä.)</span><span class="sxs-lookup"><span data-stu-id="df4cd-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="df4cd-147">- Valitse XML-määritys-ruutu.</span><span class="sxs-lookup"><span data-stu-id="df4cd-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="df4cd-148">- Valitse mukautettu Raportti-XML-osa valintaruudussa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="df4cd-149">- Yhdistä valitun mukautetun XML-osan elementtien ja Word-asiakirjan sisällön ohjausobjektien määritykset.</span><span class="sxs-lookup"><span data-stu-id="df4cd-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="df4cd-150">- Tallenna päivitetty Word-asiakirja paikalliseen asemaan.</span><span class="sxs-lookup"><span data-stu-id="df4cd-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="df4cd-151">Sisällön ohjausobjekteihin sidottuja mukautettuja XML-osia sisältävän Word-mallin lataaminen palvelimeen</span><span class="sxs-lookup"><span data-stu-id="df4cd-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="df4cd-152">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="df4cd-152">Click Delete.</span></span>
2. <span data-ttu-id="df4cd-153">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="df4cd-153">Click Yes.</span></span>
    * <span data-ttu-id="df4cd-154">Lisää uusi malli.</span><span class="sxs-lookup"><span data-stu-id="df4cd-154">Add a new template.</span></span> <span data-ttu-id="df4cd-155">Jos olet suorittanut edellisen vaiheen alitehtävät, valitse valmisteltu ja paikallisesti tallennettu Word-asiakirja.</span><span class="sxs-lookup"><span data-stu-id="df4cd-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="df4cd-156">Valitse muussa tapauksessa aiemmin ladattu MS Word -malli SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="df4cd-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="df4cd-157">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="df4cd-157">Click New.</span></span>
4. <span data-ttu-id="df4cd-158">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="df4cd-158">Click File.</span></span>
5. <span data-ttu-id="df4cd-159">Valitse Selaa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-159">Click Browse.</span></span> <span data-ttu-id="df4cd-160">Siirry aiemmin ladattuun asiakirjaan SampleVendPaymDocReportBounded.docx ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="df4cd-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="df4cd-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="df4cd-161">Click OK.</span></span>
6. <span data-ttu-id="df4cd-162">Valitse Malli-kentässä edellisessä vaiheessa lataamasi asiakirja.</span><span class="sxs-lookup"><span data-stu-id="df4cd-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="df4cd-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="df4cd-163">Click Save.</span></span>
8. <span data-ttu-id="df4cd-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="df4cd-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="df4cd-165">Word-asiakirjan luovan muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="df4cd-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="df4cd-166">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="df4cd-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="df4cd-167">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="df4cd-167">Click User parameters.</span></span>
3. <span data-ttu-id="df4cd-168">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="df4cd-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="df4cd-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="df4cd-169">Click OK.</span></span>
5. <span data-ttu-id="df4cd-170">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-170">Click Edit.</span></span>
6. <span data-ttu-id="df4cd-171">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="df4cd-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="df4cd-172">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="df4cd-172">Click Save.</span></span>
8. <span data-ttu-id="df4cd-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="df4cd-173">Close the page.</span></span>
9. <span data-ttu-id="df4cd-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="df4cd-174">Close the page.</span></span>
10. <span data-ttu-id="df4cd-175">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="df4cd-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="df4cd-176">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="df4cd-176">Click Lines.</span></span>
12. <span data-ttu-id="df4cd-177">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="df4cd-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="df4cd-178">Valitse Maksun tila.</span><span class="sxs-lookup"><span data-stu-id="df4cd-178">Click Payment status.</span></span>
14. <span data-ttu-id="df4cd-179">Valitse Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="df4cd-179">Click None.</span></span>
15. <span data-ttu-id="df4cd-180">Valitse Muodosta maksut.</span><span class="sxs-lookup"><span data-stu-id="df4cd-180">Click Generate payments.</span></span>
16. <span data-ttu-id="df4cd-181">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="df4cd-181">Click OK.</span></span>
17. <span data-ttu-id="df4cd-182">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="df4cd-182">Click OK.</span></span>
    * <span data-ttu-id="df4cd-183">Analysoi luotu raportti.</span><span class="sxs-lookup"><span data-stu-id="df4cd-183">Analyze the generated output.</span></span> <span data-ttu-id="df4cd-184">Huomaa, että luotu raportti on Word-muotoinen ja että siinä on käsiteltyjen maksujen tiedot.</span><span class="sxs-lookup"><span data-stu-id="df4cd-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

