---
title: Kulujen hallinnan Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään Power BI -sisältöpaketin kulujen hallinnan sisältöä.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0dcb6114544b3817d8b80122a32759e67ad8dc94
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181700"
---
# <a name="expense-management-power-bi-content"></a><span data-ttu-id="0a1a2-103">Kulujen hallinnan Power BI -sisältö</span><span class="sxs-lookup"><span data-stu-id="0a1a2-103">Expense management Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a1a2-104">Tässä aiheessa käsitellään Power BI -sisällön kulujen hallinnan sisältöä.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-104">This topic describes what is included in the Expense management Power BI content.</span></span> 

## <a name="overview"></a><span data-ttu-id="0a1a2-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="0a1a2-105">Overview</span></span>
<span data-ttu-id="0a1a2-106">Versiosta 8.1 alkaen kulujen hallinnan kanssa on käytettävissä kaksi Power BI -sisältöpakettia.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-106">Two Power BI content packs are available for use with Expense management in version 8.1 and later.</span></span> 
- <span data-ttu-id="0a1a2-107">Kuluraportteja lähettäville työntekijöille on suunniteltu henkilökohtainen koontinäyttö.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-107">There is a personal dashboard designed for employees who submit expense reports.</span></span> 

  <span data-ttu-id="0a1a2-108">Tämä koontinäyttö on mukautettu antamaan käyttäjille tärkeitä tietoja lähettämättömistä ja lähetetyistä summista sekä historiatietoja ja muita tietoja kulutapahtumien historiasta.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-108">The dashboard is tailored to provide key information to individuals about unsubmitted and submitted amounts, as well as history and insights into expense transaction history.</span></span> <span data-ttu-id="0a1a2-109">Henkilökohtaisessa koontinäytössä on yksi sivu, jossa on käyttäjän kannalta tärkeimmät tiedot.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-109">The personal dashboard is a single page containing the most important information for the user.</span></span>

- <span data-ttu-id="0a1a2-110">Ostoreskontran käyttäjille ja esimiehille on oma hallinnan koontinäyttö.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-110">There is an admin dashboard designed for accounts payable clerks and managers.</span></span> <span data-ttu-id="0a1a2-111">Koontinäyttö on suunniteltu siten, että sen avulla voi seurata työntekijän kokonaiskuluja ja raportoida niistä.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-111">The dashboard is tailored toward tracking and reporting on overall employee expenses.</span></span> <span data-ttu-id="0a1a2-112">Siinä tärkeitä kulumittareita, kuten lähettämättömät kulut, kilometrimäärä ja kuluraporttien keskimääräinen summa.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-112">It provides key expense metrics, such as unsubmitted expenses, mileage, and average expense report amounts.</span></span> <span data-ttu-id="0a1a2-113">Se käyttää tapahtumatietoja, ja siinä on kaikkien yritysten kulujen hallinnan koostenäkymät.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-113">It uses transactional data and provides aggregate views of expense management across all companies.</span></span> <span data-ttu-id="0a1a2-114">Siinä on myös työntekijäkohtainen erittely ja mahdollisuus lisätä taloushallinnon dimension tietoja.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-114">It also provides a breakdown per employee, with the option to add financial dimension data.</span></span> <span data-ttu-id="0a1a2-115">Järjestelmänvalvojan kuluanalytiikan sisältö:</span><span class="sxs-lookup"><span data-stu-id="0a1a2-115">The Admin expense analytics content contains:</span></span> 
  - <span data-ttu-id="0a1a2-116">Yhteenvetosivu, jolla on tärkeitä mittareita kulujen summista sekä tietoja luonnosvaiheessa olevista, keskeneräisistä ja valmiista kuluraporteista.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-116">An overview page with key metrics about expense amounts and insights into draft, in process, and completed expense reports.</span></span> 
  - <span data-ttu-id="0a1a2-117">Työntekijätilastosivulla voi tarkastella työntekijäkohtaisia tietoja ajan, kustannuslajin ja tilastoryhmän perusteella.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-117">An employee statistics page to review individual details about an employee by time, cost type, and statistics group.</span></span> 
  - <span data-ttu-id="0a1a2-118">Työntekijän vertailusivulla voi vertailla useita työntekijöitä aikavälillä.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-118">An employee comparison page to compare multiple employees over time.</span></span> 

