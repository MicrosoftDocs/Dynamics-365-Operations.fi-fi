---
title: ER Käytä vaakasuunnassa laajennettavia alueita sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin (Osa 2 – Muodon suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4596f7d7789ea44d49d7e7f273e4a52ee38dd90f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684520"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="3997e-103">ER Käytä vaakasuunnassa laajennettavia alueita sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin (Osa 2 – Muodon suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="3997e-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3997e-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla.</span><span class="sxs-lookup"><span data-stu-id="3997e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="3997e-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="3997e-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="3997e-106">Näiden toimien suorittamisen edellytys on, että "ER Luo vaakasuunnassa laajennettavia alueita dynaamisten Excel-sarakkeiden luomista varten (osa 1: suunnittele muoto)" -menettelyn vaiheet on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="3997e-106">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="3997e-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="3997e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="3997e-108">Etsi luotu muoto</span><span class="sxs-lookup"><span data-stu-id="3997e-108">Find created format</span></span>
1. <span data-ttu-id="3997e-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="3997e-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3997e-110">Laajenna puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="3997e-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="3997e-111">Valitse puussa "Financial dimensions sample model\Sample report with horizontally expandable ranges".</span><span class="sxs-lookup"><span data-stu-id="3997e-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="3997e-112">Luo Excel-tuotos suorittamalla muoto</span><span class="sxs-lookup"><span data-stu-id="3997e-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="3997e-113">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="3997e-113">Click Run.</span></span>
2. <span data-ttu-id="3997e-114">Kirjoita Dimension nimi -kenttään "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="3997e-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="3997e-115">Syötä tai valitse Dimension nimi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="3997e-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="3997e-116">Jos haluat valita kaikki nykyisen yrityksen dimensiot, kirjoita seuraavat: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="3997e-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="3997e-117">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="3997e-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="3997e-118">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="3997e-118">Click Filter.</span></span>
5. <span data-ttu-id="3997e-119">Valitse Kirjanpidon kirjauskansio -taulukon rivi ja Kirjauskansion eränumero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="3997e-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="3997e-120">Syötä Ehdot-kenttään "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="3997e-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="3997e-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="3997e-121">00057..00058</span></span>  
7. <span data-ttu-id="3997e-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3997e-122">Click OK.</span></span>
8. <span data-ttu-id="3997e-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3997e-123">Click OK.</span></span>
    * <span data-ttu-id="3997e-124">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="3997e-124">Review the generated output.</span></span> <span data-ttu-id="3997e-125">Huomaa, että juuri luotu Excel-tiedosto sisältää saman määrän sarakkeita, jotka valittiin taloushallinnon dimensioille.</span><span class="sxs-lookup"><span data-stu-id="3997e-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="3997e-126">Näiden sarakkeiden ylätunniste edustaa taloushallinnon dimensioiden nimiä.</span><span class="sxs-lookup"><span data-stu-id="3997e-126">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="3997e-127">Näiden sarakkeiden tapahtumarivit edustavat taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="3997e-127">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="3997e-128">Aja raportti ja valitse eri dimensioita, jotta näet, että raportti ei ole riippuvainen valittujen dimensioiden määrästä tai tälle esiintymälle konfiguroitujen dimensioden määrästä.</span><span class="sxs-lookup"><span data-stu-id="3997e-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

