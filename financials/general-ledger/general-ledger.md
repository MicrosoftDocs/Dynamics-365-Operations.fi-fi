---
title: Kirjanpidon ja talousraportoinnin aloitussivu
description: "Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita. Kirjanpito on debet- ja kredit-tapahtumien luettelo. Nämä merkinnät on luokiteltu tilikartan tilien avulla."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="a1236-105">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="a1236-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a1236-106">Kirjanpidon avulla voit määrittää ja hallinnoida yrityksen kirjanpitotietueita.</span><span class="sxs-lookup"><span data-stu-id="a1236-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="a1236-107">Kirjanpito on debet- ja kredit-tapahtumien luettelo.</span><span class="sxs-lookup"><span data-stu-id="a1236-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="a1236-108">Nämä merkinnät on luokiteltu tilikartan tilien avulla.</span><span class="sxs-lookup"><span data-stu-id="a1236-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="a1236-109">Voit kohdistaa tai jakaa rahasummia yhdelle tai usealle tilille tai tilin ja dimension yhdistelmälle kohdistussääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a1236-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="a1236-110">Kohdistuksia on kahta tyyppiä: kiinteitä ja muuttuvia.</span><span class="sxs-lookup"><span data-stu-id="a1236-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="a1236-111">Voit myös selvittää kirjanpitotilien väliset tapahtumat ja uudelleenarvostaa valuuttasummat.</span><span class="sxs-lookup"><span data-stu-id="a1236-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="a1236-112">Tilikauden lopulla sinun on luotava sulkemistapahtumat ja valmisteltava tilit seuraavaa tilikautta varten.</span><span class="sxs-lookup"><span data-stu-id="a1236-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="a1236-113">Konsolidointitoimintojen avulla voit yhdistää useiden tytäryhtiöiden taloudelliset tulokset yhteen konsolidointiorganisaatioon.</span><span class="sxs-lookup"><span data-stu-id="a1236-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="a1236-114">Tytäryhtiöt voivat olla samassa Microsoft Dynamics 365 for Finance and Operations -tietokannassa tai erillisissä tietokannoissa.</span><span class="sxs-lookup"><span data-stu-id="a1236-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="a1236-115">Arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="a1236-115">Sales tax</span></span>
<span data-ttu-id="a1236-116">Jokainen yritys kerää ja maksaa veroja eri veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="a1236-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="a1236-117">Säännöt ja prosentit vaihtelevat maan tai alueen, osavaltion, kunnan tai kaupungin mukaan.</span><span class="sxs-lookup"><span data-stu-id="a1236-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="a1236-118">Lisäksi säännöt on päivitettävä säännöllisesti, kun veroviranomaisten vaatimukset muuttuvat.</span><span class="sxs-lookup"><span data-stu-id="a1236-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="a1236-119">Arvonlisäverokoodi sisältää perustiedot veroviranomaisille kerättävistä ja maksettavista veroista.</span><span class="sxs-lookup"><span data-stu-id="a1236-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="a1236-120">Kun määrität arvonlisäverokoodit, määrität summat tai prosentit, jotka on kerättävä.</span><span class="sxs-lookup"><span data-stu-id="a1236-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="a1236-121">Voit myös määrittää, eri menetelmät joilla ne summat tai prosentit kohdistetaan tapahtumasummiin.</span><span class="sxs-lookup"><span data-stu-id="a1236-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="a1236-122">Tämän osan ohjeaiheissa käsitellään veronviranomaisten edellyttämien menetelmien ja veroprosenttien mukaisten arvonlisäverokoodien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="a1236-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







