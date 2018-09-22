---
title: "Järjestä Report Designerin raporttiosat"
description: "Kun olet suunnitellut rakennusosat ja luonut raportit, kyseiset objektit kannattaa järjestää niin, että käyttäjien on helppo löytää ne. Tässä artikkelissa käsitellään aiemmin luotujen Report Designerin raporttien, rakennusosien ja objektien järjestämistä."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c9772d45cf9d9941dd8fe0de13ce624ea3aa3b53
ms.contentlocale: fi-fi
ms.lasthandoff: 08/13/2018

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="2641f-104">Järjestä Report Designerin raporttiosat</span><span class="sxs-lookup"><span data-stu-id="2641f-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2641f-105">Kun olet suunnitellut rakennusosat ja luonut raportit, kyseiset objektit kannattaa järjestää niin, että käyttäjien on helppo löytää ne.</span><span class="sxs-lookup"><span data-stu-id="2641f-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="2641f-106">Tässä artikkelissa käsitellään aiemmin luotujen Report Designerin raporttien, rakennusosien ja objektien järjestämistä.</span><span class="sxs-lookup"><span data-stu-id="2641f-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="2641f-107">Voit nimetä uudelleen kansioita, raportteja, rakenneosia ja muita objekteja Report Designerissa.</span><span class="sxs-lookup"><span data-stu-id="2641f-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="2641f-108">Uudelleennimetyn objektityypistä riippuen voit joutua päivittämään kyseisen objektin liitokset.</span><span class="sxs-lookup"><span data-stu-id="2641f-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="2641f-109">Kansion tai rakenneosan nimeäminen uudelleen Report Designerissa</span><span class="sxs-lookup"><span data-stu-id="2641f-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="2641f-110">Raporttien suunnitteluohjelmalla voidaan nimetä uudelleen kansiot sekä raportti-, rivi-, sarake- ja raporttipuumääritykset.</span><span class="sxs-lookup"><span data-stu-id="2641f-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

> [!NOTE]
> <span data-ttu-id="2641f-111">Kun nimeät rakenneosan uudelleen, myös kyseistä rakenneosaa käyttävät raportin määritykset on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="2641f-111">When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="2641f-112">Muussa tapauksessa uutta raporttia ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="2641f-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="2641f-113">Kansion tai rakenneosan nimeäminen uudelleen Report Designerissa</span><span class="sxs-lookup"><span data-stu-id="2641f-113">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="2641f-114">Käytä Report Designerissa siirtymisruutua löytääksesi uudelleennimettävän kansion tai objektin.</span><span class="sxs-lookup"><span data-stu-id="2641f-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="2641f-115">Valitse kansio tai objekti hiiren kakkospainikkeella ja valitse sitten **Nimeä uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="2641f-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="2641f-116">Siirtymisruudun **Nimi**-kenttä tulee käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2641f-116">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="2641f-117">Kirjoita uusi nimi ja paina sitten Enter-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="2641f-117">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="2641f-118">Jos rakenneosa on rivin määritys, sarakkeen määritys tai raportointipuun määritys, muut siihen liitetyt rakenneosat on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="2641f-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="2641f-119">Valitse ensin vaiheessa 3 uudelleennimetty rakenneosa hiiren kakkospainikkeella, valitse sitten **Liitokset** ja valitse lopuksi luettelosta päivitettävä kohde.</span><span class="sxs-lookup"><span data-stu-id="2641f-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="2641f-120">Toista vaihe 4, kunnes kaikki liitokset on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="2641f-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="2641f-121">Reititysryhmien luonti ja hallinta</span><span class="sxs-lookup"><span data-stu-id="2641f-121">Create and manage report groups</span></span>
<span data-ttu-id="2641f-122">Voit ryhmitellä raporttimäärityksiä luodaksesi useita raportteja samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="2641f-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="2641f-123">Jos haluat luoda, muokata, poistaa ja luoda raporttiryhmiä, sinulla on oltava suunnittelijan tai järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="2641f-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="2641f-124">Käyttäjät, joilla on luontirooli, voivat luoda raporttiryhmiä. He voivat myös muokata käyttäjien raportin määritysten asetuksia raporttiryhmille.</span><span class="sxs-lookup"><span data-stu-id="2641f-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="2641f-125">Raporttiryhmän luonti</span><span class="sxs-lookup"><span data-stu-id="2641f-125">Create a report group</span></span>

