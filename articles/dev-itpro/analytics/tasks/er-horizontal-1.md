--- 
title: "Excel-raporttien sarakkeiden dynaamisessa lisäämisessä käytettävien vaakasuuntaisesti laajennettavien alueiden muodon suunnitteleminen"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9c3cf17cd406a50a9f92e78991289f9139d7c73
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="16f91-103">Excel-raporttien sarakkeiden dynaamisessa lisäämisessä käytettävien vaakasuuntaisesti laajennettavien alueiden muodon suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="16f91-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16f91-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla.</span><span class="sxs-lookup"><span data-stu-id="16f91-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="16f91-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="16f91-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="16f91-106">Näiden vaiheiden edellytyksenä on seuraavien kolmen tehtäväoppaan suorittaminen:</span><span class="sxs-lookup"><span data-stu-id="16f91-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="16f91-107">ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi</span><span class="sxs-lookup"><span data-stu-id="16f91-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="16f91-108">ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 1: tietomallin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="16f91-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="16f91-109">ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 2: malliyhdistämismääritys).</span><span class="sxs-lookup"><span data-stu-id="16f91-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="16f91-110">Voit myös ladata ja tallentaa paikallisen kopion mallista, jossa on tässä oleva malliraportti, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="16f91-110">You must also download and save a local copy of the template with a sample report found here, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 


<span data-ttu-id="16f91-111">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="16f91-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="16f91-112">Uuden raporttikonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="16f91-112">Create a new report configuration</span></span>
1. <span data-ttu-id="16f91-113">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="16f91-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="16f91-114">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="16f91-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="16f91-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="16f91-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="16f91-116">Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.</span><span class="sxs-lookup"><span data-stu-id="16f91-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="16f91-117">Käytä etukäteen luotua mallia uuden raportin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="16f91-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="16f91-118">Kirjoita Nimi-kenttään "Malliraportti, joka sisältää vaakasuunnassa laajennettavat alueet".</span><span class="sxs-lookup"><span data-stu-id="16f91-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="16f91-119">Malliraportti, joka sisältää vaakasuunnassa laajennettavat alueet</span><span class="sxs-lookup"><span data-stu-id="16f91-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="16f91-120">Kirjoita Kuvaus-kenttään "Excel-tuotoksen luonti lisäämällä sarakkeita dynaamisesti".</span><span class="sxs-lookup"><span data-stu-id="16f91-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="16f91-121">Excel-tuotoksen luonti lisäämällä sarakkeita dynaamisesti</span><span class="sxs-lookup"><span data-stu-id="16f91-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="16f91-122">Valitse Tietomallin määritelmä -kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="16f91-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="16f91-123">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="16f91-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="16f91-124">Suunnittele raporttimuoto</span><span class="sxs-lookup"><span data-stu-id="16f91-124">Design the report format</span></span>
1. <span data-ttu-id="16f91-125">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="16f91-125">Click Designer.</span></span>
2. <span data-ttu-id="16f91-126">Ota käyttöön "Näytä tiedot" -painike.</span><span class="sxs-lookup"><span data-stu-id="16f91-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="16f91-127">Valitse toimintoruudussa Tuo.</span><span class="sxs-lookup"><span data-stu-id="16f91-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="16f91-128">Napsauta Tuo Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="16f91-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="16f91-129">Napsauta Liitteet.</span><span class="sxs-lookup"><span data-stu-id="16f91-129">Click Attachments.</span></span>
    * <span data-ttu-id="16f91-130">Tuo raportin malli.</span><span class="sxs-lookup"><span data-stu-id="16f91-130">Import the report’s template.</span></span> <span data-ttu-id="16f91-131">Käytä siihen lataamaasi Excel-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="16f91-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="16f91-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="16f91-132">Click New.</span></span>
