--- 
title: "Vaakasuuntaisesti laajennettavia alueita käyttävän muodon suorittaminen sarakkeiden lisäämiseksi dynaamisesti sähköistä raportointia (ER) varten"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="22183-103">Vaakasuuntaisesti laajennettavia alueita käyttävän muodon suorittaminen sarakkeiden lisäämiseksi dynaamisesti sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="22183-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22183-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla.</span><span class="sxs-lookup"><span data-stu-id="22183-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="22183-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="22183-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="22183-106">Näiden toimien suorittamisen edellytys on, että "ER Luo vaakasuunnassa laajennettavia alueita dynaamisten Excel-sarakkeiden luomista varten (osa 1: suunnittele muoto)" -menettelyn vaiheet on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="22183-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="22183-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="22183-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="22183-108">Etsi luotu muoto</span><span class="sxs-lookup"><span data-stu-id="22183-108">Find created format</span></span>
1. <span data-ttu-id="22183-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="22183-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="22183-110">Laajenna puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="22183-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="22183-111">Valitse puussa "Financial dimensions sample model\Sample report with horizontally expandable ranges".</span><span class="sxs-lookup"><span data-stu-id="22183-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="22183-112">Luo Excel-tuotos suorittamalla muoto</span><span class="sxs-lookup"><span data-stu-id="22183-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="22183-113">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="22183-113">Click Run.</span></span>
2. <span data-ttu-id="22183-114">Kirjoita Dimension nimi -kenttään "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="22183-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="22183-115">Syötä tai valitse Dimension nimi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="22183-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="22183-116">Jos haluat valita kaikki nykyisen yrityksen dimensiot, kirjoita seuraavat: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="22183-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="22183-117">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="22183-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="22183-118">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="22183-118">Click Filter.</span></span>
5. <span data-ttu-id="22183-119">Valitse Kirjanpidon kirjauskansio -taulukon rivi ja Kirjauskansion eränumero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="22183-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="22183-120">Syötä Ehdot-kenttään "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="22183-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="22183-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="22183-121">00057..00058</span></span>  
7. <span data-ttu-id="22183-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22183-122">Click OK.</span></span>
8. <span data-ttu-id="22183-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22183-123">Click OK.</span></span>
    * <span data-ttu-id="22183-124">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="22183-124">Review the generated output.</span></span> <span data-ttu-id="22183-125">Huomaa, että juuri luotu Excel-tiedosto sisältää saman määrän sarakkeita, jotka valittiin taloushallinnon dimensioille.</span><span class="sxs-lookup"><span data-stu-id="22183-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="22183-126">Näiden sarakkeiden ylätunniste edustaa taloushallinnon dimensioiden nimiä.</span><span class="sxs-lookup"><span data-stu-id="22183-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="22183-127">Näiden sarakkeiden tapahtumarivit edustavat taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="22183-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="22183-128">Aja raportti ja valitse eri dimensioita, jotta näet, että raportti ei ole riippuvainen valittujen dimensioiden määrästä tai tälle Dynamics 365 for Finance and Operations, Enterprise Edition -esiintymälle konfiguroitujen dimensioiden määrästä.</span><span class="sxs-lookup"><span data-stu-id="22183-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


