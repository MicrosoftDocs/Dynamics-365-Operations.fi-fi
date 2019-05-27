---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 4 – Raportin suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544653"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a><span data-ttu-id="5ccef-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 4: raportin suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="5ccef-103">ER Use financial dimensions as a data source (Part 4: Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ccef-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="5ccef-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="5ccef-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="5ccef-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="5ccef-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 3: raportin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="5ccef-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="5ccef-107">Sähköisen raportoinnin parametrit -sivulla on myös määritettävä asiakirjojen oletustyypit.</span><span class="sxs-lookup"><span data-stu-id="5ccef-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="5ccef-108">Asiakirjojen oletustyypit asetetaan myös, kun lataat ja tuot ER-kokoonpanon.</span><span class="sxs-lookup"><span data-stu-id="5ccef-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="5ccef-109">Aja raportti</span><span class="sxs-lookup"><span data-stu-id="5ccef-109">Run report</span></span>
1. <span data-ttu-id="5ccef-110">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="5ccef-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5ccef-111">Laajenna puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="5ccef-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5ccef-112">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli\Kirjanpitokansion raportti".</span><span class="sxs-lookup"><span data-stu-id="5ccef-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="5ccef-113">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="5ccef-113">Click Run.</span></span>
5. <span data-ttu-id="5ccef-114">Kirjoita tai valitse Dimension nimi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="5ccef-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="5ccef-115">Jos haluat valita kaikki nykyisen yrityksen dimensiot, kirjoita seuraavat: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="5ccef-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="5ccef-116">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="5ccef-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="5ccef-117">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="5ccef-117">Click Filter.</span></span>
8. <span data-ttu-id="5ccef-118">Valitse Kirjanpidon kirjauskansio -taulukon rivi ja Kirjauskansion eränumero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="5ccef-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="5ccef-119">Kirjoita Ehdot-kenttään 00057.</span><span class="sxs-lookup"><span data-stu-id="5ccef-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="5ccef-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5ccef-120">Click OK.</span></span>
11. <span data-ttu-id="5ccef-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5ccef-121">Click OK.</span></span>
    * <span data-ttu-id="5ccef-122">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="5ccef-122">Review the generated output.</span></span> <span data-ttu-id="5ccef-123">Huomaa, että jokaiselle valitun erän tapahtumalle esitetään vastaavan dimensiojoukon taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="5ccef-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="5ccef-124">Aja raportti ja valitse eri dimensioita, jotta näet, että raportti ei ole riippuvainen valittujen dimensioiden määrästä tai tälle Dynamics 365 for Finance and Operations, Enterprise Edition -esiintymälle konfiguroitujen dimensioiden määrästä.</span><span class="sxs-lookup"><span data-stu-id="5ccef-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

