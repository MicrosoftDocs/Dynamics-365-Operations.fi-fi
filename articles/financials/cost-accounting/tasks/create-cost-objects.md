--- 
title: Kustannusobjektien luominen
description: "Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operationsin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 21fa90557b665e0777935cc6bae8cd9f1c29cb60
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="2769e-103">Kustannusobjektien luominen</span><span class="sxs-lookup"><span data-stu-id="2769e-103">Create cost objects</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2769e-104">Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operationsin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="2769e-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="2769e-105">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="2769e-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="2769e-106">Nämä ohjeet koskevat kustannuslaskentatoimintoa, joka lisättiin Dynamics 365 for Operationsin versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="2769e-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="2769e-107">Luo uudet kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="2769e-107">Create new cost objects</span></span>
1. <span data-ttu-id="2769e-108">Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="2769e-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="2769e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2769e-109">Click New.</span></span>
3. <span data-ttu-id="2769e-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2769e-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2769e-111">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2769e-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="2769e-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2769e-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2769e-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2769e-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="2769e-114">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="2769e-114">Configure the data connector</span></span>
1. <span data-ttu-id="2769e-115">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="2769e-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="2769e-116">Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="2769e-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="2769e-117">Valitse Dimension nimi -kentässä Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="2769e-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="2769e-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2769e-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="2769e-119">Tuo kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="2769e-119">Import cost centers</span></span>
1. <span data-ttu-id="2769e-120">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="2769e-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="2769e-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2769e-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="2769e-122">Näytä tuodut kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="2769e-122">View the imported cost centers</span></span>
1. <span data-ttu-id="2769e-123">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="2769e-123">Click View dimension members.</span></span>


