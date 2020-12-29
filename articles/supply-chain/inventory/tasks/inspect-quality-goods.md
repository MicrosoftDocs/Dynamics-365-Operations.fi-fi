---
title: Tarkista tavaroiden laatu
description: Tässä ohjeaiheessa kerrotaan, kuinka laatutilaus käsitellään.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee5f83b2dad60567341f33a73ce63d01e9da8289
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427334"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="1056e-103">Tarkista tavaroiden laatu</span><span class="sxs-lookup"><span data-stu-id="1056e-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1056e-104">Tässä ohjeaiheessa kerrotaan, kuinka laatutilaus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="1056e-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="1056e-105">Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1056e-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="1056e-106">Vahvista ostotilaus 000016 ennen tämän esimerkin menettelyn aloittamista ja kirjaa tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="1056e-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="1056e-107">Tällöin laatutilaus luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1056e-107">This will automatically create a quality order.</span></span> <span data-ttu-id="1056e-108">Laatuassistentti suorittaa yleensä laatutarkastukset.</span><span class="sxs-lookup"><span data-stu-id="1056e-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="1056e-109">Valitse laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="1056e-109">Select a quality order</span></span>
1. <span data-ttu-id="1056e-110">Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Laadunhallinta > Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="1056e-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="1056e-111">Valitse ennen tämän menettelyn aloittamista luotu laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="1056e-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="1056e-112">Testitulosten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="1056e-112">Record test results</span></span>
1. <span data-ttu-id="1056e-113">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="1056e-113">Select **Results**.</span></span>
2. <span data-ttu-id="1056e-114">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="1056e-114">Select **Edit**.</span></span>
3. <span data-ttu-id="1056e-115">Syötä numero **Tulosmäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1056e-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="1056e-116">Valitse **Tulos**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="1056e-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="1056e-117">Tässä esimerkissä tulos perustuu ennalta määritettyyn tulokseen.</span><span class="sxs-lookup"><span data-stu-id="1056e-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="1056e-118">Yleensä tallennetaan yksityiskohtaisempia testituloksia, kuten esimerkiksi koko tai muu dimensio.</span><span class="sxs-lookup"><span data-stu-id="1056e-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="1056e-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="1056e-119">Select **Save**.</span></span>
6. <span data-ttu-id="1056e-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1056e-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="1056e-121">Vahvista laatutilaus</span><span class="sxs-lookup"><span data-stu-id="1056e-121">Validate the quality order</span></span>
1. <span data-ttu-id="1056e-122">Valitse **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="1056e-122">Select **Validate**.</span></span>
2. <span data-ttu-id="1056e-123">Valitse **Vahvistaja**-kentässä avattavasta valikosta käyttäjä, joka suorittaa tarkastuksen.</span><span class="sxs-lookup"><span data-stu-id="1056e-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="1056e-124">Klikkaa **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="1056e-124">Click **Select**.</span></span>
4. <span data-ttu-id="1056e-125">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1056e-125">Select **OK**.</span></span>
5. <span data-ttu-id="1056e-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1056e-126">Close the page.</span></span>

