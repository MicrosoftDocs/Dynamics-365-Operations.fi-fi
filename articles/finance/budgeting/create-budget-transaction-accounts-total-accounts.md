---
title: Budjetin luominen tapahtumatileistä ja summatileistä
description: Tässä artikkelissa on summatileihin perustuvien budjettien luontiprosessin yleiskatsaus. Artikkelissa kerrotaan myös, miten summatilien budjetin hallinta otetaan käyttöön, jos budjetin hallinta vaaditaan.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f60963bee790737c85161dff03278df0572e3abc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177570"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="5fab3-104">Budjetin luominen tapahtumatileistä ja summatileistä</span><span class="sxs-lookup"><span data-stu-id="5fab3-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fab3-105">Tässä artikkelissa on summatileihin perustuvien budjettien luontiprosessin yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="5fab3-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="5fab3-106">Artikkelissa kerrotaan myös, miten summatilien budjetin hallinta otetaan käyttöön, jos budjetin hallinta vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="5fab3-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="5fab3-107">Sekä budjettisuunnitelman että budjettirekisterimerkinnän asiakirjat mahdollistavat budjetoinnin päätileillä, joiden päätilin tyyppi on **Yhteensä**.</span><span class="sxs-lookup"><span data-stu-id="5fab3-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="5fab3-108">Toteutuneet summat voidaan kirjata vain tapahtumien päätileille.</span><span class="sxs-lookup"><span data-stu-id="5fab3-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="5fab3-109">Määritä kausittaiselle **Muodosta budjettisuunnitelma kirjanpidosta** -prosessille **Lähde**-välilehdessä ehdoksi päätilin **Yhteensä**-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="5fab3-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="5fab3-110">Tässä tapauksessa kukin pääsummatili sisällytetään kohdebudjettisuunnitelmaan. Summa on sama kuin valittujen päätilien alueen kokonaissumma.</span><span class="sxs-lookup"><span data-stu-id="5fab3-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="5fab3-111">Voit aktivoida **Yhteensä**-tyypin päätilien budjetin hallinnan.</span><span class="sxs-lookup"><span data-stu-id="5fab3-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="5fab3-112">Tätä toimintoa tuetaan kaikkien budjettiryhmien käytössä.</span><span class="sxs-lookup"><span data-stu-id="5fab3-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="5fab3-113">Jokaiselle pääsummatilille budjettiryhmän osalta hallittava budjetti pitää luoda \*\*Budjetin hallinnan konfiguraatio \*\*-sivulla.</span><span class="sxs-lookup"><span data-stu-id="5fab3-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="5fab3-114">Määrittämiesi ehtojen on sisällettävä pääsummatili ja tilialue.</span><span class="sxs-lookup"><span data-stu-id="5fab3-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="5fab3-115">Voit nopeuttaa budjettiryhmien luontiprosessia käyttämällä budjetin hallintaryhmien tietoyksikköä.</span><span class="sxs-lookup"><span data-stu-id="5fab3-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="5fab3-116">Jos budjetointia käytetään raportoinnissa, esimerkiksi tilinpäätöksessä, summatilin budjettisumma sisältää seuraavat summat:</span><span class="sxs-lookup"><span data-stu-id="5fab3-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="5fab3-117">kullekin tapahtumakirjanpitotilille summatilin aikavälinä luodut budjetit</span><span class="sxs-lookup"><span data-stu-id="5fab3-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="5fab3-118">suoraan summatilille syötetty budjettisumma.</span><span class="sxs-lookup"><span data-stu-id="5fab3-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="5fab3-119">Näin voidaan luoda summatilin aikavälille erilliset budjetit tärkeimpiä tapahtumatilejä varten ja lisätä sitten käytettävissä oleva budjettisumma summatilille.</span><span class="sxs-lookup"><span data-stu-id="5fab3-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>


