---
title: Lainaa kohde työntekijälle
description: Tässä menettelyssä kerrotaan, miten kohde lainataan työntekijälle sekä se, miten työntekijän tekemä kohteen palautus tallennetaan.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPersonLoan, HcmPersonLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 000d589ed4c17d9259866daf69a5abe879c61e09
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177635"
---
# <a name="loan-item-to-a-worker"></a><span data-ttu-id="c1f53-103">Lainaa kohde työntekijälle</span><span class="sxs-lookup"><span data-stu-id="c1f53-103">Loan item to a worker</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1f53-104">Tässä menettelyssä kerrotaan, miten kohde lainataan työntekijälle sekä se, miten työntekijän tekemä kohteen palautus tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="c1f53-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="c1f53-105">Työntekijät voivat pyytää lainan kohteita myös Työntekijän itsepalvelu -sivujen kautta.</span><span class="sxs-lookup"><span data-stu-id="c1f53-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="c1f53-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="c1f53-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="c1f53-107">Lainaa kohde työntekijälle</span><span class="sxs-lookup"><span data-stu-id="c1f53-107">Loan item to a worker</span></span>
1. <span data-ttu-id="c1f53-108">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatut laitteet.</span><span class="sxs-lookup"><span data-stu-id="c1f53-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="c1f53-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c1f53-109">Click New.</span></span>
3. <span data-ttu-id="c1f53-110">Syötä tai valitse arvo Henkilö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1f53-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="c1f53-111">Anna tai valitse arvo Lainanimike-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1f53-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="c1f53-112">Syötä Suunniteltu palautus -kenttään päivämäärä, jolloin työntekijän on palautettava lainan kohde.</span><span class="sxs-lookup"><span data-stu-id="c1f53-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="c1f53-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c1f53-113">Click Save.</span></span>
7. <span data-ttu-id="c1f53-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c1f53-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="c1f53-115">Lainan kohteen palauttaminen</span><span class="sxs-lookup"><span data-stu-id="c1f53-115">Return a loan item</span></span>
1. <span data-ttu-id="c1f53-116">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatut laitteet.</span><span class="sxs-lookup"><span data-stu-id="c1f53-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="c1f53-117">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c1f53-117">Click Edit.</span></span>
3. <span data-ttu-id="c1f53-118">Syötä Todellinen palautuspvm -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="c1f53-118">In the Actual return field, enter a date.</span></span>

