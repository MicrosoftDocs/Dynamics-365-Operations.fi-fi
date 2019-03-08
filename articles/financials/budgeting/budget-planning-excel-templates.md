---
title: Excelin budjettisuunnittelumallit
description: Tässä ohjeaiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 079aa6bb4be020fc050b81c400050ed23d48f6ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "337046"
---
# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="2a390-103">Excelin budjettisuunnittelumallit</span><span class="sxs-lookup"><span data-stu-id="2a390-103">Budget planning templates for Excel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a390-104">Tässä ohjeaiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="2a390-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="2a390-105">Tässä ohjeaiheessa kuvataan, miten luodaan Excel-malleja, joita käytetään budjettisuunnitelmissa käyttämällä vakionäytetietoja ja Järjestelmänvalvoja-käyttäjätunnusta.</span><span class="sxs-lookup"><span data-stu-id="2a390-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="2a390-106">Saat lisätietoja budjettisuunnittelusta artikkelista [Budjetin suunnittelun yhteenveto.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="2a390-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="2a390-107">Voit myös seurata [Budjettisuunnittelun perusteet](budget-plan.md) -opetusohjelma oppiaksesi perustiedot moduulin määrityksestä sekä käytön periaatteet.</span><span class="sxs-lookup"><span data-stu-id="2a390-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="2a390-108">Luo laskentataulukko budjettisuunnitelman asiakirja-asettelun avulla</span><span class="sxs-lookup"><span data-stu-id="2a390-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="2a390-109">Budjettisuunnitelma-asiakirjoja voi tarkastella ja muokata käyttämällä yhtä tai useampaa asettelua.</span><span class="sxs-lookup"><span data-stu-id="2a390-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="2a390-110">Kussakin asettelussa voi olla liitetty budjettisuunnitelman asiakirjamalli, jotta budjettisuunnitelman tietoja voidaan tarkastella ja muokata Excel-laskentataulukossa.</span><span class="sxs-lookup"><span data-stu-id="2a390-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="2a390-111">Tässä ohjeaiheessa luodaan budjettisuunnitelman asiakirjamalli käyttämällä valmista asettelumääritystä.</span><span class="sxs-lookup"><span data-stu-id="2a390-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="2a390-112">Avaa **Budjettisuunnitelmien luettelo** (**Budjetointi** &gt; **Budjettisuunnitelmat**).</span><span class="sxs-lookup"><span data-stu-id="2a390-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="2a390-113">Luo uusi budjettisuunnitelma-asiakirja valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2a390-113">Click **New** to create a new budget plan document.</span></span> 

   <span data-ttu-id="2a390-114">[![Budjettisuunnitelmaluettelo](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="2a390-115">Käytä **Lisää rivi** -vaihtoehtoa, jos haluat lisätä rivejä.</span><span class="sxs-lookup"><span data-stu-id="2a390-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="2a390-116">Voit tarkastella budjettisuunnitelman asiakirjan asettelun määrityksiä valitsemalla **Asettelut**.</span><span class="sxs-lookup"><span data-stu-id="2a390-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

   <span data-ttu-id="2a390-117">[![Budjettisuunnitelmien lisäys](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="2a390-118">Voit tarkistaa asettelun määritykset ja muuttaa niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2a390-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="2a390-119">Siirry kohtaan **Malli** &gt; **Luo** luodaksesi Excel-tiedoston tälle asettelulle.</span><span class="sxs-lookup"><span data-stu-id="2a390-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="2a390-120">Kun malli on luotu, siirry kohtaan **Malli** &gt; **Näytä** avataksesi ja tarkistaaksesi budjettisuunnitelman asiakirjamallin.</span><span class="sxs-lookup"><span data-stu-id="2a390-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="2a390-121">Voit tallentaa Excel-tiedoston paikalliseen asemaan.</span><span class="sxs-lookup"><span data-stu-id="2a390-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="2a390-122">[![Tallenna nimellä](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="2a390-123">Budjettisuunnitelman asiakirjan asettelua ei voi muokata, kun Excel-malli on liitetty siihen.</span><span class="sxs-lookup"><span data-stu-id="2a390-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="2a390-124">Voit muokata asettelua, poistamalla liitetyn Excel-mallitiedoston ja luomalla se uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2a390-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="2a390-125">Tämä tarvitaan pitämään asettelun kentät ja laskentataulukko synkronoituna.</span><span class="sxs-lookup"><span data-stu-id="2a390-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="2a390-126">Excel-malli sisältää budjettisuunnitelman asiakirja-asettelun kaikki osat, joiden **Käytettävissä työkirjassa** -sarakkeen arvo on Tosi.</span><span class="sxs-lookup"><span data-stu-id="2a390-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="2a390-127">Excel-mallissa ei sallita päällekkäisiä osia.</span><span class="sxs-lookup"><span data-stu-id="2a390-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="2a390-128">Esimerkiksi jos asettelu sisältää sarakkeet Request Q1, Request Q2, Request Q3 ja Request Q4 sekä summasarakkeen, joka edustaa kaikkien neljän neljännesvuosittaisen sarakkeen summaa, vain neljännesvuosittaisia sarakkeita tai summasaraketta voidaan käyttää Excel-mallissa.</span><span class="sxs-lookup"><span data-stu-id="2a390-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="2a390-129">Excel-tiedosto ei voi päivittää päällekkäisiä sarakkeita päivityksen aikana, koska taulukon tiedoista voi tulla vanhentuneita tai virheellisiä.</span><span class="sxs-lookup"><span data-stu-id="2a390-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="2a390-130">[![Esimerkki](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="2a390-131">Voit välttää mahdollisia ongelmia budjettisuunnitelman tietojen tarkastelemisessa ja muokkaamisessa Excelissä, jos sama käyttäjä on kirjautunut sekä Microsoft Dynamics 365 for Finance and Operationsiin että Microsoft Dynamics Office -apuohjelman tietoyhdistimeen.</span><span class="sxs-lookup"><span data-stu-id="2a390-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="2a390-132">Otsikon lisääminen budjettisuunnitelman asiakirjamalliin</span><span class="sxs-lookup"><span data-stu-id="2a390-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="2a390-133">Jos haluat lisätä otsikkotietoja, valitse ylin rivi Excel-tiedostossa ja lisää tyhjiä rivejä.</span><span class="sxs-lookup"><span data-stu-id="2a390-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="2a390-134">Lisää otsikkokentät Excel-tiedostoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2a390-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="2a390-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="2a390-136">Valitse **Rakenne**-välilehdessä, **Lisää kenttiä** ja sitten **BudgetPlanHeader** yksikön tietolähteeksi.</span><span class="sxs-lookup"><span data-stu-id="2a390-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="2a390-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="2a390-138">Siirrä kohdistin Excel-tiedostossa haluamaasi paikkaan.</span><span class="sxs-lookup"><span data-stu-id="2a390-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="2a390-139">Valitse **Lisää otsikko** lisätäksesi kentän otsikon valittuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="2a390-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="2a390-140">Valitse **Lisää arvo** lisätäksesi arvokentän valittuun paikkaan.</span><span class="sxs-lookup"><span data-stu-id="2a390-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="2a390-141">Valitse **Valmis** sulkeaksesi suunnitteluohjelman.</span><span class="sxs-lookup"><span data-stu-id="2a390-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="2a390-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="2a390-143">Lasketun sarakkeen lisääminen budjettisuunnitelman asiakirjamallin taulukkoon</span><span class="sxs-lookup"><span data-stu-id="2a390-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="2a390-144">Seuraavaksi, lasketut sarakkeet lisätään muodostettuun budjettisuunnitelman asiakirjamalliin.</span><span class="sxs-lookup"><span data-stu-id="2a390-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="2a390-145">**Total Request** -sarake, joka summaa sarakkeet Request Q1 – Request Q4 ja **Oikaisu**-sarakkeen, joka laskee **Total request** -sarakkeen esimääritetyn kertoimen avulla.</span><span class="sxs-lookup"><span data-stu-id="2a390-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="2a390-146">Lisää sarakkeet taulukkoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2a390-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="2a390-147">Valitse **Muokkaa** **BudgetPlanWorksheet**-tietolähteen vieressä aloittaaksesi sarakkeiden lisäämisen.</span><span class="sxs-lookup"><span data-stu-id="2a390-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="2a390-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="2a390-149">Valittu kenttäryhmää näyttää mallissa käytettävissä olevat sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="2a390-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="2a390-150">Valitse **Kaava**, kun haluat lisätä uuden sarakkeen.</span><span class="sxs-lookup"><span data-stu-id="2a390-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="2a390-151">Nimeä uusi sarake ja liitä sitten kaava **Kaava**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a390-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="2a390-152">Valitse **Päivitä**, jos haluat lisätä sarakkeen.</span><span class="sxs-lookup"><span data-stu-id="2a390-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="2a390-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="2a390-154">Luo kaava laskentataulukossa ja kopioi se **Rakenne**-ikkunaan määrittääksesi kaavan.</span><span class="sxs-lookup"><span data-stu-id="2a390-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="2a390-155">Finance and Operationsin sidottu taulukko nimeksi annetaan yleensä AXTable1.</span><span class="sxs-lookup"><span data-stu-id="2a390-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="2a390-156">Jos esimerkiksi haluat summata laskentataulukossa sarakkeet Request Q1 – Request Q4, kaava on: AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span><span class="sxs-lookup"><span data-stu-id="2a390-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="2a390-157">Toista nämä vaiheet lisätäksesi **Oikaisu**-sarakkeen.</span><span class="sxs-lookup"><span data-stu-id="2a390-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="2a390-158">Käytä tälle sarakkeelle kaavaa = AxTable1\[Total request\]\*$I$1.</span><span class="sxs-lookup"><span data-stu-id="2a390-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="2a390-159">Tämä ottaa solun I1 arvon ja kertoo **Total request** -sarakkeen laskeakseen oikaisusummat.</span><span class="sxs-lookup"><span data-stu-id="2a390-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="2a390-160">Tallenna ja sulje Excel-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="2a390-160">Save and close the Excel file.</span></span> <span data-ttu-id="2a390-161">Palaa Finance and Operationsiin ja lataa budjettisuunnitelmassa käytettävä tallennettu Excel-malli valitsemalla **Asettelu**-kohdassa **Malli &gt; Lataa**.</span><span class="sxs-lookup"><span data-stu-id="2a390-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="2a390-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="2a390-163">Sulje **Asettelut**-liukusäädin.</span><span class="sxs-lookup"><span data-stu-id="2a390-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="2a390-164">Valitse **Budjettisuunnitelma**-asiakirjassa **Työkirja**, jolloin voit tarkastella ja muokata asiakirjaa Excelissä.</span><span class="sxs-lookup"><span data-stu-id="2a390-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="2a390-165">Huomaa, että tämän budjettisuunnitelman työkirjan luomiseen käytettiin oikaistua Excel-mallia, ja lasketut sarakkeet päivitetään käyttäen kaavoja, jotka määritettiin edellisissä vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="2a390-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="2a390-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="2a390-167">Vinkkejä budjettisuunnitelman mallien luomiseen</span><span class="sxs-lookup"><span data-stu-id="2a390-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="2a390-168">Voinko lisätä ja käyttää muita tietolähteitä budjettisuunnitelman malliin?</span><span class="sxs-lookup"><span data-stu-id="2a390-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="2a390-169">Kyllä, voit käyttää **Rakenne**-valikkoa lisätäksesi lisäyksikköjä samaan tai muihin taulukoihin Excel-mallissa.</span><span class="sxs-lookup"><span data-stu-id="2a390-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="2a390-170">Esimerkiksi, voit lisätä **BudgetPlanProposedProject**-tietolähteen luodaksesi ja ylläpitääksesi ehdotettujen projektien luetteloa samaan aikaan kun työstät budjettisuunnitelman tietoja Excelissä.</span><span class="sxs-lookup"><span data-stu-id="2a390-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="2a390-171">Huomaa, että suuren datamäärän tietolähteiden lisääminen saattaa heikentää Excel-työkirjan suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="2a390-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="2a390-172">Voit käyttää **Suodatin** -vaihtoehtoa kohdassa **Data Connector** lisätäksesi haluamasi suodattimet muihin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="2a390-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="2a390-173">Voinko piilottaa Rakenne-toiminnon Data Connectorissa muilta käyttäjiltä?</span><span class="sxs-lookup"><span data-stu-id="2a390-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="2a390-174">Kyllä, avaa **Data Connector** -asetukset piilottaaksesi **Rakenne**-vaihtoehdon muilta käyttäjiltä.</span><span class="sxs-lookup"><span data-stu-id="2a390-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="2a390-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="2a390-176">Laajenna **Data connector -asetukset** ja tyhjennä **Ota rakenne käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2a390-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="2a390-177">Tämä piilottaa **Rakenne**-asetuksen **Data connector** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="2a390-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="2a390-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="2a390-179">Voinko estää käyttäjiä vahingossa sulkemasta Data Connectorin, kun he työstävät tietoja?</span><span class="sxs-lookup"><span data-stu-id="2a390-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="2a390-180">Suosittelemme, että haluat estää käyttäjiä sulkemasta mallin lukitsemalla mallin.</span><span class="sxs-lookup"><span data-stu-id="2a390-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="2a390-181">Voit määrittää lukituksen valitsemalla **Data connector** oikeassa yläkulmassa, jolloin näkyviin tulee nuoli.</span><span class="sxs-lookup"><span data-stu-id="2a390-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="2a390-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="2a390-183">Klikkaamalla nuolta näet lisävalikon.</span><span class="sxs-lookup"><span data-stu-id="2a390-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="2a390-184">Valitse **Lukitse**.</span><span class="sxs-lookup"><span data-stu-id="2a390-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="2a390-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="2a390-186">voinko käyttää muita Excelin ominaisuuksia, kuten solun muotoilua, värejä, ehdollista muotoilua ja kaavioita omissa budjettisuunnitelmamalleissani?</span><span class="sxs-lookup"><span data-stu-id="2a390-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="2a390-187">Kyllä, useimmat Excelin perusominaisuudet toimivat budjettisuunnitelmamalleissa.</span><span class="sxs-lookup"><span data-stu-id="2a390-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="2a390-188">On suositeltavaa käyttää värikoodausta käyttäjille, jotta he erottavat Vain luku- ja muokattavat sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="2a390-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="2a390-189">Ehdollista muotoilua voi käyttää korostamaan budjetin ongelmallisia alueita.</span><span class="sxs-lookup"><span data-stu-id="2a390-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="2a390-190">Sarakkeiden summat voidaan esittää helposti tavallisten Excel-kaavojen (taulukon yläpuolella) avulla.</span><span class="sxs-lookup"><span data-stu-id="2a390-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="2a390-191">Voit myös luoda ja käyttää pivot-taulukoita ja kaavioita budjetin tietojen ylimääräisiin ryhmittelyihin ja visualisointeihin.</span><span class="sxs-lookup"><span data-stu-id="2a390-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="2a390-192">Valitse **Tiedot**-välilehden **Yhteydet**-ryhmässä **Päivitä kaikki** ja sitten **Yhteyden ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="2a390-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="2a390-193">Valitse **Käyttö**-välilehti ja valitse kohdassa **Päivitä** **Päivitä tiedot, kun tiedosto avataan** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2a390-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="2a390-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="2a390-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>



