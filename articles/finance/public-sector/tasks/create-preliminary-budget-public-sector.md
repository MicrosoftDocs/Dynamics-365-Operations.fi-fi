---
title: Alustavan budjetin luominen julkiselle sektorille
description: Voit luoda tietyn budjettimallin ja dimensioarvojen alustavat budjettitapahtumat.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c7937402f63db23c2b42d61c584c17dce5e1bf10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811212"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="b236f-103">Alustavan budjetin luominen julkiselle sektorille</span><span class="sxs-lookup"><span data-stu-id="b236f-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b236f-104">Voit luoda tietyn budjettimallin ja dimensioarvojen alustavat budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b236f-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="b236f-105">Kun todellinen budjetti on hyväksytty, voit luoda alkuperäiset budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b236f-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="b236f-106">Tämä menettely luotiin käyttämällä PSUS-yrityksen demotietoja julkisen sektorin osiossa.</span><span class="sxs-lookup"><span data-stu-id="b236f-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="b236f-107">Valitse Budjetointi > Budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="b236f-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="b236f-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b236f-108">Click New.</span></span>
3. <span data-ttu-id="b236f-109">Avaa haku napsauttamalla Budjettimalli-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b236f-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b236f-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b236f-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b236f-111">Avaa haku napsauttamalla Budjettikoodi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b236f-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b236f-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b236f-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b236f-113">Avaa haku napsauttamalla Syykoodi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b236f-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b236f-114">Valitse tietue luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b236f-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="b236f-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b236f-115">Click Save.</span></span>
10. <span data-ttu-id="b236f-116">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="b236f-116">Click Add line.</span></span>
    * <span data-ttu-id="b236f-117">Valinnainen: Jos haluat muuttaa otsikon päivämäärää, anna uusi päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b236f-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="b236f-118">Tämä päivämäärä määrittää tilikauden, johon budjetti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="b236f-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="b236f-119">Jos haluat täyttää tehtäväopastuksen muita kenttiä, valitse sivun yläosassa lukituksen vapautus.</span><span class="sxs-lookup"><span data-stu-id="b236f-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="b236f-120">Avaa haku napsauttamalla Tilirakenne-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b236f-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b236f-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b236f-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="b236f-122">Määritä Dimension arvot -kentässä arvot.</span><span class="sxs-lookup"><span data-stu-id="b236f-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="b236f-123">Lisää Summa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b236f-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="b236f-124">Voit antaa myös summan tyypin.</span><span class="sxs-lookup"><span data-stu-id="b236f-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="b236f-125">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b236f-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="b236f-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b236f-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b236f-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b236f-127">Click Save.</span></span>
18. <span data-ttu-id="b236f-128">Valitse Päivitä budjettisaldot.</span><span class="sxs-lookup"><span data-stu-id="b236f-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="b236f-129">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="b236f-129">Click Update.</span></span>
    * <span data-ttu-id="b236f-130">Voit tarkastella päivityksen tuloksia valitsemalla sinisessä palkissa Sanoman tiedot.</span><span class="sxs-lookup"><span data-stu-id="b236f-130">To see the results of the update, click Message details on the blue bar.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]