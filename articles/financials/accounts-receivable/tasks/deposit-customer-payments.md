---
title: Talleta asiakkaan maksuja
description: Talleta asiakkaan maksut.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867771"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="72cd7-103">Talleta asiakkaan maksuja</span><span class="sxs-lookup"><span data-stu-id="72cd7-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72cd7-104">Talleta asiakkaan maksut.</span><span class="sxs-lookup"><span data-stu-id="72cd7-104">Deposit customer payments.</span></span> <span data-ttu-id="72cd7-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="72cd7-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="72cd7-106">Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Maksut > Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="72cd7-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-107">Select **New**.</span></span>
3. <span data-ttu-id="72cd7-108">Valitse avattavasta **Nimi**-kentästä **CustPay**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="72cd7-109">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-109">Select **Lines**.</span></span>
5. <span data-ttu-id="72cd7-110">Valitse **Tili**-kentässä asiakas, jolle maksu kirjataan.</span><span class="sxs-lookup"><span data-stu-id="72cd7-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="72cd7-111">Syötä **Kredit**-kenttään maksun summa.</span><span class="sxs-lookup"><span data-stu-id="72cd7-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="72cd7-112">Voit jättää summan tyhjäksi, jolloin järjestelmä laskee sen valitsemalla maksetut laskut.</span><span class="sxs-lookup"><span data-stu-id="72cd7-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="72cd7-113">Syötä **Maksuviite**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="72cd7-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="72cd7-114">Maksuviite voi olla syöttämäsi maksun sekkinumero.</span><span class="sxs-lookup"><span data-stu-id="72cd7-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="72cd7-115">Maksuviite vaaditaan, jotta maksu voidaan sisällyttää talletuskuittiin.</span><span class="sxs-lookup"><span data-stu-id="72cd7-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="72cd7-116">Valitse Käytä talletuskuittia -kohta.</span><span class="sxs-lookup"><span data-stu-id="72cd7-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="72cd7-117">Jos maksu halutaan sisällyttää talletukseen, muuta tämän asetuksen arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="72cd7-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="72cd7-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-118">Select **New**.</span></span>
10. <span data-ttu-id="72cd7-119">Valitse **Tili**-kentässä asiakas seuraa maksua varten.</span><span class="sxs-lookup"><span data-stu-id="72cd7-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="72cd7-120">Syötä **Kredit**-kenttään maksun summa.</span><span class="sxs-lookup"><span data-stu-id="72cd7-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="72cd7-121">Syötä **Maksuviite**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="72cd7-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="72cd7-122">Valitse **Käytä talletuskuittia** -kohta.</span><span class="sxs-lookup"><span data-stu-id="72cd7-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="72cd7-123">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-123">Select **Post**.</span></span> <span data-ttu-id="72cd7-124">Maksut on kirjattava, ennen kuin talletuskuitti luodaan.</span><span class="sxs-lookup"><span data-stu-id="72cd7-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="72cd7-125">Näin varmistetaan, että maksut eivät muutu talletuskuitin luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="72cd7-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="72cd7-126">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-126">Select **Functions**.</span></span>
16. <span data-ttu-id="72cd7-127">Valitse **Talletuskuitti**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="72cd7-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-128">Select **OK**.</span></span> <span data-ttu-id="72cd7-129">Ensimmäisellä sivulla luodaan talletuskuitti.</span><span class="sxs-lookup"><span data-stu-id="72cd7-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="72cd7-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="72cd7-130">Select **OK**.</span></span> <span data-ttu-id="72cd7-131">Toisessa vaiheessa talletuskuitti tulostetaan. Tämä vaihe ei kuitenkaan ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="72cd7-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

