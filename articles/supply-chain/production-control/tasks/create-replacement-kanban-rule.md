--- 
title: "Luo korvaava kanban-sääntö"
description: "Tämän menetelmä keskittyy korvaamaan vanhoja kanban-sääntöjä uusilla säännöillä tiettynä päivämääränä."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5b27200a8d56192d473887f01076eced0f92e4c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="7dfb0-103">Luo korvaava kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="7dfb0-103">Create a replacement kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7dfb0-104">Tämän menetelmä keskittyy korvaamaan vanhoja kanban-sääntöjä uusilla säännöillä tiettynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="7dfb0-105">Tästä on hyötyä, kun muutoksia tuotantovirtaan tai täydennyssääntöihin on koordinoitava ja ajoitettava.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="7dfb0-106">Tämän menettelyn luonnissa käytettiin esittely-yrityksenä USMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="7dfb0-107">Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle muutetun tuotantovirran tai uuden täydennyssäännön tuotannon valmisteluun.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="7dfb0-108">Tämän tehtävä korvaa kanban-säännön 000022 uudella säännöllä ja nostaa enimmäismäärän 48:sta 100:an uudessa säännössä.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="7dfb0-109">Valitse korvattava kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="7dfb0-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="7dfb0-110">Valitse Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7dfb0-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7dfb0-112">Valitse kanban-sääntö 000022.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="7dfb0-113">Luo korvaava kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="7dfb0-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="7dfb0-114">Napsauta kohtaa Korvaa kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="7dfb0-115">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="7dfb0-116">Valitse tuleva päivämäärä, esimerkiksi viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="7dfb0-117">Tämä on päivämäärä ja aika, jona uusi kanban-sääntö aktivoituu ja korvaa vanhan kanban-säännön.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="7dfb0-118">Jos kanban-sääntö muuttaa polkua tuotantovirrassa, toisen tehtävän voi valita.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="7dfb0-119">Näissä toimintaohjeissa on tehtävää ei muuteta.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="7dfb0-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-120">Click OK.</span></span>
    * <span data-ttu-id="7dfb0-121">Huomaa, että kanban-sääntö 000022 korvataan uudella kanban-säännöllä.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="7dfb0-122">Voimaantulopäivä määritetään kanban-sääntöä korvatessa valitun päivämäärän mukaan.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="7dfb0-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7dfb0-124">Valitse korvattu kanban-sääntö 000022.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="7dfb0-125">Huomaa, että korvatulla kanban-säännöllä on sama päivämäärä kuin päättymispäivämäärä, sillä tämä on päivämäärä, jona se vanhenee.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="7dfb0-126">Valitse luettelosta rivi 1.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="7dfb0-127">Valitse uusi kanban-sääntö luettelon alusta.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="7dfb0-128">Tällä kanban-säännölle on suurin kanban-säännön numero.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="7dfb0-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7dfb0-130">Avaa kanban-sääntö napsauttamalla sen numeroa.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="7dfb0-131">Muokkaa korvaavan kanban-säännön enimmäismäärää</span><span class="sxs-lookup"><span data-stu-id="7dfb0-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="7dfb0-132">Määritä Enimmäismäärä-arvoksi 100.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="7dfb0-133">Laajenna Määrät-pikavälilehti nähdäksesi Suurin määrä -kentän.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="7dfb0-134">Jos muutat enimmäismääräksi 100, voit käsitellä enintään 100:a kanbania.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="7dfb0-135">Tämä on tämän tehtävän viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-135">This is the last step in this task.</span></span>  


