---
title: Uusien kenttien lisääminen liiketoiminta-asiakirjamalliin Microsoft Excelissä
description: Tässä ohjeaiheessa on tietoja uusien kenttien lisäämisestä liiketoiminta-asiakirjamalliin Microsoft Exceliin liiketoiminta-asiakirjojen hallintatoiminnolla.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d6e0f2c914b8d348ef6eac42557fb46c53df04a9
ms.sourcegitcommit: d16d370dab734e09312cb06711beca9cca52d4c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809517"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="94271-103">Uusien kenttien lisääminen liiketoiminta-asiakirjamalliin Microsoft Excelissä</span><span class="sxs-lookup"><span data-stu-id="94271-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="94271-104">Voit lisätä uusia kenttiä malliin, jolla luodaan lMicrosoft Excel -muotoisia liiketoiminta-asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="94271-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="94271-105">Nämä kentät voidaan lisätä paikkamerkkeinä, joiden avulla muodostettuihin asiakirjoihin täytetään tarvittavat tiedot sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="94271-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="94271-106">Voit määrittää jokaiseen lisättävään kenttään myös sidonnan tietolähteisiin. Tällä tavoin määritetään, mitä sovelluksen tietoja lisätään kenttään, kun liiketoiminta-asiakirjoja luodaan mallin avulla.</span><span class="sxs-lookup"><span data-stu-id="94271-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="94271-107">Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin.</span><span class="sxs-lookup"><span data-stu-id="94271-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="94271-108">Tämä esimerkki näyttää, miten malli päivitetään täyttämään luotavien vapaatekstilaskujen lomakkeiden kenttiä.</span><span class="sxs-lookup"><span data-stu-id="94271-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="94271-109">Mallien muokkaaminen liiketoiminta-asiakirjojen hallinnan avulla</span><span class="sxs-lookup"><span data-stu-id="94271-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="94271-110">Koska liiketoiminta-asiakirjojen hallinta (BDM) perustuu [sähköisen raportoinnin (ER) yleiskatsauksen](general-electronic-reporting.md) kehykseen, tarvittavat ER- ja BDM-parametrit on määritettävä ennen liiketoiminta-asiakirjojen hallinnan käytön aloittamista.</span><span class="sxs-lookup"><span data-stu-id="94271-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="94271-111">Kirjaudu Microsoftin Dynamics 365 Financen esiintymään järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="94271-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="94271-112">Suorita seuraavat ohjeaiheen [Liiketoiminta-asiakirjojen hallinnan yleiskatsaus](er-business-document-management.md) esimerkin vaiheet:</span><span class="sxs-lookup"><span data-stu-id="94271-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="94271-113">Määritä ER-parametrit.</span><span class="sxs-lookup"><span data-stu-id="94271-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="94271-114">Ota liiketoiminta-asiakirjojen hallinta käyttöön.</span><span class="sxs-lookup"><span data-stu-id="94271-114">Turn on BDM.</span></span>

