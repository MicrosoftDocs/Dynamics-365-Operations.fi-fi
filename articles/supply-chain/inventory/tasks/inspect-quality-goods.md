---
title: Tarkista tavaroiden laatu
description: Tässä ohjeaiheessa kerrotaan, kuinka laatutilaus käsitellään.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855683"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="54430-103">Tarkista tavaroiden laatu</span><span class="sxs-lookup"><span data-stu-id="54430-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54430-104">Tässä ohjeaiheessa kerrotaan, kuinka laatutilaus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="54430-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="54430-105">Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="54430-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="54430-106">Vahvista ostotilaus 000016 ennen tämän esimerkin menettelyn aloittamista ja kirjaa tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="54430-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="54430-107">Tällöin laatutilaus luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="54430-107">This will automatically create a quality order.</span></span> <span data-ttu-id="54430-108">Laatuassistentti suorittaa yleensä laatutarkastukset.</span><span class="sxs-lookup"><span data-stu-id="54430-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="54430-109">Valitse laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="54430-109">Select a quality order</span></span>
1. <span data-ttu-id="54430-110">Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Laadunhallinta > Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="54430-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="54430-111">Valitse ennen tämän menettelyn aloittamista luotu laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="54430-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="54430-112">Testitulosten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="54430-112">Record test results</span></span>
1. <span data-ttu-id="54430-113">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="54430-113">Select **Results**.</span></span>
2. <span data-ttu-id="54430-114">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="54430-114">Select **Edit**.</span></span>
3. <span data-ttu-id="54430-115">Syötä numero **Tulosmäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54430-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="54430-116">Valitse **Tulos**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="54430-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="54430-117">Tässä esimerkissä tulos perustuu ennalta määritettyyn tulokseen.</span><span class="sxs-lookup"><span data-stu-id="54430-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="54430-118">Yleensä tallennetaan yksityiskohtaisempia testituloksia, kuten esimerkiksi koko tai muu dimensio.</span><span class="sxs-lookup"><span data-stu-id="54430-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="54430-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="54430-119">Select **Save**.</span></span>
6. <span data-ttu-id="54430-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54430-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="54430-121">Vahvista laatutilaus</span><span class="sxs-lookup"><span data-stu-id="54430-121">Validate the quality order</span></span>
1. <span data-ttu-id="54430-122">Valitse **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="54430-122">Select **Validate**.</span></span>
2. <span data-ttu-id="54430-123">Valitse **Vahvistaja**-kentässä avattavasta valikosta käyttäjä, joka suorittaa tarkastuksen.</span><span class="sxs-lookup"><span data-stu-id="54430-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="54430-124">Klikkaa **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="54430-124">Click **Select**.</span></span>
4. <span data-ttu-id="54430-125">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="54430-125">Select **OK**.</span></span>
5. <span data-ttu-id="54430-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54430-126">Close the page.</span></span>

