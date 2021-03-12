---
title: Liiketoiminta-asiakirjan mallin rakenteen päivittäminen
description: Tässä aiheessa kerrotaan, kuinka liiketoiminta-asiakirjan malli voidaan päivittää käyttämällä Liiketoiminta-asiakirjan hallintaominaisuutta.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cb0188e372b5f6275472cf040d10bb796eed1858
ms.sourcegitcommit: 95d2fc0fa7d17d3a96f7969f12c985b018b4ff94
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/12/2020
ms.locfileid: "4728086"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="976b7-103">Liiketoiminta-asiakirjan mallin rakenteen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="976b7-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="976b7-104">Voit muokata liiketoiminta-asiakirjan mallia **Mallin rakenne** -ruudussa [Liiketoiminta-asiakirjan hallinta](er-business-document-management.md)  -mallin editorissa [lisäämällä uusia kenttiä](er-bdm-add-field-to-excel-template.md) malliin Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="976b7-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="976b7-105">Mallin rakenne päivitetään automaattisesti Dynamics 365 Finance -järjestelmässä, jotta se vastaa **Mallin rakenne** -ruudussa tehtyjä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="976b7-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="976b7-106">Voit myös muokata mallia käyttämällä Office 365:n online-toimintoja.</span><span class="sxs-lookup"><span data-stu-id="976b7-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="976b7-107">Voit esimerkiksi lisätä uuden nimetyn nimikkeen, kuten kuvan tai muodon, muokattavaan laskentataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="976b7-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="976b7-108">Tässä tapauksessa mallin rakennetta ei päivitetä automaattisesti Financeen, eikä lisäämäsi nimike näy **Mallin rakenne** -ruudussa.</span><span class="sxs-lookup"><span data-stu-id="976b7-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="976b7-109">Voit päivittää mallin rakenteen Financessa manuaalisesti valitsemalla **Päivitä rakenne** mallieditorisivulla.</span><span class="sxs-lookup"><span data-stu-id="976b7-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="976b7-110">Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.</span><span class="sxs-lookup"><span data-stu-id="976b7-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="976b7-111">Esimerkki: liiketoiminta-asiakirjan mallin rakenteen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="976b7-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="976b7-112">Tässä esimerkissä näytetään, miten järjestelmänvalvoja voi päivittää yrityksen liiketoiminta-asiakirjan mallin rakenteen sen jälkeen, kun mallia on muokattu Office Onlinessa.</span><span class="sxs-lookup"><span data-stu-id="976b7-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="976b7-113">Seuraavissa osissa selitetään tarvittavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="976b7-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="976b7-114">Liiketoiminta-asiakirjan mallin valmisteleminen muokkausta varten</span><span class="sxs-lookup"><span data-stu-id="976b7-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="976b7-115">Tee seuraavat toimet [Liiketoiminta-asiakirjan hallinnan yleiskatsaus](er-business-document-management.md) -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="976b7-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="976b7-116">Konfiguroi ER-parametrit</span><span class="sxs-lookup"><span data-stu-id="976b7-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="976b7-117">Tuo ER-ratkaisut</span><span class="sxs-lookup"><span data-stu-id="976b7-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="976b7-118">Ota liiketoiminta-asiakirjojen hallinta käyttöön</span><span class="sxs-lookup"><span data-stu-id="976b7-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="976b7-119">Konfiguroi parametrit</span><span class="sxs-lookup"><span data-stu-id="976b7-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="976b7-120">Liiketoiminta -asiakirjan mallin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="976b7-120">Edit a business document template</span></span>