1. <span data-ttu-id="2641f-126">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2641f-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="2641f-127">Avaa uusi raporttiryhmä katseluohjelman ikkunassa valitsemalla **Tiedosto**-valikossa **Uusi** &gt; **Raporttiryhmän määritys**.</span><span class="sxs-lookup"><span data-stu-id="2641f-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="2641f-128">Voit vaihtoehtoisesti napsauttaa työkalurivillä **Raporttiryhmä**-painiketta ![Raporttiryhmä](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Raporttiryhmä").</span><span class="sxs-lookup"><span data-stu-id="2641f-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="2641f-129">Valitse **Raporttiryhmä**-välilehti. Ohittaaksesi yksittäisiä raportin määrityksiä koskevat tiedot tätä raporttia luotaessa, valitse **Ohita yritys-, tiedot- ja päivä-määritykset yksittäisissä raporttimäärityksissä** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2641f-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="2641f-130">Yrityksen nimi, tietojen taso, alustava asetus ja päivämäärätiedot täytetään automaattisesti, mutta voit tehdä päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="2641f-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="2641f-131">Jos haluat luoda useita raportointivaluutan näyttäviä raportteja, valitse **Sisällytä kaikki raportointivaluutat** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2641f-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="2641f-132">Voit sitten käyttää useita näkymiä valitsemalla **Valuutta**-painikkeen verkkokatseluohjelmassa, kun katsot raporttia.</span><span class="sxs-lookup"><span data-stu-id="2641f-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="2641f-133">Valitse raporttiryhmään sisällytettävät raportit valitsemalla **Ryhmän raportit** -kentässä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="2641f-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="2641f-134">Jos haluat valita useita raportteja **Lisää**-valintaikkunassa, pidä Ctrl-näppäintä painettuna valitessasi raportteja.</span><span class="sxs-lookup"><span data-stu-id="2641f-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="2641f-135">Kun olet valinnut raportit, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2641f-135">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="2641f-136">Tallenna uusi raporttiryhmä valitsemalla **Tiedosto** &gt; **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2641f-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="2641f-137">Raporttiryhmän muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2641f-137">Modify a report group</span></span>

