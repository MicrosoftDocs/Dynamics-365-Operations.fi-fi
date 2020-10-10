---
title: Kirjanpidon ja talousraportoinnin yleiskatsaus
description: Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.
author: ShylaThompson
manager: AnnBe
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53d37d0a02b6771957e2516ef7e3b0bb277014a6
ms.sourcegitcommit: 71a7fb9e7133d872790ec25def5453bbbb17c627
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888129"
---
# <a name="general-ledger-home-page"></a><span data-ttu-id="1cbbe-103">Kirjanpidon kotisivu</span><span class="sxs-lookup"><span data-stu-id="1cbbe-103">General ledger home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cbbe-104">Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="1cbbe-105">Kirjanpito on debet- ja kredit-tapahtumien luettelo.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="1cbbe-106">Nämä merkinnät on luokiteltu tilikartan tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="1cbbe-107">Tilikartan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="1cbbe-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="1cbbe-108">Päätilin tyypit</span><span class="sxs-lookup"><span data-stu-id="1cbbe-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="1cbbe-109">Voit kohdistaa tai jakaa rahasummia yhdelle tai usealle tilille tai tilin ja dimension yhdistelmälle kohdistussääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="1cbbe-110">Kohdistuksia on kahta tyyppiä: kiinteitä ja muuttuvia.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="1cbbe-111">Voit myös selvittää kirjanpitotilien väliset tapahtumat ja uudelleenarvostaa valuuttasummat.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="1cbbe-112">Tilikauden lopulla sinun on luotava sulkemistapahtumat ja valmisteltava tilit seuraavaa tilikautta varten.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="1cbbe-113">Konsolidointitoimintojen avulla voit yhdistää useiden tytäryhtiöiden taloudelliset tulokset yhteen konsolidointiorganisaatioon.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="1cbbe-114">Tytäryhtiöt voivat olla samassa tietokannassa tai erillisissä tietokannoissa.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="1cbbe-115">Konsolidoinnin ja eliminoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1cbbe-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="1cbbe-116">Kirjanpitotilin saldot</span><span class="sxs-lookup"><span data-stu-id="1cbbe-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="1cbbe-117">Taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="1cbbe-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="1cbbe-118">[![Liiketoimintaprosessi](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="1cbbe-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="1cbbe-119">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="1cbbe-119">Sales tax</span></span>
<span data-ttu-id="1cbbe-120">Jokainen yritys kerää ja maksaa veroja eri veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="1cbbe-121">Säännöt ja prosentit vaihtelevat maan tai alueen, osavaltion, kunnan tai kaupungin mukaan.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="1cbbe-122">Lisäksi säännöt on päivitettävä säännöllisesti, kun veroviranomaisten vaatimukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="1cbbe-123">Arvonlisäverokoodi sisältää perustiedot veroviranomaisille kerättävistä ja maksettavista veroista.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="1cbbe-124">Kun määrität arvonlisäverokoodit, määrität summat tai prosentit, jotka on kerättävä.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="1cbbe-125">Voit myös määrittää, eri menetelmät joilla ne summat tai prosentit kohdistetaan tapahtumasummiin.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="1cbbe-126">Tämän osan ohjeaiheissa käsitellään veronviranomaisten edellyttämien menetelmien ja veroprosenttien mukaisten arvonlisäverokoodien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="1cbbe-127">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1cbbe-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="1cbbe-128">Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella</span><span class="sxs-lookup"><span data-stu-id="1cbbe-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="1cbbe-129">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="1cbbe-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="1cbbe-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1cbbe-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="1cbbe-131">Uudet ja kehitteillä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="1cbbe-131">What's new and in development</span></span>

<span data-ttu-id="1cbbe-132">Siirry [Microsoft Dynamics 365:n julkaisusuunnitelmiin](https://go.microsoft.com/fwlink/?linkid=2010158), kun haluat nähdä, millaisia uusia toimintoja on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-132">Go to the [Microsoft Dynamics 365 release plans](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="financial-reporting"></a><span data-ttu-id="1cbbe-133">Taloushallinnan raportointi</span><span class="sxs-lookup"><span data-stu-id="1cbbe-133">Financial reporting</span></span>
<span data-ttu-id="1cbbe-134">Lisätietoja taloudellisista raporteista on kohdassa [Financial reportingin yhteenveto](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) -aiheessa.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-134">Go to the [Financial reporting overview](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) topic for information about financial reports.</span></span>

#### <a name="blogs"></a><span data-ttu-id="1cbbe-135">Blogit</span><span class="sxs-lookup"><span data-stu-id="1cbbe-135">Blogs</span></span>

<span data-ttu-id="1cbbe-136">[Microsoft Dynamics 365 -blogissa](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ja [Microsoft Dynamics 365 Finance and Operations -sovelluksen taloushallinnon blogissa](https://community.dynamics.com/365/financeandoperations/b/financials) on paljon ajatuksia, uutisia ja muita tietoja.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-136">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="1cbbe-137">[Microsoft Dynamics Operations -kumppaniyhteisön blogista](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics -kumppanit saavat keskitetysti tietoja Dynamics 365:n uutuuksista ja suosituista aiheista.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in Dynamics 365.</span></span>

### <a name="videos"></a><span data-ttu-id="1cbbe-138">Videot</span><span class="sxs-lookup"><span data-stu-id="1cbbe-138">Videos</span></span>

<span data-ttu-id="1cbbe-139">Tutustu [Microsoft Dynamics 365 YouTube -kanavan](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) ohjevideoihin.</span><span class="sxs-lookup"><span data-stu-id="1cbbe-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="1cbbe-140">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="1cbbe-140">Community blogs</span></span>

- [<span data-ttu-id="1cbbe-141">Tärkeitä tietoja Dynamics 365 for Finance and Operationsin kirjanpidosta</span><span class="sxs-lookup"><span data-stu-id="1cbbe-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

