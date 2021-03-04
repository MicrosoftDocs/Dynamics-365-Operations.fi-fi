---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tässä ohjeaiheessa käsitellään kysymyksiä, joita muilla käyttäjillä on ollut taloushallinnon raportoinnista.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070214"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="76231-103">Taloushallinnon raportoinnin usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="76231-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="76231-104">Tässä ohjeaiheessa käsitellään kysymyksiä, joita muilla käyttäjillä on ollut taloushallinnon raportoinnista.</span><span class="sxs-lookup"><span data-stu-id="76231-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="76231-105">Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?</span><span class="sxs-lookup"><span data-stu-id="76231-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="76231-106">Skenaario: esittely-yrityksellä USMF on taseraportti, jota se ei halua kaikkien taloushallinnon raportoinnin käyttäjien voivan nähdä D365:ssä.</span><span class="sxs-lookup"><span data-stu-id="76231-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="76231-107">Ratkaisu: voit rajoittaa yksittäisen raportin käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää raporttia.</span><span class="sxs-lookup"><span data-stu-id="76231-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="76231-108">Kirjaudu raporttien suunnitteluohjelmaan</span><span class="sxs-lookup"><span data-stu-id="76231-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="76231-109">Luo uusi puumääritys (Tiedosto | Uusi | Puumääritys) a.</span><span class="sxs-lookup"><span data-stu-id="76231-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="76231-110">Kaksoisnapsauta **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="76231-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="76231-111">i.</span><span class="sxs-lookup"><span data-stu-id="76231-111">i.</span></span>    <span data-ttu-id="76231-112">Valitse Käyttäjät ja ryhmät.</span><span class="sxs-lookup"><span data-stu-id="76231-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="76231-113">1. Valitse käyttäjät tai ryhmä, joiden haluat voivat käyttää tätä raporttia.</span><span class="sxs-lookup"><span data-stu-id="76231-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="76231-114">[![käyttäjänäyttö](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="76231-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="76231-115">[![suojausnäyttö](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="76231-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="76231-116">b.</span><span class="sxs-lookup"><span data-stu-id="76231-116">b.</span></span>    <span data-ttu-id="76231-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="76231-117">Click **Save**.</span></span>
  
<span data-ttu-id="76231-118">[![Tallenna-painike](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="76231-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="76231-119">Lisää uusi puumäärityksesi raportin määritykseen</span><span class="sxs-lookup"><span data-stu-id="76231-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="76231-120">[![puumäärityslomake](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="76231-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="76231-121">A.</span><span class="sxs-lookup"><span data-stu-id="76231-121">A.</span></span>  <span data-ttu-id="76231-122">Valitse puumäärityksessä Asetus ja valitse Raporttiyksikön valinta -kohdassa Sisällytä kaikki yksiköt</span><span class="sxs-lookup"><span data-stu-id="76231-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="76231-123">[![raporttiyksikön valintalomake](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="76231-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="76231-124">**Ennen:** [![ennen-näyttökuva](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="76231-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="76231-125">**Jälkeen:** [![jälkeen-näyttökuva](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="76231-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="76231-126">Huomautus: edellä kuvatun sanoman syy on se, että käyttäjällä ei ole raportin käyttöoikeutta yksikön suojauksen käyttöönoton jälkeen</span><span class="sxs-lookup"><span data-stu-id="76231-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="76231-127">Miten selvitän, mitkä tilit eivät täsmää saldojeni kanssa D365:ssä?</span><span class="sxs-lookup"><span data-stu-id="76231-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="76231-128">Jos sinulla on D365:ssä raportti, joka ei vastaa odotuksiasi, voit kokeilla seuraavia toimia täsmäämättömien tilien ja niiden varianssien tunnistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="76231-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="76231-129">Raporttien suunnitteluohjelmassa</span><span class="sxs-lookup"><span data-stu-id="76231-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="76231-130">Luo uusi rivimääritys a.</span><span class="sxs-lookup"><span data-stu-id="76231-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="76231-131">Valitse Muokkaa | Lisää rivit dimensioista i.</span><span class="sxs-lookup"><span data-stu-id="76231-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="76231-132">Valitse MainAccount [![Valitse päätili ‑näyttö_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="76231-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="76231-133">ii.</span><span class="sxs-lookup"><span data-stu-id="76231-133">ii.</span></span> <span data-ttu-id="76231-134">Valitse Ok b.</span><span class="sxs-lookup"><span data-stu-id="76231-134">Click Ok b.</span></span>    <span data-ttu-id="76231-135">Tallenna rivimääritys</span><span class="sxs-lookup"><span data-stu-id="76231-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="76231-136">Luo uusi sarakemääritys     [![Luo uusi sarakemääritys](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="76231-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="76231-137">Luo uusi raportin määritys a.</span><span class="sxs-lookup"><span data-stu-id="76231-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="76231-138">Valitse Asetukset ja poista [![Asetukset-lomakkeen](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png) valinta</span><span class="sxs-lookup"><span data-stu-id="76231-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="76231-139">Luo raportti.</span><span class="sxs-lookup"><span data-stu-id="76231-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="76231-140">Vie raportti Exceliin.</span><span class="sxs-lookup"><span data-stu-id="76231-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="76231-141">D365:ssä:</span><span class="sxs-lookup"><span data-stu-id="76231-141">In D365:</span></span> 
1.  <span data-ttu-id="76231-142">Valitse Kirjanpito | Kyselyt ja raportit | Pääkirja a.</span><span class="sxs-lookup"><span data-stu-id="76231-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="76231-143">Parametrit i.</span><span class="sxs-lookup"><span data-stu-id="76231-143">Parameters i.</span></span>  <span data-ttu-id="76231-144">Aloituspäivä: tilikauden alku ii.</span><span class="sxs-lookup"><span data-stu-id="76231-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="76231-145">Päivämäärään: päivämäärä, jolle olet luonut raportin iii.</span><span class="sxs-lookup"><span data-stu-id="76231-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="76231-146">Taloushallinnon dimensioyhdistelmä ”Asetettu päätili” [![Päätili-lomake](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="76231-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="76231-147">b.</span><span class="sxs-lookup"><span data-stu-id="76231-147">b.</span></span>    <span data-ttu-id="76231-148">Valitse Laske</span><span class="sxs-lookup"><span data-stu-id="76231-148">Click Calculate</span></span>

2.  <span data-ttu-id="76231-149">Vie raportti Exceliin</span><span class="sxs-lookup"><span data-stu-id="76231-149">Export the report to Excel</span></span>

<span data-ttu-id="76231-150">Nyt sinun pitäisi nyt pystyä kopioimaan tiedot FR Excel -raportista D365:n Pääkirja-raporttiin ja vertaamaan Loppusaldo-sarakkeita.</span><span class="sxs-lookup"><span data-stu-id="76231-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>
