---
title: Excel-malleja sisältävien ER-määritysten käyttäminen uudelleen Word-muotoisten raporttien luontiin
description: Tässä aiheessa käsitellään sellaisten raporttimuotojen määrittämistä luomaan raportteja Word-asiakirjoina, jotka suunniteltiin luomaan raportteja Excel-työkirjoina.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769913fd0344eb276b3b1bd055255272ca5dfffd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092713"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="f67d3-103">Excel-malleja sisältävien ER-määritysten käyttäminen uudelleen Word-muotoisten raporttien luontiin</span><span class="sxs-lookup"><span data-stu-id="f67d3-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f67d3-104">Raporttien luonti Microsoft Word -asiakirjoina edellyttää uuden [sähköisen raportoinnin (ER)](../general-electronic-reporting.md) [muodon](../general-electronic-reporting.md#FormatComponentOutbound) [määrittämistä](../er-design-configuration-word.md).</span><span class="sxs-lookup"><span data-stu-id="f67d3-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="f67d3-105">Vaihtoehtoisesti voidaan käyttää uudelleen ER-muotoa, joka suunniteltiin alun perin luomaan raportteja Excel-työkirjoina.</span><span class="sxs-lookup"><span data-stu-id="f67d3-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="f67d3-106">Siinä tapauksessa Excel-malli on korvattava Word-mallilla.</span><span class="sxs-lookup"><span data-stu-id="f67d3-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="f67d3-107">Seuraavat menettelyt osoittavat, miten käyttäjät, jolla on joko järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi määrittää ER-muodon luomaan raportteja Word-tiedostoina käyttämällä uudelleen ER-muotoa, joka suunniteltiin luomaan raportteja Excel-tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="f67d3-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="f67d3-108">Nämä menettelyt voidaan suorittaa GBSI-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="f67d3-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f67d3-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f67d3-109">Prerequisites</span></span>

