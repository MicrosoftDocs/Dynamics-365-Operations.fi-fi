--- 
title: Talleta asiakkaan maksuja
description: Talleta asiakkaan maksut.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="ae7d6-103">Talleta asiakkaan maksuja</span><span class="sxs-lookup"><span data-stu-id="ae7d6-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae7d6-104">Talleta asiakkaan maksut.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-104">Deposit customer payments.</span></span> <span data-ttu-id="ae7d6-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ae7d6-106">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ae7d6-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-107">Click New.</span></span>
3. <span data-ttu-id="ae7d6-108">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ae7d6-109">Valitse maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="ae7d6-110">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-110">Click Lines.</span></span>
6. <span data-ttu-id="ae7d6-111">Valitse Tili-kentässä asiakas, jolle maksu kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="ae7d6-112">Syötä Kredit-kenttään maksun summa.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="ae7d6-113">Voit jättää summan tyhjäksi, jolloin järjestelmä laskee sen valitsemalla maksetut laskut.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="ae7d6-114">Syötä Maksuviite-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="ae7d6-115">Maksuviite voi olla syöttämäsi maksun sekkinumero.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="ae7d6-116">Maksuviite vaaditaan, jotta maksu voidaan sisällyttää talletuskuittiin.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="ae7d6-117">Valitse Käytä talletuskuittia -kohta.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="ae7d6-118">Jos maksu halutaan sisällyttää talletukseen, muuta tämän asetuksen arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="ae7d6-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-119">Click New.</span></span>
11. <span data-ttu-id="ae7d6-120">Valitse Tili-kentässä asiakas seuraa maksua varten.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="ae7d6-121">Syötä Kredit-kenttään maksun summa.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="ae7d6-122">Syötä Maksuviite-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="ae7d6-123">Valitse Käytä talletuskuittia -kohta.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="ae7d6-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-124">Click Post.</span></span>
    * <span data-ttu-id="ae7d6-125">Maksut on kirjattava, ennen kuin talletuskuitti luodaan.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="ae7d6-126">Näin varmistetaan, että maksut eivät muutu talletuskuitin luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="ae7d6-127">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-127">Click Functions.</span></span>
17. <span data-ttu-id="ae7d6-128">Tulosta talletuskuitti.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="ae7d6-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-129">Click OK.</span></span>
    * <span data-ttu-id="ae7d6-130">Ensimmäisellä sivulla luodaan talletuskuitti.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="ae7d6-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-131">Click OK.</span></span>
    * <span data-ttu-id="ae7d6-132">Toisessa vaiheessa talletuskuitti tulostetaan. Tämä vaihe ei kuitenkaan ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


