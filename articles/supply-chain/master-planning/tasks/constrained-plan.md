---
title: Rajoitetun suunnitelman luominen
description: Tässä aiheessa kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cc44876938074e72526e75f0df5c119cbcfd845
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213420"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="848ea-103">Rajoitetun suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="848ea-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="848ea-104">Tässä aiheessa kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.</span><span class="sxs-lookup"><span data-stu-id="848ea-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="848ea-105">Suunnitelma varmistaa, että valmistus aloitetaan vasta sitten, kun materiaalit ovat käytettävissä. Se myös estää resurssien ylivaraamisen.</span><span class="sxs-lookup"><span data-stu-id="848ea-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="848ea-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="848ea-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="848ea-107">Tämä menettely on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="848ea-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="848ea-108">Rajoitetun suunnitelman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="848ea-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="848ea-109">Valitse aloitussivulla **Pääsuunnittelu**-työtila.</span><span class="sxs-lookup"><span data-stu-id="848ea-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="848ea-110">Valitse **Pääsuunnitelmat** työtilan äärimmäisenä oikealla puolella olevasta linkkiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="848ea-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="848ea-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="848ea-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="848ea-112">Esimerkki: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="848ea-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="848ea-113">Valitse **Rajallinen kapasiteetti** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="848ea-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="848ea-114">Syötä **Rajallisen kapasiteetin aikaraja** -kenttään `30`.</span><span class="sxs-lookup"><span data-stu-id="848ea-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="848ea-115">Laajenna **Aikarajat päivissä** -osa.</span><span class="sxs-lookup"><span data-stu-id="848ea-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="848ea-116">Valitse **Kapasiteetti**-kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="848ea-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="848ea-117">Syötä **Kapasiteetin aikataulutuksen aikaraja (päivää)** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="848ea-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="848ea-118">Esimerkki: `60`</span><span class="sxs-lookup"><span data-stu-id="848ea-118">Example: `60`</span></span>  
9. <span data-ttu-id="848ea-119">Valitse **Lasketut viiveet** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="848ea-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="848ea-120">Syötä **Laskettujen viiveiden aikaraja (päivää)** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="848ea-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="848ea-121">Esimerkki: `60`</span><span class="sxs-lookup"><span data-stu-id="848ea-121">Example: `60`</span></span> 
11. <span data-ttu-id="848ea-122">Laajenna **Lasketut viiveet** -osa.</span><span class="sxs-lookup"><span data-stu-id="848ea-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="848ea-123">Valitse kaikissa **Lisää laskettu viive tarvepäivämäärään** -kentissä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="848ea-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="848ea-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="848ea-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="848ea-125">Rajoitetun suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="848ea-125">Create a constrained plan</span></span>
1. <span data-ttu-id="848ea-126">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="848ea-126">Select **Run**.</span></span>
2. <span data-ttu-id="848ea-127">Kirjoita tai valitse **Pääsuunnitelma**-kentässä suunnitelma, jolle olet määrittänyt rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="848ea-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="848ea-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="848ea-128">Select **OK**.</span></span>
4. <span data-ttu-id="848ea-129">Valitse **Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="848ea-129">Select **Planned orders**.</span></span>