1. <span data-ttu-id="976b7-121">Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="976b7-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="976b7-122">Valitse **Luo uusi malli** -sivulla **Vapaan tekstin lasku (ER-näyte)(Excel)** -malli.</span><span class="sxs-lookup"><span data-stu-id="976b7-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="976b7-123">Valitse **Luo asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="976b7-123">Select **Create document**.</span></span>
4. <span data-ttu-id="976b7-124">Syötä **Otsikko**-kenttään **FTI sample Litware**.</span><span class="sxs-lookup"><span data-stu-id="976b7-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="976b7-125">Luo uusi malli valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="976b7-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="976b7-126">Jos et ole vielä kirjautunut sisään Office Onlineen, sinut [ohjataan Office 365 -kirjautumissivulle](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="976b7-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="976b7-127">Voit palata Finance-ympäristöön valitsemalla selaimen **Edellinen**-painikkeen.</span><span class="sxs-lookup"><span data-stu-id="976b7-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="976b7-128">Uusi malli avataan muokkaamista varten mallieditori-sivun upotetussa Excel Online -ohjausobjektissa.</span><span class="sxs-lookup"><span data-stu-id="976b7-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="976b7-129">[![Liiketoiminta-asiakirjan hallinnan työtilan käyttäminen liiketoiminta-asiakirjan mallin muokkaamiseen](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="976b7-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="976b7-130">Muokattavan mallin nykyisen rakenteen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="976b7-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="976b7-131">Valitse Excel Onlinessa valintanauhan **Näkymä**-välilehden **Näytä**-ryhmästä **Ruudukko**.</span><span class="sxs-lookup"><span data-stu-id="976b7-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="976b7-132">Valitse muokattavan mallin otsikon yläpuolella oleva suorakulmio.</span><span class="sxs-lookup"><span data-stu-id="976b7-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="976b7-133">Tämä suorakulmio on kuva, jonka nimi on **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="976b7-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="976b7-134">Jos **Mallin rakenne** -ruutu on piilotettu, valitse **Näytä rakenne**.</span><span class="sxs-lookup"><span data-stu-id="976b7-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="976b7-135">Laajenna **Mallin rakenne** -ruudussa **Raportti \> Lasku \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="976b7-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="976b7-136">Huomaa, että Finances mallirakenteessa **rptHeaderCompLogo** -nimike esitetään **Report \> Invoice \> rptHeader \> rptHeaderPart1** -nimikkeen alielementtinä.</span><span class="sxs-lookup"><span data-stu-id="976b7-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="976b7-137">[![Liiketoiminta-asiakirjojen hallinnan työtilan käyttäminen muokattavan mallin nykyisen rakenteen tarkasteluun](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="976b7-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="976b7-138">Liiketoiminta-asiakirjan mallin rakenteen päivittäminen poistamalla kuva</span><span class="sxs-lookup"><span data-stu-id="976b7-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="976b7-139">Valitse Excel Onlinessa muokattavassa mallissa kuva **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="976b7-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="976b7-140">Poista valittu kuva muokattavana olevasta mallista noudattamalla jotakin seuraavista vaiheista:</span><span class="sxs-lookup"><span data-stu-id="976b7-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="976b7-141">Valitse **Delete**-näppäin näppäimistöltäsi.</span><span class="sxs-lookup"><span data-stu-id="976b7-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="976b7-142">Pidä kuvaa valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse **Leikkaa**.</span><span class="sxs-lookup"><span data-stu-id="976b7-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="976b7-143">The **rptHeaderCompLogo** nimike on edelleen Financen mallin rakenteessa, vaikka kuva ei enää sisälly Excel-malliin.</span><span class="sxs-lookup"><span data-stu-id="976b7-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="976b7-144">Valitsemalla **Päivitä rakenne** voit synkronoida Excelin ja Financen muokattavan mallin rakenteen.</span><span class="sxs-lookup"><span data-stu-id="976b7-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="976b7-145">Laajenna **Mallin rakenne** -ruudussa **Raportti \> Lasku \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="976b7-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="976b7-146">Huomaa, että **rptHeaderCompLogo**-nimike ei enää sisälly Financen mallirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="976b7-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="976b7-147">[![Liiketoiminta-asiakirjan hallinnan työtilan käyttäminen kuvan poistamiseen liiketoiminta-asiakirjan mallista](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="976b7-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="976b7-148">Liiketoiminta-asiakirjan mallin rakenteen päivittäminen lisäämällä kuva</span><span class="sxs-lookup"><span data-stu-id="976b7-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="976b7-149">Valitse Excel Onlinessa valintanauhan **Lisää**-välilehden **Kuvitus**-ryhmästä **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="976b7-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="976b7-150">Valitse **Valitse tiedosto**, siirry lisättävän kuvan kohdalle, valitse se ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="976b7-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="976b7-151">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="976b7-151">Select **Insert**.</span></span>
4. <span data-ttu-id="976b7-152">Siirrä uutta kuvaa, kunnes se on oikeassa paikassa.</span><span class="sxs-lookup"><span data-stu-id="976b7-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="976b7-153">Excel nimeää kuvan oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="976b7-153">By default, Excel names the picture.</span></span> <span data-ttu-id="976b7-154">Se voi esimerkiksi nimetä kuvan kuvaksi **Kuva 2**.</span><span class="sxs-lookup"><span data-stu-id="976b7-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="976b7-155">Valitsemalla **Päivitä rakenne** voit synkronoida Excelin ja Financen muokattavan mallin rakenteen.</span><span class="sxs-lookup"><span data-stu-id="976b7-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="976b7-156">Laajenna **Mallin rakenne** -ruudussa **Raportti \> Lasku \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="976b7-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="976b7-157">Huomaa, että uusi kuva sisältyy nyt nimikkeenä Financen mallirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="976b7-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="976b7-158">[![Liiketoiminta-asiakirjan hallinnan työtilan käyttäminen kuvan lisäämiseen liiketoiminta-asiakirjan malliin](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="976b7-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="976b7-159">Liittyvät linkit</span><span class="sxs-lookup"><span data-stu-id="976b7-159">Related links</span></span>

[<span data-ttu-id="976b7-160">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="976b7-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="976b7-161">Liiketoiminta-asiakirjojen hallinta – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="976b7-161">Business document management overview</span></span>](er-business-document-management.md)
