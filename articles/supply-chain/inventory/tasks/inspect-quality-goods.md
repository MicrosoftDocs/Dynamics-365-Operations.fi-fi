---
title: Tarkista tavaroiden laatu
description: Tässä menettelyssä näytetään, miten laatutilaus käsitellään.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "315426"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="0bc25-103">Tarkista tavaroiden laatu</span><span class="sxs-lookup"><span data-stu-id="0bc25-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0bc25-104">Tässä menettelyssä näytetään, miten laatutilaus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="0bc25-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="0bc25-105">Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="0bc25-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="0bc25-106">Vahvista ostotilaus 000016 ennen tämän esimerkin menettelyn aloittamista ja kirjaa tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="0bc25-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="0bc25-107">Tällöin laatutilaus luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0bc25-107">This will automatically create a quality order.</span></span> <span data-ttu-id="0bc25-108">Laatuassistentti suorittaa yleensä laatutarkastukset.</span><span class="sxs-lookup"><span data-stu-id="0bc25-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="0bc25-109">Valitse laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="0bc25-109">Select a quality order</span></span>
1. <span data-ttu-id="0bc25-110">Valitse Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Laadunhallinta > Laatutilaukset.</span><span class="sxs-lookup"><span data-stu-id="0bc25-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="0bc25-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0bc25-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0bc25-112">Valitse ennen tämän menettelyn aloittamista luotu laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="0bc25-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="0bc25-113">Testitulosten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="0bc25-113">Record test results</span></span>
1. <span data-ttu-id="0bc25-114">Valitse Tulos.</span><span class="sxs-lookup"><span data-stu-id="0bc25-114">Click Results.</span></span>
2. <span data-ttu-id="0bc25-115">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0bc25-115">Click Edit.</span></span>
3. <span data-ttu-id="0bc25-116">Syötä numero Tulosmäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0bc25-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="0bc25-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0bc25-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="0bc25-118">Avaa haku valitsemalla Tulos-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0bc25-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0bc25-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0bc25-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0bc25-120">Tässä esimerkissä tulos perustuu ennalta määritettyyn tulokseen.</span><span class="sxs-lookup"><span data-stu-id="0bc25-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="0bc25-121">Yleensä tallennetaan yksityiskohtaisempia testituloksia, kuten esimerkiksi koko tai muu dimensio.</span><span class="sxs-lookup"><span data-stu-id="0bc25-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="0bc25-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0bc25-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0bc25-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0bc25-123">Click Save.</span></span>
9. <span data-ttu-id="0bc25-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0bc25-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="0bc25-125">Vahvista laatutilaus</span><span class="sxs-lookup"><span data-stu-id="0bc25-125">Validate the quality order</span></span>
1. <span data-ttu-id="0bc25-126">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="0bc25-126">Click Validate.</span></span>
2. <span data-ttu-id="0bc25-127">Avaa haku valitsemalla Vahvistaja-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0bc25-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0bc25-128">Valitse tarkastuksen suorittava käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="0bc25-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="0bc25-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0bc25-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0bc25-130">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="0bc25-130">Click Select.</span></span>
5. <span data-ttu-id="0bc25-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0bc25-131">Click OK.</span></span>
6. <span data-ttu-id="0bc25-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0bc25-132">Close the page.</span></span>

