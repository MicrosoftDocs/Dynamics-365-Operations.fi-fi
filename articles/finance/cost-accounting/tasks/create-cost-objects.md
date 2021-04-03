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
ms.openlocfilehash: 91c25c52a2c6dc7f096a494577b361ff30406e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236791"
---
# <a name="create-cost-objects"></a><span data-ttu-id="c3b95-103">Kustannusobjektien luominen</span><span class="sxs-lookup"><span data-stu-id="c3b95-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3b95-104">Tässä menettelyssä käsitellään tapaa, jolla kustannusobjekteja luodaan tuomalla kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="c3b95-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="c3b95-105">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="c3b95-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="c3b95-106">Luo uudet kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="c3b95-106">Create new cost objects</span></span>
1. <span data-ttu-id="c3b95-107">Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c3b95-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="c3b95-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c3b95-108">Click New.</span></span>
3. <span data-ttu-id="c3b95-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3b95-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c3b95-110">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c3b95-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="c3b95-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c3b95-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c3b95-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c3b95-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="c3b95-113">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="c3b95-113">Configure the data connector</span></span>
1. <span data-ttu-id="c3b95-114">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="c3b95-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="c3b95-115">Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="c3b95-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="c3b95-116">Valitse Dimension nimi -kentässä Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="c3b95-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="c3b95-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c3b95-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="c3b95-118">Tuo kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="c3b95-118">Import cost centers</span></span>
1. <span data-ttu-id="c3b95-119">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="c3b95-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="c3b95-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c3b95-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="c3b95-121">Näytä tuodut kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="c3b95-121">View the imported cost centers</span></span>
1. <span data-ttu-id="c3b95-122">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="c3b95-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]