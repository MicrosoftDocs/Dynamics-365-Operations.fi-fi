---
title: Alustavan budjetin luominen julkiselle sektorille
description: Voit luoda tietyn budjettimallin ja dimensioarvojen alustavat budjettitapahtumat.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05e8059f44000fd305ed2c2555511da29b130af9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442860"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="0dd44-103">Alustavan budjetin luominen julkiselle sektorille</span><span class="sxs-lookup"><span data-stu-id="0dd44-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0dd44-104">Voit luoda tietyn budjettimallin ja dimensioarvojen alustavat budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="0dd44-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="0dd44-105">Kun todellinen budjetti on hyväksytty, voit luoda alkuperäiset budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="0dd44-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="0dd44-106">Tämä menettely luotiin käyttämällä PSUS-yrityksen demotietoja julkisen sektorin osiossa.</span><span class="sxs-lookup"><span data-stu-id="0dd44-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="0dd44-107">Valitse Budjetointi > Budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="0dd44-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="0dd44-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0dd44-108">Click New.</span></span>
3. <span data-ttu-id="0dd44-109">Avaa haku napsauttamalla Budjettimalli-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="0dd44-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0dd44-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0dd44-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0dd44-111">Avaa haku napsauttamalla Budjettikoodi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="0dd44-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0dd44-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0dd44-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0dd44-113">Avaa haku napsauttamalla Syykoodi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="0dd44-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0dd44-114">Valitse tietue luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0dd44-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="0dd44-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0dd44-115">Click Save.</span></span>
10. <span data-ttu-id="0dd44-116">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="0dd44-116">Click Add line.</span></span>
    * <span data-ttu-id="0dd44-117">Valinnainen: Jos haluat muuttaa otsikon päivämäärää, anna uusi päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="0dd44-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="0dd44-118">Tämä päivämäärä määrittää tilikauden, johon budjetti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="0dd44-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="0dd44-119">Jos haluat täyttää tehtäväopastuksen muita kenttiä, valitse sivun yläosassa lukituksen vapautus.</span><span class="sxs-lookup"><span data-stu-id="0dd44-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="0dd44-120">Avaa haku napsauttamalla Tilirakenne-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="0dd44-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="0dd44-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0dd44-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="0dd44-122">Määritä Dimension arvot -kentässä arvot.</span><span class="sxs-lookup"><span data-stu-id="0dd44-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="0dd44-123">Lisää Summa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0dd44-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="0dd44-124">Voit antaa myös summan tyypin.</span><span class="sxs-lookup"><span data-stu-id="0dd44-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="0dd44-125">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0dd44-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="0dd44-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0dd44-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="0dd44-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0dd44-127">Click Save.</span></span>
18. <span data-ttu-id="0dd44-128">Valitse Päivitä budjettisaldot.</span><span class="sxs-lookup"><span data-stu-id="0dd44-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="0dd44-129">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="0dd44-129">Click Update.</span></span>
    * <span data-ttu-id="0dd44-130">Voit tarkastella päivityksen tuloksia valitsemalla sinisessä palkissa Sanoman tiedot.</span><span class="sxs-lookup"><span data-stu-id="0dd44-130">To see the results of the update, click Message details on the blue bar.</span></span>  

