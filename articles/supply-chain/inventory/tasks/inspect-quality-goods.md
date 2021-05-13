---
title: Tarkista tavaroiden laatu
description: Tässä ohjeaiheessa kerrotaan, kuinka laatutilauksia käsitellään.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956131"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="e1b31-103">Tarkista tavaroiden laatu</span><span class="sxs-lookup"><span data-stu-id="e1b31-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1b31-104">Tässä ohjeaiheessa kerrotaan, kuinka laatutilauksia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="e1b31-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="e1b31-105">Laatuassistentti suorittaa yleensä laatutarkastukset.</span><span class="sxs-lookup"><span data-stu-id="e1b31-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="e1b31-106">Jos vakioesittely on asennettu, voit suorittaa sen avulla tässä ohjeaiheessa olevat toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="e1b31-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="e1b31-107">Valitse *USMF*-yritys ennen kuin aloitat, jotta voit käyttää esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="e1b31-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="e1b31-108">Sen jälkeen on vahvistettava ostotilaus *000016* ja kirjattava tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="e1b31-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="e1b31-109">Laatutilaus luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e1b31-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="e1b31-110">Vaihe 1: Valitse laatutilaus</span><span class="sxs-lookup"><span data-stu-id="e1b31-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="e1b31-111">Voit luoda laatutilauksen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e1b31-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="e1b31-112">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="e1b31-113">Valitse ennen tämän menettelyn aloittamista luotu laatutilaus.</span><span class="sxs-lookup"><span data-stu-id="e1b31-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="e1b31-114">Vaihe 2: Testitulosten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="e1b31-114">Step 2: Record test results</span></span>

<span data-ttu-id="e1b31-115">Voit tallentaa testitulokset noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e1b31-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="e1b31-116">Valitse **Tulokset**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-116">Select **Results**.</span></span>
1. <span data-ttu-id="e1b31-117">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-117">Select **Edit**.</span></span>
1. <span data-ttu-id="e1b31-118">Syötä numero **Tulosmäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1b31-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="e1b31-119">Etsi haluamasi tietue **Tulos**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="e1b31-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="e1b31-120">Tässä esimerkissä tulos perustuu ennalta määritettyyn tulokseen.</span><span class="sxs-lookup"><span data-stu-id="e1b31-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="e1b31-121">Yleensä tallennetaan yksityiskohtaisempia testituloksia, kuten esimerkiksi koko tai muu dimensio.</span><span class="sxs-lookup"><span data-stu-id="e1b31-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="e1b31-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-122">Select **Save**.</span></span>
1. <span data-ttu-id="e1b31-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b31-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="e1b31-124">Vaihe 3: Vahvista laatutilaus</span><span class="sxs-lookup"><span data-stu-id="e1b31-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="e1b31-125">Voit vahvistaa laatutilauksen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e1b31-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="e1b31-126">Valitse **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-126">Select **Validate**.</span></span>
1. <span data-ttu-id="e1b31-127">Valitse **Vahvistaja**-kentästä tarkastuksen tehnyt käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="e1b31-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="e1b31-128">Valitse **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-128">Select **Select**.</span></span>
1. <span data-ttu-id="e1b31-129">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1b31-129">Select **OK**.</span></span>
1. <span data-ttu-id="e1b31-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b31-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
