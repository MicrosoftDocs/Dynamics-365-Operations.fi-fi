---
title: Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet
description: Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14fd7d0bfa17427883f97c5e0a72044016d4965e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552575"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="c8398-103">Luo tarjouspyyntöjen pyyntötyypit ja pisteytysperusteet</span><span class="sxs-lookup"><span data-stu-id="c8398-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8398-104">Tässä oppaassa esitellään pyyntötyypin luominen ja sen liittäminen pisteytysmenetelmään.</span><span class="sxs-lookup"><span data-stu-id="c8398-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="c8398-105">Siinä esitellään myös pyyntötyypin käyttäminen tarjouspyynnössä, jolla asetetaan oletuspisteytysmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="c8398-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="c8398-106">Yleensä ostopäällikkö tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="c8398-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="c8398-107">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="c8398-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c8398-108">Tarvitset käytettävän pisteytysmenetelmän ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="c8398-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="c8398-109">Luo pyyntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="c8398-109">Create a solicitation type</span></span>
1. <span data-ttu-id="c8398-110">Siirry kohtaan Hankinta > Asetukset > Tarjouspyyntö > Pyyntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="c8398-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="c8398-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c8398-111">Click New.</span></span>
3. <span data-ttu-id="c8398-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c8398-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c8398-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c8398-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c8398-114">Valitse Pisteytysmenetelmä-kentästä menetelmä, jota haluat käyttää kyseisellä pyyntötyypillä.</span><span class="sxs-lookup"><span data-stu-id="c8398-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="c8398-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c8398-115">Click Save.</span></span>
7. <span data-ttu-id="c8398-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c8398-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="c8398-117">Käytä pyyntötyyppiä</span><span class="sxs-lookup"><span data-stu-id="c8398-117">Use the solicitation type</span></span>
1. <span data-ttu-id="c8398-118">Valitse Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt.</span><span class="sxs-lookup"><span data-stu-id="c8398-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="c8398-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c8398-119">Click New.</span></span>
3. <span data-ttu-id="c8398-120">Valitse Pyyntö-kentässä juuri luomasi pyyntötyyppi.</span><span class="sxs-lookup"><span data-stu-id="c8398-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="c8398-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8398-121">Click OK.</span></span>
5. <span data-ttu-id="c8398-122">Valitse Pisteytysehdot.</span><span class="sxs-lookup"><span data-stu-id="c8398-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="c8398-123">Esitetyt pisteytysperusteet ovat peräisin on pyyntöön liittämästäsi pisteytysmenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="c8398-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="c8398-124">Voit halutessasi lisätä tai poistaa perusteita tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="c8398-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="c8398-125">On myös mahdollista lisätä uusia perusteita kopioimalla ne muista pisteytysmenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="c8398-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="c8398-126">Napsauta Kopioi ehdot -painiketta.</span><span class="sxs-lookup"><span data-stu-id="c8398-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="c8398-127">Anna tai valitse arvo Pisteytysmenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c8398-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="c8398-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8398-128">Click OK.</span></span>
9. <span data-ttu-id="c8398-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c8398-129">Close the page.</span></span>