7. <span data-ttu-id="16f91-133">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="16f91-133">Click File.</span></span>
8. <span data-ttu-id="16f91-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="16f91-134">Close the page.</span></span>
9. <span data-ttu-id="16f91-135">Syötä tai valitse Malli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="16f91-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="16f91-136">Valitse ladattu malli.</span><span class="sxs-lookup"><span data-stu-id="16f91-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="16f91-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="16f91-137">Click OK.</span></span>
    * <span data-ttu-id="16f91-138">Lisää uusi alue, josta luodaan dynaamisesti Excel-tuotos, jossa on (käyttäjän valintanäytöllä) valitsemasi määrä taloushallinnon dimensiosarakkeita.</span><span class="sxs-lookup"><span data-stu-id="16f91-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="16f91-139">Jokaisen sarakkeen jokainen solu edustaa yhden taloushallinnon dimension nimeä.</span><span class="sxs-lookup"><span data-stu-id="16f91-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="16f91-140">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="16f91-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="16f91-141">Valitse puussa solmu "Excel\Range".</span><span class="sxs-lookup"><span data-stu-id="16f91-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="16f91-142">Kirjoita Excel-alue -kenttään "DimNames".</span><span class="sxs-lookup"><span data-stu-id="16f91-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="16f91-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="16f91-143">DimNames</span></span>  