<span data-ttu-id="94271-115">Voit nyt aloittaa liiketoiminta-asiakirjamallien muokkaaminen käyttämällä liiketoiminta-asiakirjojen hallintaa.</span><span class="sxs-lookup"><span data-stu-id="94271-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="94271-116">Mallin sisältävien ER-ratkaisujen tuominen</span><span class="sxs-lookup"><span data-stu-id="94271-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="94271-117">Tämän menettelyn esimerkissä käytetään virallisesti julkaistua ER-ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="94271-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="94271-118">Ratkaisun ER-määritykset on tuotava Financen nykyiseen esiintymään.</span><span class="sxs-lookup"><span data-stu-id="94271-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="94271-119">Ratkaisun **Vapaatekstilasku** -ER-muotomäärityksessä on Excel-muotoinen liiketoiminta-asiakirjamalli, jota voi muokata liiketoiminta-asiakirjojen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="94271-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="94271-120">Tuo tämän ER-muotomäärityksen uusin versio Microsoft Dynamics Lifecycle Servicesta (LCS).</span><span class="sxs-lookup"><span data-stu-id="94271-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="94271-121">Vastaavat ER-tietomalli ja ER-mallin yhdistämismääritykset tuodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="94271-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="94271-122">Lisätietoja ER-määritysten tuonnista on kohdassa [ER-konfiguraation elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="94271-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Jaettu LCS-ominaisuuskirjasto -sivu](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="94271-124">ER-ratkaisumallin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="94271-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="94271-125">Kirjaudu käyttäjänä, jolla on **liiketoiminta-asiakirjojen hallinnan** työtilan käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="94271-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="94271-126">Avaa **liiketoiminta-asiakirjojen hallinnan** työtila.</span><span class="sxs-lookup"><span data-stu-id="94271-126">Open the **Business document management** workspace.</span></span>

    ![Liiketoiminta-asiakirjojen hallinnan työtila](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="94271-128">Valitse ruudukossa **Vapaatekstilasku (Excel)** -malli.</span><span class="sxs-lookup"><span data-stu-id="94271-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="94271-129">Luo valittuun malliin perustuva uusi malli valitsemalla oikeassa ruudussa **Uusi malli**.</span><span class="sxs-lookup"><span data-stu-id="94271-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="94271-130">Kirjoita **Otsikko**-kenttään uuden mallin otsikoksi **Vapaatekstilasku (Excel) Contoso**.</span><span class="sxs-lookup"><span data-stu-id="94271-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="94271-131">Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="94271-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="94271-132">BDM-mallieditorin sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="94271-132">The BDM template editor page appears.</span></span> <span data-ttu-id="94271-133">Voit muokata valittua mallia verkossa upotetun ohjausobjektin avulla käyttämällä Microsoft Office 365:tä.</span><span class="sxs-lookup"><span data-stu-id="94271-133">You can use Microsoft Office 365 to edit the selected template online in the embedded control.</span></span>

![BDM-mallieditorin sivu](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="94271-135">Uuden kentän otsikon lisääminen malliin</span><span class="sxs-lookup"><span data-stu-id="94271-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="94271-136">Valitse BDM-mallieditorisivun Excel-valintanauhan **Näytä**-välilehdessä muokattavan Excel-mallin **Otsikko- ja Ruudukko-** valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="94271-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Otsikot- ja Ruudukko-valintaruudut valittuina](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="94271-138">Valitse solut **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="94271-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="94271-139">Valitse Excel-valintanauhan **Aloitus**-välilehdessä **Yhdistä ja keskitä**. Valitut yhdistetään nyt uuteen yhdistettyyn **E8:F8**-soluun.</span><span class="sxs-lookup"><span data-stu-id="94271-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="94271-140">Kirjoita yhdistettyyn **E8:F8**-soluun **URL**.</span><span class="sxs-lookup"><span data-stu-id="94271-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="94271-141">Valitse ensin yhdistetty solu **E7:F7**, sitten **Muotoilusivellin** ja lopuksi valittu yhdistetty solu **E8:F8**. Tämän muotoilu on nyt sama yhdistetyssä solussa **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="94271-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Malliin lisätty uuden kentän otsikko](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="94271-143">Tilan varaaminen uudelle kentälle mallia muotoilemalla</span><span class="sxs-lookup"><span data-stu-id="94271-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="94271-144">Valitse BDM-mallieditorin sivulla yhdistetty solu **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="94271-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="94271-145">Valitse Excel-valintanauhan **Aloitus**-välilehdessä **Yhdistä ja keskitä**. Valitut yhdistetään nyt uuteen yhdistettyyn **G8:H8**-soluun.</span><span class="sxs-lookup"><span data-stu-id="94271-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="94271-146">Valitse ensin yhdistetty solu **G7:H7**, sitten **Muotoilusivellin** ja lopuksi valittu yhdistetty solu **G8:H8**. Tämän muotoilu on nyt sama yhdistetyssä solussa **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="94271-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Uudelle kentälle varattu tila](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="94271-148">Valitse **Nimi**-kentässä **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="94271-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="94271-149">Nykyisen Excel-mallin **CompanyInfo**-alue sisältää kaikki kentät, joilla täytetään muodostetun raportin otsikkoon nykyisen yrityksen tiedot myyvänä osapuolena.</span><span class="sxs-lookup"><span data-stu-id="94271-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![CompanyInfo-alue valittu](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="94271-151">Uuden kentän lisääminen malliin</span><span class="sxs-lookup"><span data-stu-id="94271-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="94271-152">Valitse **BDM-mallieditorin** sivun toimintoruudussa **Näytä muotoilu**.</span><span class="sxs-lookup"><span data-stu-id="94271-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="94271-153">Valitse **Mallin rakenne** -ruudussa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="94271-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="94271-154">Uutena kenttänä käytettävää mallin osaa on muokattava.</span><span class="sxs-lookup"><span data-stu-id="94271-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="94271-155">Tämä muokkaus tehtiin jo muotoilemalla yhdistetty solu **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="94271-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Uuden kentän lisääminen malliin](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="94271-157">Lisää uusi kenttä soluna malliin valitsemalla **Excel\Solu**.</span><span class="sxs-lookup"><span data-stu-id="94271-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="94271-158">Voit valita **Excel\Alue**, jos haluat lisätä uuden alueen malliin.</span><span class="sxs-lookup"><span data-stu-id="94271-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="94271-159">Annettu alue voi sisältää useita soluja.</span><span class="sxs-lookup"><span data-stu-id="94271-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="94271-160">Voit lisätä nämä solut myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="94271-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="94271-161">Huomaa, että mallin **CompanyInfo**-osa valitaan automaattisesti **Mallin rakenne** -ruudussa, koska on parhaiten sopiva pääosa nykyisessä mallirakenteessa lisättävän kentän kannalta.</span><span class="sxs-lookup"><span data-stu-id="94271-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="94271-162">Kirjoita **Excel-alue**-kenttään **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="94271-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="94271-163">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="94271-163">Select **OK**.</span></span>

    ![CompanyURL_Value-kenttä lisätään mallin rakenteeseen.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="94271-165">Valitse **Mallin rakenne** -ruudussa kolmen pisteen painike (...) ja valitse sitten **Näytä sidonnat**.</span><span class="sxs-lookup"><span data-stu-id="94271-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Näytä sidonnat valittu](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="94271-167">**Mallin rakenne** -ruudussa näkyy nyt pohjana olevassa ER-muodossa käytettävissä olevat tietolähteet.</span><span class="sxs-lookup"><span data-stu-id="94271-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="94271-168">Valitse **CompanyInfo_Value** kentäksi, johon pohjana olevan ER-muodon tietolähde on tarkoitus sitoa.</span><span class="sxs-lookup"><span data-stu-id="94271-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="94271-169">Laajenna **Mallin rakenne** -ruudun **Tietolähteet**-osassa **Malli \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="94271-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="94271-170">Valitse **CompanyInfo**-kohdassa **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="94271-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![WebsiteURI valittuna](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="94271-172">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="94271-172">Select **Bind**.</span></span>
11. <span data-ttu-id="94271-173">Valitse **Mallin rakenne** -ruudussa **Tallenna** ja sulje sitten BDM-mallieditorin sivu.</span><span class="sxs-lookup"><span data-stu-id="94271-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="94271-174">Päivitetty malli näkyy **Liiketoiminta-asiakirjojen hallinnan** työtilan oikeanpuolisen ruudun **Malli**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="94271-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="94271-175">Huomaa, että ruudukossa muokatun mallin **Tila**-kentän arvo on nyt **Luonnos** eikä **Tarkistusversio**-kenttä ole enää tyhjä.</span><span class="sxs-lookup"><span data-stu-id="94271-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="94271-176">Nämä muutoksen ilmaisevat, että mallin muokkausprosessi on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="94271-176">These changes indicate that the process of editing this template has been started.</span></span>

![Muokattu malli liiketoiminta-asiakirjojen hallinnan työtilassa](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="94271-178">Yrityksen asetusten tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="94271-178">Review company settings</span></span>

1.  <span data-ttu-id="94271-179">Valitse **Organisaation hallinto \> Organisaatiot \> Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="94271-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="94271-180">Tarkista, että yrityksen URL-osoite on annettu **Yhteystiedot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="94271-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Yritykset-sivulla annettu yrityksen URL-osoite](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="94271-182">Päivitetyn mallin testaaminen luomalla liiketoiminta-asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="94271-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="94271-183">Vaihda sovelluksessa yritykseksi **USMF** ja valitse sitten **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**.</span><span class="sxs-lookup"><span data-stu-id="94271-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="94271-184">Valitse ensin lasku **FTI-00000002** ja sitten **Tulostuksenhallinta**.</span><span class="sxs-lookup"><span data-stu-id="94271-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="94271-185">Laajenna vasemmassa ruudussa **Moduuli - Myyntireskontra \> Asiakirjat \> Vapaatekstilasku**.</span><span class="sxs-lookup"><span data-stu-id="94271-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="94271-186">Määritä käsiteltävien laskujen vaikutusalue valitsemalla **Vapaatekstilasku**-kohdassa **Alkuperäinen tiedosto** -taso.</span><span class="sxs-lookup"><span data-stu-id="94271-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="94271-187">Valitse oikeassa ruudussa ensin **Raportin muoto** -kenttä ja sitten määritetyn asiakirjatason **Vapaatekstilasku (Excel) Contoso** -malli.</span><span class="sxs-lookup"><span data-stu-id="94271-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Vapaatekstilasku (Excel) Contoso -malli valittuna](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="94271-189">Sulje nykyinen sivu painamalla **Esc**-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="94271-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="94271-190">Valitse **Tulosta \> Valitut**.</span><span class="sxs-lookup"><span data-stu-id="94271-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="94271-191">Lataa muodostettu asiakirja ja avaa se Excelissä.</span><span class="sxs-lookup"><span data-stu-id="94271-191">Download the generated document, and open it in Excel.</span></span>

    ![Excelin vapaatekstilasku](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="94271-193">Muokatun mallin avulla luodaan valitulle nimikkeelle vapaatekstilaskun raportti.</span><span class="sxs-lookup"><span data-stu-id="94271-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="94271-194">Jos haluat analysoida, miten malliin tekemäsi muutokset vaikuttavat tähän raporttiin, suorita raportti yhdessä sovellusistunnossa heti sen jälkeen, kun olet muuttanut mallia toisessa sovellusistunnossa.</span><span class="sxs-lookup"><span data-stu-id="94271-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="94271-195">Liittyvät linkit</span><span class="sxs-lookup"><span data-stu-id="94271-195">Related links</span></span>

[<span data-ttu-id="94271-196">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="94271-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="94271-197">Liiketoiminta-asiakirjojen hallinta – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="94271-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="94271-198">Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa</span><span class="sxs-lookup"><span data-stu-id="94271-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)