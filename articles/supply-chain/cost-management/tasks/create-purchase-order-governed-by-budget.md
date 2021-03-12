---
title: Ostotilauksen luonti budjetin mukaan
description: Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbfbbef3bd7c7398f0f17b6cddbbff8c4755638d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963710"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="646e0-103">Ostotilauksen luonti budjetin mukaan</span><span class="sxs-lookup"><span data-stu-id="646e0-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="646e0-104">Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="646e0-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="646e0-105">Tämä tallenne käyttää esittelytietojen USMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="646e0-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="646e0-106">Budjetin hallinnan konfiguraation tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="646e0-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="646e0-107">Valitse Budjetointi > Asetukset > Budjetin hallinta > Budjetin hallinnan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="646e0-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="646e0-108">Valitse Käytettävissä olevat budjettivarat -välilehti.</span><span class="sxs-lookup"><span data-stu-id="646e0-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="646e0-109">Valitse Tiedostot ja kirjauskansiot -välilehti.</span><span class="sxs-lookup"><span data-stu-id="646e0-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="646e0-110">Valitse Määritä budjetin hallintasäännöt -välilehti.</span><span class="sxs-lookup"><span data-stu-id="646e0-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="646e0-111">Valitse Määritä budjettiryhmät -välilehti.</span><span class="sxs-lookup"><span data-stu-id="646e0-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="646e0-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="646e0-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="646e0-113">Luo ostotilauksen otsikko</span><span class="sxs-lookup"><span data-stu-id="646e0-113">Create the purchase order header</span></span>
1. <span data-ttu-id="646e0-114">Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="646e0-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="646e0-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="646e0-115">Click New.</span></span>
3. <span data-ttu-id="646e0-116">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="646e0-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="646e0-117">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="646e0-117">Expand the General section.</span></span>
5. <span data-ttu-id="646e0-118">Määritä Kirjauspäivä-kentässä päivämääräksi 1.1.2016.</span><span class="sxs-lookup"><span data-stu-id="646e0-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="646e0-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="646e0-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="646e0-120">Ostotilausrivin lisääminen</span><span class="sxs-lookup"><span data-stu-id="646e0-120">Add a purchase order line</span></span>
1. <span data-ttu-id="646e0-121">Kirjoita tai valitse arvo Hankintaluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="646e0-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="646e0-122">Määritä Määrä-kenttään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="646e0-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="646e0-123">Syötä tai valitse arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="646e0-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="646e0-124">Aseta yksikköhinnaksi 10 000.</span><span class="sxs-lookup"><span data-stu-id="646e0-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="646e0-125">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="646e0-125">Click Financials.</span></span>
6. <span data-ttu-id="646e0-126">Valitse Jaa summat.</span><span class="sxs-lookup"><span data-stu-id="646e0-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="646e0-127">Määritä Kirjanpitotili-kentässä haluamasi arvo 601300-001-023--.</span><span class="sxs-lookup"><span data-stu-id="646e0-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="646e0-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="646e0-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="646e0-129">Tarkista budjetti</span><span class="sxs-lookup"><span data-stu-id="646e0-129">Perform budget checking</span></span>
1. <span data-ttu-id="646e0-130">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="646e0-130">Click Financials.</span></span>
2. <span data-ttu-id="646e0-131">Valitse Tarkista budjetti.</span><span class="sxs-lookup"><span data-stu-id="646e0-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="646e0-132">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="646e0-132">Click Financials.</span></span>
4. <span data-ttu-id="646e0-133">Valitse Budjetin tarkistusvirheet tai -varoitukset.</span><span class="sxs-lookup"><span data-stu-id="646e0-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="646e0-134">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="646e0-134">Click Close.</span></span>

