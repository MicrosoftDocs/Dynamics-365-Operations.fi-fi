---
title: Lainaa kohde työntekijälle
description: Tässä menettelyssä kerrotaan, miten kohde lainataan työntekijälle sekä se, miten työntekijän tekemä kohteen palautus tallennetaan.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPersonLoan, HcmPersonLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ea400c48058bc31ba5e4dfc187564da3bee527c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130154"
---
# <a name="loan-item-to-a-worker"></a><span data-ttu-id="d4933-103">Lainaa kohde työntekijälle</span><span class="sxs-lookup"><span data-stu-id="d4933-103">Loan item to a worker</span></span>



<span data-ttu-id="d4933-104">Tässä menettelyssä kerrotaan, miten kohde lainataan työntekijälle sekä se, miten työntekijän tekemä kohteen palautus tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="d4933-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="d4933-105">Työntekijät voivat pyytää lainan kohteita myös Työntekijän itsepalvelu -sivujen kautta.</span><span class="sxs-lookup"><span data-stu-id="d4933-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="d4933-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="d4933-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="d4933-107">Lainaa kohde työntekijälle</span><span class="sxs-lookup"><span data-stu-id="d4933-107">Loan item to a worker</span></span>
1. <span data-ttu-id="d4933-108">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatut laitteet.</span><span class="sxs-lookup"><span data-stu-id="d4933-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="d4933-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d4933-109">Click New.</span></span>
3. <span data-ttu-id="d4933-110">Syötä tai valitse arvo Henkilö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d4933-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="d4933-111">Anna tai valitse arvo Lainanimike-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d4933-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="d4933-112">Syötä Suunniteltu palautus -kenttään päivämäärä, jolloin työntekijän on palautettava lainan kohde.</span><span class="sxs-lookup"><span data-stu-id="d4933-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="d4933-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d4933-113">Click Save.</span></span>
7. <span data-ttu-id="d4933-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d4933-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="d4933-115">Lainan kohteen palauttaminen</span><span class="sxs-lookup"><span data-stu-id="d4933-115">Return a loan item</span></span>
1. <span data-ttu-id="d4933-116">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatut laitteet.</span><span class="sxs-lookup"><span data-stu-id="d4933-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="d4933-117">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d4933-117">Click Edit.</span></span>
3. <span data-ttu-id="d4933-118">Syötä Todellinen palautuspvm -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d4933-118">In the Actual return field, enter a date.</span></span>

