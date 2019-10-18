---
title: Järjestä Report Designerin raporttiosat
description: Kun olet suunnitellut rakennusosat ja luonut raportit, kyseiset objektit kannattaa järjestää niin, että käyttäjien on helppo löytää ne. Tässä artikkelissa käsitellään aiemmin luotujen Report Designerin raporttien, rakennusosien ja objektien järjestämistä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4a4733dc4da7a8713ac7ddec5c96ae18c91edc18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185287"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="4b46f-104">Järjestä Report Designerin raporttiosat</span><span class="sxs-lookup"><span data-stu-id="4b46f-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b46f-105">Kun olet suunnitellut rakennusosat ja luonut raportit, kyseiset objektit kannattaa järjestää niin, että käyttäjien on helppo löytää ne.</span><span class="sxs-lookup"><span data-stu-id="4b46f-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="4b46f-106">Tässä artikkelissa käsitellään aiemmin luotujen Report Designerin raporttien, rakennusosien ja objektien järjestämistä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="4b46f-107">Voit nimetä uudelleen kansioita, raportteja, rakenneosia ja muita objekteja Report Designerissa.</span><span class="sxs-lookup"><span data-stu-id="4b46f-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="4b46f-108">Uudelleennimetyn objektityypistä riippuen voit joutua päivittämään kyseisen objektin liitokset.</span><span class="sxs-lookup"><span data-stu-id="4b46f-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="4b46f-109">Kansion tai rakenneosan nimeäminen uudelleen Report Designerissa</span><span class="sxs-lookup"><span data-stu-id="4b46f-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="4b46f-110">Raporttien suunnitteluohjelmalla voidaan nimetä uudelleen kansiot sekä raportti-, rivi-, sarake- ja raporttipuumääritykset.</span><span class="sxs-lookup"><span data-stu-id="4b46f-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="4b46f-111">Kansion tai rakenneosan nimeäminen uudelleen raporttien suunnitteluohjelmalla</span><span class="sxs-lookup"><span data-stu-id="4b46f-111">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="4b46f-112">Etsi kansio tai kohde, jonka haluat nimetä uudelleen, käyttämällä raporttien suunnitteluohjelman siirtymisruutua.</span><span class="sxs-lookup"><span data-stu-id="4b46f-112">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="4b46f-113">Valitse kansio tai objekti hiiren kakkospainikkeella ja valitse sitten **Nimeä uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-113">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="4b46f-114">Siirtymisruudun **Nimi**-kenttä tulee käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4b46f-114">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="4b46f-115">Kirjoita uusi nimi ja paina sitten Enter-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-115">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="4b46f-116">Jos rakenneosa on rivin määritys, sarakkeen määritys tai raportointipuun määritys, muut siihen liitetyt rakenneosat on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-116">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="4b46f-117">Valitse ensin vaiheessa 3 uudelleennimetty rakenneosa hiiren kakkospainikkeella, valitse sitten **Liitokset** ja valitse lopuksi luettelosta päivitettävä kohde.</span><span class="sxs-lookup"><span data-stu-id="4b46f-117">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="4b46f-118">Toista vaihe 4, kunnes kaikki liitokset on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="4b46f-118">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="4b46f-119">Reititysryhmien luonti ja hallinta</span><span class="sxs-lookup"><span data-stu-id="4b46f-119">Create and manage report groups</span></span>
<span data-ttu-id="4b46f-120">Voit ryhmitellä raporttimäärityksiä luodaksesi useita raportteja samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="4b46f-120">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="4b46f-121">Jos haluat luoda, muokata, poistaa ja luoda raporttiryhmiä, sinulla on oltava suunnittelijan tai järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="4b46f-121">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="4b46f-122">Käyttäjät, joilla on luontirooli, voivat luoda raporttiryhmiä. He voivat myös muokata käyttäjien raportin määritysten asetuksia raporttiryhmille.</span><span class="sxs-lookup"><span data-stu-id="4b46f-122">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="4b46f-123">Raporttiryhmän luonti</span><span class="sxs-lookup"><span data-stu-id="4b46f-123">Create a report group</span></span>