<span data-ttu-id="f67d3-110">Näiden menettelyjen suorittaminen edellyttää, että tehtäväoppaassa [OPENXML-muodossa luotavien raporttien määritysten suunnittelu](er-design-reports-openxml-2016-11.md) olevat vaiheet suoritetaan ensin.</span><span class="sxs-lookup"><span data-stu-id="f67d3-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="f67d3-111">Lisäksi malliraporttia varten on ladattava ja tallennettava paikallisesti seuraavat mallit:</span><span class="sxs-lookup"><span data-stu-id="f67d3-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="f67d3-112">Maksuraportin malli (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="f67d3-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="f67d3-113">Maksuraportin sidottu malli (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="f67d3-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="f67d3-114">Nämä menettelyt koskevat toimintoa, joka lisättiin Dynamics 365 for Operationsin versiossa 1611 (marraskuu 2016).</span><span class="sxs-lookup"><span data-stu-id="f67d3-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="f67d3-115">Aiemmin luodun ER-raporttimäärityksen valitseminen</span><span class="sxs-lookup"><span data-stu-id="f67d3-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="f67d3-116">Valitse Dynamics 365 Financessa **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f67d3-117">Varmista, että konfiguraation lähde **Litware Inc.** on valittu **aktiivisena**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="f67d3-118">Jos näin ei ole, noudata tehtäväoppaan [Määrityspalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f67d3-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="f67d3-119">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="f67d3-120">Käytössä on aiemmin luodut ER-määritykset, jotka suunniteltiin alun perin luomaan OPENXML-muotoisia raportteja.</span><span class="sxs-lookup"><span data-stu-id="f67d3-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="f67d3-121">Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Maksumalli** ja valitse sitten **Laskentataulukkoraportin esimerkki**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f67d3-122">Valitun ER-muodon luonnosversiota voi muokata **Versiot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="f67d3-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="f67d3-123">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-123">Select **Designer**.</span></span>
6. <span data-ttu-id="f67d3-124">Huomaa, että **Muodon suunnittelija** -sivulla oleva juuren muotoelementin otsikko ilmaisee, että käytössä on Excel-malli.</span><span class="sxs-lookup"><span data-stu-id="f67d3-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Aiemmin luodun määrityksen valitseminen](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="f67d3-126">Ladatun Word-mallin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="f67d3-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="f67d3-127">Avaa Wordin työpöytäsovelluksessa aiemmin ladattu **SampleVendPaymDocReport.docx**-mallitiedosto.</span><span class="sxs-lookup"><span data-stu-id="f67d3-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="f67d3-128">Tarkista, että mallissa on vain sen asiakirjan asettelu, jonka haluat luoda ER-raporttina.</span><span class="sxs-lookup"><span data-stu-id="f67d3-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Word-mallin asettelu työpöytäsovelluksessa](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="f67d3-130">Excel-mallin korvaaminen Word-mallilla ja mukautetun XML-osan lisääminen</span><span class="sxs-lookup"><span data-stu-id="f67d3-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="f67d3-131">Tällä hetkellä OPENXML-muotoisen raportin luonnissa käytetään mallina Excel-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="f67d3-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="f67d3-132">Tämä malli korvataan aiemmin ladatulla Wordin SampleVendPaymDocReport.docx-mallitiedostolla.</span><span class="sxs-lookup"><span data-stu-id="f67d3-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="f67d3-133">Lisäksi Word-mallia laajennetaan lisäämällä mukautettu XML-osa.</span><span class="sxs-lookup"><span data-stu-id="f67d3-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="f67d3-134">Valitse Financessa **Muodon suunnittelija** -sivun **Muoto**-välilehdessä **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="f67d3-135">Poista aiemmin luotu Excel-malli valitsemalla **Liitteet**-sivulla **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="f67d3-136">Vahvista muutos valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="f67d3-137">Valitse **Uusi** \> **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f67d3-138">Valittavan asiakirjatyypin on oltava sellainen, että se on [määritetty](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER-parametreissa tallentamaan ER-muotojen mallit.</span><span class="sxs-lookup"><span data-stu-id="f67d3-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="f67d3-139">Valitse **Selaa**, siirry aiemmin ladattuun **SampleVendPaymDocReport.docx**-tiedostoon ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f67d3-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="f67d3-140">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-140">Select **OK**.</span></span>
6. <span data-ttu-id="f67d3-141">Sulje **Liitteet**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f67d3-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="f67d3-142">Anna tai valitse **Muodon suunnittelija** -sivun **Malli**-kentässä **SampleVendPaymDocReport.docx**-tiedosto. Näin käytetään tätä Word-mallia eikä aiemmin käytettyä Excel-mallia.</span><span class="sxs-lookup"><span data-stu-id="f67d3-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="f67d3-143">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-143">Select **Save**.</span></span>

    <span data-ttu-id="f67d3-144">Määritysmuutosten tallennuksen lisäksi **Tallenna**-toiminto päivittää liitteenä olevan Word-mallin.</span><span class="sxs-lookup"><span data-stu-id="f67d3-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="f67d3-145">Suunnittelun muodon hierarkkinen rakenne lisätään liitettyyn Word-asiakirjaan uutena mukautettuna, **Raportti**-nimisenä XML-osana.</span><span class="sxs-lookup"><span data-stu-id="f67d3-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="f67d3-146">Liitetty Word-malli sisältää sen asiakirjan asettelun, joka luodaan ER-raporttina, ja niiden tietojen rakenteen, jotka ER lisää kyseiseen malliin suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f67d3-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="f67d3-147">Huomaa, että juuren muotoelementin otsikko ilmaisee käytössä olevan Word-malli.</span><span class="sxs-lookup"><span data-stu-id="f67d3-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Excel-mallin korvaaminen Word-mallilla ja mukautetun XML-osan lisääminen](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="f67d3-149">Valitse **Muoto **-välilehdestä** Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="f67d3-150">Mukautetun **Raportti**-XML-osan elementit voidaan nyt yhdistää Word-asiakirjan sisällön ohjausobjekteihin.</span><span class="sxs-lookup"><span data-stu-id="f67d3-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="f67d3-151">Jos olet suunnitellut aiemminkin Word-asiakirjoja lomakkeina, jotka sisältävät [mukautettujen XML-osien](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) elementteihin yhdistettäviä [sisällön ohjausobjekteja](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word), luo asiakirja seuraavan menettelyn ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f67d3-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="f67d3-152">Lisätietoja on kohdassa [Käyttäjien Wordissa täyttämien tai tulostamien lomakkeiden luominen](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="f67d3-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="f67d3-153">Muussa tapauksessa voit ohittaa seuraavan menettelyn.</span><span class="sxs-lookup"><span data-stu-id="f67d3-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="f67d3-154">Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen ja tietojen yhdistämismäärityksen tekeminen</span><span class="sxs-lookup"><span data-stu-id="f67d3-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="f67d3-155">Lataa valittu malli Financesta ja tallenna se paikallisesti Word-asiakirjana valitsemalla Financen **Liitteet**-sivulla **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="f67d3-156">Avaa juuri ladattu asiakirja Wordin työpöytäsovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f67d3-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="f67d3-157">Valitse **Kehittäjä**-välilehdessä **XML-määritysruutu**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f67d3-158">Jos **Kehittäjä**-välilehti ei näy valintanauha, lisää se mukauttamalla valintanauhaa.</span><span class="sxs-lookup"><span data-stu-id="f67d3-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="f67d3-159">Valitse **XML-määritys**-ruudun **Mukautettu XML-osa** -kentässä mukautettu **Raportti**-XML-osa.</span><span class="sxs-lookup"><span data-stu-id="f67d3-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="f67d3-160">Yhdistä valitun mukautetun **Raportti**-XML-osan elementit ja Word-asiakirjan sisällön ohjausobjektit.</span><span class="sxs-lookup"><span data-stu-id="f67d3-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="f67d3-161">Tallenna päivitetty Word-asiakirja paikallisesti nimellä **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="f67d3-162">Sellaisen Word-mallin tarkasteleminen, jossa mukautettu XML-osa on yhdistetty sisällön ohjausobjekteihin</span><span class="sxs-lookup"><span data-stu-id="f67d3-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="f67d3-163">Avaa Wordin työpöytäsovelluksessa **SampleVendPaymDocReportBounded.docx**-mallitiedosto.</span><span class="sxs-lookup"><span data-stu-id="f67d3-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="f67d3-164">Tarkista, että mallissa on sen asiakirjan asettelu, jonka haluat luoda ER-raporttina.</span><span class="sxs-lookup"><span data-stu-id="f67d3-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="f67d3-165">ER:n tähän malliin suorituksen aikana lisäävien tietojen paikkamerkkeinä käytetyt sisällön ohjausobjektit perustuvat yhdistämismäärityksiin, jotka määritetään mukautetun **Raportti**-XML-osan ja Word-asiakirjan sisällön ohjausobjektien elementtien välille.</span><span class="sxs-lookup"><span data-stu-id="f67d3-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Word-mallin esikatselu työpöytäsovelluksessa](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="f67d3-167">Sellaisen Word-mallin lataaminen, jossa mukautettu XML-osa on yhdistetty sisällön ohjausobjekteihin</span><span class="sxs-lookup"><span data-stu-id="f67d3-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="f67d3-168">Poista valitsemalla Financen **Liitteet**-sivulla **Poista** Word-malli, jossa mukautetun **Raportti**-XML-osan ja sisällön ohjausobjektien elementtien välillä ei ole yhdistämismäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="f67d3-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="f67d3-169">Vahvista muutos valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="f67d3-170">Lisää valitsemalla **Uusi** \> **Tiedosto** uusi mallitiedosta, jossa on yhdistämismäärityksiä mukautetun **Raportti**-XML-osan ja sisällön ohjausobjektien elementtien välillä.</span><span class="sxs-lookup"><span data-stu-id="f67d3-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f67d3-171">Valittavan asiakirjatyypin on oltava sellainen, että se on [määritetty](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER-parametreissa tallentamaan ER-muotojen mallit.</span><span class="sxs-lookup"><span data-stu-id="f67d3-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="f67d3-172">Valitse **Selaa**, siirry aiemmin ladatun tai valmisteltuun **SampleVendPaymDocReportBounded.docx** -tiedostoon ja valitse se. Valmistelun ohjeet ovat edellä kohdassa [Mukautetun XML-osan sisältävän Word-asiakirjan hakeminen ja tietojen yhdistämismäärityksen tekeminen](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="f67d3-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="f67d3-173">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-173">Select **OK**.</span></span>
5. <span data-ttu-id="f67d3-174">Sulje **Liitteet**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f67d3-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="f67d3-175">Valitse **Muodon suunnittelija** -sivun **Malli**-kentässä juuri ladattu asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="f67d3-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="f67d3-176">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-176">Select **Save**.</span></span>
8. <span data-ttu-id="f67d3-177">Sulje **Muodon suunnittelija** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f67d3-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="f67d3-178">Määritetyn muodon merkitseminen suorittavissa olevaksi</span><span class="sxs-lookup"><span data-stu-id="f67d3-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="f67d3-179">Muokattavissa olevan muodon luonnosversion suorittaminen edellyttää, että se [suorittavissa oleva](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="f67d3-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="f67d3-180">Valitse Financen **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="f67d3-181">**Käyttäjän parametrit** -valintaikkunassa määritä **Suorita asetukset** -valinnaksi **Kyllä**, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="f67d3-182">Tee tarvittaessa nykyisestä sivusta muokattava valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="f67d3-183">Määritä valitun **Laskentataulukkoraportin esimerkki** -määrityksen **Suorita luonnos** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="f67d3-184">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="f67d3-185">Word-muotoisen tulosteen luominen suorittamalla muoto</span><span class="sxs-lookup"><span data-stu-id="f67d3-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="f67d3-186">Valitse Financessa **Ostoreskontra** \> **Maksut** \> **Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="f67d3-187">Valitse aiemmin annetussa maksukirjauskansiossa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="f67d3-188">Valitse **Toimittajan maksut** -sivulla kaikki ruudukon rivit.</span><span class="sxs-lookup"><span data-stu-id="f67d3-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="f67d3-189">Valitse **Maksun tila** \> **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-189">Select **Payment status** \> **None**.</span></span>

    ![Toimittajan maksut -sivulla käsiteltävät maksut](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="f67d3-191">Valitse toimintoruudussa **Luo maksut**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="f67d3-192">Toimi seuraavasti avautuvassa valintaikkunassa:</span><span class="sxs-lookup"><span data-stu-id="f67d3-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="f67d3-193">Valitse **Maksutapa**-kentässä **Sähköinen**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="f67d3-194">Valitse **Pankkitili**-kentässä **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="f67d3-195">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-195">Select **OK**.</span></span>

7. <span data-ttu-id="f67d3-196">Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="f67d3-197">Luotu tuloste on Word-muotoinen ja että siinä on käsiteltyjen maksujen tiedot.</span><span class="sxs-lookup"><span data-stu-id="f67d3-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="f67d3-198">Analysoi luotu raportti.</span><span class="sxs-lookup"><span data-stu-id="f67d3-198">Analyze the generated output.</span></span>

    ![Word-muotoinen luotu tuloste](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="f67d3-200">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f67d3-200">Additional resources</span></span>

- [<span data-ttu-id="f67d3-201">Uuden ER-määrityksen suunnitteleminen luomaan Word-muotoisia raportteja</span><span class="sxs-lookup"><span data-stu-id="f67d3-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="f67d3-202">Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla</span><span class="sxs-lookup"><span data-stu-id="f67d3-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
