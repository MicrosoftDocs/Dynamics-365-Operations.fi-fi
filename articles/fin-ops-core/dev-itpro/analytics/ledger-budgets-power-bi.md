---
title: Todellinen vs. budjetti – Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään Todellinen vs. budjetti – Power BI -sisältöä Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184390"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="7b0cd-104">Todellinen vs. budjetti – Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="7b0cd-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b0cd-105">Tässä ohjeaiheessa käsitellään **Todellinen vs. budjetti** – Microsoft Power BI -sisältöä</span><span class="sxs-lookup"><span data-stu-id="7b0cd-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="7b0cd-106">Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="7b0cd-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="7b0cd-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7b0cd-107">Overview</span></span>

<span data-ttu-id="7b0cd-108">**Todellinen vs. budjetti** – Power BI -sisältö luotiin henkilöille, jotka vastaavat organisaatiossa todellisen ja budjetoidun suorituksen vertailun seurannasta.</span><span class="sxs-lookup"><span data-stu-id="7b0cd-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="7b0cd-109">**Todellinen vs. budjetti** – Power BI -sisältö tuo näkyvyyttä budjetin variansseihin.</span><span class="sxs-lookup"><span data-stu-id="7b0cd-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="7b0cd-110">Voit analysoida kuluvan vuoden budjettia tililuokan, budjettikoodin, päätilin, päätilin kuvauksen tai tilikauden mukaan. Saat tällä tavoin paremman käsityksen varianssien syystä.</span><span class="sxs-lookup"><span data-stu-id="7b0cd-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7b0cd-111">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="7b0cd-111">Accessing the Power BI content</span></span>
<span data-ttu-id="7b0cd-112">**Todellinen vs. budjetti** – Power BI -sisällön raportit näkyvät **Kirjanpitobudjetit ja ennusteet**- ja **Talousjohtaja**-työtiloissa.</span><span class="sxs-lookup"><span data-stu-id="7b0cd-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7b0cd-113">Raportit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="7b0cd-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="7b0cd-114">Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **Todellinen vs. budjetti** – Power BI -sisällön kultakin raporttisivulta.</span><span class="sxs-lookup"><span data-stu-id="7b0cd-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="7b0cd-115">Raportti</span><span class="sxs-lookup"><span data-stu-id="7b0cd-115">Report</span></span>                      | <span data-ttu-id="7b0cd-116">Mittarit</span><span class="sxs-lookup"><span data-stu-id="7b0cd-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0cd-117">Kulut – todellinen vs. budjetti</span><span class="sxs-lookup"><span data-stu-id="7b0cd-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="7b0cd-118">Kuluvan vuoden kokonaiskulut</span><span class="sxs-lookup"><span data-stu-id="7b0cd-118">Total expenses this year</span></span></li><li><span data-ttu-id="7b0cd-119">Kuluvan vuoden budjetoidut kokonaiskulut</span><span class="sxs-lookup"><span data-stu-id="7b0cd-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="7b0cd-120">Tuotto – todellinen vs. budjetti</span><span class="sxs-lookup"><span data-stu-id="7b0cd-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="7b0cd-121">Kuluvan vuoden kokonaistuotto</span><span class="sxs-lookup"><span data-stu-id="7b0cd-121">Total revenue this year</span></span></li><li><span data-ttu-id="7b0cd-122">Kuluvan vuoden budjetoitu kokonaistuotto</span><span class="sxs-lookup"><span data-stu-id="7b0cd-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="7b0cd-123">Kulu</span><span class="sxs-lookup"><span data-stu-id="7b0cd-123">Expense</span></span>                     | <ul><li><span data-ttu-id="7b0cd-124">Kuluvan vuoden kokonaiskulut</span><span class="sxs-lookup"><span data-stu-id="7b0cd-124">Total expenses this year</span></span></li><li><span data-ttu-id="7b0cd-125">Budjettiin perustuva kulutavoite</span><span class="sxs-lookup"><span data-stu-id="7b0cd-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="7b0cd-126">Myyntituotto</span><span class="sxs-lookup"><span data-stu-id="7b0cd-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="7b0cd-127">Kuluvan vuoden kokonaistuotto</span><span class="sxs-lookup"><span data-stu-id="7b0cd-127">Total revenue this year</span></span></li><li><span data-ttu-id="7b0cd-128">Budjettiin perustuva tuottotavoite</span><span class="sxs-lookup"><span data-stu-id="7b0cd-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="7b0cd-129">Nettotuotto</span><span class="sxs-lookup"><span data-stu-id="7b0cd-129">Net income</span></span>                  | <ul><li><span data-ttu-id="7b0cd-130">Kuluvan vuoden nettotulot</span><span class="sxs-lookup"><span data-stu-id="7b0cd-130">Net income this year</span></span></li><li><span data-ttu-id="7b0cd-131">Budjettiin perustuva nettotulotavoite</span><span class="sxs-lookup"><span data-stu-id="7b0cd-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="7b0cd-132">Tietomallin ja yksiköiden tiedot</span><span class="sxs-lookup"><span data-stu-id="7b0cd-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="7b0cd-133">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="7b0cd-133">Entity</span></span>                    | <span data-ttu-id="7b0cd-134">Sisältö</span><span class="sxs-lookup"><span data-stu-id="7b0cd-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b0cd-135">Kirjanpitotehtävät</span><span class="sxs-lookup"><span data-stu-id="7b0cd-135">General Ledger Activities</span></span> | <span data-ttu-id="7b0cd-136">Kirjanpidon tapahtumasummat</span><span class="sxs-lookup"><span data-stu-id="7b0cd-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="7b0cd-137">Budjettitehtävät</span><span class="sxs-lookup"><span data-stu-id="7b0cd-137">Budget Activities</span></span>         | <span data-ttu-id="7b0cd-138">Budjettirekisterin tapahtumasummat</span><span class="sxs-lookup"><span data-stu-id="7b0cd-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="7b0cd-139">Päätilit</span><span class="sxs-lookup"><span data-stu-id="7b0cd-139">Main Accounts</span></span>             | <span data-ttu-id="7b0cd-140">Päätilit, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="7b0cd-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="7b0cd-141">Kirjanpidon kalenterit</span><span class="sxs-lookup"><span data-stu-id="7b0cd-141">Fiscal Calendars</span></span>          | <span data-ttu-id="7b0cd-142">Kirjanpidon kalenterit, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="7b0cd-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="7b0cd-143">Kirjanpidot</span><span class="sxs-lookup"><span data-stu-id="7b0cd-143">Ledgers</span></span>                   | <span data-ttu-id="7b0cd-144">Kirjanpidot, joilla raporit suodatetaan nykyiseen kirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="7b0cd-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="7b0cd-145">Budjettikoodit</span><span class="sxs-lookup"><span data-stu-id="7b0cd-145">Budget Codes</span></span>              | <span data-ttu-id="7b0cd-146">Budjettikoodit, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="7b0cd-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="7b0cd-147">Yritykset</span><span class="sxs-lookup"><span data-stu-id="7b0cd-147">Legal Entities</span></span>            | <span data-ttu-id="7b0cd-148">Yritykset, joilla raporit suodatetaan nykyiseen yritykseen</span><span class="sxs-lookup"><span data-stu-id="7b0cd-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