14. <span data-ttu-id="16f91-144">Valitse Vaakasuuntainen-vaihtoehto kentässä Replikointisuunta.</span><span class="sxs-lookup"><span data-stu-id="16f91-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="16f91-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="16f91-145">Click OK.</span></span>
16. <span data-ttu-id="16f91-146">Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="16f91-147">Valitse Siirrä ylöspäin.</span><span class="sxs-lookup"><span data-stu-id="16f91-147">Click Move up.</span></span>
18. <span data-ttu-id="16f91-148">Valitse puussa Excel = "SampleFinDimWsReport"\Cell<DimNames>.</span><span class="sxs-lookup"><span data-stu-id="16f91-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="16f91-149">Valitse Leikkaa.</span><span class="sxs-lookup"><span data-stu-id="16f91-149">Click Cut.</span></span>
20. <span data-ttu-id="16f91-150">Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="16f91-151">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="16f91-151">Click Paste.</span></span>
22. <span data-ttu-id="16f91-152">Laajenna puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="16f91-153">Laajenna puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.</span><span class="sxs-lookup"><span data-stu-id="16f91-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="16f91-154">Laajenna puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.</span><span class="sxs-lookup"><span data-stu-id="16f91-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="16f91-155">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.</span><span class="sxs-lookup"><span data-stu-id="16f91-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="16f91-156">Lisää uusi alue, josta luodaan dynaamisesti Excel-tuotos, jossa on (käyttäjän valintanäytöllä) valitsemasi määrä taloushallinnon dimensiosarakkeita.</span><span class="sxs-lookup"><span data-stu-id="16f91-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="16f91-157">Jokaisen sarakkeen jokainen solu edustaa yhden taloushallinnon dimension arvoa kullekin raportoinnin tapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="16f91-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="16f91-158">Valitse Lisää alue.</span><span class="sxs-lookup"><span data-stu-id="16f91-158">Click Add Range.</span></span>
27. <span data-ttu-id="16f91-159">Kirjoita Excel-alue -kenttään "DimValues".</span><span class="sxs-lookup"><span data-stu-id="16f91-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="16f91-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="16f91-160">DimValues</span></span>  
28. <span data-ttu-id="16f91-161">Valitse Vaakasuuntainen-vaihtoehto kentässä Replikointisuunta.</span><span class="sxs-lookup"><span data-stu-id="16f91-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="16f91-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="16f91-162">Click OK.</span></span>
30. <span data-ttu-id="16f91-163">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>.</span><span class="sxs-lookup"><span data-stu-id="16f91-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="16f91-164">Valitse Leikkaa.</span><span class="sxs-lookup"><span data-stu-id="16f91-164">Click Cut.</span></span>
32. <span data-ttu-id="16f91-165">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="16f91-166">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="16f91-166">Click Paste.</span></span>
34. <span data-ttu-id="16f91-167">Laajenna puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="16f91-168">Yhdistä muodon osat tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="16f91-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="16f91-169">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="16f91-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="16f91-170">Laajenna puussa "model: Data model Financial dimensions sample model".</span><span class="sxs-lookup"><span data-stu-id="16f91-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="16f91-171">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="16f91-172">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="16f91-173">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="16f91-174">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>.</span><span class="sxs-lookup"><span data-stu-id="16f91-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="16f91-175">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="16f91-176">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-176">Click Bind.</span></span>
9. <span data-ttu-id="16f91-177">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="16f91-178">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="16f91-179">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-179">Click Bind.</span></span>
12. <span data-ttu-id="16f91-180">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>.</span><span class="sxs-lookup"><span data-stu-id="16f91-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="16f91-181">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".</span><span class="sxs-lookup"><span data-stu-id="16f91-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="16f91-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-182">Click Bind.</span></span>
15. <span data-ttu-id="16f91-183">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>.</span><span class="sxs-lookup"><span data-stu-id="16f91-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="16f91-184">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".</span><span class="sxs-lookup"><span data-stu-id="16f91-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="16f91-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-185">Click Bind.</span></span>
18. <span data-ttu-id="16f91-186">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>.</span><span class="sxs-lookup"><span data-stu-id="16f91-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="16f91-187">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="16f91-188">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-188">Click Bind.</span></span>
21. <span data-ttu-id="16f91-189">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>.</span><span class="sxs-lookup"><span data-stu-id="16f91-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="16f91-190">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".</span><span class="sxs-lookup"><span data-stu-id="16f91-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="16f91-191">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-191">Click Bind.</span></span>
24. <span data-ttu-id="16f91-192">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>.</span><span class="sxs-lookup"><span data-stu-id="16f91-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="16f91-193">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="16f91-194">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-194">Click Bind.</span></span>
27. <span data-ttu-id="16f91-195">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>.</span><span class="sxs-lookup"><span data-stu-id="16f91-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="16f91-196">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="16f91-197">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-197">Click Bind.</span></span>
30. <span data-ttu-id="16f91-198">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.</span><span class="sxs-lookup"><span data-stu-id="16f91-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="16f91-199">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="16f91-200">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-200">Click Bind.</span></span>
33. <span data-ttu-id="16f91-201">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>.</span><span class="sxs-lookup"><span data-stu-id="16f91-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="16f91-202">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="16f91-203">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-203">Click Bind.</span></span>
36. <span data-ttu-id="16f91-204">Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.</span><span class="sxs-lookup"><span data-stu-id="16f91-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="16f91-205">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="16f91-206">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-206">Click Bind.</span></span>
39. <span data-ttu-id="16f91-207">Laajenna puussa "model: Data model Financial dimensions sample model\Dimensions setting: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="16f91-208">Valitse puussa "model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="16f91-209">Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>.</span><span class="sxs-lookup"><span data-stu-id="16f91-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="16f91-210">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-210">Click Bind.</span></span>
43. <span data-ttu-id="16f91-211">Valitse puussa "model: Data model Financial dimensions sample model\Dimensions setting: Record list".</span><span class="sxs-lookup"><span data-stu-id="16f91-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="16f91-212">Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.</span><span class="sxs-lookup"><span data-stu-id="16f91-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="16f91-213">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-213">Click Bind.</span></span>
46. <span data-ttu-id="16f91-214">Valitse puussa Excel = "SampleFinDimWsReport"\Cell<CompanyName>.</span><span class="sxs-lookup"><span data-stu-id="16f91-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="16f91-215">Valitse puussa "model: Data model Financial dimensions sample model\Company: String".</span><span class="sxs-lookup"><span data-stu-id="16f91-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="16f91-216">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="16f91-216">Click Bind.</span></span>
49. <span data-ttu-id="16f91-217">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="16f91-217">Click Save.</span></span>
50. <span data-ttu-id="16f91-218">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="16f91-218">Close the page.</span></span>


