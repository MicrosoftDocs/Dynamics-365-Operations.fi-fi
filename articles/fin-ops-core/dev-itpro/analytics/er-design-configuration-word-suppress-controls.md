---
title: Piilota Word-sisällön ohjausobjektit luoduissa raporteissa
description: Tässä aiheessa kerrotaan, miten määritetään sähköisen raportoinnin (ER) muoto, jotta raportit voidaan luoda Microsoft Word -tiedostoina, joissa sisällön ohjausobjektit on piilotettu.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562115"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="e6644-103">Piilota Word-sisällön ohjausobjektit luoduissa raporteissa</span><span class="sxs-lookup"><span data-stu-id="e6644-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6644-104">Jos haluat luoda raportteja Microsoft Word -asiakirjoina, suunnittele raporttien malli Word-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="e6644-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="e6644-105">Tämän mallin on sisällettävä Word-sisällön ohjausobjektit suorituksen aikana täytettävinä tietojen paikkamerkkeinä.</span><span class="sxs-lookup"><span data-stu-id="e6644-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="e6644-106">Luotua Word-asiakirjaa voi käyttää mallina [määrittämällä](er-design-configuration-word.md) uuden [sähköisen raportoinnin (ER)](general-electronic-reporting.md) [ratkaisun](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="e6644-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="e6644-107">Ratkaisussa on oltava ER-[määritys](general-electronic-reporting.md#Configuration), joka sisältää ER-[muodon](general-electronic-reporting.md#FormatComponentOutbound) osan.</span><span class="sxs-lookup"><span data-stu-id="e6644-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="e6644-108">Tämä ER-muoto on määritettävä käyttämään suunniteltua mallia raportin luontiin.</span><span class="sxs-lookup"><span data-stu-id="e6644-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="e6644-109">Dynamics 365 Financen versiossa 10.0.6 ja sitä myöhemmissä versioissa ER-muotoisia kaavoja voi konfiguroida piilottamaan luotujen tiedostojen Word-sisällön ohjausobjektit.</span><span class="sxs-lookup"><span data-stu-id="e6644-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="e6644-110">Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin rooliin määritetty käyttäjä voi konfiguroida ER-muodon, joka luo raportit Word-tiedostoina ja piilottaa joitakin Word-mallin avulla konfiguroitujen luotujen raporttien sisällön ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="e6644-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="e6644-111">Nämä vaiheet voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e6644-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e6644-112">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="e6644-112">Prerequisites</span></span>

<span data-ttu-id="e6644-113">Näiden vaiheiden edellytyksenä on seuraavien tehtäväoppaiden vaiheiden suorittaminen:</span><span class="sxs-lookup"><span data-stu-id="e6644-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="e6644-114">Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa</span><span class="sxs-lookup"><span data-stu-id="e6644-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="e6644-115">Raporttien luominen Word-muodossa käyttämällä ER-konfiguraatioita uudelleen Excel-mallien avulla</span><span class="sxs-lookup"><span data-stu-id="e6644-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="e6644-116">Kun suoritat näiden tehtäväoppaiden vaiheet, seuraavat kohteet valmistellaan:</span><span class="sxs-lookup"><span data-stu-id="e6644-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="e6644-117">**Laskentataulukon malliraportti** -ER-muoto, joka on määritetty luomaan asiakirja Word-muodossa</span><span class="sxs-lookup"><span data-stu-id="e6644-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="e6644-118">**Mallilaskentataulukon** ER-muodon [luonnosversio](general-electronic-reporting.md#component-versioning), joka on merkitty **Runnable**</span><span class="sxs-lookup"><span data-stu-id="e6644-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="e6644-119">**Sähköiset** maksutavat, jotka on määritetty käyttämään toimittajan maksujen käsittelyssä **laskentataulukon esimerkkiraportin** ER-muotoa</span><span class="sxs-lookup"><span data-stu-id="e6644-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="e6644-120">Lisäksi malliraporttia varten on ladattava ja tallennettava seuraava malli:</span><span class="sxs-lookup"><span data-stu-id="e6644-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="e6644-121">Maksuraportin sidottu malli 2 (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="e6644-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="e6644-122">Ladatun Word-mallin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="e6644-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="e6644-123">Avaa Wordin työpöytäsovelluksessa aiemmin ladattu **SampleVendPaymDocReportBounded2.docx**-mallitiedosto.</span><span class="sxs-lookup"><span data-stu-id="e6644-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="e6644-124">Varmista, että mallitiedosto sisältää yhteenveto-osan, jossa näkyvät käsiteltyjen maksujen maksujen kokonaissummat jokaisen käsiteltyjen maksujen valuuttakoodin osalta.</span><span class="sxs-lookup"><span data-stu-id="e6644-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="e6644-125">Yhteenveto-osa sijaitsee erillisessä Word-asiakirjan taulussa.</span><span class="sxs-lookup"><span data-stu-id="e6644-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="e6644-126">Tämän taulun ensimmäisellä rivillä on taulukon sarakkeiden otsikot osan otsikkona.</span><span class="sxs-lookup"><span data-stu-id="e6644-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="e6644-127">Tämän taulun toisella rivillä on toistuvan sisällön ohjausobjekti osan tietoina.</span><span class="sxs-lookup"><span data-stu-id="e6644-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="e6644-128">Tämä sisällön ohjausobjekti on yhdistetty mukautetun **Report**-XML-osan **SummaryLines**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e6644-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="e6644-129">Tämän määrityksen perusteella sisällön ohjausobjekti liittyy muokattavan ER-muodon **SummaryLines**-elementtiin.</span><span class="sxs-lookup"><span data-stu-id="e6644-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6644-130">Toistuvan sisällön ohjausobjekti on koodattu **SummaryLines**-avaimella, joka vastaa sen mukautetun XML-osan kenttää, johon se on yhdistetty.</span><span class="sxs-lookup"><span data-stu-id="e6644-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word-mallin asettelu](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="e6644-132">Aiemmin luodun ER-raporttimäärityksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="e6644-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="e6644-133">Seuraavissa vaiheissa käytät uudelleen aiemmin – kun suoritit aiemmin mainittujen tehtäväoppaiden vaiheet – määritettyä ER-konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="e6644-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="e6644-134">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="e6644-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e6644-135">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e6644-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e6644-136">Laajenna **Konfiguraatiot**-sivun määrityspuussa **Maksumalli** ja valitse sitten **Laskentataulukkoraportin esimerkki**.</span><span class="sxs-lookup"><span data-stu-id="e6644-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="e6644-137">Valitse **Suunnitteluohjelma**, jos haluat muokata valitun ER-muodon luonnosversiota.</span><span class="sxs-lookup"><span data-stu-id="e6644-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="e6644-138">Nykyisen malliin korvaaminen uudella mallilla</span><span class="sxs-lookup"><span data-stu-id="e6644-138">Replace the current template with the new template</span></span>

<span data-ttu-id="e6644-139">Tällä hetkellä Word-muotoisen raportin luonnissa käytetään mallina SampleVendPaymDocReportBounded.docx-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="e6644-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="e6644-140">Seuraavissa vaiheissa tämä Word-malli korvataan aiemmin ladatulla uudella Word-mallilla SampleVendPaymDocReportBounded2.docx.</span><span class="sxs-lookup"><span data-stu-id="e6644-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="e6644-141">Vallitse **Muodon suunnittelu** -sivulla **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="e6644-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="e6644-142">Poista aiemmin luotu malli valitsemalla **Liitteet**-sivulla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="e6644-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="e6644-143">Vahvista poisto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e6644-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="e6644-144">Valitse **Uusi** \> **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="e6644-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="e6644-145">Valitse **Selaa**, siirry aiemmin ladattuun **SampleVendPaymDocReportBounded2.docx**-tiedostoon ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e6644-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="e6644-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6644-146">Select **OK**.</span></span>
7. <span data-ttu-id="e6644-147">Sulje **Liitteet**-sivu.</span><span class="sxs-lookup"><span data-stu-id="e6644-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="e6644-148">Kirjoita tai valitse **Muodon suunnittelu** -sivun **Malli**-kentässä **SampleVendPaymDocReportBounded2.docx**-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e6644-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="e6644-149">Word-asiakirjan luovan muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="e6644-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="e6644-150">Valitse **Ostoreskontra** \> **Maksut** \> **Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="e6644-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="e6644-151">Valitse kaikki maksut **Toimittajamaksut**-sivun **Luettelo**-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="e6644-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="e6644-152">Valitse **Maksun tila** \> **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="e6644-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="e6644-153">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="e6644-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="e6644-154">Valitse **Maksutapa**-kentässä **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="e6644-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="e6644-155">Valitse **Pankkitili**-kentässä **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="e6644-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="e6644-156">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6644-156">Select **OK**.</span></span>
8. <span data-ttu-id="e6644-157">Valitse **Sähköisen raportin parametrit** -valintaikkunassa **OK** ja analysoi luotu tuloste.</span><span class="sxs-lookup"><span data-stu-id="e6644-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Toimittajan maksut -sivulla käsiteltävät maksut](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="e6644-159">Tuloste esitetään Word-muodossa, ja se sisältää yhteenveto-osan.</span><span class="sxs-lookup"><span data-stu-id="e6644-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="e6644-160">Konfiguroi muokattavissa oleva muoto piilottamaabn yhteenveto-osa</span><span class="sxs-lookup"><span data-stu-id="e6644-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="e6644-161">Jos haluat piilottaa yhteenveto-osan luodussa tiedostossa tämän ER-muodon suorittaneen käyttäjän pyynnön perusteella, muokkaa muokattavaa ER-muotoa.</span><span class="sxs-lookup"><span data-stu-id="e6644-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="e6644-162">Siirry kohtaan **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi** ja avaa ER-muodon luonnosversio muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="e6644-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="e6644-163">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="e6644-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="e6644-164">Laajenna **Konfiguraatiot**-sivun määrityspuussa **Maksumalli** \> **Laskentataulukkoraportin esimerkki**.</span><span class="sxs-lookup"><span data-stu-id="e6644-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="e6644-165">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="e6644-165">Select **Designer**.</span></span>
5. <span data-ttu-id="e6644-166">Laajenna **Muodon suunnittelu** -sivulla **Word** ja valitse **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="e6644-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="e6644-167">Lisää **Määritys**-välilehdessä uusi tietolähde, joka kysyy käyttäjältä ajon aikana, tuleeko yhteenveto-osa piilottaa:</span><span class="sxs-lookup"><span data-stu-id="e6644-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="e6644-168">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="e6644-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="e6644-169">Valitse **Lisää tietolähde** -valintaikkunassa **Yleinen\Käyttäjän syöteparametri** avataksesi **Käyttäjän syöttöparametri -tietolähteen ominaisuudet** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="e6644-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="e6644-170">Kirjoita **Nimi**-kenttään **uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="e6644-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="e6644-171">Kirjoita **Otsikko**-kenttään **Piilota yhteenveto-osa**.</span><span class="sxs-lookup"><span data-stu-id="e6644-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="e6644-172">Valitse tai kirjoita **Toiminnon tietotyypin nimi** -kentässä **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="e6644-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="e6644-173">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6644-173">Select **OK**.</span></span>

7. <span data-ttu-id="e6644-174">Lisää uusi **NoYes**-sovelluksen valintalistatyyppinen tietolähde:</span><span class="sxs-lookup"><span data-stu-id="e6644-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="e6644-175">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="e6644-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="e6644-176">Valitse **Lisää tietolähde** -valintaikkunassa **Dynamics 365 for Operations\Valintalista**, niin näyttöön tulee **Valintalista-tietolähteen ominaisuudet** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="e6644-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="e6644-177">Kirjoita **Nimi**-kenttään **enumNoYes**.</span><span class="sxs-lookup"><span data-stu-id="e6644-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="e6644-178">Kirjoita **Otsikko**-kenttään **Piilota asetukset**.</span><span class="sxs-lookup"><span data-stu-id="e6644-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="e6644-179">Valitse tai kirjoita **Toiminnon tietotyypin nimi** -kentässä **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="e6644-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="e6644-180">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6644-180">Select **OK**.</span></span>

8. <span data-ttu-id="e6644-181">Määritä valitulle **SummaryLines**-muotoelementille kaava, joka määrittää, milloin valittuun muotoelementtiin liittyvän Word-sisällön ohjausobjekti tulee piilottaa:</span><span class="sxs-lookup"><span data-stu-id="e6644-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="e6644-182">Valitse **Määritys**-välilehden **Poistettu**-osassa **Muokkaa** avataksesi **[Muodon suunnittelu](general-electronic-reporting-formula-designer.md)** -sivun.</span><span class="sxs-lookup"><span data-stu-id="e6644-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="e6644-183">Kirjoita **Kaava**-kenttään kaava `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="e6644-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="e6644-184">Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e6644-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e6644-185">Tätä kaavaa käytetään luodussa tiedostossa kaikkien **muiden muotoelementtien suorittamisen jälkeen**.</span><span class="sxs-lookup"><span data-stu-id="e6644-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="e6644-186">Voit käyttää tätä kaavaa, kun Word-sisällön ohjausobjekti, joka on merkitty muotoelementinä, jota varten kaava on määritetty (tässä tapauksessa **SummaryLines**), löytyy luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="e6644-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="e6644-187">Tämä sisältöohjausobjekti poistetaan sitten kokonaan yhdessä sen Word-taulukon rivin kanssa, joka sisältää sen.</span><span class="sxs-lookup"><span data-stu-id="e6644-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="e6644-188">Yhteenveto-osan erittelyrivi poistetaan luodusta asiakirjasta.</span><span class="sxs-lookup"><span data-stu-id="e6644-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="e6644-189">Suunnittelun aikana voit konfiguroida **Poistettu**-kaavan muotoelementille, vaikka käytössä olevassa Word-mallin yhdessäkään sisällön ohjausobjektissa ei ole tunnistetta, joka vastaa sellaisen muotoelementin nimeä, jolle **Poistettu**-ominaisuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="e6644-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="e6644-190">Kun tarkistat muodon suunnittelun aikana, saat [varoituksen](er-components-inspections.md#i14) tästä ristiriidasta.</span><span class="sxs-lookup"><span data-stu-id="e6644-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="e6644-191">Suoritusaika tuotetaan poikkeus, jos käytössä olevan Word-mallin missään sisältöohjausobjektissa ei ole tunnistetta, joka vastaisi sellaisen muotoelementin nimeä, jolle **Poistettu**-ominaisuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="e6644-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="e6644-192">Määritä **Määritys**-välilehden **Poistettu**-osassa **Ylätason kanssa** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e6644-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e6644-193">Tämä asetus on määritettävä **Kyllä**-arvoksi, jos haluat poistaa koko Word-taulun sen rivin ylätason objektina, joka sisältää yhteenveto-osan tiedot.</span><span class="sxs-lookup"><span data-stu-id="e6644-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="e6644-194">Jos määrität tämän asetuksen arvoksi **Ei**, osan otsikkorivi jää luotuun tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="e6644-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="e6644-195">Tallenna muokattavan muodon muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e6644-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Word-muotoinen luotu tuloste](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="e6644-197">Word-asiakirjan luovan muokatun muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="e6644-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="e6644-198">Valitse **Ostoreskontra** \> **Maksut** \> **Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="e6644-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="e6644-199">Valitse luomasi maksukirjauskansio ja valitse sitten **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="e6644-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="e6644-200">Valitse **Toimittajamaksut**-sivulla kaikki rivit ja valitse sitten **Maksun tila** \> **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="e6644-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="e6644-201">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="e6644-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="e6644-202">Valitse **Maksutapa**-kentässä **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="e6644-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="e6644-203">Valitse **Pankkitili**-kentässä **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="e6644-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="e6644-204">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6644-204">Select **OK**.</span></span>
8. <span data-ttu-id="e6644-205">Valitse **Sähköisen raportoinnin parametrit** -valintaikkunan **Piilota yhteeneveto-osa** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e6644-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="e6644-206">Valitse **OK** ja analysoi luotu tuloste.</span><span class="sxs-lookup"><span data-stu-id="e6644-206">Select **OK**, and analyze the generated output.</span></span>

    ![Word-muotoinen luotu tuloste](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="e6644-208">Huomaa, että tuloste ei sisällä yhteenveto-osaa, koska se on piilotettu.</span><span class="sxs-lookup"><span data-stu-id="e6644-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6644-209">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e6644-209">Additional resources</span></span>

- [<span data-ttu-id="e6644-210">Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa</span><span class="sxs-lookup"><span data-stu-id="e6644-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="e6644-211">Uuden ER-konfiguraation suunnitteleminen raporttien luomiseksi Word-muodossa</span><span class="sxs-lookup"><span data-stu-id="e6644-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="e6644-212">Raporttien luominen Word-muodossa käyttämällä ER-konfiguraatioita uudelleen Excel-mallien avulla</span><span class="sxs-lookup"><span data-stu-id="e6644-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="e6644-213">Tarkista määritetty ER-komponentti estääksesi suorituksen aikaiset ongelmat</span><span class="sxs-lookup"><span data-stu-id="e6644-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]