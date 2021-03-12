---
title: Alkuperäisen budjetin luominen ja alustavien budjettimerkintöjen palauttaminen julkiselle sektorille
description: Tässä ohjeaiheessa on tietoja siitä, miten alkuperäinen budjettimerkintä luodaan ja palautetaan käyttäen budjettimallia ja dimensioarvoja, joissa on alustavat budjettisummat.
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
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 134e2ca851d72965198026107817c66a808ac705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987951"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="07c35-103">Alkuperäisen budjetin luominen ja alustavien budjettimerkintöjen palauttaminen julkiselle sektorille</span><span class="sxs-lookup"><span data-stu-id="07c35-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07c35-104">Kun luot alkuperäisen budjettitapahtuman ja käytät budjettimallia ja dimension arvoja, jotka sisältävät alustavat budjettisummat, alustavat budjettisummat voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="07c35-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="07c35-105">Tämä menettely luotiin käyttämällä PSUS-yrityksen demotietoja julkisen sektorin osiossa.</span><span class="sxs-lookup"><span data-stu-id="07c35-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="07c35-106">Valitse Budjetointi > Budjettitapahtumat.</span><span class="sxs-lookup"><span data-stu-id="07c35-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="07c35-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="07c35-107">Click New.</span></span>
3. <span data-ttu-id="07c35-108">Avaa haku napsauttamalla Budjettimalli-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="07c35-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="07c35-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="07c35-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="07c35-110">Avaa haku napsauttamalla Budjettikoodi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="07c35-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="07c35-111">Valitse luettelossa Alkuperäinen budjetti.</span><span class="sxs-lookup"><span data-stu-id="07c35-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="07c35-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="07c35-112">Click Save.</span></span>
8. <span data-ttu-id="07c35-113">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="07c35-113">Click Add line.</span></span>
9. <span data-ttu-id="07c35-114">Valinnainen: Jos haluat muuttaa otsikon päivämäärää, anna uusi päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="07c35-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="07c35-115">Tämä päivämäärä määrittää tilikauden, johon budjetti kirjataan.</span><span class="sxs-lookup"><span data-stu-id="07c35-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="07c35-116">Avaa haku napsauttamalla Tilirakenne-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="07c35-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="07c35-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="07c35-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="07c35-118">Määritä Dimension arvot -kentässä arvot.</span><span class="sxs-lookup"><span data-stu-id="07c35-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="07c35-119">Lisää Summa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="07c35-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="07c35-120">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="07c35-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="07c35-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="07c35-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="07c35-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="07c35-122">Click Save.</span></span>
17. <span data-ttu-id="07c35-123">Valitse Päivitä budjettisaldot.</span><span class="sxs-lookup"><span data-stu-id="07c35-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="07c35-124">Valinnainen: Voit valita alustavan budjetin palautusvaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="07c35-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="07c35-125">Huomaa, että voit palauttaa kaikki alustavat budjettitapahtumat vai vain ne alustavat budjettitapahtumat, joilla on määrittämäsi budjettikoodi.</span><span class="sxs-lookup"><span data-stu-id="07c35-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="07c35-126">Jos haluat tehdä valinnaisia valintoja, napsauta sivun yläosassa avauskuvaketta.</span><span class="sxs-lookup"><span data-stu-id="07c35-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="07c35-127">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="07c35-127">Click Update.</span></span>

