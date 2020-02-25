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
ms.openlocfilehash: e38f52d961c27c3b12cdef448c85b1ac3f1d9e34
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008913"
---
# <a name="loan-item-to-a-worker"></a><span data-ttu-id="2754e-103">Lainaa kohde työntekijälle</span><span class="sxs-lookup"><span data-stu-id="2754e-103">Loan item to a worker</span></span>



<span data-ttu-id="2754e-104">Tässä menettelyssä kerrotaan, miten kohde lainataan työntekijälle sekä se, miten työntekijän tekemä kohteen palautus tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="2754e-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="2754e-105">Työntekijät voivat pyytää lainan kohteita myös Työntekijän itsepalvelu -sivujen kautta.</span><span class="sxs-lookup"><span data-stu-id="2754e-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="2754e-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="2754e-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="2754e-107">Lainaa kohde työntekijälle</span><span class="sxs-lookup"><span data-stu-id="2754e-107">Loan item to a worker</span></span>
1. <span data-ttu-id="2754e-108">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatut laitteet.</span><span class="sxs-lookup"><span data-stu-id="2754e-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="2754e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2754e-109">Click New.</span></span>
3. <span data-ttu-id="2754e-110">Syötä tai valitse arvo Henkilö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2754e-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="2754e-111">Anna tai valitse arvo Lainanimike-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2754e-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="2754e-112">Syötä Suunniteltu palautus -kenttään päivämäärä, jolloin työntekijän on palautettava lainan kohde.</span><span class="sxs-lookup"><span data-stu-id="2754e-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="2754e-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2754e-113">Click Save.</span></span>
7. <span data-ttu-id="2754e-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2754e-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="2754e-115">Lainan kohteen palauttaminen</span><span class="sxs-lookup"><span data-stu-id="2754e-115">Return a loan item</span></span>
1. <span data-ttu-id="2754e-116">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatut laitteet.</span><span class="sxs-lookup"><span data-stu-id="2754e-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="2754e-117">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2754e-117">Click Edit.</span></span>
3. <span data-ttu-id="2754e-118">Syötä Todellinen palautuspvm -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="2754e-118">In the Actual return field, enter a date.</span></span>