1. <span data-ttu-id="2641f-138">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2641f-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="2641f-139">Kaksoisnapsauta muokattavaa raporttiryhmää.</span><span class="sxs-lookup"><span data-stu-id="2641f-139">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="2641f-140">Tee tarvittavat muutokset **Raporttiryhmä**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="2641f-140">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="2641f-141">Tallenna muokattu raporttiryhmä valitsemalla **Tiedosto**-valikossa **Tallenna**. Vaihtoehtoisesti voi napsauttaa työkalurivillä **Tallenna**-painiketta ![Tallenna](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Tallenna").</span><span class="sxs-lookup"><span data-stu-id="2641f-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="2641f-142">[HUOMAUTUS] Jos olet ajoittanut raporttien luonnin tapahtumaan tietyin väliajoin, voit ohittaa nämä asetukset ja luoda raportin heti.</span><span class="sxs-lookup"><span data-stu-id="2641f-142">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="2641f-143">Raporttiryhmän raportin luonti</span><span class="sxs-lookup"><span data-stu-id="2641f-143">Generate a report group report</span></span>

1. <span data-ttu-id="2641f-144">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2641f-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="2641f-145">Avaa luotava raporttiryhmä.</span><span class="sxs-lookup"><span data-stu-id="2641f-145">Open the report group to generate.</span></span>
3. <span data-ttu-id="2641f-146">Luo raportteja napsauttamalla **Luo raportti** -painiketta ![Luo raportti](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Luo raportti").</span><span class="sxs-lookup"><span data-stu-id="2641f-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="2641f-147">Raporttiryhmän poistaminen</span><span class="sxs-lookup"><span data-stu-id="2641f-147">Delete a report group</span></span>

1. <span data-ttu-id="2641f-148">Valitse Report Designerin siirtymisruudussa **Raporttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2641f-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="2641f-149">Napsauta poistettavaa raporttiryhmää hiiren kakkospainikkeella ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="2641f-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="2641f-150">Kun vahvistussanoma avautuu, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2641f-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="2641f-151">Raporttiryhmä-välilehden ohjausobjektit</span><span class="sxs-lookup"><span data-stu-id="2641f-151">Report Group tab controls</span></span>
<span data-ttu-id="2641f-152">Seuraavassa taulukossa käsitellään **Raporttiryhmä**-välilehden ohjausobjekteja.</span><span class="sxs-lookup"><span data-stu-id="2641f-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2641f-153">Ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="2641f-153">Control</span></span></th>
<th><span data-ttu-id="2641f-154">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="2641f-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2641f-155">Yritys-, tiedot- ja päivä-määritysten ohittaminen yksittäisistä raporttimäärityksistä</span><span class="sxs-lookup"><span data-stu-id="2641f-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="2641f-156">Valitse tämä valintaruutu ohittaaksesi tähän raporttiryhmään kuuluvien raporttien yksittäiset raporttimääritykset vain näiden raporttien luonnissa.</span><span class="sxs-lookup"><span data-stu-id="2641f-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-157">Yrityksen nimi</span><span class="sxs-lookup"><span data-stu-id="2641f-157">Company name</span></span></td>
<td><span data-ttu-id="2641f-158">Valitse yritys, jota käytetään raporteissa.</span><span class="sxs-lookup"><span data-stu-id="2641f-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-159">Erittelytaso</span><span class="sxs-lookup"><span data-stu-id="2641f-159">Detail level</span></span></td>
<td><span data-ttu-id="2641f-160">Määritä raporttien yksityiskohtien taso.</span><span class="sxs-lookup"><span data-stu-id="2641f-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="2641f-161"><strong>Taloudellinen</strong> – Korkean tason yhteenvetoraportti.</span><span class="sxs-lookup"><span data-stu-id="2641f-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="2641f-162">Et voi porautua tileihin ja dimensioihin lukuun ottamatta niitä tilejä ja dimensioita, jotka on lisätty raportointipuun kautta.</span><span class="sxs-lookup"><span data-stu-id="2641f-162">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="2641f-163"><strong>Rahoitus &amp; Tili</strong>− Raportti, joka sisältää korkean tason yhteenveto- ja tilitietoja.</span><span class="sxs-lookup"><span data-stu-id="2641f-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="2641f-164"><strong>Rahoitus, Tili &amp; Tapahtuma</strong>− Raportti, joka sisältää korkean tason yhteenveto- ja tapahtumatietoja.</span><span class="sxs-lookup"><span data-stu-id="2641f-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-165">Alustava</span><span class="sxs-lookup"><span data-stu-id="2641f-165">Provisional</span></span></td>
<td><span data-ttu-id="2641f-166">Määritä raportteihin sisältyvät tehtävätyypit.</span><span class="sxs-lookup"><span data-stu-id="2641f-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="2641f-167"><strong>Vain kirjatut aktiviteetit</strong> – Sisällytä vain ne tapahtumat ja saldot, jotka kirjataan taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="2641f-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="2641f-168"><strong>Kirjatut ja kirjaamattomat aktiviteetit</strong> – Sisällytä kaikki ne tapahtumat ja saldot, jotka syötetään ja kirjataan taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="2641f-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="2641f-169"><strong>Vain kirjaamattomat aktiviteetit</strong> – Sisällytä vain ne tapahtumat ja saldot, jotka syötetään mutta joita ei kirjata taloushallinnon tietoihin.</span><span class="sxs-lookup"><span data-stu-id="2641f-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-170">Sisällytetään kaikki raportointivaluutat</span><span class="sxs-lookup"><span data-stu-id="2641f-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="2641f-171">Mahdolliset Microsoft Dynamics ERP -järjestelmässä määritetyt lisäraportointivaluutat on lueteltu täällä.</span><span class="sxs-lookup"><span data-stu-id="2641f-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="2641f-172">Valitsemalla tämän valintaruudun voit luoda lisäraportteja annetuissa valuutoissa.</span><span class="sxs-lookup"><span data-stu-id="2641f-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="2641f-173">Niitä raportteja voi sitten tarkastella verkkokatseluohjelmassa napsauttamalla <strong>Valuutta</strong>-painiketta ja valitsemalla valuutan.</span><span class="sxs-lookup"><span data-stu-id="2641f-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-174">Päivämäärätietoa ei ole tallennettu raportin määrityksiin</span><span class="sxs-lookup"><span data-stu-id="2641f-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="2641f-175">Perusjakso</span><span class="sxs-lookup"><span data-stu-id="2641f-175">Base period</span></span></li>
<li><span data-ttu-id="2641f-176">Perusvuosi</span><span class="sxs-lookup"><span data-stu-id="2641f-176">Base year</span></span></li>
<li><span data-ttu-id="2641f-177">Raportin ajanjakso</span><span class="sxs-lookup"><span data-stu-id="2641f-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="2641f-178">Vain oletusarvoiset perusjaksoasetukset tallennetaan raportin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="2641f-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-179">Päivämäärätiedot on tallennettu raportin määrityksiin</span><span class="sxs-lookup"><span data-stu-id="2641f-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="2641f-180">Raporttipäivämäärä</span><span class="sxs-lookup"><span data-stu-id="2641f-180">Report date</span></span></li>
<li><span data-ttu-id="2641f-181">Oletusperuskausi</span><span class="sxs-lookup"><span data-stu-id="2641f-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2641f-182">Raportit ryhmässä</span><span class="sxs-lookup"><span data-stu-id="2641f-182">Reports in group</span></span></td>
<td><span data-ttu-id="2641f-183">Lisää, poista ja tilaa uudelleen raporttiryhmän raportteja.</span><span class="sxs-lookup"><span data-stu-id="2641f-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="2641f-184">Jos haluat lisätä raporttiryhmään raporttimäärityksiä, avaa ryhmä kaksoisnapsauttamalla ja valitse sitten <strong>Lisää</strong>.</span><span class="sxs-lookup"><span data-stu-id="2641f-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="2641f-185">Valitse raporttiryhmään sisällytettävät raportit ja valitse sitten <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="2641f-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="2641f-186">Jos haluat poistaa raportin raporttiryhmästä, valitse ensin raportti ja sitten <strong>Poista</strong>.</span><span class="sxs-lookup"><span data-stu-id="2641f-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="2641f-187">Voit muokata raporttien luontijärjestystä valitsemalla ensin raportin luettelosta ja sitten <strong>Siirrä ylöspäin</strong> tai <strong>Siirrä alaspäin</strong>.</span><span class="sxs-lookup"><span data-stu-id="2641f-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="2641f-188">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2641f-188">Additional resources</span></span>

[<span data-ttu-id="2641f-189">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="2641f-189">Financial reporting</span></span>](financial-reporting-intro.md)

