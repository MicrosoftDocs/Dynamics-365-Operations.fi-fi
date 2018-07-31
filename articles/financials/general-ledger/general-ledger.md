---
title: Kirjanpidon ja talousraportoinnin aloitussivu
description: "Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 03bab1d03be71c0e23a6ea93f542d6a52a212a1f
ms.openlocfilehash: 9ee3f73cd11b38ed2237ea3fe08db18000e55f07
ms.contentlocale: fi-fi
ms.lasthandoff: 06/25/2018

---

# <a name="general-ledger"></a><span data-ttu-id="546b3-103">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="546b3-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="546b3-104">Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.</span><span class="sxs-lookup"><span data-stu-id="546b3-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="546b3-105">Kirjanpito on debet- ja kredit-tapahtumien luettelo.</span><span class="sxs-lookup"><span data-stu-id="546b3-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="546b3-106">Nämä merkinnät on luokiteltu tilikartan tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="546b3-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="546b3-107">Tilikartan suunnittelu</span><span class="sxs-lookup"><span data-stu-id="546b3-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="546b3-108">Päätilin tyypit</span><span class="sxs-lookup"><span data-stu-id="546b3-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="546b3-109">Voit kohdistaa tai jakaa rahasummia yhdelle tai usealle tilille tai tilin ja dimension yhdistelmälle kohdistussääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="546b3-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="546b3-110">Kohdistuksia on kahta tyyppiä: kiinteitä ja muuttuvia.</span><span class="sxs-lookup"><span data-stu-id="546b3-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="546b3-111">Voit myös selvittää kirjanpitotilien väliset tapahtumat ja uudelleenarvostaa valuuttasummat.</span><span class="sxs-lookup"><span data-stu-id="546b3-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="546b3-112">Tilikauden lopulla sinun on luotava sulkemistapahtumat ja valmisteltava tilit seuraavaa tilikautta varten.</span><span class="sxs-lookup"><span data-stu-id="546b3-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="546b3-113">Konsolidointitoimintojen avulla voit yhdistää useiden tytäryhtiöiden taloudelliset tulokset yhteen konsolidointiorganisaatioon.</span><span class="sxs-lookup"><span data-stu-id="546b3-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="546b3-114">Tytäryhtiöt voivat olla samassa Microsoft Dynamics 365 for Finance and Operations -tietokannassa tai erillisissä tietokannoissa.</span><span class="sxs-lookup"><span data-stu-id="546b3-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="546b3-115">Konsolidoinnin ja eliminoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="546b3-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="546b3-116">Kirjanpitotilin saldot</span><span class="sxs-lookup"><span data-stu-id="546b3-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="546b3-117">Taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="546b3-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="546b3-118">[![Liiketoimintaprosessi](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="546b3-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="546b3-119">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="546b3-119">Sales tax</span></span>
<span data-ttu-id="546b3-120">Jokainen yritys kerää ja maksaa veroja eri veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="546b3-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="546b3-121">Säännöt ja prosentit vaihtelevat maan tai alueen, osavaltion, kunnan tai kaupungin mukaan.</span><span class="sxs-lookup"><span data-stu-id="546b3-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="546b3-122">Lisäksi säännöt on päivitettävä säännöllisesti, kun veroviranomaisten vaatimukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="546b3-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="546b3-123">Arvonlisäverokoodi sisältää perustiedot veroviranomaisille kerättävistä ja maksettavista veroista.</span><span class="sxs-lookup"><span data-stu-id="546b3-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="546b3-124">Kun määrität arvonlisäverokoodit, määrität summat tai prosentit, jotka on kerättävä.</span><span class="sxs-lookup"><span data-stu-id="546b3-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="546b3-125">Voit myös määrittää, eri menetelmät joilla ne summat tai prosentit kohdistetaan tapahtumasummiin.</span><span class="sxs-lookup"><span data-stu-id="546b3-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="546b3-126">Tämän osan ohjeaiheissa käsitellään veronviranomaisten edellyttämien menetelmien ja veroprosenttien mukaisten arvonlisäverokoodien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="546b3-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="546b3-127">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="546b3-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="546b3-128">Arvonlisäveroprosentit Alv-rajan peruste- ja Laskentatapa-kenttien perusteella</span><span class="sxs-lookup"><span data-stu-id="546b3-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="546b3-129">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="546b3-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="546b3-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="546b3-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="546b3-131">Uutta</span><span class="sxs-lookup"><span data-stu-id="546b3-131">What's new</span></span>

<span data-ttu-id="546b3-132">Siirry kohtaan [julkaisutiedot](https://docs.microsoft.com/en-us/business-applications-release-notes/) nähdäksesi mitä uusia toimintoja on julkaistu.</span><span class="sxs-lookup"><span data-stu-id="546b3-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="546b3-133">Videot</span><span class="sxs-lookup"><span data-stu-id="546b3-133">Videos</span></span>

<span data-ttu-id="546b3-134">Tutustu [Microsoft Dynamics 365:n YouTube-kanavan](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) ohjevideoihin.</span><span class="sxs-lookup"><span data-stu-id="546b3-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="546b3-135">Blogit</span><span class="sxs-lookup"><span data-stu-id="546b3-135">Blogs</span></span>

<span data-ttu-id="546b3-136">[Microsoft Dynamics 365 -blogissa](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) on ostoreskontraa ja muita ratkaisuja koskevia mielipiteitä, uutisia ja muita tietoja.</span><span class="sxs-lookup"><span data-stu-id="546b3-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="546b3-137">[Microsoft Dynamics AX -tuoteryhmän blogissa](https://blogs.msdn.microsoft.com/dax/) on useita kirjanpitoa käsitteleviä kirjoituksia.</span><span class="sxs-lookup"><span data-stu-id="546b3-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="546b3-138">Vaikka monet kirjoitukset koskevat kirjanpidon aiempaa versiota, samoja käsitteitä käytetään edelleen ja menettelyt ovat samanlaisia myös nykyisessä versiossa.</span><span class="sxs-lookup"><span data-stu-id="546b3-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="546b3-139">[Microsoft Dynamics Operations -kumppaniyhteisön blogista](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics -kumppanit saavat keskitetysti tietoja MBS Operations -sovelluksen uutuuksista ja suosituista aiheista.</span><span class="sxs-lookup"><span data-stu-id="546b3-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="546b3-140">Yhteisöblogit</span><span class="sxs-lookup"><span data-stu-id="546b3-140">Community blogs</span></span>

- [<span data-ttu-id="546b3-141">Tärkeitä tietoja Dynamics 365 for Finance and Operations -sovelluksesta</span><span class="sxs-lookup"><span data-stu-id="546b3-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)


