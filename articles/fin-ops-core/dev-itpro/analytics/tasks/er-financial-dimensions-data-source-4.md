---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 4 – Raportin suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: a9a6f07d6c665097fabab4d3ec6d7fa5ba80b65d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406471"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="dbd53-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 4 – Raportin suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="dbd53-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbd53-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="dbd53-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="dbd53-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="dbd53-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="dbd53-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 3: raportin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="dbd53-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="dbd53-107">Sähköisen raportoinnin parametrit -sivulla on myös määritettävä asiakirjojen oletustyypit.</span><span class="sxs-lookup"><span data-stu-id="dbd53-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="dbd53-108">Asiakirjojen oletustyypit asetetaan myös, kun lataat ja tuot ER-kokoonpanon.</span><span class="sxs-lookup"><span data-stu-id="dbd53-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="dbd53-109">Aja raportti</span><span class="sxs-lookup"><span data-stu-id="dbd53-109">Run report</span></span>
1. <span data-ttu-id="dbd53-110">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="dbd53-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dbd53-111">Laajenna puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="dbd53-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="dbd53-112">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli\Kirjanpitokansion raportti".</span><span class="sxs-lookup"><span data-stu-id="dbd53-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="dbd53-113">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="dbd53-113">Click Run.</span></span>
<span data-ttu-id="dbd53-114">![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="dbd53-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="dbd53-115">Syötä tai valitse Dimension nimi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="dbd53-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="dbd53-116">Jos haluat valita kaikki nykyisen yrityksen dimensiot, kirjoita seuraavat tiedot: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="dbd53-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="dbd53-118">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="dbd53-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="dbd53-119">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="dbd53-119">Click Filter.</span></span>
8. <span data-ttu-id="dbd53-120">Valitse Kirjanpidon kirjauskansio -taulukon rivi ja Kirjauskansion eränumero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="dbd53-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="dbd53-121">Kirjoita Ehdot-kenttään 00057.</span><span class="sxs-lookup"><span data-stu-id="dbd53-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="dbd53-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dbd53-122">Click OK.</span></span>
11. <span data-ttu-id="dbd53-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dbd53-123">Click OK.</span></span>
<span data-ttu-id="dbd53-124">![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="dbd53-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="dbd53-125">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="dbd53-125">Review the generated output.</span></span> <span data-ttu-id="dbd53-126">Jokaiselle valitun erän tapahtumalle esitetään vastaavan dimensiojoukon taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="dbd53-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="dbd53-127">Aja raportti ja valitse eri dimensioita, jotta näet, että raportti ei ole riippuvainen valittujen dimensioiden määrästä tai tälle esiintymälle konfiguroitujen dimensioden määrästä.</span><span class="sxs-lookup"><span data-stu-id="dbd53-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Sähköisen raportoinnin konfiguroinnit -sivu](../media/er-financial-dimensions-guides-run4.png)