<span data-ttu-id="0a1a2-119">Kaikkien summat näytetään yrityksen valuuttana.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-119">All the amounts are shown in the company currency.</span></span> <span data-ttu-id="0a1a2-120">Kaikkien yritysten tiedot näytetään, mutta voit tarvittaessa lisätä yrityssuodattimen.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-120">Data for all companies are shown, but if needed you can add a company filter.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="0a1a2-121">Power BI -sisällön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="0a1a2-121">Accessing the Power BI content</span></span>
<span data-ttu-id="0a1a2-122">Expense Admin Dashboard.pbix- ja Expense Personal Dashboard.pbix-tiedostot (Power BI -sisältö) sijaistee Microsoft Dynamics Lifecycle Servicesin (LCS) jaettujen resurssien kirjastosta.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-122">You can find the Expense Admin Dashboard.pbix and Expense Personal Dashboard.pbix Power BI content in the Shared assets library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0a1a2-123">Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).</span><span class="sxs-lookup"><span data-stu-id="0a1a2-123">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).</span></span>
<span data-ttu-id="0a1a2-124">Sisältö on käytettävissä kulujenhallinnan työtilassa upotetun Power BI -sisältönä.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-124">The content is available from the Expense Management workspace as embedded Power Bi content.</span></span> <span data-ttu-id="0a1a2-125">Kulun omistaja voi käyttää henkilökohtaisia kuluja itse, kun taas ostoreskontran käyttäjät ja esimiehet voivat käyttää kaikkien käyttäjien kulutietojen hallintasisältöä.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-125">Any expense owner can access personal expenses for themselves, while only Accounts Payable clerks and managers have access to the Admin content to view all user's expense data.</span></span>

## <a name="refreshing-the-power-bi-content"></a><span data-ttu-id="0a1a2-126">Power BI -sisällön päivittäminen</span><span class="sxs-lookup"><span data-stu-id="0a1a2-126">Refreshing the Power BI content</span></span>
<span data-ttu-id="0a1a2-127">Kulujenhallinnan Power BI -sisältö edellyttää, että TrvBiExpenseMeasurement-mitta ja BudgetActivityMeasure päivitetään yksikkösäilöstä.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-127">The Expense management Power BI content requires the TrvBiExpenseMeasurement measure and the BudgetActivityMeasure to be refreshed from the Entity Store.</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="0a1a2-128">Mittarit, jotka sisältyvät Power BI -sisältöön</span><span class="sxs-lookup"><span data-stu-id="0a1a2-128">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="0a1a2-129">Sisältö sisältää joukon raporttisivuja.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-129">The content includes a set of report pages.</span></span> <span data-ttu-id="0a1a2-130">Jokainen sivu koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-130">Each page consists of a set of metrics that are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="0a1a2-131">Seuraavassa taulukossa on yhteenveto Power BI -sisällössä käytettävistä visualisoinneista.</span><span class="sxs-lookup"><span data-stu-id="0a1a2-131">The following table provides an overview of the visualizations in the Power BI content.</span></span>

<span data-ttu-id="0a1a2-132">**Henkilökohtainen kuluanalytiikka**</span><span class="sxs-lookup"><span data-stu-id="0a1a2-132">**Personal expenses analytics**</span></span>

| <span data-ttu-id="0a1a2-133">Raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0a1a2-133">Report page</span></span> | <span data-ttu-id="0a1a2-134">Visualisointi</span><span class="sxs-lookup"><span data-stu-id="0a1a2-134">Visualization</span></span>                             |
|-------------|-------------------------------------------|
| <span data-ttu-id="0a1a2-135">Omat kulut</span><span class="sxs-lookup"><span data-stu-id="0a1a2-135">My expenses</span></span> | <span data-ttu-id="0a1a2-136">Kilometrikorvauksen määrä</span><span class="sxs-lookup"><span data-stu-id="0a1a2-136">Amount of mileage</span></span>                         |
|             | <span data-ttu-id="0a1a2-137">Keskeneräiset kuluraportit</span><span class="sxs-lookup"><span data-stu-id="0a1a2-137">In process expense reports</span></span>                |
|             | <span data-ttu-id="0a1a2-138">Nro</span><span class="sxs-lookup"><span data-stu-id="0a1a2-138">No.</span></span> <span data-ttu-id="0a1a2-139">lähettämättömiä kuluja</span><span class="sxs-lookup"><span data-stu-id="0a1a2-139">of Unsubmitted expenses</span></span>               |
|             | <span data-ttu-id="0a1a2-140">Maksettavat henkilökohtaiset kulut</span><span class="sxs-lookup"><span data-stu-id="0a1a2-140">Personal expenses to be paid</span></span>              |
|             | <span data-ttu-id="0a1a2-141">Lähettämätön määrä</span><span class="sxs-lookup"><span data-stu-id="0a1a2-141">Amount unsubmitted</span></span>                        |
|             | <span data-ttu-id="0a1a2-142">Lähetetty määrä</span><span class="sxs-lookup"><span data-stu-id="0a1a2-142">Amount submitted</span></span>                          |
|             | <span data-ttu-id="0a1a2-143">Hyvistä odottava summa</span><span class="sxs-lookup"><span data-stu-id="0a1a2-143">Amount awaiting reimbursement</span></span>             |
|             | <span data-ttu-id="0a1a2-144">Kuluraportit sekä niiden summat ja tila</span><span class="sxs-lookup"><span data-stu-id="0a1a2-144">Expense reports with amounts and status</span></span>   |
|             | <span data-ttu-id="0a1a2-145">Lähetetyt mutta hyväksymättömät kuluraportit</span><span class="sxs-lookup"><span data-stu-id="0a1a2-145">Submitted but unapproved expense reports</span></span>  |
|             | <span data-ttu-id="0a1a2-146">Kulut kustannustyypin mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-146">Expenses by cost type</span></span>                     |
|             | <span data-ttu-id="0a1a2-147">Kulut kauppiaan mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-147">Expenses by merchant</span></span>                      |
|             | <span data-ttu-id="0a1a2-148">Kulut käsiteltyjen kulujen mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-148">Expenses by processed expenses</span></span>            |
|             | <span data-ttu-id="0a1a2-149">Kulut projektin mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-149">Expenses by project</span></span>                       |
|             | <span data-ttu-id="0a1a2-150">Tapahtuman kokonaissumman kehittyminen</span><span class="sxs-lookup"><span data-stu-id="0a1a2-150">Total transaction amount over time</span></span>        |

