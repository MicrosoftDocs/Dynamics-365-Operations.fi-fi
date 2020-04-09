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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142314"
---
# <a name="create-cost-objects"></a><span data-ttu-id="8b121-103">Kustannusobjektien luominen</span><span class="sxs-lookup"><span data-stu-id="8b121-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b121-104">Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="8b121-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="8b121-105">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="8b121-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="8b121-106">Luo uudet kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="8b121-106">Create new cost objects</span></span>
1. <span data-ttu-id="8b121-107">Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="8b121-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="8b121-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b121-108">Click New.</span></span>
3. <span data-ttu-id="8b121-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b121-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8b121-110">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8b121-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="8b121-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b121-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8b121-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8b121-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="8b121-113">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="8b121-113">Configure the data connector</span></span>
1. <span data-ttu-id="8b121-114">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="8b121-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="8b121-115">Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="8b121-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="8b121-116">Valitse Dimension nimi -kentässä Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="8b121-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="8b121-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8b121-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="8b121-118">Tuo kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="8b121-118">Import cost centers</span></span>
1. <span data-ttu-id="8b121-119">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="8b121-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="8b121-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8b121-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="8b121-121">Näytä tuodut kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="8b121-121">View the imported cost centers</span></span>
1. <span data-ttu-id="8b121-122">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="8b121-122">Click View dimension members.</span></span>

