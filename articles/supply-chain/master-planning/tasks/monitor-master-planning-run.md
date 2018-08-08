--- 
title: "Pääsuunnitteluajon valvonta"
description: "Tuotannon suunnittelija haluaa nähdä, onko pääsuunnitteluajo käynnissä."
author: ShylaThompson
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 94a78d79d86cd480528e96bde70b84f870e0e59c
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="9961a-103">Pääsuunnitteluajon valvonta</span><span class="sxs-lookup"><span data-stu-id="9961a-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9961a-104">Tuotannon suunnittelija haluaa nähdä, onko pääsuunnitteluajo käynnissä.</span><span class="sxs-lookup"><span data-stu-id="9961a-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="9961a-105">Käytä menettelyn täytössä USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="9961a-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="9961a-106">Pääsuunnittelun suorittaminen</span><span class="sxs-lookup"><span data-stu-id="9961a-106">Run master planning</span></span>
1. <span data-ttu-id="9961a-107">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="9961a-107">Click Master planning.</span></span>
    * <span data-ttu-id="9961a-108">Löydät tämän oletuskoontinäytöltä.</span><span class="sxs-lookup"><span data-stu-id="9961a-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="9961a-109">Anna tai valitse Suunnitelma-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9961a-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="9961a-110">Esimerkki: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="9961a-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="9961a-111">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="9961a-111">Click Run.</span></span>
4. <span data-ttu-id="9961a-112">Valitse Seuraa käsittelyaikaa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9961a-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="9961a-113">Jos tämä kenttä on jo valittu, voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="9961a-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="9961a-114">Syötä Säikeiden määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9961a-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="9961a-115">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="9961a-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9961a-116">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="9961a-116">Click Filter.</span></span>
8. <span data-ttu-id="9961a-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9961a-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9961a-118">Merkitse rivi, jossa Kenttä = Nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="9961a-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="9961a-119">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9961a-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="9961a-120">Esimerkki: T0001</span><span class="sxs-lookup"><span data-stu-id="9961a-120">Example: T0001</span></span>  
10. <span data-ttu-id="9961a-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9961a-121">Click OK.</span></span>
11. <span data-ttu-id="9961a-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9961a-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="9961a-123">Pääsuunnitteluajon valvonta</span><span class="sxs-lookup"><span data-stu-id="9961a-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="9961a-124">Valitse Historia.</span><span class="sxs-lookup"><span data-stu-id="9961a-124">Click History.</span></span>
2. <span data-ttu-id="9961a-125">Valitse Kyselyt.</span><span class="sxs-lookup"><span data-stu-id="9961a-125">Click Inquiries.</span></span>
3. <span data-ttu-id="9961a-126">Valitse Käsittelytehtävän kesto.</span><span class="sxs-lookup"><span data-stu-id="9961a-126">Click Process task duration.</span></span>
4. <span data-ttu-id="9961a-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9961a-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9961a-128">Saat kullekin nimikkeelle yhteenvedon jokaiseen suunnitteluvaiheeseen kuluneesta ajasta.</span><span class="sxs-lookup"><span data-stu-id="9961a-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