<span data-ttu-id="0a1a2-151">**Järjestelmänvalvojan kuluanalytiikka**</span><span class="sxs-lookup"><span data-stu-id="0a1a2-151">**Admin expenses analytics**</span></span>

| <span data-ttu-id="0a1a2-152">Raporttisivu</span><span class="sxs-lookup"><span data-stu-id="0a1a2-152">Report page</span></span>         | <span data-ttu-id="0a1a2-153">Visualisointi</span><span class="sxs-lookup"><span data-stu-id="0a1a2-153">Visualization</span></span>                           |           
|---------------------|-----------------------------------------|
| <span data-ttu-id="0a1a2-154">Kuluyhteenveto</span><span class="sxs-lookup"><span data-stu-id="0a1a2-154">Expense Overview</span></span>    | <span data-ttu-id="0a1a2-155">Kulusummaluonnos</span><span class="sxs-lookup"><span data-stu-id="0a1a2-155">Draft expenses amount</span></span>                   |
|                     | <span data-ttu-id="0a1a2-156">Kululuonnosrivien määrä</span><span class="sxs-lookup"><span data-stu-id="0a1a2-156">Number of draft expense lines</span></span>           |
|                     | <span data-ttu-id="0a1a2-157">Kululuonnosrivit</span><span class="sxs-lookup"><span data-stu-id="0a1a2-157">Draft expense lines</span></span>                     |
|                     | <span data-ttu-id="0a1a2-158">Kuluraportin käytäntörikkeet</span><span class="sxs-lookup"><span data-stu-id="0a1a2-158">Expense report policy violations</span></span>        |
|                     | <span data-ttu-id="0a1a2-159">Avoin summa</span><span class="sxs-lookup"><span data-stu-id="0a1a2-159">Amount outstanding</span></span>                      |
|                     | <span data-ttu-id="0a1a2-160">Lähetetyt mutta hyväksymättömät kulut</span><span class="sxs-lookup"><span data-stu-id="0a1a2-160">Submitted but unapproved expenses</span></span>       |
|                     | <span data-ttu-id="0a1a2-161">Hyväksytyt kulut</span><span class="sxs-lookup"><span data-stu-id="0a1a2-161">Approved expenses</span></span>                       |
|                     | <span data-ttu-id="0a1a2-162">Kulujen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="0a1a2-162">Total expense amount</span></span>                    |
|                     | <span data-ttu-id="0a1a2-163">Kuluraportin yhteenveto</span><span class="sxs-lookup"><span data-stu-id="0a1a2-163">Expense report summaries</span></span>                |
|                     | <span data-ttu-id="0a1a2-164">Kulut kustannustyypin mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-164">Expenses by cost type</span></span>                   |
|                     | <span data-ttu-id="0a1a2-165">Kulut kauppiaan mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-165">Expenses by merchant</span></span>                    |
|                     | <span data-ttu-id="0a1a2-166">Kulut työntekijän mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-166">Expenses by employees</span></span>                   |
|                     | <span data-ttu-id="0a1a2-167">Kulujen vs. projekti</span><span class="sxs-lookup"><span data-stu-id="0a1a2-167">Expenses vs project</span></span>                     |
| <span data-ttu-id="0a1a2-168">Työntekijävertailu</span><span class="sxs-lookup"><span data-stu-id="0a1a2-168">Employee Comparison</span></span> | <span data-ttu-id="0a1a2-169">Kulusummat</span><span class="sxs-lookup"><span data-stu-id="0a1a2-169">Expense amounts</span></span>                         |
|                     | <span data-ttu-id="0a1a2-170">Kulusummien kehittymien työntekijän mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-170">Expense amounts over time by employee</span></span>   |
| <span data-ttu-id="0a1a2-171">Työntekijätilastot</span><span class="sxs-lookup"><span data-stu-id="0a1a2-171">Employee Statistics</span></span> | <span data-ttu-id="0a1a2-172">Kuluraportit kustannustyypin mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-172">Expense reports by cost type</span></span>            |
|                     | <span data-ttu-id="0a1a2-173">Henkilökohtaiset kulut</span><span class="sxs-lookup"><span data-stu-id="0a1a2-173">Personal expenses</span></span>                       |
|                     | <span data-ttu-id="0a1a2-174">Kuluraportit tilastoryhmän mukaan</span><span class="sxs-lookup"><span data-stu-id="0a1a2-174">Expense reports by statistics group</span></span>     |
