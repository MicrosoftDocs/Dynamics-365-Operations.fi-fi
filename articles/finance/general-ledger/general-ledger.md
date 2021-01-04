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
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ade10020e4bab02490c9104c37fe1f234d634e8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442881"
---
# <a name="general-ledger-home-page"></a><span data-ttu-id="d65f3-103">Kirjanpidon kotisivu</span><span class="sxs-lookup"><span data-stu-id="d65f3-103">General ledger home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d65f3-104">Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.</span><span class="sxs-lookup"><span data-stu-id="d65f3-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="d65f3-105">Kirjanpito on debet- ja kredit-tapahtumien luettelo.</span><span class="sxs-lookup"><span data-stu-id="d65f3-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="d65f3-106">Nämä merkinnät on luokiteltu tilikartan tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="d65f3-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="d65f3-107">Tilikartan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="d65f3-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="d65f3-108">Päätilin tyypit</span><span class="sxs-lookup"><span data-stu-id="d65f3-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="d65f3-109">Voit kohdistaa tai jakaa rahasummia yhdelle tai usealle tilille tai tilin ja dimension yhdistelmälle kohdistussääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d65f3-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="d65f3-110">Kohdistuksia on kahta tyyppiä: kiinteitä ja muuttuvia.</span><span class="sxs-lookup"><span data-stu-id="d65f3-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="d65f3-111">Voit myös selvittää kirjanpitotilien väliset tapahtumat ja uudelleenarvostaa valuuttasummat.</span><span class="sxs-lookup"><span data-stu-id="d65f3-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="d65f3-112">Tilikauden lopulla sinun on luotava sulkemistapahtumat ja valmisteltava tilit seuraavaa tilikautta varten.</span><span class="sxs-lookup"><span data-stu-id="d65f3-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="d65f3-113">Konsolidointitoimintojen avulla voit yhdistää useiden tytäryhtiöiden taloudelliset tulokset yhteen konsolidointiorganisaatioon.</span><span class="sxs-lookup"><span data-stu-id="d65f3-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="d65f3-114">Tytäryhtiöt voivat olla samassa tietokannassa tai erillisissä tietokannoissa.</span><span class="sxs-lookup"><span data-stu-id="d65f3-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="d65f3-115">Konsolidoinnin ja eliminoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d65f3-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="d65f3-116">Kirjanpitotilin saldot</span><span class="sxs-lookup"><span data-stu-id="d65f3-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="d65f3-117">Taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="d65f3-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="d65f3-118">[![Liiketoimintaprosessi](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="d65f3-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="d65f3-119">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="d65f3-119">Sales tax</span></span>
<span data-ttu-id="d65f3-120">Jokainen yritys kerää ja maksaa veroja eri veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="d65f3-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="d65f3-121">Säännöt ja prosentit vaihtelevat maan tai alueen, osavaltion, kunnan tai kaupungin mukaan.</span><span class="sxs-lookup"><span data-stu-id="d65f3-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="d65f3-122">Lisäksi säännöt on päivitettävä säännöllisesti, kun veroviranomaisten vaatimukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="d65f3-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="d65f3-123">Arvonlisäverokoodi sisältää perustiedot veroviranomaisille kerättävistä ja maksettavista veroista.</span><span class="sxs-lookup"><span data-stu-id="d65f3-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="d65f3-124">Kun määrität arvonlisäverokoodit, määrität summat tai prosentit, jotka on kerättävä.</span><span class="sxs-lookup"><span data-stu-id="d65f3-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="d65f3-125">Voit myös määrittää, eri menetelmät joilla ne summat tai prosentit kohdistetaan tapahtumasummiin.</span><span class="sxs-lookup"><span data-stu-id="d65f3-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="d65f3-126">Tämän osan ohjeaiheissa käsitellään veronviranomaisten edellyttämien menetelmien ja veroprosenttien mukaisten arvonlisäverokoodien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="d65f3-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="d65f3-127">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d65f3-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="d65f3-128">Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella</span><span class="sxs-lookup"><span data-stu-id="d65f3-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="d65f3-129">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="d65f3-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="d65f3-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d65f3-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="d65f3-131">Uudet ja kehitteillä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="d65f3-131">What's new and in development</span></span>

<span data-ttu-id="d65f3-132">Siirry [Microsoft Dynamics 365:n julkaisusuunnitelmiin](https://go.microsoft.com/fwlink/?linkid=2010158), kun haluat nähdä, millaisia uusia toimintoja on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="d65f3-132">Go to the [Microsoft Dynamics 365 release plans](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="financial-reporting"></a><span data-ttu-id="d65f3-133">Taloushallinnan raportointi</span><span class="sxs-lookup"><span data-stu-id="d65f3-133">Financial reporting</span></span>
<span data-ttu-id="d65f3-134">Lisätietoja taloudellisista raporteista on kohdassa [Financial reportingin yhteenveto](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) -aiheessa.</span><span class="sxs-lookup"><span data-stu-id="d65f3-134">Go to the [Financial reporting overview](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) topic for information about financial reports.</span></span>

#### <a name="blogs"></a><span data-ttu-id="d65f3-135">Blogit</span><span class="sxs-lookup"><span data-stu-id="d65f3-135">Blogs</span></span>

<span data-ttu-id="d65f3-136">[Microsoft Dynamics 365 -blogissa](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ja [Microsoft Dynamics 365 Finance and Operations -sovelluksen taloushallinnon blogissa](https://community.dynamics.com/365/financeandoperations/b/financials) on paljon ajatuksia, uutisia ja muita tietoja.</span><span class="sxs-lookup"><span data-stu-id="d65f3-136">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="d65f3-137">[Microsoft Dynamics Operations -kumppaniyhteisön blogista](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics -kumppanit saavat keskitetysti tietoja Dynamics 365:n uutuuksista ja suosituista aiheista.</span><span class="sxs-lookup"><span data-stu-id="d65f3-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in Dynamics 365.</span></span>

### <a name="videos"></a><span data-ttu-id="d65f3-138">Videot</span><span class="sxs-lookup"><span data-stu-id="d65f3-138">Videos</span></span>

<span data-ttu-id="d65f3-139">Tutustu [Microsoft Dynamics 365 YouTube -kanavan](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) ohjevideoihin.</span><span class="sxs-lookup"><span data-stu-id="d65f3-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="d65f3-140">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="d65f3-140">Community blogs</span></span>

- [<span data-ttu-id="d65f3-141">Tärkeitä tietoja Dynamics 365 for Finance and Operationsin kirjanpidosta</span><span class="sxs-lookup"><span data-stu-id="d65f3-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