1. <span data-ttu-id="4b46f-124">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-124">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="4b46f-125">Avaa uusi raporttiryhmä katseluohjelman ikkunassa valitsemalla **Tiedosto**-valikossa **Uusi** &gt; **Raporttiryhmän määritys**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-125">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="4b46f-126">Voit vaihtoehtoisesti napsauttaa työkalurivillä **Raporttiryhmä**-painiketta ![Raporttiryhmä](media/report-group.gif "Raporttiryhmä").</span><span class="sxs-lookup"><span data-stu-id="4b46f-126">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="4b46f-127">Valitse **Raporttiryhmä**-välilehti. Ohittaaksesi yksittäisiä raportin määrityksiä koskevat tiedot tätä raporttia luotaessa, valitse **Ohita yritys-, tiedot- ja päivä-määritykset yksittäisissä raporttimäärityksissä** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4b46f-127">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="4b46f-128">Yrityksen nimi, tietojen taso, alustava asetus ja päivämäärätiedot täytetään automaattisesti, mutta voit tehdä päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-128">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="4b46f-129">Jos haluat luoda useita raportointivaluutan näyttäviä raportteja, valitse **Sisällytä kaikki raportointivaluutat** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4b46f-129">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="4b46f-130">Voit sitten käyttää useita näkymiä valitsemalla **Valuutta**-painikkeen verkkokatseluohjelmassa, kun katsot raporttia.</span><span class="sxs-lookup"><span data-stu-id="4b46f-130">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="4b46f-131">Valitse raporttiryhmään sisällytettävät raportit valitsemalla **Ryhmän raportit** -kentässä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-131">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="4b46f-132">Jos haluat valita useita raportteja **Lisää**-valintaikkunassa, pidä Ctrl-näppäintä painettuna valitessasi raportteja.</span><span class="sxs-lookup"><span data-stu-id="4b46f-132">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="4b46f-133">Kun olet valinnut raportit, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-133">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="4b46f-134">Tallenna uusi raporttiryhmä valitsemalla **Tiedosto** &gt; **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-134">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="4b46f-135">Raporttiryhmän muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="4b46f-135">Modify a report group</span></span>

1. <span data-ttu-id="4b46f-136">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-136">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="4b46f-137">Kaksoisnapsauta muokattavaa raporttiryhmää.</span><span class="sxs-lookup"><span data-stu-id="4b46f-137">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="4b46f-138">Tee tarvittavat muutokset **Raporttiryhmä**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-138">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="4b46f-139">Tallenna muokattu raporttiryhmä valitsemalla **Tiedosto**-valikossa **Tallenna**. Vaihtoehtoisesti voi napsauttaa työkalurivillä **Tallenna**-painiketta ![Tallenna](media/save.gif "Tallenna").</span><span class="sxs-lookup"><span data-stu-id="4b46f-139">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="4b46f-140">[HUOMAUTUS] Jos olet ajoittanut raporttien luonnin tapahtumaan tietyin väliajoin, voit ohittaa nämä asetukset ja luoda raportin heti.</span><span class="sxs-lookup"><span data-stu-id="4b46f-140">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="4b46f-141">Raporttiryhmän raportin luonti</span><span class="sxs-lookup"><span data-stu-id="4b46f-141">Generate a report group report</span></span>

1. <span data-ttu-id="4b46f-142">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-142">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="4b46f-143">Avaa luotava raporttiryhmä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-143">Open the report group to generate.</span></span>
3. <span data-ttu-id="4b46f-144">Luo raportteja napsauttamalla **Luo raportti** -painiketta ![Luo raportti](media/generate-report.gif "Luo raportti").</span><span class="sxs-lookup"><span data-stu-id="4b46f-144">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="4b46f-145">Raporttiryhmän poistaminen</span><span class="sxs-lookup"><span data-stu-id="4b46f-145">Delete a report group</span></span>

