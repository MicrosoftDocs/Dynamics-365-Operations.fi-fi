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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220248"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="ffffe-103">Talleta asiakkaan maksuja</span><span class="sxs-lookup"><span data-stu-id="ffffe-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffffe-104">Talleta asiakkaan maksut.</span><span class="sxs-lookup"><span data-stu-id="ffffe-104">Deposit customer payments.</span></span> <span data-ttu-id="ffffe-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="ffffe-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ffffe-106">Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Maksut > Maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="ffffe-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-107">Select **New**.</span></span>
3. <span data-ttu-id="ffffe-108">Valitse avattavasta **Nimi**-kentästä **CustPay**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="ffffe-109">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-109">Select **Lines**.</span></span>
5. <span data-ttu-id="ffffe-110">Valitse **Tili**-kentässä asiakas, jolle maksu kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ffffe-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="ffffe-111">Syötä **Kredit**-kenttään maksun summa.</span><span class="sxs-lookup"><span data-stu-id="ffffe-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="ffffe-112">Voit jättää summan tyhjäksi, jolloin järjestelmä laskee sen valitsemalla maksetut laskut.</span><span class="sxs-lookup"><span data-stu-id="ffffe-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="ffffe-113">Syötä **Maksuviite**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ffffe-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="ffffe-114">Maksuviite voi olla syöttämäsi maksun sekkinumero.</span><span class="sxs-lookup"><span data-stu-id="ffffe-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="ffffe-115">Maksuviite vaaditaan, jotta maksu voidaan sisällyttää talletuskuittiin.</span><span class="sxs-lookup"><span data-stu-id="ffffe-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="ffffe-116">Valitse Käytä talletuskuittia -kohta.</span><span class="sxs-lookup"><span data-stu-id="ffffe-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="ffffe-117">Jos maksu halutaan sisällyttää talletukseen, muuta tämän asetuksen arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="ffffe-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="ffffe-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-118">Select **New**.</span></span>
10. <span data-ttu-id="ffffe-119">Valitse **Tili**-kentässä asiakas seuraa maksua varten.</span><span class="sxs-lookup"><span data-stu-id="ffffe-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="ffffe-120">Syötä **Kredit**-kenttään maksun summa.</span><span class="sxs-lookup"><span data-stu-id="ffffe-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="ffffe-121">Syötä **Maksuviite**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ffffe-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="ffffe-122">Valitse **Käytä talletuskuittia** -kohta.</span><span class="sxs-lookup"><span data-stu-id="ffffe-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="ffffe-123">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-123">Select **Post**.</span></span> <span data-ttu-id="ffffe-124">Maksut on kirjattava, ennen kuin talletuskuitti luodaan.</span><span class="sxs-lookup"><span data-stu-id="ffffe-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="ffffe-125">Näin varmistetaan, että maksut eivät muutu talletuskuitin luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ffffe-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="ffffe-126">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-126">Select **Functions**.</span></span>
16. <span data-ttu-id="ffffe-127">Valitse **Talletuskuitti**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="ffffe-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-128">Select **OK**.</span></span> <span data-ttu-id="ffffe-129">Ensimmäisellä sivulla luodaan talletuskuitti.</span><span class="sxs-lookup"><span data-stu-id="ffffe-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="ffffe-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffffe-130">Select **OK**.</span></span> <span data-ttu-id="ffffe-131">Toisessa vaiheessa talletuskuitti tulostetaan. Tämä vaihe ei kuitenkaan ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="ffffe-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]