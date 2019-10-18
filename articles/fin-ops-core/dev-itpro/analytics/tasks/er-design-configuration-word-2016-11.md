---
title: Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa
description: Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää sähköisen raportoinnin muotoja luomaan raportteja Microsoft Word -tiedostoina.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182597"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="75022-103">Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa</span><span class="sxs-lookup"><span data-stu-id="75022-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75022-104">Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää sähköisen raportoinnin (ER) muotoja luomaan raportteja Microsoft Word -tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="75022-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="75022-105">Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="75022-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="75022-106">Näiden vaiheiden suorittaminen edellyttää, että ER-määrityksen luonti OPENXML-muotoisten raporttien luomiseksi -tehtäväoppaan vaiheet on suoritettu ensin.</span><span class="sxs-lookup"><span data-stu-id="75022-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="75022-107">Lisäksi malliraporttia varten on etukäteen ladattava ja tallennettava paikallisesti seuraavat mallit:</span><span class="sxs-lookup"><span data-stu-id="75022-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="75022-108">Maksuraportin malli</span><span class="sxs-lookup"><span data-stu-id="75022-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="75022-109">Maksuraportin sidottu malli</span><span class="sxs-lookup"><span data-stu-id="75022-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="75022-110">Nämä ohjeet koskevat toimintoa, joka lisättiin Microsoft Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="75022-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="75022-111">Aiemmin luodun ER-raporttimäärityksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="75022-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="75022-112">Siirry kohtaan **siirtymisruutu > Moduulit > organisaation hallinto > Työtilat > Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="75022-112">In the **Navigation pane, go to Modules > Organization administration > Workspaces > Electronic reporting**.</span></span> <span data-ttu-id="75022-113">Varmista, että konfiguraation lähde, Litware Inc.,</span><span class="sxs-lookup"><span data-stu-id="75022-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="75022-114">on valittu aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="75022-114">is selected as active.</span></span>  
2. <span data-ttu-id="75022-115">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="75022-115">Click **Reporting configurations**.</span></span> <span data-ttu-id="75022-116">Käytämme aiemmin luotuja ER-määrityksiä, jotka on alun perin suunniteltu luomaan raportti OPENXML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="75022-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="75022-117">Laajenna puussa solmu Payment model.</span><span class="sxs-lookup"><span data-stu-id="75022-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="75022-118">Valitse puusta Maksumalli\Laskentataulukkoraportin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="75022-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="75022-119">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="75022-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="75022-120">Excel-malliin korvaaminen Word-mallilla</span><span class="sxs-lookup"><span data-stu-id="75022-120">Replace the Excel template with the Word template</span></span>

<span data-ttu-id="75022-121">Tällä hetkellä OPENXML-muotoisen raportin luonnissa käytetään mallina Excel-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="75022-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="75022-122">Raporttimalli tuodaan Word-muodossa.</span><span class="sxs-lookup"><span data-stu-id="75022-122">We will import the report’s template in Word format.</span></span>