1. <span data-ttu-id="4b46f-146">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-146">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="4b46f-147">Napsauta poistettavaa raporttiryhmää hiiren kakkospainikkeella ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-147">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="4b46f-148">Kun vahvistussanoma avautuu, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4b46f-148">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="4b46f-149">Raporttiryhmä-välilehden ohjausobjektit</span><span class="sxs-lookup"><span data-stu-id="4b46f-149">Report Group tab controls</span></span>
<span data-ttu-id="4b46f-150">Seuraavassa taulukossa käsitellään **Raporttiryhmä**-välilehden ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="4b46f-150">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b46f-151">Ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="4b46f-151">Control</span></span></th>
<th><span data-ttu-id="4b46f-152">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4b46f-152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b46f-153">Yritys-, tiedot- ja päivä-määritysten ohittaminen yksittäisistä raporttimäärityksistä</span><span class="sxs-lookup"><span data-stu-id="4b46f-153">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="4b46f-154">Valitse tämä valintaruutu ohittaaksesi tähän raporttiryhmään kuuluvien raporttien yksittäiset raporttimääritykset vain näiden raporttien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="4b46f-154">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-155">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="4b46f-155">Company name</span></span></td>
<td><span data-ttu-id="4b46f-156">Valitse yritys, jota käytetään raporteissa.</span><span class="sxs-lookup"><span data-stu-id="4b46f-156">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-157">Erittelytaso</span><span class="sxs-lookup"><span data-stu-id="4b46f-157">Detail level</span></span></td>
<td><span data-ttu-id="4b46f-158">Määritä raporttien yksityiskohtien taso.</span><span class="sxs-lookup"><span data-stu-id="4b46f-158">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="4b46f-159"><strong>Taloudellinen</strong> – Korkean tason yhteenvetoraportti.</span><span class="sxs-lookup"><span data-stu-id="4b46f-159"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="4b46f-160">Et voi porautua tileihin ja dimensioihin lukuun ottamatta niitä tilejä ja dimensioita, jotka on lisätty raportointipuun kautta.</span><span class="sxs-lookup"><span data-stu-id="4b46f-160">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="4b46f-161"><strong>Rahoitus &amp; Tili</strong>− Raportti, joka sisältää korkean tason yhteenveto- ja tilitietoja.</span><span class="sxs-lookup"><span data-stu-id="4b46f-161"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="4b46f-162"><strong>Rahoitus, Tili &amp; Tapahtuma</strong>− Raportti, joka sisältää korkean tason yhteenveto- ja tapahtumatietoja.</span><span class="sxs-lookup"><span data-stu-id="4b46f-162"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-163">Alustava</span><span class="sxs-lookup"><span data-stu-id="4b46f-163">Provisional</span></span></td>
<td><span data-ttu-id="4b46f-164">Määritä raportteihin sisältyvät tehtävätyypit.</span><span class="sxs-lookup"><span data-stu-id="4b46f-164">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="4b46f-165"><strong>Vain kirjatut aktiviteetit</strong> – Sisällytä vain ne tapahtumat ja saldot, jotka kirjataan taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="4b46f-165"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="4b46f-166"><strong>Kirjatut ja kirjaamattomat aktiviteetit</strong> – Sisällytä kaikki ne tapahtumat ja saldot, jotka syötetään ja kirjataan taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="4b46f-166"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="4b46f-167"><strong>Vain kirjaamattomat aktiviteetit</strong> – Sisällytä vain ne tapahtumat ja saldot, jotka syötetään mutta joita ei kirjata taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="4b46f-167"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-168">Sisällytetään kaikki raportointivaluutat</span><span class="sxs-lookup"><span data-stu-id="4b46f-168">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="4b46f-169">Mahdolliset Microsoft Dynamics ERP -järjestelmässä määritetyt lisäraportointivaluutat on lueteltu täällä.</span><span class="sxs-lookup"><span data-stu-id="4b46f-169">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="4b46f-170">Valitsemalla tämän valintaruudun voit luoda lisäraportteja annetuissa valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="4b46f-170">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="4b46f-171">Niitä raportteja voi sitten tarkastella verkkokatseluohjelmassa napsauttamalla <strong>Valuutta</strong>-painiketta ja valitsemalla valuutan.</span><span class="sxs-lookup"><span data-stu-id="4b46f-171">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-172">Päivämäärätietoa ei ole tallennettu raportin määrityksiin</span><span class="sxs-lookup"><span data-stu-id="4b46f-172">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="4b46f-173">Perusjakso</span><span class="sxs-lookup"><span data-stu-id="4b46f-173">Base period</span></span></li>
<li><span data-ttu-id="4b46f-174">Perusvuosi</span><span class="sxs-lookup"><span data-stu-id="4b46f-174">Base year</span></span></li>
<li><span data-ttu-id="4b46f-175">Raportin ajanjakso</span><span class="sxs-lookup"><span data-stu-id="4b46f-175">Period covered</span></span></li>
</ul>
<span data-ttu-id="4b46f-176">Vain oletusarvoiset perusjaksoasetukset tallennetaan raportin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="4b46f-176">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-177">Päivämäärätiedot on tallennettu raportin määrityksiin</span><span class="sxs-lookup"><span data-stu-id="4b46f-177">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="4b46f-178">Raporttipäivämäärä</span><span class="sxs-lookup"><span data-stu-id="4b46f-178">Report date</span></span></li>
<li><span data-ttu-id="4b46f-179">Oletusperuskausi</span><span class="sxs-lookup"><span data-stu-id="4b46f-179">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="4b46f-180">Raportit ryhmässä</span><span class="sxs-lookup"><span data-stu-id="4b46f-180">Reports in group</span></span></td>
<td><span data-ttu-id="4b46f-181">Lisää, poista ja tilaa uudelleen raporttiryhmän raportteja.</span><span class="sxs-lookup"><span data-stu-id="4b46f-181">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="4b46f-182">Jos haluat lisätä raporttiryhmään raporttimäärityksiä, avaa ryhmä kaksoisnapsauttamalla ja valitse sitten <strong>Lisää</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b46f-182">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="4b46f-183">Valitse raporttiryhmään sisällytettävät raportit ja valitse sitten <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b46f-183">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="4b46f-184">Jos haluat poistaa raportin raporttiryhmästä, valitse ensin raportti ja sitten <strong>Poista</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b46f-184">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="4b46f-185">Voit muokata raporttien luontijärjestystä valitsemalla ensin raportin luettelosta ja sitten <strong>Siirrä ylöspäin</strong> tai <strong>Siirrä alaspäin</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b46f-185">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="4b46f-186">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4b46f-186">Additional resources</span></span>

[<span data-ttu-id="4b46f-187">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="4b46f-187">Financial reporting</span></span>](financial-reporting-intro.md)
