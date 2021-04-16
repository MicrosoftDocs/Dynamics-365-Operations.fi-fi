---
title: Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet
description: Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812059"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="31d3e-103">Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet</span><span class="sxs-lookup"><span data-stu-id="31d3e-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31d3e-104">Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.</span><span class="sxs-lookup"><span data-stu-id="31d3e-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="31d3e-105">Siinä esitellään myös pyyntötyypin käyttäminen tarjouspyynnössä, jolla asetetaan oletuspisteytysmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="31d3e-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="31d3e-106">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="31d3e-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="31d3e-107">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="31d3e-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="31d3e-108">Tarvitset käytettävän pisteytysmenetelmän ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="31d3e-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="31d3e-109">Luo pyyntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="31d3e-109">Create a solicitation type</span></span>
1. <span data-ttu-id="31d3e-110">Siirry kohtaan Hankinta > Asetukset > Tarjouspyyntö > Pyyntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="31d3e-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="31d3e-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="31d3e-111">Click New.</span></span>
3. <span data-ttu-id="31d3e-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31d3e-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="31d3e-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="31d3e-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31d3e-114">Valitse Pisteytysmenetelmä-kentästä menetelmä, jota haluat käyttää kyseisellä pyyntötyypillä.</span><span class="sxs-lookup"><span data-stu-id="31d3e-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="31d3e-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="31d3e-115">Click Save.</span></span>
7. <span data-ttu-id="31d3e-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="31d3e-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="31d3e-117">Käytä pyyntötyyppiä</span><span class="sxs-lookup"><span data-stu-id="31d3e-117">Use the solicitation type</span></span>
1. <span data-ttu-id="31d3e-118">Valitse Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt.</span><span class="sxs-lookup"><span data-stu-id="31d3e-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="31d3e-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="31d3e-119">Click New.</span></span>
3. <span data-ttu-id="31d3e-120">Valitse Pyyntö-kentässä juuri luomasi pyyntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="31d3e-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="31d3e-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31d3e-121">Click OK.</span></span>
5. <span data-ttu-id="31d3e-122">Valitse Pisteytysehdot.</span><span class="sxs-lookup"><span data-stu-id="31d3e-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="31d3e-123">Esitetyt pisteytysperusteet ovat peräisin on pyyntöön liittämästäsi pisteytysmenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="31d3e-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="31d3e-124">Voit halutessasi lisätä tai poistaa perusteita tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="31d3e-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="31d3e-125">On myös mahdollista lisätä uusia perusteita kopioimalla ne muista pisteytysmenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="31d3e-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="31d3e-126">Napsauta Kopioi ehdot -painiketta.</span><span class="sxs-lookup"><span data-stu-id="31d3e-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="31d3e-127">Anna tai valitse arvo Pisteytysmenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="31d3e-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="31d3e-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31d3e-128">Click OK.</span></span>
9. <span data-ttu-id="31d3e-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="31d3e-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]