1. <span data-ttu-id="75022-123">Napsauta **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="75022-123">Click **Attachments**.</span></span> <span data-ttu-id="75022-124">Korvaa aiemmin luotu Excel-malli aiemmin ladatulla Word-mallilla SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="75022-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="75022-125">Huomaa, että tässä mallissa on vain ER-raporttina luotavan asiakirjan asettelu.</span><span class="sxs-lookup"><span data-stu-id="75022-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="75022-126">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="75022-126">Click **Delete**.</span></span>
3. <span data-ttu-id="75022-127">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="75022-127">Click **Yes**.</span></span>
4. <span data-ttu-id="75022-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="75022-128">Click **New**.</span></span>
5. <span data-ttu-id="75022-129">Napsauta **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="75022-129">Click **File**.</span></span>
6. <span data-ttu-id="75022-130">Valitse **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="75022-130">Click **Browse**.</span></span> <span data-ttu-id="75022-131">Siirry aiemmin ladattuun asiakirjaan SampleVendPaymDocReport.docx ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="75022-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="75022-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75022-132">Click **OK**.</span></span> <span data-ttu-id="75022-133">Valitse edellisessä vaiheessa lataamasi malli.</span><span class="sxs-lookup"><span data-stu-id="75022-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="75022-134">Syötä tai valitse **Malli**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="75022-134">In the **Template** field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="75022-135">Word-mallin laajentaminen lisäämällä mukautettu XML-osa</span><span class="sxs-lookup"><span data-stu-id="75022-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="75022-136">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75022-136">Click **Save**.</span></span> <span data-ttu-id="75022-137">Määritysmuutosten tallennuksen lisäksi tallennustoiminto myös päivittää liitteenä olevan Word-mallin.</span><span class="sxs-lookup"><span data-stu-id="75022-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="75022-138">Suunnittelun muodon rakenne siirretään liitettyyn Word-asiakirjaan uutena mukautettuna, Raportti-nimisenä XML-osana.</span><span class="sxs-lookup"><span data-stu-id="75022-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="75022-139">Huomaa, että ER-raporttina luotavan asiakirjan asettelun lisäksi liitetty Word-malli sisältää myös tietorakenteen, jonka tiedot ER täyttää malliin suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="75022-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="75022-140">Napsauta **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="75022-140">Click **Attachments**.</span></span>
    + <span data-ttu-id="75022-141">Mukautetun Raportti-XML-osan elementit on nyt sidottava Word-asiakirjan osiin.</span><span class="sxs-lookup"><span data-stu-id="75022-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    + <span data-ttu-id="75022-142">Jos olet käyttänyt Word-asiakirjoja, jotka on suunniteltu mukautettujen XML-osien elementteihin sidottuja sisällön ohjausobjekteja sisältäviksi lomakkeiksi, luo kyseinen asiakirja toistamalla kaikki seuraavan alitehtävän vaiheet.</span><span class="sxs-lookup"><span data-stu-id="75022-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="75022-143">Lisätietoja on kohdassa [Luo lomakkeita, jotka käyttäjät täyttävät tai tulostavat Wordissa](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="75022-143">For more details, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span></span> <span data-ttu-id="75022-144">Muussa tapauksessa voit ohittaa kaikki seuraavan alitehtävän vaiheet.</span><span class="sxs-lookup"><span data-stu-id="75022-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="75022-145">Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen tietojen sidontaa varten</span><span class="sxs-lookup"><span data-stu-id="75022-145">Get Word with custom XML part to do data bindings</span></span>

<span data-ttu-id="75022-146">Avaa tämän asiakirja Wordissa ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="75022-146">Open this document in Word and do the following:</span></span>  
1. <span data-ttu-id="75022-147">Avaa Word-kehittäjät-välilehti (muokkaa valintanauhaa, jos se ei ole vielä käytettävissä.)</span><span class="sxs-lookup"><span data-stu-id="75022-147">Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>
2. <span data-ttu-id="75022-148">Valitse XML-määritys -ruutu.</span><span class="sxs-lookup"><span data-stu-id="75022-148">Select XML mapping pane.</span></span>
3. <span data-ttu-id="75022-149">Valitse mukautettu Raportti-XML-osa valintaruudussa.</span><span class="sxs-lookup"><span data-stu-id="75022-149">Select the ‘Report’ custom XML part in the lookup.</span></span>
4. <span data-ttu-id="75022-150">Yhdistä valitun mukautetun XML-osan elementtien ja Word-asiakirjan sisällön ohjausobjektien määritykset.</span><span class="sxs-lookup"><span data-stu-id="75022-150">Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="75022-151">5.</span><span class="sxs-lookup"><span data-stu-id="75022-151">5.</span></span> <span data-ttu-id="75022-152">Tallenna päivitetty Word-asiakirja paikalliseen asemaan.</span><span class="sxs-lookup"><span data-stu-id="75022-152">Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="75022-153">Sisällön ohjausobjekteihin sidottuja mukautettuja XML-osia sisältävän Word-mallin lataaminen palvelimeen</span><span class="sxs-lookup"><span data-stu-id="75022-153">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="75022-154">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="75022-154">Click **Delete**.</span></span>
2. <span data-ttu-id="75022-155">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="75022-155">Click **Yes**.</span></span> <span data-ttu-id="75022-156">Lisää uusi malli.</span><span class="sxs-lookup"><span data-stu-id="75022-156">Add a new template.</span></span> <span data-ttu-id="75022-157">Jos olet suorittanut edellisen vaiheen alitehtävät, valitse valmisteltu ja paikallisesti tallennettu Word-asiakirja.</span><span class="sxs-lookup"><span data-stu-id="75022-157">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="75022-158">Valitse muussa tapauksessa aiemmin ladattu MS Word -malli SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="75022-158">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="75022-159">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="75022-159">Click **New**.</span></span>
4. <span data-ttu-id="75022-160">Napsauta **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="75022-160">Click **File**.</span></span>
5. <span data-ttu-id="75022-161">Valitse **Selaa**.</span><span class="sxs-lookup"><span data-stu-id="75022-161">Click **Browse**.</span></span> <span data-ttu-id="75022-162">Siirry aiemmin ladattuun asiakirjaan SampleVendPaymDocReportBounded.docx ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="75022-162">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="75022-163">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75022-163">Click **OK**.</span></span>
6. <span data-ttu-id="75022-164">Valitse **Malli**-kentässä edellisessä vaiheessa lataamasi asiakirja.</span><span class="sxs-lookup"><span data-stu-id="75022-164">In the **Template** field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="75022-165">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75022-165">Click **Save**.</span></span>
8. <span data-ttu-id="75022-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75022-166">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="75022-167">Word-asiakirjan luovan muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="75022-167">Execute the format to create Word output</span></span>
1. <span data-ttu-id="75022-168">Valitse **toimintoruudussa** **Konfiguroinnit**.</span><span class="sxs-lookup"><span data-stu-id="75022-168">On the **Action Pane**, click **Configurations**.</span></span>
2. <span data-ttu-id="75022-169">Valitse **Käyttäjän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="75022-169">Click **User parameters**.</span></span>
3. <span data-ttu-id="75022-170">Valitse **Suorita asetukset** -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="75022-170">Select Yes in the **Run settings** field.</span></span>
4. <span data-ttu-id="75022-171">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75022-171">Click **OK**.</span></span>
5. <span data-ttu-id="75022-172">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="75022-172">Click **Edit**.</span></span>
6. <span data-ttu-id="75022-173">Valitse **Suorita luonnos** -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="75022-173">Select Yes in the **Run Draft** field.</span></span>
7. <span data-ttu-id="75022-174">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="75022-174">Click **Save**.</span></span>
8. <span data-ttu-id="75022-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75022-175">Close the page.</span></span>
9. <span data-ttu-id="75022-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75022-176">Close the page.</span></span>
10. <span data-ttu-id="75022-177">Siirry **siirtymisruudussa** kohtaan **Moduulit > Ostoreskontra > Maksut > Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="75022-177">In the **Navigation pane**, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
11. <span data-ttu-id="75022-178">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="75022-178">Click **Lines**.</span></span>
12. <span data-ttu-id="75022-179">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="75022-179">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="75022-180">Valitse **Maksun tila**.</span><span class="sxs-lookup"><span data-stu-id="75022-180">Click **Payment status**.</span></span>
14. <span data-ttu-id="75022-181">Valitse **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="75022-181">Click **None**.</span></span>
15. <span data-ttu-id="75022-182">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="75022-182">Click **Generate payments**.</span></span>
16. <span data-ttu-id="75022-183">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75022-183">Click **OK**.</span></span>
17. <span data-ttu-id="75022-184">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75022-184">Click **OK**.</span></span> <span data-ttu-id="75022-185">Analysoi luotu raportti.</span><span class="sxs-lookup"><span data-stu-id="75022-185">Analyze the generated output.</span></span> <span data-ttu-id="75022-186">Huomaa, että luotu raportti on Word-muotoinen ja että siinä on käsiteltyjen maksujen tiedot.</span><span class="sxs-lookup"><span data-stu-id="75022-186">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

