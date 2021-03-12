---
title: Kustannusobjektien luominen
description: Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990764"
---
# <a name="create-cost-objects"></a><span data-ttu-id="f3218-103">Kustannusobjektien luominen</span><span class="sxs-lookup"><span data-stu-id="f3218-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3218-104">Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="f3218-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="f3218-105">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="f3218-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="f3218-106">Luo uudet kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="f3218-106">Create new cost objects</span></span>
1. <span data-ttu-id="f3218-107">Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="f3218-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="f3218-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f3218-108">Click New.</span></span>
3. <span data-ttu-id="f3218-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3218-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f3218-110">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="f3218-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="f3218-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f3218-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f3218-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f3218-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="f3218-113">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="f3218-113">Configure the data connector</span></span>
1. <span data-ttu-id="f3218-114">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="f3218-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="f3218-115">Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="f3218-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="f3218-116">Valitse Dimension nimi -kentässä Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="f3218-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="f3218-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f3218-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="f3218-118">Tuo kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="f3218-118">Import cost centers</span></span>
1. <span data-ttu-id="f3218-119">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="f3218-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="f3218-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f3218-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="f3218-121">Näytä tuodut kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="f3218-121">View the imported cost centers</span></span>
1. <span data-ttu-id="f3218-122">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="f3218-122">Click View dimension members.</span></span>

