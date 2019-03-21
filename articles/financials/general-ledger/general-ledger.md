---
title: Kirjanpidon ja talousraportoinnin aloitussivu
description: Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b6683107f4b2dbe36af78749612ce950ea19582
ms.sourcegitcommit: afab5269613d1d1dfd79cd39370b747dee13d3fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2019
ms.locfileid: "403234"
---
# <a name="general-ledger"></a><span data-ttu-id="2a41f-103">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="2a41f-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a41f-104">Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.</span><span class="sxs-lookup"><span data-stu-id="2a41f-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="2a41f-105">Kirjanpito on debet- ja kredit-tapahtumien luettelo.</span><span class="sxs-lookup"><span data-stu-id="2a41f-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="2a41f-106">Nämä merkinnät on luokiteltu tilikartan tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="2a41f-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="2a41f-107">Tilikartan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="2a41f-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="2a41f-108">Päätilin tyypit</span><span class="sxs-lookup"><span data-stu-id="2a41f-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="2a41f-109">Voit kohdistaa tai jakaa rahasummia yhdelle tai usealle tilille tai tilin ja dimension yhdistelmälle kohdistussääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2a41f-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="2a41f-110">Kohdistuksia on kahta tyyppiä: kiinteitä ja muuttuvia.</span><span class="sxs-lookup"><span data-stu-id="2a41f-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="2a41f-111">Voit myös selvittää kirjanpitotilien väliset tapahtumat ja uudelleenarvostaa valuuttasummat.</span><span class="sxs-lookup"><span data-stu-id="2a41f-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="2a41f-112">Tilikauden lopulla sinun on luotava sulkemistapahtumat ja valmisteltava tilit seuraavaa tilikautta varten.</span><span class="sxs-lookup"><span data-stu-id="2a41f-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="2a41f-113">Konsolidointitoimintojen avulla voit yhdistää useiden tytäryhtiöiden taloudelliset tulokset yhteen konsolidointiorganisaatioon.</span><span class="sxs-lookup"><span data-stu-id="2a41f-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="2a41f-114">Tytäryhtiöt voivat olla samassa Microsoft Dynamics 365 for Finance and Operations -tietokannassa tai erillisissä tietokannoissa.</span><span class="sxs-lookup"><span data-stu-id="2a41f-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="2a41f-115">Konsolidoinnin ja eliminoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2a41f-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="2a41f-116">Kirjanpitotilin saldot</span><span class="sxs-lookup"><span data-stu-id="2a41f-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="2a41f-117">Taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="2a41f-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="2a41f-118">[![Liiketoimintaprosessi](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="2a41f-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="2a41f-119">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="2a41f-119">Sales tax</span></span>
<span data-ttu-id="2a41f-120">Jokainen yritys kerää ja maksaa veroja eri veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="2a41f-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="2a41f-121">Säännöt ja prosentit vaihtelevat maan tai alueen, osavaltion, kunnan tai kaupungin mukaan.</span><span class="sxs-lookup"><span data-stu-id="2a41f-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="2a41f-122">Lisäksi säännöt on päivitettävä säännöllisesti, kun veroviranomaisten vaatimukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="2a41f-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="2a41f-123">Arvonlisäverokoodi sisältää perustiedot veroviranomaisille kerättävistä ja maksettavista veroista.</span><span class="sxs-lookup"><span data-stu-id="2a41f-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="2a41f-124">Kun määrität arvonlisäverokoodit, määrität summat tai prosentit, jotka on kerättävä.</span><span class="sxs-lookup"><span data-stu-id="2a41f-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="2a41f-125">Voit myös määrittää, eri menetelmät joilla ne summat tai prosentit kohdistetaan tapahtumasummiin.</span><span class="sxs-lookup"><span data-stu-id="2a41f-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="2a41f-126">Tämän osan ohjeaiheissa käsitellään veronviranomaisten edellyttämien menetelmien ja veroprosenttien mukaisten arvonlisäverokoodien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="2a41f-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="2a41f-127">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2a41f-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="2a41f-128">Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella</span><span class="sxs-lookup"><span data-stu-id="2a41f-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="2a41f-129">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="2a41f-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="2a41f-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2a41f-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="2a41f-131">Uudet ja kehitteillä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="2a41f-131">What's new and in development</span></span>

<span data-ttu-id="2a41f-132">Tutustu suunniteltuihin uusiin ominaisuuksiin siirtymällä [Microsoft Dynamics 365:n julkaisutietoihin](https://go.microsoft.com/fwlink/?linkid=2010158).</span><span class="sxs-lookup"><span data-stu-id="2a41f-132">Go to the [Microsoft Dynamics 365 Release Notes](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="2a41f-133">Blogit</span><span class="sxs-lookup"><span data-stu-id="2a41f-133">Blogs</span></span>

<span data-ttu-id="2a41f-134">Mielipiteitä, uutisia ja muita tietoja on [Microsoft Dynamics 365:n blogissa](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ja [Microsoft Dynamics 365 Finance and Operationsin taloushallinnon blogissa](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="2a41f-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="2a41f-135">[Microsoft Dynamics Operations -kumppaniyhteisön blogista](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics -kumppanit saavat keskitetysti tietoja MBS Operations -sovelluksen uutuuksista ja suosituista aiheista.</span><span class="sxs-lookup"><span data-stu-id="2a41f-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="2a41f-136">Videot</span><span class="sxs-lookup"><span data-stu-id="2a41f-136">Videos</span></span>

<span data-ttu-id="2a41f-137">Tutustu [Microsoft Dynamics 365 YouTube -kanavan](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) ohjevideoihin.</span><span class="sxs-lookup"><span data-stu-id="2a41f-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="2a41f-138">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="2a41f-138">Community blogs</span></span>

- [<span data-ttu-id="2a41f-139">Tärkeitä tietoja Dynamics 365 for Finance and Operationsin kirjanpidosta</span><span class="sxs-lookup"><span data-stu-id="2a41f-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

