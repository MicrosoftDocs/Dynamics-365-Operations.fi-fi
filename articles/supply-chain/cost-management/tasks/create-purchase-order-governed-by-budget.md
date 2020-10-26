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
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 319eb0070a3677035e2a5d89744e80cd38c08d8e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980504"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="bcdfe-103">Ostotilauksen luonti budjetin mukaan</span><span class="sxs-lookup"><span data-stu-id="bcdfe-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcdfe-104">Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="bcdfe-105">Tämä tallenne käyttää esittelytietojen USMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="bcdfe-106">Budjetin hallinnan konfiguraation tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="bcdfe-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="bcdfe-107">Valitse Budjetointi > Asetukset > Budjetin hallinta > Budjetin hallinnan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="bcdfe-108">Valitse Käytettävissä olevat budjettivarat -välilehti.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="bcdfe-109">Valitse Tiedostot ja kirjauskansiot -välilehti.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="bcdfe-110">Valitse Määritä budjetin hallintasäännöt -välilehti.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="bcdfe-111">Valitse Määritä budjettiryhmät -välilehti.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="bcdfe-112">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="bcdfe-113">Luo ostotilauksen otsikko</span><span class="sxs-lookup"><span data-stu-id="bcdfe-113">Create the purchase order header</span></span>
1. <span data-ttu-id="bcdfe-114">Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="bcdfe-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-115">Click New.</span></span>
3. <span data-ttu-id="bcdfe-116">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="bcdfe-117">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-117">Expand the General section.</span></span>
5. <span data-ttu-id="bcdfe-118">Määritä Kirjauspäivä-kentässä päivämääräksi 1.1.2016.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="bcdfe-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="bcdfe-120">Ostotilausrivin lisääminen</span><span class="sxs-lookup"><span data-stu-id="bcdfe-120">Add a purchase order line</span></span>
1. <span data-ttu-id="bcdfe-121">Kirjoita tai valitse arvo Hankintaluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="bcdfe-122">Määritä Määrä-kenttään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="bcdfe-123">Syötä tai valitse arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="bcdfe-124">Aseta yksikköhinnaksi 10 000.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="bcdfe-125">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-125">Click Financials.</span></span>
6. <span data-ttu-id="bcdfe-126">Valitse Jaa summat.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="bcdfe-127">Määritä Kirjanpitotili-kentässä haluamasi arvo 601300-001-023--.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="bcdfe-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="bcdfe-129">Tarkista budjetti</span><span class="sxs-lookup"><span data-stu-id="bcdfe-129">Perform budget checking</span></span>
1. <span data-ttu-id="bcdfe-130">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-130">Click Financials.</span></span>
2. <span data-ttu-id="bcdfe-131">Valitse Tarkista budjetti.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="bcdfe-132">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-132">Click Financials.</span></span>
4. <span data-ttu-id="bcdfe-133">Valitse Budjetin tarkistusvirheet tai -varoitukset.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="bcdfe-134">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="bcdfe-134">Click Close.</span></span>

