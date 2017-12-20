---
title: "Todellinen vs. budjetti – Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään Todellinen vs. budjetti – Power BI -sisältöä Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: fi-fi
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="25fa6-104">Todellinen vs. budjetti – Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="25fa6-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="25fa6-105">Tässä ohjeaiheessa käsitellään **Todellinen vs. budjetti** – Microsoft Power BI -sisältöä</span><span class="sxs-lookup"><span data-stu-id="25fa6-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="25fa6-106">Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.</span><span class="sxs-lookup"><span data-stu-id="25fa6-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="25fa6-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="25fa6-107">Overview</span></span>

<span data-ttu-id="25fa6-108">**Todellinen vs. budjetti** – Power BI -sisältö luotiin henkilöille, jotka vastaavat organisaatiossa todellisen ja budjetoidun suorituksen vertailun seurannasta.</span><span class="sxs-lookup"><span data-stu-id="25fa6-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="25fa6-109">**Todellinen vs. budjetti** – Power BI -sisältö tuo näkyvyyttä budjetin variansseihin.</span><span class="sxs-lookup"><span data-stu-id="25fa6-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="25fa6-110">Voit analysoida kuluvan vuoden budjettia tililuokan, budjettikoodin, päätilin, päätilin kuvauksen tai tilikauden mukaan. Saat tällä tavoin paremman käsityksen varianssien syystä.</span><span class="sxs-lookup"><span data-stu-id="25fa6-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="25fa6-111">Power BI -sisällön käyttö</span><span class="sxs-lookup"><span data-stu-id="25fa6-111">Accessing the Power BI content</span></span>
<span data-ttu-id="25fa6-112">**Todellinen vs. budjetti** – Power BI -sisällön raportit näkyvät **Kirjanpitobudjetit ja ennusteet**- ja **Talousjohtaja**-työtiloissa.</span><span class="sxs-lookup"><span data-stu-id="25fa6-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="25fa6-113">Raportit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="25fa6-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="25fa6-114">Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **Todellinen vs. budjetti** – Power BI -sisällön kultakin raporttisivulta.</span><span class="sxs-lookup"><span data-stu-id="25fa6-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="25fa6-115">Raportti</span><span class="sxs-lookup"><span data-stu-id="25fa6-115">Report</span></span>                      | <span data-ttu-id="25fa6-116">Mittarit</span><span class="sxs-lookup"><span data-stu-id="25fa6-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="25fa6-117">Kulut – todellinen vs. budjetti</span><span class="sxs-lookup"><span data-stu-id="25fa6-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="25fa6-118">Kuluvan vuoden kokonaiskulut</span><span class="sxs-lookup"><span data-stu-id="25fa6-118">Total expenses this year</span></span></li><li><span data-ttu-id="25fa6-119">Kuluvan vuoden budjetoidut kokonaiskulut</span><span class="sxs-lookup"><span data-stu-id="25fa6-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="25fa6-120">Tuotto – todellinen vs. budjetti</span><span class="sxs-lookup"><span data-stu-id="25fa6-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="25fa6-121">Kuluvan vuoden kokonaistuotto</span><span class="sxs-lookup"><span data-stu-id="25fa6-121">Total revenue this year</span></span></li><li><span data-ttu-id="25fa6-122">Kuluvan vuoden budjetoitu kokonaistuotto</span><span class="sxs-lookup"><span data-stu-id="25fa6-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="25fa6-123">Kulu</span><span class="sxs-lookup"><span data-stu-id="25fa6-123">Expense</span></span>                     | <ul><li><span data-ttu-id="25fa6-124">Kuluvan vuoden kokonaiskulut</span><span class="sxs-lookup"><span data-stu-id="25fa6-124">Total expenses this year</span></span></li><li><span data-ttu-id="25fa6-125">Budjettiin perustuva kulutavoite</span><span class="sxs-lookup"><span data-stu-id="25fa6-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="25fa6-126">Myyntituotto</span><span class="sxs-lookup"><span data-stu-id="25fa6-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="25fa6-127">Kuluvan vuoden kokonaistuotto</span><span class="sxs-lookup"><span data-stu-id="25fa6-127">Total revenue this year</span></span></li><li><span data-ttu-id="25fa6-128">Budjettiin perustuva tuottotavoite</span><span class="sxs-lookup"><span data-stu-id="25fa6-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="25fa6-129">Nettotuotto</span><span class="sxs-lookup"><span data-stu-id="25fa6-129">Net income</span></span>                  | <ul><li><span data-ttu-id="25fa6-130">Kuluvan vuoden nettotulot</span><span class="sxs-lookup"><span data-stu-id="25fa6-130">Net income this year</span></span></li><li><span data-ttu-id="25fa6-131">Budjettiin perustuva nettotulotavoite</span><span class="sxs-lookup"><span data-stu-id="25fa6-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="25fa6-132">Power BI -sisällön laajentaminen</span><span class="sxs-lookup"><span data-stu-id="25fa6-132">Extending the Power BI content</span></span>
<span data-ttu-id="25fa6-133">Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä.</span><span class="sxs-lookup"><span data-stu-id="25fa6-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="25fa6-134">Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="25fa6-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="25fa6-135">**Todellinen vs. budjetti** – Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="25fa6-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="25fa6-136">Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="25fa6-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="25fa6-137">Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="25fa6-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="25fa6-138">Tietomallin ja yksiköiden tiedot</span><span class="sxs-lookup"><span data-stu-id="25fa6-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="25fa6-139">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="25fa6-139">Entity</span></span>                    | <span data-ttu-id="25fa6-140">Sisältö</span><span class="sxs-lookup"><span data-stu-id="25fa6-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="25fa6-141">Kirjanpitotehtävät</span><span class="sxs-lookup"><span data-stu-id="25fa6-141">General Ledger Activities</span></span> | <span data-ttu-id="25fa6-142">Kirjanpidon tapahtumasummat</span><span class="sxs-lookup"><span data-stu-id="25fa6-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="25fa6-143">Budjettitehtävät</span><span class="sxs-lookup"><span data-stu-id="25fa6-143">Budget Activities</span></span>         | <span data-ttu-id="25fa6-144">Budjettirekisterin tapahtumasummat</span><span class="sxs-lookup"><span data-stu-id="25fa6-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="25fa6-145">Päätilit</span><span class="sxs-lookup"><span data-stu-id="25fa6-145">Main Accounts</span></span>             | <span data-ttu-id="25fa6-146">Päätilit, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="25fa6-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="25fa6-147">Kirjanpidon kalenterit</span><span class="sxs-lookup"><span data-stu-id="25fa6-147">Fiscal Calendars</span></span>          | <span data-ttu-id="25fa6-148">Kirjanpidon kalenterit, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="25fa6-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="25fa6-149">Kirjanpidot</span><span class="sxs-lookup"><span data-stu-id="25fa6-149">Ledgers</span></span>                   | <span data-ttu-id="25fa6-150">Kirjanpidot, joilla raporit suodatetaan nykyiseen kirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="25fa6-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="25fa6-151">Budjettikoodit</span><span class="sxs-lookup"><span data-stu-id="25fa6-151">Budget Codes</span></span>              | <span data-ttu-id="25fa6-152">Budjettikoodit, joiden mukaan raportit suodatetaan</span><span class="sxs-lookup"><span data-stu-id="25fa6-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="25fa6-153">Yritykset</span><span class="sxs-lookup"><span data-stu-id="25fa6-153">Legal Entities</span></span>            | <span data-ttu-id="25fa6-154">Yritykset, joilla raporit suodatetaan nykyiseen yritykseen</span><span class="sxs-lookup"><span data-stu-id="25fa6-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

